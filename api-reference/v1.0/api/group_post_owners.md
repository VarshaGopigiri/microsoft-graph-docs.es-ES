# <a name="add-group-owner"></a><span data-ttu-id="235f5-101">Añadir propietario de grupo</span><span class="sxs-lookup"><span data-stu-id="235f5-101">Add group owner</span></span>
<span data-ttu-id="235f5-p101">Agrega un usuario a los propietarios del grupo. Los propietarios son un conjunto de usuarios no administradores que tienen permiso para modificar el objeto de grupo.</span><span class="sxs-lookup"><span data-stu-id="235f5-p101">Add a user to the group's owners. The owners are a set of non-admin users who are allowed to modify the group object.</span></span>

## <a name="permissions"></a><span data-ttu-id="235f5-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="235f5-104">Permissions</span></span>
<span data-ttu-id="235f5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="235f5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="235f5-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="235f5-107">Permission type</span></span>      | <span data-ttu-id="235f5-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="235f5-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="235f5-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="235f5-109">Delegated (work or school account)</span></span> | <span data-ttu-id="235f5-110">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="235f5-110">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="235f5-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="235f5-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="235f5-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="235f5-112">Not supported.</span></span>    |
|<span data-ttu-id="235f5-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="235f5-113">Application</span></span> | <span data-ttu-id="235f5-114">Group.ReadWrite.All y User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="235f5-114">Group.ReadWrite.All and User.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="235f5-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="235f5-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/owners/$ref
```
## <a name="request-headers"></a><span data-ttu-id="235f5-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="235f5-116">Request headers</span></span>
| <span data-ttu-id="235f5-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="235f5-117">Name</span></span>       | <span data-ttu-id="235f5-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="235f5-118">Type</span></span> | <span data-ttu-id="235f5-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="235f5-119">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="235f5-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="235f5-120">Authorization</span></span>  | <span data-ttu-id="235f5-121">cadena</span><span class="sxs-lookup"><span data-stu-id="235f5-121">string</span></span>  | <span data-ttu-id="235f5-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="235f5-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="235f5-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="235f5-124">Request body</span></span>
<span data-ttu-id="235f5-125">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="235f5-125">In the request body, supply a JSON representation of [user](../resources/user.md) object to be added.</span></span>

## <a name="response"></a><span data-ttu-id="235f5-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="235f5-126">Response</span></span>
<span data-ttu-id="235f5-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="235f5-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="235f5-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="235f5-129">Example</span></span>
#### <a name="request"></a><span data-ttu-id="235f5-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="235f5-130">Request</span></span>
<span data-ttu-id="235f5-131">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="235f5-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_group"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/owners/$ref
Content-type: application/json
Content-length: 30

{
  "@odata.id": "https://graph.microsoft.com/v1.0/users/{id}"
}
```
<span data-ttu-id="235f5-132">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="235f5-132">In the request body, supply a JSON representation of [user](../resources/user.md) object to be added.</span></span>

#### <a name="response"></a><span data-ttu-id="235f5-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="235f5-133">Response</span></span>
<span data-ttu-id="235f5-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="235f5-134">The following is an example of the response.</span></span>
><span data-ttu-id="235f5-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="235f5-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create owner",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
