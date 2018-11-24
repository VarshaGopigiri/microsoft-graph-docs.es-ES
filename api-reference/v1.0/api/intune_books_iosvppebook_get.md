# <a name="get-iosvppebook"></a><span data-ttu-id="f8e96-101">Obtener iosVppEBook</span><span class="sxs-lookup"><span data-stu-id="f8e96-101">Get iosVppEBook</span></span>

> <span data-ttu-id="f8e96-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f8e96-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f8e96-103">Lea las propiedades y las relaciones del objeto [iosVppEBook](../resources/intune_books_iosvppebook.md).</span><span class="sxs-lookup"><span data-stu-id="f8e96-103">Read properties and relationships of the [iosVppEBook](../resources/intune_books_iosvppebook.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f8e96-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f8e96-104">Prerequisites</span></span>
<span data-ttu-id="f8e96-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f8e96-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f8e96-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f8e96-107">Permission type</span></span>|<span data-ttu-id="f8e96-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f8e96-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f8e96-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f8e96-109">Delegated (work or school account)</span></span>|<span data-ttu-id="f8e96-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="f8e96-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="f8e96-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f8e96-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f8e96-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f8e96-112">Not supported.</span></span>|
|<span data-ttu-id="f8e96-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f8e96-113">Application</span></span>|<span data-ttu-id="f8e96-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f8e96-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f8e96-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f8e96-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedEBooks/{managedEBookId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="f8e96-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f8e96-116">Optional query parameters</span></span>
<span data-ttu-id="f8e96-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f8e96-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="f8e96-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f8e96-118">Request headers</span></span>
|<span data-ttu-id="f8e96-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8e96-119">Header</span></span>|<span data-ttu-id="f8e96-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f8e96-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f8e96-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="f8e96-121">Authorization</span></span>|<span data-ttu-id="f8e96-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f8e96-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f8e96-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f8e96-123">Accept</span></span>|<span data-ttu-id="f8e96-124">application/json</span><span class="sxs-lookup"><span data-stu-id="f8e96-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f8e96-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f8e96-125">Request body</span></span>
<span data-ttu-id="f8e96-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f8e96-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f8e96-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f8e96-127">Response</span></span>
<span data-ttu-id="f8e96-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosVppEBook](../resources/intune_books_iosvppebook.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f8e96-128">If successful, this method returns a `200 OK` response code and [iosVppEBook](../resources/intune_books_iosvppebook.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f8e96-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f8e96-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="f8e96-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f8e96-130">Request</span></span>
<span data-ttu-id="f8e96-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f8e96-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}
```

### <a name="response"></a><span data-ttu-id="f8e96-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f8e96-132">Response</span></span>
<span data-ttu-id="f8e96-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f8e96-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1033

{
  "value": {
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
    "vppTokenId": "9148ac60-ac60-9148-60ac-489160ac4891",
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
}
```



