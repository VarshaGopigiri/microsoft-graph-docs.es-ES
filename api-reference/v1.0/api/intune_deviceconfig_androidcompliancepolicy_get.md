# <a name="get-androidcompliancepolicy"></a><span data-ttu-id="12c1b-101">Obtener androidCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="12c1b-101">Get androidCompliancePolicy</span></span>

> <span data-ttu-id="12c1b-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="12c1b-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="12c1b-103">Lea las propiedades y las relaciones del objeto [androidCompliancePolicy](../resources/intune_deviceconfig_androidcompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="12c1b-103">Read properties and relationships of [plannerPlanDetails](../resources/intune_deviceconfig_androidcompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="12c1b-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="12c1b-104">Prerequisites</span></span>
<span data-ttu-id="12c1b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="12c1b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="12c1b-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="12c1b-107">Permission type</span></span>|<span data-ttu-id="12c1b-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="12c1b-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="12c1b-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="12c1b-109">Delegated (work or school account)</span></span>|<span data-ttu-id="12c1b-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="12c1b-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="12c1b-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="12c1b-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="12c1b-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="12c1b-112">Not supported.</span></span>|
|<span data-ttu-id="12c1b-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="12c1b-113">Application</span></span>|<span data-ttu-id="12c1b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="12c1b-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="12c1b-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="12c1b-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="12c1b-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="12c1b-116">Optional query parameters</span></span>
<span data-ttu-id="12c1b-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="12c1b-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="12c1b-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="12c1b-118">Request headers</span></span>
|<span data-ttu-id="12c1b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12c1b-119">Header</span></span>|<span data-ttu-id="12c1b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="12c1b-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="12c1b-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="12c1b-121">Authorization</span></span>|<span data-ttu-id="12c1b-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="12c1b-122">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="12c1b-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="12c1b-123">Accept</span></span>|<span data-ttu-id="12c1b-124">application/json</span><span class="sxs-lookup"><span data-stu-id="12c1b-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="12c1b-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="12c1b-125">Request body</span></span>
<span data-ttu-id="12c1b-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="12c1b-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="12c1b-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="12c1b-127">Response</span></span>
<span data-ttu-id="12c1b-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidCompliancePolicy](../resources/intune_deviceconfig_androidcompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="12c1b-128">If successful, this method returns a `200 OK` response code and a [DriveItemVersion](../resources/intune_deviceconfig_androidcompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="12c1b-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="12c1b-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="12c1b-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="12c1b-130">Request</span></span>
<span data-ttu-id="12c1b-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="12c1b-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

### <a name="response"></a><span data-ttu-id="12c1b-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="12c1b-132">Response</span></span>
<span data-ttu-id="12c1b-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="12c1b-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1406

{
  "value": {
    "@odata.type": "#microsoft.graph.androidCompliancePolicy",
    "id": "752c820f-820f-752c-0f82-2c750f822c75",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "displayName": "Display Name value",
    "version": 7,
    "passwordRequired": true,
    "passwordMinimumLength": 5,
    "passwordRequiredType": "alphabetic",
    "passwordMinutesOfInactivityBeforeLock": 5,
    "passwordExpirationDays": 6,
    "passwordPreviousPasswordBlockCount": 2,
    "securityPreventInstallAppsFromUnknownSources": true,
    "securityDisableUsbDebugging": true,
    "securityRequireVerifyApps": true,
    "deviceThreatProtectionEnabled": true,
    "deviceThreatProtectionRequiredSecurityLevel": "secured",
    "securityBlockJailbrokenDevices": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value",
    "minAndroidSecurityPatchLevel": "Min Android Security Patch Level value",
    "storageRequireEncryption": true,
    "securityRequireSafetyNetAttestationBasicIntegrity": true,
    "securityRequireSafetyNetAttestationCertifiedDevice": true,
    "securityRequireGooglePlayServices": true,
    "securityRequireUpToDateSecurityProviders": true,
    "securityRequireCompanyPortalAppIntegrity": true
  }
}
```



