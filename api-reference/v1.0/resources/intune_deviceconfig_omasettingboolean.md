# <a name="omasettingboolean-resource-type"></a>Tipo de recurso omaSettingBoolean

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Definición booleana de la configuración de OMA.

Hereda de [omaSetting](../resources/intune_deviceconfig_omasetting.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|cadena|Nombre para mostrar. Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)|
|descripción|String|Descripción. Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)|
|omaUri|cadena|OMA. Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)|
|valor|Booleano|Valor.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.omaSettingBoolean"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingBoolean",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "value": true
}
```








