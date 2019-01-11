---
title: 'post: reply'
description: 'Responda a una publicación y agregue una nueva publicación al hilo especificado de una conversación de grupo. Puede especificar '
author: dkershaw10
localization_priority: Normal
ms.openlocfilehash: f4692680833b45e0b2542a7d55c5bda3a861af07
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27814822"
---
# <a name="post-reply"></a><span data-ttu-id="0cbc0-104">post: reply</span><span class="sxs-lookup"><span data-stu-id="0cbc0-104">post: reply</span></span>

<span data-ttu-id="0cbc0-p102">Responde a una publicación y agrega una nueva publicación al hilo especificado de una conversación de grupo. Puede especificar la conversación y el hilo primarios en la solicitud, o bien, especificar solo el hilo primario sin la conversación primaria.</span><span class="sxs-lookup"><span data-stu-id="0cbc0-p102">Reply to a post and add a new post to the specified thread in a group conversation. You can specify both the parent conversation and thread in the request, or, you can specify just the parent thread without the parent conversation.</span></span>

## <a name="permissions"></a><span data-ttu-id="0cbc0-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="0cbc0-107">Permissions</span></span>
<span data-ttu-id="0cbc0-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0cbc0-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0cbc0-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0cbc0-110">Permission type</span></span>      | <span data-ttu-id="0cbc0-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0cbc0-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0cbc0-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0cbc0-112">Delegated (work or school account)</span></span> | <span data-ttu-id="0cbc0-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0cbc0-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="0cbc0-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0cbc0-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0cbc0-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0cbc0-115">Not supported.</span></span>    |
|<span data-ttu-id="0cbc0-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0cbc0-116">Application</span></span> | <span data-ttu-id="0cbc0-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0cbc0-117">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="0cbc0-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0cbc0-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/threads/{id}/posts/{id}/reply
POST /groups/{id}/conversations/{id}/threads/{id}/posts/{id}/reply

```
## <a name="request-headers"></a><span data-ttu-id="0cbc0-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0cbc0-119">Request headers</span></span>
| <span data-ttu-id="0cbc0-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0cbc0-120">Header</span></span>       | <span data-ttu-id="0cbc0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="0cbc0-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="0cbc0-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="0cbc0-122">Authorization</span></span>  | <span data-ttu-id="0cbc0-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0cbc0-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="0cbc0-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0cbc0-125">Request body</span></span>
<span data-ttu-id="0cbc0-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="0cbc0-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="0cbc0-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="0cbc0-127">Parameter</span></span>    | <span data-ttu-id="0cbc0-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="0cbc0-128">Type</span></span>   |<span data-ttu-id="0cbc0-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="0cbc0-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0cbc0-130">post</span><span class="sxs-lookup"><span data-stu-id="0cbc0-130">post</span></span>|[<span data-ttu-id="0cbc0-131">post</span><span class="sxs-lookup"><span data-stu-id="0cbc0-131">post</span></span>](../resources/post.md)|<span data-ttu-id="0cbc0-132">La nueva publicación con que se responde.</span><span class="sxs-lookup"><span data-stu-id="0cbc0-132">The new post that is being replied with.</span></span>|

## <a name="response"></a><span data-ttu-id="0cbc0-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0cbc0-133">Response</span></span>

<span data-ttu-id="0cbc0-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0cbc0-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0cbc0-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0cbc0-136">Example</span></span>
<span data-ttu-id="0cbc0-137">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="0cbc0-137">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="0cbc0-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0cbc0-138">Request</span></span>
<span data-ttu-id="0cbc0-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0cbc0-139">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="0cbc0-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0cbc0-140">Response</span></span>
<span data-ttu-id="0cbc0-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0cbc0-141">Here is an example of the response.</span></span>
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
