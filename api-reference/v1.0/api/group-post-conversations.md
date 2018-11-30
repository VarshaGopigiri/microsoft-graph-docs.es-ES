---
title: Crear conversación
description: 'Crea una nueva conversación incluyendo un hilo y una publicación. '
ms.openlocfilehash: 7bbfea5f7b083340191d752e436747b898154f59
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030195"
---
# <a name="create-conversation"></a><span data-ttu-id="70c83-103">Crear conversación</span><span class="sxs-lookup"><span data-stu-id="70c83-103">Create conversation</span></span>
<span data-ttu-id="70c83-104">Crea una [conversación](../resources/conversation.md) nueva al incluir un hilo y una publicación.</span><span class="sxs-lookup"><span data-stu-id="70c83-104">Create a new [conversation](../resources/conversation.md) by including a thread and a post.</span></span> 

<span data-ttu-id="70c83-105">Use [responder hilo](conversationthread-reply.md) o [responder publicación](post-reply.md) para agregar publicaciones a la conversación.</span><span class="sxs-lookup"><span data-stu-id="70c83-105">Use [reply thread](conversationthread-reply.md) or [reply post](post-reply.md) to further post to that conversation.</span></span>

## <a name="permissions"></a><span data-ttu-id="70c83-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="70c83-106">Permissions</span></span>
<span data-ttu-id="70c83-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="70c83-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="70c83-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="70c83-109">Permission type</span></span>      | <span data-ttu-id="70c83-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="70c83-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="70c83-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="70c83-111">Delegated (work or school account)</span></span> | <span data-ttu-id="70c83-112">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="70c83-112">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="70c83-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="70c83-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="70c83-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="70c83-114">Not supported.</span></span>    |
|<span data-ttu-id="70c83-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="70c83-115">Application</span></span> | <span data-ttu-id="70c83-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="70c83-116">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="70c83-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="70c83-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/conversations
```

## <a name="request-headers"></a><span data-ttu-id="70c83-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="70c83-118">Request headers</span></span>
| <span data-ttu-id="70c83-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70c83-119">Header</span></span>       | <span data-ttu-id="70c83-120">Valor</span><span class="sxs-lookup"><span data-stu-id="70c83-120">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="70c83-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="70c83-121">Authorization</span></span>  | <span data-ttu-id="70c83-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="70c83-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="70c83-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="70c83-124">Content-Type</span></span>  | <span data-ttu-id="70c83-125">application/json</span><span class="sxs-lookup"><span data-stu-id="70c83-125">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="70c83-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="70c83-126">Request body</span></span>
<span data-ttu-id="70c83-127">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [conversation](../resources/conversation.md) que contiene un [conversationThread](../resources/conversationthread.md) y un [post](../resources/post.md).</span><span class="sxs-lookup"><span data-stu-id="70c83-127">In the request body, supply a JSON representation of [conversation](../resources/conversation.md) object containing a [conversationThread](../resources/conversationthread.md) and a [post](../resources/post.md).</span></span>

## <a name="response"></a><span data-ttu-id="70c83-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="70c83-128">Response</span></span>
<span data-ttu-id="70c83-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [conversation](../resources/conversation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="70c83-129">If successful, this method returns `201 Created` response code and [conversation](../resources/conversation.md) object in the response body.</span></span>

<span data-ttu-id="70c83-130">La respuesta incluye los Id. de la conversación e hilo nuevos, que puede usar en la operación de [publicaciones de lista](conversationthread-list-posts.md) para obtener también la nueva publicación.</span><span class="sxs-lookup"><span data-stu-id="70c83-130">The response includes the IDs for the new conversation and thread, which you can use in the [list posts](conversationthread-list-posts.md) operation to get the new post as well.</span></span>

## <a name="example"></a><span data-ttu-id="70c83-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="70c83-131">Example</span></span>
#### <a name="request"></a><span data-ttu-id="70c83-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="70c83-132">Request</span></span>
<span data-ttu-id="70c83-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="70c83-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["29981b6a-0e57-42dc-94c9-cd24f5306196"],
  "name": "create_conversation_from_group"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/29981b6a-0e57-42dc-94c9-cd24f5306196/conversations
Content-type: application/json

{
    "topic":"New locations for this quarter",
    "threads":[
        {
            "posts":[
                {
                    "body":{
                        "contentType":"html",
                        "content":"What do we know so far?"
                    },
                    "newParticipants":[
                        {
                            "emailAddress":{
                                "name":"Adele Vance",
                                "address":"AdeleV@contoso.onmicrosoft.com"
                            }
                        }
                    ]
                }
            ]
        }
    ]
}
```

#### <a name="response"></a><span data-ttu-id="70c83-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="70c83-134">Response</span></span>
<span data-ttu-id="70c83-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="70c83-135">The following is an example of the response.</span></span>
><span data-ttu-id="70c83-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="70c83-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversation"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups('29981b6a-0e57-42dc-94c9-cd24f5306196')/conversations/$entity",
    "id":"AAQkADDVKtMlRp4Txc6k=",
    "threads@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups('29981b6a-0e57-42dc-94c9-cd24f5306196')/conversations('AAQkADDVKtMlRp4Txc6k%3D')/threads",
    "threads":[
        {
            "id":"AAQkADQDarUNUq0yVGnhPFzqQ=="
        }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Conversation",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->