---
title: 'message: createReply'
description: 'Cree un borrador de un mensaje de respuesta para incluir un comentario o actualizar las propiedades de mensaje '
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 27e6aabe05cb732cd40242f3c17c822c920c062e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27943742"
---
# <a name="message-createreply"></a><span data-ttu-id="34958-103">message: createReply</span><span class="sxs-lookup"><span data-stu-id="34958-103">message: createReply</span></span>

> <span data-ttu-id="34958-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="34958-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="34958-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="34958-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="34958-106">Cree un borrador de un mensaje de respuesta para incluir un comentario o actualizar las propiedades de mensaje todo en una sola llamada **createReply** .</span><span class="sxs-lookup"><span data-stu-id="34958-106">Create a draft of a reply message to include a comment or update any message properties all in one **createReply** call.</span></span> <span data-ttu-id="34958-107">A continuación, puede [Actualizar](../api/message-update.md) o [Enviar](../api/message-send.md) el borrador.</span><span class="sxs-lookup"><span data-stu-id="34958-107">You can then [update](../api/message-update.md) or [send](../api/message-send.md) the draft.</span></span>

<span data-ttu-id="34958-108">**Nota**</span><span class="sxs-lookup"><span data-stu-id="34958-108">**Note**</span></span>

- <span data-ttu-id="34958-109">Puede especificar un comentario o la propiedad **body** de la `message` parámetro.</span><span class="sxs-lookup"><span data-stu-id="34958-109">You can specify either a comment or the **body** property of the `message` parameter.</span></span> <span data-ttu-id="34958-110">Si se especifica tanto devolverá un error HTTP 400 Solicitud incorrecta.</span><span class="sxs-lookup"><span data-stu-id="34958-110">Specifying both will return an HTTP 400 Bad Request error.</span></span>
- <span data-ttu-id="34958-111">Si el **origen** se especifica en el mensaje original, por el formato de mensaje de Internet ([RFC 2822](https://www.rfc-editor.org/info/rfc2822)), debe enviar la respuesta a los destinatarios en **replyTo**y no los destinatarios **desde**.</span><span class="sxs-lookup"><span data-stu-id="34958-111">If **replyTo** is specified in the original message, per Internet Message Format ([RFC 2822](https://www.rfc-editor.org/info/rfc2822)), you should send the reply to the recipients in **replyTo**, and not the recipients in **from**.</span></span> 

## <a name="permissions"></a><span data-ttu-id="34958-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="34958-112">Permissions</span></span>
<span data-ttu-id="34958-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="34958-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="34958-115">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="34958-115">Permission type</span></span>      | <span data-ttu-id="34958-116">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="34958-116">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="34958-117">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="34958-117">Delegated (work or school account)</span></span> | <span data-ttu-id="34958-118">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34958-118">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="34958-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="34958-119">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="34958-120">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34958-120">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="34958-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="34958-121">Application</span></span> | <span data-ttu-id="34958-122">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34958-122">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="34958-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="34958-123">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/createReply
POST /users/{id | userPrincipalName}/messages/{id}/createReply
POST /me/mailFolders/{id}/messages/{id}/createReply
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/createReply
```
## <a name="request-headers"></a><span data-ttu-id="34958-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="34958-124">Request headers</span></span>
| <span data-ttu-id="34958-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="34958-125">Name</span></span>       | <span data-ttu-id="34958-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="34958-126">Type</span></span> | <span data-ttu-id="34958-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="34958-127">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="34958-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="34958-128">Authorization</span></span>  | <span data-ttu-id="34958-129">string</span><span class="sxs-lookup"><span data-stu-id="34958-129">string</span></span>  | <span data-ttu-id="34958-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="34958-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="34958-132">Content-Type</span><span class="sxs-lookup"><span data-stu-id="34958-132">Content-Type</span></span> | <span data-ttu-id="34958-133">string</span><span class="sxs-lookup"><span data-stu-id="34958-133">string</span></span>  | <span data-ttu-id="34958-p106">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="34958-p106">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="34958-136">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="34958-136">Request body</span></span>
<span data-ttu-id="34958-137">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="34958-137">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="34958-138">Parámetro</span><span class="sxs-lookup"><span data-stu-id="34958-138">Parameter</span></span>    | <span data-ttu-id="34958-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="34958-139">Type</span></span>   |<span data-ttu-id="34958-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="34958-140">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="34958-141">comment</span><span class="sxs-lookup"><span data-stu-id="34958-141">comment</span></span>|<span data-ttu-id="34958-142">String</span><span class="sxs-lookup"><span data-stu-id="34958-142">String</span></span>|<span data-ttu-id="34958-p107">Comentario que se va a incluir. Puede ser una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="34958-p107">A comment to include. Can be an empty string.</span></span>|
|<span data-ttu-id="34958-145">mensaje</span><span class="sxs-lookup"><span data-stu-id="34958-145">message</span></span>|[<span data-ttu-id="34958-146">message</span><span class="sxs-lookup"><span data-stu-id="34958-146">message</span></span>](../resources/message.md)|<span data-ttu-id="34958-147">Cualquier propiedad grabable para actualizar en el mensaje de respuesta.</span><span class="sxs-lookup"><span data-stu-id="34958-147">Any writeable properties to update in the reply message.</span></span>|

## <a name="response"></a><span data-ttu-id="34958-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34958-148">Response</span></span>

<span data-ttu-id="34958-149">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="34958-149">If successful, this method returns `201 Created` response code and [message](../resources/message.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="34958-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="34958-150">Example</span></span>
<span data-ttu-id="34958-151">En el ejemplo siguiente se crea un borrador de respuesta, se agrega un comentario y un destinatario en el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="34958-151">The following example creates a reply draft, adds a comment and a recipient in the request body.</span></span>
##### <a name="request"></a><span data-ttu-id="34958-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="34958-152">Request</span></span>
<span data-ttu-id="34958-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="34958-153">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_createreply"
}-->
```http
POST https://graph.microsoft.com/beta/me/messages/AAMkADA1MTAAAAqldOAAA=/createReply
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
  "comment": "Samantha, Randi, would you name the group if the project is approved, please?" 
}
```

##### <a name="response"></a><span data-ttu-id="34958-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34958-154">Response</span></span>
<span data-ttu-id="34958-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="34958-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "@odata.id": "https://graph.microsoft.com/beta/users('86b6ceaf-57f7-4278-97c4-4da0a97f6cdb@70559e59-b378-49ea-8e53-07a3a3d27f5b')/messages('AAMkADA1MTAAAH5JKoAAA=')",
  "@odata.etag": "W/\"CQAAABYAAADX8oL1Wa7jQbcPAHouCzswAAAH5/DO\"",
  "id": "AAMkADA1MTAAAH5JKoAAA=",
  "subject": "RE: Let's start a group",
  "Body": {
    "contentType": "HTML",
    "content": "<html>\r\n<body>Samantha, Randi, would you name the group if the project is approved, please?\r\n<b>From:</b> Samantha Booth<br>\r\n<b>Sent:</b> Friday, March 4, 2016 12:23:35 AM<br>\r\n<b>To:</b> Admin<br>\r\n<b>Subject:</b> Re: Let's start a group</font>\r\n<p>That's a great idea!<br>\r\n</body>\r\n</html>"
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
  "description": "message: createReply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
