# <a name="calendar-resource-type"></a>tipo de recurso calendar

Un calendario que es un contenedor de eventos.

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Enumerar calendarios](../api/user_list_calendars.md)|Colección [calendar](calendar.md)|Obtenga todos los calendarios del usuario o los calendarios en el grupo de calendarios predeterminado o en otro grupo de calendarios específico.|
|[Crear calendario](../api/user_post_calendars.md) |[calendar](calendar.md)| Cree un calendario en el grupo de calendarios predeterminado o en el grupo de calendario especificado.|
|[Obtener calendario](../api/calendar_get.md) | [calendar](calendar.md) |Lea las propiedades y las relaciones del objeto de calendario.|
|[Actualizar](../api/calendar_update.md) | [calendar](calendar.md)  |Actualice el objeto de calendario. |
|[Eliminar](../api/calendar_delete.md) | Ninguno |Elimine el objeto de calendario. |
|[Enumerar calendarView](../api/calendar_list_calendarview.md) |Colección [Event](event.md)| Obtiene las repeticiones, excepciones e instancias únicas de eventos en una vista de calendario definida por un intervalo de tiempo del calendario principal del usuario `(../me/calendarview)` o de un calendario especificado.|
|[Enumerar eventos](../api/calendar_list_events.md) |Colección [event](event.md)| Recupere una lista de eventos de un calendario.  La lista contiene patrones de serie y reuniones de instancia única.|
|[Crear evento](../api/calendar_post_events.md) |[Event](event.md)| Cree un nuevo objeto Event en el calendario especificado o el predeterminado.|
|[Crear propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty_post_singlevalueextendedproperties.md) |[calendar](calendar.md)  |Cree una o varias propiedades extendidas de valor único en un calendario nuevo o existente.   |
|[Obtener calendario con propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty_get.md)  | [calendar](calendar.md) | Obtenga calendarios que contienen una propiedad extendida de valor único mediante el uso de `$expand` o `$filter`. |
|[Crear propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty_post_multivalueextendedproperties.md) | [calendar](calendar.md) | Cree una o varias propiedades extendidas de varios valores en un calendario nuevo o existente.  |
|[Obtener calendario con propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty_get.md)  | [calendar](calendar.md) | Obtenga un calendario que contiene una propiedad extendida de varios valores mediante el uso de `$expand`. |


## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|name|String|El nombre del calendario.|
|changeKey|String|Identifica la versión del objeto de calendario. Cada vez que cambia el calendario, cambia también ChangeKey. Permite que Exchange aplique los cambios a la versión correcta del objeto. Solo lectura.|
|color|String|Especifica el tema de color para distinguir el calendario de otros calendarios en una interfaz de usuario. Los valores de propiedad son: LightBlue=0, LightGreen=1, LightOrange=2, LightGray=3, LightYellow=4, LightTeal=5, LightPink=6, LightBrown=7, LightRed=8, MaxColor=9, Auto=-1|
|id|String|Identificador único del grupo. Solo lectura.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo    |Descripción|
|:---------------|:--------|:----------|
|calendarView|Colección [event](event.md)|La vista Calendario del calendario. Propiedad Navigation. Solo lectura.|
|events|Colección [event](event.md)|Los eventos del calendario. Propiedad Navigation. Solo lectura.|
|multiValueExtendedProperties|Colección [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)| La colección de propiedades extendidas de varios valores definidas para el calendario. Solo lectura. Admite valores NULL.|
|singleValueExtendedProperties|Colección [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md)| La colección de propiedades extendidas de valor único definidas para el calendario. Solo lectura. Admite valores NULL.|

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
  "changeKey": "string",
  "color": "String",
  "id": "string (identifier)",
  "name": "string"
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
