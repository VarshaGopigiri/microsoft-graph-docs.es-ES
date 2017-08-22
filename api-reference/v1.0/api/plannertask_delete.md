# <a name="delete-plannertask"></a><span data-ttu-id="fed19-101">Eliminar plannerTask</span><span class="sxs-lookup"><span data-stu-id="fed19-101">Delete plannerTask</span></span>

<span data-ttu-id="fed19-102">Eliminar **plannerTask**.</span><span class="sxs-lookup"><span data-stu-id="fed19-102">Delete **plannerTask**.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fed19-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fed19-103">Prerequisites</span></span>
<span data-ttu-id="fed19-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="fed19-104">The following **scopes** are required to execute this API:</span></span> 

<span data-ttu-id="fed19-105">*Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="fed19-105">*Group.ReadWrite.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="fed19-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fed19-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /planner/tasks/<id>
```
## <a name="request-headers"></a><span data-ttu-id="fed19-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fed19-107">Request headers</span></span>
| <span data-ttu-id="fed19-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="fed19-108">Name</span></span>       | <span data-ttu-id="fed19-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="fed19-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="fed19-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="fed19-110">Authorization</span></span>  | <span data-ttu-id="fed19-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fed19-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="fed19-113">If-Match</span><span class="sxs-lookup"><span data-stu-id="fed19-113">If-Match</span></span>  | <span data-ttu-id="fed19-p102">Último valor ETag conocido para que se elimine **plannerTask**. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fed19-p102">Last known ETag value for the **plannerTask** to be deleted. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="fed19-116">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="fed19-116">Request body</span></span>
<span data-ttu-id="fed19-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="fed19-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="fed19-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fed19-118">Response</span></span>

<span data-ttu-id="fed19-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fed19-p103">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

<span data-ttu-id="fed19-p104">Este método puede devolver cualquiera de los [códigos de estado HTTP](../../../concepts/errors.md). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="fed19-p104">This method can return any of the [HTTP status codes](../../../concepts/errors.md). The most common errors that apps should handle for this method are the 400, 403, 404, 409, and 412 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="fed19-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fed19-124">Example</span></span>
##### <a name="request"></a><span data-ttu-id="fed19-125">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fed19-125">Request</span></span>
<span data-ttu-id="fed19-126">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fed19-126">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_plannertask"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/planner/tasks/<id>
If-Match: W/"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc="
```
##### <a name="response"></a><span data-ttu-id="fed19-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fed19-127">Response</span></span>
<span data-ttu-id="fed19-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fed19-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Delete plannerTask",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->