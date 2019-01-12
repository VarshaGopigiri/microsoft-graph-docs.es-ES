---
title: 'message: createReplyAll'
description: 'Crear un borrador de un mensaje de responder a todos para incluir un comentario o actualizar las propiedades de mensaje '
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 7f0b2631f02a94a7627e96e24308b135d70d20e1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27922175"
---
# <a name="message-createreplyall"></a><span data-ttu-id="c42fd-103">message: createReplyAll</span><span class="sxs-lookup"><span data-stu-id="c42fd-103">message: createReplyAll</span></span>

> <span data-ttu-id="c42fd-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c42fd-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c42fd-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c42fd-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c42fd-106">Cree un borrador de un mensaje de responder a todos para incluir un comentario o actualizar las propiedades del mensaje, todo en una sola llamada **createReplyAll** .</span><span class="sxs-lookup"><span data-stu-id="c42fd-106">Create a draft of a reply-all message to include a comment or update any message properties, all in one **createReplyAll** call.</span></span> <span data-ttu-id="c42fd-107">A continuación, puede [Actualizar](../api/message-update.md) o [Enviar](../api/message-send.md) el borrador.</span><span class="sxs-lookup"><span data-stu-id="c42fd-107">You can then [update](../api/message-update.md) or [send](../api/message-send.md) the draft.</span></span>

<span data-ttu-id="c42fd-108">**Nota**</span><span class="sxs-lookup"><span data-stu-id="c42fd-108">**Note**</span></span>

