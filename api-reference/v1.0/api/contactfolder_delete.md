# <a name="delete-contactfolder"></a><span data-ttu-id="2ff62-101">Eliminar contactFolder.</span><span class="sxs-lookup"><span data-stu-id="2ff62-101">Delete contactFolder</span></span>

<span data-ttu-id="2ff62-102">Elimina una contactFolder que no sea la predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2ff62-102">Delete contactFolder other than the default contactFolder.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2ff62-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2ff62-103">Prerequisites</span></span>
<span data-ttu-id="2ff62-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Contacts.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="2ff62-104">One of the following **scopes** is required to execute this API: *Contacts.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="2ff62-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2ff62-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/contactFolders/{id}
DELETE /users/{id | userPrincipalName}/contactFolders/{id}
```
## <a name="request-headers"></a><span data-ttu-id="2ff62-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2ff62-106">Request headers</span></span>
| <span data-ttu-id="2ff62-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="2ff62-107">Name</span></span>       | <span data-ttu-id="2ff62-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="2ff62-108">Type</span></span> | <span data-ttu-id="2ff62-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ff62-109">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="2ff62-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="2ff62-110">Authorization</span></span>  | <span data-ttu-id="2ff62-111">string</span><span class="sxs-lookup"><span data-stu-id="2ff62-111">string</span></span>  | <span data-ttu-id="2ff62-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2ff62-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="2ff62-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2ff62-114">Request body</span></span>
<span data-ttu-id="2ff62-115">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2ff62-115">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2ff62-116">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2ff62-116">Response</span></span>

<span data-ttu-id="2ff62-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ff62-p102">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2ff62-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2ff62-119">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2ff62-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2ff62-120">Request</span></span>
<span data-ttu-id="2ff62-121">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2ff62-121">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_contactfolder"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/contactFolders/{id}
```
##### <a name="response"></a><span data-ttu-id="2ff62-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2ff62-122">Response</span></span>
<span data-ttu-id="2ff62-123">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ff62-123">Here is an example of the response.</span></span> 
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
  "description": "Delete contactFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
