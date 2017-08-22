# <a name="update-device"></a><span data-ttu-id="69dc7-101">Actualizar device</span><span class="sxs-lookup"><span data-stu-id="69dc7-101">Update device</span></span>

<span data-ttu-id="69dc7-102">Actualiza las propiedades de un dispositivo registrado.</span><span class="sxs-lookup"><span data-stu-id="69dc7-102">Update the properties of a registered device.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="69dc7-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="69dc7-103">Prerequisites</span></span>
<span data-ttu-id="69dc7-104">Se necesita uno de los siguientes **ámbitos** para ejecutar esta API: *Device.ReadWrite.All* o *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="69dc7-104">One of the following **scopes** is required to execute this API: *Device.ReadWrite.All* or *Directory.AccessAsUser.All*</span></span> 

## <a name="http-request"></a><span data-ttu-id="69dc7-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="69dc7-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /devices/{id}
```
> <span data-ttu-id="69dc7-106">Nota: El "id" de la solicitud es la propiedad "id" del dispositivo, no la propiedad "deviceId".</span><span class="sxs-lookup"><span data-stu-id="69dc7-106">Note: The "id" in the request is the "id" property of the device, not the "deviceId" property.</span></span>

## <a name="request-headers"></a><span data-ttu-id="69dc7-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="69dc7-107">Request headers</span></span>
| <span data-ttu-id="69dc7-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="69dc7-108">Name</span></span>       | <span data-ttu-id="69dc7-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="69dc7-109">Type</span></span> | <span data-ttu-id="69dc7-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="69dc7-110">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="69dc7-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="69dc7-111">Authorization</span></span>  | <span data-ttu-id="69dc7-112">string</span><span class="sxs-lookup"><span data-stu-id="69dc7-112">string</span></span>  | <span data-ttu-id="69dc7-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="69dc7-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="69dc7-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="69dc7-115">Request body</span></span>
<span data-ttu-id="69dc7-116">En el cuerpo de la solicitud, proporcione los valores de las propiedades [device](../resources/device.md) que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="69dc7-116">In the request body, supply the values for the [device](../resources/device.md) properties that should be updated.</span></span>

## <a name="response"></a><span data-ttu-id="69dc7-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="69dc7-117">Response</span></span>

<span data-ttu-id="69dc7-118">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="69dc7-118">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="69dc7-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="69dc7-119">Example</span></span>
##### <a name="request"></a><span data-ttu-id="69dc7-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="69dc7-120">Request</span></span>
<span data-ttu-id="69dc7-121">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="69dc7-121">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_device"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/devices/{id}
Content-type: application/json

{
  "accountEnabled": true
}
```
##### <a name="response"></a><span data-ttu-id="69dc7-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="69dc7-122">Response</span></span>
<span data-ttu-id="69dc7-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="69dc7-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.device"
} -->
```http
HTTP/1.1 204 No Content
```
