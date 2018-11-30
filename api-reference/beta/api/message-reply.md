---
title: 'message: reply'
description: 'Responder al remitente de un mensaje, agregar un comentario o modificar las propiedades actualizables todo en una **respuesta** de llamada. '
ms.openlocfilehash: 93130e8a877b9a7bdc553646037f583fd8da84fc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087797"
---
# <a name="message-reply"></a><span data-ttu-id="734a5-103">message: reply</span><span class="sxs-lookup"><span data-stu-id="734a5-103">message: reply</span></span>

> <span data-ttu-id="734a5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="734a5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="734a5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="734a5-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="734a5-106">Responder al remitente de un mensaje, agregar un comentario o modificar las propiedades actualizables todo en una **respuesta** de llamada.</span><span class="sxs-lookup"><span data-stu-id="734a5-106">Reply to the sender of a message, add a comment or modify any updateable properties all in one **reply** call.</span></span> <span data-ttu-id="734a5-107">A continuación, se guarda el mensaje en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="734a5-107">The message is then saved in the Sent Items folder.</span></span>

<span data-ttu-id="734a5-108">Como alternativa, puede [crear un mensaje de respuesta de borrador](../api/message-createreply.md) para incluir un comentario o actualizar las propiedades del mensaje y, a continuación, [Enviar](../api/message-send.md) la respuesta.</span><span class="sxs-lookup"><span data-stu-id="734a5-108">Alternatively, you can first [create a draft reply message](../api/message-createreply.md) to include a comment or update any message properties, and then [send](../api/message-send.md) the reply.</span></span>

<span data-ttu-id="734a5-109">**Nota**</span><span class="sxs-lookup"><span data-stu-id="734a5-109">**Note**</span></span>

- <span data-ttu-id="734a5-110">Puede especificar un comentario o la propiedad **body** de la `message` parámetro.</span><span class="sxs-lookup"><span data-stu-id="734a5-110">You can specify either a comment or the **body** property of the `message` parameter.</span></span> <span data-ttu-id="734a5-111">Si se especifica tanto devolverá un error HTTP 400 Solicitud incorrecta.</span><span class="sxs-lookup"><span data-stu-id="734a5-111">Specifying both will return an HTTP 400 Bad Request error.</span></span>
- <span data-ttu-id="734a5-112">Si la propiedad de **origen** se especifica en el mensaje original, por el formato de mensaje de Internet ([RFC 2822](https://www.rfc-editor.org/info/rfc2822)), debe enviar la respuesta a los destinatarios en el **origen** y no el destinatario en la propiedad **from** .</span><span class="sxs-lookup"><span data-stu-id="734a5-112">If the **replyTo** property is specified in the original message, per Internet Message Format ([RFC 2822](https://www.rfc-editor.org/info/rfc2822)), you should send the reply to the recipients in **replyTo** and not the recipient in the **from** property.</span></span> 


## <a name="permissions"></a><span data-ttu-id="734a5-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="734a5-113">Permissions</span></span>
<span data-ttu-id="734a5-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="734a5-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="734a5-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="734a5-116">Permission type</span></span>      | <span data-ttu-id="734a5-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="734a5-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="734a5-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="734a5-118">Delegated (work or school account)</span></span> | <span data-ttu-id="734a5-119">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="734a5-119">Mail.Send</span></span>    |
|<span data-ttu-id="734a5-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="734a5-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="734a5-121">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="734a5-121">Mail.Send</span></span>    |
|<span data-ttu-id="734a5-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="734a5-122">Application</span></span> | <span data-ttu-id="734a5-123">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="734a5-123">Mail.Send</span></span> |

## <a name="http-request"></a><span data-ttu-id="734a5-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="734a5-124">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/reply
POST /users/{id | userPrincipalName}/messages/{id}/reply
POST /me/mailFolders/{id}/messages/{id}/reply
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/reply
```
## <a name="request-headers"></a><span data-ttu-id="734a5-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="734a5-125">Request headers</span></span>
| <span data-ttu-id="734a5-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="734a5-126">Name</span></span>       | <span data-ttu-id="734a5-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="734a5-127">Type</span></span> | <span data-ttu-id="734a5-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="734a5-128">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="734a5-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="734a5-129">Authorization</span></span>  | <span data-ttu-id="734a5-130">string</span><span class="sxs-lookup"><span data-stu-id="734a5-130">string</span></span>  | <span data-ttu-id="734a5-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="734a5-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="734a5-133">Content-Type</span><span class="sxs-lookup"><span data-stu-id="734a5-133">Content-Type</span></span> | <span data-ttu-id="734a5-134">string</span><span class="sxs-lookup"><span data-stu-id="734a5-134">string</span></span>  | <span data-ttu-id="734a5-p106">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="734a5-p106">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="734a5-137">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="734a5-137">Request body</span></span>
<span data-ttu-id="734a5-138">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="734a5-138">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="734a5-139">Parámetro</span><span class="sxs-lookup"><span data-stu-id="734a5-139">Parameter</span></span>    | <span data-ttu-id="734a5-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="734a5-140">Type</span></span>   |<span data-ttu-id="734a5-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="734a5-141">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="734a5-142">comment</span><span class="sxs-lookup"><span data-stu-id="734a5-142">comment</span></span>|<span data-ttu-id="734a5-143">String</span><span class="sxs-lookup"><span data-stu-id="734a5-143">String</span></span>|<span data-ttu-id="734a5-p107">Comentario que se va a incluir. Puede ser una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="734a5-p107">A comment to include. Can be an empty string.</span></span>|
|<span data-ttu-id="734a5-146">mensaje</span><span class="sxs-lookup"><span data-stu-id="734a5-146">message</span></span>|[<span data-ttu-id="734a5-147">message</span><span class="sxs-lookup"><span data-stu-id="734a5-147">message</span></span>](../resources/message.md)|<span data-ttu-id="734a5-148">Cualquier propiedad grabable para actualizar en el mensaje de respuesta.</span><span class="sxs-lookup"><span data-stu-id="734a5-148">Any writeable properties to update in the reply message.</span></span>|

## <a name="response"></a><span data-ttu-id="734a5-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="734a5-149">Response</span></span>

<span data-ttu-id="734a5-p108">Si se ejecuta correctamente, este método devuelve el código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="734a5-p108">If successful, this method returns `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="734a5-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="734a5-152">Example</span></span>
<span data-ttu-id="734a5-153">En el ejemplo siguiente se incluye un comentario y agrega a un destinatario para el mensaje de respuesta.</span><span class="sxs-lookup"><span data-stu-id="734a5-153">The following example includes a comment and adds a recipient to the reply message.</span></span>
##### <a name="request"></a><span data-ttu-id="734a5-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="734a5-154">Request</span></span>
<span data-ttu-id="734a5-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="734a5-155">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_reply"
}-->
```http
POST https://graph.microsoft.com/beta/me/messages/AAMkADA1MTAAAAqldOAAA=/reply
Content-Type: application/json

{
  "message":{  
    "toRecipients":[
      {
        "emailAddress": {
          "address":"samanthab@contoso.onmicrosoft.com",
          "name":"Samantha Booth"
        }
      },
      {
        "emailAddress":{
          "address":"randiw@contoso.onmicrosoft.com",
          "name":"Randi Welch"
        }
      }
     ]
  },
  "comment": "Samantha, Randi, would you name the group please?" 
}
```

##### <a name="response"></a><span data-ttu-id="734a5-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="734a5-156">Response</span></span>
<span data-ttu-id="734a5-157">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="734a5-157">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 201 Created
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: reply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
