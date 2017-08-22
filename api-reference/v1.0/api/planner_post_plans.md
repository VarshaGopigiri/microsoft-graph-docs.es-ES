# <a name="create-plannerplan"></a><span data-ttu-id="db201-101">Crear plannerPlan</span><span class="sxs-lookup"><span data-stu-id="db201-101">Create plannerPlan</span></span>

<span data-ttu-id="db201-102">Use esta API para crear un nuevo **plannerPlan**.</span><span class="sxs-lookup"><span data-stu-id="db201-102">Use this API to create a new **plannerPlan**.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="db201-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="db201-103">Prerequisites</span></span>
<span data-ttu-id="db201-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="db201-104">The following **scopes** are required to execute this API:</span></span> 

<span data-ttu-id="db201-105">*Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="db201-105">*Group.ReadWrite.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="db201-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="db201-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /planner/plans

```
## <a name="request-headers"></a><span data-ttu-id="db201-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="db201-107">Request headers</span></span>
| <span data-ttu-id="db201-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="db201-108">Name</span></span>       | <span data-ttu-id="db201-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="db201-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="db201-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="db201-110">Authorization</span></span>  | <span data-ttu-id="db201-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="db201-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="db201-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="db201-113">Request body</span></span>
<span data-ttu-id="db201-p102">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [plannerPlan](../resources/plannerplan.md). La propiedad de propietario **plannerPlan** se debe establecer en un identificador de un objeto [group](../resources/group.md).</span><span class="sxs-lookup"><span data-stu-id="db201-p102">In the request body, supply a JSON representation of [plannerPlan](../resources/plannerplan.md) object. The **plannerPlan** owner property must be set to an id of a [group](../resources/group.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="db201-116">Respuesta</span><span class="sxs-lookup"><span data-stu-id="db201-116">Response</span></span>

<span data-ttu-id="db201-117">Si se ejecuta correctamente, este método devuelve un código de respuesta `201, Created` y el objeto [plannerPlan](../resources/plannerplan.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="db201-117">If successful, this method returns `201, Created` response code and [plannerPlan](../resources/plannerplan.md) object in the response body.</span></span>

<span data-ttu-id="db201-p103">Este método puede devolver cualquiera de los [códigos de estado HTTP](../../../concepts/errors.md). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="db201-p103">This method can return any of the [HTTP status codes](../../../concepts/errors.md). The most common errors that apps should handle for this method are the 400, 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="db201-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="db201-121">Example</span></span>
##### <a name="request"></a><span data-ttu-id="db201-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="db201-122">Request</span></span>
<span data-ttu-id="db201-123">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="db201-123">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_plannerplan_from_planner"
}-->
```http
POST https://graph.microsoft.com/v1.0/planner/plans
Content-type: application/json
Content-length: 381

{
  "owner": "ebf3b108-5234-4e22-b93d-656d7dae5874",
  "title": "title-value"
}
```
<span data-ttu-id="db201-124">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [plannerPlan](../resources/plannerplan.md).</span><span class="sxs-lookup"><span data-stu-id="db201-124">In the request body, supply a JSON representation of [plannerPlan](../resources/plannerplan.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="db201-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="db201-125">Response</span></span>
<span data-ttu-id="db201-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="db201-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerPlan"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 357

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
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create plannerPlan",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->