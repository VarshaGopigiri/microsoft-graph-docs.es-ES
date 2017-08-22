# <a name="assign-a-manager"></a><span data-ttu-id="bc6f9-101">Assign a manager</span><span class="sxs-lookup"><span data-stu-id="bc6f9-101">Assign a manager</span></span>

<span data-ttu-id="bc6f9-102">Use esta API para asignar un administrador de usuarios.</span><span class="sxs-lookup"><span data-stu-id="bc6f9-102">Use this API to assign a user's manager.</span></span>
> <span data-ttu-id="bc6f9-103">Nota: No puede asignar subordinados directos; en lugar de ello, use esta API.</span><span class="sxs-lookup"><span data-stu-id="bc6f9-103">Note: You cannot assign direct reports - instead use this API.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bc6f9-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bc6f9-104">Prerequisites</span></span>
<span data-ttu-id="bc6f9-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.ReadWrite.All* o *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="bc6f9-105">One of the following **scopes** is required to execute this API: *Directory.ReadWrite.All* or *Directory.AccessAsUser.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="bc6f9-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bc6f9-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PUT /users/{id}/manager/$ref
```
## <a name="request-headers"></a><span data-ttu-id="bc6f9-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bc6f9-107">Request headers</span></span>
| <span data-ttu-id="bc6f9-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="bc6f9-108">Name</span></span>       | <span data-ttu-id="bc6f9-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc6f9-109">Type</span></span> | <span data-ttu-id="bc6f9-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc6f9-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="bc6f9-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="bc6f9-111">Authorization</span></span>  | <span data-ttu-id="bc6f9-112">string</span><span class="sxs-lookup"><span data-stu-id="bc6f9-112">string</span></span>  | <span data-ttu-id="bc6f9-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bc6f9-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="bc6f9-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bc6f9-115">Request body</span></span>
<span data-ttu-id="bc6f9-116">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryObject](../resources/directoryobject.md) o [user](../resources/user.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="bc6f9-116">In the request body, supply a JSON representation of [directoryObject](../resources/directoryobject.md) or [user](../resources/user.md) object to be added.</span></span>

## <a name="response"></a><span data-ttu-id="bc6f9-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bc6f9-117">Response</span></span>

<span data-ttu-id="bc6f9-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bc6f9-p102">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bc6f9-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bc6f9-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bc6f9-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bc6f9-121">Request</span></span>
<span data-ttu-id="bc6f9-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bc6f9-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_group"
}-->
```http
PUT https://graph.microsoft.com/v1.0/users/{id}/manager/$ref
Content-type: application/json
Content-length: xxx

{
  "@odata.id": "https://graph.microsoft.com/v1.0/users/{id}"
}
```
<span data-ttu-id="bc6f9-123">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="bc6f9-123">In the request body, supply a JSON representation of [user](../resources/user.md) object to be added.</span></span>
##### <a name="response"></a><span data-ttu-id="bc6f9-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bc6f9-124">Response</span></span>
<span data-ttu-id="bc6f9-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bc6f9-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Create member",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
