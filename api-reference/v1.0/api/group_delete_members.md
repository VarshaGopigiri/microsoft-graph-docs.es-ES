# <a name="remove-member"></a><span data-ttu-id="f2321-101">Quitar miembro</span><span class="sxs-lookup"><span data-stu-id="f2321-101">Remove member</span></span>
<span data-ttu-id="f2321-p101">Use esta API para quitar un miembro de un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación **members**. Puede quitar usuarios u otros grupos.</span><span class="sxs-lookup"><span data-stu-id="f2321-p101">Use this API to remove a member from an Office 365 group, a security group or a mail-enabled security group through the **members** navigation property. You can remove users or other groups.</span></span>

## <a name="permissions"></a><span data-ttu-id="f2321-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="f2321-104">Permissions</span></span>
<span data-ttu-id="f2321-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f2321-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f2321-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f2321-107">Permission type</span></span>      | <span data-ttu-id="f2321-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f2321-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f2321-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f2321-109">Delegated (work or school account)</span></span> | <span data-ttu-id="f2321-110">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="f2321-110">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="f2321-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f2321-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f2321-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f2321-112">Not supported.</span></span>    |
|<span data-ttu-id="f2321-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f2321-113">Application</span></span> | <span data-ttu-id="f2321-114">Group.ReadWrite.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f2321-114">Group.ReadWrite.All, Directory.ReadWrite.All</span></span>  |

## <a name="http-request"></a><span data-ttu-id="f2321-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f2321-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/members/{id}/$ref
```

## <a name="request-headers"></a><span data-ttu-id="f2321-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f2321-116">Request headers</span></span>
| <span data-ttu-id="f2321-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="f2321-117">Name</span></span>       | <span data-ttu-id="f2321-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="f2321-118">Type</span></span> | <span data-ttu-id="f2321-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="f2321-119">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="f2321-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="f2321-120">Authorization</span></span>  | <span data-ttu-id="f2321-121">string</span><span class="sxs-lookup"><span data-stu-id="f2321-121">string</span></span>  | <span data-ttu-id="f2321-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f2321-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f2321-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f2321-124">Request body</span></span>
<span data-ttu-id="f2321-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f2321-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f2321-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f2321-126">Response</span></span>
<span data-ttu-id="f2321-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f2321-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f2321-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f2321-129">Example</span></span>
#### <a name="request"></a><span data-ttu-id="f2321-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f2321-130">Request</span></span>
<span data-ttu-id="f2321-131">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f2321-131">The following is an example of making the request in ASP.NET that uses the TokenHelper file:</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_group"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groups/{id}/members/{id}/$ref
```
<span data-ttu-id="f2321-132">En la solicitud, especifique la `id` del objeto de directorio que quiere quitar después del segmento de $ref.</span><span class="sxs-lookup"><span data-stu-id="f2321-132">In the request, specify the `id` of the directory object you want to remove after the $ref segment.</span></span>

#### <a name="response"></a><span data-ttu-id="f2321-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f2321-133">Response</span></span>
<span data-ttu-id="f2321-134">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f2321-134">Here is an example of the response.</span></span>
><span data-ttu-id="f2321-135">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="f2321-135">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="f2321-136">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f2321-136">All the properties will be returned from an actual call.</span></span>
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