# <a name="manageddeviceoverview-resource-type"></a>Tipo de recurso managedDeviceOverview

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Datos de resumen de los dispositivos administrados
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener managedDeviceOverview](../api/intune_devices_manageddeviceoverview_get.md)|[managedDeviceOverview](../resources/intune_devices_manageddeviceoverview.md)|Lea las propiedades y las relaciones del objeto [managedDeviceOverview](../resources/intune_devices_manageddeviceoverview.md).|
|[Actualizar managedDeviceOverview](../api/intune_devices_manageddeviceoverview_update.md)|[managedDeviceOverview](../resources/intune_devices_manageddeviceoverview.md)|Actualice las propiedades de un objeto [managedDeviceOverview](../resources/intune_devices_manageddeviceoverview.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único del resumen|
|enrolledDeviceCount|Int32|Número total de dispositivos inscritos. No incluye equipos administrados mediante el agente de PC de Intune|
|mdmEnrolledCount|Int32|El número de dispositivos inscritos en MDM|
|dualEnrolledDeviceCount|Int32|El número de dispositivos inscritos tanto en MDM como EAS|
|deviceOperatingSystemSummary|[deviceOperatingSystemSummary](../resources/intune_devices_deviceoperatingsystemsummary.md)|Resumen de sistemas operativos de dispositivos.|
|deviceExchangeAccessStateSummary|[deviceExchangeAccessStateSummary](../resources/intune_devices_deviceexchangeaccessstatesummary.md)|Distribución del estado de acceso de Exchange en Intune|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedDeviceOverview"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDeviceOverview",
  "id": "String (identifier)",
  "enrolledDeviceCount": 1024,
  "mdmEnrolledCount": 1024,
  "dualEnrolledDeviceCount": 1024,
  "deviceOperatingSystemSummary": {
    "@odata.type": "microsoft.graph.deviceOperatingSystemSummary",
    "androidCount": 1024,
    "iosCount": 1024,
    "macOSCount": 1024,
    "windowsMobileCount": 1024,
    "windowsCount": 1024,
    "unknownCount": 1024
  },
  "deviceExchangeAccessStateSummary": {
    "@odata.type": "microsoft.graph.deviceExchangeAccessStateSummary",
    "allowedDeviceCount": 1024,
    "blockedDeviceCount": 1024,
    "quarantinedDeviceCount": 1024,
    "unknownDeviceCount": 1024,
    "unavailableDeviceCount": 1024
  }
}
```








