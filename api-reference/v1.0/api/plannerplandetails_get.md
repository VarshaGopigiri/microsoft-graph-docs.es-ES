# <a name="get-plannerplandetails"></a><span data-ttu-id="865cb-101">Obtener plannerPlanDetails</span><span class="sxs-lookup"><span data-stu-id="865cb-101">Get plannerPlanDetails</span></span>

<span data-ttu-id="865cb-102">Recuperar las propiedades y las relaciones del objeto **plannerplandetails**.</span><span class="sxs-lookup"><span data-stu-id="865cb-102">Retrieve the properties and relationships of **plannerplandetails** object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="865cb-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="865cb-103">Prerequisites</span></span>
<span data-ttu-id="865cb-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="865cb-104">The following **scopes** are required to execute this API:</span></span> 

<span data-ttu-id="865cb-105">*Group.Read.All*</span><span class="sxs-lookup"><span data-stu-id="865cb-105">*Group.Read.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="865cb-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="865cb-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /planner/plans/<id>/details
```

## <a name="request-headers"></a><span data-ttu-id="865cb-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="865cb-107">Request headers</span></span>
| <span data-ttu-id="865cb-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="865cb-108">Name</span></span>      |<span data-ttu-id="865cb-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="865cb-109">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="865cb-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="865cb-110">Authorization</span></span>  | <span data-ttu-id="865cb-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="865cb-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="865cb-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="865cb-113">Request body</span></span>
<span data-ttu-id="865cb-114">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="865cb-114">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="865cb-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="865cb-115">Response</span></span>

<span data-ttu-id="865cb-116">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerPlanDetails](../resources/plannerplandetails.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="865cb-116">If successful, this method returns a `200 OK` response code and [plannerPlanDetails](../resources/plannerplandetails.md) object in the response body.</span></span>

<span data-ttu-id="865cb-p102">Este método puede devolver cualquiera de los [códigos de estado HTTP](../../../concepts/errors.md). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="865cb-p102">This method can return any of the [HTTP status codes](../../../concepts/errors.md). The most common errors that apps should handle for this method are the 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="865cb-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="865cb-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="865cb-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="865cb-121">Request</span></span>
<span data-ttu-id="865cb-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="865cb-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_plannerplandetails"
}-->
```http
GET https://graph.microsoft.com/v1.0/planner/plans/xqQg5FS2LkCp935s-FIFm2QAFkHM/details
```
##### <a name="response"></a><span data-ttu-id="865cb-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="865cb-123">Response</span></span>
<span data-ttu-id="865cb-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="865cb-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerPlanDetails"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 373

{
  "sharedWith": {
    "aaa27244-1db4-476a-a5cb-004607466324" : true,
    "6463a5ce-2119-4198-9f2a-628761df4a62" : true
  },
  "categoryDescriptions": {
    "category1": "Indoors",
    "category2": "Outdoors",
    "category3": null,
    "category4": null,
    "category5": "Needs materials",
    "category6": "Needs equipment"
  },
  "id": "xqQg5FS2LkCp935s-FIFm2QAFkHM"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get plannerPlanDetails",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->