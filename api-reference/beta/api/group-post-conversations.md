---
title: Crear conversación
description: 'Crea una nueva conversación incluyendo un hilo y una publicación. '
ms.openlocfilehash: d7b04e71b4a58c6e1a44931fdf835b5c9770e177
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083945"
---
# <a name="create-conversation"></a><span data-ttu-id="8a503-103">Crear conversación</span><span class="sxs-lookup"><span data-stu-id="8a503-103">Create conversation</span></span>

> <span data-ttu-id="8a503-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8a503-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8a503-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8a503-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8a503-106">Crea una [conversación](../resources/conversation.md) nueva al incluir un hilo y una publicación.</span><span class="sxs-lookup"><span data-stu-id="8a503-106">Create a new [conversation](../resources/conversation.md) by including a thread and a post.</span></span> 

<span data-ttu-id="8a503-107">Use [responder hilo](conversationthread-reply.md) o [responder publicación](post-reply.md) para agregar publicaciones a la conversación.</span><span class="sxs-lookup"><span data-stu-id="8a503-107">Use [reply thread](conversationthread-reply.md) or [reply post](post-reply.md) to further post to that conversation.</span></span>

## <a name="permissions"></a><span data-ttu-id="8a503-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="8a503-108">Permissions</span></span>
<span data-ttu-id="8a503-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8a503-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8a503-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8a503-111">Permission type</span></span>      | <span data-ttu-id="8a503-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8a503-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8a503-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8a503-113">Delegated (work or school account)</span></span> | <span data-ttu-id="8a503-114">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8a503-114">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="8a503-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8a503-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8a503-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8a503-116">Not supported.</span></span>    |
|<span data-ttu-id="8a503-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8a503-117">Application</span></span> | <span data-ttu-id="8a503-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8a503-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="8a503-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8a503-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/conversations
```

## <a name="request-headers"></a><span data-ttu-id="8a503-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8a503-120">Request headers</span></span>
| <span data-ttu-id="8a503-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a503-121">Header</span></span>       | <span data-ttu-id="8a503-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8a503-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="8a503-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="8a503-123">Authorization</span></span>  | <span data-ttu-id="8a503-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8a503-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="8a503-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="8a503-126">Content-Type</span></span>  | <span data-ttu-id="8a503-127">application/json</span><span class="sxs-lookup"><span data-stu-id="8a503-127">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="8a503-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8a503-128">Request body</span></span>
<span data-ttu-id="8a503-129">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [conversation](../resources/conversation.md) que contiene un [conversationThread](../resources/conversationthread.md) y un [post](../resources/post.md).</span><span class="sxs-lookup"><span data-stu-id="8a503-129">In the request body, supply a JSON representation of [conversation](../resources/conversation.md) object containing a [conversationThread](../resources/conversationthread.md) and a [post](../resources/post.md).</span></span>

## <a name="response"></a><span data-ttu-id="8a503-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a503-130">Response</span></span>
<span data-ttu-id="8a503-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [conversation](../resources/conversation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8a503-131">If successful, this method returns `201 Created` response code and [conversation](../resources/conversation.md) object in the response body.</span></span> 

<span data-ttu-id="8a503-132">La respuesta incluye los Id. de la conversación e hilo nuevos, que puede usar en la operación de [publicaciones de lista](conversationthread-list-posts.md) para obtener también la nueva publicación.</span><span class="sxs-lookup"><span data-stu-id="8a503-132">The response includes the IDs for the new conversation and thread, which you can use in the [list posts](conversationthread-list-posts.md) operation to get the new post as well.</span></span>

## <a name="example"></a><span data-ttu-id="8a503-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8a503-133">Example</span></span>
#### <a name="request"></a><span data-ttu-id="8a503-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8a503-134">Request</span></span>
<span data-ttu-id="8a503-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8a503-135">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_conversation_from_group"
}-->
```http
POST https://graph.microsoft.com/beta/groups('29981b6a-0e57-42dc-94c9-cd24f5306196')/conversations
Content-type: application/json

{
    "topic":"New head count",
    "threads":[
        {
            "posts":[
                {
                    "body":{
                        "contentType":"html",
                        "content":"The confirmation will come by the end of the week."
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

#### <a name="response"></a><span data-ttu-id="8a503-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a503-136">Response</span></span>
<span data-ttu-id="8a503-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8a503-137">The following is an example of the response.</span></span>
><span data-ttu-id="8a503-138">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="8a503-138">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="8a503-139">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8a503-139">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversation"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#groups('29981b6a-0e57-42dc-94c9-cd24f5306196')/conversations/$entity",
    "id":"AAQkADPxBgqECsrFDTuM=",
    "threads@odata.context":"https://graph.microsoft.com/beta/$metadata#groups('29981b6a-0e57-42dc-94c9-cd24f5306196')/conversations('AAQkADPxBgqECsrFDTuM%3D')/threads",
    "threads":[
        {
            "id":"AAQkADUNO4xAAMbGA93Sw-EGCoQKysUNO4w=="
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