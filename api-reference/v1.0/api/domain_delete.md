# <a name="delete-domain"></a><span data-ttu-id="5870a-101">Eliminar dominio</span><span class="sxs-lookup"><span data-stu-id="5870a-101">Delete domain</span></span>

<span data-ttu-id="5870a-102">Elimina un dominio de un inquilino.</span><span class="sxs-lookup"><span data-stu-id="5870a-102">Deletes a domain from a tenant.</span></span>

> <span data-ttu-id="5870a-103">**Importante:**</span><span class="sxs-lookup"><span data-stu-id="5870a-103">**Important:**</span></span>
> - <span data-ttu-id="5870a-104">Los dominios eliminados no son recuperables.</span><span class="sxs-lookup"><span data-stu-id="5870a-104">Deleted domains are not recoverable.</span></span><br />
> - <span data-ttu-id="5870a-p101">Los intentos de eliminar el dominio fallarán si hay recursos u objetos que aún dependen de este. Encontrará todos los recursos dependientes mediante el uso de la API [Enumerar domainNameReferences](domain_list_domainnamereferences.md).</span><span class="sxs-lookup"><span data-stu-id="5870a-p101">Attempts to delete will fail if there are any resources or objects still dependent on the domain. You can find all dependent resources by using the [List domainNameReferences](domain_list_domainnamereferences.md) API.</span></span>

## <a name="permissions"></a><span data-ttu-id="5870a-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="5870a-107">Permissions</span></span>

<span data-ttu-id="5870a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="5870a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="5870a-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5870a-110">Permission type</span></span>      | <span data-ttu-id="5870a-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5870a-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5870a-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5870a-112">Delegated (work or school account)</span></span> | <span data-ttu-id="5870a-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="5870a-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="5870a-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5870a-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5870a-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5870a-115">Not supported.</span></span>    |
|<span data-ttu-id="5870a-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5870a-116">Application</span></span> | <span data-ttu-id="5870a-117">Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5870a-117">Domain.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="5870a-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5870a-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /domains/{id}
```

> <span data-ttu-id="5870a-119">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="5870a-119">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="request-headers"></a><span data-ttu-id="5870a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5870a-120">Request headers</span></span>

| <span data-ttu-id="5870a-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="5870a-121">Name</span></span>       | <span data-ttu-id="5870a-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="5870a-122">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="5870a-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="5870a-123">Authorization</span></span>  | <span data-ttu-id="5870a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5870a-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="5870a-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="5870a-126">Content-Type</span></span>  | <span data-ttu-id="5870a-127">application/json</span><span class="sxs-lookup"><span data-stu-id="5870a-127">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="5870a-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5870a-128">Request body</span></span>

<span data-ttu-id="5870a-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5870a-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5870a-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5870a-130">Response</span></span>

<span data-ttu-id="5870a-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve un cuerpo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="5870a-p104">If successful, this method returns `204 No Content` response code. It does not return a response body.</span></span>

## <a name="example"></a><span data-ttu-id="5870a-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5870a-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="5870a-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5870a-134">Request</span></span>

<!-- {
  "blockType": "request",
  "sampleKeys": ["contoso.com"],
  "name": "delete_domain"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/domains/contoso.com
```

##### <a name="response"></a><span data-ttu-id="5870a-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5870a-135">Response</span></span>

<span data-ttu-id="5870a-p105">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5870a-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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