# <a name="delete-group"></a><span data-ttu-id="55335-101">Delete group</span><span class="sxs-lookup"><span data-stu-id="55335-101">Delete group</span></span>
<span data-ttu-id="55335-102">Elimina el grupo.</span><span class="sxs-lookup"><span data-stu-id="55335-102">Delete group.</span></span>

## <a name="permissions"></a><span data-ttu-id="55335-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="55335-103">Permissions</span></span>
<span data-ttu-id="55335-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="55335-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="55335-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="55335-106">Permission type</span></span>      | <span data-ttu-id="55335-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="55335-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="55335-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="55335-108">Delegated (work or school account)</span></span> | <span data-ttu-id="55335-109">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="55335-109">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="55335-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="55335-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="55335-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="55335-111">Not supported.</span></span>    |
|<span data-ttu-id="55335-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="55335-112">Application</span></span> | <span data-ttu-id="55335-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="55335-113">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="55335-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="55335-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}
```

## <a name="request-headers"></a><span data-ttu-id="55335-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="55335-115">Request headers</span></span>
| <span data-ttu-id="55335-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="55335-116">Name</span></span>       | <span data-ttu-id="55335-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="55335-117">Type</span></span> | <span data-ttu-id="55335-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="55335-118">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="55335-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="55335-119">Authorization</span></span>  | <span data-ttu-id="55335-120">string</span><span class="sxs-lookup"><span data-stu-id="55335-120">string</span></span>  | <span data-ttu-id="55335-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="55335-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="55335-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="55335-123">Request body</span></span>
<span data-ttu-id="55335-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="55335-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="55335-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="55335-125">Response</span></span>
<span data-ttu-id="55335-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="55335-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="55335-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="55335-128">Example</span></span>
#### <a name="request"></a><span data-ttu-id="55335-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="55335-129">Request</span></span>
<span data-ttu-id="55335-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="55335-130">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_group"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groups/{id}
```

#### <a name="response"></a><span data-ttu-id="55335-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="55335-131">Response</span></span>
<span data-ttu-id="55335-132">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="55335-132">The following is an example of the response.</span></span> 
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
  "description": "Delete group",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->