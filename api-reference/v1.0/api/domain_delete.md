# <a name="delete-domain"></a><span data-ttu-id="dce22-101">Eliminar dominio</span><span class="sxs-lookup"><span data-stu-id="dce22-101">Delete domain</span></span>

<span data-ttu-id="dce22-102">Elimina un dominio de un inquilino.</span><span class="sxs-lookup"><span data-stu-id="dce22-102">Deletes a domain from a tenant.</span></span>

> <span data-ttu-id="dce22-103">**Importante:**</span><span class="sxs-lookup"><span data-stu-id="dce22-103">**Important:**</span></span>
> - <span data-ttu-id="dce22-104">Los dominios eliminados no son recuperables.</span><span class="sxs-lookup"><span data-stu-id="dce22-104">Deleted domains are not recoverable.</span></span><br />
> - <span data-ttu-id="dce22-p101">Los intentos de eliminar el dominio fallarán si hay recursos u objetos que aún dependen de este. Encontrará todos los recursos dependientes mediante el uso de la API [Enumerar domainNameReferences](domain_list_domainnamereferences.md).</span><span class="sxs-lookup"><span data-stu-id="dce22-p101">Attempts to delete will fail if there are any resources or objects still dependent on the domain. You can find all dependent resources by using the [List domainNameReferences](domain_list_domainnamereferences.md) API.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="dce22-107">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="dce22-107">Prerequisites</span></span>

<span data-ttu-id="dce22-108">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Domain.ReadWrite.All* o *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="dce22-108">One of the following **scopes** is required to execute this API: *Domain.ReadWrite.All* or *Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="dce22-109">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dce22-109">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /domains/{id}
```

> <span data-ttu-id="dce22-110">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="dce22-110">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="request-headers"></a><span data-ttu-id="dce22-111">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dce22-111">Request headers</span></span>

| <span data-ttu-id="dce22-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="dce22-112">Name</span></span>       | <span data-ttu-id="dce22-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="dce22-113">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="dce22-114">Authorization</span><span class="sxs-lookup"><span data-stu-id="dce22-114">Authorization</span></span>  | <span data-ttu-id="dce22-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dce22-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="dce22-117">Content-Type</span><span class="sxs-lookup"><span data-stu-id="dce22-117">Content-Type</span></span>  | <span data-ttu-id="dce22-118">application/json</span><span class="sxs-lookup"><span data-stu-id="dce22-118">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="dce22-119">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dce22-119">Request body</span></span>

<span data-ttu-id="dce22-120">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="dce22-120">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="dce22-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dce22-121">Response</span></span>

<span data-ttu-id="dce22-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve un cuerpo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="dce22-p103">If successful, this method returns `204, No Content` response code. It does not return a response body.</span></span>

## <a name="example"></a><span data-ttu-id="dce22-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dce22-124">Example</span></span>
##### <a name="request"></a><span data-ttu-id="dce22-125">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dce22-125">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_domain"
}-->
```http
DELETE https://graph.microsoft.com/V1.0/domains/contoso.com
```

##### <a name="response"></a><span data-ttu-id="dce22-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dce22-126">Response</span></span>

<span data-ttu-id="dce22-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dce22-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete domain",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->