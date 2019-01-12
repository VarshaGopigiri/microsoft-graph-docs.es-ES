---
title: tipo de recurso windowsManagedDevice
description: Dispositivos de Windows que están administrados o pre-enrolled a través de Intune
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 54b11d8ee0a5b2c7b325289c897fe2e511ec3b4b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27933396"
---
# <a name="windowsmanageddevice-resource-type"></a>tipo de recurso windowsManagedDevice

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Dispositivos de Windows que están administrados o pre-enrolled a través de Intune

Hereda de [managedDevice](../resources/intune-devices-manageddevice.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista windowsManagedDevices](../api/intune-devices-windowsmanageddevice-list.md)|colección de [windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md)|Propiedades de la lista y relaciones de los objetos [windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md) .|
|[Obtener windowsManagedDevice](../api/intune-devices-windowsmanageddevice-get.md)|[windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md)|Leer las propiedades y las relaciones del objeto [windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md) .|
|[Crear windowsManagedDevice](../api/intune-devices-windowsmanageddevice-create.md)|[windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md)|Crear un nuevo objeto [windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md) .|
|[Eliminar windowsManagedDevice](../api/intune-devices-windowsmanageddevice-delete.md)|Ninguno|Elimina un [windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md).|
|[Actualizar windowsManagedDevice](../api/intune-devices-windowsmanageddevice-update.md)|[windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md)|Actualizar las propiedades de un objeto [windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Identificador único para el dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)|
|userId|Cadena|Identificador único para el usuario asociado con el dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)|
|deviceName|Cadena|Nombre del dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)|
|hardwareInformation|[hardwareInformation](../resources/intune-devices-hardwareinformation.md)|Los detalles de hardward para el dispositivo.  Incluye información como el espacio de almacenamiento, el fabricante, el número de serie, etcetera. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|ownerType|[ownerType](../resources/intune-devices-ownertype.md)|Propietario del dispositivo. Puede ser 'compañía' o 'personal' heredado de [managedDevice](../resources/intune-devices-manageddevice.md). Los valores posibles son: `unknown`, `company` y `personal`.|
|managedDeviceOwnerType|[managedDeviceOwnerType](../resources/intune-devices-manageddeviceownertype.md)|Propietario del dispositivo. Puede ser 'compañía' o 'personal' heredado de [managedDevice](../resources/intune-devices-manageddevice.md). Los valores posibles son: `unknown`, `company` y `personal`.|
|deviceActionResults|Colección [deviceActionResult](../resources/intune-devices-deviceactionresult.md)|Lista de objetos deviceActionResult ComplexType. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|managementState|[managementState](../resources/intune-devices-managementstate.md)|Estado de administración del dispositivo. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md). Los valores posibles son: `managed`, `retirePending`, `retireFailed`, `wipePending`, `wipeFailed`, `unhealthy`, `deletePending`, `retireIssued`, `wipeIssued`, `wipeCanceled`, `retireCanceled` y `discovered`.|
|enrolledDateTime|DateTimeOffset|Hora de inscripción del dispositivo. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|lastSyncDateTime|DateTimeOffset|Fecha y hora en que el dispositivo completó por última vez una sincronización correcta con Intune. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|chassisType|[chassisType](../resources/intune-devices-chassistype.md)|Tipo de chasis del dispositivo. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md). Los valores posibles son: `unknown`, `desktop`, `laptop`, `worksWorkstation`, `enterpriseServer`, `phone`, `tablet`, `mobileOther` y `mobileUnknown`.|
|operatingSystem|Cadena|Sistema operativo del dispositivo. Windows, iOS, etcetera. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|deviceType|[deviceType](../resources/intune-shared-devicetype.md)|Plataforma del dispositivo. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md). Los valores posibles son: `desktop`, `windowsRT`, `winMO6`, `nokia`, `windowsPhone`, `mac`, `winCE`, `winEmbedded`, `iPhone`, `iPad`, `iPod`, `android`, `iSocConsumer`, `unix`, `macMDM`, `holoLens`, `surfaceHub`, `androidForWork`, `androidEnterprise` , `blackberry`, `palm`, `unknown`.|
|complianceState|[complianceState](../resources/intune-devices-compliancestate.md)|Estado de cumplimiento del dispositivo. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md). Los valores posibles son: `unknown`, `compliant`, `noncompliant`, `conflict`, `error`, `inGracePeriod` y `configManager`.|
|jailBroken|Cadena|Indica si se trata de un dispositivo liberado o con permisos elevados. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|managementAgent|[managementAgentType](../resources/intune-devices-managementagenttype.md)|Canal de administración del dispositivo. Intune, EAS, etcetera. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md). Los valores posibles son: `eas`, `mdm`, `easMdm`, `intuneClient`, `easIntuneClient`, `configurationManagerClient`, `configurationManagerClientMdm`, `configurationManagerClientMdmEas`, `unknown`, `jamf`, `googleCloudDevicePolicyController` y `microsoft365ManagedMdm`.|
|osVersion|Cadena|Versión del sistema operativo del dispositivo. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|easActivated|Booleano|Indica si el dispositivo tiene Exchange ActiveSync activado. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|easDeviceId|Cadena|Identificador de Exchange ActiveSync del dispositivo. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|easActivationDateTime|DateTimeOffset|Hora de activación de Exchange ActivationSync del dispositivo. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|aadRegistered|Booleano|Indica si el dispositivo está registrado en Azure Active Directory. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|azureADRegistered|Booleano|Indica si el dispositivo está registrado en Azure Active Directory. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|deviceEnrollmentType|[deviceEnrollmentType](../resources/intune-shared-deviceenrollmenttype.md)|Tipo de inscripción del dispositivo. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md). Los valores posibles son: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin` y `windowsCoManagement`.|
|lostModeState|[lostModeState](../resources/intune-devices-lostmodestate.md)|Indica si el modo pierden está habilitado o deshabilitado Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md). Los valores posibles son: `disabled` y `enabled`.|
|activationLockBypassCode|Cadena|Código que permite que se omita el bloqueo de activación en un dispositivo. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|emailAddress|Cadena|Email(s) para el usuario asociado con el dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)|
|azureActiveDirectoryDeviceId|Cadena|Identificador único del dispositivo de Azure Active Directory. Solo lectura. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|azureADDeviceId|Cadena|Identificador único del dispositivo de Azure Active Directory. Solo lectura. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|deviceRegistrationState|[deviceRegistrationState](../resources/intune-devices-deviceregistrationstate.md)|Estado de registro del dispositivo. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md). Los valores posibles son: `notRegistered`, `registered`, `revoked`, `keyConflict`, `approvalPending`, `certificateReset`, `notRegisteredPendingEnrollment` y `unknown`.|
|deviceCategoryDisplayName|Cadena|Nombre para mostrar categoría dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)|
|isSupervised|Booleano|Estado del dispositivo supervisado Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)|
|exchangeLastSuccessfulSyncDateTime|DateTimeOffset|Última vez que el dispositivo estableció contacto con Exchange. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|exchangeAccessState|[deviceManagementExchangeAccessState](../resources/intune-devices-devicemanagementexchangeaccessstate.md)|Estado de acceso del dispositivo en Exchange. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md). Los valores posibles son: `none`, `unknown`, `allowed`, `blocked` y `quarantined`.|
|exchangeAccessStateReason|[deviceManagementExchangeAccessStateReason](../resources/intune-devices-devicemanagementexchangeaccessstatereason.md)|Motivo del estado de acceso del dispositivo en Exchange. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md). Los valores posibles son: `none`, `unknown`, `exchangeGlobalRule`, `exchangeIndividualRule`, `exchangeDeviceRule`, `exchangeUpgrade`, `exchangeMailboxPolicy`, `other`, `compliant`, `notCompliant`, `notEnrolled`, `unknownLocation`, `mfaRequired`, `azureADBlockDueToAccessPolicy`, `compromisedPassword` y `deviceNotKnownWithManagedApp`.|
|remoteAssistanceSessionUrl|Cadena|Dirección URL que permite que se establezca una sesión remota con el dispositivo. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|remoteAssistanceSessionErrorDetails|Cadena|Cadena de error que identifica los problemas al crear objetos de la sesión de asistencia remota. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|isEncrypted|Booleano|Estado del dispositivo cifrado Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)|
|userPrincipalName|Cadena|Dispositivo nombre principal de usuario Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)|
|model|Cadena|Modelo del dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)|
|manufacturer|Cadena|Fabricante del dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)|
|imei|Cadena|IMEI se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|complianceGracePeriodExpirationDateTime|DateTimeOffset|La fecha y hora en período de gracia de cumplimiento de normas de dispositivo expira Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)|
|serialNumber|Cadena|SerialNumber heredado de [managedDevice](../resources/intune-devices-manageddevice.md)|
|phoneNumber|Cadena|Número de teléfono del dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)|
|androidSecurityPatchLevel|Cadena|Nivel de revisión de seguridad para Android Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)|
|userDisplayName|Cadena|Nombre de usuario para mostrar Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)|
|configurationManagerClientEnabledFeatures|[configurationManagerClientEnabledFeatures](../resources/intune-devices-configurationmanagerclientenabledfeatures.md)|ConfigrMgr cliente habilitado para las características Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)|
|wiFiMacAddress|Cadena|Wi-Fi MAC se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|deviceHealthAttestationState|[deviceHealthAttestationState](../resources/intune-devices-devicehealthattestationstate.md)|Estado de la atestación de estado del dispositivo. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|subscriberCarrier|Cadena|Operador de suscriptor se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|meid|Cadena|MEID se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|totalStorageSpaceInBytes|Int64|Almacenamiento total en Bytes se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|freeStorageSpaceInBytes|Int64|Espacio de almacenamiento en Bytes se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|managedDeviceName|Cadena|Nombre generado automáticamente para identificar un dispositivo. Se puede sobrescribir con un nombre descriptivo del usuario. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|partnerReportedThreatState|[managedDevicePartnerReportedHealthState](../resources/intune-devices-manageddevicepartnerreportedhealthstate.md)|Indica el estado de amenazas de un dispositivo cuando la cuenta y el dispositivo usan un partner de Mobile Threat Defense. Solo lectura. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md). Los valores posibles son: `unknown`, `activated`, `deactivated`, `secured`, `lowSeverity`, `mediumSeverity`, `highSeverity`, `unresponsive`, `compromised` y `misconfigured`.|
|usersLoggedOn|colección de [loggedOnUser](../resources/intune-devices-loggedonuser.md)|Indica la última sesión a los usuarios de un dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)|
|preferMdmOverGroupPolicyAppliedDateTime|DateTimeOffset|Informes la fecha y hora de que la configuración de preferMdmOverGroupPolicy se estableció.  Cuando se establece, la configuración MDM Intune invalidará la configuración de directiva de grupo si hay un conflicto. Solo lectura. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|autopilotEnrolled|Booleano|Informa de si el dispositivo administrado está inscrito a través de piloto automático. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|requireUserEnrollmentApproval|Booleano|Informa de si el dispositivo iOS administrada es inscripción de aprobación del usuario. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|managementCertificateExpirationDate|DateTimeOffset|Informes de dispositivo administración certificado fecha de caducidad Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)|
|iccid|Cadena|Identificador de la tarjeta de circuitos integrados, es número de identificación único de la tarjeta SIM A. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|UDID|Cadena|Identificador único de dispositivo para dispositivos iOS y Mac OS. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|roleScopeTagIds|Colección String|Lista de identificadores de etiqueta de ámbito para esta instancia de dispositivo. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|
|windowsActiveMalwareCount|Int32|Recuento de malware para este dispositivo windows Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)|
|windowsRemediatedMalwareCount|Int32|Recuento de malware corregidos con pruebas para este dispositivo windows Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)|
|notas|Cadena|Notas en el dispositivo creado mediante la administración de TI se hereda desde [managedDevice](../resources/intune-devices-manageddevice.md)|
|configurationManagerClientHealthState|[configurationManagerClientHealthState](../resources/intune-devices-configurationmanagerclienthealthstate.md)|Configuración Administrador cliente estado de mantenimiento, válido sólo para los dispositivos administrados por MDM/ConfigMgr heredado de agente de [managedDevice](../resources/intune-devices-manageddevice.md)|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|detectedApps|Colección [detectedApp](../resources/intune-devices-detectedapp.md)|Todas las aplicaciones instaladas actualmente en el dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)|
|deviceCategory|[deviceCategory](../resources/intune-shared-devicecategory.md)|Categoría de dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)|
|windowsProtectionState|[windowsProtectionState](../resources/intune-devices-windowsprotectionstate.md)|El estado de protección del dispositivo. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsManagedDevice"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsManagedDevice",
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





