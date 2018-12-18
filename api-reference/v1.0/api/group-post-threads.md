---
title: Crear hilo de conversación
description: 'Inicie una nueva conversación de grupo creando primero un hilo de conversación. '
author: dkershaw10
ms.openlocfilehash: e3517c3a933d428a8ba5b719ba72d0967ce1ae71
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27352006"
---
# <a name="create-conversation-thread"></a><span data-ttu-id="cadbd-103">Crear hilo de conversación</span><span class="sxs-lookup"><span data-stu-id="cadbd-103">Create conversation thread</span></span>
<span data-ttu-id="cadbd-104">Inicie una nueva conversación de grupo creando primero un hilo de conversación.</span><span class="sxs-lookup"><span data-stu-id="cadbd-104">Start a new group conversation by first creating a thread.</span></span> 

<span data-ttu-id="cadbd-p101">Se crea una conversación, un hilo de conversación y una publicación en el grupo. Use [responder hilo](conversationthread-reply.md) o [responder publicación](post-reply.md) para agregar publicaciones al hilo.</span><span class="sxs-lookup"><span data-stu-id="cadbd-p101">A new conversation, conversation thread, and post are created in the group. Use [reply thread](conversationthread-reply.md) or [reply post](post-reply.md) to further post to that thread.</span></span>

<span data-ttu-id="cadbd-107">Nota: También puede [iniciar un nuevo hilo en una conversación ya existente](conversation-post-threads.md).</span><span class="sxs-lookup"><span data-stu-id="cadbd-107">Note: You can also [start a new thread in an existing conversation](conversation-post-threads.md).</span></span> 

## <a name="permissions"></a><span data-ttu-id="cadbd-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="cadbd-108">Permissions</span></span>
<span data-ttu-id="cadbd-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cadbd-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cadbd-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cadbd-111">Permission type</span></span>      | <span data-ttu-id="cadbd-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cadbd-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="cadbd-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cadbd-113">Delegated (work or school account)</span></span> | <span data-ttu-id="cadbd-114">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cadbd-114">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="cadbd-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cadbd-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cadbd-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cadbd-116">Not supported.</span></span>    |
|<span data-ttu-id="cadbd-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cadbd-117">Application</span></span> | <span data-ttu-id="cadbd-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cadbd-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="cadbd-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cadbd-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/threads
```
## <a name="request-headers"></a><span data-ttu-id="cadbd-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cadbd-120">Request headers</span></span>
| <span data-ttu-id="cadbd-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cadbd-121">Header</span></span>       | <span data-ttu-id="cadbd-122">Valor</span><span class="sxs-lookup"><span data-stu-id="cadbd-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="cadbd-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="cadbd-123">Authorization</span></span>  | <span data-ttu-id="cadbd-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cadbd-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="cadbd-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="cadbd-126">Content-Type</span></span>  | <span data-ttu-id="cadbd-127">application/json</span><span class="sxs-lookup"><span data-stu-id="cadbd-127">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="cadbd-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cadbd-128">Request body</span></span>
<span data-ttu-id="cadbd-129">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [conversationThread](../resources/conversationthread.md) que contiene un [post](../resources/post.md).</span><span class="sxs-lookup"><span data-stu-id="cadbd-129">In the request body, supply a JSON representation of [conversationThread](../resources/conversationthread.md) object containing a [post](../resources/post.md).</span></span>

## <a name="response"></a><span data-ttu-id="cadbd-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cadbd-130">Response</span></span>
<span data-ttu-id="cadbd-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [conversationThread](../resources/conversationthread.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cadbd-131">If successful, this method returns `201 Created` response code and [conversationThread](../resources/conversationthread.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cadbd-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cadbd-132">Example</span></span>
#### <a name="request"></a><span data-ttu-id="cadbd-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cadbd-133">Request</span></span>
<span data-ttu-id="cadbd-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cadbd-134">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_conversationthread_from_group"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/threads
Content-type: application/json

{
  "topic": "New Conversation Thread Topic",
  "posts": [{
    "body": {
      "contentType": "html",
      "content": "this is body content"
    },
    "newParticipants": [{
      "emailAddress": {
        "name": "Alex Darrow",
        "address": "alexd@contoso.com"
      }
    }]
  }]
}
```
#### <a name="response"></a><span data-ttu-id="cadbd-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cadbd-135">Response</span></span>
<span data-ttu-id="cadbd-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cadbd-136">The following is an example of the response.</span></span>
><span data-ttu-id="cadbd-137">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="cadbd-137">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="cadbd-138">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cadbd-138">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversationThread"
} -->
```http
HTTP/1.1 201 OK
Content-type: application/json
Content-length: 419

{
  "toRecipients": [
    {
      "emailAddress": {
        "name": "name-value",
        "address": "address-value"
      }
    }
  ],
  "topic": "topic-value",
  "hasAttachments": true,
  "lastDeliveredDateTime": "datetime-value",
  "uniqueSenders": [
    "uniqueSenders-value"
  ],
  "ccRecipients": [
    {
      "emailAddress": {
        "name": "name-value",
        "address": "address-value"
      }
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create thread",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
