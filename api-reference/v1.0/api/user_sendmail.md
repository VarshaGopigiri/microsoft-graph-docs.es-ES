# <a name="send-mail"></a><span data-ttu-id="ee4e3-101">Enviar correo</span><span class="sxs-lookup"><span data-stu-id="ee4e3-101">Send mail</span></span>

<span data-ttu-id="ee4e3-p101">Envía el mensaje especificado en el cuerpo de la solicitud. De manera predeterminada, el mensaje se guarda en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-p101">Send the message specified in the request body. The message is saved in the Sent Items folder by default.</span></span>

<span data-ttu-id="ee4e3-104">Puede incluir [datos adjuntos del archivo](../resources/fileattachment.md) en la misma llamada de acción **sendMail**.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-104">You can include a [file attachment](../resources/fileattachment.md) in the same **sendMail** action call.</span></span>

## <a name="permissions"></a><span data-ttu-id="ee4e3-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="ee4e3-105">Permissions</span></span>
<span data-ttu-id="ee4e3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ee4e3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="ee4e3-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ee4e3-108">Permission type</span></span>      | <span data-ttu-id="ee4e3-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ee4e3-109">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="ee4e3-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ee4e3-110">Delegated (work or school account)</span></span> | <span data-ttu-id="ee4e3-111">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="ee4e3-111">Mail.Send</span></span>    | 
|<span data-ttu-id="ee4e3-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ee4e3-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ee4e3-113">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="ee4e3-113">Mail.Send</span></span>    | 
|<span data-ttu-id="ee4e3-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ee4e3-114">Application</span></span> | <span data-ttu-id="ee4e3-115">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="ee4e3-115">Mail.Send</span></span> | 

## <a name="http-request"></a><span data-ttu-id="ee4e3-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ee4e3-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/sendMail
```
## <a name="request-headers"></a><span data-ttu-id="ee4e3-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ee4e3-117">Request headers</span></span>
| <span data-ttu-id="ee4e3-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee4e3-118">Header</span></span>       | <span data-ttu-id="ee4e3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="ee4e3-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ee4e3-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="ee4e3-120">Authorization</span></span>  | <span data-ttu-id="ee4e3-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="ee4e3-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ee4e3-123">Content-Type</span></span>  | <span data-ttu-id="ee4e3-124">application/json</span><span class="sxs-lookup"><span data-stu-id="ee4e3-124">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ee4e3-125">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="ee4e3-125">Request body</span></span>
<span data-ttu-id="ee4e3-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="ee4e3-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ee4e3-127">Parameter</span></span>    | <span data-ttu-id="ee4e3-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="ee4e3-128">Type</span></span>   |<span data-ttu-id="ee4e3-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee4e3-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ee4e3-130">Message</span><span class="sxs-lookup"><span data-stu-id="ee4e3-130">Message</span></span>|[<span data-ttu-id="ee4e3-131">Message</span><span class="sxs-lookup"><span data-stu-id="ee4e3-131">Message</span></span>](../resources/message.md)|<span data-ttu-id="ee4e3-p104">Mensaje que se va a enviar. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-p104">The message to send. Required.</span></span>|
|<span data-ttu-id="ee4e3-134">SaveToSentItems</span><span class="sxs-lookup"><span data-stu-id="ee4e3-134">SaveToSentItems</span></span>|<span data-ttu-id="ee4e3-135">Boolean</span><span class="sxs-lookup"><span data-stu-id="ee4e3-135">Boolean</span></span>|<span data-ttu-id="ee4e3-p105">Indica si se va a guardar el mensaje en Elementos enviados. Especifíquelo solo si el parámetro es falso, de forma predeterminada es verdadero.  Opcional.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-p105">Indicates whether to save the message in Sent Items. Specify it only if the parameter is false; default is true.  Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="ee4e3-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ee4e3-139">Response</span></span>

<span data-ttu-id="ee4e3-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `202, Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-p106">If successful, this method returns `202, Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ee4e3-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ee4e3-142">Example</span></span>
<span data-ttu-id="ee4e3-143">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-143">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="ee4e3-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ee4e3-144">Request</span></span>
<span data-ttu-id="ee4e3-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-145">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="ee4e3-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ee4e3-146">Response</span></span>
<span data-ttu-id="ee4e3-147">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ee4e3-147">Here is an example of the response.</span></span>
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
