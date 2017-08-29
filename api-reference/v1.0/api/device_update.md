# <a name="update-device"></a><span data-ttu-id="cc4a5-101">Actualizar device</span><span class="sxs-lookup"><span data-stu-id="cc4a5-101">Update device</span></span>

<span data-ttu-id="cc4a5-102">Actualiza las propiedades de un dispositivo registrado.</span><span class="sxs-lookup"><span data-stu-id="cc4a5-102">Update the properties of a registered device.</span></span>

## <a name="permissions"></a><span data-ttu-id="cc4a5-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="cc4a5-103">Permissions</span></span>
<span data-ttu-id="cc4a5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="cc4a5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="cc4a5-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cc4a5-106">Permission type</span></span>      | <span data-ttu-id="cc4a5-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cc4a5-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="cc4a5-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cc4a5-108">Delegated (work or school account)</span></span> | <span data-ttu-id="cc4a5-109">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="cc4a5-109">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="cc4a5-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cc4a5-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cc4a5-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cc4a5-111">Not supported.</span></span>    |
|<span data-ttu-id="cc4a5-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cc4a5-112">Application</span></span> | <span data-ttu-id="cc4a5-113">Device.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cc4a5-113">Device.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="cc4a5-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cc4a5-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /devices/{id}
```
> <span data-ttu-id="cc4a5-115">Nota: El "id" de la solicitud es la propiedad "id" del dispositivo, no la propiedad "deviceId".</span><span class="sxs-lookup"><span data-stu-id="cc4a5-115">Note: The "id" in the request is the "id" property of the device, not the "deviceId" property.</span></span>

## <a name="request-headers"></a><span data-ttu-id="cc4a5-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cc4a5-116">Request headers</span></span>
| <span data-ttu-id="cc4a5-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="cc4a5-117">Name</span></span>       | <span data-ttu-id="cc4a5-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="cc4a5-118">Type</span></span> | <span data-ttu-id="cc4a5-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc4a5-119">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="cc4a5-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="cc4a5-120">Authorization</span></span>  | <span data-ttu-id="cc4a5-121">string</span><span class="sxs-lookup"><span data-stu-id="cc4a5-121">string</span></span>  | <span data-ttu-id="cc4a5-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cc4a5-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="cc4a5-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cc4a5-124">Request body</span></span>
<span data-ttu-id="cc4a5-125">En el cuerpo de la solicitud, proporcione los valores de las propiedades [device](../resources/device.md) que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="cc4a5-125">In the request body, supply the values for the [device](../resources/device.md) properties that should be updated.</span></span>

## <a name="response"></a><span data-ttu-id="cc4a5-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cc4a5-126">Response</span></span>

<span data-ttu-id="cc4a5-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="cc4a5-127">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="cc4a5-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cc4a5-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="cc4a5-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cc4a5-129">Request</span></span>
<span data-ttu-id="cc4a5-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cc4a5-130">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="cc4a5-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cc4a5-131">Response</span></span>
<span data-ttu-id="cc4a5-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cc4a5-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.device"
} -->
```http
HTTP/1.1 204 No Content
```
