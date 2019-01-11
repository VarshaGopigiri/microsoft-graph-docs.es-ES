---
title: 'message: replyAll'
description: Responde a todos los remitentes de un mensaje. El mensaje se guarda en la carpeta Elementos enviados.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: 8e2d9b2481e4fb0fc4e6e166dae1189baa77b7e5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27884311"
---
# <a name="message-replyall"></a><span data-ttu-id="1cb8e-104">message: replyAll</span><span class="sxs-lookup"><span data-stu-id="1cb8e-104">message: replyAll</span></span>

<span data-ttu-id="1cb8e-p102">Responde a todos los remitentes de un mensaje. El mensaje se guarda en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-p102">Reply to all recipients of a message. The message is then saved in the Sent Items folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="1cb8e-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="1cb8e-107">Permissions</span></span>
<span data-ttu-id="1cb8e-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1cb8e-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1cb8e-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1cb8e-110">Permission type</span></span>      | <span data-ttu-id="1cb8e-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1cb8e-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1cb8e-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1cb8e-112">Delegated (work or school account)</span></span> | <span data-ttu-id="1cb8e-113">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="1cb8e-113">Mail.Send</span></span>    |
|<span data-ttu-id="1cb8e-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1cb8e-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1cb8e-115">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="1cb8e-115">Mail.Send</span></span>    |
|<span data-ttu-id="1cb8e-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1cb8e-116">Application</span></span> | <span data-ttu-id="1cb8e-117">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="1cb8e-117">Mail.Send</span></span> |

## <a name="http-request"></a><span data-ttu-id="1cb8e-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1cb8e-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/me/messages/{id}/replyAll
POST /users/{id | userPrincipalName}/messages/{id}/replyAll
POST /me/mailFolders/{id}/messages/{id}/replyAll
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/replyAll
```
## <a name="request-headers"></a><span data-ttu-id="1cb8e-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1cb8e-119">Request headers</span></span>
| <span data-ttu-id="1cb8e-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="1cb8e-120">Name</span></span>       | <span data-ttu-id="1cb8e-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="1cb8e-121">Type</span></span> | <span data-ttu-id="1cb8e-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="1cb8e-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="1cb8e-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="1cb8e-123">Authorization</span></span>  | <span data-ttu-id="1cb8e-124">string</span><span class="sxs-lookup"><span data-stu-id="1cb8e-124">string</span></span>  | <span data-ttu-id="1cb8e-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="1cb8e-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="1cb8e-127">Content-Type</span></span> | <span data-ttu-id="1cb8e-128">string</span><span class="sxs-lookup"><span data-stu-id="1cb8e-128">string</span></span>  | <span data-ttu-id="1cb8e-p105">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-p105">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="1cb8e-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1cb8e-131">Request body</span></span>
<span data-ttu-id="1cb8e-132">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-132">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="1cb8e-133">Parámetro</span><span class="sxs-lookup"><span data-stu-id="1cb8e-133">Parameter</span></span>    | <span data-ttu-id="1cb8e-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="1cb8e-134">Type</span></span>   |<span data-ttu-id="1cb8e-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="1cb8e-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1cb8e-136">comment</span><span class="sxs-lookup"><span data-stu-id="1cb8e-136">comment</span></span>|<span data-ttu-id="1cb8e-137">String</span><span class="sxs-lookup"><span data-stu-id="1cb8e-137">String</span></span>|<span data-ttu-id="1cb8e-p106">Comentario que se va a incluir. Puede ser una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-p106">A comment to include. Can be an empty string.</span></span>|

## <a name="response"></a><span data-ttu-id="1cb8e-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1cb8e-140">Response</span></span>

<span data-ttu-id="1cb8e-p107">Si se ejecuta correctamente, este método devuelve el código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-p107">If successful, this method returns `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1cb8e-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1cb8e-143">Example</span></span>
<span data-ttu-id="1cb8e-144">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-144">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="1cb8e-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1cb8e-145">Request</span></span>
<span data-ttu-id="1cb8e-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-146">Here is an example of the request.</span></span>
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


##### <a name="response"></a><span data-ttu-id="1cb8e-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1cb8e-147">Response</span></span>
<span data-ttu-id="1cb8e-148">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-148">Here is an example of the response.</span></span>
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
