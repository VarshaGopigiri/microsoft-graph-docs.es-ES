# <a name="add-member"></a><span data-ttu-id="4df63-101">Add member</span><span class="sxs-lookup"><span data-stu-id="4df63-101">Add member</span></span>
<span data-ttu-id="4df63-102">Use esta API para agregar un miembro a un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación **members**.</span><span class="sxs-lookup"><span data-stu-id="4df63-102">Use this API to add a member to an Office 365 group, a security group or a mail-enabled security group through the **members** navigation property. You can add users or other groups. Important: You can add only users to Office 365 groups.</span></span>

<span data-ttu-id="4df63-103">Puede agregar usuarios u otros grupos.</span><span class="sxs-lookup"><span data-stu-id="4df63-103">You can add users or other groups.</span></span> <span data-ttu-id="4df63-104">Importante: Solo se pueden agregar usuarios a grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="4df63-104">Important: You can add only users to Office 365 groups.</span></span>

## <a name="permissions"></a><span data-ttu-id="4df63-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="4df63-105">Permissions</span></span>
<span data-ttu-id="4df63-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="4df63-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="4df63-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4df63-108">Permission type</span></span>      | <span data-ttu-id="4df63-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4df63-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4df63-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4df63-110">Delegated (work or school account)</span></span> | <span data-ttu-id="4df63-111">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="4df63-111">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="4df63-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4df63-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4df63-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4df63-113">Not supported.</span></span>    |
|<span data-ttu-id="4df63-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4df63-114">Application</span></span> | <span data-ttu-id="4df63-115">Group.ReadWrite.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4df63-115">Group.ReadWrite.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="4df63-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4df63-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/members/$ref
```

## <a name="request-headers"></a><span data-ttu-id="4df63-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4df63-117">Request headers</span></span>
| <span data-ttu-id="4df63-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="4df63-118">Name</span></span>       | <span data-ttu-id="4df63-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="4df63-119">Type</span></span> | <span data-ttu-id="4df63-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="4df63-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="4df63-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="4df63-121">Authorization</span></span>  | <span data-ttu-id="4df63-122">string</span><span class="sxs-lookup"><span data-stu-id="4df63-122">string</span></span>  | <span data-ttu-id="4df63-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4df63-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4df63-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4df63-125">Request body</span></span>
<span data-ttu-id="4df63-126">En el cuerpo de la solicitud, proporcione una representación JSON de un objeto [directoryObject](../resources/directoryobject.md), [user](../resources/user.md) o [group](../resources/group.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="4df63-126">In the request body, supply a JSON representation of a [directoryObject](../resources/directoryobject.md), [user](../resources/user.md) or [group](../resources/group.md) object to be added.</span></span>

## <a name="response"></a><span data-ttu-id="4df63-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4df63-127">Response</span></span>
<span data-ttu-id="4df63-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4df63-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4df63-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4df63-130">Example</span></span>
#### <a name="request"></a><span data-ttu-id="4df63-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4df63-131">Request</span></span>
<span data-ttu-id="4df63-132">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4df63-132">The following is an example of making the request in ASP.NET that uses the TokenHelper file:</span></span>
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
<span data-ttu-id="4df63-133">En el cuerpo de la solicitud, proporcione una representación JSON del `id` de un objeto [directoryObject](../resources/directoryobject.md), [user](../resources/user.md) o [group](../resources/group.md) que quiera agregar.</span><span class="sxs-lookup"><span data-stu-id="4df63-133">In the request body, supply a JSON representation of the `id` of the [directoryObject](../resources/directoryobject.md), [user](../resources/user.md) or [group](../resources/group.md) object you want to add.</span></span>

#### <a name="response"></a><span data-ttu-id="4df63-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4df63-134">Response</span></span>
<span data-ttu-id="4df63-135">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4df63-135">Here is an example of the response.</span></span>
><span data-ttu-id="4df63-136">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="4df63-136">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="4df63-137">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4df63-137">All the properties will be returned from an actual call.</span></span>
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