# <a name="omasettingstringxml-resource-type"></a>Tipo de recurso omaSettingStringXml

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Definición de la cadena XML de la configuración de OMA.

Hereda de [omaSetting](../resources/intune_deviceconfig_omasetting.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|cadena|Nombre para mostrar. Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)|
|descripción|cadena|Descripción. Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)|
|omaUri|cadena|OMA. Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)|
|fileName|cadena|Nombre de archivo asociado a la propiedad de valor (*.xml).|
|valor|Binario|Valor. (Matriz de bytes codificada UTF8)|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.omaSettingStringXml"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingStringXml",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "fileName": "String",
  "value": "binary"
}
```



