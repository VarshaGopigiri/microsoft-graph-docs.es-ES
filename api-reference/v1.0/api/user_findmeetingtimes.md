# <a name="user-findmeetingtimes"></a>user: findMeetingTimes
Busque sugerencias de hora de la reunión en función de la disponibilidad del organizador y los asistentes, y restricciones de hora o de ubicación especificadas como parámetros.

Si **findMeetingTimes** no puede devolver sugerencias de reunión, la respuesta podría indicar un motivo en la propiedad **emptySuggestionsReason**. Basándose en este valor, se pueden ajustar mejor los parámetros y llamar otra vez a **findMeetingTimes**.

**Nota**

En la actualidad, **findMeetingTimes** asume lo siguiente:

- Cualquier [asistente](../resources/attendee.md) que es una persona (en oposición a un recurso) es un asistente requerido. Por tanto, especifique `required` para una persona y `resource` para un recurso en al propiedad **type** correspondiente, como parte del parámetro de la colección **attendees**.
- Cualquier sugerencia de reunión se produce durante las horas de trabajo del organizador o un asistente. Puede omitir la especificación de la propiedad **activityDomain** de una [timeConstraint](../resources/timeConstraint.md). 


## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Calendars.Read.Shared* o *Calendars.ReadWrite.Shared*
## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /me/findMeetingTimes
POST /users/{id|userPrincipalName}/findMeetingTimes
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Valor|
|:---------------|:----------|
| Autorización  | <code> de portador|
| Prefer: outlook.timezone | Una cadena que representa una zona horaria concreta para la respuesta, por ejemplo, "Hora estándar del Pacífico". |


## <a name="request-body"></a>Cuerpo de solicitud
Todos los parámetros admitidos se enumeran a continuación. Dependiendo de su escenario, especifique un objeto JSON para cada uno de los parámetros necesarios en el cuerpo de la solicitud. Basándose en los parámetros especificados, **findMeetingTimes** comprueba el estado de disponibilidad en los calendarios principales del organizador y los asistentes. La acción calcula la mejor hora de la reunión posible y devuelve cualquier sugerencia de reunión.


