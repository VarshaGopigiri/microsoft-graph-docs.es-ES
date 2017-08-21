# <a name="add-group-owner"></a><span data-ttu-id="314cd-101">Add group owner</span><span class="sxs-lookup"><span data-stu-id="314cd-101">Add group owner</span></span>
<span data-ttu-id="314cd-p101">Agrega un usuario a los propietarios del grupo. Los propietarios son un conjunto de usuarios no administradores que tienen permiso para modificar el objeto de grupo.</span><span class="sxs-lookup"><span data-stu-id="314cd-p101">Add a user to the group's owners. The owners are a set of non-admin users who are allowed to modify the group object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="314cd-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="314cd-104">Prerequisites</span></span>
<span data-ttu-id="314cd-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.ReadWrite.All*, *Directory.ReadWrite.All* o *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="314cd-105">One of the following **scopes** is required to execute this API: *Group.ReadWrite.All* or *Directory.ReadWrite.All* or *Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="314cd-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="314cd-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/owners/$ref
```
## <a name="request-headers"></a><span data-ttu-id="314cd-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="314cd-107">Request headers</span></span>
| <span data-ttu-id="314cd-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="314cd-108">Name</span></span>       | <span data-ttu-id="314cd-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="314cd-109">Type</span></span> | <span data-ttu-id="314cd-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="314cd-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="314cd-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="314cd-111">Authorization</span></span>  | <span data-ttu-id="314cd-112">string</span><span class="sxs-lookup"><span data-stu-id="314cd-112">string</span></span>  | <span data-ttu-id="314cd-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="314cd-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="314cd-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="314cd-115">Request body</span></span>
<span data-ttu-id="314cd-116">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="314cd-116">In the request body, supply a JSON representation of [user](../resources/user.md) object to be added.</span></span>

## <a name="response"></a><span data-ttu-id="314cd-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="314cd-117">Response</span></span>

<span data-ttu-id="314cd-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="314cd-p103">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="314cd-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="314cd-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="314cd-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="314cd-121">Request</span></span>
<span data-ttu-id="314cd-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="314cd-122">Here is an example of the request.</span></span>
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
<span data-ttu-id="314cd-123">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="314cd-123">In the request body, supply a JSON representation of [user](../resources/user.md) object to be added.</span></span>
##### <a name="response"></a><span data-ttu-id="314cd-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="314cd-124">Response</span></span>
<span data-ttu-id="314cd-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="314cd-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
