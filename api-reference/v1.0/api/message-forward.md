---
title: 'message: forward'
description: Reenvía un mensaje. El mensaje se guarda en la carpeta Elementos enviados.
author: angelgolfer-ms
ms.openlocfilehash: fe1b5f9498d8be417818168b83abc56da8986bd1
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27301585"
---
# <a name="message-forward"></a><span data-ttu-id="e9c15-104">message: forward</span><span class="sxs-lookup"><span data-stu-id="e9c15-104">message: forward</span></span>

<span data-ttu-id="e9c15-p102">Reenvía un mensaje. El mensaje se guarda en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="e9c15-p102">Forward a message. The message is saved in the Sent Items folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="e9c15-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="e9c15-107">Permissions</span></span>
<span data-ttu-id="e9c15-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e9c15-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e9c15-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e9c15-110">Permission type</span></span>      | <span data-ttu-id="e9c15-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e9c15-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e9c15-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e9c15-112">Delegated (work or school account)</span></span> | <span data-ttu-id="e9c15-113">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="e9c15-113">Mail.Send</span></span>    |
|<span data-ttu-id="e9c15-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e9c15-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e9c15-115">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="e9c15-115">Mail.Send</span></span>    |
|<span data-ttu-id="e9c15-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e9c15-116">Application</span></span> | <span data-ttu-id="e9c15-117">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="e9c15-117">Mail.Send</span></span> |

## <a name="http-request"></a><span data-ttu-id="e9c15-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e9c15-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/forward
POST /users/{id | userPrincipalName}/messages/{id}/forward
POST /me/mailFolders/{id}/messages/{id}/forward
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/forward
```
## <a name="request-headers"></a><span data-ttu-id="e9c15-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e9c15-119">Request headers</span></span>
| <span data-ttu-id="e9c15-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="e9c15-120">Name</span></span>       | <span data-ttu-id="e9c15-121">Type</span><span class="sxs-lookup"><span data-stu-id="e9c15-121">Type</span></span> | <span data-ttu-id="e9c15-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9c15-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="e9c15-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="e9c15-123">Authorization</span></span>  | <span data-ttu-id="e9c15-124">string</span><span class="sxs-lookup"><span data-stu-id="e9c15-124">string</span></span>  | <span data-ttu-id="e9c15-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e9c15-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="e9c15-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="e9c15-127">Content-Type</span></span> | <span data-ttu-id="e9c15-128">string</span><span class="sxs-lookup"><span data-stu-id="e9c15-128">string</span></span>  | <span data-ttu-id="e9c15-p105">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e9c15-p105">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e9c15-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e9c15-131">Request body</span></span>
<span data-ttu-id="e9c15-132">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="e9c15-132">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="e9c15-133">Parámetro</span><span class="sxs-lookup"><span data-stu-id="e9c15-133">Parameter</span></span>    | <span data-ttu-id="e9c15-134">Type</span><span class="sxs-lookup"><span data-stu-id="e9c15-134">Type</span></span>   |<span data-ttu-id="e9c15-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9c15-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e9c15-136">comment</span><span class="sxs-lookup"><span data-stu-id="e9c15-136">comment</span></span>|<span data-ttu-id="e9c15-137">String</span><span class="sxs-lookup"><span data-stu-id="e9c15-137">String</span></span>|<span data-ttu-id="e9c15-p106">Comentario que se va a incluir. Puede ser una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="e9c15-p106">A comment to include. Can be an empty string.</span></span>|
|<span data-ttu-id="e9c15-140">toRecipients</span><span class="sxs-lookup"><span data-stu-id="e9c15-140">toRecipients</span></span>|<span data-ttu-id="e9c15-141">Colección [Recipient](../resources/recipient.md)</span><span class="sxs-lookup"><span data-stu-id="e9c15-141">[Recipient](../resources/recipient.md) collection</span></span>|<span data-ttu-id="e9c15-142">La lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="e9c15-142">The list of recipients.</span></span>|

## <a name="response"></a><span data-ttu-id="e9c15-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9c15-143">Response</span></span>

<span data-ttu-id="e9c15-p107">Si se ejecuta correctamente, este método devuelve el código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9c15-p107">If successful, this method returns `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e9c15-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e9c15-146">Example</span></span>
<span data-ttu-id="e9c15-147">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="e9c15-147">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="e9c15-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e9c15-148">Request</span></span>
<span data-ttu-id="e9c15-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e9c15-149">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="e9c15-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9c15-150">Response</span></span>
##### <a name="response"></a><span data-ttu-id="e9c15-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9c15-151">Response</span></span>
<span data-ttu-id="e9c15-152">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9c15-152">Here is an example of the response.</span></span>
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
