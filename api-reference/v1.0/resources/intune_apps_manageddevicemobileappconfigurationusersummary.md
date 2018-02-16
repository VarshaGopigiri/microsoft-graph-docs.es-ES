# <a name="manageddevicemobileappconfigurationusersummary-resource-type"></a>Tipo de recurso managedDeviceMobileAppConfigurationUserSummary

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades, las propiedades heredadas y las acciones para un resumen de estado de usuario de la configuración de aplicaciones móviles de MDM.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener managedDeviceMobileAppConfigurationUserSummary](../api/intune_apps_manageddevicemobileappconfigurationusersummary_get.md)|[managedDeviceMobileAppConfigurationUserSummary](../resources/intune_apps_manageddevicemobileappconfigurationusersummary.md)|Lea las propiedades y las relaciones del objeto [managedDeviceMobileAppConfigurationUserSummary](../resources/intune_apps_manageddevicemobileappconfigurationusersummary.md).|
|[Actualizar managedDeviceMobileAppConfigurationUserSummary](../api/intune_apps_manageddevicemobileappconfigurationusersummary_update.md)|[managedDeviceMobileAppConfigurationUserSummary](../resources/intune_apps_manageddevicemobileappconfigurationusersummary.md)|Actualice las propiedades de un objeto [managedDeviceMobileAppConfigurationUserSummary](../resources/intune_apps_manageddevicemobileappconfigurationusersummary.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|Clave de la entidad.|
|pendingCount|Int32|Número de usuarios pendientes|
|notApplicableCount|Int32|Número de dispositivos no aplicables|
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
  "@odata.type": "microsoft.graph.managedDeviceMobileAppConfigurationUserSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationUserSummary",
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



