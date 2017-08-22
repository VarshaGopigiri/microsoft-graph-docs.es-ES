# <a name="delete-photo"></a><span data-ttu-id="031c6-101">Delete photo</span><span class="sxs-lookup"><span data-stu-id="031c6-101">Delete photo</span></span>

<span data-ttu-id="031c6-102">Elimina una foto.</span><span class="sxs-lookup"><span data-stu-id="031c6-102">Delete a photo.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="031c6-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="031c6-103">Prerequisites</span></span>
<span data-ttu-id="031c6-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="031c6-104">One of the following **scopes** is required to execute this API:</span></span>

  * <span data-ttu-id="031c6-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="031c6-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="031c6-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="031c6-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /users/{id | userPrincipalName}/photo
DELETE /groups/{id}/photo
DELETE /drive/root/createdByUser/photo

```
## <a name="request-headers"></a><span data-ttu-id="031c6-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="031c6-107">Request headers</span></span>
| <span data-ttu-id="031c6-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="031c6-108">Name</span></span>       | <span data-ttu-id="031c6-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="031c6-109">Type</span></span> | <span data-ttu-id="031c6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="031c6-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="031c6-111">if-match</span><span class="sxs-lookup"><span data-stu-id="031c6-111">if-match</span></span>  | <span data-ttu-id="031c6-112">string</span><span class="sxs-lookup"><span data-stu-id="031c6-112">string</span></span>  | <span data-ttu-id="031c6-113">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide con la etiqueta actual del archivo, se devuelve una respuesta `412 Precondition Failed` y el elemento no se borrará.</span><span class="sxs-lookup"><span data-stu-id="031c6-113">If this request header is included and the eTag (or cTag) provided does not match the current tag on the item, a `412 Precondition Failed` response is returned and the item will not be deleted.</span></span>|
| <span data-ttu-id="031c6-114">Autorización</span><span class="sxs-lookup"><span data-stu-id="031c6-114">Authorization</span></span>  | <span data-ttu-id="031c6-115">string</span><span class="sxs-lookup"><span data-stu-id="031c6-115">string</span></span>  | <span data-ttu-id="031c6-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="031c6-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="031c6-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="031c6-118">Request body</span></span>
<span data-ttu-id="031c6-119">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="031c6-119">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="031c6-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="031c6-120">Response</span></span>

<span data-ttu-id="031c6-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="031c6-p102">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="031c6-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="031c6-123">Example</span></span>
##### <a name="request"></a><span data-ttu-id="031c6-124">Solicitud</span><span class="sxs-lookup"><span data-stu-id="031c6-124">Request</span></span>
<span data-ttu-id="031c6-125">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="031c6-125">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
"name": "delete_photo"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/users/{id|userPrincipalName}/photo
```
##### <a name="response"></a><span data-ttu-id="031c6-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="031c6-126">Response</span></span>
<span data-ttu-id="031c6-127">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="031c6-127">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete photo",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
