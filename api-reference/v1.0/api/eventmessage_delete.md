# <a name="delete-eventmessage"></a><span data-ttu-id="8b48e-101">Delete eventMessage</span><span class="sxs-lookup"><span data-stu-id="8b48e-101">Delete eventMessage</span></span>

<span data-ttu-id="8b48e-102">Elimina el eventMessage.</span><span class="sxs-lookup"><span data-stu-id="8b48e-102">Delete eventMessage.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8b48e-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8b48e-103">Prerequisites</span></span>
<span data-ttu-id="8b48e-104">Se requieren los siguientes **ámbitos** para ejecutar esta API: _Mail.ReadWrite_</span><span class="sxs-lookup"><span data-stu-id="8b48e-104">The following **scopes** are required to execute this API: _Mail.ReadWrite_</span></span> 
## <a name="http-request"></a><span data-ttu-id="8b48e-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8b48e-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/messages/{id}
DELETE /users/{id | userPrincipalName}/messages/{id}

DELETE /me/mailFolders/{id}/messages/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="8b48e-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8b48e-106">Request headers</span></span>
| <span data-ttu-id="8b48e-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="8b48e-107">Name</span></span>       | <span data-ttu-id="8b48e-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="8b48e-108">Type</span></span> | <span data-ttu-id="8b48e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b48e-109">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="8b48e-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="8b48e-110">Authorization</span></span>  | <span data-ttu-id="8b48e-111">string</span><span class="sxs-lookup"><span data-stu-id="8b48e-111">string</span></span>  | <span data-ttu-id="8b48e-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8b48e-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="8b48e-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8b48e-114">Request body</span></span>
<span data-ttu-id="8b48e-115">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8b48e-115">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8b48e-116">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8b48e-116">Response</span></span>

<span data-ttu-id="8b48e-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8b48e-p102">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8b48e-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8b48e-119">Example</span></span>
##### <a name="request"></a><span data-ttu-id="8b48e-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8b48e-120">Request</span></span>
<span data-ttu-id="8b48e-121">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8b48e-121">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_eventmessage"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/messages/{id}
```
##### <a name="response"></a><span data-ttu-id="8b48e-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8b48e-122">Response</span></span>
<span data-ttu-id="8b48e-123">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8b48e-123">Here is an example of the response.</span></span> 
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
  "description": "Delete eventMessage",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->