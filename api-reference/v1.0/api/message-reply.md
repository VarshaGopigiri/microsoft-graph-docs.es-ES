---
title: 'message: reply'
description: Responde al remitente de un mensaje. El mensaje se guarda en la carpeta Elementos enviados.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: 2ba3df6551aab9138e90fa5e3fc452f2929b4815
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27856326"
---
# <a name="message-reply"></a><span data-ttu-id="a0501-104">message: reply</span><span class="sxs-lookup"><span data-stu-id="a0501-104">message: reply</span></span>

<span data-ttu-id="a0501-p102">Responde al remitente de un mensaje. El mensaje se guarda en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="a0501-p102">Reply to the sender of a message. The message is then saved in the Sent Items folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="a0501-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="a0501-107">Permissions</span></span>
<span data-ttu-id="a0501-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a0501-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a0501-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a0501-110">Permission type</span></span>      | <span data-ttu-id="a0501-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a0501-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a0501-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a0501-112">Delegated (work or school account)</span></span> | <span data-ttu-id="a0501-113">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="a0501-113">Mail.Send</span></span>    |
|<span data-ttu-id="a0501-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a0501-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a0501-115">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="a0501-115">Mail.Send</span></span>    |
|<span data-ttu-id="a0501-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a0501-116">Application</span></span> | <span data-ttu-id="a0501-117">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="a0501-117">Mail.Send</span></span> |

## <a name="http-request"></a><span data-ttu-id="a0501-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a0501-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/reply
POST /users/{id | userPrincipalName}/messages/{id}/reply
POST /me/mailFolders/{id}/messages/{id}/reply
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/reply
```
## <a name="request-headers"></a><span data-ttu-id="a0501-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a0501-119">Request headers</span></span>
| <span data-ttu-id="a0501-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="a0501-120">Name</span></span>       | <span data-ttu-id="a0501-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="a0501-121">Type</span></span> | <span data-ttu-id="a0501-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0501-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="a0501-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="a0501-123">Authorization</span></span>  | <span data-ttu-id="a0501-124">string</span><span class="sxs-lookup"><span data-stu-id="a0501-124">string</span></span>  | <span data-ttu-id="a0501-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a0501-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="a0501-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a0501-127">Content-Type</span></span> | <span data-ttu-id="a0501-128">string</span><span class="sxs-lookup"><span data-stu-id="a0501-128">string</span></span>  | <span data-ttu-id="a0501-p105">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a0501-p105">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a0501-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a0501-131">Request body</span></span>
<span data-ttu-id="a0501-132">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="a0501-132">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="a0501-133">Parámetro</span><span class="sxs-lookup"><span data-stu-id="a0501-133">Parameter</span></span>    | <span data-ttu-id="a0501-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="a0501-134">Type</span></span>   |<span data-ttu-id="a0501-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0501-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a0501-136">comment</span><span class="sxs-lookup"><span data-stu-id="a0501-136">comment</span></span>|<span data-ttu-id="a0501-137">String</span><span class="sxs-lookup"><span data-stu-id="a0501-137">String</span></span>|<span data-ttu-id="a0501-p106">Comentario que se va a incluir. Puede ser una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="a0501-p106">A comment to include. Can be an empty string.</span></span>|

## <a name="response"></a><span data-ttu-id="a0501-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0501-140">Response</span></span>

<span data-ttu-id="a0501-p107">Si se ejecuta correctamente, este método devuelve el código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a0501-p107">If successful, this method returns `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a0501-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a0501-143">Example</span></span>
<span data-ttu-id="a0501-144">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="a0501-144">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="a0501-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a0501-145">Request</span></span>
<span data-ttu-id="a0501-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a0501-146">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_reply"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/reply
Content-type: application/json
Content-length: 32

{
  "comment": "comment-value"
}
```

##### <a name="response"></a><span data-ttu-id="a0501-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0501-147">Response</span></span>
##### <a name="response"></a><span data-ttu-id="a0501-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0501-148">Response</span></span>
<span data-ttu-id="a0501-149">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a0501-149">Here is an example of the response.</span></span>
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
  "description": "message: reply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
