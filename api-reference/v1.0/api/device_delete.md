# <a name="delete-device"></a><span data-ttu-id="e028b-101">Delete device</span><span class="sxs-lookup"><span data-stu-id="e028b-101">Delete device</span></span>

<span data-ttu-id="e028b-102">Elimina un dispositivo registrado.</span><span class="sxs-lookup"><span data-stu-id="e028b-102">Delete a registered device.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e028b-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e028b-103">Prerequisites</span></span>
<span data-ttu-id="e028b-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.AccessAsUser.All*, *Device.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="e028b-104">One of the following **scopes** is required to execute this API: *Directory.AccessAsUser.All*, *Device.ReadWrite.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="e028b-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e028b-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /devices/{id}
```
> <span data-ttu-id="e028b-106">Nota: El "id" de la solicitud es la propiedad "id" del dispositivo, no la propiedad "deviceId".</span><span class="sxs-lookup"><span data-stu-id="e028b-106">Note: The "id" in the request is the "id" property of the device, not the "deviceId" property.</span></span>

## <a name="request-headers"></a><span data-ttu-id="e028b-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e028b-107">Request headers</span></span>
| <span data-ttu-id="e028b-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="e028b-108">Name</span></span>       | <span data-ttu-id="e028b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e028b-109">Type</span></span> | <span data-ttu-id="e028b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e028b-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="e028b-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="e028b-111">Authorization</span></span>  | <span data-ttu-id="e028b-112">string</span><span class="sxs-lookup"><span data-stu-id="e028b-112">string</span></span>  | <span data-ttu-id="e028b-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e028b-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e028b-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e028b-115">Request body</span></span>
<span data-ttu-id="e028b-116">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e028b-116">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e028b-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e028b-117">Response</span></span>

<span data-ttu-id="e028b-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e028b-p102">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e028b-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e028b-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e028b-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e028b-121">Request</span></span>
<span data-ttu-id="e028b-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e028b-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_device"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/devices/{id}
```
##### <a name="response"></a><span data-ttu-id="e028b-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e028b-123">Response</span></span>
<span data-ttu-id="e028b-124">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e028b-124">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete device",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
