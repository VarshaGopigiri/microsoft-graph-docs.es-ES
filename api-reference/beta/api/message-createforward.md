---
title: 'message: createForward'
description: 'Crear un borrador de mensaje de reenvío para incluir un comentario o actualizar las propiedades de mensaje  '
ms.openlocfilehash: 8e7710871000222d1281a274ee270885097351f9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087086"
---
# <a name="message-createforward"></a><span data-ttu-id="a6f4b-103">message: createForward</span><span class="sxs-lookup"><span data-stu-id="a6f4b-103">message: createForward</span></span>

> <span data-ttu-id="a6f4b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a6f4b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a6f4b-106">Crear un borrador de mensaje de reenvío para incluir un comentario o actualizar las propiedades de mensaje</span><span class="sxs-lookup"><span data-stu-id="a6f4b-106">Create a draft forward message to include a comment or update any message properties</span></span>  
<span data-ttu-id="a6f4b-107">todo en una **createForward** la llamada.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-107">all in one **createForward** call.</span></span> <span data-ttu-id="a6f4b-108">A continuación, puede [Enviar](../api/message-send.md) el mensaje de borrador.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-108">You can then [send](../api/message-send.md) the draft message.</span></span>

<span data-ttu-id="a6f4b-109">**Nota**</span><span class="sxs-lookup"><span data-stu-id="a6f4b-109">**Note**</span></span>

- <span data-ttu-id="a6f4b-110">Puede especificar un comentario o la propiedad **body** de la `message` parámetro.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-110">You can specify either a comment or the **body** property of the `message` parameter.</span></span> <span data-ttu-id="a6f4b-111">Si se especifica tanto devolverá un error HTTP 400 Solicitud incorrecta.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-111">Specifying both will return an HTTP 400 Bad Request error.</span></span>
- <span data-ttu-id="a6f4b-112">Debe especificar el `toRecipients` parámetro o la propiedad **toRecipients** de la `message` parámetro.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-112">You must specify either the `toRecipients` parameter or the **toRecipients** property of the `message` parameter.</span></span> <span data-ttu-id="a6f4b-113">Si se especifica tanto o especificar ninguno devolverá un error HTTP 400 Solicitud incorrecta.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-113">Specifying both or specifying neither will return an HTTP 400 Bad Request error.</span></span>

