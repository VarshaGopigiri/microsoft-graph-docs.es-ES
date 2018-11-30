---
title: Eliminar datos adjuntos
description: Eliminar datos adjuntos de un evento de calendario
ms.openlocfilehash: 5e5fe0205e667908947993b01388f90c1688c95e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083721"
---
# <a name="delete-attachment"></a><span data-ttu-id="1b6e8-103">Eliminar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="1b6e8-103">Delete attachment</span></span>

> <span data-ttu-id="1b6e8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1b6e8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1b6e8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1b6e8-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1b6e8-106">Eliminar datos adjuntos de un [evento](../resources/event.md)del calendario, [mensaje](../resources/message.md), [tarea de Outlook](../resources/outlooktask.md)o [Publicar](../resources/post.md).</span><span class="sxs-lookup"><span data-stu-id="1b6e8-106">Delete an attachment from a calendar [event](../resources/event.md), [message](../resources/message.md), [Outlook task](../resources/outlooktask.md), or [post](../resources/post.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="1b6e8-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="1b6e8-107">Permissions</span></span>
<span data-ttu-id="1b6e8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1b6e8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

* <span data-ttu-id="1b6e8-110">Si obtiene acceso a los datos adjuntos en los mensajes: Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1b6e8-110">If accessing attachments in messages: Mail.ReadWrite</span></span>
* <span data-ttu-id="1b6e8-111">Si obtiene acceso a los datos adjuntos en eventos: Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1b6e8-111">If accessing attachments in events: Calendars.ReadWrite</span></span>
* <span data-ttu-id="1b6e8-112">Si obtiene acceso a los datos adjuntos en las tareas de Outlook: Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1b6e8-112">If accessing attachments in Outlook tasks: Tasks.ReadWrite</span></span>
* <span data-ttu-id="1b6e8-113">Si obtiene acceso a los datos adjuntos en entradas de grupo: Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1b6e8-113">If accessing attachments in group posts: Group.ReadWrite.All</span></span>
<!--
* If accessing attachments in Group Events or Posts: Group.ReadWrite.All
-->

## <a name="http-request"></a><span data-ttu-id="1b6e8-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1b6e8-114">HTTP request</span></span>
<span data-ttu-id="1b6e8-115">Los datos adjuntos para un [evento](../resources/event.md) en el usuario de forma predeterminada [calendario](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="1b6e8-115">Attachments for an [event](../resources/event.md) in the user's default [calendar](../resources/calendar.md).</span></span>

<!--
Attachments for an [event](../resources/event.md) in the user's or group's default [calendar](../resources/calendar.md).
-->
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/events/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/events/{id}/attachments/{id}

DELETE /me/calendar/{id}/events/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/calendar/events/{id}/attachments/{id}
```

<!--
DELETE /groups/{id}/events/{id}/attachments/{id}
DELETE /groups/{id}/calendar/events/{id}/attachments/{id}
-->

<span data-ttu-id="1b6e8-116">Datos adjuntos de un [event](../resources/event.md) en un [calendar](../resources/calendar.md) perteneciente al [calendarGroup](../resources/calendargroup.md) predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="1b6e8-116">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to the user's default [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/calendars/{id}/events/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/calendars/{id}/events/{id}/attachments/{id}

DELETE /me/calendargroup/calendars/{id}/events/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/attachments/{id}
```
<span data-ttu-id="1b6e8-117">Datos adjuntos de un [event](../resources/event.md) en un [calendar](../resources/calendar.md) perteneciente al [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="1b6e8-117">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to a user's [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/calendargroups/{id}/calendars/{id}/events/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/attachments/{id}
```
<span data-ttu-id="1b6e8-118">Datos adjuntos de un [message](../resources/message.md) en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="1b6e8-118">Attachments for a [message](../resources/message.md) in a user's mailbox.</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/messages/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/messages/{id}/attachments/{id}
```
<span data-ttu-id="1b6e8-119">Datos adjuntos de un [message](../resources/message.md) contenido en una [mailFolder](../resources/mailfolder.md) de nivel superior en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="1b6e8-119">Attachments for a [message](../resources/message.md) contained in a top level [mailFolder](../resources/mailfolder.md) in a user's mailbox.</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/mailFolders/{id}/messages/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/attachments/{id}
```
<span data-ttu-id="1b6e8-120">Datos adjuntos de un [mensaje de](../resources/message.md) contenidos en una carpeta secundaria de un [mailFolder](../resources/mailfolder.md) en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="1b6e8-120">Attachments for a [message](../resources/message.md) contained in a child folder of a [mailFolder](../resources/mailfolder.md) in a user's mailbox.</span></span>  <span data-ttu-id="1b6e8-121">En el ejemplo siguiente se muestra un nivel de anidamiento, pero un mensaje puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="1b6e8-121">The example below shows one level of nesting, but a message can be located in a child of a child and so on.</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/mailFolders/{id}/childFolders/{id}/.../messages/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}/childFolders/{id}/messages/{id}/attachments/{id}
```

<span data-ttu-id="1b6e8-122">Datos adjuntos para una [tarea de Outlook](../resources/outlooktask.md) en el buzón del usuario, o en un grupo de tareas o la carpeta de la tarea especificada.</span><span class="sxs-lookup"><span data-stu-id="1b6e8-122">Attachments for an [Outlook task](../resources/outlooktask.md) in the user's mailbox, or in a specified task folder or task group.</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/outlook/tasks/<id>/attachments/{id}
DELETE /users/<id>/outlook/tasks/<id>/attachments/{id}

DELETE /me/outlook/taskFolders/<id>/tasks/<id>/attachments/{id}
DELETE /users/<id>/outlook/taskFolders/<id>/tasks/<id>/attachments/{id}

DELETE /me/outlook/taskGroups/<id>/taskFolders/<id>/tasks/<id>/attachments/{id}
DELETE /users/<id>/outlook/taskGroups/<id>/taskFolders/<id>/tasks/<id>/attachments/{id}
```

<span data-ttu-id="1b6e8-123">Datos adjuntos para un [post](../resources/post.md) de un [thread](../resources/conversationthread.md) perteneciente a una [conversation](../resources/conversation.md) de un grupo.</span><span class="sxs-lookup"><span data-stu-id="1b6e8-123">Attachments for a [post](../resources/post.md) in a [thread](../resources/conversationthread.md) belonging to a [conversation](../resources/conversation.md) of a group.</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/threads/{id}/posts/{id}/attachments/{id}
DELETE /groups/{id}/conversations/{id}/threads/{id}/posts/{id}/attachments/{id}
```
## <a name="request-headers"></a><span data-ttu-id="1b6e8-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1b6e8-124">Request headers</span></span>
| <span data-ttu-id="1b6e8-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="1b6e8-125">Name</span></span>       | <span data-ttu-id="1b6e8-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="1b6e8-126">Type</span></span> | <span data-ttu-id="1b6e8-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b6e8-127">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="1b6e8-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="1b6e8-128">Authorization</span></span>  | <span data-ttu-id="1b6e8-129">string</span><span class="sxs-lookup"><span data-stu-id="1b6e8-129">string</span></span>  | <span data-ttu-id="1b6e8-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1b6e8-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="1b6e8-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1b6e8-132">Request body</span></span>
<span data-ttu-id="1b6e8-133">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1b6e8-133">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1b6e8-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1b6e8-134">Response</span></span>

<span data-ttu-id="1b6e8-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1b6e8-p105">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1b6e8-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1b6e8-137">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1b6e8-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1b6e8-138">Request</span></span>
<span data-ttu-id="1b6e8-139">Este es un ejemplo de la solicitud para eliminar un archivo adjunto en un evento.</span><span class="sxs-lookup"><span data-stu-id="1b6e8-139">Here is an example of the request to delete an attachment on an event.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_attachment"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/events/{id}/attachments/{id}
```
##### <a name="response"></a><span data-ttu-id="1b6e8-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1b6e8-140">Response</span></span>
<span data-ttu-id="1b6e8-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1b6e8-141">Here is an example of the response.</span></span>
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
