# <a name="delete-conversationthread"></a><span data-ttu-id="51024-101">Delete conversationThread</span><span class="sxs-lookup"><span data-stu-id="51024-101">Delete conversationThread</span></span>

<span data-ttu-id="51024-102">Elimina el objeto conversationThread.</span><span class="sxs-lookup"><span data-stu-id="51024-102">Delete conversationThread.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="51024-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="51024-103">Prerequisites</span></span>
<span data-ttu-id="51024-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="51024-104">One of the following **scopes** is required to execute this API: *Group.ReadWrite.All*</span></span>
 
## <a name="http-request"></a><span data-ttu-id="51024-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="51024-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/threads/{id}
DELETE /groups/{id}/conversations/{id}/threads/{id}

```
## <a name="request-headers"></a><span data-ttu-id="51024-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="51024-106">Request headers</span></span>
| <span data-ttu-id="51024-107">Encabezado</span><span class="sxs-lookup"><span data-stu-id="51024-107">Header</span></span>       | <span data-ttu-id="51024-108">Valor</span><span class="sxs-lookup"><span data-stu-id="51024-108">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="51024-109">Authorization</span><span class="sxs-lookup"><span data-stu-id="51024-109">Authorization</span></span>  | <span data-ttu-id="51024-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="51024-p101">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="51024-112">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="51024-112">Request body</span></span>
<span data-ttu-id="51024-113">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="51024-113">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="51024-114">Respuesta</span><span class="sxs-lookup"><span data-stu-id="51024-114">Response</span></span>

<span data-ttu-id="51024-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="51024-p102">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="51024-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="51024-117">Example</span></span>
##### <a name="request"></a><span data-ttu-id="51024-118">Solicitud</span><span class="sxs-lookup"><span data-stu-id="51024-118">Request</span></span>
<span data-ttu-id="51024-119">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="51024-119">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_conversationthread"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groups/{id}/threads/{id}
```
##### <a name="response"></a><span data-ttu-id="51024-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="51024-120">Response</span></span>
<span data-ttu-id="51024-121">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="51024-121">Here is an example of the response.</span></span> 
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
  "description": "Delete conversationThread",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->