# <a name="delete-plannerbucket"></a><span data-ttu-id="7fbcf-101">Eliminar plannerBucket</span><span class="sxs-lookup"><span data-stu-id="7fbcf-101">Delete plannerBucket</span></span>

<span data-ttu-id="7fbcf-102">Eliminar **plannerBucket**.</span><span class="sxs-lookup"><span data-stu-id="7fbcf-102">Delete **plannerBucket**.</span></span>
## <a name="permissions"></a><span data-ttu-id="7fbcf-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="7fbcf-103">Permissions</span></span>
<span data-ttu-id="7fbcf-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="7fbcf-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="7fbcf-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7fbcf-106">Permission type</span></span>      | <span data-ttu-id="7fbcf-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7fbcf-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7fbcf-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7fbcf-108">Delegated (work or school account)</span></span> | <span data-ttu-id="7fbcf-109">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7fbcf-109">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="7fbcf-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7fbcf-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7fbcf-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7fbcf-111">Not supported.</span></span>    |
|<span data-ttu-id="7fbcf-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7fbcf-112">Application</span></span> | <span data-ttu-id="7fbcf-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7fbcf-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="7fbcf-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7fbcf-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /planner/buckets/{id}
```
## <a name="request-headers"></a><span data-ttu-id="7fbcf-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7fbcf-115">Request headers</span></span>
| <span data-ttu-id="7fbcf-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="7fbcf-116">Name</span></span>       | <span data-ttu-id="7fbcf-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="7fbcf-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="7fbcf-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="7fbcf-118">Authorization</span></span>  | <span data-ttu-id="7fbcf-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7fbcf-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="7fbcf-121">If-Match</span><span class="sxs-lookup"><span data-stu-id="7fbcf-121">If-Match</span></span>  | <span data-ttu-id="7fbcf-p103">Último valor ETag conocido para que se elimine **plannerBucket**. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7fbcf-p103">Last known ETag value for the **plannerBucket** to be deleted. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="7fbcf-124">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="7fbcf-124">Request body</span></span>
<span data-ttu-id="7fbcf-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7fbcf-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7fbcf-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7fbcf-126">Response</span></span>

<span data-ttu-id="7fbcf-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7fbcf-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

<span data-ttu-id="7fbcf-p105">Este método puede devolver cualquiera de los [códigos de estado HTTP](../../../concepts/errors.md). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="7fbcf-p105">This method can return any of the [HTTP status codes](../../../concepts/errors.md). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="7fbcf-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7fbcf-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7fbcf-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7fbcf-133">Request</span></span>
<span data-ttu-id="7fbcf-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7fbcf-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_plannerbucket"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/planner/buckets/{id}
If-Match: W/"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc="
```
##### <a name="response"></a><span data-ttu-id="7fbcf-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7fbcf-135">Response</span></span>
<span data-ttu-id="7fbcf-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7fbcf-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Delete plannerBucket",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->