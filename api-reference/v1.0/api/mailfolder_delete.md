# <a name="delete-mailfolder"></a><span data-ttu-id="50065-101">Delete mailFolder</span><span class="sxs-lookup"><span data-stu-id="50065-101">Delete mailFolder</span></span>

<span data-ttu-id="50065-102">Elimina el objeto mailfolder.</span><span class="sxs-lookup"><span data-stu-id="50065-102">Delete mailFolder.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="50065-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="50065-103">Prerequisites</span></span>
<span data-ttu-id="50065-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Mail.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="50065-104">One of the following **scopes** is required to execute this API: *Mail.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="50065-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="50065-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/mailFolders/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}
```
## <a name="request-headers"></a><span data-ttu-id="50065-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="50065-106">Request headers</span></span>
| <span data-ttu-id="50065-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="50065-107">Name</span></span>       | <span data-ttu-id="50065-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="50065-108">Type</span></span> | <span data-ttu-id="50065-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="50065-109">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="50065-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="50065-110">Authorization</span></span>  | <span data-ttu-id="50065-111">string</span><span class="sxs-lookup"><span data-stu-id="50065-111">string</span></span>  | <span data-ttu-id="50065-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="50065-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="50065-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="50065-114">Request body</span></span>
<span data-ttu-id="50065-115">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="50065-115">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="50065-116">Respuesta</span><span class="sxs-lookup"><span data-stu-id="50065-116">Response</span></span>

<span data-ttu-id="50065-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="50065-p102">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="50065-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="50065-119">Example</span></span>
##### <a name="request"></a><span data-ttu-id="50065-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="50065-120">Request</span></span>
<span data-ttu-id="50065-121">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="50065-121">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_mailfolder"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/mailFolders/{id}
```
##### <a name="response"></a><span data-ttu-id="50065-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="50065-122">Response</span></span>
<span data-ttu-id="50065-123">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="50065-123">Here is an example of the response.</span></span> 
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
  "description": "Delete mailFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->