---
title: 'message: forward'
description: 'Reenviar un mensaje, agregar un comentario o modificar las propiedades actualizables  '
ms.openlocfilehash: 3edb96a90c99f1bc9eb2d8499e9cda83774a7ab3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090752"
---
# <a name="message-forward"></a><span data-ttu-id="f50dc-103">message: forward</span><span class="sxs-lookup"><span data-stu-id="f50dc-103">message: forward</span></span>

> <span data-ttu-id="f50dc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f50dc-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f50dc-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f50dc-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f50dc-106">Reenviar un mensaje, agregar un comentario o modificar las propiedades actualizables</span><span class="sxs-lookup"><span data-stu-id="f50dc-106">Forward a message, add a comment or modify any updateable properties</span></span>  
<span data-ttu-id="f50dc-107">todo en uno **desviar** llamadas.</span><span class="sxs-lookup"><span data-stu-id="f50dc-107">all in one **forward** call.</span></span> <span data-ttu-id="f50dc-108">El mensaje se guarda en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="f50dc-108">The message is saved in the Sent Items folder.</span></span>

<span data-ttu-id="f50dc-109">Como alternativa, puede [crear un borrador de mensaje hacia delante](../api/message-createforward.md) para incluir un comentario o actualizar las propiedades del mensaje y, a continuación, [Enviar](../api/message-send.md) el mensaje de borrador.</span><span class="sxs-lookup"><span data-stu-id="f50dc-109">Alternatively, you can first [create a draft forward message](../api/message-createforward.md) to include a comment or update any message properties, and then [send](../api/message-send.md) the draft message.</span></span>

<span data-ttu-id="f50dc-110">**Nota**</span><span class="sxs-lookup"><span data-stu-id="f50dc-110">**Note**</span></span>

- <span data-ttu-id="f50dc-111">Puede especificar un comentario o la propiedad **body** de la `message` parámetro.</span><span class="sxs-lookup"><span data-stu-id="f50dc-111">You can specify either a comment or the **body** property of the `message` parameter.</span></span> <span data-ttu-id="f50dc-112">Si se especifica tanto devolverá un error HTTP 400 Solicitud incorrecta.</span><span class="sxs-lookup"><span data-stu-id="f50dc-112">Specifying both will return an HTTP 400 Bad Request error.</span></span>
- <span data-ttu-id="f50dc-113">Debe especificar el `toRecipients` parámetro o la propiedad **toRecipients** de la `message` parámetro.</span><span class="sxs-lookup"><span data-stu-id="f50dc-113">You must specify either the `toRecipients` parameter or the **toRecipients** property of the `message` parameter.</span></span> <span data-ttu-id="f50dc-114">Si se especifica tanto o especificar ninguno devolverá un error HTTP 400 Solicitud incorrecta.</span><span class="sxs-lookup"><span data-stu-id="f50dc-114">Specifying both or specifying neither will return an HTTP 400 Bad Request error.</span></span>

## <a name="permissions"></a><span data-ttu-id="f50dc-115">Permisos</span><span class="sxs-lookup"><span data-stu-id="f50dc-115">Permissions</span></span>
<span data-ttu-id="f50dc-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f50dc-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f50dc-118">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f50dc-118">Permission type</span></span>      | <span data-ttu-id="f50dc-119">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f50dc-119">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f50dc-120">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f50dc-120">Delegated (work or school account)</span></span> | <span data-ttu-id="f50dc-121">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="f50dc-121">Mail.Send</span></span>    |
|<span data-ttu-id="f50dc-122">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f50dc-122">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f50dc-123">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="f50dc-123">Mail.Send</span></span>    |
|<span data-ttu-id="f50dc-124">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f50dc-124">Application</span></span> | <span data-ttu-id="f50dc-125">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="f50dc-125">Mail.Send</span></span> |

