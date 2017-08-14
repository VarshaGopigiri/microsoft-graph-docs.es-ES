# <a name="groupsetting-resource-type"></a>Tipo de recurso groupSetting

Comportamientos del control de configuración de grupo, como listas de palabras bloqueadas para los nombres para mostrar del grupo o si los usuarios invitados pueden ser propietarios del grupo.

La configuración de grupo se puede crear según las plantillas de [groupSettingTemplates](groupSettingTemplate.md) disponibles y se pueden cambiar los valores predeterminados. Esta configuración controla el comportamiento del grupo a nivel de todo el inquilino o en un grupo específico. Cuando se establece la misma configuración a nivel de todo el inquilino y en un grupo específico, la configuración de nivel de grupo reemplaza la configuración a nivel de inquilino.  Por ejemplo, puede que una configuración a nivel de todo el inquilino permite que los miembros existentes inviten a otros usuarios, pero la configuración de un grupo concreto puede reemplazarla y no permitir que los miembros del grupo puedan invitar a otros usuarios como invitados. La configuración de grupo solo controla el comportamiento de los grupos de Office 365.

## <a name="methods"></a>Métodos

| Método | Tipo de valor devuelto | Descripción |
|:---------------|:--------|:----------|
|[Create setting](../api/groupsetting_post_groupsettings.md) | [groupSetting](groupsetting.md) |Crea un objeto de configuración según una plantilla de groupSettingTemplate. La solicitud POST debe proporcionar settingValues para toda la configuración establecida en la plantilla. |
|[Get setting](../api/groupsetting_get.md) | [groupSetting](groupsetting.md) | Lee las propiedades de un objeto de configuración específico. |
|[List settings](../api/groupsetting_list.md) | Colección de [groupSetting](groupsetting.md) | Enumera las propiedades de todos los objetos de configuración. |
|[Update setting](../api/groupsetting_update.md) | [groupSetting](groupsetting.md) | Actualiza el objeto groupSetting. |
|[Delete setting](../api/groupsetting_delete.md) | Ninguno | Elimina un objeto de configuración. |

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:---------------|:--------|:----------|
|displayName|String| El nombre para mostrar de este grupo de configuraciones, que proviene de la plantilla asociada. |
|id|String| Identificador único de esta configuración. Solo lectura. |
|templateId|String| Identificador único para la plantilla que se usa para crear este grupo de configuraciones. Solo lectura. |
|values|Colección de [settingValue](settingvalue.md)| Colección de pares de nombre y valor. Debe contener y establecer todas las configuraciones definidas en la plantilla. |

## <a name="relationships"></a>Relaciones

Ninguna.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.groupSetting"
}-->

```json
{
  "displayName": "String",
  "id": "String (identifier)",
  "templateId": "String",
  "values": [{"@odata.type": "microsoft.graph.settingValue"}]
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "groupSetting resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->