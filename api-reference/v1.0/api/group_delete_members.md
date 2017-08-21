# <a name="remove-member"></a><span data-ttu-id="aa3bc-101">Quitar miembro</span><span class="sxs-lookup"><span data-stu-id="aa3bc-101">Remove member</span></span>

<span data-ttu-id="aa3bc-p101">Use esta API para quitar un miembro de un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación **members**. Puede quitar usuarios u otros grupos.</span><span class="sxs-lookup"><span data-stu-id="aa3bc-p101">Use this API to remove a member from an Office 365 group, a security group or a mail-enabled security group through the **members** navigation property. You can remove users or other groups.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="aa3bc-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="aa3bc-104">Prerequisites</span></span>
<span data-ttu-id="aa3bc-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.ReadWrite.All*, *Directory.ReadWrite.All* o *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="aa3bc-105">One of the following **scopes** is required to execute this API: *Group.ReadWrite.All* or *Directory.ReadWrite.All* or *Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="aa3bc-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="aa3bc-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/members/{id}/$ref
```
## <a name="request-headers"></a><span data-ttu-id="aa3bc-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="aa3bc-107">Request headers</span></span>
| <span data-ttu-id="aa3bc-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="aa3bc-108">Name</span></span>       | <span data-ttu-id="aa3bc-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa3bc-109">Type</span></span> | <span data-ttu-id="aa3bc-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa3bc-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="aa3bc-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="aa3bc-111">Authorization</span></span>  | <span data-ttu-id="aa3bc-112">string</span><span class="sxs-lookup"><span data-stu-id="aa3bc-112">string</span></span>  | <span data-ttu-id="aa3bc-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="aa3bc-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="aa3bc-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="aa3bc-115">Request body</span></span>
<span data-ttu-id="aa3bc-116">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="aa3bc-116">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="aa3bc-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aa3bc-117">Response</span></span>

<span data-ttu-id="aa3bc-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="aa3bc-p103">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="aa3bc-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="aa3bc-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="aa3bc-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="aa3bc-121">Request</span></span>
<span data-ttu-id="aa3bc-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="aa3bc-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_group"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groups/{id}/members/{id}/$ref
```
<span data-ttu-id="aa3bc-123">En la solicitud, especifique la `id` del objeto de directorio que quiere quitar después del segmento de $ref.</span><span class="sxs-lookup"><span data-stu-id="aa3bc-123">In the request, specify the `id` of the directory object you want to remove after the $ref segment.</span></span>

##### <a name="response"></a><span data-ttu-id="aa3bc-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aa3bc-124">Response</span></span>
<span data-ttu-id="aa3bc-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="aa3bc-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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