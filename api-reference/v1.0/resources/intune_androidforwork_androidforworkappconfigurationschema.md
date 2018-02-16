# <a name="androidforworkappconfigurationschema-resource-type"></a>Tipo de recurso androidForWorkAppConfigurationSchema

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Esquema que describe la configuración personalizada de una aplicación de Android for Work.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar androidForWorkAppConfigurationSchemas](../api/intune_androidforwork_androidforworkappconfigurationschema_list.md)|Colección [androidForWorkAppConfigurationSchema](../resources/intune_androidforwork_androidforworkappconfigurationschema.md)|Enumere las propiedades y las relaciones de los objetos [androidForWorkAppConfigurationSchema](../resources/intune_androidforwork_androidforworkappconfigurationschema.md).|
|[Obtener androidForWorkAppConfigurationSchema](../api/intune_androidforwork_androidforworkappconfigurationschema_get.md)|[androidForWorkAppConfigurationSchema](../resources/intune_androidforwork_androidforworkappconfigurationschema.md)|Lea las propiedades y las relaciones del objeto [androidForWorkAppConfigurationSchema](../resources/intune_androidforwork_androidforworkappconfigurationschema.md).|
|[Crear androidForWorkAppConfigurationSchema](../api/intune_androidforwork_androidforworkappconfigurationschema_create.md)|[androidForWorkAppConfigurationSchema](../resources/intune_androidforwork_androidforworkappconfigurationschema.md)|Cree un objeto [androidForWorkAppConfigurationSchema](../resources/intune_androidforwork_androidforworkappconfigurationschema.md).|
|[Eliminar androidForWorkAppConfigurationSchema](../api/intune_androidforwork_androidforworkappconfigurationschema_delete.md)|Ninguna|Elimina un [androidForWorkAppConfigurationSchema](../resources/intune_androidforwork_androidforworkappconfigurationschema.md)|
|[Actualizar androidForWorkAppConfigurationSchema](../api/intune_androidforwork_androidforworkappconfigurationschema_update.md)|[androidForWorkAppConfigurationSchema](../resources/intune_androidforwork_androidforworkappconfigurationschema.md)|Actualice las propiedades de un objeto [androidForWorkAppConfigurationSchema](../resources/intune_androidforwork_androidforworkappconfigurationschema.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|Clave de la entidad a la que corresponde el esquema del nombre del paquete Android para la aplicación|
|exampleJson|Binario|Matriz de bytes codificada UTF8 que contiene la cadena JSON de ejemplo conforme a este esquema que muestra cómo configurar los ajustes de esta aplicación|
|schemaItems|Colección [androidForWorkAppConfigurationSchemaItem](../resources/intune_androidforwork_androidforworkappconfigurationschemaitem.md)|Colección de elementos donde cada uno representa una opción de configuración con nombre en el esquema|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.androidForWorkAppConfigurationSchema"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidForWorkAppConfigurationSchema",
  "id": "String (identifier)",
  "exampleJson": "binary",
  "schemaItems": [
    {
      "@odata.type": "microsoft.graph.androidForWorkAppConfigurationSchemaItem",
      "schemaItemKey": "String",
      "displayName": "String",
      "description": "String",
      "defaultBoolValue": true,
      "defaultIntValue": 1024,
      "defaultStringValue": "String",
      "defaultStringArrayValue": [
        "String"
      ],
      "dataType": "String",
      "selections": [
        {
          "@odata.type": "microsoft.graph.keyValuePair",
          "name": "String",
          "value": "String"
        }
      ]
    }
  ]
}
```



