# <a name="remove-acceptedsender"></a><span data-ttu-id="4eb54-101">Remove acceptedSender</span><span class="sxs-lookup"><span data-stu-id="4eb54-101">Remove acceptedSender</span></span>

<span data-ttu-id="4eb54-102">Quita un usuario o grupo de la lista de acceptedSenders.</span><span class="sxs-lookup"><span data-stu-id="4eb54-102">Remove a user or group from the acceptedSenders list.</span></span> 
## <a name="prerequisites"></a><span data-ttu-id="4eb54-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4eb54-103">Prerequisites</span></span>
<span data-ttu-id="4eb54-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="4eb54-104">One of the following **scopes** is required to execute this API: *Group.ReadWrite.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="4eb54-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4eb54-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/acceptedSenders/$ref?$id=<id>

```
## <a name="request-headers"></a><span data-ttu-id="4eb54-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4eb54-106">Request headers</span></span>
| <span data-ttu-id="4eb54-107">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4eb54-107">Header</span></span>       | <span data-ttu-id="4eb54-108">Valor</span><span class="sxs-lookup"><span data-stu-id="4eb54-108">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="4eb54-109">Authorization</span><span class="sxs-lookup"><span data-stu-id="4eb54-109">Authorization</span></span>  | <span data-ttu-id="4eb54-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4eb54-p101">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="4eb54-112">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4eb54-112">Request body</span></span>
<span data-ttu-id="4eb54-113">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4eb54-113">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4eb54-114">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4eb54-114">Response</span></span>

<span data-ttu-id="4eb54-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4eb54-p102">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4eb54-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4eb54-117">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4eb54-118">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4eb54-118">Request</span></span>
<span data-ttu-id="4eb54-119">Aquí tiene un par de ejemplos de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4eb54-119">Here are a couple of examples of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_group"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groups/{id}/acceptedSenders/$ref?$id="users/{id}"

DELETE https://graph.microsoft.com/v1.0/groups/{id}/acceptedSenders/$ref?$id="groups/{id}"
```

##### <a name="response"></a><span data-ttu-id="4eb54-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4eb54-120">Response</span></span>
<span data-ttu-id="4eb54-121">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4eb54-121">Here is an example of the response.</span></span> 
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
  "description": "Create acceptedSender",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->