# <a name="remove-rejectedsender"></a><span data-ttu-id="dd5d2-101">Remove rejectedSender</span><span class="sxs-lookup"><span data-stu-id="dd5d2-101">Remove rejectedSender</span></span>

<span data-ttu-id="dd5d2-102">Quita un usuario o grupo de la lista de rejectedSenders.</span><span class="sxs-lookup"><span data-stu-id="dd5d2-102">Remove a user or group from the rejectedSenders list.</span></span>
## <a name="permissions"></a><span data-ttu-id="dd5d2-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="dd5d2-103">Permissions</span></span>
<span data-ttu-id="dd5d2-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="dd5d2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="dd5d2-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dd5d2-106">Permission type</span></span>      | <span data-ttu-id="dd5d2-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dd5d2-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="dd5d2-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dd5d2-108">Delegated (work or school account)</span></span> | <span data-ttu-id="dd5d2-109">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dd5d2-109">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="dd5d2-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dd5d2-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dd5d2-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dd5d2-111">Not supported.</span></span>    |
|<span data-ttu-id="dd5d2-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dd5d2-112">Application</span></span> | <span data-ttu-id="dd5d2-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dd5d2-113">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="dd5d2-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dd5d2-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/rejectedSenders/$ref?$id=<id>

```
## <a name="request-headers"></a><span data-ttu-id="dd5d2-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dd5d2-115">Request headers</span></span>
| <span data-ttu-id="dd5d2-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd5d2-116">Header</span></span>       | <span data-ttu-id="dd5d2-117">Valor</span><span class="sxs-lookup"><span data-stu-id="dd5d2-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="dd5d2-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="dd5d2-118">Authorization</span></span>  | <span data-ttu-id="dd5d2-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dd5d2-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="dd5d2-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dd5d2-121">Request body</span></span>
<span data-ttu-id="dd5d2-122">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="dd5d2-122">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="dd5d2-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dd5d2-123">Response</span></span>

<span data-ttu-id="dd5d2-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dd5d2-p103">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="dd5d2-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dd5d2-126">Example</span></span>
##### <a name="request"></a><span data-ttu-id="dd5d2-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dd5d2-127">Request</span></span>
<span data-ttu-id="dd5d2-128">Aquí tiene un par de ejemplos de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dd5d2-128">Here are a couple of examples of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_group"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groups/{id}/rejectedSenders/$ref?$id="users/{id}"

DELETE https://graph.microsoft.com/v1.0/groups/{id}/rejectedSenders/$ref?$id="groups/{id}"
```

##### <a name="response"></a><span data-ttu-id="dd5d2-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dd5d2-129">Response</span></span>
<span data-ttu-id="dd5d2-130">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dd5d2-130">Here is an example of the response.</span></span> 
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
  "description": "Create rejectedSender",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->