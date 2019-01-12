---
title: Enviar correo
description: Envía el mensaje especificado en el cuerpo de la solicitud. De manera predeterminada, el mensaje se guarda en la carpeta Elementos enviados.
author: dkershaw10
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 48e6087cb8393bb4f679cabfe73d5cb280a71907
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27991431"
---
# <a name="send-mail"></a><span data-ttu-id="a117b-104">Enviar correo</span><span class="sxs-lookup"><span data-stu-id="a117b-104">Send mail</span></span>

> <span data-ttu-id="a117b-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a117b-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a117b-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a117b-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a117b-p103">Envía el mensaje especificado en el cuerpo de la solicitud. De manera predeterminada, el mensaje se guarda en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="a117b-p103">Send the message specified in the request body. The message is saved in the Sent Items folder by default.</span></span>

<span data-ttu-id="a117b-109">En la misma llamada de acción **sendMail** , se puede:</span><span class="sxs-lookup"><span data-stu-id="a117b-109">In the same **sendMail** action call, you can:</span></span>

- <span data-ttu-id="a117b-110">Incluir [datos adjuntos](../resources/attachment.md)</span><span class="sxs-lookup"><span data-stu-id="a117b-110">Include an [attachment](../resources/attachment.md)</span></span>
- <span data-ttu-id="a117b-111">Use un [mencione](../resources/mention.md) para llamar a otro usuario en el nuevo mensaje</span><span class="sxs-lookup"><span data-stu-id="a117b-111">Use a [mention](../resources/mention.md) to call out another user in the new message</span></span>

## <a name="permissions"></a><span data-ttu-id="a117b-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="a117b-112">Permissions</span></span>
<span data-ttu-id="a117b-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a117b-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="a117b-115">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a117b-115">Permission type</span></span>      | <span data-ttu-id="a117b-116">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a117b-116">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a117b-117">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a117b-117">Delegated (work or school account)</span></span> | <span data-ttu-id="a117b-118">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="a117b-118">Mail.Send</span></span>    |
|<span data-ttu-id="a117b-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a117b-119">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a117b-120">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="a117b-120">Mail.Send</span></span>    |
|<span data-ttu-id="a117b-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a117b-121">Application</span></span> | <span data-ttu-id="a117b-122">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="a117b-122">Mail.Send</span></span> |

## <a name="http-request"></a><span data-ttu-id="a117b-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a117b-123">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/sendMail
```
## <a name="request-headers"></a><span data-ttu-id="a117b-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a117b-124">Request headers</span></span>
| <span data-ttu-id="a117b-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a117b-125">Header</span></span>       | <span data-ttu-id="a117b-126">Valor</span><span class="sxs-lookup"><span data-stu-id="a117b-126">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="a117b-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="a117b-127">Authorization</span></span>  | <span data-ttu-id="a117b-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a117b-p105">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="a117b-130">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a117b-130">Content-Type</span></span>  | <span data-ttu-id="a117b-131">application/json</span><span class="sxs-lookup"><span data-stu-id="a117b-131">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="a117b-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a117b-132">Request body</span></span>
<span data-ttu-id="a117b-133">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="a117b-133">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="a117b-134">Parámetro</span><span class="sxs-lookup"><span data-stu-id="a117b-134">Parameter</span></span>    | <span data-ttu-id="a117b-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="a117b-135">Type</span></span>   |<span data-ttu-id="a117b-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="a117b-136">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a117b-137">Message</span><span class="sxs-lookup"><span data-stu-id="a117b-137">Message</span></span>|[<span data-ttu-id="a117b-138">Message</span><span class="sxs-lookup"><span data-stu-id="a117b-138">Message</span></span>](../resources/message.md)|<span data-ttu-id="a117b-p106">Mensaje que se va a enviar. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a117b-p106">The message to send. Required.</span></span>|
|<span data-ttu-id="a117b-141">SaveToSentItems</span><span class="sxs-lookup"><span data-stu-id="a117b-141">SaveToSentItems</span></span>|<span data-ttu-id="a117b-142">Boolean</span><span class="sxs-lookup"><span data-stu-id="a117b-142">Boolean</span></span>|<span data-ttu-id="a117b-p107">Indica si se va a guardar el mensaje en Elementos enviados. Especifíquelo solo si el parámetro es falso, de forma predeterminada es verdadero.  Opcional.</span><span class="sxs-lookup"><span data-stu-id="a117b-p107">Indicates whether to save the message in Sent Items. Specify it only if the parameter is false; default is true.  Optional.</span></span>|

<span data-ttu-id="a117b-146">Si desea usar **mencione** para llamar a otro usuario en el nuevo mensaje:</span><span class="sxs-lookup"><span data-stu-id="a117b-146">If you want to use **mention** to call out another user in the new message:</span></span>

- <span data-ttu-id="a117b-147">Incluir la propiedad necesario **toRecipients** , la propiedad **menciones** y las propiedades de mensaje puede escribir en el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a117b-147">Include the required **toRecipients** property, the **mentions** property, and any writable message properties in the request body.</span></span>
- <span data-ttu-id="a117b-148">Para cada mención en la propiedad **menciones** , debe especificar la propiedad **que se mencionan** .</span><span class="sxs-lookup"><span data-stu-id="a117b-148">For each mention in the **mentions** property, you must specify the **mentioned** property.</span></span>

## <a name="response"></a><span data-ttu-id="a117b-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a117b-149">Response</span></span>

<span data-ttu-id="a117b-p108">Si se ejecuta correctamente, este método devuelve el código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a117b-p108">If successful, this method returns `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a117b-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a117b-152">Example</span></span>
<span data-ttu-id="a117b-153">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="a117b-153">Here is an example of how to call this API.</span></span>
##### <a name="request-1"></a><span data-ttu-id="a117b-154">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="a117b-154">Request 1</span></span>
<span data-ttu-id="a117b-155">Este es un ejemplo de la solicitud para crear y enviar un mensaje sobre la marcha.</span><span class="sxs-lookup"><span data-stu-id="a117b-155">Here is an example of the request to create and send a message on the fly.</span></span>
<!-- {
  "blockType": "request",
  "name": "user_sendmail"
}-->
```http
POST https://graph.microsoft.com/beta/me/sendMail
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
          "address": "samanthab@contoso.onmicrosoft.com"
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

##### <a name="response-1"></a><span data-ttu-id="a117b-156">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="a117b-156">Response 1</span></span>
<span data-ttu-id="a117b-157">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a117b-157">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 202 Accepted
```


