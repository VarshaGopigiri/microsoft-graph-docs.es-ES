# <a name="list-devices"></a><span data-ttu-id="a007e-101">List devices</span><span class="sxs-lookup"><span data-stu-id="a007e-101">List devices</span></span>

<span data-ttu-id="a007e-102">Recupera una lista de objetos de dispositivo registrados en la organización.</span><span class="sxs-lookup"><span data-stu-id="a007e-102">Retrieve a list of device objects registered in the organization.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a007e-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a007e-103">Prerequisites</span></span>
<span data-ttu-id="a007e-104">Se necesita uno de los siguientes **ámbitos** para ejecutar esta API: *Device.ReadWrite.All*, *Directory.Read.All*, *Directory.ReadWrite.All* o *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="a007e-104">One of the following **scopes** is required to execute this API: *Device.ReadWrite.All* or *Directory.Read.All* or *Directory.ReadWrite.All* or *Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="a007e-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a007e-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /devices
```
## <a name="optional-query-parameters"></a><span data-ttu-id="a007e-106">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a007e-106">Optional query parameters</span></span>
<span data-ttu-id="a007e-107">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a007e-107">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="a007e-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a007e-108">Request headers</span></span>
| <span data-ttu-id="a007e-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="a007e-109">Name</span></span>       | <span data-ttu-id="a007e-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="a007e-110">Type</span></span> | <span data-ttu-id="a007e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a007e-111">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="a007e-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="a007e-112">Authorization</span></span>  | <span data-ttu-id="a007e-113">string</span><span class="sxs-lookup"><span data-stu-id="a007e-113">string</span></span>  | <span data-ttu-id="a007e-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a007e-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a007e-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a007e-116">Request body</span></span>
<span data-ttu-id="a007e-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a007e-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a007e-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a007e-118">Response</span></span>

<span data-ttu-id="a007e-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [device](../resources/device.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a007e-119">If successful, this method returns a `200 OK` response code and collection of [device](../resources/device.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="a007e-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a007e-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a007e-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a007e-121">Request</span></span>
<span data-ttu-id="a007e-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a007e-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_devices"
}-->
```http
GET https://graph.microsoft.com/v1.0/devices
```

##### <a name="response"></a><span data-ttu-id="a007e-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a007e-123">Response</span></span>
<span data-ttu-id="a007e-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a007e-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.device",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "accountEnabled":false,
      "alternativeSecurityIds":
      [
        {
          "type":2,
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
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List devices",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
