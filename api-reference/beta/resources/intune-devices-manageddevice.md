---
title: Tipo de recurso managedDevice
description: Dispositivos administrados o inscritos previamente a través de Intune
author: tfitzmac
ms.openlocfilehash: ac55f444eb4c87f65befbc1ba33c2e9bc65dced2
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27309614"
---
# <a name="manageddevice-resource-type"></a>Tipo de recurso managedDevice

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Dispositivos administrados o inscritos previamente a través de Intune
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener managedDevice](../api/intune-devices-manageddevice-get.md)|[managedDevice](../resources/intune-devices-manageddevice.md)|Lea las propiedades y las relaciones del objeto [managedDevice](../resources/intune-devices-manageddevice.md).|
|[Actualizar managedDevice](../api/intune-devices-manageddevice-update.md)|[managedDevice](../resources/intune-devices-manageddevice.md)|Actualice las propiedades de un objeto [managedDevice](../resources/intune-devices-manageddevice.md).|
|[acción executeAction](../api/intune-devices-manageddevice-executeaction.md)|[bulkManagedDeviceActionResult](../resources/intune-devices-bulkmanageddeviceactionresult.md)|Todavía no documentado|
|[acción enableLostMode](../api/intune-devices-manageddevice-enablelostmode.md)|Ninguno|Habilitar el modo pierden|
|[acción playLostModeSound](../api/intune-devices-manageddevice-playlostmodesound.md)|Ninguno|Bloqueo remoto|
|[acción setDeviceName](../api/intune-devices-manageddevice-setdevicename.md)|Ninguno|Establecer el nombre de dispositivo del dispositivo.|
|[Acción retire](../api/intune-devices-manageddevice-retire.md)|Ninguno|Retirar un dispositivo|
|[Acción wipe](../api/intune-devices-manageddevice-wipe.md)|Ninguno|Eliminar los datos de un dispositivo|
|[Acción resetPasscode](../api/intune-devices-manageddevice-resetpasscode.md)|Ninguno|Restablecer código de acceso|
|[Acción remoteLock](../api/intune-devices-manageddevice-remotelock.md)|Ninguno|Bloqueo remoto|
|[Acción requestRemoteAssistance](../api/intune-devices-manageddevice-requestremoteassistance.md)|Ninguno|Solicitar asistencia remota|
|[Acción disableLostMode](../api/intune-devices-manageddevice-disablelostmode.md)|Ninguno|Deshabilitar modo Perdido|
|[Acción locateDevice](../api/intune-devices-manageddevice-locatedevice.md)|Ninguno|Buscar un dispositivo|
|[Acción bypassActivationLock](../api/intune-devices-manageddevice-bypassactivationlock.md)|Ninguno|Omitir bloqueo de activación|
|[Acción rebootNow](../api/intune-devices-manageddevice-rebootnow.md)|Ninguno|Reiniciar el dispositivo|
|[Acción shutDown](../api/intune-devices-manageddevice-shutdown.md)|Ninguno|Apagar el dispositivo|
|[Acción recoverPasscode](../api/intune-devices-manageddevice-recoverpasscode.md)|Ninguno|Recuperar código de acceso|
|[Acción cleanWindowsDevice](../api/intune-devices-manageddevice-cleanwindowsdevice.md)|Ninguno|Limpiar dispositivo Windows|
|[Acción logoutSharedAppleDeviceActiveUser](../api/intune-devices-manageddevice-logoutsharedappledeviceactiveuser.md)|Ninguno|Cerrar la sesión del usuario activo del dispositivo Apple compartido|
|[Acción deleteUserFromSharedAppleDevice](../api/intune-devices-manageddevice-deleteuserfromsharedappledevice.md)|Ninguno|Eliminar usuario del dispositivo Apple compartido|
|[Acción syncDevice](../api/intune-devices-manageddevice-syncdevice.md)|Ninguno|Todavía no documentado|
|[Acción windowsDefenderScan](../api/intune-devices-manageddevice-windowsdefenderscan.md)|Ninguno|Todavía no documentado|
|[Acción windowsDefenderUpdateSignatures](../api/intune-devices-manageddevice-windowsdefenderupdatesignatures.md)|Ninguno|Todavía no documentado|
|[Acción updateWindowsDeviceAccount](../api/intune-devices-manageddevice-updatewindowsdeviceaccount.md)|Ninguno|Todavía no documentado|
|[acción revokeAppleVppLicenses](../api/intune-devices-manageddevice-revokeapplevpplicenses.md)|Ninguno|Revocar todas las licencias de Apple Vpp para un dispositivo|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único del dispositivo.|
|userId|String|Identificador único del usuario asociado al dispositivo.|
|deviceName|String|Nombre del dispositivo.|
|hardwareInformation|[hardwareInformation](../resources/intune-devices-hardwareinformation.md)|Los detalles de hardward para el dispositivo.  Incluye información como el espacio de almacenamiento, el fabricante, el número de serie, etcetera.|
|ownerType|[ownerType](../resources/intune-devices-ownertype.md)|Propietario del dispositivo. Puede ser 'compañía' o 'personal'. Los valores posibles son: `unknown`, `company` y `personal`.|
|managedDeviceOwnerType|[managedDeviceOwnerType](../resources/intune-devices-manageddeviceownertype.md)|Propietario del dispositivo. Puede ser 'compañía' o 'personal'. Los valores posibles son: `unknown`, `company` y `personal`.|
|deviceActionResults|Colección [deviceActionResult](../resources/intune-devices-deviceactionresult.md)|Lista de objetos deviceActionResult ComplexType.|
|managementState|[managementState](../resources/intune-devices-managementstate.md)|Estado de administración del dispositivo. Los valores posibles son: `managed`, `retirePending`, `retireFailed`, `wipePending`, `wipeFailed`, `unhealthy`, `deletePending`, `retireIssued`, `wipeIssued`, `wipeCanceled`, `retireCanceled` y `discovered`.|
|enrolledDateTime|DateTimeOffset|Hora de inscripción del dispositivo.|
|lastSyncDateTime|DateTimeOffset|Fecha y hora en que el dispositivo completó por última vez una sincronización correcta con Intune.|
|chassisType|[chassisType](../resources/intune-devices-chassistype.md)|Tipo de chasis del dispositivo. Los valores posibles son: `unknown`, `desktop`, `laptop`, `worksWorkstation`, `enterpriseServer`, `phone`, `tablet`, `mobileOther` y `mobileUnknown`.|
|operatingSystem|String|Sistema operativo del dispositivo. Windows, iOS, etc.|
|deviceType|[deviceType](../resources/intune-shared-devicetype.md)|Plataforma del dispositivo. Los valores posibles son: `desktop`, `windowsRT`, `winMO6`, `nokia`, `windowsPhone`, `mac`, `winCE`, `winEmbedded`, `iPhone`, `iPad`, `iPod`, `android`, `iSocConsumer`, `unix`, `macMDM`, `holoLens`, `surfaceHub`, `androidForWork`, `androidEnterprise` , `blackberry`, `palm`, `unknown`.|
|complianceState|[complianceState](../resources/intune-devices-compliancestate.md)|Estado de cumplimiento del dispositivo. Los valores posibles son: `unknown`, `compliant`, `noncompliant`, `conflict`, `error`, `inGracePeriod` y `configManager`.|
|jailBroken|String|Indica si se trata de un dispositivo liberado o con permisos elevados.|
|managementAgent|[managementAgentType](../resources/intune-devices-managementagenttype.md)|Canal de administración del dispositivo. Intune, EAS, etcetera. Los valores posibles son: `eas`, `mdm`, `easMdm`, `intuneClient`, `easIntuneClient`, `configurationManagerClient`, `configurationManagerClientMdm`, `configurationManagerClientMdmEas`, `unknown`, `jamf`, `googleCloudDevicePolicyController`, `microsoft365ManagedMdm`.|
|osVersion|String|Versión del sistema operativo del dispositivo.|
|easActivated|Boolean|Indica si el dispositivo tiene Exchange ActiveSync activado.|
|easDeviceId|String|Identificador de Exchange ActiveSync del dispositivo.|
|easActivationDateTime|DateTimeOffset|Hora de activación de Exchange ActivationSync del dispositivo.|
|aadRegistered|Boolean|Indica si el dispositivo está registrado en Azure Active Directory.|
|azureADRegistered|Boolean|Indica si el dispositivo está registrado en Azure Active Directory.|
|deviceEnrollmentType|[deviceEnrollmentType](../resources/intune-shared-deviceenrollmenttype.md)|Tipo de inscripción del dispositivo. Los valores posibles son: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin` y `windowsCoManagement`.|
|lostModeState|[lostModeState](../resources/intune-devices-lostmodestate.md)|Indica si el modo pierden está habilitado o deshabilitado. Los valores posibles son: `disabled` y `enabled`.|
|activationLockBypassCode|String|Código que permite que se omita el bloqueo de activación en un dispositivo.|
|emailAddress|String|Direcciones de correo electrónico del usuario asociado al dispositivo.|
|azureActiveDirectoryDeviceId|String|Identificador único del dispositivo de Azure Active Directory. Solo lectura.|
|azureADDeviceId|String|Identificador único del dispositivo de Azure Active Directory. Solo lectura.|
|deviceRegistrationState|[deviceRegistrationState](../resources/intune-devices-deviceregistrationstate.md)|Estado de registro del dispositivo. Los valores posibles son: `notRegistered`, `registered`, `revoked`, `keyConflict`, `approvalPending`, `certificateReset`, `notRegisteredPendingEnrollment` y `unknown`.|
|deviceCategoryDisplayName|String|Nombre para mostrar de la categoría de dispositivo.|
|isSupervised|Boolean|Estado supervisado del dispositivo.|
|exchangeLastSuccessfulSyncDateTime|DateTimeOffset|Última vez que el dispositivo estableció contacto con Exchange.|
|exchangeAccessState|[deviceManagementExchangeAccessState](../resources/intune-devices-devicemanagementexchangeaccessstate.md)|Estado de acceso del dispositivo en Exchange. Los valores posibles son: `none`, `unknown`, `allowed`, `blocked` y `quarantined`.|
|exchangeAccessStateReason|[deviceManagementExchangeAccessStateReason](../resources/intune-devices-devicemanagementexchangeaccessstatereason.md)|Motivo del estado de acceso del dispositivo en Exchange. Los valores posibles son: `none`, `unknown`, `exchangeGlobalRule`, `exchangeIndividualRule`, `exchangeDeviceRule`, `exchangeUpgrade`, `exchangeMailboxPolicy`, `other`, `compliant`, `notCompliant`, `notEnrolled`, `unknownLocation`, `mfaRequired`, `azureADBlockDueToAccessPolicy`, `compromisedPassword` y `deviceNotKnownWithManagedApp`.|
|remoteAssistanceSessionUrl|String|Dirección URL que permite que se establezca una sesión remota con el dispositivo.|
|remoteAssistanceSessionErrorDetails|String|Cadena de error que identifica los problemas al crear objetos de la sesión de asistencia remota.|
|isEncrypted|Boolean|Estado del cifrado del dispositivo.|
|userPrincipalName|String|Nombre principal de usuario del dispositivo.|
|model|String|Modelo del dispositivo.|
|manufacturer|String|Fabricante del dispositivo.|
|imei|String|IMEI|
|complianceGracePeriodExpirationDateTime|DateTimeOffset|Fecha y hora en que expira el período de gracia de cumplimiento del dispositivo.|
|serialNumber|String|Número de serie.|
|phoneNumber|String|Número de teléfono del dispositivo.|
|androidSecurityPatchLevel|String|Nivel de revisión de seguridad de Android.|
|userDisplayName|String|Nombre para mostrar del usuario.|
|configurationManagerClientEnabledFeatures|[configurationManagerClientEnabledFeatures](../resources/intune-devices-configurationmanagerclientenabledfeatures.md)|Características activadas del cliente ConfigrMgr.|
|wiFiMacAddress|String|MAC de Wi-Fi.|
|deviceHealthAttestationState|[deviceHealthAttestationState](../resources/intune-devices-devicehealthattestationstate.md)|Estado de la atestación de estado del dispositivo.|
|subscriberCarrier|String|Operador del suscriptor.|
|meid|String|MEID|
|totalStorageSpaceInBytes|Int64|Almacenamiento total en bytes.|
|freeStorageSpaceInBytes|Int64|Almacenamiento disponible en bytes.|
|managedDeviceName|String|Nombre generado automáticamente para identificar un dispositivo. Se puede sobrescribir con un nombre descriptivo del usuario.|
|partnerReportedThreatState|[managedDevicePartnerReportedHealthState](../resources/intune-devices-manageddevicepartnerreportedhealthstate.md)|Indica el estado de amenazas de un dispositivo cuando la cuenta y el dispositivo usan un partner de Mobile Threat Defense. Solo lectura. Los valores posibles son: `unknown`, `activated`, `deactivated`, `secured`, `lowSeverity`, `mediumSeverity`, `highSeverity`, `unresponsive`, `compromised` y `misconfigured`.|
|usersLoggedOn|colección de [loggedOnUser](../resources/intune-devices-loggedonuser.md)|Indica la última sesión de los usuarios de un dispositivo|
|preferMdmOverGroupPolicyAppliedDateTime|DateTimeOffset|Informes la fecha y hora de que la configuración de preferMdmOverGroupPolicy se estableció.  Cuando se establece, la configuración MDM Intune invalidará la configuración de directiva de grupo si hay un conflicto. Solo lectura.|
|autopilotEnrolled|Boolean|Informa de si el dispositivo administrado está inscrito a través de piloto automático.|
|requireUserEnrollmentApproval|Boolean|Informa de si el dispositivo iOS administrada es inscripción de aprobación del usuario.|
|managementCertificateExpirationDate|DateTimeOffset|Fecha de caducidad de certificado de administración de dispositivos de informes|
|iccid|String|Identificador de la tarjeta de circuitos integrados, es número de identificación único de la tarjeta SIM A.|
|UDID|String|Identificador único de dispositivo para dispositivos iOS y Mac OS.|
|roleScopeTagIds|Colección String|Lista de identificadores de etiqueta de ámbito para esta instancia de dispositivo.|
|windowsActiveMalwareCount|Int32|Recuento de malware para este dispositivo de windows|
|windowsRemediatedMalwareCount|Int32|Recuento de malware corregidos con pruebas para este dispositivo de windows|
|notas|String|Notas en el dispositivo creado por el Administrador de TI|
|configurationManagerClientHealthState|[configurationManagerClientHealthState](../resources/intune-devices-configurationmanagerclienthealthstate.md)|Configuración Administrador cliente estado de mantenimiento, válido sólo para los dispositivos administrados por agente MDM/ConfigMgr|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|detectedApps|Colección [detectedApp](../resources/intune-devices-detectedapp.md)|Todas las aplicaciones instaladas actualmente en el dispositivo|
|deviceCategory|[deviceCategory](../resources/intune-shared-devicecategory.md)|Categoría de dispositivo|
|windowsProtectionState|[windowsProtectionState](../resources/intune-devices-windowsprotectionstate.md)|El estado de protección del dispositivo.|

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
  "hardwareInformation": {
    "@odata.type": "microsoft.graph.hardwareInformation",
    "serialNumber": "String",
    "totalStorageSpace": 1024,
    "freeStorageSpace": 1024,
    "imei": "String",
    "meid": "String",
    "manufacturer": "String",
    "model": "String",
    "phoneNumber": "String",
    "subscriberCarrier": "String",
    "cellularTechnology": "String",
    "wifiMac": "String",
    "operatingSystemLanguage": "String",
    "isSupervised": true,
    "isEncrypted": true,
    "isSharedDevice": true,
    "sharedDeviceCachedUsers": [
      {
        "@odata.type": "microsoft.graph.sharedAppleDeviceUser",
        "userPrincipalName": "String",
        "dataToSync": true,
        "dataQuota": 1024,
        "dataUsed": 1024
      }
    ],
    "tpmSpecificationVersion": "String",
    "operatingSystemEdition": "String",
    "deviceFullQualifiedDomainName": "String",
    "deviceGuardVirtualizationBasedSecurityHardwareRequirementState": "String",
    "deviceGuardVirtualizationBasedSecurityState": "String",
    "deviceGuardLocalSystemAuthorityCredentialGuardState": "String"
  },
  "ownerType": "String",
  "managedDeviceOwnerType": "String",
  "deviceActionResults": [
    {
      "@odata.type": "microsoft.graph.deviceActionResult",
      "actionName": "String",
      "actionState": "String",
      "startDateTime": "String (timestamp)",
      "lastUpdatedDateTime": "String (timestamp)"
    }
  ],
  "managementState": "String",
  "enrolledDateTime": "String (timestamp)",
  "lastSyncDateTime": "String (timestamp)",
  "chassisType": "String",
  "operatingSystem": "String",
  "deviceType": "String",
  "complianceState": "String",
  "jailBroken": "String",
  "managementAgent": "String",
  "osVersion": "String",
  "easActivated": true,
  "easDeviceId": "String",
  "easActivationDateTime": "String (timestamp)",
  "aadRegistered": true,
  "azureADRegistered": true,
  "deviceEnrollmentType": "String",
  "lostModeState": "String",
  "activationLockBypassCode": "String",
  "emailAddress": "String",
  "azureActiveDirectoryDeviceId": "String",
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
  "partnerReportedThreatState": "String",
  "usersLoggedOn": [
    {
      "@odata.type": "microsoft.graph.loggedOnUser",
      "userId": "String",
      "lastLogOnDateTime": "String (timestamp)"
    }
  ],
  "preferMdmOverGroupPolicyAppliedDateTime": "String (timestamp)",
  "autopilotEnrolled": true,
  "requireUserEnrollmentApproval": true,
  "managementCertificateExpirationDate": "String (timestamp)",
  "iccid": "String",
  "udid": "String",
  "roleScopeTagIds": [
    "String"
  ],
  "windowsActiveMalwareCount": 1024,
  "windowsRemediatedMalwareCount": 1024,
  "notes": "String",
  "configurationManagerClientHealthState": {
    "@odata.type": "microsoft.graph.configurationManagerClientHealthState",
    "state": "String",
    "errorCode": 1024,
    "lastSyncDateTime": "String (timestamp)"
  }
}
```





