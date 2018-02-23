# <a name="manageddevice-resource-type"></a>Tipo de recurso managedDevice

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Dispositivos administrados o inscritos previamente a través de Intune
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar managedDevices](../api/intune_devices_manageddevice_list.md)|Colección [managedDevice](../resources/intune_devices_manageddevice.md)|Enumere las propiedades y las relaciones de los objetos [managedDevice](../resources/intune_devices_manageddevice.md).|
|[Obtener managedDevice](../api/intune_devices_manageddevice_get.md)|[managedDevice](../resources/intune_devices_manageddevice.md)|Lea las propiedades y las relaciones del objeto [managedDevice](../resources/intune_devices_manageddevice.md).|
|[Crear managedDevice](../api/intune_devices_manageddevice_create.md)|[managedDevice](../resources/intune_devices_manageddevice.md)|Cree un objeto [managedDevice](../resources/intune_devices_manageddevice.md).|
|[Eliminar managedDevice](../api/intune_devices_manageddevice_delete.md)|Ninguno|Elimina un [managedDevice](../resources/intune_devices_manageddevice.md).|
|[Actualizar managedDevice](../api/intune_devices_manageddevice_update.md)|[managedDevice](../resources/intune_devices_manageddevice.md)|Actualice las propiedades de un objeto [managedDevice](../resources/intune_devices_manageddevice.md).|
|[Acción retire](../api/intune_devices_manageddevice_retire.md)|Ninguno|Retirar un dispositivo|
|[Acción wipe](../api/intune_devices_manageddevice_wipe.md)|Ninguno|Eliminar los datos de un dispositivo|
|[Acción resetPasscode](../api/intune_devices_manageddevice_resetpasscode.md)|Ninguno|Restablecer código de acceso|
|[Acción remoteLock](../api/intune_devices_manageddevice_remotelock.md)|Ninguno|Bloqueo remoto|
|[Acción requestRemoteAssistance](../api/intune_devices_manageddevice_requestremoteassistance.md)|Ninguno|Solicitar asistencia remota|
|[Acción disableLostMode](../api/intune_devices_manageddevice_disablelostmode.md)|Ninguno|Deshabilitar modo Perdido|
|[Acción locateDevice](../api/intune_devices_manageddevice_locatedevice.md)|Ninguno|Buscar un dispositivo|
|[Acción bypassActivationLock](../api/intune_devices_manageddevice_bypassactivationlock.md)|Ninguno|Omitir bloqueo de activación|
|[Acción rebootNow](../api/intune_devices_manageddevice_rebootnow.md)|Ninguno|Reiniciar el dispositivo|
|[Acción shutDown](../api/intune_devices_manageddevice_shutdown.md)|Ninguno|Apagar el dispositivo|
|[Acción recoverPasscode](../api/intune_devices_manageddevice_recoverpasscode.md)|Ninguno|Recuperar código de acceso|
|[Acción cleanWindowsDevice](../api/intune_devices_manageddevice_cleanwindowsdevice.md)|Ninguno|Limpiar dispositivo Windows|
|[Acción logoutSharedAppleDeviceActiveUser](../api/intune_devices_manageddevice_logoutsharedappledeviceactiveuser.md)|Ninguno|Cerrar la sesión del usuario activo del dispositivo Apple compartido|
|[Acción deleteUserFromSharedAppleDevice](../api/intune_devices_manageddevice_deleteuserfromsharedappledevice.md)|Ninguno|Eliminar usuario del dispositivo Apple compartido|
|[Acción syncDevice](../api/intune_devices_manageddevice_syncdevice.md)|Ninguno|Todavía no documentado|
|[Acción windowsDefenderScan](../api/intune_devices_manageddevice_windowsdefenderscan.md)|Ninguno|Todavía no documentado|
|[Acción windowsDefenderUpdateSignatures](../api/intune_devices_manageddevice_windowsdefenderupdatesignatures.md)|Ninguno|Todavía no documentado|
|[Acción updateWindowsDeviceAccount](../api/intune_devices_manageddevice_updatewindowsdeviceaccount.md)|Ninguno|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Identificador único del dispositivo|
|userId|Cadena|Identificador único para el usuario asociado con el dispositivo|
|deviceName|Cadena|Nombre del dispositivo|
|deviceActionResults|Colección [deviceActionResult](../resources/intune_devices_deviceactionresult.md)|Lista de objetos deviceActionResult ComplexType.|
|enrolledDateTime|DateTimeOffset|Tiempo de inscripción del dispositivo.|
|lastSyncDateTime|DateTimeOffset|La fecha y la hora en que el dispositivo completó por última vez una sincronización correcta con Intune.|
|operatingSystem|Cadena|Sistema operativo del dispositivo. Windows, iOS, etc.|
|complianceState|Cadena|Estado de cumplimiento del dispositivo. Los valores posibles son: `unknown`, `compliant`, `noncompliant`, `conflict`, `error`, `inGracePeriod` y `configManager`.|
|jailBroken|Cadena|Si el dispositivo está liberado o tiene acceso raíz.|
|managementAgent|Cadena|Canal de administración del dispositivo. Intune, EAS, etc. Los valores posibles son: `eas`, `mdm`, `easMdm`, `intuneClient`, `easIntuneClient`, `configurationManagerClient`, `configurationManagerClientMdm`, `configurationManagerClientMdmEas`, `unknown`, `jamf` y `googleCloudDevicePolicyController`.|
|osVersion|Cadena|Versión del sistema operativo del dispositivo.|
|easActivated|Booleano|Si el dispositivo tiene Exchange ActiveSync activado.|
|easDeviceId|Cadena|Identificador de Exchange ActiveSync del dispositivo.|
|easActivationDateTime|DateTimeOffset|Tiempo de activación de Exchange ActivationSync del dispositivo.|
|azureADRegistered|Booleano|Si el dispositivo está registrado en Azure Active Directory.|
|deviceEnrollmentType|Cadena|Tipo de inscripción del dispositivo. Los valores posibles son: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin` y `windowsCoManagement`.|
|activationLockBypassCode|Cadena|Código que permite que se omita el bloqueo de activación en un dispositivo.|
|emailAddress|Cadena|Direcciones de correo electrónico para el usuario asociado con el dispositivo|
|azureADDeviceId|Cadena|El identificador único del dispositivo de Azure Active Directory. Solo lectura.|
|deviceRegistrationState|Cadena|El estado de registro del dispositivo. Los valores posibles son: `notRegistered`, `registered`, `revoked`, `keyConflict`, `approvalPending`, `certificateReset`, `notRegisteredPendingEnrollment` y `unknown`.|
|deviceCategoryDisplayName|Cadena|Nombre para mostrar de la categoría de dispositivo.|
|isSupervised|Booleano|Estado supervisado del dispositivo|
|exchangeLastSuccessfulSyncDateTime|DateTimeOffset|Última vez que el dispositivo contactó con Exchange.|
|exchangeAccessState|Cadena|El estado de acceso del dispositivo en Exchange. Los valores posibles son: `none`, `unknown`, `allowed`, `blocked` y `quarantined`.|
|exchangeAccessStateReason|Cadena|Motivo del estado de acceso del dispositivo en Exchange. Los valores posibles son: `none`, `unknown`, `exchangeGlobalRule`, `exchangeIndividualRule`, `exchangeDeviceRule`, `exchangeUpgrade`, `exchangeMailboxPolicy`, `other`, `compliant`, `notCompliant`, `notEnrolled`, `unknownLocation`, `mfaRequired`, `azureADBlockDueToAccessPolicy`, `compromisedPassword` y `deviceNotKnownWithManagedApp`.|
|remoteAssistanceSessionUrl|Cadena|Dirección URL que permite que se establezca una sesión remota con el dispositivo.|
|remoteAssistanceSessionErrorDetails|Cadena|Una cadena de error que identifica los problemas al crear objetos de la sesión de asistencia remota.|
|isEncrypted|Booleano|Estado del cifrado del dispositivo|
|userPrincipalName|Cadena|Nombre principal de usuario del dispositivo|
|modelo|Cadena|Modelo del dispositivo|
|fabricante|Cadena|Fabricante del dispositivo|
|IMEI|Cadena|IMEI|
|complianceGracePeriodExpirationDateTime|DateTimeOffset|La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo|
|serialNumber|Cadena|Número de serie|
|phoneNumber|Cadena|Número de teléfono del dispositivo|
|androidSecurityPatchLevel|Cadena|Nivel de revisión de seguridad de Android|
|userDisplayName|Cadena|Nombre para mostrar del usuario|
|configurationManagerClientEnabledFeatures|[configurationManagerClientEnabledFeatures](../resources/intune_devices_configurationmanagerclientenabledfeatures.md)|Características activadas del cliente ConfigrMgr|
|wiFiMacAddress|Cadena|MAC de Wi-Fi|
|deviceHealthAttestationState|[deviceHealthAttestationState](../resources/intune_devices_devicehealthattestationstate.md)|El estado de la atestación de estado del dispositivo.|
|subscriberCarrier|Cadena|Operador de suscriptores|
|meid|Cadena|MEID|
|totalStorageSpaceInBytes|Int64|Almacenamiento total en bytes|
|freeStorageSpaceInBytes|Int64|Almacenamiento libre en bytes|
|managedDeviceName|Cadena|Nombre generado automáticamente para identificar un dispositivo. Se puede sobrescribir por un nombre descriptivo del usuario.|
|partnerReportedThreatState|Cadena|Indica el estado de amenazas de un dispositivo cuando la cuenta y el dispositivo usan un partner de Mobile Threat Defense. Solo lectura. Los valores posibles son: `unknown`, `activated`, `deactivated`, `secured`, `lowSeverity`, `mediumSeverity`, `highSeverity` y `unresponsive`.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|deviceCategory|[deviceCategory](../resources/intune_devices_devicecategory.md)|Categoría de dispositivo|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedDevice"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDevice",
  "id": "String (identifier)",
  "userId": "String",
  "deviceName": "String",
  "deviceActionResults": [
    {
      "@odata.type": "microsoft.graph.deviceActionResult",
      "actionName": "String",
      "actionState": "String",
      "startDateTime": "String (timestamp)",
      "lastUpdatedDateTime": "String (timestamp)"
    }
  ],
  "enrolledDateTime": "String (timestamp)",
  "lastSyncDateTime": "String (timestamp)",
  "operatingSystem": "String",
  "complianceState": "String",
  "jailBroken": "String",
  "managementAgent": "String",
  "osVersion": "String",
  "easActivated": true,
  "easDeviceId": "String",
  "easActivationDateTime": "String (timestamp)",
  "azureADRegistered": true,
  "deviceEnrollmentType": "String",
  "activationLockBypassCode": "String",
  "emailAddress": "String",
  "azureADDeviceId": "String",
  "deviceRegistrationState": "String",
  "deviceCategoryDisplayName": "String",
  "isSupervised": true,
  "exchangeLastSuccessfulSyncDateTime": "String (timestamp)",
  "exchangeAccessState": "String",
  "exchangeAccessStateReason": "String",
  "remoteAssistanceSessionUrl": "String",
  "remoteAssistanceSessionErrorDetails": "String",
  "isEncrypted": true,
  "userPrincipalName": "String",
  "model": "String",
  "manufacturer": "String",
  "imei": "String",
  "complianceGracePeriodExpirationDateTime": "String (timestamp)",
  "serialNumber": "String",
  "phoneNumber": "String",
  "androidSecurityPatchLevel": "String",
  "userDisplayName": "String",
  "configurationManagerClientEnabledFeatures": {
    "@odata.type": "microsoft.graph.configurationManagerClientEnabledFeatures",
    "inventory": true,
    "modernApps": true,
    "resourceAccess": true,
    "deviceConfiguration": true,
    "compliancePolicy": true,
    "windowsUpdateForBusiness": true
  },
  "wiFiMacAddress": "String",
  "deviceHealthAttestationState": {
    "@odata.type": "microsoft.graph.deviceHealthAttestationState",
    "lastUpdateDateTime": "String",
    "contentNamespaceUrl": "String",
    "deviceHealthAttestationStatus": "String",
    "contentVersion": "String",
    "issuedDateTime": "String (timestamp)",
    "attestationIdentityKey": "String",
    "resetCount": 1024,
    "restartCount": 1024,
    "dataExcutionPolicy": "String",
    "bitLockerStatus": "String",
    "bootManagerVersion": "String",
    "codeIntegrityCheckVersion": "String",
    "secureBoot": "String",
    "bootDebugging": "String",
    "operatingSystemKernelDebugging": "String",
    "codeIntegrity": "String",
    "testSigning": "String",
    "safeMode": "String",
    "windowsPE": "String",
    "earlyLaunchAntiMalwareDriverProtection": "String",
    "virtualSecureMode": "String",
    "pcrHashAlgorithm": "String",
    "bootAppSecurityVersion": "String",
    "bootManagerSecurityVersion": "String",
    "tpmVersion": "String",
    "pcr0": "String",
    "secureBootConfigurationPolicyFingerPrint": "String",
    "codeIntegrityPolicy": "String",
    "bootRevisionListInfo": "String",
    "operatingSystemRevListInfo": "String",
    "healthStatusMismatchInfo": "String",
    "healthAttestationSupportedStatus": "String"
  },
  "subscriberCarrier": "String",
  "meid": "String",
  "totalStorageSpaceInBytes": 1024,
  "freeStorageSpaceInBytes": 1024,
  "managedDeviceName": "String",
  "partnerReportedThreatState": "String"
}
```



