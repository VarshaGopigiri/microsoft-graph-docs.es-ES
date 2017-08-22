# <a name="list-buckets"></a><span data-ttu-id="4e45f-101">Enumerar depósitos</span><span class="sxs-lookup"><span data-stu-id="4e45f-101">List buckets</span></span>

<span data-ttu-id="4e45f-102">Recupere una lista de objetos **plannerbucket** contenidos en un objeto [plannerPlan](../resources/plannerplan.md).</span><span class="sxs-lookup"><span data-stu-id="4e45f-102">Retrieve a list of **plannerbucket** objects contained by a [plannerPlan](../resources/plannerplan.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4e45f-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4e45f-103">Prerequisites</span></span>
<span data-ttu-id="4e45f-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="4e45f-104">The following **scopes** are required to execute this API:</span></span> 

<span data-ttu-id="4e45f-105">*Group.Read.All*</span><span class="sxs-lookup"><span data-stu-id="4e45f-105">*Group.Read.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="4e45f-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4e45f-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /planner/plans/<id>/buckets
```

## <a name="request-headers"></a><span data-ttu-id="4e45f-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4e45f-107">Request headers</span></span>
| <span data-ttu-id="4e45f-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="4e45f-108">Name</span></span>      |<span data-ttu-id="4e45f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e45f-109">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="4e45f-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="4e45f-110">Authorization</span></span>  | <span data-ttu-id="4e45f-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4e45f-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4e45f-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4e45f-113">Request body</span></span>
<span data-ttu-id="4e45f-114">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4e45f-114">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4e45f-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4e45f-115">Response</span></span>

<span data-ttu-id="4e45f-116">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [plannerBucket](../resources/plannerbucket.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4e45f-116">If successful, this method returns a `200 OK` response code and collection of [plannerBucket](../resources/plannerbucket.md) objects in the response body.</span></span>

<span data-ttu-id="4e45f-p102">Este método puede devolver cualquiera de los [códigos de estado HTTP](../../../concepts/errors.md). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="4e45f-p102">This method can return any of the [HTTP status codes](../../../concepts/errors.md). The most common errors that apps should handle for this method are the 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions).</span></span>
## <a name="example"></a><span data-ttu-id="4e45f-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4e45f-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4e45f-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4e45f-121">Request</span></span>
<span data-ttu-id="4e45f-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4e45f-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_buckets"
}-->
```http
GET https://graph.microsoft.com/v1.0/planner/plans/2txjA-BMZEq-bKi6Wfj5aGQAB1OJ/buckets
```
##### <a name="response"></a><span data-ttu-id="4e45f-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4e45f-123">Response</span></span>
<span data-ttu-id="4e45f-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4e45f-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerBucket",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 251

{
  "value": [
    {
      "@odata.etag": "W/\"JzEtQnVja2V0QEBAQEBAQEBAQEBAQEBARCc=\"",
      "name": "To do",
      "planId": "2txjA-BMZEq-bKi6Wfj5aGQAB1OJ",
      "orderHint": "85752723360752+",
      "id": "hsOf2dhOJkqyYYZEtdzDe2QAIUCR"
    }
  ]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List buckets",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->