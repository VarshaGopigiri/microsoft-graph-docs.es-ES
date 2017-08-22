# <a name="create-plannerbucket"></a><span data-ttu-id="19d52-101">Crear plannerBucket</span><span class="sxs-lookup"><span data-stu-id="19d52-101">Create plannerBucket</span></span>

<span data-ttu-id="19d52-102">Use esta API para crear un nuevo **plannerBucket**.</span><span class="sxs-lookup"><span data-stu-id="19d52-102">Use this API to create a new **plannerBucket**.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="19d52-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="19d52-103">Prerequisites</span></span>
<span data-ttu-id="19d52-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="19d52-104">The following **scopes** are required to execute this API:</span></span> 

<span data-ttu-id="19d52-105">*Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="19d52-105">*Group.ReadWrite.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="19d52-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="19d52-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /planner/buckets

```
## <a name="request-headers"></a><span data-ttu-id="19d52-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="19d52-107">Request headers</span></span>
| <span data-ttu-id="19d52-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="19d52-108">Name</span></span>       | <span data-ttu-id="19d52-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="19d52-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="19d52-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="19d52-110">Authorization</span></span>  | <span data-ttu-id="19d52-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="19d52-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="19d52-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="19d52-113">Request body</span></span>
<span data-ttu-id="19d52-114">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [plannerBucket](../resources/plannerbucket.md).</span><span class="sxs-lookup"><span data-stu-id="19d52-114">In the request body, supply a JSON representation of [plannerBucket](../resources/plannerbucket.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="19d52-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="19d52-115">Response</span></span>

<span data-ttu-id="19d52-116">Si se ejecuta correctamente, este método devuelve un código de respuesta `201, Created` y el objeto [plannerBucket](../resources/plannerbucket.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="19d52-116">If successful, this method returns `201, Created` response code and [plannerBucket](../resources/plannerbucket.md) object in the response body.</span></span>

<span data-ttu-id="19d52-p102">Este método puede devolver cualquiera de los [códigos de estado HTTP](../../../concepts/errors.md). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="19d52-p102">This method can return any of the [HTTP status codes](../../../concepts/errors.md). The most common errors that apps should handle for this method are the 400, 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="19d52-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="19d52-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="19d52-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="19d52-121">Request</span></span>
<span data-ttu-id="19d52-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="19d52-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_plannerbucket_from_planner"
}-->
```http
POST https://graph.microsoft.com/v1.0/planner/buckets
Content-type: application/json
Content-length: 92

{
  "name": "Advertising",
  "planId": "xqQg5FS2LkCp935s-FIFm2QAFkHM",
  "orderHint": " !"
}
```
<span data-ttu-id="19d52-123">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [plannerBucket](../resources/plannerbucket.md).</span><span class="sxs-lookup"><span data-stu-id="19d52-123">In the request body, supply a JSON representation of [plannerBucket](../resources/plannerbucket.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="19d52-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="19d52-124">Response</span></span>
<span data-ttu-id="19d52-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="19d52-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerBucket"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 145

{
  "name": "Advertising",
  "planId": "xqQg5FS2LkCp935s-FIFm2QAFkHM",
  "orderHint": "85752723360752+",
  "id": "hsOf2dhOJkqyYYZEtdzDe2QAIUCR"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create plannerBucket",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->