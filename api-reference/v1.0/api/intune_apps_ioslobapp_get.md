# <a name="get-ioslobapp"></a><span data-ttu-id="e4988-101">Obtener iosLobApp</span><span class="sxs-lookup"><span data-stu-id="e4988-101">Get iosLobApp</span></span>

> <span data-ttu-id="e4988-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e4988-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e4988-103">Lea las propiedades y las relaciones del objeto [iosLobApp](../resources/intune_apps_ioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="e4988-103">Read properties and relationships of [plannerTaskDetails](../resources/intune_apps_ioslobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e4988-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e4988-104">Prerequisites</span></span>
<span data-ttu-id="e4988-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e4988-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e4988-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e4988-107">Permission type</span></span>|<span data-ttu-id="e4988-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e4988-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e4988-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e4988-109">Delegated (work or school account)</span></span>|<span data-ttu-id="e4988-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="e4988-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="e4988-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e4988-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e4988-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e4988-112">Not supported.</span></span>|
|<span data-ttu-id="e4988-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e4988-113">Application</span></span>|<span data-ttu-id="e4988-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e4988-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e4988-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e4988-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="e4988-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e4988-116">Optional query parameters</span></span>
<span data-ttu-id="e4988-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e4988-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="e4988-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e4988-118">Request headers</span></span>
|<span data-ttu-id="e4988-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e4988-119">Header</span></span>|<span data-ttu-id="e4988-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e4988-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e4988-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="e4988-121">Authorization</span></span>|<span data-ttu-id="e4988-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e4988-122">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="e4988-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e4988-123">Accept</span></span>|<span data-ttu-id="e4988-124">application/json</span><span class="sxs-lookup"><span data-stu-id="e4988-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e4988-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e4988-125">Request body</span></span>
<span data-ttu-id="e4988-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e4988-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e4988-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e4988-127">Response</span></span>
<span data-ttu-id="e4988-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosLobApp](../resources/intune_apps_ioslobapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e4988-128">If successful, this method returns a `200 OK` response code and a [ListItemVersion](../resources/intune_apps_ioslobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e4988-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e4988-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="e4988-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e4988-130">Request</span></span>
<span data-ttu-id="e4988-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e4988-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
```

### <a name="response"></a><span data-ttu-id="e4988-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e4988-132">Response</span></span>
<span data-ttu-id="e4988-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e4988-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1456

{
  "value": {
    "@odata.type": "#microsoft.graph.iosLobApp",
    "id": "b34052ea-52ea-b340-ea52-40b3ea5240b3",
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
    "committedContentVersion": "Committed Content Version value",
    "fileName": "File Name value",
    "size": 4,
    "bundleId": "Bundle Id value",
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
      "v11_0": true
    },
    "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
    "versionNumber": "Version Number value",
    "buildNumber": "Build Number value"
  }
}
```



