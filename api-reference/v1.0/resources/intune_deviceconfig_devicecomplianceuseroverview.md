# <a name="devicecomplianceuseroverview-resource-type"></a>Tipo de recurso deviceComplianceUserOverview

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener deviceComplianceUserOverview](../api/intune_deviceconfig_devicecomplianceuseroverview_get.md)|[deviceComplianceUserOverview](../resources/intune_deviceconfig_devicecomplianceuseroverview.md)|Lea las propiedades y las relaciones del objeto [deviceComplianceUserOverview](../resources/intune_deviceconfig_devicecomplianceuseroverview.md).|
|[Actualizar deviceComplianceUserOverview](../api/intune_deviceconfig_devicecomplianceuseroverview_update.md)|[deviceComplianceUserOverview](../resources/intune_deviceconfig_devicecomplianceuseroverview.md)|Actualice las propiedades de un objeto [deviceComplianceUserOverview](../resources/intune_deviceconfig_devicecomplianceuseroverview.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|Clave de la entidad.|
|pendingCount|Int32|Número de usuarios pendientes|
|notApplicableCount|Int32|Número de usuarios no es aplicable.|
|successCount|Int32|Número de usuarios correctos|
|errorCount|Int32|Número de usuarios con error|
|failedCount|Int32|Número de usuarios erróneos|
|lastUpdateDateTime|DateTimeOffset|Última hora de actualización|
|configurationVersion|Int32|Versión de la directiva para esa información general|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceComplianceUserOverview"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceComplianceUserOverview",
  "id": "String (identifier)",
  "pendingCount": 1024,
  "notApplicableCount": 1024,
  "successCount": 1024,
  "errorCount": 1024,
  "failedCount": 1024,
  "lastUpdateDateTime": "String (timestamp)",
  "configurationVersion": 1024
}
```



