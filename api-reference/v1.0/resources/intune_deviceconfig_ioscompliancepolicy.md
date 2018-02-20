# <a name="ioscompliancepolicy-resource-type"></a>Tipo de recurso iosCompliancePolicy

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Esta clase contiene la configuración de cumplimiento para iOS.

Hereda de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar iosCompliancePolicies](../api/intune_deviceconfig_ioscompliancepolicy_list.md)|Colección [iosCompliancePolicy](../resources/intune_deviceconfig_ioscompliancepolicy.md)|Enumere las propiedades y las relaciones de los objetos [iosCompliancePolicy](../resources/intune_deviceconfig_ioscompliancepolicy.md).|
|[Obtener iosCompliancePolicy](../api/intune_deviceconfig_ioscompliancepolicy_get.md)|[iosCompliancePolicy](../resources/intune_deviceconfig_ioscompliancepolicy.md)|Lea las propiedades y las relaciones del objeto [iosCompliancePolicy](../resources/intune_deviceconfig_ioscompliancepolicy.md).|
|[Crear iosCompliancePolicy](../api/intune_deviceconfig_ioscompliancepolicy_create.md)|[iosCompliancePolicy](../resources/intune_deviceconfig_ioscompliancepolicy.md)|Cree un objeto [iosCompliancePolicy](../resources/intune_deviceconfig_ioscompliancepolicy.md).|
|[Eliminar iosCompliancePolicy](../api/intune_deviceconfig_ioscompliancepolicy_delete.md)|Ninguna|Elimina un [iosCompliancePolicy](../resources/intune_deviceconfig_ioscompliancepolicy.md).|
|[Actualizar iosCompliancePolicy](../api/intune_deviceconfig_ioscompliancepolicy_update.md)|[iosCompliancePolicy](../resources/intune_deviceconfig_ioscompliancepolicy.md)|Actualice las propiedades de un objeto [iosCompliancePolicy](../resources/intune_deviceconfig_ioscompliancepolicy.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)|
|descripción|Cadena|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)|
|displayName|Cadena|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)|
|versión|Int32|Versión de la configuración del dispositivo. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)|
|passcodeBlockSimple|Booleano|Indica si quiere bloquear o no los códigos de acceso simples.|
|passcodeExpirationDays|Int32|Número de días antes de que expire el código de acceso. Valores válidos de 1 a 65535|
|passcodeMinimumLength|Int32|Longitud mínima de los códigos de acceso. Valores válidos de 4 a 14|
|passcodeMinutesOfInactivityBeforeLock|Int32|Minutos de inactividad antes de que sea necesario un código de acceso.|
|passcodePreviousPasscodeBlockCount|Int32|Número de códigos de acceso anteriores que bloquear. Valores válidos de 1 a 24|
|passcodeMinimumCharacterSetCount|Int32|El número de los juegos de caracteres necesarios en la contraseña.|
|passcodeRequiredType|Cadena|El tipo de código de acceso necesario. Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.|
|passcodeRequired|Booleano|Indica si quiere requerir o no un código de acceso.|
|osMinimumVersion|Cadena|Versión mínima de iOS.|
|osMaximumVersion|Cadena|Versión máxima de iOS.|
|securityBlockJailbrokenDevices|Booleano|No pueden usarse dispositivos con jailbreak o rooting.|
|deviceThreatProtectionEnabled|Booleano|Requerir que los dispositivos hayan habilitado la protección contra amenazas de dispositivo.|
|deviceThreatProtectionRequiredSecurityLevel|Cadena|Requerir que el nivel de riesgo mínimo de Mobile Threat Protection informe del no cumplimiento. Los valores posibles son: `unavailable`, `secured`, `low`, `medium`, `high` y `notSet`.|
|managedEmailProfileRequired|Booleano|Indica si quiere requerir o no un perfil de correo electrónico administrado.|

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
  "@odata.type": "microsoft.graph.iosCompliancePolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosCompliancePolicy",
  "id": "String (identifier)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "version": 1024,
  "passcodeBlockSimple": true,
  "passcodeExpirationDays": 1024,
  "passcodeMinimumLength": 1024,
  "passcodeMinutesOfInactivityBeforeLock": 1024,
  "passcodePreviousPasscodeBlockCount": 1024,
  "passcodeMinimumCharacterSetCount": 1024,
  "passcodeRequiredType": "String",
  "passcodeRequired": true,
  "osMinimumVersion": "String",
  "osMaximumVersion": "String",
  "securityBlockJailbrokenDevices": true,
  "deviceThreatProtectionEnabled": true,
  "deviceThreatProtectionRequiredSecurityLevel": "String",
  "managedEmailProfileRequired": true
}
```



