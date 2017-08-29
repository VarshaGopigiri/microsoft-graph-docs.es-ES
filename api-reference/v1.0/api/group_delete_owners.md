# <a name="remove-owner"></a><span data-ttu-id="094d9-101">Remove owner</span><span class="sxs-lookup"><span data-stu-id="094d9-101">Remove owner</span></span>

<span data-ttu-id="094d9-102">Use esta API para quitar un propietario de un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación owners.</span><span class="sxs-lookup"><span data-stu-id="094d9-102">Use this API to remove an owner from an Office 365 group, a security group or a mail-enabled security group through the owners navigation property.</span></span>

## <a name="permissions"></a><span data-ttu-id="094d9-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="094d9-103">Permissions</span></span>
<span data-ttu-id="094d9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="094d9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="094d9-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="094d9-106">Permission type</span></span>      | <span data-ttu-id="094d9-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="094d9-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="094d9-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="094d9-108">Delegated (work or school account)</span></span> | <span data-ttu-id="094d9-109">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="094d9-109">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="094d9-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="094d9-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="094d9-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="094d9-111">Not supported.</span></span>    |
|<span data-ttu-id="094d9-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="094d9-112">Application</span></span> | <span data-ttu-id="094d9-113">Group.ReadWrite.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="094d9-113">Group.ReadWrite.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="094d9-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="094d9-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/owners/{id}/$ref
```
## <a name="request-headers"></a><span data-ttu-id="094d9-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="094d9-115">Request headers</span></span>
| <span data-ttu-id="094d9-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="094d9-116">Name</span></span>       | <span data-ttu-id="094d9-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="094d9-117">Type</span></span> | <span data-ttu-id="094d9-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="094d9-118">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="094d9-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="094d9-119">Authorization</span></span>  | <span data-ttu-id="094d9-120">string</span><span class="sxs-lookup"><span data-stu-id="094d9-120">string</span></span>  | <span data-ttu-id="094d9-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="094d9-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="094d9-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="094d9-123">Request body</span></span>
<span data-ttu-id="094d9-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="094d9-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="094d9-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="094d9-125">Response</span></span>

<span data-ttu-id="094d9-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="094d9-p103">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="094d9-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="094d9-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="094d9-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="094d9-129">Request</span></span>
<span data-ttu-id="094d9-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="094d9-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_group"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groups/{id}/owners/{id}/$ref
```
<span data-ttu-id="094d9-131">En la solicitud, especifique la `id` del objeto de directorio que quiere quitar después del segmento de $ref.</span><span class="sxs-lookup"><span data-stu-id="094d9-131">In the request, specify the `id` of the directory object you want to remove after the $ref segment.</span></span>

##### <a name="response"></a><span data-ttu-id="094d9-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="094d9-132">Response</span></span>
<span data-ttu-id="094d9-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="094d9-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
