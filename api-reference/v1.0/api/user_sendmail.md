# <a name="send-mail"></a><span data-ttu-id="70c38-101">Enviar correo</span><span class="sxs-lookup"><span data-stu-id="70c38-101">Send mail</span></span>

<span data-ttu-id="70c38-p101">Envía el mensaje especificado en el cuerpo de la solicitud. De manera predeterminada, el mensaje se guarda en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="70c38-p101">Send the message specified in the request body. The message is saved in the Sent Items folder by default.</span></span>

<span data-ttu-id="70c38-104">Puede incluir [datos adjuntos del archivo](../resources/fileattachment.md) en la misma llamada de acción **sendMail**.</span><span class="sxs-lookup"><span data-stu-id="70c38-104">You can include a [file attachment](../resources/fileattachment.md) in the same **sendMail** action call.</span></span>

## <a name="permissions"></a><span data-ttu-id="70c38-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="70c38-105">Permissions</span></span>
<span data-ttu-id="70c38-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="70c38-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="70c38-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="70c38-108">Permission type</span></span>      | <span data-ttu-id="70c38-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="70c38-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="70c38-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="70c38-110">Delegated (work or school account)</span></span> | <span data-ttu-id="70c38-111">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="70c38-111">Mail.Send</span></span>    |
|<span data-ttu-id="70c38-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="70c38-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="70c38-113">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="70c38-113">Mail.Send</span></span>    |
|<span data-ttu-id="70c38-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="70c38-114">Application</span></span> | <span data-ttu-id="70c38-115">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="70c38-115">Mail.Send</span></span> |

## <a name="http-request"></a><span data-ttu-id="70c38-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="70c38-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/sendMail
```
## <a name="request-headers"></a><span data-ttu-id="70c38-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="70c38-117">Request headers</span></span>
| <span data-ttu-id="70c38-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70c38-118">Header</span></span>       | <span data-ttu-id="70c38-119">Valor</span><span class="sxs-lookup"><span data-stu-id="70c38-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="70c38-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="70c38-120">Authorization</span></span>  | <span data-ttu-id="70c38-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="70c38-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="70c38-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="70c38-123">Content-Type</span></span>  | <span data-ttu-id="70c38-124">application/json</span><span class="sxs-lookup"><span data-stu-id="70c38-124">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="70c38-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="70c38-125">Request body</span></span>
<span data-ttu-id="70c38-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="70c38-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="70c38-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="70c38-127">Parameter</span></span>    | <span data-ttu-id="70c38-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="70c38-128">Type</span></span>   |<span data-ttu-id="70c38-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="70c38-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="70c38-130">message</span><span class="sxs-lookup"><span data-stu-id="70c38-130">message</span></span>|[<span data-ttu-id="70c38-131">Mensaje</span><span class="sxs-lookup"><span data-stu-id="70c38-131">Message</span></span>](../resources/message.md)|<span data-ttu-id="70c38-p104">Mensaje que se va a enviar. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="70c38-p104">The message to send. Required.</span></span>|
|<span data-ttu-id="70c38-134">saveToSentItems</span><span class="sxs-lookup"><span data-stu-id="70c38-134">SaveToSentItems</span></span>|<span data-ttu-id="70c38-135">Booleano</span><span class="sxs-lookup"><span data-stu-id="70c38-135">Boolean</span></span>|<span data-ttu-id="70c38-p105">Indica si se va a guardar el mensaje en Elementos enviados. Especifíquelo solo si el parámetro es falso, de forma predeterminada es verdadero.  Opcional.</span><span class="sxs-lookup"><span data-stu-id="70c38-p105">Indicates whether to save the message in Sent Items. Specify it only if the parameter is false; default is true.  Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="70c38-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="70c38-139">Response</span></span>

<span data-ttu-id="70c38-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="70c38-p106">If successful, this method returns `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="70c38-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="70c38-142">Example</span></span>
<span data-ttu-id="70c38-143">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="70c38-143">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="70c38-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="70c38-144">Request</span></span>
<span data-ttu-id="70c38-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="70c38-145">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="70c38-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="70c38-146">Response</span></span>
<span data-ttu-id="70c38-147">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="70c38-147">Here is an example of the response.</span></span>
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
