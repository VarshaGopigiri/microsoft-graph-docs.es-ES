# <a name="create-device"></a><span data-ttu-id="224b7-101">Create device</span><span class="sxs-lookup"><span data-stu-id="224b7-101">Create device</span></span>

<span data-ttu-id="224b7-102">Crea y registra un nuevo dispositivo en la organización.</span><span class="sxs-lookup"><span data-stu-id="224b7-102">Create and register a new device in the organization.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="224b7-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="224b7-103">Prerequisites</span></span>
<span data-ttu-id="224b7-104">Se necesita uno de los siguientes **ámbitos** para ejecutar esta API: *Device.ReadWrite.All* o *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="224b7-104">One of the following **scopes** is required to execute this API: *Device.ReadWrite.All* or *Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="224b7-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="224b7-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /devices

```
## <a name="request-headers"></a><span data-ttu-id="224b7-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="224b7-106">Request headers</span></span>
| <span data-ttu-id="224b7-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="224b7-107">Name</span></span>       | <span data-ttu-id="224b7-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="224b7-108">Type</span></span> | <span data-ttu-id="224b7-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="224b7-109">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="224b7-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="224b7-110">Authorization</span></span>  | <span data-ttu-id="224b7-111">string</span><span class="sxs-lookup"><span data-stu-id="224b7-111">string</span></span>  | <span data-ttu-id="224b7-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="224b7-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="224b7-114">Tipo de contenido</span><span class="sxs-lookup"><span data-stu-id="224b7-114">Content-type</span></span> | <span data-ttu-id="224b7-115">string</span><span class="sxs-lookup"><span data-stu-id="224b7-115">string</span></span> | <span data-ttu-id="224b7-116">application/json</span><span class="sxs-lookup"><span data-stu-id="224b7-116">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="224b7-117">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="224b7-117">Request body</span></span>
<span data-ttu-id="224b7-118">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [device](../resources/device.md).</span><span class="sxs-lookup"><span data-stu-id="224b7-118">In the request body, supply a JSON representation of [device](../resources/device.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="224b7-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="224b7-119">Response</span></span>

<span data-ttu-id="224b7-120">Si se ejecuta correctamente, este método devuelve un código de respuesta `201, Created` y el objeto [device](../resources/device.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="224b7-120">If successful, this method returns `201, Created` response code and [device](../resources/device.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="224b7-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="224b7-121">Example</span></span>
##### <a name="request"></a><span data-ttu-id="224b7-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="224b7-122">Request</span></span>
<span data-ttu-id="224b7-123">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="224b7-123">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_device_from_devices"
}-->
```http
POST https://graph.microsoft.com/v1.0/devices
Content-type: application/json

{
  "accountEnabled":false,
  "alternativeSecurityIds":
  [
    {
      "type":2,
      "key":"Y3YxN2E1MWFlYw=="
    }
  ],
  "deviceId":"4c299165-6e8f-4b45-a5ba-c5d250a707ff",
  "displayName":"Test device",
  "operatingSystem":"linux",
  "operatingSystemVersion":"1"
}
```
<span data-ttu-id="224b7-124">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [device](../resources/device.md).</span><span class="sxs-lookup"><span data-stu-id="224b7-124">In the request body, supply a JSON representation of [device](../resources/device.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="224b7-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="224b7-125">Response</span></span>
<span data-ttu-id="224b7-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="224b7-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.device"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "accountEnabled":false,
  "alternativeSecurityIds":
  [
    {
      "type":2,
      "key":"Y3YxN2E1MWFlYw=="
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
  "description": "Create device",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
