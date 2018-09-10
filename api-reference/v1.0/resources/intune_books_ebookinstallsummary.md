# <a name="ebookinstallsummary-resource-type"></a>Tipo de recurso eBookInstallSummary

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades del resumen de la instalación de un libro para un dispositivo.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener eBookInstallSummary](../api/intune_books_ebookinstallsummary_get.md)|[eBookInstallSummary](../resources/intune_books_ebookinstallsummary.md)|Lea las propiedades y las relaciones del objeto [eBookInstallSummary](../resources/intune_books_ebookinstallsummary.md).|
|[Actualizar eBookInstallSummary](../api/intune_books_ebookinstallsummary_update.md)|[eBookInstallSummary](../resources/intune_books_ebookinstallsummary.md)|Actualice las propiedades de un objeto [eBookInstallSummary](../resources/intune_books_ebookinstallsummary.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|installedDeviceCount|Int32|Número de dispositivos que han instalado correctamente este libro.|
|failedDeviceCount|Int32|Número de dispositivos que no han podido instalar este libro.|
|notInstalledDeviceCount|Int32|Número de dispositivos que no han instalado este libro.|
|installedUserCount|Int32|Número de usuarios cuyos dispositivos al completo han instalado este libro.|
|failedUserCount|Int32|Número de usuarios que tienen 1 o más dispositivos que no han podido instalar este libro.|
|notInstalledUserCount|Int32|Número de usuarios que no han instalado este libro.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.eBookInstallSummary"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.eBookInstallSummary",
  "id": "String (identifier)",
  "installedDeviceCount": 1024,
  "failedDeviceCount": 1024,
  "notInstalledDeviceCount": 1024,
  "installedUserCount": 1024,
  "failedUserCount": 1024,
  "notInstalledUserCount": 1024
}
```








