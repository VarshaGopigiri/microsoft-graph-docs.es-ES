---
title: Crear hilo
description: 'Cree un nuevo hilo en la conversación especificada. '
author: dkershaw10
localization_priority: Normal
ms.openlocfilehash: cd231fd3108d70c0732b61f7f72b64111251d58e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27839917"
---
# <a name="create-thread"></a><span data-ttu-id="7eaf4-103">Crear hilo</span><span class="sxs-lookup"><span data-stu-id="7eaf4-103">Create thread</span></span>

<span data-ttu-id="7eaf4-104">Cree un nuevo hilo en la conversación especificada.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-104">Create a new thread in the specified conversation.</span></span> 

<span data-ttu-id="7eaf4-p101">Se crean un hilo y una publicación como se ha especificado. Use [responder hilo](conversationthread-reply.md) para agregar publicaciones al hilo. O, si tiene el identificador de la publicación, también puede [responder](post-reply.md) a esa publicación en ese hilo.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-p101">A thread and post are created as specified. Use [reply thread](conversationthread-reply.md) to further post to that thread. Or, if you get the post ID, you can also [reply](post-reply.md) to that post in that thread.</span></span>

<span data-ttu-id="7eaf4-108">Nota: También puede [crear primero un hilo para iniciar una nueva conversación](group-post-threads.md).</span><span class="sxs-lookup"><span data-stu-id="7eaf4-108">Note: You can also [start a new conversation by first creating a thread](group-post-threads.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="7eaf4-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="7eaf4-109">Permissions</span></span>
<span data-ttu-id="7eaf4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7eaf4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7eaf4-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7eaf4-112">Permission type</span></span>      | <span data-ttu-id="7eaf4-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7eaf4-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7eaf4-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7eaf4-114">Delegated (work or school account)</span></span> | <span data-ttu-id="7eaf4-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7eaf4-115">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="7eaf4-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7eaf4-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7eaf4-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-117">Not supported.</span></span>    |
|<span data-ttu-id="7eaf4-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7eaf4-118">Application</span></span> | <span data-ttu-id="7eaf4-119">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7eaf4-119">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="7eaf4-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7eaf4-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/conversations/{id}/threads
```
## <a name="request-headers"></a><span data-ttu-id="7eaf4-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7eaf4-121">Request headers</span></span>
| <span data-ttu-id="7eaf4-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="7eaf4-122">Name</span></span>       | <span data-ttu-id="7eaf4-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="7eaf4-123">Type</span></span> | <span data-ttu-id="7eaf4-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="7eaf4-124">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="7eaf4-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="7eaf4-125">Authorization</span></span>  | <span data-ttu-id="7eaf4-126">string</span><span class="sxs-lookup"><span data-stu-id="7eaf4-126">string</span></span>  | <span data-ttu-id="7eaf4-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="7eaf4-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7eaf4-129">Request body</span></span>
<span data-ttu-id="7eaf4-130">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [ConversationThread](../resources/conversationthread.md).</span><span class="sxs-lookup"><span data-stu-id="7eaf4-130">In the request body, supply a JSON representation of [ConversationThread](../resources/conversationthread.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="7eaf4-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7eaf4-131">Response</span></span>

<span data-ttu-id="7eaf4-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [ConversationThread](../resources/conversationthread.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-132">If successful, this method returns `201 Created` response code and [ConversationThread](../resources/conversationthread.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7eaf4-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7eaf4-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7eaf4-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7eaf4-134">Request</span></span>
<span data-ttu-id="7eaf4-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_conversationthread_from_conversation"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/conversations/{id}/threads
Content-type: application/json

{
  "topic": "topic-value",
  "posts": [{
      "body": {
        "contentType": "html",
        "content": "this is body content"
      }
  }]
}
```
<span data-ttu-id="7eaf4-136">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [conversationThread](../resources/conversationthread.md).</span><span class="sxs-lookup"><span data-stu-id="7eaf4-136">In the request body, supply a JSON representation of [conversationThread](../resources/conversationthread.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="7eaf4-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7eaf4-137">Response</span></span>

<span data-ttu-id="7eaf4-p104">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el `id` del nuevo hilo en el cuerpo de la respuesta. Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-p104">If successful, this method returns `201 Created` response code and the `id` of the new thread in the response body. Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversationThread"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 346

{
  "id": "thread-id-value"
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
