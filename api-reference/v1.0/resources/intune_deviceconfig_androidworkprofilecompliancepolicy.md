# <a name="androidworkprofilecompliancepolicy-resource-type"></a>tipo de recurso androidWorkProfileCompliancePolicy

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Esta clase contiene la configuración de cumplimiento para Android perfil de trabajo.

Hereda de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista androidWorkProfileCompliancePolicies](../api/intune_deviceconfig_androidworkprofilecompliancepolicy_list.md)|colección de [androidWorkProfileCompliancePolicy](../resources/intune_deviceconfig_androidworkprofilecompliancepolicy.md)|Propiedades de la lista y relaciones de los objetos [androidWorkProfileCompliancePolicy](../resources/intune_deviceconfig_androidworkprofilecompliancepolicy.md) .|
|[Obtener androidWorkProfileCompliancePolicy](../api/intune_deviceconfig_androidworkprofilecompliancepolicy_get.md)|[androidWorkProfileCompliancePolicy](../resources/intune_deviceconfig_androidworkprofilecompliancepolicy.md)|Leer las propiedades y las relaciones del objeto [androidWorkProfileCompliancePolicy](../resources/intune_deviceconfig_androidworkprofilecompliancepolicy.md) .|
|[Crear androidWorkProfileCompliancePolicy](../api/intune_deviceconfig_androidworkprofilecompliancepolicy_create.md)|[androidWorkProfileCompliancePolicy](../resources/intune_deviceconfig_androidworkprofilecompliancepolicy.md)|Crear un nuevo objeto [androidWorkProfileCompliancePolicy](../resources/intune_deviceconfig_androidworkprofilecompliancepolicy.md) .|
|[Eliminar androidWorkProfileCompliancePolicy](../api/intune_deviceconfig_androidworkprofilecompliancepolicy_delete.md)|Ninguno|Elimina un [androidWorkProfileCompliancePolicy](../resources/intune_deviceconfig_androidworkprofilecompliancepolicy.md).|
|[Actualizar androidWorkProfileCompliancePolicy](../api/intune_deviceconfig_androidworkprofilecompliancepolicy_update.md)|[androidWorkProfileCompliancePolicy](../resources/intune_deviceconfig_androidworkprofilecompliancepolicy.md)|Actualizar las propiedades de un objeto [androidWorkProfileCompliancePolicy](../resources/intune_deviceconfig_androidworkprofilecompliancepolicy.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).|
|descripción|String|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).|
|displayName|String|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).|
|version|Int32|Versión de la configuración del dispositivo. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).|
|passwordRequired|Booleano|Exigir una contraseña para desbloquear el dispositivo.|
|passwordMinimumLength|Int32|Longitud mínima de la contraseña. Valores válidos de 4 a 16|
|passwordRequiredType|[androidRequiredPasswordType](../resources/intune_deviceconfig_androidrequiredpasswordtype.md)|Tipo de caracteres de contraseña. Los valores posibles son: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex` y `any`.|
|passwordMinutesOfInactivityBeforeLock|Int32|Minutos de inactividad antes de que sea necesaria una contraseña.|
|passwordExpirationDays|Int32|Número de días antes de que expire la contraseña. Valores válidos de 1 a 365|
|passwordPreviousPasswordBlockCount|Int32|Número de contraseñas anteriores que bloquear.|
|securityPreventInstallAppsFromUnknownSources|Booleano|Exigir que los dispositivos impidan la instalación de aplicaciones de orígenes desconocidos.|
|securityDisableUsbDebugging|Booleano|Deshabilitar la depuración USB en dispositivos Android.|
|securityRequireVerifyApps|Booleano|Exigir que la característica Verificar aplicaciones de Android esté activada.|
|deviceThreatProtectionEnabled|Booleano|Exigir que los dispositivos hayan habilitado la protección contra amenazas de dispositivo.|
|deviceThreatProtectionRequiredSecurityLevel|[deviceThreatProtectionLevel](../resources/intune_deviceconfig_devicethreatprotectionlevel.md)|Exigir que el nivel de riesgo mínimo de Mobile Threat Protection informe del no cumplimiento. Los valores posibles son: `unavailable`, `secured`, `low`, `medium`, `high` y `notSet`.|
|securityBlockJailbrokenDevices|Booleano|No pueden usarse dispositivos con jailbreak o rooting.|
|osMinimumVersion|String|Versión mínima de Android.|
|osMaximumVersion|String|Versión máxima de Android.|
|minAndroidSecurityPatchLevel|String|Nivel de revisión de seguridad mínimo de Android.|
|storageRequireEncryption|Booleano|Exigir cifrado en dispositivos Android.|
|securityRequireSafetyNetAttestationBasicIntegrity|Booleano|Exigir que el dispositivo supere la comprobación de integridad básica de SafetyNet.|
|securityRequireSafetyNetAttestationCertifiedDevice|Booleano|Exigir que el dispositivo supere la comprobación de dispositivos certificados de SafetyNet.|
|securityRequireGooglePlayServices|Booleano|Exigir que Google Play Services esté instalado y habilitado en el dispositivo.|
|securityRequireUpToDateSecurityProviders|Booleano|Exigir que el dispositivo tenga los proveedores de seguridad actualizados. El dispositivo requerirá que Google Play Services esté instalado y habilitado.|
|securityRequireCompanyPortalAppIntegrity|Booleano|Requerir que el dispositivo pase la comprobación de integridad en tiempo de ejecución de la aplicación del cliente del Portal de empresa.|

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
  "@odata.type": "microsoft.graph.androidWorkProfileCompliancePolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidWorkProfileCompliancePolicy",
  "id": "String (identifier)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "version": 1024,
  "passwordRequired": true,
  "passwordMinimumLength": 1024,
  "passwordRequiredType": "String",
  "passwordMinutesOfInactivityBeforeLock": 1024,
  "passwordExpirationDays": 1024,
  "passwordPreviousPasswordBlockCount": 1024,
  "securityPreventInstallAppsFromUnknownSources": true,
  "securityDisableUsbDebugging": true,
  "securityRequireVerifyApps": true,
  "deviceThreatProtectionEnabled": true,
  "deviceThreatProtectionRequiredSecurityLevel": "String",
  "securityBlockJailbrokenDevices": true,
  "osMinimumVersion": "String",
  "osMaximumVersion": "String",
  "minAndroidSecurityPatchLevel": "String",
  "storageRequireEncryption": true,
  "securityRequireSafetyNetAttestationBasicIntegrity": true,
  "securityRequireSafetyNetAttestationCertifiedDevice": true,
  "securityRequireGooglePlayServices": true,
  "securityRequireUpToDateSecurityProviders": true,
  "securityRequireCompanyPortalAppIntegrity": true
}
```