## <a name="http-request"></a><span data-ttu-id="f50dc-126">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f50dc-126">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/forward
POST /users/{id | userPrincipalName}/messages/{id}/forward
POST /me/mailFolders/{id}/messages/{id}/forward
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/forward
```
## <a name="request-headers"></a><span data-ttu-id="f50dc-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f50dc-127">Request headers</span></span>
| <span data-ttu-id="f50dc-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="f50dc-128">Name</span></span>       | <span data-ttu-id="f50dc-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="f50dc-129">Type</span></span> | <span data-ttu-id="f50dc-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="f50dc-130">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="f50dc-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="f50dc-131">Authorization</span></span>  | <span data-ttu-id="f50dc-132">string</span><span class="sxs-lookup"><span data-stu-id="f50dc-132">string</span></span>  | <span data-ttu-id="f50dc-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f50dc-p106">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="f50dc-135">Content-Type</span><span class="sxs-lookup"><span data-stu-id="f50dc-135">Content-Type</span></span> | <span data-ttu-id="f50dc-136">string</span><span class="sxs-lookup"><span data-stu-id="f50dc-136">string</span></span>  | <span data-ttu-id="f50dc-p107">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f50dc-p107">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f50dc-139">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f50dc-139">Request body</span></span>
<span data-ttu-id="f50dc-140">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="f50dc-140">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="f50dc-141">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f50dc-141">Parameter</span></span>    | <span data-ttu-id="f50dc-142">Tipo</span><span class="sxs-lookup"><span data-stu-id="f50dc-142">Type</span></span>   |<span data-ttu-id="f50dc-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="f50dc-143">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f50dc-144">comment</span><span class="sxs-lookup"><span data-stu-id="f50dc-144">comment</span></span>|<span data-ttu-id="f50dc-145">String</span><span class="sxs-lookup"><span data-stu-id="f50dc-145">String</span></span>|<span data-ttu-id="f50dc-p108">Comentario que se va a incluir. Puede ser una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="f50dc-p108">A comment to include. Can be an empty string.</span></span>|
|<span data-ttu-id="f50dc-148">toRecipients</span><span class="sxs-lookup"><span data-stu-id="f50dc-148">toRecipients</span></span>|<span data-ttu-id="f50dc-149">Colección [recipient](../resources/recipient.md)</span><span class="sxs-lookup"><span data-stu-id="f50dc-149">[recipient](../resources/recipient.md) collection</span></span>|<span data-ttu-id="f50dc-150">La lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="f50dc-150">The list of recipients.</span></span>|
|<span data-ttu-id="f50dc-151">mensaje</span><span class="sxs-lookup"><span data-stu-id="f50dc-151">message</span></span>|[<span data-ttu-id="f50dc-152">message</span><span class="sxs-lookup"><span data-stu-id="f50dc-152">message</span></span>](../resources/message.md)|<span data-ttu-id="f50dc-153">Cualquier propiedad grabable para actualizar en el mensaje de respuesta.</span><span class="sxs-lookup"><span data-stu-id="f50dc-153">Any writeable properties to update in the reply message.</span></span>|

## <a name="response"></a><span data-ttu-id="f50dc-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f50dc-154">Response</span></span>

<span data-ttu-id="f50dc-p109">Si se ejecuta correctamente, este método devuelve el código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f50dc-p109">If successful, this method returns `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f50dc-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f50dc-157">Example</span></span>
<span data-ttu-id="f50dc-158">En el ejemplo siguiente se establece la propiedad **isDeliveryReceiptRequested** en true, se agrega un comentario y reenvía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f50dc-158">The following example sets the **isDeliveryReceiptRequested** property to true, adds a comment and forwards the message.</span></span>
##### <a name="request"></a><span data-ttu-id="f50dc-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f50dc-159">Request</span></span>
<span data-ttu-id="f50dc-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f50dc-160">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_forward"
}-->
```http
POST https://graph.microsoft.com/beta/me/messages/AAMkADA1MTAAAH5JaLAAA=/forward
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
  "comment": "Dana, just want to make sure you get this." 
}
```

##### <a name="response"></a><span data-ttu-id="f50dc-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f50dc-161">Response</span></span>
<span data-ttu-id="f50dc-162">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f50dc-162">Here is an example of the response.</span></span>
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
  "description": "message: forward",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->