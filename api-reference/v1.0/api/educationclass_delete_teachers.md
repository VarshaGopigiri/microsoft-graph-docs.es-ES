# <a name="remove-teacher"></a><span data-ttu-id="ff34b-101">Quitar profesor</span><span class="sxs-lookup"><span data-stu-id="ff34b-101">Remove teacher</span></span>

<span data-ttu-id="ff34b-102">Quite un profesor de una clase.</span><span class="sxs-lookup"><span data-stu-id="ff34b-102">Remove a teacher from a class.</span></span>

## <a name="permissions"></a><span data-ttu-id="ff34b-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="ff34b-103">Permissions</span></span>
<span data-ttu-id="ff34b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ff34b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ff34b-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ff34b-106">Permission type</span></span>      | <span data-ttu-id="ff34b-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ff34b-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ff34b-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ff34b-108">Delegated (work or school account)</span></span> |  <span data-ttu-id="ff34b-109">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ff34b-109">Not supported.</span></span>  |
|<span data-ttu-id="ff34b-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ff34b-110">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="ff34b-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ff34b-111">Not supported.</span></span>  |
|<span data-ttu-id="ff34b-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ff34b-112">Application</span></span> | <span data-ttu-id="ff34b-113">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ff34b-113">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="ff34b-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ff34b-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/classes/{id}/teachers/{userId}/$ref
```
## <a name="request-headers"></a><span data-ttu-id="ff34b-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ff34b-115">Request headers</span></span>
| <span data-ttu-id="ff34b-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ff34b-116">Header</span></span>       | <span data-ttu-id="ff34b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ff34b-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ff34b-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="ff34b-118">Authorization</span></span>  | <span data-ttu-id="ff34b-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ff34b-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ff34b-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ff34b-121">Request body</span></span>
<span data-ttu-id="ff34b-122">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ff34b-122">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="ff34b-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ff34b-123">Response</span></span>
<span data-ttu-id="ff34b-124">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content` y un cuerpo de la respuesta vacío.</span><span class="sxs-lookup"><span data-stu-id="ff34b-124">If successful, this method returns a `204 No Content` response code and an empty response body.</span></span>

## <a name="example"></a><span data-ttu-id="ff34b-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ff34b-125">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ff34b-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ff34b-126">Request</span></span>
<span data-ttu-id="ff34b-127">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ff34b-127">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationclass_from_educationschool"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/education/classes/{class-id}/teachers/{teacher-id}
```

##### <a name="response"></a><span data-ttu-id="ff34b-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ff34b-128">Response</span></span>
<span data-ttu-id="ff34b-129">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ff34b-129">The following is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationClass"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create educationClass",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
