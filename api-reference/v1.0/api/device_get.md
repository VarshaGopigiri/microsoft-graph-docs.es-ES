# <a name="get-device"></a><span data-ttu-id="bef92-101">Obtener device</span><span class="sxs-lookup"><span data-stu-id="bef92-101">Get device</span></span>

<span data-ttu-id="bef92-102">Obtiene las propiedades y relaciones de un objeto device.</span><span class="sxs-lookup"><span data-stu-id="bef92-102">Get the properties and relationships of a device object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bef92-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bef92-103">Prerequisites</span></span>
<span data-ttu-id="bef92-104">Se necesita uno de los siguientes **ámbitos** para ejecutar esta API: *Device.ReadWrite.All*, *Directory.Read.All*, *Directory.ReadWrite.All* o *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="bef92-104">One of the following **scopes** is required to execute this API: *Device.ReadWrite.All* or *Directory.Read.All* or *Directory.ReadWrite.All* or *Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="bef92-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bef92-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /devices/{id}
```
> <span data-ttu-id="bef92-106">Nota: El "id" de la solicitud es la propiedad "id" del dispositivo, no la propiedad "deviceId".</span><span class="sxs-lookup"><span data-stu-id="bef92-106">Note: The "id" in the request is the "id" property of the device, not the "deviceId" property.</span></span>

## <a name="optional-query-parameters"></a><span data-ttu-id="bef92-107">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="bef92-107">Optional query parameters</span></span>
<span data-ttu-id="bef92-108">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bef92-108">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="bef92-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bef92-109">Request headers</span></span>
| <span data-ttu-id="bef92-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="bef92-110">Name</span></span>       | <span data-ttu-id="bef92-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="bef92-111">Type</span></span> | <span data-ttu-id="bef92-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="bef92-112">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="bef92-113">Authorization</span><span class="sxs-lookup"><span data-stu-id="bef92-113">Authorization</span></span>  | <span data-ttu-id="bef92-114">string</span><span class="sxs-lookup"><span data-stu-id="bef92-114">string</span></span>  | <span data-ttu-id="bef92-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bef92-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="bef92-117">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bef92-117">Request body</span></span>
<span data-ttu-id="bef92-118">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bef92-118">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bef92-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bef92-119">Response</span></span>

<span data-ttu-id="bef92-120">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [device](../resources/device.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bef92-120">If successful, this method returns a `200 OK` response code and [device](../resources/device.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="bef92-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bef92-121">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bef92-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bef92-122">Request</span></span>
<span data-ttu-id="bef92-123">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bef92-123">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_device"
}-->
```http
GET https://graph.microsoft.com/v1.0/devices/{id}
```
##### <a name="response"></a><span data-ttu-id="bef92-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bef92-124">Response</span></span>
<span data-ttu-id="bef92-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bef92-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.device"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "accountEnabled":false,
  "alternativeSecurityIds":
  [
    {
      "type": 2,
      "key":"Y3YxN2E1MWFlYw==",
      "identityProvider": null
    }
  ],
  "deviceId":"4c299165-6e8f-4b45-a5ba-c5d250a707ff",
  "displayName":"Test device",
  "id": "id-value",
  "operatingSystem":"linux",
  "operatingSystemVersion":"1"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get device",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
