# <a name="calendar-resource-type"></a>tipo de recurso calendar

Un calendario que es un contenedor de eventos.

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[List calendars](../api/user_list_calendars.md)|[calendar](calendar.md) collection|Obtenga todos los calendarios del usuario o los calendarios en el grupo de calendarios predeterminado o en otro grupo de calendarios específico.|
|[Create calendar](../api/user_post_calendars.md) |[calendar](calendar.md)| Cree un calendario en el grupo de calendarios predeterminado o en el grupo de calendario especificado.|
|[Get calendar](../api/calendar_get.md) | [calendar](calendar.md) |Lea las propiedades y las relaciones del objeto de calendario.|
|[Update](../api/calendar_update.md) | [calendar](calendar.md)  |Actualice el objeto de calendario. |
|[Delete](../api/calendar_delete.md) | Ninguno |Elimine el objeto de calendario. |
|[List calendarView](../api/calendar_list_calendarview.md) |Colección [event](event.md)| Obtiene las repeticiones, excepciones e instancias únicas de eventos en una vista de calendario definida por un intervalo de tiempo del calendario principal del usuario `(../me/calendarview)` o de un calendario especificado.|
|[List events](../api/calendar_list_events.md) |Colección [event](event.md)| Recupera una lista de eventos de un calendario.  La lista contiene patrones de serie y reuniones de instancia única.|
|[Create Event](../api/calendar_post_events.md) |[event](event.md)| Crea un evento en el calendario especificado o el predeterminado.|
|[Create single-value extended property](../api/singlevaluelegacyextendedproperty_post_singlevalueextendedproperties.md) |[calendar](calendar.md)  |Cree una o varias propiedades extendidas de valor único en un calendario nuevo o existente.   |
|[Get calendar with single-value extended property](../api/singlevaluelegacyextendedproperty_get.md)  | [calendar](calendar.md) | Obtenga calendarios que contienen una propiedad extendida de valor único mediante el uso de `$expand` o `$filter`. |
|[Create multi-value extended property](../api/multivaluelegacyextendedproperty_post_multivalueextendedproperties.md) | [calendar](calendar.md) | Cree una o varias propiedades extendidas de varios valores en un calendario nuevo o existente.  |
|[Get calendar with multi-value extended property](../api/multivaluelegacyextendedproperty_get.md)  | [calendar](calendar.md) | Obtenga un calendario que contiene una propiedad extendida de varios valores mediante el uso de `$expand`. |


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|canEdit |Booleano |Es verdadero si el usuario puede escribir en el calendario; de lo contrario, es falso. Esta propiedad es verdadera para el usuario que creó el calendario. Esta propiedad también es verdadera para un usuario con quien se compartió un calendario y al que se concedió acceso de escritura. |
|canShare |Booleano |Es verdadero si el usuario tiene permiso para compartir el calendario; de lo contrario, es falso. Solo el usuario que creó el calendario puede compartirlo. |
|canViewPrivateItems |Booleano |Es verdadero si el usuario puede leer elementos del calendario que se marcaron como privados; de lo contrario, es falso. |
|changeKey|String|Identifica la versión del objeto “calendar”. Cada vez que se cambia el calendario, también se cambia changeKey. Esto permite que Exchange aplique los cambios en la versión correcta del objeto. Solo lectura.|
|color|String|Especifica el tema de color para distinguir el calendario de otros calendarios en una interfaz de usuario. Los valores de propiedad son: LightBlue=0, LightGreen=1, LightOrange=2, LightGray=3, LightYellow=4, LightTeal=5, LightPink=6, LightBrown=7, LightRed=8, MaxColor=9, Auto=-1|
|id|String|El identificador único del grupo. Solo lectura.|
|name|String|El nombre del calendario.|
|owner |[emailAddress](emailaddress.md) | Si se establece, representa al usuario que creó o agregó el calendario. Para un calendario que el usuario creó o agregó, la propiedad **owner** se establece en el usuario. Para un calendario compartido con el usuario, la propiedad **owner** se establece en la persona que compartió el calendario con el usuario. |

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|calendarView|[Event](event.md) collection|La vista Calendario del calendario. Propiedad Navigation. Solo lectura.|
|events|[Event](event.md) collection|Los eventos del calendario. Propiedad Navigation. Solo lectura.|
|multiValueExtendedProperties|Colección [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)| La colección de propiedades extendidas de varios valores definidas para el calendario. Solo lectura. Admite valores NULL.|
|singleValueExtendedProperties|[singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md) collection| La colección de propiedades extendidas de valor único definidas para el calendario. Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "calendarView",
    "events",
    "multiValueExtendedProperties",
    "singleValueExtendedProperties"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.calendar"
}-->

```json
{
  "canEdit": "boolean",
  "canShare": "boolean",
  "canViewPrivateItems": "boolean",
  "changeKey": "string",
  "color": "String",
  "id": "string (identifier)",
  "name": "string",
  "owner": {"@odata.type": "microsoft.graph.emailAddress"}
}

```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "calendar resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
