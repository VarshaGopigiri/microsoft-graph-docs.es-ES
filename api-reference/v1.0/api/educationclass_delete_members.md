# <a name="remove-a-student"></a><span data-ttu-id="a1050-101">Quitar un alumno</span><span class="sxs-lookup"><span data-stu-id="a1050-101">Remove a student</span></span>

<span data-ttu-id="a1050-102">Quita un [educationUser](../resources/educationuser.md) de un [educationClass](../resources/educationclass.md)</span><span class="sxs-lookup"><span data-stu-id="a1050-102">Removes an [educationUser](../resources/educationuser.md) from an [educationClass](../resources/educationclass.md)</span></span>

><span data-ttu-id="a1050-103">**Nota:** Los profesores _y_ los alumnos se encuentran en la colección **members** de la clase.</span><span class="sxs-lookup"><span data-stu-id="a1050-103">**Note:** Teachers _and_ students are in the class **members** collection.</span></span> <span data-ttu-id="a1050-104">Antes de llamar a esta API, asegúrese de que el **educationUser** que quita no es un profesor.</span><span class="sxs-lookup"><span data-stu-id="a1050-104">Before calling this API, insure that the **educationUser** you are removing is not a teacher.</span></span>  <span data-ttu-id="a1050-105">Obtenga la lista de profesores llamando a [educationclass_list_teachers](educationclass_list_teachers.md) y comprobando que el identificador de usuario del usuario que se va a quitar no se encuentra en la lista de profesores devuelta.</span><span class="sxs-lookup"><span data-stu-id="a1050-105">Get the list of teachers by calling [educationclass_list_teachers](educationclass_list_teachers.md) and verifying the user Id of the user to be removed is not in the returned teacher list.</span></span>

## <a name="permissions"></a><span data-ttu-id="a1050-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="a1050-106">Permissions</span></span>
<span data-ttu-id="a1050-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a1050-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a1050-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a1050-109">Permission type</span></span>      | <span data-ttu-id="a1050-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a1050-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a1050-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a1050-111">Delegated (work or school account)</span></span> |  <span data-ttu-id="a1050-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a1050-112">Not supported.</span></span>  |
|<span data-ttu-id="a1050-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a1050-113">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="a1050-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a1050-114">Not supported.</span></span>  |
|<span data-ttu-id="a1050-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a1050-115">Application</span></span> | <span data-ttu-id="a1050-116">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a1050-116">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="a1050-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a1050-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/classes/{id}/members/{userId}/$ref
```
## <a name="request-headers"></a><span data-ttu-id="a1050-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a1050-118">Request headers</span></span>
| <span data-ttu-id="a1050-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1050-119">Header</span></span>       | <span data-ttu-id="a1050-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a1050-120">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="a1050-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="a1050-121">Authorization</span></span>  | <span data-ttu-id="a1050-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a1050-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="a1050-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a1050-124">Request body</span></span>
<span data-ttu-id="a1050-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a1050-125">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="a1050-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a1050-126">Response</span></span>
<span data-ttu-id="a1050-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content` y un cuerpo de la respuesta vacío.</span><span class="sxs-lookup"><span data-stu-id="a1050-127">If successful, this method returns a `204 No Content` response code and an event object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a1050-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a1050-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a1050-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a1050-129">Request</span></span>
<span data-ttu-id="a1050-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a1050-130">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationclass_from_educationschool"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/education/classes/11003/members/14008
```

##### <a name="response"></a><span data-ttu-id="a1050-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a1050-131">Response</span></span>
<span data-ttu-id="a1050-132">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a1050-132">The following is an example of the response.</span></span> 
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