##### <a name="request-2"></a><span data-ttu-id="a117b-158">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="a117b-158">Request 2</span></span>
<span data-ttu-id="a117b-159">En el ejemplo siguiente se muestra un mensaje por el usuario ha iniciado sesión a Samantha Booth.</span><span class="sxs-lookup"><span data-stu-id="a117b-159">The next example shows a message by the signed-in user to Samantha Booth.</span></span> <span data-ttu-id="a117b-160">El mensaje también incluye una mención de otro usuario, Dana Swope.</span><span class="sxs-lookup"><span data-stu-id="a117b-160">The message also includes a mention of another user, Dana Swope.</span></span>
<!-- {
  "blockType": "request",
  "name": "user_sendmail_with_mentions"
}-->
```http
POST https://graph.microsoft.com/beta/me/sendMail
Content-type: application/json
Content-length: 344

{
  "Message": {
    "subject": "Project kickoff",
    "toRecipients":[
      {
          "emailAddress":{
              "name":"Samantha Booth",
              "address":"samanthab@contoso.onmicrosoft.com"
          }
      }
    ],
    "mentions":[
      {
        "mentioned":{
          "name":"Dana Swope",
          "address":"danas@contoso.onmicrosoft.com"
         }
      }
    ]
  }
}
```

##### <a name="response-2"></a><span data-ttu-id="a117b-161">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="a117b-161">Response 2</span></span>
<span data-ttu-id="a117b-162">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a117b-162">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 202 Accepted
```

##### <a name="request-3"></a><span data-ttu-id="a117b-163">Solicitud 3</span><span class="sxs-lookup"><span data-stu-id="a117b-163">Request 3</span></span>
<span data-ttu-id="a117b-164">En el ejemplo siguiente se crea un mensaje con encabezados de mensaje de Internet personalizados y envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="a117b-164">The next example creates a message with custom Internet message headers and sends the message.</span></span>
<!-- {
  "blockType": "request",
  "name": "user_sendmail_with_headers"
}-->
```http
POST https://graph.microsoft.com/beta/me/sendMail
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

##### <a name="response-3"></a><span data-ttu-id="a117b-165">Respuesta 3</span><span class="sxs-lookup"><span data-stu-id="a117b-165">Response 3</span></span>
<span data-ttu-id="a117b-166">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a117b-166">Here is an example of the response.</span></span>
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
