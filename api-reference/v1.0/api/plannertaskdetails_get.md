# <a name="get-plannertaskdetails"></a><span data-ttu-id="302d4-101">Get plannerTaskDetails</span><span class="sxs-lookup"><span data-stu-id="302d4-101">Get plannerTaskDetails</span></span>

<span data-ttu-id="302d4-102">Recuperar las propiedades y las relaciones del objeto **plannertaskdetails**.</span><span class="sxs-lookup"><span data-stu-id="302d4-102">Retrieve the properties and relationships of **plannertaskdetails** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="302d4-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="302d4-103">Permissions</span></span>
<span data-ttu-id="302d4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="302d4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="302d4-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="302d4-106">Permission type</span></span>      | <span data-ttu-id="302d4-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="302d4-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="302d4-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="302d4-108">Delegated (work or school account)</span></span> | <span data-ttu-id="302d4-109">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="302d4-109">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="302d4-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="302d4-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="302d4-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="302d4-111">Not supported.</span></span>    |
|<span data-ttu-id="302d4-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="302d4-112">Application</span></span> | <span data-ttu-id="302d4-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="302d4-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="302d4-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="302d4-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /planner/tasks/{id}/details
```

## <a name="request-headers"></a><span data-ttu-id="302d4-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="302d4-115">Request headers</span></span>
| <span data-ttu-id="302d4-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="302d4-116">Name</span></span>      |<span data-ttu-id="302d4-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="302d4-117">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="302d4-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="302d4-118">Authorization</span></span>  | <span data-ttu-id="302d4-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="302d4-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="302d4-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="302d4-121">Request body</span></span>
<span data-ttu-id="302d4-122">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="302d4-122">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="302d4-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="302d4-123">Response</span></span>

<span data-ttu-id="302d4-124">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerTaskDetails](../resources/plannertaskdetails.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="302d4-124">If successful, this method returns a `200 OK` response code and [plannerTaskDetails](../resources/plannertaskdetails.md) object in the response body.</span></span>

<span data-ttu-id="302d4-p103">Este método puede devolver cualquiera de los [códigos de estado HTTP](../../../concepts/errors.md). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="302d4-p103">This method can return any of the [HTTP status codes](../../../concepts/errors.md). The most common errors that apps should handle for this method are the 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="302d4-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="302d4-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="302d4-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="302d4-129">Request</span></span>
<span data-ttu-id="302d4-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="302d4-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_plannertaskdetails"
}-->
```http
GET https://graph.microsoft.com/v1.0/planner/tasks/{task-id}/details
```
##### <a name="response"></a><span data-ttu-id="302d4-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="302d4-131">Response</span></span>
<span data-ttu-id="302d4-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="302d4-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerTaskDetails"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 1036

{
  "description": "Task details properties:\nchecklist:Sub items\nreferences:Related links",
  "previewType": "automatic",
  "references": {
    "https%3A//developer%2Emicrosoft%2Ecom/en-us/graph/graph-explorer": {
      "@odata.type": "#microsoft.graph.plannerExternalReference",
      "alias": "Graph Explorer",
      "type": "Other",
      "previewPriority": "0009005706180391122",
      "lastModifiedBy": {
        "user": {
          "id": "fbab97d0-4932-4511-b675-204639209557"
        }
      },
      "lastModifiedDateTime": "2017-04-24T22:52:29.814Z"
    }
  },
  "checklist": {
    "d280ed1a-9f6b-4f9c-a962-fb4d00dc50ff": {
      "@odata.type": "#microsoft.graph.plannerChecklistItem",
      "isChecked": false,
      "title": "Try reading task details",
      "orderHint": "8587094707721254251P]",
      "lastModifiedBy": {
        "user": {
          "id": "e396de0e-4812-4fcb-9f9e-0358744df343"
        }
      },
      "lastModifiedDateTime": "2017-04-14T02:16:14.866Z"
    }
  },
  "id": "gcrYAaAkgU2EQUvpkNNXLGQAGTtu"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get plannerTaskDetails",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->