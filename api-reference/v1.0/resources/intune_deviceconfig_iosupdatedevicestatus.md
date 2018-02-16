# <a name="iosupdatedevicestatus-resource-type"></a>Tipo de recurso iosUpdateDeviceStatus

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar iosUpdateDeviceStatuses](../api/intune_deviceconfig_iosupdatedevicestatus_list.md)|Colección [iosUpdateDeviceStatus](../resources/intune_deviceconfig_iosupdatedevicestatus.md)|Enumere las propiedades y las relaciones de los objetos [iosUpdateDeviceStatus](../resources/intune_deviceconfig_iosupdatedevicestatus.md).|
|[Obtener iosUpdateDeviceStatus](../api/intune_deviceconfig_iosupdatedevicestatus_get.md)|[iosUpdateDeviceStatus](../resources/intune_deviceconfig_iosupdatedevicestatus.md)|Lea las propiedades y las relaciones del objeto [iosUpdateDeviceStatus](../resources/intune_deviceconfig_iosupdatedevicestatus.md).|
|[Crear iosUpdateDeviceStatus](../api/intune_deviceconfig_iosupdatedevicestatus_create.md)|[iosUpdateDeviceStatus](../resources/intune_deviceconfig_iosupdatedevicestatus.md)|Cree un objeto [iosUpdateDeviceStatus](../resources/intune_deviceconfig_iosupdatedevicestatus.md).|
|[Eliminar iosUpdateDeviceStatus](../api/intune_deviceconfig_iosupdatedevicestatus_delete.md)|Ninguna|Elimina un [iosUpdateDeviceStatus](../resources/intune_deviceconfig_iosupdatedevicestatus.md).|
|[Actualizar iosUpdateDeviceStatus](../api/intune_deviceconfig_iosupdatedevicestatus_update.md)|[iosUpdateDeviceStatus](../resources/intune_deviceconfig_iosupdatedevicestatus.md)|Actualice las propiedades de un objeto [iosUpdateDeviceStatus](../resources/intune_deviceconfig_iosupdatedevicestatus.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|Clave de la entidad.|
|installStatus|cadena|Estado de la instalación del informe de directiva. Los valores posibles son: `success`, `available`, `idle`, `downloading`, `downloadFailed`, `downloadRequiresComputer`, `downloadInsufficientSpace`, `downloadInsufficientPower`, `downloadInsufficientNetwork`, `installing`, `installInsufficientSpace`, `installInsufficientPower`, `installPhoneCallInProgress`, `installFailed`, `notSupportedOperation` y `sharedDeviceUserLoggedInError`.|
|osVersion|cadena|La versión del dispositivo que se está notificando.|
|deviceId|cadena|El identificador del dispositivo que se está notificando.|
|userId|cadena|El identificador del usuario que se está notificando.|
|deviceDisplayName|cadena|Nombre de dispositivo de DevicePolicyStatus.|
|userName|cadena|El nombre de usuario que se está notificando|
|deviceModel|cadena|El modelo de dispositivo que se está notificando|
|complianceGracePeriodExpirationDateTime|DateTimeOffset|La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo|
|estado|cadena|Estado de cumplimiento del informe de directiva. Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error` y `conflict`.|
|lastReportedDateTime|DateTimeOffset|Fecha y hora de la última modificación del informe de directiva.|
|userPrincipalName|cadena|UserPrincipalName.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosUpdateDeviceStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosUpdateDeviceStatus",
  "id": "String (identifier)",
  "installStatus": "String",
  "osVersion": "String",
  "deviceId": "String",
  "userId": "String",
  "deviceDisplayName": "String",
  "userName": "String",
  "deviceModel": "String",
  "complianceGracePeriodExpirationDateTime": "String (timestamp)",
  "status": "String",
  "lastReportedDateTime": "String (timestamp)",
  "userPrincipalName": "String"
}
```



