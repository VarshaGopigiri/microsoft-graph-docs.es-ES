# <a name="add-educationuser-to-an-educationschool"></a><span data-ttu-id="0e2eb-101">Agregar educationUser a un educationSchool</span><span class="sxs-lookup"><span data-stu-id="0e2eb-101">Add educationUser to an educationSchool</span></span>

<span data-ttu-id="0e2eb-102">Agregue un usuario a un centro educativo.</span><span class="sxs-lookup"><span data-stu-id="0e2eb-102">Add a user to a school.</span></span>

## <a name="permissions"></a><span data-ttu-id="0e2eb-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="0e2eb-103">Permissions</span></span>
<span data-ttu-id="0e2eb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="0e2eb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="0e2eb-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0e2eb-106">Permission type</span></span>      | <span data-ttu-id="0e2eb-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0e2eb-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0e2eb-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0e2eb-108">Delegated (work or school account)</span></span> |  <span data-ttu-id="0e2eb-109">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0e2eb-109">Not supported.</span></span>  |
|<span data-ttu-id="0e2eb-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0e2eb-110">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="0e2eb-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0e2eb-111">Not supported.</span></span>  |
|<span data-ttu-id="0e2eb-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0e2eb-112">Application</span></span> | <span data-ttu-id="0e2eb-113">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0e2eb-113">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="0e2eb-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0e2eb-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/schools/{id}/users/$ref
```
## <a name="request-headers"></a><span data-ttu-id="0e2eb-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0e2eb-115">Request headers</span></span>
| <span data-ttu-id="0e2eb-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0e2eb-116">Header</span></span>       | <span data-ttu-id="0e2eb-117">Valor</span><span class="sxs-lookup"><span data-stu-id="0e2eb-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="0e2eb-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="0e2eb-118">Authorization</span></span>  | <span data-ttu-id="0e2eb-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0e2eb-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="0e2eb-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="0e2eb-121">Content-Type</span></span>  | <span data-ttu-id="0e2eb-122">application/json</span><span class="sxs-lookup"><span data-stu-id="0e2eb-122">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="0e2eb-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0e2eb-123">Request body</span></span>
<span data-ttu-id="0e2eb-124">En el cuerpo de la solicitud, especifique una representación JSON de un objeto [educationUser](../resources/educationuser.md).</span><span class="sxs-lookup"><span data-stu-id="0e2eb-124">In the request body, supply a JSON representation of an [educationUser](../resources/educationuser.md) object.</span></span>


## <a name="response"></a><span data-ttu-id="0e2eb-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e2eb-125">Response</span></span>
<span data-ttu-id="0e2eb-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content` y un objeto [educationClass](../resources/educationclass.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0e2eb-126">If successful, this method returns a `204 No Content` response code and an [educationClass](../resources/educationclass.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0e2eb-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0e2eb-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="0e2eb-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0e2eb-128">Request</span></span>
<span data-ttu-id="0e2eb-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0e2eb-129">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationuser_from_educationschool"
}-->
```http
POST https://graph.microsoft.com/v1.0/education/schools/{id}/users/$ref
Content-type: application/json
Content-length: 56

{
  "@odata.id":"https://graph.microsoft.com/v1.0/education/users/14008"
}
```

##### <a name="response"></a><span data-ttu-id="0e2eb-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e2eb-130">Response</span></span>
<span data-ttu-id="0e2eb-131">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0e2eb-131">The following is an example of the response.</span></span> 

<!-- Add the educationClass resource to the response. -->

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationUser"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create educationUser",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->