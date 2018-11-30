---
title: 'message: replyAll'
description: 'Responder a todos los destinatarios de un mensaje mediante la especificación de un comentario y modificación de las propiedades actualizables '
ms.openlocfilehash: c79320229aad67a406a6519762c7cdd99af2ad50
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089625"
---
# <a name="message-replyall"></a><span data-ttu-id="c0c22-103">message: replyAll</span><span class="sxs-lookup"><span data-stu-id="c0c22-103">message: replyAll</span></span>

> <span data-ttu-id="c0c22-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c0c22-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c0c22-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c0c22-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c0c22-106">Responder a todos los destinatarios de un mensaje mediante la especificación de un comentario y modificación de las propiedades para la respuesta, puede actualizables todos los mediante el método **replyAll** .</span><span class="sxs-lookup"><span data-stu-id="c0c22-106">Reply to all recipients of a message by specifying a comment and modifying any updateable properties for the reply, all by using the **replyAll** method.</span></span> <span data-ttu-id="c0c22-107">A continuación, se guarda el mensaje en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="c0c22-107">The message is then saved in the Sent Items folder.</span></span>

<span data-ttu-id="c0c22-108">Como alternativa, puede [crear un borrador de mensaje de responder a todos](../api/message-createreplyall.md) para incluir un comentario o actualizar las propiedades del mensaje y, a continuación, [Enviar](../api/message-send.md) la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0c22-108">Alternatively, you can first [create a draft reply-all message](../api/message-createreplyall.md) to include a comment or update any message properties, and then [send](../api/message-send.md) the reply.</span></span>

<span data-ttu-id="c0c22-109">**Nota**</span><span class="sxs-lookup"><span data-stu-id="c0c22-109">**Note**</span></span>

