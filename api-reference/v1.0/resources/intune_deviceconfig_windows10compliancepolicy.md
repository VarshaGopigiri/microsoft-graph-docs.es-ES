# <a name="windows10compliancepolicy-resource-type"></a>Tipo de recurso windows10CompliancePolicy

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Esta clase contiene la configuración de cumplimiento para Windows 10.

Hereda de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar windows10CompliancePolicies](../api/intune_deviceconfig_windows10compliancepolicy_list.md)|Colección [windows10CompliancePolicy](../resources/intune_deviceconfig_windows10compliancepolicy.md)|Enumere las propiedades y las relaciones de los objetos [windows10CompliancePolicy](../resources/intune_deviceconfig_windows10compliancepolicy.md).|
|[Obtener windows10CompliancePolicy](../api/intune_deviceconfig_windows10compliancepolicy_get.md)|[windows10CompliancePolicy](../resources/intune_deviceconfig_windows10compliancepolicy.md)|Lea las propiedades y las relaciones del objeto [windows10CompliancePolicy](../resources/intune_deviceconfig_windows10compliancepolicy.md).|
|[Crear windows10CompliancePolicy](../api/intune_deviceconfig_windows10compliancepolicy_create.md)|[windows10CompliancePolicy](../resources/intune_deviceconfig_windows10compliancepolicy.md)|Cree un objeto [windows10CompliancePolicy](../resources/intune_deviceconfig_windows10compliancepolicy.md).|
|[Eliminar windows10CompliancePolicy](../api/intune_deviceconfig_windows10compliancepolicy_delete.md)|Ninguno|Elimina un [windows10CompliancePolicy](../resources/intune_deviceconfig_windows10compliancepolicy.md).|
|[Actualizar windows10CompliancePolicy](../api/intune_deviceconfig_windows10compliancepolicy_update.md)|[windows10CompliancePolicy](../resources/intune_deviceconfig_windows10compliancepolicy.md)|Actualice las propiedades de un objeto [windows10CompliancePolicy](../resources/intune_deviceconfig_windows10compliancepolicy.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)|
|description|Cadena|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)|
|displayName|Cadena|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)|
|versión|Int32|Versión de la configuración del dispositivo. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)|
|passwordRequired|Booleano|Exige una contraseña para desbloquear el dispositivo Windows.|
|passwordBlockSimple|Booleano|Indica si se va a bloquear la contraseña simple.|
|passwordRequiredToUnlockFromIdle|Booleano|Exige una contraseña para desbloquear el dispositivo inactivo.|
|passwordMinutesOfInactivityBeforeLock|Int32|Minutos de inactividad antes de que sea necesaria una contraseña.|
|passwordExpirationDays|Int32|La expiración de la contraseña en días.|
|passwordMinimumLength|Int32|La longitud mínima de contraseña.|
|passwordMinimumCharacterSetCount|Int32|El número de los juegos de caracteres necesarios en la contraseña.|
|passwordRequiredType|Cadena|El tipo de contraseña necesaria. Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.|
|passwordPreviousPasswordBlockCount|Int32|El número de contraseñas anteriores que se impedirá volver a usar.|
|requireHealthyDeviceReport|Booleano|Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos.|
|osMinimumVersion|Cadena|Versión mínima de Windows 10.|
|osMaximumVersion|Cadena|Versión máxima de Windows 10.|
|mobileOsMinimumVersion|Cadena|Versión mínima de Windows Phone.|
|mobileOsMaximumVersion|Cadena|Versión máxima de Windows Phone.|
|earlyLaunchAntiMalwareDriverEnabled|Booleano|Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; el controlador antimalware de inicio temprano está habilitado.|
|bitLockerEnabled|Booleano|Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; BitLocker está habilitado.|
|secureBootEnabled|Booleano|Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; el arranque seguro está habilitado.|
|codeIntegrityEnabled|Booleano|Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos.|
|storageRequireEncryption|Booleano|Exige el cifrado en dispositivos Windows.|

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
  "@odata.type": "microsoft.graph.windows10CompliancePolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windows10CompliancePolicy",
  "id": "String (identifier)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "version": 1024,
  "passwordRequired": true,
  "passwordBlockSimple": true,
  "passwordRequiredToUnlockFromIdle": true,
  "passwordMinutesOfInactivityBeforeLock": 1024,
  "passwordExpirationDays": 1024,
  "passwordMinimumLength": 1024,
  "passwordMinimumCharacterSetCount": 1024,
  "passwordRequiredType": "String",
  "passwordPreviousPasswordBlockCount": 1024,
  "requireHealthyDeviceReport": true,
  "osMinimumVersion": "String",
  "osMaximumVersion": "String",
  "mobileOsMinimumVersion": "String",
  "mobileOsMaximumVersion": "String",
  "earlyLaunchAntiMalwareDriverEnabled": true,
  "bitLockerEnabled": true,
  "secureBootEnabled": true,
  "codeIntegrityEnabled": true,
  "storageRequireEncryption": true
}
```



