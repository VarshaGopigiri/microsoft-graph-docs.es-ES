# <a name="get-plannertask"></a><span data-ttu-id="a2909-101">Obtener plannerTask</span><span class="sxs-lookup"><span data-stu-id="a2909-101">Get plannerTask</span></span>

<span data-ttu-id="a2909-102">Recuperar las propiedades y las relaciones del objeto **plannertask**.</span><span class="sxs-lookup"><span data-stu-id="a2909-102">Retrieve the properties and relationships of **plannertask** object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a2909-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a2909-103">Prerequisites</span></span>
<span data-ttu-id="a2909-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="a2909-104">The following **scopes** are required to execute this API:</span></span> 

<span data-ttu-id="a2909-105">*Group.Read.All*</span><span class="sxs-lookup"><span data-stu-id="a2909-105">*Group.Read.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="a2909-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a2909-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /planner/tasks/<id>
```

## <a name="request-headers"></a><span data-ttu-id="a2909-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a2909-107">Request headers</span></span>
| <span data-ttu-id="a2909-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="a2909-108">Name</span></span>      |<span data-ttu-id="a2909-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2909-109">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="a2909-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="a2909-110">Authorization</span></span>  | <span data-ttu-id="a2909-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a2909-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a2909-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a2909-113">Request body</span></span>
<span data-ttu-id="a2909-114">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a2909-114">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a2909-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2909-115">Response</span></span>

<span data-ttu-id="a2909-116">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerTask](../resources/plannertask.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2909-116">If successful, this method returns a `200 OK` response code and [plannerTask](../resources/plannertask.md) object in the response body.</span></span>

<span data-ttu-id="a2909-p102">Este método puede devolver cualquiera de los [códigos de estado HTTP](../../../concepts/errors.md). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="a2909-p102">This method can return any of the [HTTP status codes](../../../concepts/errors.md). The most common errors that apps should handle for this method are the 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="a2909-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a2909-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a2909-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a2909-121">Request</span></span>
<span data-ttu-id="a2909-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a2909-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_plannertask"
}-->
```http
GET https://graph.microsoft.com/v1.0/planner/tasks/01gzSlKkIUSUl6DF_EilrmQAKDhh
```
##### <a name="response"></a><span data-ttu-id="a2909-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2909-123">Response</span></span>
<span data-ttu-id="a2909-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a2909-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerTask"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 707

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
      "@odata.type": "#microsoft.graph.plannerAssignment",
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
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get plannerTask",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->