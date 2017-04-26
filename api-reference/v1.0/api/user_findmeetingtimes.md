# <a name="user-findmeetingtimes"></a>user: findMeetingTimes
Busque sugerencias de hora de la reunión en función de la disponibilidad del organizador y los asistentes, y restricciones de hora o de ubicación especificadas como parámetros.

Si **findMeetingTimes** no puede devolver sugerencias de reunión, la respuesta podría indicar un motivo en la propiedad **emptySuggestionsReason**. Basándose en este valor, se pueden ajustar mejor los parámetros y llamar otra vez a **findMeetingTimes**.


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
| Autorización  | Portador<code>. Required.|
| Prefer: outlook.timezone | Una cadena que representa una zona horaria concreta para la respuesta, por ejemplo, "Hora estándar del Pacífico". Opcional. Se utiliza la hora UTC si no se especifica este encabezado.|


## <a name="request-body"></a>Cuerpo de solicitud
Todos los parámetros admitidos se enumeran a continuación. Dependiendo de su escenario, especifique un objeto JSON para cada uno de los parámetros necesarios en el cuerpo de la solicitud. 


| Parámetro       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|attendees|Colección [attendeeBase](../resources/attendeebase.md)|Una colección de los asistentes o los recursos de la reunión. Puesto que findMeetingTimes supone que cualquier asistente que sea una persona siempre es necesario, especifique `required` para una persona y `resource` para un recurso en la propiedad **tipo** correspondiente. Una colección vacía hace que **findMeetingTimes** busque intervalos de tiempo libres solo para el organizador. Opcional.|
|isOrganizerOptional|Edm.Boolean|Especificar `True` si no es preciso que el organizador asista. El valor predeterminado es `false`. Opcional.|
|locationConstraint|[locationConstraint](../resources/locationconstraint.md)|Los requisitos del organizador sobre la ubicación de la reunión, por ejemplo si se requiere una sugerencia para una ubicación de la reunión o si hay ubicaciones específicas en las que únicamente pueda tener lugar la reunión. Opcional.|
|maxCandidates|Edm.Int32|El número máximo de sugerencias de hora de la reunión que se va a devolver. Opcional.|
|meetingDuration|Edm.Duration|La duración de la reunión, en formato [ISO8601](http://www.iso.org/iso/iso8601). Por ejemplo, 1 hora se indica como 'PT1H', donde 'P' es el designador de duración, 't' es el designador de tiempo y 'H' es el designador de hora. Si no se especifica ninguna duración de la reunión, **findMeetingTimes** usa el valor predeterminado de 30 minutos. Opcional.|
|minimumAttendeePercentage|Edm.Double| La [confianza](#the-confidence-of-a-meeting-suggestion) mínima necesaria para que se devuelva un intervalo de tiempo en la respuesta. Es un valor de porcentaje (%) comprendido entre 0 y 100. Opcional.|
|returnSuggestionReasons|Edm.Boolean|Especifique `True` para devolver un motivo para cada sugerencia de la reunión en la propiedad **suggestionReason**. El valor predeterminado es `false` para no devolver esa propiedad. Opcional.|
|timeConstraint|[timeConstraint](../resources/timeconstraint.md)|Las restricciones de tiempo para una reunión, que pueden incluir la naturaleza de la reunión (propiedad **activityDomain**) y posibles periodos de tiempo de la reunión (propiedad **timeSlots**). **findMeetingTimes** asume **activityDomain** como `work` si no especifica este parámetro. Opcional.|

En la tabla siguiente se describen las restricciones puede especificar en el parámetro **timeConstraint**.

|**valor activityDomain en timeConstraint**|**Sugerencias de hora de reunión**|
|:-----|:-----|
|trabajo| Las sugerencias se encuentran dentro de la jornada laboral del usuario, que está definida en su configuración de calendario y tanto el administrador como el propio usuario pueden personalizar. Las horas de trabajo por defecto son de lunes al viernes, de 8 a.m. a 5 p.m. en la zona horaria establecida para el buzón. Este es el valor predeterminado si no se especifica **activityDomain**. |
|personal| Las sugerencias se encuentran dentro de la jornada laboral del usuario y en sábado y domingo. El valor predeterminado es del lunes al domingo, de 8 a.m. a 5 p.m., en la configuración de zona horaria para el buzón.|
|sin restricciones | Las sugerencias pueden pertenecer a cualquier hora del día, todos los días de la semana.|
|desconocido | No utilice este valor, pues quedará obsoleto en el futuro. Actualmente se comporta igual que `work`. Cambie cualquier código existente para usar `work`, `personal` o `unrestricted` según corresponda.


Basándose en los parámetros especificados, **findMeetingTimes** comprueba el estado de disponibilidad en los calendarios principales del organizador y los asistentes. La acción calcula la mejor hora de la reunión posible y devuelve cualquier sugerencia de reunión.


## <a name="response"></a>Respuesta
Si es correcto, este método devuelve un código de respuesta `200, OK` y un objeto [meetingTimeSuggestionsResult](../resources/meetingTimeSuggestionsResult.md) en el cuerpo de la respuesta. 

Un objeto **meetingTimeSuggestionsResult** incluye una colección de sugerencias de la reunión y una propiedad **emptySuggestionsReason**. Cada sugerencia se define como una [meetingTimeSuggestion](../resources/meetingTimeSuggestion.md), con los asistentes con un nivel de confianza medio del 50 % de asistir o un porcentaje concreto que especificó en el parámetro **minimumAttendeePercentage**. 

De forma predeterminada, cada sugerencia de hora de la reunión se devuelve en formato UTC. 

Si **findMeetingTimes** no puede devolver sugerencias de reunión, la respuesta podría indicar un motivo en la propiedad **emptySuggestionsReason**. Basándose en este valor, se pueden ajustar mejor los parámetros y llamar otra vez a **findMeetingTimes**.

### <a name="the-confidence-of-a-meeting-suggestion"></a>La confianza de una sugerencia de la reunión

La propiedad **confidence** de un objeto **meetingTimeSuggestion** oscila entre 0 % y 100 %, y representa la posibilidad de que todos los asistentes asistan a la reunión, tomando como base de su estado de disponibilidad individual:

- Para cada asistente, un estado libre para una periodo de tiempo de reunión especificado se corresponde al 100 % de posibilidades de asistencia, un estado desconocido al 49 % y un estado ocupado al 0 %.
- La confianza de una sugerencia de hora de la reunión se calcula promediando la posibilidad de asistencia sobre todos los asistentes especificados para esa reunión.
- Se puede usar el parámetro opcional **minimumAttendeePercentage** para **findMeetingTimes** para especificar que solo se devuelvan sugerencias de la hora de la reunión con al menos un nivel de confianza determinado. Por ejemplo, se puede especificar un valor **minimumAttendeePercentage** de 80 % si solo se quieren sugerencias que tengan una probabilidad del 80 % o más de que asistan todos los asistentes. Si no se especifica **minimumAttendeePercentage**, **findMeetingTimes** da por supuesto un valor de 50 %.
- Si hay varias sugerencias de hora de la reunión, la acción **findMeetingTimes** ordena primero las sugerencias por su valor de confianza calculado de alto a bajo. Si hay sugerencias con la misma confianza, entonces la acción las ordena cronológicamente.

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
Prefer: outlook.timezone="Pacific Standard Time"
Content-Type: application/json

{ 
  "attendees": [ 
    { 
      "type": "required",  
      "emailAddress": { 
        "name": "Fanny Downs",
        "address": "fannyd@contoso.onmicrosoft.com" 
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
    "activityDomain":"unrestricted", 
    "timeslots": [ 
      { 
        "start": { 
          "dateTime": "2017-04-17T09:00:00",  
          "timeZone": "Pacific Standard Time" 
        },  
        "end": { 
          "dateTime": "2017-04-19T17:00:00",  
          "timeZone": "Pacific Standard Time" 
        } 
      } 
    ] 
  },  
  "meetingDuration": "PT2H",
  "returnSuggestionReasons": "true",
  "minimumAttendeePercentage": "100"
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
Preference-Applied: outlook.timezone="Pacific Standard Time"
Content-Length: 976

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#microsoft.graph.meetingTimeSuggestionsResult",
    "emptySuggestionsReason":"",
    "meetingTimeSuggestions":[
        {
            "confidence":100.0,
            "organizerAvailability":"free",
            "suggestionReason":"Suggested because it is one of the nearest times when all attendees are available.",
            "meetingTimeSlot":{
                "start":{
                    "dateTime":"2017-04-17T18:00:00.0000000",
                    "timeZone":"Pacific Standard Time"
                },
                "end":{
                    "dateTime":"2017-04-17T20:00:00.0000000",
                    "timeZone":"Pacific Standard Time"
                }
            },
            "attendeeAvailability":[
                {
                    "availability":"free",
                    "attendee":{
                        "type":"required",
                        "emailAddress":{
                            "address":"fannyd@contoso.onmicrosoft.com"
                        }
                    }
                }
            ],
            "locations":[
                {
                    "displayName":"Conf room Hood"
                }
            ]
        },
        {
            "confidence":100.0,
            "organizerAvailability":"free",
            "suggestionReason":"Suggested because it is one of the nearest times when all attendees are available.",
            "meetingTimeSlot":{
                "start":{
                    "dateTime":"2017-04-17T20:00:00.0000000",
                    "timeZone":"Pacific Standard Time"
                },
                "end":{
                    "dateTime":"2017-04-17T22:00:00.0000000",
                    "timeZone":"Pacific Standard Time"
                }
            },
            "attendeeAvailability":[
                {
                    "availability":"free",
                    "attendee":{
                        "type":"required",
                        "emailAddress":{
                            "address":"fannyd@contoso.onmicrosoft.com"
                        }
                    }
                }
            ],
            "locations":[
                {
                    "displayName":"Conf room Hood"
                }
            ]
        }
   ]
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