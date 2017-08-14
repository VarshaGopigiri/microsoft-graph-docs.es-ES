# <a name="groupsettingtemplate-resource-type"></a>Tipo de recurso groupSettingTemplate

Las plantillas de configuración de grupo representan configuraciones definidas por el sistema disponibles para el inquilino. La [configuración de grupo](groupsetting.md) se puede crear según las plantillas de **groupSettingTemplates** disponibles y se pueden cambiar los valores predeterminados. Las plantillas de configuración de grupo no se pueden crear, actualizar ni eliminar. Esta configuración puede representar configuración para todo el inquilino o una para un grupo específico. Actualmente, las únicas plantillas disponibles se aplican a grupos de Office 365 e incluyen opciones como las que establecen si los usuarios pueden crear grupos o no, o si pueden invitar a usuarios de fuera de la organización para convertirse en miembros de un grupo.

## <a name="methods"></a>Métodos

| Método | Tipo de valor devuelto | Descripción |
|:---------------|:--------|:----------|
|[Get groupSettingTemplate](../api/groupsettingtemplate_get.md) | [groupSettingTemplate](groupsettingtemplate.md) | Lee las propiedades específicas de uno de los objetos groupSettingTemplate definido por el sistema. |
|[List groupSettingTemplate](../api/groupsettingtemplate_list.md) | [Colección de groupSettingTemplate](groupsettingtemplate.md) |Enumera todos los objetos groupSettingTemplate definidos por el sistema.|

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:---------------|:--------|:----------|
|description|String| Descripción de la plantilla. |
|displayName|String| Muestra el nombre de la plantilla. |
|id|String| Identificador único de la plantilla. Solo lectura.|
|values|Colección de [settingTemplateValue](settingtemplatevalue.md)| Colección de settingTemplateValues que enumera el conjunto de opciones disponibles, los valores predeterminados y los tipos que forman esta plantilla. |

## <a name="relationships"></a>Relaciones

Ninguna.


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.groupSettingTemplate"
}-->

```json
{
  "description": "String",
  "displayName": "String",
  "id": "String (identifier)",
  "values": [{"@odata.type": "microsoft.graph.settingTemplateValue"}]
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "groupSettingTemplate resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->