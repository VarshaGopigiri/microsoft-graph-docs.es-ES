# <a name="remove-member"></a><span data-ttu-id="fdc17-101">Quitar miembro</span><span class="sxs-lookup"><span data-stu-id="fdc17-101">Remove member</span></span>

<span data-ttu-id="fdc17-p101">Use esta API para quitar un miembro de un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación **members**. Puede quitar usuarios u otros grupos.</span><span class="sxs-lookup"><span data-stu-id="fdc17-p101">Use this API to remove a member from an Office 365 group, a security group or a mail-enabled security group through the **members** navigation property. You can remove users or other groups.</span></span>

## <a name="permissions"></a><span data-ttu-id="fdc17-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="fdc17-104">Permissions</span></span>
<span data-ttu-id="fdc17-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="fdc17-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="fdc17-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fdc17-107">Permission type</span></span>      | <span data-ttu-id="fdc17-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fdc17-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fdc17-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fdc17-109">Delegated (work or school account)</span></span> | <span data-ttu-id="fdc17-110">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="fdc17-110">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="fdc17-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fdc17-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fdc17-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fdc17-112">Not supported.</span></span>    |
|<span data-ttu-id="fdc17-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fdc17-113">Application</span></span> | <span data-ttu-id="fdc17-114">Group.ReadWrite.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fdc17-114">Group.ReadWrite.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="fdc17-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fdc17-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/members/{id}/$ref
```
## <a name="request-headers"></a><span data-ttu-id="fdc17-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fdc17-116">Request headers</span></span>
| <span data-ttu-id="fdc17-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="fdc17-117">Name</span></span>       | <span data-ttu-id="fdc17-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="fdc17-118">Type</span></span> | <span data-ttu-id="fdc17-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="fdc17-119">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="fdc17-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="fdc17-120">Authorization</span></span>  | <span data-ttu-id="fdc17-121">string</span><span class="sxs-lookup"><span data-stu-id="fdc17-121">string</span></span>  | <span data-ttu-id="fdc17-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fdc17-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="fdc17-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fdc17-124">Request body</span></span>
<span data-ttu-id="fdc17-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="fdc17-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="fdc17-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fdc17-126">Response</span></span>

<span data-ttu-id="fdc17-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fdc17-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fdc17-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fdc17-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="fdc17-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fdc17-130">Request</span></span>
<span data-ttu-id="fdc17-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fdc17-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_group"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groups/{id}/members/{id}/$ref
```
<span data-ttu-id="fdc17-132">En la solicitud, especifique la `id` del objeto de directorio que quiere quitar después del segmento de $ref.</span><span class="sxs-lookup"><span data-stu-id="fdc17-132">In the request, specify the `id` of the directory object you want to remove after the $ref segment.</span></span>

##### <a name="response"></a><span data-ttu-id="fdc17-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fdc17-133">Response</span></span>
<span data-ttu-id="fdc17-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fdc17-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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