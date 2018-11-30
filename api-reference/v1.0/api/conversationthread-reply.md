---
title: 'conversationThread: reply'
description: 'Responder a un subproceso en una conversación en grupo y agregue una nueva entrada a ella. Puede especificar la conversación primario '
ms.openlocfilehash: ca252cb578c0b04cddead455ca046d13180626e4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031169"
---
# <a name="conversationthread-reply"></a><span data-ttu-id="09930-104">conversationThread: reply</span><span class="sxs-lookup"><span data-stu-id="09930-104">conversationThread: reply</span></span>

<span data-ttu-id="09930-p102">Responde a un hilo de una conversación de grupo y agrega una nueva publicación a la misma. Puede especificar la conversación primaria en la solicitud, o bien, especificar solo el hilo sin la conversación primaria.</span><span class="sxs-lookup"><span data-stu-id="09930-p102">Reply to a thread in a group conversation and add a new post to it. You can specify the parent conversation in the request, or, you can specify just the thread without the parent conversation.</span></span>

## <a name="permissions"></a><span data-ttu-id="09930-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="09930-107">Permissions</span></span>
<span data-ttu-id="09930-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="09930-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="09930-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="09930-110">Permission type</span></span>      | <span data-ttu-id="09930-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="09930-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="09930-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="09930-112">Delegated (work or school account)</span></span> | <span data-ttu-id="09930-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="09930-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="09930-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="09930-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="09930-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="09930-115">Not supported.</span></span>    |
|<span data-ttu-id="09930-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="09930-116">Application</span></span> | <span data-ttu-id="09930-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="09930-117">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="09930-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="09930-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/threads/{id}/reply
POST /groups/{id}/conversations/{id}/threads/{id}/reply
```
## <a name="request-headers"></a><span data-ttu-id="09930-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="09930-119">Request headers</span></span>
| <span data-ttu-id="09930-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09930-120">Header</span></span>       | <span data-ttu-id="09930-121">Valor</span><span class="sxs-lookup"><span data-stu-id="09930-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="09930-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="09930-122">Authorization</span></span>  | <span data-ttu-id="09930-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="09930-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="09930-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="09930-125">Content-Type</span></span>  | <span data-ttu-id="09930-p105">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="09930-p105">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="09930-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="09930-128">Request body</span></span>
<span data-ttu-id="09930-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="09930-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="09930-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="09930-130">Parameter</span></span>    | <span data-ttu-id="09930-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="09930-131">Type</span></span>   |<span data-ttu-id="09930-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="09930-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="09930-133">post</span><span class="sxs-lookup"><span data-stu-id="09930-133">post</span></span>|[<span data-ttu-id="09930-134">post</span><span class="sxs-lookup"><span data-stu-id="09930-134">post</span></span>](../resources/post.md)|<span data-ttu-id="09930-135">La nueva publicación con que se responde.</span><span class="sxs-lookup"><span data-stu-id="09930-135">The new post that is being replied with.</span></span>|

## <a name="response"></a><span data-ttu-id="09930-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="09930-136">Response</span></span>

<span data-ttu-id="09930-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="09930-p106">If successful, this method returns `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="09930-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="09930-139">Example</span></span>
<span data-ttu-id="09930-140">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="09930-140">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="09930-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="09930-141">Request</span></span>
<span data-ttu-id="09930-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="09930-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "conversationthread_reply"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/threads/{id}/reply
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

##### <a name="response"></a><span data-ttu-id="09930-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="09930-143">Response</span></span>
<span data-ttu-id="09930-144">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="09930-144">Here is an example of the response.</span></span>
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
