# <a name="iosdevicetype-resource-type"></a>Tipo de recurso iosDeviceType

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades de los posibles tipos de dispositivo iOS en los que se puede ejecutar la aplicación móvil.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|iPad|Booleano|Si la aplicación debe ejecutarse en iPad.|
|iPhoneAndIPod|Booleano|Si la aplicación debe ejecutarse en iPhone y iPod.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosDeviceType"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.iosDeviceType",
  "iPad": true,
  "iPhoneAndIPod": true
}
```



