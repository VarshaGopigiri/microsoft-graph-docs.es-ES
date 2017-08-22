# <a name="list-plans"></a><span data-ttu-id="17314-101">Enumerar planes</span><span class="sxs-lookup"><span data-stu-id="17314-101">List plans</span></span>

<span data-ttu-id="17314-102">Recuperar una lista de objetos **plannerplan** compartidos con un objeto [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="17314-102">Retrieve a list of **plannerplan** objects shared with a [user](../resources/user.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="17314-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="17314-103">Prerequisites</span></span>
<span data-ttu-id="17314-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="17314-104">The following **scopes** are required to execute this API:</span></span> 

<span data-ttu-id="17314-105">*Group.Read.All*</span><span class="sxs-lookup"><span data-stu-id="17314-105">*Group.Read.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="17314-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="17314-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/planner/plans
GET /users/<id>/planner/plans
GET /drive/root/createdByUser/planner/plans
```

## <a name="request-headers"></a><span data-ttu-id="17314-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="17314-107">Request headers</span></span>
| <span data-ttu-id="17314-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="17314-108">Name</span></span>      |<span data-ttu-id="17314-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="17314-109">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="17314-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="17314-110">Authorization</span></span>  | <span data-ttu-id="17314-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="17314-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="17314-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="17314-113">Request body</span></span>
<span data-ttu-id="17314-114">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="17314-114">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="17314-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="17314-115">Response</span></span>

<span data-ttu-id="17314-116">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [plannerPlan](../resources/plannerplan.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="17314-116">If successful, this method returns a `200 OK` response code and collection of [plannerPlan](../resources/plannerplan.md) objects in the response body.</span></span>

<span data-ttu-id="17314-p102">Este método puede devolver cualquiera de los [códigos de estado HTTP](../../../concepts/errors.md). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="17314-p102">This method can return any of the [HTTP status codes](../../../concepts/errors.md). The most common errors that apps should handle for this method are the 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="17314-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="17314-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="17314-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="17314-121">Request</span></span>
<span data-ttu-id="17314-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="17314-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_plans"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/planner/plans
```
##### <a name="response"></a><span data-ttu-id="17314-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="17314-123">Response</span></span>
<span data-ttu-id="17314-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="17314-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerPlan",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 438

{
  "value": [
    {
      "createdBy": {
        "application": {
          "id": "95e27074-6c4a-447a-aa24-9d718a0b86fa"
        },
        "user": {
          "id": "ebf3b108-5234-4e22-b93d-656d7dae5874"
        }
      },
      "createdDateTime": "2015-03-30T18:36:49.2407981Z",
      "owner": "ebf3b108-5234-4e22-b93d-656d7dae5874",
      "title": "title-value",
      "id": "xqQg5FS2LkCp935s-FIFm2QAFkHM"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List plans",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->