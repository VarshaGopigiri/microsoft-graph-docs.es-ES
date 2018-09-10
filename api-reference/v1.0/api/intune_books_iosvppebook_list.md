# <a name="list-iosvppebooks"></a><span data-ttu-id="3a39d-101">Enumerar iosVppEBooks</span><span class="sxs-lookup"><span data-stu-id="3a39d-101">List iosVppEBooks</span></span>

> <span data-ttu-id="3a39d-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3a39d-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3a39d-103">Enumere las propiedades y las relaciones de los objetos [iosVppEBook](../resources/intune_books_iosvppebook.md).</span><span class="sxs-lookup"><span data-stu-id="3a39d-103">List properties and relationships of the [iosVppEBook](../resources/intune_books_iosvppebook.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3a39d-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3a39d-104">Prerequisites</span></span>
<span data-ttu-id="3a39d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="3a39d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="3a39d-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3a39d-107">Permission type</span></span>|<span data-ttu-id="3a39d-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3a39d-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3a39d-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3a39d-109">Delegated (work or school account)</span></span>|<span data-ttu-id="3a39d-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="3a39d-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="3a39d-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3a39d-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3a39d-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3a39d-112">Not supported.</span></span>|
|<span data-ttu-id="3a39d-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3a39d-113">Application</span></span>|<span data-ttu-id="3a39d-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3a39d-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3a39d-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3a39d-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedEBooks
```

## <a name="request-headers"></a><span data-ttu-id="3a39d-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3a39d-116">Request headers</span></span>
|<span data-ttu-id="3a39d-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a39d-117">Header</span></span>|<span data-ttu-id="3a39d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3a39d-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3a39d-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="3a39d-119">Authorization</span></span>|<span data-ttu-id="3a39d-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3a39d-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3a39d-121">Accept</span><span class="sxs-lookup"><span data-stu-id="3a39d-121">Accept</span></span>|<span data-ttu-id="3a39d-122">application/json</span><span class="sxs-lookup"><span data-stu-id="3a39d-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3a39d-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3a39d-123">Request body</span></span>
<span data-ttu-id="3a39d-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3a39d-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3a39d-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3a39d-125">Response</span></span>
<span data-ttu-id="3a39d-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [iosVppEBook](../resources/intune_books_iosvppebook.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3a39d-126">If successful, this method returns a `200 OK` response code and a collection of [iosVppEBook](../resources/intune_books_iosvppebook.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3a39d-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3a39d-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="3a39d-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3a39d-128">Request</span></span>
<span data-ttu-id="3a39d-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3a39d-129">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks
```

### <a name="response"></a><span data-ttu-id="3a39d-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3a39d-130">Response</span></span>
<span data-ttu-id="3a39d-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3a39d-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1094

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.iosVppEBook",
      "id": "3b9f627e-627e-3b9f-7e62-9f3b7e629f3b",
      "displayName": "Display Name value",
      "description": "Description value",
      "publisher": "Publisher value",
      "publishedDateTime": "2016-12-31T23:58:16.1180489-08:00",
      "largeCover": {
        "@odata.type": "microsoft.graph.mimeContent",
        "type": "Type value",
        "value": "dmFsdWU="
      },
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "informationUrl": "https://example.com/informationUrl/",
      "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
      "vppTokenId": "<Unknown Primitive Type Edm.Guid>",
      "appleId": "Apple Id value",
      "vppOrganizationName": "Vpp Organization Name value",
      "genres": [
        "Genres value"
      ],
      "language": "Language value",
      "seller": "Seller value",
      "totalLicenseCount": 1,
      "usedLicenseCount": 0
    }
  ]
}
```