| Parámetro       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|attendees|Colección [attendeeBase](../resources/attendeebase.md)|Una colección de los asistentes o los recursos de la reunión. Una colección vacía hace que **findMeetingTimes** busque intervalos de tiempo libres solo para el organizador.|
|locationConstraint|[locationConstraint](../resources/locationconstraint.md)|Los requisitos del organizador sobre la ubicación de la reunión, por ejemplo si se requiere una sugerencia para una ubicación de la reunión o si hay ubicaciones específicas en las que únicamente pueda tener lugar la reunión.|
|timeConstraint|[timeConstraint](../resources/timeconstraint.md)|El intervalo de la hora de inicio y finalización en el que debe producirse la reunión. Se puede especificar una zona horaria como parte de las **start** y **end** propiedades para este parámetro. Pero esta zona horaria solo afecta al parámetro **timeConstraint**. Los valores de hora devueltos en la respuesta, si existen, siguen en formato UTC de manera predeterminada. Se puede usar el encabezado de solicitud `Prefer: outlook.timezone` para especificar una zona horaria concreta para los valores de hora de la respuesta. |
|meetingDuration|Edm.Duration|La duración de la reunión, en formato [ISO8601](http://www.iso.org/iso/iso8601). Por ejemplo, 1 hora se indica como 'PT1H', donde 'P' es el designador de duración, 't' es el designador de tiempo y 'H' es el designador de hora. Si no se especifica ninguna duración de la reunión, **findMeetingTimes** usa el valor predeterminado de 30 minutos. |
|maxCandidates|Edm.Int32|El número máximo de sugerencias de hora de la reunión que se va a devolver.|
|isOrganizerOptional|Edm.Boolean|`True` si no es necesaria la asistencia del organizador o `false` en caso contrario.|
|returnSuggestionReasons|Edm.Boolean|`True` para devolver un motivo para cada sugerencia de la reunión en la propiedad **suggestionReason**. El valor predeterminado es `false` para no devolver esa propiedad.|
|minimumAttendeePercentage|Edm.Double| La [confianza](#the-confidence-of-a-meeting-suggestion) mínima necesaria para que se devuelva un intervalo de tiempo en la respuesta. Es un valor de porcentaje (%) comprendido entre 0 y 100. |

## <a name="response"></a>Respuesta
Si es correcto, este método devuelve un código de respuesta `200, OK` y un objeto [meetingTimeSuggestionsResult](../resources/meetingTimeSuggestionsResult.md) en el cuerpo de la respuesta. 

Un objeto **meetingTimeSuggestionsResult** incluye una colección de sugerencias de la reunión y una propiedad **emptySuggestionsReason**. Cada sugerencia se define como una [meetingTimeSuggestion](../resources/meetingTimeSuggestion.md), con los asistentes con un nivel de confianza medio del 50 % de asistir o un porcentaje concreto que especificó en el parámetro **minimumAttendeePercentage**. 

De forma predeterminada, cada sugerencia de hora de la reunión se devuelve en formato UTC. 

### <a name="the-confidence-of-a-meeting-suggestion"></a>La confianza de una sugerencia de la reunión

La propiedad **confidence** de un objeto **meetingTimeSuggestion** oscila entre 0 % y 100 %, y representa la posibilidad de que todos los asistentes asistan a la reunión, tomando como base de su estado de disponibilidad individual:

- Para cada asistente, un estado libre para una periodo de tiempo de reunión especificado se corresponde al 100 % de posibilidades de asistencia, un estado desconocido al 49 % y un estado ocupado al 0 %.
- La confianza de una sugerencia de hora de la reunión se calcula promediando la posibilidad de asistencia sobre todos los asistentes especificados para esa reunión.
- Si hay varias sugerencias de hora de la reunión, la acción **findMeetingTimes** ordena primero las sugerencias por su valor de confianza calculado de alto a bajo. Si hay sugerencias con la misma confianza, entonces la acción las ordena cronológicamente.
- Se puede usar el parámetro opcional **minimumAttendeePercentage** para **findMeetingTimes** para especificar que solo se devuelvan sugerencias de la hora de la reunión con al menos un nivel de confianza determinado. Por ejemplo, se puede especificar un valor **minimumAttendeePercentage** de 80 % si solo se quieren sugerencias que tengan una probabilidad del 80 % o más de que asistan todos los asistentes. Si no se especifica **minimumAttendeePercentage**, **findMeetingTimes** da por supuesto un valor de 50 %.

Por ejemplo, si una sugerencia de hora de la reunión implica tres asistentes con el siguiente estado de disponibilidad:

|**Asistente**|**Estado de disponibilidad**|**Posibilidades de asistencia (%)**|
|:-----|:-----|:-----|
|Dana | Libre | 100 % |
|Pelayo | Desconocido | 49 % |
|Fanny | Ocupado | 0 % |

Entonces la confianza de la sugerencia de hora de la reunión, que es la posibilidad media de asistencia, es (100 % + 49 % + 0 %)/3 = 49,66 %.

Si especifica un valor **minimumAttendeePercentage** del 80 % en una operación **findMeetingTimes**, porque 49,66 %< 8 0%, la operación no sugerirá esta hora en la respuesta.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra cómo encontrar tiempo para reunirse en un lugar determinado y solicitar un motivo para cada sugerencia, especificando los siguientes parámetros en el cuerpo de la solicitud:

- **attendees**
- **locationConstraint**
- **timeConstraint**
- **meetingDuration**
- **returnSuggestionReasons**
- **minimumAttendeePercentage**

Al establecer el parámetro **returnSuggestionReasons**, también se obtiene una explicación en la propiedad **suggestionReason** de cada sugerencia, si **findMeetingTimes** devuelve alguna sugerencia.

Observe que la solicitud especifica la hora en la zona horaria PST y la respuesta devuelve las sugerencias de hora de la reunión en UTC, de forma predeterminada. Se puede usar el encabezado de solicitud `Prefer: outlook.timezone` para especificar también PST para los valores de hora de la respuesta.

##### <a name="request"></a>Solicitud
Aquí está la solicitud de ejemplo.
<!-- {
  "blockType": "request",
  "name": "user_findmeetingtimes"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/findMeetingTimes
Content-type: application/json

{ 
  "attendees": [ 
    { 
      "type": "required",  
      "emailAddress": { 
        "name": "Fanny Downs",
        "address": "fannyd@a830edad905084922E16072013.onmicrosoft.com" 
      } 
    },
    { 
      "type": "optional",  
      "emailAddress": { 
        "name": "Dana Swope",
        "address": "danas@a830edad905084922E16072013.onmicrosoft.com" 
      } 
    } 
  ],  
  "locationConstraint": { 
    "isRequired": "false",  
    "suggestLocation": "false",  
    "locations": [ 
      { 
        "resolveAvailability": "false",
        "displayName": "Conf room Hood" 
      } 
    ] 
  },  
  "timeConstraint": { 
    "timeslots": [ 
      { 
        "start": { 
          "dateTime": "2016-10-20T07:00:00",  
          "timeZone": "Pacific Standard Time" 
        },  
        "end": { 
          "dateTime": "2016-10-20T17:00:00",  
          "timeZone": "Pacific Standard Time" 
        } 
      } 
    ] 
  },  
  "meetingDuration": "PT2H",
  "returnSuggestionReasons": "true",
  "minimumAttendeePercentage": "60"
}
```

##### <a name="response"></a>Respuesta
Esta es una solicitud de ejemplo. Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.meetingTimeSuggestionsResult",
  "isCollection": false
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json


{
   "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#microsoft.graph.meetingTimeSuggestionsResult",
   "meetingTimeSuggestions":[
      {
         "meetingTimeSlot":{
            "start":{
               "dateTime":"2016-10-20T15:00:00.0000000",
               "timeZone":"UTC"
            },
            "end":{
               "dateTime":"2016-10-20T17:00:00.0000000",
               "timeZone":"UTC"
            }
         },
         "confidence":100,
         "organizerAvailability":"free",
         "attendeeAvailability":[
            {
               "attendee":{
                  "type":"required",
                  "emailAddress":{
                    "name": "Fanny Downs",
                    "address": "fannyd@a830edad905084922E16072013.onmicrosoft.com" 
                  }
               },
               "availability":"free"
            },
            {
               "attendee":{
                  "type":"required",
                  "emailAddress":{
                    "name": "Dana Swope",
                    "address": "danas@a830edad905084922E16072013.onmicrosoft.com" 
                  }
               },
               "availability":"free"
            }
         ],
         "locations":[
            {
               "displayName":"Conf room Hood"
            }
         ],
         "suggestionReason":"Suggested because it is one of the nearest times when all attendees are available."
      },
      {
         "meetingTimeSlot":{
            "start":{
               "dateTime":"2016-10-20T17:00:00.0000000",
               "timeZone":"UTC"
            },
            "end":{
               "dateTime":"2016-10-20T19:00:00.0000000",
               "timeZone":"UTC"
            }
         },
         "confidence":100,
         "organizerAvailability":"free",
         "attendeeAvailability":[
            {
               "attendee":{
                  "type":"required",
                  "emailAddress":{
                    "name": "Fanny Downs",
                    "address": "fannyd@a830edad905084922E16072013.onmicrosoft.com" 
                  }
               },
               "availability":"free"
            },
            {
               "attendee":{
                  "type":"required",
                  "emailAddress":{
                    "name": "Dana Swope",
                    "address": "danas@a830edad905084922E16072013.onmicrosoft.com" 
                  }
               },
               "availability":"unknown"
            }
         ],
         "locations":[
            {
               "displayName":"Conf room Hood"
            }
         ],
         "suggestionReason":"Suggested because it is one of the nearest times when all attendees are available."
      }
   ],
   "emptySuggestionsReason":""
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: findMeetingTimes",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->