- <span data-ttu-id="c0c22-110">Puede especificar un comentario o la propiedad **body** de la `message` parámetro.</span><span class="sxs-lookup"><span data-stu-id="c0c22-110">You can specify either a comment or the **body** property of the `message` parameter.</span></span> <span data-ttu-id="c0c22-111">Si se especifica tanto devolverá un error HTTP 400 Solicitud incorrecta.</span><span class="sxs-lookup"><span data-stu-id="c0c22-111">Specifying both will return an HTTP 400 Bad Request error.</span></span>
- <span data-ttu-id="c0c22-112">Si la propiedad de **origen** se especifica en el mensaje original, por el formato de mensaje de Internet ([RFC 2822](https://www.rfc-editor.org/info/rfc2822)), debe enviar la respuesta a los destinatarios en el</span><span class="sxs-lookup"><span data-stu-id="c0c22-112">If the **replyTo** property is specified in the original message, per Internet Message Format ([RFC 2822](https://www.rfc-editor.org/info/rfc2822)), you should send the reply to the recipients in the</span></span>  
<span data-ttu-id="c0c22-113">propiedades de **origen** y **toRecipients** y no los destinatarios en las propiedades **de** y **toRecipients** .</span><span class="sxs-lookup"><span data-stu-id="c0c22-113">**replyTo** and **toRecipients** properties, and not the recipients in the **from** and **toRecipients** properties.</span></span> 


## <a name="permissions"></a><span data-ttu-id="c0c22-114">Permisos</span><span class="sxs-lookup"><span data-stu-id="c0c22-114">Permissions</span></span>
<span data-ttu-id="c0c22-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c0c22-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c0c22-117">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c0c22-117">Permission type</span></span>      | <span data-ttu-id="c0c22-118">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c0c22-118">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c0c22-119">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c0c22-119">Delegated (work or school account)</span></span> | <span data-ttu-id="c0c22-120">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="c0c22-120">Mail.Send</span></span>    |
|<span data-ttu-id="c0c22-121">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c0c22-121">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c0c22-122">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="c0c22-122">Mail.Send</span></span>    |
|<span data-ttu-id="c0c22-123">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c0c22-123">Application</span></span> | <span data-ttu-id="c0c22-124">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="c0c22-124">Mail.Send</span></span> |

## <a name="http-request"></a><span data-ttu-id="c0c22-125">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c0c22-125">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/me/messages/{id}/replyAll
POST /users/{id | userPrincipalName}/messages/{id}/replyAll
POST /me/mailFolders/{id}/messages/{id}/replyAll
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/replyAll
```
## <a name="request-headers"></a><span data-ttu-id="c0c22-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c0c22-126">Request headers</span></span>
| <span data-ttu-id="c0c22-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="c0c22-127">Name</span></span>       | <span data-ttu-id="c0c22-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="c0c22-128">Type</span></span> | <span data-ttu-id="c0c22-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0c22-129">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="c0c22-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="c0c22-130">Authorization</span></span>  | <span data-ttu-id="c0c22-131">string</span><span class="sxs-lookup"><span data-stu-id="c0c22-131">string</span></span>  | <span data-ttu-id="c0c22-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c0c22-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c0c22-134">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c0c22-134">Content-Type</span></span> | <span data-ttu-id="c0c22-135">string</span><span class="sxs-lookup"><span data-stu-id="c0c22-135">string</span></span>  | <span data-ttu-id="c0c22-p106">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c0c22-p106">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c0c22-138">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c0c22-138">Request body</span></span>
<span data-ttu-id="c0c22-139">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="c0c22-139">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="c0c22-140">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c0c22-140">Parameter</span></span>    | <span data-ttu-id="c0c22-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="c0c22-141">Type</span></span>   |<span data-ttu-id="c0c22-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0c22-142">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c0c22-143">comment</span><span class="sxs-lookup"><span data-stu-id="c0c22-143">comment</span></span>|<span data-ttu-id="c0c22-144">String</span><span class="sxs-lookup"><span data-stu-id="c0c22-144">String</span></span>|<span data-ttu-id="c0c22-p107">Comentario que se va a incluir. Puede ser una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="c0c22-p107">A comment to include. Can be an empty string.</span></span>|
|<span data-ttu-id="c0c22-147">mensaje</span><span class="sxs-lookup"><span data-stu-id="c0c22-147">message</span></span>|[<span data-ttu-id="c0c22-148">message</span><span class="sxs-lookup"><span data-stu-id="c0c22-148">message</span></span>](../resources/message.md)|<span data-ttu-id="c0c22-149">Cualquier propiedad grabable para actualizar en el mensaje de respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0c22-149">Any writeable properties to update in the reply message.</span></span>|

## <a name="response"></a><span data-ttu-id="c0c22-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c0c22-150">Response</span></span>

<span data-ttu-id="c0c22-p108">Si se ejecuta correctamente, este método devuelve el código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0c22-p108">If successful, this method returns `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c0c22-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c0c22-153">Example</span></span>
<span data-ttu-id="c0c22-154">En el ejemplo siguiente se incluye un comentario y agrega datos adjuntos al mensaje de responder a todos.</span><span class="sxs-lookup"><span data-stu-id="c0c22-154">The following example includes a comment and adds an attachment to the reply-all message.</span></span>
##### <a name="request"></a><span data-ttu-id="c0c22-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c0c22-155">Request</span></span>
<span data-ttu-id="c0c22-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c0c22-156">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_replyall"
}-->
```http
POST https://graph.microsoft.com/beta/me/messages/AAMkADA1MTAAAH5JaKAAA=/replyAll
Content-Type: application/json

{
    "message":{
      "attachments": [ 
        { 
          "@odata.type": "#microsoft.graph.fileAttachment", 
          "name": "guidelines.txt", 
          "contentBytes": "bWFjIGFuZCBjaGVlc2UgdG9kYXk=" 
        } 
      ]
    },
    "comment": "Please take a look at the attached guidelines before you decide on the name." 
}
```


##### <a name="response"></a><span data-ttu-id="c0c22-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c0c22-157">Response</span></span>
<span data-ttu-id="c0c22-158">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0c22-158">Here is an example of the response.</span></span>
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
  "description": "message: replyAll",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
