# <a name="list-tasks"></a><span data-ttu-id="799e7-101">Enumerar tareas</span><span class="sxs-lookup"><span data-stu-id="799e7-101">List tasks</span></span>

<span data-ttu-id="799e7-102">Recuperar una lista de objetos **plannerTask** asociados a un objeto [plannerBucket](../resources/plannerBucket.md).</span><span class="sxs-lookup"><span data-stu-id="799e7-102">Retrieve a list of **plannerTask** objects associated to a [plannerBucket](../resources/plannerBucket.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="799e7-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="799e7-103">Prerequisites</span></span>
<span data-ttu-id="799e7-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="799e7-104">The following **scopes** are required to execute this API:</span></span> 

<span data-ttu-id="799e7-105">*Group.Read.All*</span><span class="sxs-lookup"><span data-stu-id="799e7-105">*Group.Read.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="799e7-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="799e7-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /planner/buckets/<id>/tasks
```

## <a name="request-headers"></a><span data-ttu-id="799e7-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="799e7-107">Request headers</span></span>
| <span data-ttu-id="799e7-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="799e7-108">Name</span></span>      |<span data-ttu-id="799e7-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="799e7-109">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="799e7-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="799e7-110">Authorization</span></span>  | <span data-ttu-id="799e7-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="799e7-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="799e7-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="799e7-113">Request body</span></span>
<span data-ttu-id="799e7-114">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="799e7-114">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="799e7-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="799e7-115">Response</span></span>

<span data-ttu-id="799e7-116">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [plannerTask](../resources/plannertask.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="799e7-116">If successful, this method returns a `200 OK` response code and collection of [plannerTask](../resources/plannertask.md) objects in the response body.</span></span>

<span data-ttu-id="799e7-p102">Este método puede devolver cualquiera de los [códigos de estado HTTP](../../../concepts/errors.md). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="799e7-p102">This method can return any of the [HTTP status codes](../../../concepts/errors.md). The most common errors that apps should handle for this method are the 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="799e7-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="799e7-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="799e7-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="799e7-121">Request</span></span>
<span data-ttu-id="799e7-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="799e7-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_tasks"
}-->
```http
GET https://graph.microsoft.com/v1.0/planner/buckets/gcrYAaAkgU2EQUvpkNNXLGQAGTtu/tasks
```
##### <a name="response"></a><span data-ttu-id="799e7-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="799e7-123">Response</span></span>
<span data-ttu-id="799e7-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="799e7-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerTask",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 833

{
  "value": [
    {
      "createdBy": {
        "user": {
          "id": "6463a5ce-2119-4198-9f2a-628761df4a62"
        }
      },
      "planId": "xqQg5FS2LkCp935s-FIFm2QAFkHM",
      "bucketId": "gcrYAaAkgU2EQUvpkNNXLGQAGTtu",
      "title": "title-value",
      "orderHint": "9223370609546166567W",
      "assigneePriority": "90057581\"",
      "createdDateTime": "2015-03-25T18:36:49.2407981Z",
      "assignments": {
        "fbab97d0-4932-4511-b675-204639209557": {
          "@odata.type": "#microsoft.graph.plannerassignment",
          "assignedBy": {
            "user": {
              "id": "1e9955d2-6acd-45bf-86d3-b546fdc795eb"
            }
          },
          "assignedDateTime": "2015-03-25T18:38:21.956Z",
          "orderHint": "RWk1"
         }
      },
      "id":"01gzSlKkIUSUl6DF_EilrmQAKDhh"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List tasks",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->