# <a name="omasettingbase64-resource-type"></a>Tipo de recurso omaSettingBase64

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Definición de Base64 de la configuración de OMA.

Hereda de [omaSetting](../resources/intune_deviceconfig_omasetting.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|cadena|Nombre para mostrar. Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)|
|descripción|Cadena|Descripción. Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)|
|omaUri|cadena|OMA. Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)|
|fileName|cadena|Nombre de archivo asociado a la propiedad de valor (*.cer | *.crt | *.p7b | *.bin).|
|valor|cadena|Valor. (Cadena codificada en Base64)|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.omaSettingBase64"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingBase64",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "fileName": "String",
  "value": "String"
}
```








