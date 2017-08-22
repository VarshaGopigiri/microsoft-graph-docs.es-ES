# <a name="delete-page"></a><span data-ttu-id="03896-101">Eliminar página</span><span class="sxs-lookup"><span data-stu-id="03896-101">Delete page</span></span>

<span data-ttu-id="03896-102">Elimine una página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="03896-102">Delete a OneNote page.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="03896-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="03896-103">Prerequisites</span></span>
<span data-ttu-id="03896-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="03896-104">One of the following **scopes** is required to execute this API:</span></span>   

<span data-ttu-id="03896-105">Notes.ReadWrite o Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="03896-105">Notes.ReadWrite, or Notes.ReadWrite.All</span></span> 

## <a name="http-request"></a><span data-ttu-id="03896-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="03896-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/onenote/pages/{id}
DELETE /users/{id | userPrincipalName}/onenote/pages/{id}
DELETE /groups/{id}/onenote/pages/{id}
DELETE /sites/{id}/onenote/pages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="03896-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="03896-107">Request headers</span></span>
| <span data-ttu-id="03896-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="03896-108">Name</span></span>       | <span data-ttu-id="03896-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="03896-109">Type</span></span> | <span data-ttu-id="03896-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="03896-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="03896-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="03896-111">Authorization</span></span>  | <span data-ttu-id="03896-112">string</span><span class="sxs-lookup"><span data-stu-id="03896-112">string</span></span>  | <span data-ttu-id="03896-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="03896-p101">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="03896-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03896-115">Response</span></span>

<span data-ttu-id="03896-p102">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="03896-p102">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="03896-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="03896-118">Example</span></span>
##### <a name="request"></a><span data-ttu-id="03896-119">Solicitud</span><span class="sxs-lookup"><span data-stu-id="03896-119">Request</span></span>
<span data-ttu-id="03896-120">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="03896-120">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_page"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/onenote/pages/{id}
```
##### <a name="response"></a><span data-ttu-id="03896-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03896-121">Response</span></span>
<span data-ttu-id="03896-122">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="03896-122">Here is an example of the response.</span></span>
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
  "description": "Delete page",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->