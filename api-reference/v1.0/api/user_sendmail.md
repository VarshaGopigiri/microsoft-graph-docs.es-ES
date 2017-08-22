# <a name="send-mail"></a><span data-ttu-id="433e5-101">Enviar correo</span><span class="sxs-lookup"><span data-stu-id="433e5-101">Send mail</span></span>

<span data-ttu-id="433e5-p101">Envía el mensaje especificado en el cuerpo de la solicitud. De manera predeterminada, el mensaje se guarda en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="433e5-p101">Send the message specified in the request body. The message is saved in the Sent Items folder by default.</span></span>

<span data-ttu-id="433e5-104">Puede incluir [datos adjuntos del archivo](../resources/fileattachment.md) en la misma llamada de acción **sendMail**.</span><span class="sxs-lookup"><span data-stu-id="433e5-104">You can include a [file attachment](../resources/fileattachment.md) in the same **sendMail** action call.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="433e5-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="433e5-105">Prerequisites</span></span>
<span data-ttu-id="433e5-106">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Mail.Send*</span><span class="sxs-lookup"><span data-stu-id="433e5-106">One of the following **scopes** is required to execute this API: *Mail.Send*</span></span>

## <a name="http-request"></a><span data-ttu-id="433e5-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="433e5-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/sendMail
```
## <a name="request-headers"></a><span data-ttu-id="433e5-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="433e5-108">Request headers</span></span>
| <span data-ttu-id="433e5-109">Encabezado</span><span class="sxs-lookup"><span data-stu-id="433e5-109">Header</span></span>       | <span data-ttu-id="433e5-110">Valor</span><span class="sxs-lookup"><span data-stu-id="433e5-110">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="433e5-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="433e5-111">Authorization</span></span>  | <span data-ttu-id="433e5-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="433e5-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="433e5-114">Content-Type</span><span class="sxs-lookup"><span data-stu-id="433e5-114">Content-Type</span></span>  | <span data-ttu-id="433e5-115">application/json</span><span class="sxs-lookup"><span data-stu-id="433e5-115">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="433e5-116">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="433e5-116">Request body</span></span>
<span data-ttu-id="433e5-117">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="433e5-117">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="433e5-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="433e5-118">Parameter</span></span>    | <span data-ttu-id="433e5-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="433e5-119">Type</span></span>   |<span data-ttu-id="433e5-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="433e5-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="433e5-121">Message</span><span class="sxs-lookup"><span data-stu-id="433e5-121">Message</span></span>|[<span data-ttu-id="433e5-122">Message</span><span class="sxs-lookup"><span data-stu-id="433e5-122">Message</span></span>](../resources/message.md)|<span data-ttu-id="433e5-p103">Mensaje que se va a enviar. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="433e5-p103">The message to send. Required.</span></span>|
|<span data-ttu-id="433e5-125">SaveToSentItems</span><span class="sxs-lookup"><span data-stu-id="433e5-125">SaveToSentItems</span></span>|<span data-ttu-id="433e5-126">Boolean</span><span class="sxs-lookup"><span data-stu-id="433e5-126">Boolean</span></span>|<span data-ttu-id="433e5-p104">Indica si se va a guardar el mensaje en Elementos enviados. Especifíquelo solo si el parámetro es falso, de forma predeterminada es verdadero.  Opcional.</span><span class="sxs-lookup"><span data-stu-id="433e5-p104">Indicates whether to save the message in Sent Items. Specify it only if the parameter is false; default is true.  Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="433e5-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="433e5-130">Response</span></span>

<span data-ttu-id="433e5-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `202, Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="433e5-p105">If successful, this method returns `202, Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="433e5-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="433e5-133">Example</span></span>
<span data-ttu-id="433e5-134">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="433e5-134">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="433e5-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="433e5-135">Request</span></span>
<span data-ttu-id="433e5-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="433e5-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "user_sendmail"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/sendMail
Content-type: application/json
Content-length: 512

{
  "message": {
    "subject": "Meet for lunch?",
    "body": {
      "contentType": "Text",
      "content": "The new cafeteria is open."
    },
    "toRecipients": [
      {
        "emailAddress": {
          "address": "fannyd@contoso.onmicrosoft.com"
        }
      }
    ],
    "ccRecipients": [
      {
        "emailAddress": {
          "address": "danas@contoso.onmicrosoft.com"
        }
      }
    ]
  },
  "saveToSentItems": "false"
}
```

##### <a name="response"></a><span data-ttu-id="433e5-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="433e5-137">Response</span></span>
<span data-ttu-id="433e5-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="433e5-138">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 202 Accepted
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: sendMail",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
