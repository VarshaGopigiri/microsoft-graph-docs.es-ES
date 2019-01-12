---
title: 'message: forward'
description: Reenvía un mensaje. El mensaje se guarda en la carpeta Elementos enviados.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 12409685e21b338a86b392f32449b006a0e958f7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27960549"
---
# <a name="message-forward"></a><span data-ttu-id="5e034-104">message: forward</span><span class="sxs-lookup"><span data-stu-id="5e034-104">message: forward</span></span>

<span data-ttu-id="5e034-p102">Reenvía un mensaje. El mensaje se guarda en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="5e034-p102">Forward a message. The message is saved in the Sent Items folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="5e034-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="5e034-107">Permissions</span></span>
<span data-ttu-id="5e034-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5e034-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5e034-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5e034-110">Permission type</span></span>      | <span data-ttu-id="5e034-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5e034-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5e034-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5e034-112">Delegated (work or school account)</span></span> | <span data-ttu-id="5e034-113">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="5e034-113">Mail.Send</span></span>    |
|<span data-ttu-id="5e034-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5e034-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5e034-115">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="5e034-115">Mail.Send</span></span>    |
|<span data-ttu-id="5e034-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5e034-116">Application</span></span> | <span data-ttu-id="5e034-117">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="5e034-117">Mail.Send</span></span> |

## <a name="http-request"></a><span data-ttu-id="5e034-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5e034-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/forward
POST /users/{id | userPrincipalName}/messages/{id}/forward
POST /me/mailFolders/{id}/messages/{id}/forward
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/forward
```
## <a name="request-headers"></a><span data-ttu-id="5e034-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5e034-119">Request headers</span></span>
| <span data-ttu-id="5e034-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="5e034-120">Name</span></span>       | <span data-ttu-id="5e034-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="5e034-121">Type</span></span> | <span data-ttu-id="5e034-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e034-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="5e034-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="5e034-123">Authorization</span></span>  | <span data-ttu-id="5e034-124">string</span><span class="sxs-lookup"><span data-stu-id="5e034-124">string</span></span>  | <span data-ttu-id="5e034-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5e034-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="5e034-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="5e034-127">Content-Type</span></span> | <span data-ttu-id="5e034-128">string</span><span class="sxs-lookup"><span data-stu-id="5e034-128">string</span></span>  | <span data-ttu-id="5e034-p105">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5e034-p105">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="5e034-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5e034-131">Request body</span></span>
<span data-ttu-id="5e034-132">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="5e034-132">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="5e034-133">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5e034-133">Parameter</span></span>    | <span data-ttu-id="5e034-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="5e034-134">Type</span></span>   |<span data-ttu-id="5e034-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e034-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5e034-136">comment</span><span class="sxs-lookup"><span data-stu-id="5e034-136">comment</span></span>|<span data-ttu-id="5e034-137">String</span><span class="sxs-lookup"><span data-stu-id="5e034-137">String</span></span>|<span data-ttu-id="5e034-p106">Comentario que se va a incluir. Puede ser una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="5e034-p106">A comment to include. Can be an empty string.</span></span>|
|<span data-ttu-id="5e034-140">toRecipients</span><span class="sxs-lookup"><span data-stu-id="5e034-140">toRecipients</span></span>|<span data-ttu-id="5e034-141">Colección [Recipient](../resources/recipient.md)</span><span class="sxs-lookup"><span data-stu-id="5e034-141">[Recipient](../resources/recipient.md) collection</span></span>|<span data-ttu-id="5e034-142">La lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="5e034-142">The list of recipients.</span></span>|

## <a name="response"></a><span data-ttu-id="5e034-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5e034-143">Response</span></span>

<span data-ttu-id="5e034-p107">Si se ejecuta correctamente, este método devuelve el código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5e034-p107">If successful, this method returns `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5e034-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5e034-146">Example</span></span>
<span data-ttu-id="5e034-147">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="5e034-147">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="5e034-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5e034-148">Request</span></span>
<span data-ttu-id="5e034-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5e034-149">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_forward"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/forward
Content-type: application/json
Content-length: 166

{
  "comment": "comment-value",
  "toRecipients": [
    {
      "emailAddress": {
        "name": "name-value",
        "address": "address-value"
      }
    }
  ]
}
```

##### <a name="response"></a><span data-ttu-id="5e034-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5e034-150">Response</span></span>
##### <a name="response"></a><span data-ttu-id="5e034-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5e034-151">Response</span></span>
<span data-ttu-id="5e034-152">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5e034-152">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 200 OK
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
