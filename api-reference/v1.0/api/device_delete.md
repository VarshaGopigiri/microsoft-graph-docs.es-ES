# <a name="delete-device"></a><span data-ttu-id="589e7-101">Delete device</span><span class="sxs-lookup"><span data-stu-id="589e7-101">Delete device</span></span>

<span data-ttu-id="589e7-102">Elimina un dispositivo registrado.</span><span class="sxs-lookup"><span data-stu-id="589e7-102">Delete a registered device.</span></span>

## <a name="permissions"></a><span data-ttu-id="589e7-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="589e7-103">Permissions</span></span>
<span data-ttu-id="589e7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="589e7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="589e7-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="589e7-106">Permission type</span></span>      | <span data-ttu-id="589e7-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="589e7-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="589e7-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="589e7-108">Delegated (work or school account)</span></span> | <span data-ttu-id="589e7-109">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="589e7-109">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="589e7-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="589e7-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="589e7-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="589e7-111">Not supported.</span></span>    |
|<span data-ttu-id="589e7-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="589e7-112">Application</span></span> | <span data-ttu-id="589e7-113">Device.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="589e7-113">Device.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="589e7-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="589e7-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /devices/{id}
```
> <span data-ttu-id="589e7-115">Nota: El "id" de la solicitud es la propiedad "id" del dispositivo, no la propiedad "deviceId".</span><span class="sxs-lookup"><span data-stu-id="589e7-115">Note: The "id" in the request is the "id" property of the device, not the "deviceId" property.</span></span>

## <a name="request-headers"></a><span data-ttu-id="589e7-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="589e7-116">Request headers</span></span>
| <span data-ttu-id="589e7-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="589e7-117">Name</span></span>       | <span data-ttu-id="589e7-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="589e7-118">Type</span></span> | <span data-ttu-id="589e7-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="589e7-119">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="589e7-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="589e7-120">Authorization</span></span>  | <span data-ttu-id="589e7-121">string</span><span class="sxs-lookup"><span data-stu-id="589e7-121">string</span></span>  | <span data-ttu-id="589e7-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="589e7-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="589e7-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="589e7-124">Request body</span></span>
<span data-ttu-id="589e7-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="589e7-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="589e7-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="589e7-126">Response</span></span>

<span data-ttu-id="589e7-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="589e7-p103">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="589e7-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="589e7-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="589e7-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="589e7-130">Request</span></span>
<span data-ttu-id="589e7-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="589e7-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_device"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/devices/{id}
```
##### <a name="response"></a><span data-ttu-id="589e7-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="589e7-132">Response</span></span>
<span data-ttu-id="589e7-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="589e7-133">Here is an example of the response.</span></span>
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
