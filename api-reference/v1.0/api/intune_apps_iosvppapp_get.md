# <a name="get-iosvppapp"></a><span data-ttu-id="30040-101">Obtener iosVppApp</span><span class="sxs-lookup"><span data-stu-id="30040-101">Get iosVppApp</span></span>

> <span data-ttu-id="30040-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="30040-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="30040-103">Lea las propiedades y las relaciones del objeto [iosVppApp](../resources/intune_apps_iosvppapp.md).</span><span class="sxs-lookup"><span data-stu-id="30040-103">Read properties and relationships of the [iosVppApp](../resources/intune_apps_iosvppapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="30040-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="30040-104">Prerequisites</span></span>
<span data-ttu-id="30040-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="30040-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="30040-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="30040-107">Permission type</span></span>|<span data-ttu-id="30040-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="30040-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="30040-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="30040-109">Delegated (work or school account)</span></span>|<span data-ttu-id="30040-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="30040-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="30040-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="30040-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="30040-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="30040-112">Not supported.</span></span>|
|<span data-ttu-id="30040-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="30040-113">Application</span></span>|<span data-ttu-id="30040-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="30040-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="30040-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="30040-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="30040-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="30040-116">Optional query parameters</span></span>
<span data-ttu-id="30040-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="30040-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="30040-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="30040-118">Request headers</span></span>
|<span data-ttu-id="30040-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30040-119">Header</span></span>|<span data-ttu-id="30040-120">Valor</span><span class="sxs-lookup"><span data-stu-id="30040-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="30040-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="30040-121">Authorization</span></span>|<span data-ttu-id="30040-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="30040-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="30040-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="30040-123">Accept</span></span>|<span data-ttu-id="30040-124">application/json</span><span class="sxs-lookup"><span data-stu-id="30040-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="30040-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="30040-125">Request body</span></span>
<span data-ttu-id="30040-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="30040-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="30040-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="30040-127">Response</span></span>
<span data-ttu-id="30040-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosVppApp](../resources/intune_apps_iosvppapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="30040-128">If successful, this method returns a `200 OK` response code and [iosVppApp](../resources/intune_apps_iosvppapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="30040-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="30040-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="30040-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="30040-130">Request</span></span>
<span data-ttu-id="30040-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="30040-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
```

### <a name="response"></a><span data-ttu-id="30040-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="30040-132">Response</span></span>
<span data-ttu-id="30040-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="30040-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1487

{
  "value": {
    "@odata.type": "#microsoft.graph.iosVppApp",
    "id": "a0ac9b6f-9b6f-a0ac-6f9b-aca06f9baca0",
    "displayName": "Display Name value",
    "description": "Description value",
    "publisher": "Publisher value",
    "largeIcon": {
      "@odata.type": "microsoft.graph.mimeContent",
      "type": "Type value",
      "value": "dmFsdWU="
    },
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "isFeatured": true,
    "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
    "informationUrl": "https://example.com/informationUrl/",
    "owner": "Owner value",
    "developer": "Developer value",
    "notes": "Notes value",
    "publishingState": "processing",
    "usedLicenseCount": 0,
    "totalLicenseCount": 1,
    "releaseDateTime": "2017-01-01T00:01:34.7470482-08:00",
    "appStoreUrl": "https://example.com/appStoreUrl/",
    "licensingType": {
      "@odata.type": "microsoft.graph.vppLicensingType",
      "supportsUserLicensing": true,
      "supportsDeviceLicensing": true
    },
    "applicableDeviceType": {
      "@odata.type": "microsoft.graph.iosDeviceType",
      "iPad": true,
      "iPhoneAndIPod": true
    },
    "vppTokenOrganizationName": "Vpp Token Organization Name value",
    "vppTokenAccountType": "education",
    "vppTokenAppleId": "Vpp Token Apple Id value",
    "bundleId": "Bundle Id value"
  }
}
```



