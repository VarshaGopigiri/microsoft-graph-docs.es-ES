---
title: 'message: replyAll'
description: Responde a todos los remitentes de un mensaje. El mensaje se guarda en la carpeta Elementos enviados.
author: angelgolfer-ms
ms.openlocfilehash: cefe4d92d23cb9531f6fa66f74d1c9af87ef429e
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27348989"
---
# <a name="message-replyall"></a><span data-ttu-id="66623-104">message: replyAll</span><span class="sxs-lookup"><span data-stu-id="66623-104">message: replyAll</span></span>

<span data-ttu-id="66623-p102">Responde a todos los remitentes de un mensaje. El mensaje se guarda en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="66623-p102">Reply to all recipients of a message. The message is then saved in the Sent Items folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="66623-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="66623-107">Permissions</span></span>
<span data-ttu-id="66623-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="66623-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="66623-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="66623-110">Permission type</span></span>      | <span data-ttu-id="66623-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="66623-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="66623-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="66623-112">Delegated (work or school account)</span></span> | <span data-ttu-id="66623-113">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="66623-113">Mail.Send</span></span>    |
|<span data-ttu-id="66623-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="66623-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="66623-115">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="66623-115">Mail.Send</span></span>    |
|<span data-ttu-id="66623-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="66623-116">Application</span></span> | <span data-ttu-id="66623-117">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="66623-117">Mail.Send</span></span> |

## <a name="http-request"></a><span data-ttu-id="66623-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="66623-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/me/messages/{id}/replyAll
POST /users/{id | userPrincipalName}/messages/{id}/replyAll
POST /me/mailFolders/{id}/messages/{id}/replyAll
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/replyAll
```
## <a name="request-headers"></a><span data-ttu-id="66623-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="66623-119">Request headers</span></span>
| <span data-ttu-id="66623-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="66623-120">Name</span></span>       | <span data-ttu-id="66623-121">Type</span><span class="sxs-lookup"><span data-stu-id="66623-121">Type</span></span> | <span data-ttu-id="66623-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="66623-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="66623-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="66623-123">Authorization</span></span>  | <span data-ttu-id="66623-124">string</span><span class="sxs-lookup"><span data-stu-id="66623-124">string</span></span>  | <span data-ttu-id="66623-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="66623-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="66623-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="66623-127">Content-Type</span></span> | <span data-ttu-id="66623-128">string</span><span class="sxs-lookup"><span data-stu-id="66623-128">string</span></span>  | <span data-ttu-id="66623-p105">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="66623-p105">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="66623-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="66623-131">Request body</span></span>
<span data-ttu-id="66623-132">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="66623-132">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="66623-133">Parámetro</span><span class="sxs-lookup"><span data-stu-id="66623-133">Parameter</span></span>    | <span data-ttu-id="66623-134">Type</span><span class="sxs-lookup"><span data-stu-id="66623-134">Type</span></span>   |<span data-ttu-id="66623-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="66623-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="66623-136">comment</span><span class="sxs-lookup"><span data-stu-id="66623-136">comment</span></span>|<span data-ttu-id="66623-137">String</span><span class="sxs-lookup"><span data-stu-id="66623-137">String</span></span>|<span data-ttu-id="66623-p106">Comentario que se va a incluir. Puede ser una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="66623-p106">A comment to include. Can be an empty string.</span></span>|

## <a name="response"></a><span data-ttu-id="66623-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="66623-140">Response</span></span>

<span data-ttu-id="66623-p107">Si se ejecuta correctamente, este método devuelve el código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="66623-p107">If successful, this method returns `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="66623-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="66623-143">Example</span></span>
<span data-ttu-id="66623-144">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="66623-144">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="66623-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="66623-145">Request</span></span>
<span data-ttu-id="66623-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="66623-146">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_replyall"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/replyAll
Content-type: application/json
Content-length: 32

{
  "comment": "comment-value"
}
```


##### <a name="response"></a><span data-ttu-id="66623-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="66623-147">Response</span></span>
<span data-ttu-id="66623-148">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="66623-148">Here is an example of the response.</span></span>
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
  "description": "message: replyAll",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
