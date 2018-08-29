# <a name="remove-educationuser-from-an-educationschool"></a><span data-ttu-id="b4e7e-101">Quitar educationUser de un educationSchool</span><span class="sxs-lookup"><span data-stu-id="b4e7e-101">Remove educationUser from an educationSchool</span></span>

<span data-ttu-id="b4e7e-102">Elimine un usuario de un centro educativo.</span><span class="sxs-lookup"><span data-stu-id="b4e7e-102">Delete a user from a school.</span></span>

## <a name="permissions"></a><span data-ttu-id="b4e7e-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="b4e7e-103">Permissions</span></span>
<span data-ttu-id="b4e7e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b4e7e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b4e7e-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b4e7e-106">Permission type</span></span>      | <span data-ttu-id="b4e7e-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b4e7e-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b4e7e-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b4e7e-108">Delegated (work or school account)</span></span> |  <span data-ttu-id="b4e7e-109">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b4e7e-109">Not supported.</span></span>  |
|<span data-ttu-id="b4e7e-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b4e7e-110">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="b4e7e-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b4e7e-111">Not supported.</span></span>  |
|<span data-ttu-id="b4e7e-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b4e7e-112">Application</span></span> | <span data-ttu-id="b4e7e-113">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b4e7e-113">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="b4e7e-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b4e7e-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/schools/{id}/users/{userId}/$ref
```
## <a name="request-headers"></a><span data-ttu-id="b4e7e-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b4e7e-115">Request headers</span></span>
| <span data-ttu-id="b4e7e-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4e7e-116">Header</span></span>       | <span data-ttu-id="b4e7e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b4e7e-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="b4e7e-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="b4e7e-118">Authorization</span></span>  | <span data-ttu-id="b4e7e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b4e7e-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b4e7e-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b4e7e-121">Request body</span></span>
<span data-ttu-id="b4e7e-122">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b4e7e-122">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="b4e7e-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b4e7e-123">Response</span></span>
<span data-ttu-id="b4e7e-124">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content` y un cuerpo de la respuesta vacío.</span><span class="sxs-lookup"><span data-stu-id="b4e7e-124">If successful, this method returns a `204 No Content` response code and an empty response body.</span></span>

## <a name="example"></a><span data-ttu-id="b4e7e-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b4e7e-125">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b4e7e-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b4e7e-126">Request</span></span>
<span data-ttu-id="b4e7e-127">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b4e7e-127">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationclass_from_educationschool"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/education/schools/{school-id}/users/{user-id}
```

##### <a name="response"></a><span data-ttu-id="b4e7e-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b4e7e-128">Response</span></span>
<span data-ttu-id="b4e7e-129">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b4e7e-129">The following is an example of the response.</span></span> 
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