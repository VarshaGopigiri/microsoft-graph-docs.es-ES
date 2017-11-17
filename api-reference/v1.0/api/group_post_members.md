# <a name="add-member"></a><span data-ttu-id="78df3-101">Agregar miembro</span><span class="sxs-lookup"><span data-stu-id="78df3-101">Add member</span></span>

<span data-ttu-id="78df3-p101">Use esta API para agregar un miembro a un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación **members**. Puede agregar usuarios u otros grupos. Importante: Solo puede agregar usuarios a grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="78df3-p101">Use this API to add a member to an Office 365 group, a security group or a mail-enabled security group through the **members** navigation property. You can add users or other groups. Important: You can add only users to Office 365 groups.</span></span>

## <a name="permissions"></a><span data-ttu-id="78df3-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="78df3-105">Permissions</span></span>
<span data-ttu-id="78df3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="78df3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="78df3-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="78df3-108">Permission type</span></span>      | <span data-ttu-id="78df3-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="78df3-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="78df3-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="78df3-110">Delegated (work or school account)</span></span> | <span data-ttu-id="78df3-111">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="78df3-111">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="78df3-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="78df3-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="78df3-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="78df3-113">Not supported.</span></span>    |
|<span data-ttu-id="78df3-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="78df3-114">Application</span></span> | <span data-ttu-id="78df3-115">Group.ReadWrite.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="78df3-115">Group.ReadWrite.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="78df3-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="78df3-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/members/$ref
```
## <a name="request-headers"></a><span data-ttu-id="78df3-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="78df3-117">Request headers</span></span>
| <span data-ttu-id="78df3-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="78df3-118">Name</span></span>       | <span data-ttu-id="78df3-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="78df3-119">Type</span></span> | <span data-ttu-id="78df3-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="78df3-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="78df3-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="78df3-121">Authorization</span></span>  | <span data-ttu-id="78df3-122">string</span><span class="sxs-lookup"><span data-stu-id="78df3-122">string</span></span>  | <span data-ttu-id="78df3-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="78df3-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="78df3-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="78df3-125">Request body</span></span>
<span data-ttu-id="78df3-126">En el cuerpo de la solicitud, proporcione una representación JSON de un objeto [directoryObject](../resources/directoryobject.md), [user](../resources/user.md) o [group](../resources/group.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="78df3-126">In the request body, supply a JSON representation of a [directoryObject](../resources/directoryobject.md), [user](../resources/user.md) or [group](../resources/group.md) object to be added.</span></span>

## <a name="response"></a><span data-ttu-id="78df3-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="78df3-127">Response</span></span>

<span data-ttu-id="78df3-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="78df3-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="78df3-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="78df3-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="78df3-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="78df3-131">Request</span></span>
<span data-ttu-id="78df3-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="78df3-132">Here is an example of the request.</span></span>
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
<span data-ttu-id="78df3-133">En el cuerpo de la solicitud, proporcione una representación JSON del `id` de un objeto [directoryObject](../resources/directoryobject.md), [user](../resources/user.md) o [group](../resources/group.md) que quiera agregar.</span><span class="sxs-lookup"><span data-stu-id="78df3-133">In the request body, supply a JSON representation of the `id` of the [directoryObject](../resources/directoryobject.md), [user](../resources/user.md) or [group](../resources/group.md) object you want to add.</span></span>
##### <a name="response"></a><span data-ttu-id="78df3-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="78df3-134">Response</span></span>
<span data-ttu-id="78df3-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="78df3-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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