## <a name="permissions"></a><span data-ttu-id="a6f4b-114">Permisos</span><span class="sxs-lookup"><span data-stu-id="a6f4b-114">Permissions</span></span>
<span data-ttu-id="a6f4b-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a6f4b-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a6f4b-117">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a6f4b-117">Permission type</span></span>      | <span data-ttu-id="a6f4b-118">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a6f4b-118">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a6f4b-119">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a6f4b-119">Delegated (work or school account)</span></span> | <span data-ttu-id="a6f4b-120">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a6f4b-120">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="a6f4b-121">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a6f4b-121">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a6f4b-122">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a6f4b-122">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="a6f4b-123">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a6f4b-123">Application</span></span> | <span data-ttu-id="a6f4b-124">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a6f4b-124">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="a6f4b-125">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a6f4b-125">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/createForward
POST /users/{id | userPrincipalName}/messages/{id}/createForward
POST /me/mailFolders/{id}/messages/{id}/createForward
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/createForward
```
## <a name="request-headers"></a><span data-ttu-id="a6f4b-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a6f4b-126">Request headers</span></span>
| <span data-ttu-id="a6f4b-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="a6f4b-127">Name</span></span>       | <span data-ttu-id="a6f4b-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="a6f4b-128">Type</span></span> | <span data-ttu-id="a6f4b-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6f4b-129">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="a6f4b-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="a6f4b-130">Authorization</span></span>  | <span data-ttu-id="a6f4b-131">string</span><span class="sxs-lookup"><span data-stu-id="a6f4b-131">string</span></span>  | <span data-ttu-id="a6f4b-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-p106">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="a6f4b-134">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a6f4b-134">Content-Type</span></span> | <span data-ttu-id="a6f4b-135">string</span><span class="sxs-lookup"><span data-stu-id="a6f4b-135">string</span></span>  | <span data-ttu-id="a6f4b-p107">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-p107">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a6f4b-138">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a6f4b-138">Request body</span></span>
<span data-ttu-id="a6f4b-139">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-139">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="a6f4b-140">Parámetro</span><span class="sxs-lookup"><span data-stu-id="a6f4b-140">Parameter</span></span>    | <span data-ttu-id="a6f4b-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="a6f4b-141">Type</span></span>   |<span data-ttu-id="a6f4b-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6f4b-142">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a6f4b-143">comment</span><span class="sxs-lookup"><span data-stu-id="a6f4b-143">comment</span></span>|<span data-ttu-id="a6f4b-144">String</span><span class="sxs-lookup"><span data-stu-id="a6f4b-144">String</span></span>|<span data-ttu-id="a6f4b-p108">Comentario que se va a incluir. Puede ser una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-p108">A comment to include. Can be an empty string.</span></span>|
|<span data-ttu-id="a6f4b-147">toRecipients</span><span class="sxs-lookup"><span data-stu-id="a6f4b-147">toRecipients</span></span>|<span data-ttu-id="a6f4b-148">Colección [recipient](../resources/recipient.md)</span><span class="sxs-lookup"><span data-stu-id="a6f4b-148">[recipient](../resources/recipient.md) collection</span></span>|<span data-ttu-id="a6f4b-149">La lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-149">The list of recipients.</span></span>|
|<span data-ttu-id="a6f4b-150">mensaje</span><span class="sxs-lookup"><span data-stu-id="a6f4b-150">message</span></span>|[<span data-ttu-id="a6f4b-151">message</span><span class="sxs-lookup"><span data-stu-id="a6f4b-151">message</span></span>](../resources/message.md)|<span data-ttu-id="a6f4b-152">Cualquier propiedad grabable para actualizar en el mensaje de respuesta.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-152">Any writeable properties to update in the reply message.</span></span>|

## <a name="response"></a><span data-ttu-id="a6f4b-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a6f4b-153">Response</span></span>

<span data-ttu-id="a6f4b-154">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-154">If successful, this method returns `201 Created` response code and [message](../resources/message.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a6f4b-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a6f4b-155">Example</span></span>
<span data-ttu-id="a6f4b-156">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-156">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="a6f4b-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a6f4b-157">Request</span></span>
<span data-ttu-id="a6f4b-158">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-158">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_createforward"
}-->
```http
POST https://graph.microsoft.com/beta/me/messages/AAMkADA1MTAAAH5JaLAAA=/createForward
Content-Type: application/json

{
  "message":{  
    "isDeliveryReceiptRequested": true,
    "toRecipients":[
      {
        "emailAddress": {
          "address":"danas@contoso.onmicrosoft.com",
          "name":"Dana Swope"
        }
      }
     ]
  },
  "comment": "Dana, just want to make sure you get this; you'll need this if the project gets approved." 
}
```

##### <a name="response"></a><span data-ttu-id="a6f4b-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a6f4b-159">Response</span></span>
<span data-ttu-id="a6f4b-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 272

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Me/messages/$entity",
  "@odata.id": "https://graph.microsoft.com/beta/users('86b6ceaf-57f7-4278-97c4-4da0a97f6cdb@70559e59-b378-49ea-8e53-07a3a3d27f5b')/messages('AAMkADA1MTAAAH5JKqAAA=')",
  "@odata.etag": "W/\"CQAAABYAAADX8oL1Wa7jQbcPAHouCzswAAAH5/DQ\"",
  "id": "AAMkADA1MTAAAH5JKqAAA=",
  "subject": "FW: Let's start a group",
  "body": {
    "contentType": "HTML",
    "content": "<html>\r\n<body>\r\nDana, just want to make sure you get this; you'll need this if the project gets approved.\r\n<b>From:</b> Admin<br>\r\n<b>Sent:</b> Tuesday, March 15, 2016 6:47:54 AM<br>\r\n<b>To:</b> Samantha Booth; Randi Welch<br>\r\n<b>Subject:</b> RE: Let's start a group</body>\r\n</html>\r\n"
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
        "name": "Dana Swope",
        "address": "danas@contoso.onmicrosoft.com"
      }
    }
  ]
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