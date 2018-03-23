# <a name="list-managediosstoreapps"></a><span data-ttu-id="11e43-101">Enumerar managedIOSStoreApps</span><span class="sxs-lookup"><span data-stu-id="11e43-101">List managedIOSStoreApps</span></span>

> <span data-ttu-id="11e43-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="11e43-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="11e43-103">Enumere las propiedades y las relaciones de los objetos [managedIOSStoreApp](../resources/intune_apps_managediosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="11e43-103">List properties and relationships of the [managedIOSStoreApp](../resources/intune_apps_managediosstoreapp.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="11e43-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="11e43-104">Prerequisites</span></span>
<span data-ttu-id="11e43-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="11e43-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="11e43-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="11e43-107">Permission type</span></span>|<span data-ttu-id="11e43-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="11e43-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="11e43-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="11e43-109">Delegated (work or school account)</span></span>|<span data-ttu-id="11e43-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="11e43-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="11e43-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="11e43-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="11e43-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="11e43-112">Not supported.</span></span>|
|<span data-ttu-id="11e43-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="11e43-113">Application</span></span>|<span data-ttu-id="11e43-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="11e43-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="11e43-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="11e43-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="11e43-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="11e43-116">Request headers</span></span>
|<span data-ttu-id="11e43-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11e43-117">Header</span></span>|<span data-ttu-id="11e43-118">Valor</span><span class="sxs-lookup"><span data-stu-id="11e43-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="11e43-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="11e43-119">Authorization</span></span>|<span data-ttu-id="11e43-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="11e43-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="11e43-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="11e43-121">Accept</span></span>|<span data-ttu-id="11e43-122">application/json</span><span class="sxs-lookup"><span data-stu-id="11e43-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="11e43-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="11e43-123">Request body</span></span>
<span data-ttu-id="11e43-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="11e43-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="11e43-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="11e43-125">Response</span></span>
<span data-ttu-id="11e43-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [managedIOSStoreApp](../resources/intune_apps_managediosstoreapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="11e43-126">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/intune_apps_managediosstoreapp.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="11e43-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="11e43-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="11e43-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="11e43-128">Request</span></span>
<span data-ttu-id="11e43-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="11e43-129">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
```

### <a name="response"></a><span data-ttu-id="11e43-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="11e43-130">Response</span></span>
<span data-ttu-id="11e43-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="11e43-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1409

{
  "value": [
    {
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
        "v11_0": true
      }
    }
  ]
}
```



