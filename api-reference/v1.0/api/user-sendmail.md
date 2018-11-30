---
title: Enviar correo
description: Envía el mensaje especificado en el cuerpo de la solicitud. De manera predeterminada, el mensaje se guarda en la carpeta Elementos enviados.
ms.openlocfilehash: 6d8150f7292747e7c1d182395f9a98b1a199389f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029242"
---
# <a name="send-mail"></a><span data-ttu-id="9b078-104">Enviar correo</span><span class="sxs-lookup"><span data-stu-id="9b078-104">Send mail</span></span>

<span data-ttu-id="9b078-p102">Envía el mensaje especificado en el cuerpo de la solicitud. De manera predeterminada, el mensaje se guarda en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="9b078-p102">Send the message specified in the request body. The message is saved in the Sent Items folder by default.</span></span>

<span data-ttu-id="9b078-107">Puede incluir [datos adjuntos del archivo](../resources/fileattachment.md) en la misma llamada de acción **sendMail**.</span><span class="sxs-lookup"><span data-stu-id="9b078-107">You can include a [file attachment](../resources/fileattachment.md) in the same **sendMail** action call.</span></span>

## <a name="permissions"></a><span data-ttu-id="9b078-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="9b078-108">Permissions</span></span>
<span data-ttu-id="9b078-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9b078-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="9b078-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9b078-111">Permission type</span></span>      | <span data-ttu-id="9b078-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9b078-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9b078-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9b078-113">Delegated (work or school account)</span></span> | <span data-ttu-id="9b078-114">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="9b078-114">Mail.Send</span></span>    |
|<span data-ttu-id="9b078-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9b078-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9b078-116">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="9b078-116">Mail.Send</span></span>    |
|<span data-ttu-id="9b078-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9b078-117">Application</span></span> | <span data-ttu-id="9b078-118">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="9b078-118">Mail.Send</span></span> |

## <a name="http-request"></a><span data-ttu-id="9b078-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9b078-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/sendMail
```
## <a name="request-headers"></a><span data-ttu-id="9b078-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9b078-120">Request headers</span></span>
| <span data-ttu-id="9b078-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b078-121">Header</span></span>       | <span data-ttu-id="9b078-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9b078-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="9b078-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="9b078-123">Authorization</span></span>  | <span data-ttu-id="9b078-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9b078-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="9b078-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="9b078-126">Content-Type</span></span>  | <span data-ttu-id="9b078-127">application/json</span><span class="sxs-lookup"><span data-stu-id="9b078-127">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="9b078-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9b078-128">Request body</span></span>
<span data-ttu-id="9b078-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="9b078-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="9b078-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9b078-130">Parameter</span></span>    | <span data-ttu-id="9b078-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b078-131">Type</span></span>   |<span data-ttu-id="9b078-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b078-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9b078-133">mensaje</span><span class="sxs-lookup"><span data-stu-id="9b078-133">message</span></span>|[<span data-ttu-id="9b078-134">Message</span><span class="sxs-lookup"><span data-stu-id="9b078-134">Message</span></span>](../resources/message.md)|<span data-ttu-id="9b078-p105">Mensaje que se va a enviar. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9b078-p105">The message to send. Required.</span></span>|
|<span data-ttu-id="9b078-137">saveToSentItems</span><span class="sxs-lookup"><span data-stu-id="9b078-137">saveToSentItems</span></span>|<span data-ttu-id="9b078-138">Boolean</span><span class="sxs-lookup"><span data-stu-id="9b078-138">Boolean</span></span>|<span data-ttu-id="9b078-p106">Indica si se va a guardar el mensaje en Elementos enviados. Especifíquelo solo si el parámetro es falso, de forma predeterminada es verdadero.  Opcional.</span><span class="sxs-lookup"><span data-stu-id="9b078-p106">Indicates whether to save the message in Sent Items. Specify it only if the parameter is false; default is true.  Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="9b078-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b078-142">Response</span></span>

<span data-ttu-id="9b078-p107">Si se ejecuta correctamente, este método devuelve el código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b078-p107">If successful, this method returns `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9b078-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9b078-145">Example</span></span>
<span data-ttu-id="9b078-146">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="9b078-146">Here is an example of how to call this API.</span></span>
##### <a name="request-1"></a><span data-ttu-id="9b078-147">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="9b078-147">Request 1</span></span>
<span data-ttu-id="9b078-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9b078-148">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "user_sendmail"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/sendMail
Content-type: application/json

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

##### <a name="response-1"></a><span data-ttu-id="9b078-149">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="9b078-149">Response 1</span></span>
<span data-ttu-id="9b078-150">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b078-150">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 202 Accepted
```

##### <a name="request-2"></a><span data-ttu-id="9b078-151">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="9b078-151">Request 2</span></span>
<span data-ttu-id="9b078-152">En el ejemplo siguiente se crea un mensaje con encabezados de mensaje de Internet personalizados y envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="9b078-152">The next example creates a message with custom Internet message headers and sends the message.</span></span>
<!-- {
  "blockType": "request",
  "name": "user_sendmail_with_headers"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/sendMail
Content-type: application/json

{
  "message": {
    "subject": "9/9/2018: concert",
    "body": {
      "contentType": "HTML",
      "content": "The group represents Nevada."
    },
    "toRecipients": [
      {
        "emailAddress": {
          "address": "AlexW@contoso.OnMicrosoft.com"
        }
      }
    ],
    "internetMessageHeaders":[
      {
        "name":"x-custom-header-group-name",
        "value":"Nevada"
      },
      {
        "name":"x-custom-header-group-id",
        "value":"NV001"
      }
    ]
  }
}
```

##### <a name="response-2"></a><span data-ttu-id="9b078-153">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="9b078-153">Response 2</span></span>
<span data-ttu-id="9b078-154">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b078-154">Here is an example of the response.</span></span>
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