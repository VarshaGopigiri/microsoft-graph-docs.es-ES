# <a name="macoscompliancepolicy-resource-type"></a>Tipo de recurso macOSCompliancePolicy

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Esta clase contiene la configuración de cumplimiento para Mac OS.

Hereda de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar macOSCompliancePolicies](../api/intune_deviceconfig_macoscompliancepolicy_list.md)|Colección [macOSCompliancePolicy](../resources/intune_deviceconfig_macoscompliancepolicy.md)|Enumere las propiedades y las relaciones de los objetos [macOSCompliancePolicy](../resources/intune_deviceconfig_macoscompliancepolicy.md).|
|[Obtener macOSCompliancePolicy](../api/intune_deviceconfig_macoscompliancepolicy_get.md)|[macOSCompliancePolicy](../resources/intune_deviceconfig_macoscompliancepolicy.md)|Lea las propiedades y las relaciones del objeto [macOSCompliancePolicy](../resources/intune_deviceconfig_macoscompliancepolicy.md).|
|[Crear macOSCompliancePolicy](../api/intune_deviceconfig_macoscompliancepolicy_create.md)|[macOSCompliancePolicy](../resources/intune_deviceconfig_macoscompliancepolicy.md)|Cree un objeto [macOSCompliancePolicy](../resources/intune_deviceconfig_macoscompliancepolicy.md).|
|[Eliminar macOSCompliancePolicy](../api/intune_deviceconfig_macoscompliancepolicy_delete.md)|Ninguno|Elimina un [macOSCompliancePolicy](../resources/intune_deviceconfig_macoscompliancepolicy.md).|
|[Actualizar macOSCompliancePolicy](../api/intune_deviceconfig_macoscompliancepolicy_update.md)|[macOSCompliancePolicy](../resources/intune_deviceconfig_macoscompliancepolicy.md)|Actualice las propiedades de un objeto [macOSCompliancePolicy](../resources/intune_deviceconfig_macoscompliancepolicy.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id.|Cadena|Clave de la entidad. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).|
|descripción|Cadena|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).|
|displayName|Cadena|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).|
|versión|Int32|Versión de la configuración del dispositivo. Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).|
|passwordRequired|Booleano|Si quiere requerir o no una contraseña.|
|passwordBlockSimple|Booleano|Indica si se van a bloquear las contraseñas simples.|
|passwordExpirationDays|Int32|Número de días antes de que expire la contraseña. Valores válidos de 1 a 65535|
|passwordMinimumLength|Int32|Longitud mínima de la contraseña. Valores válidos de 4 a 14|
|passwordMinutesOfInactivityBeforeLock|Int32|Minutos de inactividad antes de que sea necesaria una contraseña.|
|passwordPreviousPasswordBlockCount|Int32|Número de contraseñas anteriores que bloquear. Valores válidos de 1 a 24.|
|passwordMinimumCharacterSetCount|Int32|Número de juegos de caracteres necesarios en la contraseña.|
|passwordRequiredType|[requiredPasswordType](../resources/intune_deviceconfig_requiredpasswordtype.md)|El tipo de contraseña requerida. Los valores posibles son: `deviceDefault`, `alphanumeric`, `numeric`.|
|osMinimumVersion|Cadena|Versión mínima de iOS.|
|osMaximumVersion|Cadena|Versión máxima de iOS.|
|systemIntegrityProtectionEnabled|Booleano|Requiere que los dispositivos hayan habilitado la protección de integridad del sistema.|
|deviceThreatProtectionEnabled|Booleano|Requiere que los dispositivos hayan habilitado la protección contra amenazas de dispositivo.|
|deviceThreatProtectionRequiredSecurityLevel|[deviceThreatProtectionLevel](../resources/intune_deviceconfig_devicethreatprotectionlevel.md)|Requerir que el nivel de riesgo mínimo de la Protección contra amenazas móviles informe de un incumplimiento. Los valores posibles son: `unavailable`, `secured`, `low`, `medium`, `high`, `notSet`.|
|storageRequireEncryption|Booleano|Exige el cifrado en dispositivos Mac OS.|
|firewallEnabled|Booleano|Si el firewall se debe habilitar o no.|
|firewallBlockAllIncoming|Booleano|Corresponde a la opción "Bloquear todas las conexiones entrantes".|
|firewallEnableStealthMode|Booleano|Corresponde a "Habilitar modo silencioso".|

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
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.deviceCompliancePolicy",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.macOSCompliancePolicy"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.macOSCompliancePolicy",
  "id": "String (identifier)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "version": 1024,
  "passwordRequired": true,
  "passwordBlockSimple": true,
  "passwordExpirationDays": 1024,
  "passwordMinimumLength": 1024,
  "passwordMinutesOfInactivityBeforeLock": 1024,
  "passwordPreviousPasswordBlockCount": 1024,
  "passwordMinimumCharacterSetCount": 1024,
  "passwordRequiredType": "String",
  "osMinimumVersion": "String",
  "osMaximumVersion": "String",
  "systemIntegrityProtectionEnabled": true,
  "deviceThreatProtectionEnabled": true,
  "deviceThreatProtectionRequiredSecurityLevel": "String",
  "storageRequireEncryption": true,
  "firewallEnabled": true,
  "firewallBlockAllIncoming": true,
  "firewallEnableStealthMode": true
}
```








