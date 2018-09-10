# <a name="softwareupdatestatussummary-resource-type"></a>Tipo de recurso softwareUpdateStatusSummary

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener softwareUpdateStatusSummary](../api/intune_deviceconfig_softwareupdatestatussummary_get.md)|[softwareUpdateStatusSummary](../resources/intune_deviceconfig_softwareupdatestatussummary.md)|Lea las propiedades y las relaciones del objeto [softwareUpdateStatusSummary](../resources/intune_deviceconfig_softwareupdatestatussummary.md).|
|[Actualizar softwareUpdateStatusSummary](../api/intune_deviceconfig_softwareupdatestatussummary_update.md)|[softwareUpdateStatusSummary](../resources/intune_deviceconfig_softwareupdatestatussummary.md)|Actualice las propiedades de un objeto [softwareUpdateStatusSummary](../resources/intune_deviceconfig_softwareupdatestatussummary.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|displayName|String|El nombre de la directiva.|
|compliantDeviceCount|Int32|Número de dispositivos compatibles.|
|nonCompliantDeviceCount|Int32|Número de dispositivos no compatibles.|
|remediatedDeviceCount|Int32|Número de dispositivos corregidos.|
|errorDeviceCount|Int32|Número de dispositivos con errores.|
|unknownDeviceCount|Int32|Número de dispositivos desconocidos.|
|conflictDeviceCount|Int32|Número de dispositivos en conflicto.|
|notApplicableDeviceCount|Int32|Número de dispositivos no aplicables.|
|compliantUserCount|Int32|Número de usuarios compatibles.|
|nonCompliantUserCount|Int32|Número de usuarios no compatibles.|
|remediatedUserCount|Int32|Número de usuarios corregidos.|
|errorUserCount|Int32|Número de usuarios con errores.|
|unknownUserCount|Int32|Número de usuarios desconocidos.|
|conflictUserCount|Int32|Número de usuarios en conflicto.|
|notApplicableUserCount|Int32|Número de usuarios no aplicables.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.softwareUpdateStatusSummary"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.softwareUpdateStatusSummary",
  "id": "String (identifier)",
  "displayName": "String",
  "compliantDeviceCount": 1024,
  "nonCompliantDeviceCount": 1024,
  "remediatedDeviceCount": 1024,
  "errorDeviceCount": 1024,
  "unknownDeviceCount": 1024,
  "conflictDeviceCount": 1024,
  "notApplicableDeviceCount": 1024,
  "compliantUserCount": 1024,
  "nonCompliantUserCount": 1024,
  "remediatedUserCount": 1024,
  "errorUserCount": 1024,
  "unknownUserCount": 1024,
  "conflictUserCount": 1024,
  "notApplicableUserCount": 1024
}
```








