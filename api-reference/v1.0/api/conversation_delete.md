# <a name="delete-conversation"></a><span data-ttu-id="210dc-101">Eliminar conversation</span><span class="sxs-lookup"><span data-stu-id="210dc-101">Delete conversation</span></span>

<span data-ttu-id="210dc-102">Elimina la conversación.</span><span class="sxs-lookup"><span data-stu-id="210dc-102">Delete conversation.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="210dc-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="210dc-103">Prerequisites</span></span>
<span data-ttu-id="210dc-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="210dc-104">One of the following **scopes** is required to execute this API: *Group.ReadWrite.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="210dc-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="210dc-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/conversations/{id}
```
## <a name="request-headers"></a><span data-ttu-id="210dc-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="210dc-106">Request headers</span></span>
| <span data-ttu-id="210dc-107">Encabezado</span><span class="sxs-lookup"><span data-stu-id="210dc-107">Header</span></span>       | <span data-ttu-id="210dc-108">Valor</span><span class="sxs-lookup"><span data-stu-id="210dc-108">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="210dc-109">Authorization</span><span class="sxs-lookup"><span data-stu-id="210dc-109">Authorization</span></span>  | <span data-ttu-id="210dc-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="210dc-p101">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="210dc-112">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="210dc-112">Request body</span></span>
<span data-ttu-id="210dc-113">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="210dc-113">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="210dc-114">Respuesta</span><span class="sxs-lookup"><span data-stu-id="210dc-114">Response</span></span>

<span data-ttu-id="210dc-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="210dc-p102">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="210dc-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="210dc-117">Example</span></span>
##### <a name="request"></a><span data-ttu-id="210dc-118">Solicitud</span><span class="sxs-lookup"><span data-stu-id="210dc-118">Request</span></span>
<span data-ttu-id="210dc-119">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="210dc-119">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_conversation"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groups/{id}/conversations/{id}
```
##### <a name="response"></a><span data-ttu-id="210dc-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="210dc-120">Response</span></span>
<span data-ttu-id="210dc-121">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="210dc-121">Here is an example of the response.</span></span> 
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
  "description": "Delete conversation",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
