---
title: 'post: reply'
description: 'Responda a una publicación y agregue una nueva publicación al hilo especificado de una conversación de grupo. Puede especificar '
author: dkershaw10
localization_priority: Normal
ms.prod: groups
ms.openlocfilehash: 681fa62198d2d1e8832b90432e0a76e84722e010
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27944190"
---
# <a name="post-reply"></a><span data-ttu-id="bf9fe-104">post: reply</span><span class="sxs-lookup"><span data-stu-id="bf9fe-104">post: reply</span></span>

> <span data-ttu-id="bf9fe-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bf9fe-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bf9fe-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bf9fe-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="bf9fe-p103">Responde a una publicación y agrega una nueva publicación al hilo especificado de una conversación de grupo. Puede especificar la conversación y el hilo primarios en la solicitud, o bien, especificar solo el hilo primario sin la conversación primaria.</span><span class="sxs-lookup"><span data-stu-id="bf9fe-p103">Reply to a post and add a new post to the specified thread in a group conversation. You can specify both the parent conversation and thread in the request, or, you can specify just the parent thread without the parent conversation.</span></span>

## <a name="permissions"></a><span data-ttu-id="bf9fe-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="bf9fe-109">Permissions</span></span>
<span data-ttu-id="bf9fe-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bf9fe-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bf9fe-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bf9fe-112">Permission type</span></span>      | <span data-ttu-id="bf9fe-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bf9fe-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bf9fe-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bf9fe-114">Delegated (work or school account)</span></span> | <span data-ttu-id="bf9fe-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bf9fe-115">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="bf9fe-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bf9fe-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bf9fe-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bf9fe-117">Not supported.</span></span>    |
|<span data-ttu-id="bf9fe-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bf9fe-118">Application</span></span> | <span data-ttu-id="bf9fe-119">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bf9fe-119">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="bf9fe-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bf9fe-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/threads/{id}/posts/{id}/reply
POST /groups/{id}/conversations/{id}/threads/{id}/posts/{id}/reply

```
## <a name="request-headers"></a><span data-ttu-id="bf9fe-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bf9fe-121">Request headers</span></span>
| <span data-ttu-id="bf9fe-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf9fe-122">Header</span></span>       | <span data-ttu-id="bf9fe-123">Valor</span><span class="sxs-lookup"><span data-stu-id="bf9fe-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="bf9fe-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="bf9fe-124">Authorization</span></span>  | <span data-ttu-id="bf9fe-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bf9fe-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="bf9fe-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bf9fe-127">Request body</span></span>
<span data-ttu-id="bf9fe-128">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="bf9fe-128">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="bf9fe-129">Parámetro</span><span class="sxs-lookup"><span data-stu-id="bf9fe-129">Parameter</span></span>    | <span data-ttu-id="bf9fe-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="bf9fe-130">Type</span></span>   |<span data-ttu-id="bf9fe-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf9fe-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bf9fe-132">post</span><span class="sxs-lookup"><span data-stu-id="bf9fe-132">post</span></span>|[<span data-ttu-id="bf9fe-133">post</span><span class="sxs-lookup"><span data-stu-id="bf9fe-133">post</span></span>](../resources/post.md)|<span data-ttu-id="bf9fe-134">La nueva publicación con que se responde.</span><span class="sxs-lookup"><span data-stu-id="bf9fe-134">The new post that is being replied with.</span></span>|

## <a name="response"></a><span data-ttu-id="bf9fe-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf9fe-135">Response</span></span>

<span data-ttu-id="bf9fe-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bf9fe-p106">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bf9fe-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bf9fe-138">Example</span></span>
<span data-ttu-id="bf9fe-139">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="bf9fe-139">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="bf9fe-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bf9fe-140">Request</span></span>
<span data-ttu-id="bf9fe-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bf9fe-141">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "post_reply"
}-->
```http
POST https://graph.microsoft.com/beta/groups/{id}/threads/{id}/posts/{id}/reply
Content-type: application/json
Content-length: 1131

{
  "post": {
    "body": {
      "contentType": "",
      "content": "content-value"
    },
    "receivedDateTime": "2016-10-19T10:37:00Z",
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
    "createdDateTime": "2016-10-19T10:37:00Z",
    "lastModifiedDateTime": "2016-10-19T10:37:00Z",
    "changeKey": "changeKey-value",
    "categories": [
      "categories-value"
    ],
    "id": "id-value",
    "inReplyTo": {
    },
    "attachments": [
      {
        "lastModifiedDateTime": "2016-10-19T10:37:00Z",
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

##### <a name="response"></a><span data-ttu-id="bf9fe-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf9fe-142">Response</span></span>
##### <a name="response"></a><span data-ttu-id="bf9fe-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf9fe-143">Response</span></span>
<span data-ttu-id="bf9fe-144">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bf9fe-144">Here is an example of the response.</span></span>
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
