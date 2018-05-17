# <a name="get-manageddevice"></a><span data-ttu-id="b59b9-101">Obtener managedDevice</span><span class="sxs-lookup"><span data-stu-id="b59b9-101">Get managedDevice</span></span>

> <span data-ttu-id="b59b9-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b59b9-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b59b9-103">Lea las propiedades y las relaciones del objeto [managedDevice](../resources/intune_devices_manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="b59b9-103">Read properties and relationships of the [managedDevice](../resources/intune_devices_manageddevice.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b59b9-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b59b9-104">Prerequisites</span></span>
<span data-ttu-id="b59b9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b59b9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b59b9-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b59b9-107">Permission type</span></span>|<span data-ttu-id="b59b9-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b59b9-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b59b9-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b59b9-109">Delegated (work or school account)</span></span>|<span data-ttu-id="b59b9-110">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="b59b9-110">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="b59b9-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b59b9-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b59b9-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b59b9-112">Not supported.</span></span>|
|<span data-ttu-id="b59b9-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b59b9-113">Application</span></span>|<span data-ttu-id="b59b9-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b59b9-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b59b9-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b59b9-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /users/{usersId}/managedDevices/{managedDeviceId}
GET /deviceManagement/managedDevices/{managedDeviceId}
GET /deviceManagement/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="b59b9-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b59b9-116">Optional query parameters</span></span>
<span data-ttu-id="b59b9-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b59b9-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="b59b9-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b59b9-118">Request headers</span></span>
|<span data-ttu-id="b59b9-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b59b9-119">Header</span></span>|<span data-ttu-id="b59b9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b59b9-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b59b9-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="b59b9-121">Authorization</span></span>|<span data-ttu-id="b59b9-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b59b9-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b59b9-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b59b9-123">Accept</span></span>|<span data-ttu-id="b59b9-124">application/json</span><span class="sxs-lookup"><span data-stu-id="b59b9-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b59b9-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b59b9-125">Request body</span></span>
<span data-ttu-id="b59b9-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b59b9-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b59b9-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b59b9-127">Response</span></span>
<span data-ttu-id="b59b9-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedDevice](../resources/intune_devices_manageddevice.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b59b9-128">If successful, this method returns a `200 OK` response code and [managedDevice](../resources/intune_devices_manageddevice.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b59b9-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b59b9-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="b59b9-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b59b9-130">Request</span></span>
<span data-ttu-id="b59b9-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b59b9-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/users/{usersId}/managedDevices/{managedDeviceId}
```

### <a name="response"></a><span data-ttu-id="b59b9-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b59b9-132">Response</span></span>
<span data-ttu-id="b59b9-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b59b9-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 4920

{
  "value": {
    "@odata.type": "#microsoft.graph.managedDevice",
    "id": "705c034c-034c-705c-4c03-5c704c035c70",
    "userId": "User Id value",
    "deviceName": "Device Name value",
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
    "enrolledDateTime": "2016-12-31T23:59:43.797191-08:00",
    "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
    "operatingSystem": "Operating System value",
    "complianceState": "compliant",
    "jailBroken": "Jail Broken value",
    "managementAgent": "mdm",
    "osVersion": "Os Version value",
    "easActivated": true,
    "easDeviceId": "Eas Device Id value",
    "easActivationDateTime": "2016-12-31T23:59:43.4878784-08:00",
    "azureADRegistered": true,
    "deviceEnrollmentType": "userEnrollment",
    "activationLockBypassCode": "Activation Lock Bypass Code value",
    "emailAddress": "Email Address value",
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
    "partnerReportedThreatState": "activated"
  }
}
```



