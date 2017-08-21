# <a name="message-replyall"></a><span data-ttu-id="eb1ad-101">message: replyAll</span><span class="sxs-lookup"><span data-stu-id="eb1ad-101">message: replyAll</span></span>

<span data-ttu-id="eb1ad-p101">Responde a todos los remitentes de un mensaje. El mensaje se guarda en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="eb1ad-p101">Reply to all recipients of a message. The message is then saved in the Sent Items folder.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="eb1ad-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="eb1ad-104">Prerequisites</span></span>
<span data-ttu-id="eb1ad-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Mail.Send*</span><span class="sxs-lookup"><span data-stu-id="eb1ad-105">One of the following **scopes** is required to execute this API: *Mail.Send*</span></span>
## <a name="http-request"></a><span data-ttu-id="eb1ad-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eb1ad-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/me/messages/{id}/replyAll
POST /users/{id | userPrincipalName}/messages/{id}/replyAll
POST /me/mailFolders/{id}/messages/{id}/replyAll
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/replyAll
```
## <a name="request-headers"></a><span data-ttu-id="eb1ad-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eb1ad-107">Request headers</span></span>
| <span data-ttu-id="eb1ad-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="eb1ad-108">Name</span></span>       | <span data-ttu-id="eb1ad-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb1ad-109">Type</span></span> | <span data-ttu-id="eb1ad-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb1ad-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="eb1ad-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="eb1ad-111">Authorization</span></span>  | <span data-ttu-id="eb1ad-112">string</span><span class="sxs-lookup"><span data-stu-id="eb1ad-112">string</span></span>  | <span data-ttu-id="eb1ad-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="eb1ad-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="eb1ad-115">Content-Type</span><span class="sxs-lookup"><span data-stu-id="eb1ad-115">Content-Type</span></span> | <span data-ttu-id="eb1ad-116">string</span><span class="sxs-lookup"><span data-stu-id="eb1ad-116">string</span></span>  | <span data-ttu-id="eb1ad-p103">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="eb1ad-p103">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="eb1ad-119">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eb1ad-119">Request body</span></span>
<span data-ttu-id="eb1ad-120">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="eb1ad-120">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="eb1ad-121">Parámetro</span><span class="sxs-lookup"><span data-stu-id="eb1ad-121">Parameter</span></span>    | <span data-ttu-id="eb1ad-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb1ad-122">Type</span></span>   |<span data-ttu-id="eb1ad-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb1ad-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="eb1ad-124">comment</span><span class="sxs-lookup"><span data-stu-id="eb1ad-124">comment</span></span>|<span data-ttu-id="eb1ad-125">String</span><span class="sxs-lookup"><span data-stu-id="eb1ad-125">String</span></span>|<span data-ttu-id="eb1ad-p104">Comentario que se va a incluir. Puede ser una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="eb1ad-p104">A comment to include. Can be an empty string.</span></span>|

## <a name="response"></a><span data-ttu-id="eb1ad-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb1ad-128">Response</span></span>

<span data-ttu-id="eb1ad-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `202, Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eb1ad-p105">If successful, this method returns `202, Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="eb1ad-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eb1ad-131">Example</span></span>
<span data-ttu-id="eb1ad-132">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="eb1ad-132">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="eb1ad-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eb1ad-133">Request</span></span>
<span data-ttu-id="eb1ad-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eb1ad-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_replyall"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/replyAll
Content-type: application/json
Content-length: 32

{
  "comment": "comment-value"
}
```


##### <a name="response"></a><span data-ttu-id="eb1ad-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb1ad-135">Response</span></span>
<span data-ttu-id="eb1ad-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eb1ad-136">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: replyAll",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
