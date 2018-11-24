# <a name="windows10mobilecompliancepolicy-resource-type"></a>Tipo de recurso windows10MobileCompliancePolicy

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Esta clase contiene la configuración de cumplimiento para Windows 10 Mobile.

Hereda de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar windows10MobileCompliancePolicies](../api/intune_deviceconfig_windows10mobilecompliancepolicy_list.md)|Colección [windows10MobileCompliancePolicy](../resources/intune_deviceconfig_windows10mobilecompliancepolicy.md)|Enumere las propiedades y las relaciones de los objetos [windows10MobileCompliancePolicy](../resources/intune_deviceconfig_windows10mobilecompliancepolicy.md).|
|[Obtener windows10MobileCompliancePolicy](../api/intune_deviceconfig_windows10mobilecompliancepolicy_get.md)|[windows10MobileCompliancePolicy](../resources/intune_deviceconfig_windows10mobilecompliancepolicy.md)|Lea las propiedades y las relaciones del objeto [windows10MobileCompliancePolicy](../resources/intune_deviceconfig_windows10mobilecompliancepolicy.md).|
|[Crear windows10MobileCompliancePolicy](../api/intune_deviceconfig_windows10mobilecompliancepolicy_create.md)|[windows10MobileCompliancePolicy](../resources/intune_deviceconfig_windows10mobilecompliancepolicy.md)|Cree un objeto [windows10MobileCompliancePolicy](../resources/intune_deviceconfig_windows10mobilecompliancepolicy.md).|
|[Eliminar windows10MobileCompliancePolicy](../api/intune_deviceconfig_windows10mobilecompliancepolicy_delete.md)|Ninguna|Elimina un [windows10MobileCompliancePolicy](../resources/intune_deviceconfig_windows10mobilecompliancepolicy.md).|
|[Actualizar windows10MobileCompliancePolicy](../api/intune_deviceconfig_windows10mobilecompliancepolicy_update.md)|[windows10MobileCompliancePolicy](../resources/intune_deviceconfig_windows10mobilecompliancepolicy.md)|Actualice las propiedades de un objeto [windows10MobileCompliancePolicy](../resources/intune_deviceconfig_windows10mobilecompliancepolicy.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).|
|descripción|Cadena|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).|
|displayName|Cadena|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).|
|versión|Int32|Versión de la configuración del dispositivo. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).|
|passwordRequired|Booleano|Exigir una contraseña para desbloquear el dispositivo de Windows Phone.|
|passwordBlockSimple|Booleano|Si quiere bloquear o no la sincronización del calendario.|
|passwordMinimumLength|Int32|Longitud mínima de la contraseña. Valores válidos de 4 a 16|
|passwordMinimumCharacterSetCount|Int32|El número de los juegos de caracteres necesarios en la contraseña.|
|passwordRequiredType|[requiredPasswordType](../resources/intune_deviceconfig_requiredpasswordtype.md)|Tipo de contraseña necesaria. Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.|
|passwordPreviousPasswordBlockCount|Int32|El número de contraseñas anteriores que se impedirá volver a usar.|
|passwordExpirationDays|Int32|Número de días antes de que expire la contraseña. Valores válidos de 1 a 255|
|passwordMinutesOfInactivityBeforeLock|Int32|Minutos de inactividad antes de que sea necesaria una contraseña.|
|passwordRequireToUnlockFromIdle|Booleano|Exigir una contraseña para desbloquear el dispositivo inactivo.|
|osMinimumVersion|Cadena|Versión mínima de Windows Phone.|
|osMaximumVersion|Cadena|Versión máxima de Windows Phone.|
|earlyLaunchAntiMalwareDriverEnabled|Booleano|Exigir que la atestación del mantenimiento de dispositivos Windows notifique los dispositivos como correctos; el controlador antimalware de inicio temprano está habilitado.|
|bitLockerEnabled|Booleano|Exigir que la atestación del mantenimiento de dispositivos Windows notifique los dispositivos como correctos; BitLocker está habilitado.|
|secureBootEnabled|Booleano|Exigir que la atestación del mantenimiento de dispositivos Windows notifique los dispositivos como correctos; el arranque seguro está habilitado.|
|codeIntegrityEnabled|Booleano|Exigir que la atestación del mantenimiento de dispositivos Windows notifique los dispositivos como correctos.|
|storageRequireEncryption|Booleano|Exigir el cifrado en dispositivos Windows.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|scheduledActionsForRule|Colección [deviceComplianceScheduledActionForRule](../resources/intune_deviceconfig_devicecompliancescheduledactionforrule.md)|La lista de acción programada para esta regla. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)|
|deviceStatuses|Colección [deviceComplianceDeviceStatus](../resources/intune_deviceconfig_devicecompliancedevicestatus.md)|Lista de DeviceComplianceDeviceStatus. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)|
|userStatuses|Colección [deviceComplianceUserStatus](../resources/intune_deviceconfig_devicecomplianceuserstatus.md)|Lista de DeviceComplianceUserStatus. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)|
|deviceStatusOverview|[deviceComplianceDeviceOverview](../resources/intune_deviceconfig_devicecompliancedeviceoverview.md)|Información general sobre el estado de dispositivos del cumplimiento de dispositivo. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)|
|userStatusOverview|[deviceComplianceUserOverview](../resources/intune_deviceconfig_devicecomplianceuseroverview.md)|Información general sobre el estado de usuarios del cumplimiento de dispositivo. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)|
|deviceSettingStateSummaries|Colección [settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md)|Resumen de dispositivo sobre el estado de configuración de cumplimiento. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)|
|asignaciones|Colección [deviceCompliancePolicyAssignment](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md)|El conjunto de asignaciones para esta directiva de cumplimiento. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windows10MobileCompliancePolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windows10MobileCompliancePolicy",
  "id": "String (identifier)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "version": 1024,
  "passwordRequired": true,
  "passwordBlockSimple": true,
  "passwordMinimumLength": 1024,
  "passwordMinimumCharacterSetCount": 1024,
  "passwordRequiredType": "String",
  "passwordPreviousPasswordBlockCount": 1024,
  "passwordExpirationDays": 1024,
  "passwordMinutesOfInactivityBeforeLock": 1024,
  "passwordRequireToUnlockFromIdle": true,
  "osMinimumVersion": "String",
  "osMaximumVersion": "String",
  "earlyLaunchAntiMalwareDriverEnabled": true,
  "bitLockerEnabled": true,
  "secureBootEnabled": true,
  "codeIntegrityEnabled": true,
  "storageRequireEncryption": true
}
```



