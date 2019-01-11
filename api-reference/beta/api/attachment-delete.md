---
title: Eliminar datos adjuntos
description: Eliminar datos adjuntos de un evento del calendario, mensaje, tarea de Outlook o post.
localization_priority: Normal
ms.openlocfilehash: c8af55d2237dd481e89b888d9bc025e6a1093695
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27824944"
---
# <a name="delete-attachment"></a><span data-ttu-id="5afec-103">Eliminar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="5afec-103">Delete attachment</span></span>

> <span data-ttu-id="5afec-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5afec-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5afec-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5afec-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5afec-106">Eliminar datos adjuntos de un [evento](../resources/event.md)del calendario, [mensaje](../resources/message.md), [tarea de Outlook](../resources/outlooktask.md)o [Publicar](../resources/post.md).</span><span class="sxs-lookup"><span data-stu-id="5afec-106">Delete an attachment from a calendar [event](../resources/event.md), [message](../resources/message.md), [Outlook task](../resources/outlooktask.md), or [post](../resources/post.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="5afec-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="5afec-107">Permissions</span></span>

<span data-ttu-id="5afec-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5afec-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

* <span data-ttu-id="5afec-110">Si obtiene acceso a los datos adjuntos en los mensajes: Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5afec-110">If accessing attachments in messages: Mail.ReadWrite</span></span>
* <span data-ttu-id="5afec-111">Si obtiene acceso a los datos adjuntos en eventos: Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5afec-111">If accessing attachments in events: Calendars.ReadWrite</span></span>
* <span data-ttu-id="5afec-112">Si obtiene acceso a los datos adjuntos en las tareas de Outlook: Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5afec-112">If accessing attachments in Outlook tasks: Tasks.ReadWrite</span></span>
* <span data-ttu-id="5afec-113">Si obtiene acceso a los datos adjuntos en entradas de grupo: Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5afec-113">If accessing attachments in group posts: Group.ReadWrite.All</span></span>

<!--
* If accessing attachments in Group Events or Posts: Group.ReadWrite.All
-->

## <a name="http-request"></a><span data-ttu-id="5afec-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5afec-114">HTTP request</span></span>

<span data-ttu-id="5afec-115">Datos adjuntos para un [evento](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="5afec-115">Attachments for an [event](../resources/event.md).</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /me/events/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/events/{id}/attachments/{id}
```

<!--
DELETE /groups/{id}/events/{id}/attachments/{id}
-->

<span data-ttu-id="5afec-116">Datos adjuntos de un [message](../resources/message.md) en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="5afec-116">Attachments for a [message](../resources/message.md) in a user's mailbox.</span></span>
<!-- { "blockType": "ignored" } -->

```http
DELETE /me/messages/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/messages/{id}/attachments/{id}
```

<span data-ttu-id="5afec-117">Datos adjuntos de un [message](../resources/message.md) contenido en una [mailFolder](../resources/mailfolder.md) de nivel superior en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="5afec-117">Attachments for a [message](../resources/message.md) contained in a top level [mailFolder](../resources/mailfolder.md) in a user's mailbox.</span></span>
<!-- { "blockType": "ignored" } -->

```http
DELETE /me/mailFolders/{id}/messages/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/attachments/{id}
```

<span data-ttu-id="5afec-118">Datos adjuntos de un [mensaje de](../resources/message.md) contenidos en una carpeta secundaria de un [mailFolder](../resources/mailfolder.md) en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="5afec-118">Attachments for a [message](../resources/message.md) contained in a child folder of a [mailFolder](../resources/mailfolder.md) in a user's mailbox.</span></span>  <span data-ttu-id="5afec-119">En el ejemplo siguiente se muestra un nivel de anidamiento, pero un mensaje puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="5afec-119">The example below shows one level of nesting, but a message can be located in a child of a child and so on.</span></span>
<!-- { "blockType": "ignored" } -->

```http
DELETE /me/mailFolders/{id}/childFolders/{id}/.../messages/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}/childFolders/{id}/messages/{id}/attachments/{id}
```

<span data-ttu-id="5afec-120">Datos adjuntos para una [tarea de Outlook](../resources/outlooktask.md).</span><span class="sxs-lookup"><span data-stu-id="5afec-120">Attachments for an [Outlook task](../resources/outlooktask.md).</span></span>
<!-- { "blockType": "ignored" } -->

```http
DELETE /me/outlook/tasks/<id>/attachments/{id}
DELETE /users/<id>/outlook/tasks/<id>/attachments/{id}
```

<span data-ttu-id="5afec-121">Datos adjuntos para un [post](../resources/post.md) de un [thread](../resources/conversationthread.md) perteneciente a una [conversation](../resources/conversation.md) de un grupo.</span><span class="sxs-lookup"><span data-stu-id="5afec-121">Attachments for a [post](../resources/post.md) in a [thread](../resources/conversationthread.md) belonging to a [conversation](../resources/conversation.md) of a group.</span></span>
<!-- { "blockType": "ignored" } -->

```http
DELETE /groups/{id}/threads/{id}/posts/{id}/attachments/{id}
DELETE /groups/{id}/conversations/{id}/threads/{id}/posts/{id}/attachments/{id}
```

## <a name="request-headers"></a><span data-ttu-id="5afec-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5afec-122">Request headers</span></span>

| <span data-ttu-id="5afec-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="5afec-123">Name</span></span>       | <span data-ttu-id="5afec-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="5afec-124">Type</span></span> | <span data-ttu-id="5afec-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="5afec-125">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="5afec-126">Autorización</span><span class="sxs-lookup"><span data-stu-id="5afec-126">Authorization</span></span>  | <span data-ttu-id="5afec-127">string</span><span class="sxs-lookup"><span data-stu-id="5afec-127">string</span></span>  | <span data-ttu-id="5afec-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5afec-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="5afec-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5afec-130">Request body</span></span>

<span data-ttu-id="5afec-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5afec-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5afec-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5afec-132">Response</span></span>

<span data-ttu-id="5afec-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5afec-p105">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5afec-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5afec-135">Example</span></span>

### <a name="request"></a><span data-ttu-id="5afec-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5afec-136">Request</span></span>

<span data-ttu-id="5afec-137">Este es un ejemplo de la solicitud para eliminar un archivo adjunto en un evento.</span><span class="sxs-lookup"><span data-stu-id="5afec-137">Here is an example of the request to delete an attachment on an event.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_attachment"
}-->

```http
DELETE https://graph.microsoft.com/beta/me/events/{id}/attachments/{id}
```

### <a name="response"></a><span data-ttu-id="5afec-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5afec-138">Response</span></span>

<span data-ttu-id="5afec-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5afec-139">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->

```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete attachment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
