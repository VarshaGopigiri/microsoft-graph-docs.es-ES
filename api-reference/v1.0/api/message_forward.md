# <a name="message-forward"></a><span data-ttu-id="de7b6-101">message: forward</span><span class="sxs-lookup"><span data-stu-id="de7b6-101">message: forward</span></span>

<span data-ttu-id="de7b6-p101">Reenvía un mensaje. El mensaje se guarda en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="de7b6-p101">Forward a message. The message is saved in the Sent Items folder.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="de7b6-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="de7b6-104">Prerequisites</span></span>
<span data-ttu-id="de7b6-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Mail.Send*</span><span class="sxs-lookup"><span data-stu-id="de7b6-105">One of the following **scopes** is required to execute this API: *Mail.Send*</span></span>
## <a name="http-request"></a><span data-ttu-id="de7b6-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="de7b6-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/forward
POST /users/{id | userPrincipalName}/messages/{id}/forward
POST /me/mailFolders/{id}/messages/{id}/forward
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/forward
```
## <a name="request-headers"></a><span data-ttu-id="de7b6-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="de7b6-107">Request headers</span></span>
| <span data-ttu-id="de7b6-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="de7b6-108">Name</span></span>       | <span data-ttu-id="de7b6-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="de7b6-109">Type</span></span> | <span data-ttu-id="de7b6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="de7b6-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="de7b6-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="de7b6-111">Authorization</span></span>  | <span data-ttu-id="de7b6-112">string</span><span class="sxs-lookup"><span data-stu-id="de7b6-112">string</span></span>  | <span data-ttu-id="de7b6-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="de7b6-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="de7b6-115">Content-Type</span><span class="sxs-lookup"><span data-stu-id="de7b6-115">Content-Type</span></span> | <span data-ttu-id="de7b6-116">string</span><span class="sxs-lookup"><span data-stu-id="de7b6-116">string</span></span>  | <span data-ttu-id="de7b6-p103">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="de7b6-p103">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="de7b6-119">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="de7b6-119">Request body</span></span>
<span data-ttu-id="de7b6-120">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="de7b6-120">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="de7b6-121">Parámetro</span><span class="sxs-lookup"><span data-stu-id="de7b6-121">Parameter</span></span>    | <span data-ttu-id="de7b6-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="de7b6-122">Type</span></span>   |<span data-ttu-id="de7b6-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="de7b6-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="de7b6-124">comment</span><span class="sxs-lookup"><span data-stu-id="de7b6-124">comment</span></span>|<span data-ttu-id="de7b6-125">String</span><span class="sxs-lookup"><span data-stu-id="de7b6-125">String</span></span>|<span data-ttu-id="de7b6-p104">Comentario que se va a incluir. Puede ser una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="de7b6-p104">A comment to include. Can be an empty string.</span></span>|
|<span data-ttu-id="de7b6-128">toRecipients</span><span class="sxs-lookup"><span data-stu-id="de7b6-128">toRecipients</span></span>|<span data-ttu-id="de7b6-129">Colección [Recipient](../resources/recipient.md)</span><span class="sxs-lookup"><span data-stu-id="de7b6-129">[Recipient](../resources/recipient.md) collection</span></span>|<span data-ttu-id="de7b6-130">La lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="de7b6-130">The list of recipients.</span></span>|

## <a name="response"></a><span data-ttu-id="de7b6-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="de7b6-131">Response</span></span>

<span data-ttu-id="de7b6-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `202, Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="de7b6-p105">If successful, this method returns `202, Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="de7b6-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="de7b6-134">Example</span></span>
<span data-ttu-id="de7b6-135">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="de7b6-135">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="de7b6-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="de7b6-136">Request</span></span>
<span data-ttu-id="de7b6-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="de7b6-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_forward"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/forward
Content-type: application/json
Content-length: 166

{
  "comment": "comment-value",
  "toRecipients": [
    {
      "emailAddress": {
        "name": "name-value",
        "address": "address-value"
      }
    }
  ]
}
```

##### <a name="response"></a><span data-ttu-id="de7b6-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="de7b6-138">Response</span></span>
##### <a name="response"></a><span data-ttu-id="de7b6-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="de7b6-139">Response</span></span>
<span data-ttu-id="de7b6-140">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="de7b6-140">Here is an example of the response.</span></span>
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
  "description": "message: forward",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
