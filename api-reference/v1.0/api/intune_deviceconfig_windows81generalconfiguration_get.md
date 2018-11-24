# <a name="get-windows81generalconfiguration"></a><span data-ttu-id="f67f1-101">Obtener windows81GeneralConfiguration</span><span class="sxs-lookup"><span data-stu-id="f67f1-101">Get windows81GeneralConfiguration</span></span>

> <span data-ttu-id="f67f1-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f67f1-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f67f1-103">Lea las propiedades y las relaciones del objeto [windows81GeneralConfiguration](../resources/intune_deviceconfig_windows81generalconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="f67f1-103">Read properties and relationships of the [windows81GeneralConfiguration](../resources/intune_deviceconfig_windows81generalconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f67f1-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f67f1-104">Prerequisites</span></span>
<span data-ttu-id="f67f1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f67f1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f67f1-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f67f1-107">Permission type</span></span>|<span data-ttu-id="f67f1-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f67f1-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f67f1-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f67f1-109">Delegated (work or school account)</span></span>|<span data-ttu-id="f67f1-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="f67f1-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="f67f1-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f67f1-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f67f1-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f67f1-112">Not supported.</span></span>|
|<span data-ttu-id="f67f1-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f67f1-113">Application</span></span>|<span data-ttu-id="f67f1-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f67f1-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f67f1-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f67f1-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="f67f1-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f67f1-116">Optional query parameters</span></span>
<span data-ttu-id="f67f1-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f67f1-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="f67f1-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f67f1-118">Request headers</span></span>
|<span data-ttu-id="f67f1-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f67f1-119">Header</span></span>|<span data-ttu-id="f67f1-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f67f1-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f67f1-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="f67f1-121">Authorization</span></span>|<span data-ttu-id="f67f1-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f67f1-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f67f1-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f67f1-123">Accept</span></span>|<span data-ttu-id="f67f1-124">application/json</span><span class="sxs-lookup"><span data-stu-id="f67f1-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f67f1-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f67f1-125">Request body</span></span>
<span data-ttu-id="f67f1-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f67f1-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f67f1-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f67f1-127">Response</span></span>
<span data-ttu-id="f67f1-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows81GeneralConfiguration](../resources/intune_deviceconfig_windows81generalconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f67f1-128">If successful, this method returns a `200 OK` response code and [windows81GeneralConfiguration](../resources/intune_deviceconfig_windows81generalconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f67f1-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f67f1-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="f67f1-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f67f1-130">Request</span></span>
<span data-ttu-id="f67f1-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f67f1-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="f67f1-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f67f1-132">Response</span></span>
<span data-ttu-id="f67f1-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f67f1-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1964

{
  "value": {
    "@odata.type": "#microsoft.graph.windows81GeneralConfiguration",
    "id": "0e9285b5-85b5-0e92-b585-920eb585920e",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7,
    "accountsBlockAddingNonMicrosoftAccountEmail": true,
    "applyOnlyToWindows81": true,
    "browserBlockAutofill": true,
    "browserBlockAutomaticDetectionOfIntranetSites": true,
    "browserBlockEnterpriseModeAccess": true,
    "browserBlockJavaScript": true,
    "browserBlockPlugins": true,
    "browserBlockPopups": true,
    "browserBlockSendingDoNotTrackHeader": true,
    "browserBlockSingleWordEntryOnIntranetSites": true,
    "browserRequireSmartScreen": true,
    "browserEnterpriseModeSiteListLocation": "Browser Enterprise Mode Site List Location value",
    "browserInternetSecurityLevel": "medium",
    "browserIntranetSecurityLevel": "low",
    "browserLoggingReportLocation": "Browser Logging Report Location value",
    "browserRequireHighSecurityForRestrictedSites": true,
    "browserRequireFirewall": true,
    "browserRequireFraudWarning": true,
    "browserTrustedSitesSecurityLevel": "low",
    "cellularBlockDataRoaming": true,
    "diagnosticsBlockDataSubmission": true,
    "passwordBlockPicturePasswordAndPin": true,
    "passwordExpirationDays": 6,
    "passwordMinimumLength": 5,
    "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
    "passwordMinimumCharacterSetCount": 0,
    "passwordPreviousPasswordBlockCount": 2,
    "passwordRequiredType": "alphanumeric",
    "passwordSignInFailureCountBeforeFactoryReset": 12,
    "storageRequireDeviceEncryption": true,
    "updatesRequireAutomaticUpdates": true,
    "userAccountControlSettings": "alwaysNotify",
    "workFoldersUrl": "https://example.com/workFoldersUrl/"
  }
}
```



