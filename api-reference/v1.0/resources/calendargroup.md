# <a name="calendargroup-resource-type"></a>Tipo de recurso calendarGroup

Grupo de calendarios.

**Nota** Outlook.com solo admite el grupo de calendarios predeterminado que es accesible mediante el acceso directo ../me/calendars. No se puede eliminar ese grupo de calendarios.

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[List calendar groups](../api/user_list_calendargroups.md) |Colección [Calendar](calendar.md)| Obtiene los grupos de calendarios del usuario.|
|[Create calendar group](../api/user_post_calendargroups.md) |[Calendar](calendar.md)| Crea un grupo de calendarios.|
|[Get calendar group](../api/calendargroup_get.md) | [calendarGroup](calendargroup.md) |Lee las propiedades y relaciones de un objeto de grupo de calendarios.|
|[Update](../api/calendargroup_update.md) | [calendarGroup](calendargroup.md) |Actualiza el objeto calendarGroup. |
|[Delete](../api/calendargroup_delete.md) | None |Elimina el objeto calendarGroup. |
|[List calendars](../api/calendargroup_list_calendars.md) |Colección [Calendar](calendar.md)| Muestra la lista de calendarios de un grupo de calendarios.|
|[Create Calendar](../api/calendargroup_post_calendars.md) |[Calendar](calendar.md)| Crea un calendario en un grupo de calendarios.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|name|String|Nombre del grupo.|
|changeKey|String|Identifica la versión del grupo de calendarios. Cada vez que cambia el grupo de calendarios, cambia también ChangeKey. Permite que Exchange aplique los cambios a la versión correcta del objeto. Solo lectura.|
|classId|Guid|Identificador de la clase. Solo lectura.|
|id|String|Identificador único del grupo. Solo lectura.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|calendars|Colección [Calendar](calendar.md)|Calendarios del grupo de calendarios. Propiedad de navegación. Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "calendars"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.calendarGroup"
}-->

```json
{
  "changeKey": "string",
  "classId": "guid",
  "id": "string (identifier)",
  "name": "string"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "calendarGroup resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
