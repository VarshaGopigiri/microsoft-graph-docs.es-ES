# <a name="appconfigurationsettingitem-resource-type"></a>Tipo de recurso appConfigurationSettingItem

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades del elemento de configuración de la configuración de la aplicación.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|appConfigKey|Cadena|Clave de configuración de la aplicación.|
|appConfigKeyType|[mdmAppConfigKeyType](../resources/intune_apps_mdmappconfigkeytype.md)|Tipo de clave de configuración de la aplicación. Los valores posibles son: `stringType`, `integerType`, `realType`, `booleanType` y `tokenType`.|
|appConfigKeyValue|Cadena|Valor de clave de configuración de la aplicación.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.appConfigurationSettingItem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.appConfigurationSettingItem",
  "appConfigKey": "String",
  "appConfigKeyType": "String",
  "appConfigKeyValue": "String"
}
```



