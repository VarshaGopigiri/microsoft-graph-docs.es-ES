# <a name="settingstatedevicesummary-resource-type"></a>Tipo de recurso settingStateDeviceSummary

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Directiva de cumplimiento y configuración del dispositivo para ver un resumen de estado de la configuración
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar settingStateDeviceSummaries](../api/intune_deviceconfig_settingstatedevicesummary_list.md)|Colección [settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md)|Enumere las propiedades y las relaciones de los objetos [settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md).|
|[Obtener settingStateDeviceSummary](../api/intune_deviceconfig_settingstatedevicesummary_get.md)|[settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md)|Lea las propiedades y las relaciones del objeto [settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md).|
|[Crear settingStateDeviceSummary](../api/intune_deviceconfig_settingstatedevicesummary_create.md)|[settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md)|Cree un objeto [settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md).|
|[Eliminar settingStateDeviceSummary](../api/intune_deviceconfig_settingstatedevicesummary_delete.md)|Ninguna|Elimina un [settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md).|
|[Actualizar settingStateDeviceSummary](../api/intune_deviceconfig_settingstatedevicesummary_update.md)|[settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md)|Actualice las propiedades de un objeto [settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|settingName|String|Nombre de la configuración|
|instancePath|String|Nombre de InstancePath para la configuración|
|unknownDeviceCount|Int32|Número de dispositivos desconocido para la configuración|
|notApplicableDeviceCount|Int32|Número de dispositivos no aplicables para la configuración|
|compliantDeviceCount|Int32|Número de dispositivos compatibles para la configuración|
|remediatedDeviceCount|Int32|Número de dispositivos compatibles para la configuración|
|nonCompliantDeviceCount|Int32|Número de dispositivos no compatibles para la configuración|
|errorDeviceCount|Int32|Número de errores de dispositivo para la configuración|
|conflictDeviceCount|Int32|Número de errores de conflictos de dispositivo para la configuración|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.settingStateDeviceSummary"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.settingStateDeviceSummary",
  "id": "String (identifier)",
  "settingName": "String",
  "instancePath": "String",
  "unknownDeviceCount": 1024,
  "notApplicableDeviceCount": 1024,
  "compliantDeviceCount": 1024,
  "remediatedDeviceCount": 1024,
  "nonCompliantDeviceCount": 1024,
  "errorDeviceCount": 1024,
  "conflictDeviceCount": 1024
}
```








