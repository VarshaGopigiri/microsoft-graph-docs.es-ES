---
title: 'conversationThread: reply'
description: 'Responder a un subproceso en una conversación en grupo y agregue una nueva entrada a ella. Puede especificar la conversación primario '
author: dkershaw10
localization_priority: Normal
ms.openlocfilehash: 60d06a44f942e7c974381f717324c2c5b120454f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27887468"
---
# <a name="conversationthread-reply"></a><span data-ttu-id="de9cc-104">conversationThread: reply</span><span class="sxs-lookup"><span data-stu-id="de9cc-104">conversationThread: reply</span></span>

> <span data-ttu-id="de9cc-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="de9cc-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="de9cc-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="de9cc-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="de9cc-p103">Responde a un hilo de una conversación de grupo y agrega una nueva publicación a la misma. Puede especificar la conversación primaria en la solicitud, o bien, especificar solo el hilo sin la conversación primaria.</span><span class="sxs-lookup"><span data-stu-id="de9cc-p103">Reply to a thread in a group conversation and add a new post to it. You can specify the parent conversation in the request, or, you can specify just the thread without the parent conversation.</span></span>

## <a name="permissions"></a><span data-ttu-id="de9cc-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="de9cc-109">Permissions</span></span>
<span data-ttu-id="de9cc-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="de9cc-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="de9cc-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="de9cc-112">Permission type</span></span>      | <span data-ttu-id="de9cc-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="de9cc-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="de9cc-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="de9cc-114">Delegated (work or school account)</span></span> | <span data-ttu-id="de9cc-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="de9cc-115">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="de9cc-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="de9cc-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="de9cc-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="de9cc-117">Not supported.</span></span>    |
|<span data-ttu-id="de9cc-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="de9cc-118">Application</span></span> | <span data-ttu-id="de9cc-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="de9cc-119">Not supported.</span></span>    |

## <a name="http-request"></a><span data-ttu-id="de9cc-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="de9cc-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/threads/{id}/reply
POST /groups/{id}/conversations/{id}/threads/{id}/reply
```
## <a name="request-headers"></a><span data-ttu-id="de9cc-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="de9cc-121">Request headers</span></span>
| <span data-ttu-id="de9cc-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="de9cc-122">Header</span></span>       | <span data-ttu-id="de9cc-123">Valor</span><span class="sxs-lookup"><span data-stu-id="de9cc-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="de9cc-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="de9cc-124">Authorization</span></span>  | <span data-ttu-id="de9cc-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="de9cc-p105">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="de9cc-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="de9cc-127">Content-Type</span></span>  | <span data-ttu-id="de9cc-p106">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="de9cc-p106">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="de9cc-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="de9cc-130">Request body</span></span>
<span data-ttu-id="de9cc-131">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="de9cc-131">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="de9cc-132">Parámetro</span><span class="sxs-lookup"><span data-stu-id="de9cc-132">Parameter</span></span>    | <span data-ttu-id="de9cc-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="de9cc-133">Type</span></span>   |<span data-ttu-id="de9cc-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="de9cc-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="de9cc-135">post</span><span class="sxs-lookup"><span data-stu-id="de9cc-135">post</span></span>|[<span data-ttu-id="de9cc-136">post</span><span class="sxs-lookup"><span data-stu-id="de9cc-136">post</span></span>](../resources/post.md)|<span data-ttu-id="de9cc-137">La nueva publicación con que se responde.</span><span class="sxs-lookup"><span data-stu-id="de9cc-137">The new post that is being replied with.</span></span>|

## <a name="response"></a><span data-ttu-id="de9cc-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="de9cc-138">Response</span></span>

<span data-ttu-id="de9cc-p107">Si se ejecuta correctamente, este método devuelve el código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="de9cc-p107">If successful, this method returns `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="de9cc-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="de9cc-141">Example</span></span>
<span data-ttu-id="de9cc-142">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="de9cc-142">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="de9cc-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="de9cc-143">Request</span></span>
<span data-ttu-id="de9cc-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="de9cc-144">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "conversationthread_reply"
}-->
```http
POST https://graph.microsoft.com/beta/groups/{id}/threads/{id}/reply
Content-type: application/json
Content-length: 1131

{
  "post": {
    "body": {
      "contentType": "",
      "content": "content-value"
    }
  }
}
```

##### <a name="response"></a><span data-ttu-id="de9cc-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="de9cc-145">Response</span></span>
<span data-ttu-id="de9cc-146">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="de9cc-146">Here is an example of the response.</span></span>
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
  "description": "conversationThread: reply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
