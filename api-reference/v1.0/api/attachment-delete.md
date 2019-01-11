---
title: Eliminar datos adjuntos
description: Elimina datos adjuntos de un evento de calendario, mensaje de correo o publicación de grupo.
localization_priority: Normal
ms.openlocfilehash: f6ac2e60c9fdc8a224e22a49e6928cdc41e9730b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27816999"
---
# <a name="delete-attachment"></a><span data-ttu-id="77494-103">Eliminar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="77494-103">Delete attachment</span></span>

<span data-ttu-id="77494-104">Elimina datos adjuntos de un evento de calendario, mensaje de correo o publicación de grupo.</span><span class="sxs-lookup"><span data-stu-id="77494-104">Delete an attachment from a calendar event, mail message, or group post.</span></span>
## <a name="permissions"></a><span data-ttu-id="77494-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="77494-105">Permissions</span></span>
<span data-ttu-id="77494-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="77494-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

* <span data-ttu-id="77494-108">Si obtiene acceso a los datos adjuntos en los mensajes: Mail.ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="77494-108">If accessing attachments in messages: Mail.ReadWrite.</span></span>
* <span data-ttu-id="77494-109">Si obtiene acceso a los datos adjuntos en eventos: Calendars.ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="77494-109">If accessing attachments in events: Calendars.ReadWrite.</span></span>
* <span data-ttu-id="77494-110">Si obtiene acceso a los datos adjuntos en entradas de grupo: Group.ReadWrite.All.</span><span class="sxs-lookup"><span data-stu-id="77494-110">If accessing attachments in group posts: Group.ReadWrite.All.</span></span>

<!--
* If accessing attachments in Group Events or Posts: Group.ReadWrite.All.
-->

## <a name="http-request"></a><span data-ttu-id="77494-111">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="77494-111">HTTP request</span></span>
<span data-ttu-id="77494-112">Datos adjuntos de un [event](../resources/event.md) en el [calendar](../resources/calendar.md) predeterminado del usuario o del grupo.</span><span class="sxs-lookup"><span data-stu-id="77494-112">Attachments for an [event](../resources/event.md) in the user's or group's default [calendar](../resources/calendar.md).</span></span>
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

<span data-ttu-id="77494-113">Datos adjuntos de un [event](../resources/event.md) en un [calendar](../resources/calendar.md) perteneciente al [calendarGroup](../resources/calendargroup.md) predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="77494-113">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to the user's default [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/calendars/{id}/events/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/calendars/{id}/events/{id}/attachments/{id}

DELETE /me/calendargroup/calendars/{id}/events/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/attachments/{id}
```
<span data-ttu-id="77494-114">Datos adjuntos de un [event](../resources/event.md) en un [calendar](../resources/calendar.md) perteneciente al [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="77494-114">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to a user's [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/calendargroups/{id}/calendars/{id}/events/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/attachments/{id}
```
<span data-ttu-id="77494-115">Datos adjuntos de un [message](../resources/message.md) en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="77494-115">Attachments for a [message](../resources/message.md) in a user's mailbox.</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/messages/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/messages/{id}/attachments/{id}
```
<span data-ttu-id="77494-116">Datos adjuntos de un [message](../resources/message.md) contenido en una [mailFolder](../resources/mailfolder.md) de nivel superior en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="77494-116">Attachments for a [message](../resources/message.md) contained in a top level [mailFolder](../resources/mailfolder.md) in a user's mailbox.</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/mailFolders/{id}/messages/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/attachments/{id}
```
<span data-ttu-id="77494-117">Datos adjuntos de un [mensaje de](../resources/message.md) contenidos en una carpeta secundaria de un [mailFolder](../resources/mailfolder.md) en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="77494-117">Attachments for a [message](../resources/message.md) contained in a child folder of a [mailFolder](../resources/mailfolder.md) in a user's mailbox.</span></span>  <span data-ttu-id="77494-118">En el ejemplo siguiente se muestra un nivel de anidamiento, pero un mensaje puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="77494-118">The example below shows one level of nesting, but a message can be located in a child of a child and so on.</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/mailFolders/{id}/childFolders/{id}/.../messages/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}/childFolders/{id}/messages/{id}/attachments/{id}
```
<span data-ttu-id="77494-119">Datos adjuntos para un [post](../resources/post.md) de un [thread](../resources/conversationthread.md) perteneciente a una [conversation](../resources/conversation.md) de un grupo.</span><span class="sxs-lookup"><span data-stu-id="77494-119">Attachments for a [post](../resources/post.md) in a [thread](../resources/conversationthread.md) belonging to a [conversation](../resources/conversation.md) of a group.</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/threads/{id}/posts/{id}/attachments/{id}
DELETE /groups/{id}/conversations/{id}/threads/{id}/posts/{id}/attachments/{id}
```
## <a name="request-headers"></a><span data-ttu-id="77494-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="77494-120">Request headers</span></span>
| <span data-ttu-id="77494-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="77494-121">Name</span></span>       | <span data-ttu-id="77494-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="77494-122">Type</span></span> | <span data-ttu-id="77494-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="77494-123">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="77494-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="77494-124">Authorization</span></span>  | <span data-ttu-id="77494-125">string</span><span class="sxs-lookup"><span data-stu-id="77494-125">string</span></span>  | <span data-ttu-id="77494-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="77494-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="77494-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="77494-128">Request body</span></span>
<span data-ttu-id="77494-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="77494-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="77494-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77494-130">Response</span></span>

<span data-ttu-id="77494-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77494-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="77494-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="77494-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="77494-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="77494-134">Request</span></span>
<span data-ttu-id="77494-135">Este es un ejemplo de la solicitud para eliminar un archivo adjunto en un evento.</span><span class="sxs-lookup"><span data-stu-id="77494-135">Here is an example of the request to delete an attachment on an event.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_attachment"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/events/{id}/attachments/{id}
```
##### <a name="response"></a><span data-ttu-id="77494-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77494-136">Response</span></span>
<span data-ttu-id="77494-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77494-137">Here is an example of the response.</span></span>
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
