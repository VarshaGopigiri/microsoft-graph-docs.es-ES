# <a name="delete-a-user"></a><span data-ttu-id="7193c-101">Eliminar un usuario</span><span class="sxs-lookup"><span data-stu-id="7193c-101">Delete a user</span></span>

<span data-ttu-id="7193c-102">Elimine usuario.</span><span class="sxs-lookup"><span data-stu-id="7193c-102">Delete user.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7193c-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7193c-103">Prerequisites</span></span>
<span data-ttu-id="7193c-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="7193c-104">One of the following **scopes** is required to execute this API: *Directory.AccessAsUser.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="7193c-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7193c-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /users/{id | userPrincipalName}
```

## <a name="request-headers"></a><span data-ttu-id="7193c-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7193c-106">Request headers</span></span>
| <span data-ttu-id="7193c-107">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7193c-107">Header</span></span>       | <span data-ttu-id="7193c-108">Valor</span><span class="sxs-lookup"><span data-stu-id="7193c-108">Value</span></span>|
|:-----------|:------|
| <span data-ttu-id="7193c-109">Authorization</span><span class="sxs-lookup"><span data-stu-id="7193c-109">Authorization</span></span>  | <span data-ttu-id="7193c-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7193c-p101">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="7193c-112">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7193c-112">Request body</span></span>
<span data-ttu-id="7193c-113">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7193c-113">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7193c-114">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7193c-114">Response</span></span>

<span data-ttu-id="7193c-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7193c-p102">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7193c-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7193c-117">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7193c-118">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7193c-118">Request</span></span>
<span data-ttu-id="7193c-119">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7193c-119">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_user"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/users/mba9a3254-9f18-4209-aeb3-9e42a35b5be4
```
##### <a name="response"></a><span data-ttu-id="7193c-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7193c-120">Response</span></span>
<span data-ttu-id="7193c-121">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7193c-121">Here is an example of the response.</span></span> 
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
  "description": "Delete user",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->