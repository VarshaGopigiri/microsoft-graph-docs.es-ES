---
title: Crear hilo de conversación
description: 'Inicie una nueva conversación de grupo creando primero un hilo de conversación. '
ms.openlocfilehash: a18c64b976562a609501c6c50c809b4d11e26866
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089292"
---
# <a name="create-conversation-thread"></a><span data-ttu-id="d0779-103">Crear hilo de conversación</span><span class="sxs-lookup"><span data-stu-id="d0779-103">Create conversation thread</span></span>

> <span data-ttu-id="d0779-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d0779-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d0779-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d0779-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d0779-106">Inicie una nueva conversación de grupo creando primero un hilo de conversación.</span><span class="sxs-lookup"><span data-stu-id="d0779-106">Start a new group conversation by first creating a thread.</span></span> 

<span data-ttu-id="d0779-p102">Se crea una conversación, un hilo de conversación y una publicación en el grupo. Use [responder hilo](conversationthread-reply.md) o [responder publicación](post-reply.md) para agregar publicaciones al hilo.</span><span class="sxs-lookup"><span data-stu-id="d0779-p102">A new conversation, conversation thread, and post are created in the group. Use [reply thread](conversationthread-reply.md) or [reply post](post-reply.md) to further post to that thread.</span></span>

<span data-ttu-id="d0779-109">Nota: También puede [iniciar un nuevo hilo en una conversación ya existente](conversation-post-threads.md).</span><span class="sxs-lookup"><span data-stu-id="d0779-109">Note: You can also [start a new thread in an existing conversation](conversation-post-threads.md).</span></span> 

## <a name="permissions"></a><span data-ttu-id="d0779-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="d0779-110">Permissions</span></span>
<span data-ttu-id="d0779-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d0779-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d0779-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d0779-113">Permission type</span></span>      | <span data-ttu-id="d0779-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d0779-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d0779-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d0779-115">Delegated (work or school account)</span></span> | <span data-ttu-id="d0779-116">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d0779-116">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="d0779-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d0779-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d0779-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d0779-118">Not supported.</span></span>    |
|<span data-ttu-id="d0779-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d0779-119">Application</span></span> | <span data-ttu-id="d0779-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d0779-120">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="d0779-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d0779-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/threads
```
## <a name="request-headers"></a><span data-ttu-id="d0779-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d0779-122">Request headers</span></span>
| <span data-ttu-id="d0779-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0779-123">Header</span></span>       | <span data-ttu-id="d0779-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d0779-124">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="d0779-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="d0779-125">Authorization</span></span>  | <span data-ttu-id="d0779-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d0779-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="d0779-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d0779-128">Content-Type</span></span>  | <span data-ttu-id="d0779-129">application/json</span><span class="sxs-lookup"><span data-stu-id="d0779-129">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="d0779-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d0779-130">Request body</span></span>
<span data-ttu-id="d0779-131">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [conversationThread](../resources/conversationthread.md) que contiene un [post](../resources/post.md).</span><span class="sxs-lookup"><span data-stu-id="d0779-131">In the request body, supply a JSON representation of [conversationThread](../resources/conversationthread.md) object containing a [post](../resources/post.md).</span></span>

## <a name="response"></a><span data-ttu-id="d0779-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0779-132">Response</span></span>
<span data-ttu-id="d0779-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [conversationThread](../resources/conversationthread.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0779-133">If successful, this method returns `201 Created` response code and [conversationThread](../resources/conversationthread.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d0779-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0779-134">Example</span></span>
#### <a name="request"></a><span data-ttu-id="d0779-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d0779-135">Request</span></span>
<span data-ttu-id="d0779-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d0779-136">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_conversationthread_from_group"
}-->
```http
POST https://graph.microsoft.com/beta/groups/{id}/threads
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

#### <a name="response"></a><span data-ttu-id="d0779-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0779-137">Response</span></span>
<span data-ttu-id="d0779-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0779-138">The following is an example of the response.</span></span>
><span data-ttu-id="d0779-139">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="d0779-139">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="d0779-140">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d0779-140">All the properties will be returned from an actual call.</span></span>
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
  "lastDeliveredDateTime": "2016-10-19T10:37:00Z",
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
