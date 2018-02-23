# <a name="androidforworkappconfigurationschemaitem-resource-type"></a>Tipo de recurso androidForWorkAppConfigurationSchemaItem

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Elemento de configuración único dentro del esquema de configuración personalizada de la aplicación de Android for Work.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|schemaItemKey|Cadena|La clave única que usa la aplicación para identificar el elemento|
|displayName|Cadena|Nombre legible|
|description|Cadena|Descripción de lo que controla el elemento dentro de la aplicación|
|defaultBoolValue|Booleano|Valor predeterminado para los elementos de tipo booleano, si lo especifica el desarrollador de aplicaciones|
|defaultIntValue|Int32|Valor predeterminado para los elementos de tipo entero, si lo especifica el desarrollador de aplicaciones|
|defaultStringValue|Cadena|Valor predeterminado para los elementos de tipo cadena, si lo especifica el desarrollador de aplicaciones|
|defaultStringArrayValue|Colección de cadenas|Valor predeterminado para los elementos de tipo matriz de cadenas, si lo especifica el desarrollador de aplicaciones|
|dataType|Cadena|El tipo de valor que describe este elemento. Los valores posibles son: `bool`, `integer`, `string`, `choice`, `multiselect`, `bundle`, `bundleArray` y `hidden`.|
|selecciones|Colección [keyValuePair](../resources/intune_androidforwork_keyvaluepair.md)|Lista de los pares nombre-valor legibles para los valores válidos que se pueden establecer para este elemento (solo elementos de selección de opciones múltiples)|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.androidForWorkAppConfigurationSchemaItem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidForWorkAppConfigurationSchemaItem",
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
```



