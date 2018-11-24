# <a name="get-managediosstoreapp"></a><span data-ttu-id="ffcbe-101">Obtener managedIOSStoreApp</span><span class="sxs-lookup"><span data-stu-id="ffcbe-101">Get managedIOSStoreApp</span></span>

> <span data-ttu-id="ffcbe-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ffcbe-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ffcbe-103">Lea las propiedades y las relaciones del objeto [managedIOSStoreApp](../resources/intune_apps_managediosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="ffcbe-103">Read properties and relationships of the [managedIOSStoreApp](../resources/intune_apps_managediosstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ffcbe-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ffcbe-104">Prerequisites</span></span>
<span data-ttu-id="ffcbe-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ffcbe-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ffcbe-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ffcbe-107">Permission type</span></span>|<span data-ttu-id="ffcbe-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ffcbe-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ffcbe-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ffcbe-109">Delegated (work or school account)</span></span>|<span data-ttu-id="ffcbe-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="ffcbe-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="ffcbe-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ffcbe-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ffcbe-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ffcbe-112">Not supported.</span></span>|
|<span data-ttu-id="ffcbe-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ffcbe-113">Application</span></span>|<span data-ttu-id="ffcbe-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ffcbe-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ffcbe-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ffcbe-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="ffcbe-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ffcbe-116">Optional query parameters</span></span>
<span data-ttu-id="ffcbe-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ffcbe-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="ffcbe-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ffcbe-118">Request headers</span></span>
|<span data-ttu-id="ffcbe-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ffcbe-119">Header</span></span>|<span data-ttu-id="ffcbe-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ffcbe-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ffcbe-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="ffcbe-121">Authorization</span></span>|<span data-ttu-id="ffcbe-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ffcbe-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ffcbe-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ffcbe-123">Accept</span></span>|<span data-ttu-id="ffcbe-124">application/json</span><span class="sxs-lookup"><span data-stu-id="ffcbe-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ffcbe-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ffcbe-125">Request body</span></span>
<span data-ttu-id="ffcbe-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ffcbe-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ffcbe-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ffcbe-127">Response</span></span>
<span data-ttu-id="ffcbe-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedIOSStoreApp](../resources/intune_apps_managediosstoreapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ffcbe-128">If successful, this method returns a `200 OK` response code and [managedIOSStoreApp](../resources/intune_apps_managediosstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ffcbe-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ffcbe-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="ffcbe-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ffcbe-130">Request</span></span>
<span data-ttu-id="ffcbe-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ffcbe-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
```

### <a name="response"></a><span data-ttu-id="ffcbe-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ffcbe-132">Response</span></span>
<span data-ttu-id="ffcbe-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ffcbe-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1347

{
  "value": {
    "@odata.type": "#microsoft.graph.managedIOSStoreApp",
    "id": "51b9830f-830f-51b9-0f83-b9510f83b951",
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
    "appAvailability": "lineOfBusiness",
    "version": "Version value",
    "bundleId": "Bundle Id value",
    "appStoreUrl": "https://example.com/appStoreUrl/",
    "applicableDeviceType": {
      "@odata.type": "microsoft.graph.iosDeviceType",
      "iPad": true,
      "iPhoneAndIPod": true
    },
    "minimumSupportedOperatingSystem": {
      "@odata.type": "microsoft.graph.iosMinimumOperatingSystem",
      "v8_0": true,
      "v9_0": true,
      "v10_0": true,
      "v11_0": true,
      "v12_0": true
    }
  }
}
```



