---
title: Crear hilo
description: Cree un nuevo hilo en la conversación especificada.
ms.openlocfilehash: d545cc8fcc9ac78e9fcda1a7722bb622bf0d72ae
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084025"
---
# <a name="create-thread"></a><span data-ttu-id="6f53f-103">Crear hilo</span><span class="sxs-lookup"><span data-stu-id="6f53f-103">Create thread</span></span>

> <span data-ttu-id="6f53f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6f53f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6f53f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6f53f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6f53f-106">Cree un nuevo hilo en la conversación especificada.</span><span class="sxs-lookup"><span data-stu-id="6f53f-106">Create a new thread in the specified conversation.</span></span>

<span data-ttu-id="6f53f-p102">Se crean un hilo y una publicación como se ha especificado. Use [responder hilo](conversationthread-reply.md) para agregar publicaciones al hilo. O, si tiene el identificador de la publicación, también puede [responder](post-reply.md) a esa publicación en ese hilo.</span><span class="sxs-lookup"><span data-stu-id="6f53f-p102">A thread and post are created as specified. Use [reply thread](conversationthread-reply.md) to further post to that thread. Or, if you get the post ID, you can also [reply](post-reply.md) to that post in that thread.</span></span>

<span data-ttu-id="6f53f-110">Nota: También puede [crear primero un hilo para iniciar una nueva conversación](group-post-threads.md).</span><span class="sxs-lookup"><span data-stu-id="6f53f-110">Note: You can also [start a new conversation by first creating a thread](group-post-threads.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="6f53f-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="6f53f-111">Permissions</span></span>
<span data-ttu-id="6f53f-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6f53f-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6f53f-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6f53f-114">Permission type</span></span>      | <span data-ttu-id="6f53f-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6f53f-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6f53f-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6f53f-116">Delegated (work or school account)</span></span> | <span data-ttu-id="6f53f-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6f53f-117">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="6f53f-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6f53f-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6f53f-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6f53f-119">Not supported.</span></span>    |
|<span data-ttu-id="6f53f-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6f53f-120">Application</span></span> | <span data-ttu-id="6f53f-121">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6f53f-121">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="6f53f-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6f53f-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/conversations/{id}/threads
```
## <a name="request-headers"></a><span data-ttu-id="6f53f-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6f53f-123">Request headers</span></span>
| <span data-ttu-id="6f53f-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="6f53f-124">Name</span></span>       | <span data-ttu-id="6f53f-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="6f53f-125">Type</span></span> | <span data-ttu-id="6f53f-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f53f-126">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="6f53f-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="6f53f-127">Authorization</span></span>  | <span data-ttu-id="6f53f-128">string</span><span class="sxs-lookup"><span data-stu-id="6f53f-128">string</span></span>  | <span data-ttu-id="6f53f-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6f53f-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6f53f-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6f53f-131">Request body</span></span>
<span data-ttu-id="6f53f-132">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [ConversationThread](../resources/conversationthread.md).</span><span class="sxs-lookup"><span data-stu-id="6f53f-132">In the request body, supply a JSON representation of [ConversationThread](../resources/conversationthread.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="6f53f-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f53f-133">Response</span></span>

<span data-ttu-id="6f53f-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [ConversationThread](../resources/conversationthread.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6f53f-134">If successful, this method returns `201 Created` response code and [ConversationThread](../resources/conversationthread.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6f53f-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6f53f-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6f53f-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6f53f-136">Request</span></span>
<span data-ttu-id="6f53f-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6f53f-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_conversationthread_from_conversation"
}-->
```http
POST https://graph.microsoft.com/beta/groups/{id}/conversations/{id}/threads
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
<span data-ttu-id="6f53f-138">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [conversationThread](../resources/conversationthread.md).</span><span class="sxs-lookup"><span data-stu-id="6f53f-138">In the request body, supply a JSON representation of [conversationThread](../resources/conversationthread.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="6f53f-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f53f-139">Response</span></span>

<span data-ttu-id="6f53f-p105">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el `id` del nuevo hilo en el cuerpo de la respuesta. Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6f53f-p105">If successful, this method returns `201 Created` response code and the `id` of the new thread in the response body. Here is an example of the response.</span></span>
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
