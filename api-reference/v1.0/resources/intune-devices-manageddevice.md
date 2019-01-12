---
title: Tipo de recurso managedDevice
description: Dispositivos administrados o inscritos previamente a través de Intune
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 3643ec5020ea088b2da423ed44d0a1596e53e6a9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27955733"
---
# <a name="manageddevice-resource-type"></a>Tipo de recurso managedDevice

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Dispositivos administrados o inscritos previamente a través de Intune
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar managedDevices](../api/intune-devices-manageddevice-list.md)|Colección [managedDevice](../resources/intune-devices-manageddevice.md)|Enumere las propiedades y las relaciones de los objetos [managedDevice](../resources/intune-devices-manageddevice.md).|
|[Obtener managedDevice](../api/intune-devices-manageddevice-get.md)|[managedDevice](../resources/intune-devices-manageddevice.md)|Lea las propiedades y las relaciones del objeto [managedDevice](../resources/intune-devices-manageddevice.md).|
|[Crear managedDevice](../api/intune-devices-manageddevice-create.md)|[managedDevice](../resources/intune-devices-manageddevice.md)|Cree un objeto [managedDevice](../resources/intune-devices-manageddevice.md).|
|[Eliminar managedDevice](../api/intune-devices-manageddevice-delete.md)|Ninguno|Elimina un [managedDevice](../resources/intune-devices-manageddevice.md).|
|[Actualizar managedDevice](../api/intune-devices-manageddevice-update.md)|[managedDevice](../resources/intune-devices-manageddevice.md)|Actualice las propiedades de un objeto [managedDevice](../resources/intune-devices-manageddevice.md).|
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

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Identificador único del dispositivo.|
|userId|Cadena|Identificador único del usuario asociado al dispositivo.|
|deviceName|Cadena|Nombre del dispositivo.|
|managedDeviceOwnerType|[managedDeviceOwnerType](../resources/intune-devices-manageddeviceownertype.md)|Propietario del dispositivo. Puede ser 'compañía' o 'personal'. Los valores posibles son: `unknown`, `company` y `personal`.|
|deviceActionResults|Colección [deviceActionResult](../resources/intune-devices-deviceactionresult.md)|Lista de objetos deviceActionResult ComplexType.|
|enrolledDateTime|DateTimeOffset|Hora de inscripción del dispositivo.|
|lastSyncDateTime|DateTimeOffset|Fecha y hora en que el dispositivo completó por última vez una sincronización correcta con Intune.|
|operatingSystem|Cadena|Sistema operativo del dispositivo. Windows, iOS, etc.|
|complianceState|[complianceState](../resources/intune-devices-compliancestate.md)|Estado de cumplimiento del dispositivo. Los valores posibles son: `unknown`, `compliant`, `noncompliant`, `conflict`, `error`, `inGracePeriod` y `configManager`.|
|jailBroken|Cadena|Indica si se trata de un dispositivo liberado o con permisos elevados.|
|managementAgent|[managementAgentType](../resources/intune-devices-managementagenttype.md)|Canal de administración del dispositivo. Intune, EAS, etc. Los valores posibles son: `eas`, `mdm`, `easMdm`, `intuneClient`, `easIntuneClient`, `configurationManagerClient`, `configurationManagerClientMdm`, `configurationManagerClientMdmEas`, `unknown`, `jamf` y `googleCloudDevicePolicyController`.|
|osVersion|Cadena|Versión del sistema operativo del dispositivo.|
|easActivated|Booleano|Indica si el dispositivo tiene Exchange ActiveSync activado.|
|easDeviceId|Cadena|Identificador de Exchange ActiveSync del dispositivo.|
|easActivationDateTime|DateTimeOffset|Hora de activación de Exchange ActivationSync del dispositivo.|
|azureADRegistered|Booleano|Indica si el dispositivo está registrado en Azure Active Directory.|
|deviceEnrollmentType|[deviceEnrollmentType](../resources/intune-devices-deviceenrollmenttype.md)|Tipo de inscripción del dispositivo. Los valores posibles son: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin` y `windowsCoManagement`.|
|activationLockBypassCode|Cadena|Código que permite que se omita el bloqueo de activación en un dispositivo.|
|emailAddress|Cadena|Direcciones de correo electrónico del usuario asociado al dispositivo.|
|azureADDeviceId|Cadena|Identificador único del dispositivo de Azure Active Directory. Solo lectura.|
|deviceRegistrationState|[deviceRegistrationState](../resources/intune-devices-deviceregistrationstate.md)|Estado de registro del dispositivo. Los valores posibles son: `notRegistered`, `registered`, `revoked`, `keyConflict`, `approvalPending`, `certificateReset`, `notRegisteredPendingEnrollment` y `unknown`.|
|deviceCategoryDisplayName|Cadena|Nombre para mostrar de la categoría de dispositivo.|
|isSupervised|Booleano|Estado supervisado del dispositivo.|
|exchangeLastSuccessfulSyncDateTime|DateTimeOffset|Última vez que el dispositivo estableció contacto con Exchange.|
|exchangeAccessState|[deviceManagementExchangeAccessState](../resources/intune-devices-devicemanagementexchangeaccessstate.md)|Estado de acceso del dispositivo en Exchange. Los valores posibles son: `none`, `unknown`, `allowed`, `blocked` y `quarantined`.|
|exchangeAccessStateReason|[deviceManagementExchangeAccessStateReason](../resources/intune-devices-devicemanagementexchangeaccessstatereason.md)|Motivo del estado de acceso del dispositivo en Exchange. Los valores posibles son: `none`, `unknown`, `exchangeGlobalRule`, `exchangeIndividualRule`, `exchangeDeviceRule`, `exchangeUpgrade`, `exchangeMailboxPolicy`, `other`, `compliant`, `notCompliant`, `notEnrolled`, `unknownLocation`, `mfaRequired`, `azureADBlockDueToAccessPolicy`, `compromisedPassword` y `deviceNotKnownWithManagedApp`.|
|remoteAssistanceSessionUrl|Cadena|Dirección URL que permite que se establezca una sesión remota con el dispositivo.|
|remoteAssistanceSessionErrorDetails|Cadena|Cadena de error que identifica los problemas al crear objetos de la sesión de asistencia remota.|
|isEncrypted|Booleano|Estado del cifrado del dispositivo.|
|userPrincipalName|Cadena|Nombre principal de usuario del dispositivo.|
|model|Cadena|Modelo del dispositivo.|
|manufacturer|Cadena|Fabricante del dispositivo.|
|imei|Cadena|IMEI|
|complianceGracePeriodExpirationDateTime|DateTimeOffset|Fecha y hora en que expira el período de gracia de cumplimiento del dispositivo.|
|serialNumber|Cadena|Número de serie.|
|phoneNumber|Cadena|Número de teléfono del dispositivo.|
|androidSecurityPatchLevel|Cadena|Nivel de revisión de seguridad de Android.|
|userDisplayName|Cadena|Nombre para mostrar del usuario.|
|configurationManagerClientEnabledFeatures|[configurationManagerClientEnabledFeatures](../resources/intune-devices-configurationmanagerclientenabledfeatures.md)|Características activadas del cliente ConfigrMgr.|
|wiFiMacAddress|Cadena|MAC de Wi-Fi.|
|deviceHealthAttestationState|[deviceHealthAttestationState](../resources/intune-devices-devicehealthattestationstate.md)|Estado de la atestación de estado del dispositivo.|
|subscriberCarrier|Cadena|Operador del suscriptor.|
|meid|Cadena|MEID|
|totalStorageSpaceInBytes|Int64|Almacenamiento total en bytes.|
|freeStorageSpaceInBytes|Int64|Almacenamiento disponible en bytes.|
|managedDeviceName|Cadena|Nombre generado automáticamente para identificar un dispositivo. Se puede sobrescribir con un nombre descriptivo del usuario.|
|partnerReportedThreatState|[managedDevicePartnerReportedHealthState](../resources/intune-devices-manageddevicepartnerreportedhealthstate.md)|Indica el estado de amenazas de un dispositivo cuando la cuenta y el dispositivo usan un partner de Mobile Threat Defense. Solo lectura. Los valores posibles son: `unknown`, `activated`, `deactivated`, `secured`, `lowSeverity`, `mediumSeverity`, `highSeverity`, `unresponsive`, `compromised` y `misconfigured`.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|deviceCategory|[deviceCategory](../resources/intune-shared-devicecategory.md)|Categoría de dispositivo|

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



