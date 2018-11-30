---
title: 'post: reply'
description: 'Responda a una publicación y agregue una nueva publicación al hilo especificado de una conversación de grupo. Puede especificar '
ms.openlocfilehash: eabee7d41261566401f006c0ff794876f1b2d378
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031141"
---
# <a name="post-reply"></a><span data-ttu-id="020b7-104">post: reply</span><span class="sxs-lookup"><span data-stu-id="020b7-104">post: reply</span></span>

<span data-ttu-id="020b7-p102">Responde a una publicación y agrega una nueva publicación al hilo especificado de una conversación de grupo. Puede especificar la conversación y el hilo primarios en la solicitud, o bien, especificar solo el hilo primario sin la conversación primaria.</span><span class="sxs-lookup"><span data-stu-id="020b7-p102">Reply to a post and add a new post to the specified thread in a group conversation. You can specify both the parent conversation and thread in the request, or, you can specify just the parent thread without the parent conversation.</span></span>

## <a name="permissions"></a><span data-ttu-id="020b7-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="020b7-107">Permissions</span></span>
<span data-ttu-id="020b7-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="020b7-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="020b7-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="020b7-110">Permission type</span></span>      | <span data-ttu-id="020b7-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="020b7-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="020b7-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="020b7-112">Delegated (work or school account)</span></span> | <span data-ttu-id="020b7-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="020b7-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="020b7-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="020b7-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="020b7-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="020b7-115">Not supported.</span></span>    |
|<span data-ttu-id="020b7-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="020b7-116">Application</span></span> | <span data-ttu-id="020b7-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="020b7-117">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="020b7-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="020b7-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/threads/{id}/posts/{id}/reply
POST /groups/{id}/conversations/{id}/threads/{id}/posts/{id}/reply

```
## <a name="request-headers"></a><span data-ttu-id="020b7-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="020b7-119">Request headers</span></span>
| <span data-ttu-id="020b7-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="020b7-120">Header</span></span>       | <span data-ttu-id="020b7-121">Valor</span><span class="sxs-lookup"><span data-stu-id="020b7-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="020b7-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="020b7-122">Authorization</span></span>  | <span data-ttu-id="020b7-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="020b7-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="020b7-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="020b7-125">Request body</span></span>
<span data-ttu-id="020b7-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="020b7-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="020b7-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="020b7-127">Parameter</span></span>    | <span data-ttu-id="020b7-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="020b7-128">Type</span></span>   |<span data-ttu-id="020b7-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="020b7-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="020b7-130">post</span><span class="sxs-lookup"><span data-stu-id="020b7-130">post</span></span>|[<span data-ttu-id="020b7-131">post</span><span class="sxs-lookup"><span data-stu-id="020b7-131">post</span></span>](../resources/post.md)|<span data-ttu-id="020b7-132">La nueva publicación con que se responde.</span><span class="sxs-lookup"><span data-stu-id="020b7-132">The new post that is being replied with.</span></span>|

## <a name="response"></a><span data-ttu-id="020b7-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="020b7-133">Response</span></span>

<span data-ttu-id="020b7-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="020b7-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="020b7-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="020b7-136">Example</span></span>
<span data-ttu-id="020b7-137">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="020b7-137">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="020b7-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="020b7-138">Request</span></span>
<span data-ttu-id="020b7-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="020b7-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "post_reply"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/threads/{id}/posts/{id}/reply
Content-type: application/json
Content-length: 1131

{
  "post": {
    "body": {
      "contentType": "",
      "content": "content-value"
    },
    "receivedDateTime": "datetime-value",
    "hasAttachments": true,
    "from": {
      "emailAddress": {
        "name": "name-value",
        "address": "address-value"
      }
    },
    "sender": {
      "emailAddress": {
        "name": "name-value",
        "address": "address-value"
      }
    },
    "conversationThreadId": "conversationThreadId-value",
    "newParticipants": [
      {
        "emailAddress": {
          "name": "name-value",
          "address": "address-value"
        }
      }
    ],
    "conversationId": "conversationId-value",
    "createdDateTime": "datetime-value",
    "lastModifiedDateTime": "datetime-value",
    "changeKey": "changeKey-value",
    "categories": [
      "categories-value"
    ],
    "id": "id-value",
    "inReplyTo": {
    },
    "attachments": [
      {
        "lastModifiedDateTime": "datetime-value",
        "name": "name-value",
        "contentType": "contentType-value",
        "size": 99,
        "isInline": true,
        "id": "id-value"
      }
    ]
  }
}
```

##### <a name="response"></a><span data-ttu-id="020b7-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="020b7-140">Response</span></span>
<span data-ttu-id="020b7-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="020b7-141">Here is an example of the response.</span></span>
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
  "description": "post: reply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