- <span data-ttu-id="c42fd-109">Puede especificar un comentario o la propiedad **body** de la `message` parámetro.</span><span class="sxs-lookup"><span data-stu-id="c42fd-109">You can specify either a comment or the **body** property of the `message` parameter.</span></span> <span data-ttu-id="c42fd-110">Si se especifica tanto devolverá un error HTTP 400 Solicitud incorrecta.</span><span class="sxs-lookup"><span data-stu-id="c42fd-110">Specifying both will return an HTTP 400 Bad Request error.</span></span>
- <span data-ttu-id="c42fd-111">Si la propiedad de **origen** se especifica en el mensaje original, por el formato de mensaje de Internet ([RFC 2822](https://www.rfc-editor.org/info/rfc2822)), debe enviar la respuesta a los destinatarios en el</span><span class="sxs-lookup"><span data-stu-id="c42fd-111">If the **replyTo** property is specified in the original message, per Internet Message Format ([RFC 2822](https://www.rfc-editor.org/info/rfc2822)), you should send the reply to the recipients in the</span></span>  
<span data-ttu-id="c42fd-112">propiedades de **origen** y **toRecipients** y no los destinatarios en las propiedades **de** y **toRecipients** .</span><span class="sxs-lookup"><span data-stu-id="c42fd-112">**replyTo** and **toRecipients** properties, and not the recipients in the **from** and **toRecipients** properties.</span></span> 


## <a name="permissions"></a><span data-ttu-id="c42fd-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="c42fd-113">Permissions</span></span>
<span data-ttu-id="c42fd-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c42fd-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c42fd-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c42fd-116">Permission type</span></span>      | <span data-ttu-id="c42fd-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c42fd-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c42fd-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c42fd-118">Delegated (work or school account)</span></span> | <span data-ttu-id="c42fd-119">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c42fd-119">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="c42fd-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c42fd-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c42fd-121">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c42fd-121">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="c42fd-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c42fd-122">Application</span></span> | <span data-ttu-id="c42fd-123">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c42fd-123">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="c42fd-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c42fd-124">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/createReplyAll
POST /users/{id | userPrincipalName}/messages/{id}/createReplyAll
POST /me/mailFolders/{id}/messages/{id}/createReplyAll
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/createReplyAll
```
## <a name="request-headers"></a><span data-ttu-id="c42fd-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c42fd-125">Request headers</span></span>
| <span data-ttu-id="c42fd-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="c42fd-126">Name</span></span>       | <span data-ttu-id="c42fd-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="c42fd-127">Type</span></span> | <span data-ttu-id="c42fd-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="c42fd-128">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="c42fd-129">Autorización</span><span class="sxs-lookup"><span data-stu-id="c42fd-129">Authorization</span></span>  | <span data-ttu-id="c42fd-130">string</span><span class="sxs-lookup"><span data-stu-id="c42fd-130">string</span></span>  | <span data-ttu-id="c42fd-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c42fd-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c42fd-133">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c42fd-133">Content-Type</span></span> | <span data-ttu-id="c42fd-134">string</span><span class="sxs-lookup"><span data-stu-id="c42fd-134">string</span></span>  | <span data-ttu-id="c42fd-p106">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c42fd-p106">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c42fd-137">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c42fd-137">Request body</span></span>
<span data-ttu-id="c42fd-138">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="c42fd-138">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="c42fd-139">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c42fd-139">Parameter</span></span>    | <span data-ttu-id="c42fd-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="c42fd-140">Type</span></span>   |<span data-ttu-id="c42fd-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="c42fd-141">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c42fd-142">comment</span><span class="sxs-lookup"><span data-stu-id="c42fd-142">comment</span></span>|<span data-ttu-id="c42fd-143">String</span><span class="sxs-lookup"><span data-stu-id="c42fd-143">String</span></span>|<span data-ttu-id="c42fd-p107">Comentario que se va a incluir. Puede ser una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="c42fd-p107">A comment to include. Can be an empty string.</span></span>|
|<span data-ttu-id="c42fd-146">mensaje</span><span class="sxs-lookup"><span data-stu-id="c42fd-146">message</span></span>|[<span data-ttu-id="c42fd-147">message</span><span class="sxs-lookup"><span data-stu-id="c42fd-147">message</span></span>](../resources/message.md)|<span data-ttu-id="c42fd-148">Cualquier propiedad grabable para actualizar en el mensaje de responder a todos.</span><span class="sxs-lookup"><span data-stu-id="c42fd-148">Any writeable properties to update in the reply-all message.</span></span>|

## <a name="response"></a><span data-ttu-id="c42fd-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c42fd-149">Response</span></span>

<span data-ttu-id="c42fd-150">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c42fd-150">If successful, this method returns `201 Created` response code and [message](../resources/message.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c42fd-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c42fd-151">Example</span></span>
<span data-ttu-id="c42fd-152">En el ejemplo siguiente se crea un borrador para responder a todos y agrega un comentario y datos adjuntos todo en una **createReplyAll** llamada.</span><span class="sxs-lookup"><span data-stu-id="c42fd-152">The following example creates a draft to reply all, and adds an attachment and comment all in one **createReplyAll** call.</span></span>
##### <a name="request"></a><span data-ttu-id="c42fd-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c42fd-153">Request</span></span>
<span data-ttu-id="c42fd-154">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c42fd-154">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_createreplyall"
}-->
```http
POST https://graph.microsoft.com/beta/me/messages/AAMkADA1MTAAAH5JaKAAA=/createReplyAll
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
    "comment": "if the project gets approved, please take a look at the attached guidelines before you decide on the name." 
}
```

##### <a name="response"></a><span data-ttu-id="c42fd-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c42fd-155">Response</span></span>
<span data-ttu-id="c42fd-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c42fd-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Me/messages/$entity",
  "@odata.id": "https://graph.microsoft.com/beta/users('86b6ceaf-57f7-4278-97c4-4da0a97f6cdb@70559e59-b378-49ea-8e53-07a3a3d27f5b')/messages('AAMkADA1MTAAAH5JKpAAA=')",
  "@odata.etag": "W/\"CQAAABYAAADX8oL1Wa7jQbcPAHouCzswAAAH5/DP\"",
  "id": "AAMkADA1MTAAAH5JKpAAA=",
  "subject": "RE: Let's start a group",
  "body": {
    "contentType": "HTML",
    "content": "<html>\r\n<body dir=\"ltr\">\r\nif the project gets approved, please take a look at the attached guidelines before you decide on the name.\r\n<b>From:</b> Admin<br>\r\n<b>Sent:</b> Tuesday, March 15, 2016 6:36:32 AM<br>\r\n<b>To:</b> Samantha Booth; Randi Welch<br>\r\n<b>Subject:</b> RE: Let's start a group\r\n<div>Samantha, Randi, would you name the group please?\r\n<b>From:</b> Samantha Booth<br>\r\n<b>Sent:</b> Friday, March 4, 2016 12:23:35 AM<br>\r\n<b>To:</b> Admin<br>\r\n<b>Subject:</b> Re: Let's start a group</font>\r\n</body>\r\n</html>"
  },
  "sender": {
    "emailAddress": {
      "name": "Admin",
      "address": "admin@contoso.onmicrosoft.com"
    }
  },
  "from": null,
  "toRecipients": [
    {
      "emailAddress": {
        "name": "Samantha Booth",
        "address": "samanthab@contoso.onmicrosoft.com"
      }
    },
    {
      "emailAddress": {
        "name": "Randi Welch",
        "address": "randiw@contoso.onmicrosoft.com"
      }
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: createReplyAll",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
