# <a name="schemaextension-resource-type-schema-extensions"></a>Tipo de recurso schemaExtension (extensiones de esquema)

Las extensiones de esquema permiten definir un esquema para extender y agregar datos personalizados fuertemente tipados a un tipo de recurso. Los datos personalizados aparecen como un tipo complejo en el recurso extendido. 

Las extensiones de esquema son compatibles con los siguientes tipos de recursos:

 - [contact](contact.md)
 - [device](device.md)
 - [evento](event.md) en un usuario o un calendario de grupo de Office 365
 - [post](post.md) de un grupo de Office 365
 - [group](group.md)
 - [message](message.md) 
 - [organization](organization.md)
 - [user](user.md)

Consulte el [ejemplo de extensión de esquema](../../../concepts/extensibility_schema_groups.md) para obtener información sobre cómo agregar datos personalizados a los grupos.

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Create](../api/schemaextension_post_schemaextensions.md) | schemaExtension |Crea una definición de extensión de esquema.|
|[List](../api/schemaextension_list.md) | schemaExtension |Enumera las definiciones schemaExtension disponibles y sus propiedades.|
|[Get](../api/schemaextension_get.md) | schemaExtension |Lee las propiedades de una definición schemaExtension específica.|
|[Update](../api/schemaextension_update.md) | schemaExtension    |Actualiza una definición schemaExtension. |
|[Delete](../api/schemaextension_delete.md) | Ninguno |Elimina una definición schemaExtension. |

## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|description|Cadena|Descripción de la extensión de esquema.|
|id|Cadena|Identificador único para la definición de la extensión de esquema. El valor debe ser una concatenación de uno de los dominios verificados (por ejemplo, contoso.com) y un nombre para la extensión del esquema (por ejemplo, *contoso_miEsquema*). |
|owner|Cadena|Id. de la aplicación que creó la extensión del esquema. Solo lectura.|
|properties|Colección [extensionSchemaProperty](extensionschemaproperty.md)|La colección de nombres de propiedad y tipos que conforman la definición de la extensión de esquema.|
|status|Cadena|El estado del ciclo de vida de la extensión de esquema. Los estados posibles son **InDevelopment** (En desarrollo), **Available** (Disponible) y **Deprecated** (En desuso). En el momento de la creación se establece automáticamente en **InDevelopment**. Las [extensiones de esquema](../../../concepts/extensibility_overview.md#schema-extensions) proporcionan más información sobre los comportamientos y las transiciones de estado posibles.|
|targetTypes|Colección de cadenas|Conjunto de tipos de Microsoft Graph (compatibles con extensiones) a los que se puede aplicar la extensión de esquema. Seleccione **contact**, **device**, **event**, **group**, **message**, **organization**, **post** o **user**.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.schemaExtension"
}-->

```json
{
  "description": "String",
  "id": "String (identifier)",
  "owner": "String",
  "properties": [{"@odata.type": "microsoft.graph.extensionSchemaProperty"}],
  "status": "String",
  "targetTypes": ["String"]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "schemaExtension resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->