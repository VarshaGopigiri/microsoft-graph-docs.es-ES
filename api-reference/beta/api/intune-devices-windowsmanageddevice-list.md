---
title: Lista windowsManagedDevices
description: Propiedades de la lista y relaciones de los objetos windowsManagedDevice.
ms.openlocfilehash: 541b5c9ca7fb1702e9262c0c9f63573ed57d300b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27082933"
---
# <a name="list-windowsmanageddevices"></a><span data-ttu-id="291c2-103">Lista windowsManagedDevices</span><span class="sxs-lookup"><span data-stu-id="291c2-103">List windowsManagedDevices</span></span>

> <span data-ttu-id="291c2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="291c2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="291c2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="291c2-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="291c2-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="291c2-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="291c2-107">Propiedades de la lista y relaciones de los objetos [windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md) .</span><span class="sxs-lookup"><span data-stu-id="291c2-107">List properties and relationships of the [windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="291c2-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="291c2-108">Prerequisites</span></span>
<span data-ttu-id="291c2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="291c2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="291c2-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="291c2-111">Permission type</span></span>|<span data-ttu-id="291c2-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="291c2-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="291c2-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="291c2-113">Delegated (work or school account)</span></span>|<span data-ttu-id="291c2-114">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="291c2-114">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="291c2-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="291c2-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="291c2-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="291c2-116">Not supported.</span></span>|
|<span data-ttu-id="291c2-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="291c2-117">Application</span></span>|<span data-ttu-id="291c2-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="291c2-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="291c2-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="291c2-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /users/{usersId}/managedDevices
GET /deviceManagement/managedDevices
GET /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/detectedApps/{detectedAppId}/managedDevices
```

## <a name="request-headers"></a><span data-ttu-id="291c2-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="291c2-120">Request headers</span></span>
|<span data-ttu-id="291c2-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="291c2-121">Header</span></span>|<span data-ttu-id="291c2-122">Valor</span><span class="sxs-lookup"><span data-stu-id="291c2-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="291c2-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="291c2-123">Authorization</span></span>|<span data-ttu-id="291c2-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="291c2-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="291c2-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="291c2-125">Accept</span></span>|<span data-ttu-id="291c2-126">application/json</span><span class="sxs-lookup"><span data-stu-id="291c2-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="291c2-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="291c2-127">Request body</span></span>
<span data-ttu-id="291c2-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="291c2-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="291c2-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="291c2-129">Response</span></span>
<span data-ttu-id="291c2-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="291c2-130">If successful, this method returns a `200 OK` response code and a collection of [windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="291c2-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="291c2-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="291c2-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="291c2-132">Request</span></span>
<span data-ttu-id="291c2-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="291c2-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/users/{usersId}/managedDevices
```

### <a name="response"></a><span data-ttu-id="291c2-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="291c2-134">Response</span></span>
<span data-ttu-id="291c2-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="291c2-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 7907

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsManagedDevice",
      "id": "97842b67-2b67-9784-672b-8497672b8497",
      "userId": "User Id value",
      "deviceName": "Device Name value",
      "hardwareInformation": {
        "@odata.type": "microsoft.graph.hardwareInformation",
        "serialNumber": "Serial Number value",
        "totalStorageSpace": 1,
        "freeStorageSpace": 0,
        "imei": "Imei value",
        "meid": "Meid value",
        "manufacturer": "Manufacturer value",
        "model": "Model value",
        "phoneNumber": "Phone Number value",
        "subscriberCarrier": "Subscriber Carrier value",
        "cellularTechnology": "Cellular Technology value",
        "wifiMac": "Wifi Mac value",
        "operatingSystemLanguage": "Operating System Language value",
        "isSupervised": true,
        "isEncrypted": true,
        "isSharedDevice": true,
        "sharedDeviceCachedUsers": [
          {
            "@odata.type": "microsoft.graph.sharedAppleDeviceUser",
            "userPrincipalName": "User Principal Name value",
            "dataToSync": true,
            "dataQuota": 9,
            "dataUsed": 8
          }
        ],
        "tpmSpecificationVersion": "Tpm Specification Version value",
        "operatingSystemEdition": "Operating System Edition value",
        "deviceFullQualifiedDomainName": "Device Full Qualified Domain Name value",
        "deviceGuardVirtualizationBasedSecurityHardwareRequirementState": "secureBootRequired",
        "deviceGuardVirtualizationBasedSecurityState": "rebootRequired",
        "deviceGuardLocalSystemAuthorityCredentialGuardState": "rebootRequired"
      },
      "ownerType": "company",
      "managedDeviceOwnerType": "company",
      "deviceActionResults": [
        {
          "@odata.type": "microsoft.graph.deviceActionResult",
          "actionName": "Action Name value",
          "actionState": "pending",
          "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
          "lastUpdatedDateTime": "2017-01-01T00:00:56.8321556-08:00"
        }
      ],
      "managementState": "retirePending",
      "enrolledDateTime": "2016-12-31T23:59:43.797191-08:00",
      "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
      "chassisType": "desktop",
      "operatingSystem": "Operating System value",
      "deviceType": "windowsRT",
      "complianceState": "compliant",
      "jailBroken": "Jail Broken value",
      "managementAgent": "mdm",
      "osVersion": "Os Version value",
      "easActivated": true,
      "easDeviceId": "Eas Device Id value",
      "easActivationDateTime": "2016-12-31T23:59:43.4878784-08:00",
      "aadRegistered": true,
      "azureADRegistered": true,
      "deviceEnrollmentType": "userEnrollment",
      "lostModeState": "enabled",
      "activationLockBypassCode": "Activation Lock Bypass Code value",
      "emailAddress": "Email Address value",
      "azureActiveDirectoryDeviceId": "Azure Active Directory Device Id value",
      "azureADDeviceId": "Azure ADDevice Id value",
      "deviceRegistrationState": "registered",
      "deviceCategoryDisplayName": "Device Category Display Name value",
      "isSupervised": true,
      "exchangeLastSuccessfulSyncDateTime": "2017-01-01T00:00:45.8803083-08:00",
      "exchangeAccessState": "unknown",
      "exchangeAccessStateReason": "unknown",
      "remoteAssistanceSessionUrl": "https://example.com/remoteAssistanceSessionUrl/",
      "remoteAssistanceSessionErrorDetails": "Remote Assistance Session Error Details value",
      "isEncrypted": true,
      "userPrincipalName": "User Principal Name value",
      "model": "Model value",
      "manufacturer": "Manufacturer value",
      "imei": "Imei value",
      "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
      "serialNumber": "Serial Number value",
      "phoneNumber": "Phone Number value",
      "androidSecurityPatchLevel": "Android Security Patch Level value",
      "userDisplayName": "User Display Name value",
      "configurationManagerClientEnabledFeatures": {
        "@odata.type": "microsoft.graph.configurationManagerClientEnabledFeatures",
        "inventory": true,
        "modernApps": true,
        "resourceAccess": true,
        "deviceConfiguration": true,
        "compliancePolicy": true,
        "windowsUpdateForBusiness": true
      },
      "wiFiMacAddress": "Wi Fi Mac Address value",
      "deviceHealthAttestationState": {
        "@odata.type": "microsoft.graph.deviceHealthAttestationState",
        "lastUpdateDateTime": "Last Update Date Time value",
        "contentNamespaceUrl": "https://example.com/contentNamespaceUrl/",
        "deviceHealthAttestationStatus": "Device Health Attestation Status value",
        "contentVersion": "Content Version value",
        "issuedDateTime": "2016-12-31T23:58:22.1231038-08:00",
        "attestationIdentityKey": "Attestation Identity Key value",
        "resetCount": 10,
        "restartCount": 12,
        "dataExcutionPolicy": "Data Excution Policy value",
        "bitLockerStatus": "Bit Locker Status value",
        "bootManagerVersion": "Boot Manager Version value",
        "codeIntegrityCheckVersion": "Code Integrity Check Version value",
        "secureBoot": "Secure Boot value",
        "bootDebugging": "Boot Debugging value",
        "operatingSystemKernelDebugging": "Operating System Kernel Debugging value",
        "codeIntegrity": "Code Integrity value",
        "testSigning": "Test Signing value",
        "safeMode": "Safe Mode value",
        "windowsPE": "Windows PE value",
        "earlyLaunchAntiMalwareDriverProtection": "Early Launch Anti Malware Driver Protection value",
        "virtualSecureMode": "Virtual Secure Mode value",
        "pcrHashAlgorithm": "Pcr Hash Algorithm value",
        "bootAppSecurityVersion": "Boot App Security Version value",
        "bootManagerSecurityVersion": "Boot Manager Security Version value",
        "tpmVersion": "Tpm Version value",
        "pcr0": "Pcr0 value",
        "secureBootConfigurationPolicyFingerPrint": "Secure Boot Configuration Policy Finger Print value",
        "codeIntegrityPolicy": "Code Integrity Policy value",
        "bootRevisionListInfo": "Boot Revision List Info value",
        "operatingSystemRevListInfo": "Operating System Rev List Info value",
        "healthStatusMismatchInfo": "Health Status Mismatch Info value",
        "healthAttestationSupportedStatus": "Health Attestation Supported Status value"
      },
      "subscriberCarrier": "Subscriber Carrier value",
      "meid": "Meid value",
      "totalStorageSpaceInBytes": 8,
      "freeStorageSpaceInBytes": 7,
      "managedDeviceName": "Managed Device Name value",
      "partnerReportedThreatState": "activated",
      "usersLoggedOn": [
        {
          "@odata.type": "microsoft.graph.loggedOnUser",
          "userId": "User Id value",
          "lastLogOnDateTime": "2016-12-31T23:58:37.4262708-08:00"
        }
      ],
      "preferMdmOverGroupPolicyAppliedDateTime": "2016-12-31T23:57:34.4649887-08:00",
      "autopilotEnrolled": true,
      "requireUserEnrollmentApproval": true,
      "managementCertificateExpirationDate": "2016-12-31T23:57:59.9789653-08:00",
      "iccid": "Iccid value",
      "udid": "Udid value",
      "roleScopeTagIds": [
        "Role Scope Tag Ids value"
      ],
      "windowsActiveMalwareCount": 9,
      "windowsRemediatedMalwareCount": 13,
      "notes": "Notes value",
      "configurationManagerClientHealthState": {
        "@odata.type": "microsoft.graph.configurationManagerClientHealthState",
        "state": "installed",
        "errorCode": 9,
        "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00"
      }
    }
  ]
}
```




