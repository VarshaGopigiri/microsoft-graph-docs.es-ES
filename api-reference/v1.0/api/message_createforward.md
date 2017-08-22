# <a name="message-createforward"></a><span data-ttu-id="745f6-101">message: createForward</span><span class="sxs-lookup"><span data-stu-id="745f6-101">message: createForward</span></span>

<span data-ttu-id="745f6-p101">Crea un borrador del mensaje que de reenvío. Después puede [update](../api/message_update.md) o [send](../api/message_send.md) el borrador.</span><span class="sxs-lookup"><span data-stu-id="745f6-p101">Create a draft of the Forward message. You can then [update](../api/message_update.md) or [send](../api/message_send.md) the draft.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="745f6-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="745f6-104">Prerequisites</span></span>
<span data-ttu-id="745f6-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Mail.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="745f6-105">One of the following **scopes** is required to execute this API: *Mail.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="745f6-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="745f6-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/createForward
POST /users/{id | userPrincipalName}/messages/{id}/createForward
POST /me/mailFolders/{id}/messages/{id}/createForward
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/createForward
```
## <a name="request-headers"></a><span data-ttu-id="745f6-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="745f6-107">Request headers</span></span>
| <span data-ttu-id="745f6-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="745f6-108">Name</span></span>       | <span data-ttu-id="745f6-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="745f6-109">Type</span></span> | <span data-ttu-id="745f6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="745f6-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="745f6-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="745f6-111">Authorization</span></span>  | <span data-ttu-id="745f6-112">string</span><span class="sxs-lookup"><span data-stu-id="745f6-112">string</span></span>  | <span data-ttu-id="745f6-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="745f6-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="745f6-115">Content-Type</span><span class="sxs-lookup"><span data-stu-id="745f6-115">Content-Type</span></span> | <span data-ttu-id="745f6-116">string</span><span class="sxs-lookup"><span data-stu-id="745f6-116">string</span></span>  | <span data-ttu-id="745f6-p103">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="745f6-p103">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="745f6-119">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="745f6-119">Request body</span></span>

## <a name="response"></a><span data-ttu-id="745f6-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="745f6-120">Response</span></span>

<span data-ttu-id="745f6-121">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [Message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="745f6-121">If successful, this method returns `201, Created` response code and [message](../resources/message.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="745f6-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="745f6-122">Example</span></span>
<span data-ttu-id="745f6-123">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="745f6-123">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="745f6-124">Solicitud</span><span class="sxs-lookup"><span data-stu-id="745f6-124">Request</span></span>
<span data-ttu-id="745f6-125">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="745f6-125">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_createforward"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/createForward
Content-type: application/json
Content-length: 248

{
  "comment": "Comment-value",
  "toRecipients": [
    {
      "emailAddress": {
        "address": "address-value"
      }
    },
    {
      "emailAddress": {
        "address": "address-value"
      }
    }
  ]
}
```

##### <a name="response"></a><span data-ttu-id="745f6-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="745f6-126">Response</span></span>
<span data-ttu-id="745f6-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="745f6-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 248

{
  "receivedDateTime": "datetime-value",
  "sentDateTime": "datetime-value",
  "hasAttachments": true,
  "subject": "subject-value",
  "body": {
    "contentType": "",
    "content": "content-value"
  },
  "bodyPreview": "bodyPreview-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: createForward",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
