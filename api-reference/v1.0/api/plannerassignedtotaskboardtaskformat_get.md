# <a name="get-plannerassignedtotaskboardtaskformat"></a><span data-ttu-id="60b79-101">Obtener plannerAssignedToTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="60b79-101">Get plannerAssignedToTaskBoardTaskFormat</span></span>

<span data-ttu-id="60b79-102">Recuperar las propiedades y las relaciones del objeto **plannerAssignedToTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="60b79-102">Retrieve the properties and relationships of **plannerAssignedToTaskBoardTaskFormat** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="60b79-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="60b79-103">Permissions</span></span>
<span data-ttu-id="60b79-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="60b79-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="60b79-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="60b79-106">Permission type</span></span>      | <span data-ttu-id="60b79-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="60b79-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="60b79-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="60b79-108">Delegated (work or school account)</span></span> | <span data-ttu-id="60b79-109">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="60b79-109">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="60b79-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="60b79-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="60b79-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="60b79-111">Not supported.</span></span>    |
|<span data-ttu-id="60b79-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="60b79-112">Application</span></span> | <span data-ttu-id="60b79-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="60b79-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="60b79-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="60b79-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /planner/tasks/{id}/assignedToTaskBoardFormat
```
## <a name="request-headers"></a><span data-ttu-id="60b79-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="60b79-115">Request headers</span></span>
| <span data-ttu-id="60b79-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="60b79-116">Name</span></span>      |<span data-ttu-id="60b79-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="60b79-117">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="60b79-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="60b79-118">Authorization</span></span>  | <span data-ttu-id="60b79-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="60b79-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="60b79-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="60b79-121">Request body</span></span>
<span data-ttu-id="60b79-122">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="60b79-122">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="60b79-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="60b79-123">Response</span></span>

<span data-ttu-id="60b79-124">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerAssignedToTaskBoardTaskFormat](../resources/plannerassignedtotaskboardtaskformat.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="60b79-124">If successful, this method returns a `200 OK` response code and [plannerAssignedToTaskBoardTaskFormat](../resources/plannerassignedtotaskboardtaskformat.md) object in the response body.</span></span>

<span data-ttu-id="60b79-p103">Este método puede devolver cualquiera de los [códigos de estado HTTP](../../../concepts/errors.md). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="60b79-p103">This method can return any of the [HTTP status codes](../../../concepts/errors.md). The most common errors that apps should handle for this method are the 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="60b79-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="60b79-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="60b79-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="60b79-129">Request</span></span>
<span data-ttu-id="60b79-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="60b79-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_plannerassignedtotaskboardtaskformat"
}-->
```http
GET https://graph.microsoft.com/v1.0/planner/tasks/{task-id}/assignedToTaskBoardFormat
```
##### <a name="response"></a><span data-ttu-id="60b79-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="60b79-131">Response</span></span>
<span data-ttu-id="60b79-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="60b79-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerAssignedToTaskBoardTaskFormat"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 225

{
  "unassignedOrderHint": "RWk1",
  "orderHintsByAssignee": {
    "6463a5ce-2119-4198-9f2a-628761df4a62":"85752723360752+",
    "aaa27244-1db4-476a-a5cb-004607466324":"90057581;"
  },
  "id": "01gzSlKkIUSUl6DF_EilrmQAKDhh"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get plannerAssignedToTaskBoardTaskFormat",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->