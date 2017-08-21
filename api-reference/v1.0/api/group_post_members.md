# <a name="add-member"></a><span data-ttu-id="029ad-101">Agregar miembro</span><span class="sxs-lookup"><span data-stu-id="029ad-101">Add member</span></span>

<span data-ttu-id="029ad-p101">Use esta API para agregar un miembro a un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación **members**. Puede agregar usuarios u otros grupos. Importante: Solo puede agregar usuarios a grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="029ad-p101">Use this API to add a member to an Office 365 group, a security group or a mail-enabled security group through the **members** navigation property. You can add users or other groups. Important: You can add only users to Office 365 groups.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="029ad-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="029ad-105">Prerequisites</span></span>
<span data-ttu-id="029ad-106">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.ReadWrite.All*, *Directory.ReadWrite.All* o *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="029ad-106">One of the following **scopes** is required to execute this API: *Group.ReadWrite.All* or *Directory.ReadWrite.All* or *Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="029ad-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="029ad-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/members/$ref
```
## <a name="request-headers"></a><span data-ttu-id="029ad-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="029ad-108">Request headers</span></span>
| <span data-ttu-id="029ad-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="029ad-109">Name</span></span>       | <span data-ttu-id="029ad-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="029ad-110">Type</span></span> | <span data-ttu-id="029ad-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="029ad-111">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="029ad-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="029ad-112">Authorization</span></span>  | <span data-ttu-id="029ad-113">string</span><span class="sxs-lookup"><span data-stu-id="029ad-113">string</span></span>  | <span data-ttu-id="029ad-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="029ad-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="029ad-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="029ad-116">Request body</span></span>
<span data-ttu-id="029ad-117">En el cuerpo de la solicitud, proporcione una representación JSON de un objeto [directoryObject](../resources/directoryobject.md), [user](../resources/user.md) o [group](../resources/group.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="029ad-117">In the request body, supply a JSON representation of a [directoryObject](../resources/directoryobject.md), [user](../resources/user.md) or [group](../resources/group.md) object to be added.</span></span>

## <a name="response"></a><span data-ttu-id="029ad-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="029ad-118">Response</span></span>

<span data-ttu-id="029ad-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="029ad-p103">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="029ad-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="029ad-121">Example</span></span>
##### <a name="request"></a><span data-ttu-id="029ad-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="029ad-122">Request</span></span>
<span data-ttu-id="029ad-123">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="029ad-123">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_group"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/members/$ref
Content-type: application/json
Content-length: 30

{
  "@odata.id": "https://graph.microsoft.com/v1.0/directoryObjects/{id}"
}
```
<span data-ttu-id="029ad-124">En el cuerpo de la solicitud, proporcione una representación JSON del `id` de un objeto [directoryObject](../resources/directoryobject.md), [user](../resources/user.md) o [group](../resources/group.md) que quiera agregar.</span><span class="sxs-lookup"><span data-stu-id="029ad-124">In the request body, supply a JSON representation of the `id` of the [directoryObject](../resources/directoryobject.md), [user](../resources/user.md) or [group](../resources/group.md) object you want to add.</span></span>
##### <a name="response"></a><span data-ttu-id="029ad-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="029ad-125">Response</span></span>
<span data-ttu-id="029ad-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="029ad-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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