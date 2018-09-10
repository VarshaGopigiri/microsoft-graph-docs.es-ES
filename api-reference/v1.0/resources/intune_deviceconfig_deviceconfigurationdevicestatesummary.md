# <a name="deviceconfigurationdevicestatesummary-resource-type"></a>Tipo de recurso deviceConfigurationDeviceStateSummary

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener deviceConfigurationDeviceStateSummary](../api/intune_deviceconfig_deviceconfigurationdevicestatesummary_get.md)|[deviceConfigurationDeviceStateSummary](../resources/intune_deviceconfig_deviceconfigurationdevicestatesummary.md)|Lea las propiedades y las relaciones del objeto [deviceConfigurationDeviceStateSummary](../resources/intune_deviceconfig_deviceconfigurationdevicestatesummary.md).|
|[Actualizar deviceConfigurationDeviceStateSummary](../api/intune_deviceconfig_deviceconfigurationdevicestatesummary_update.md)|[deviceConfigurationDeviceStateSummary](../resources/intune_deviceconfig_deviceconfigurationdevicestatesummary.md)|Actualice las propiedades de un objeto [deviceConfigurationDeviceStateSummary](../resources/intune_deviceconfig_deviceconfigurationdevicestatesummary.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|unknownDeviceCount|Int32|Número de dispositivos desconocidos|
|notApplicableDeviceCount|Int32|Número de dispositivos no aplicables|
|compliantDeviceCount|Int32|Número de dispositivos compatibles|
|remediatedDeviceCount|Int32|Número de dispositivos corregidos|
|nonCompliantDeviceCount|Int32|Número de dispositivos no compatibles|
|errorDeviceCount|Int32|Número de dispositivos con error|
|conflictDeviceCount|Int32|Número de dispositivos en conflicto|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceConfigurationDeviceStateSummary"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceConfigurationDeviceStateSummary",
  "id": "String (identifier)",
  "unknownDeviceCount": 1024,
  "notApplicableDeviceCount": 1024,
  "compliantDeviceCount": 1024,
  "remediatedDeviceCount": 1024,
  "nonCompliantDeviceCount": 1024,
  "errorDeviceCount": 1024,
  "conflictDeviceCount": 1024
}
```








