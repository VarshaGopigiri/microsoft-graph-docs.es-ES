---
title: 'evento: Cancelar'
description: 'Esta acción permite al organizador de una reunión enviar un mensaje de cancelación y cancelar el evento. '
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 7fe7841ae1f0a7a4d3128177203becbb363073f6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27951203"
---
# <a name="event-cancel"></a><span data-ttu-id="b53be-103">evento: Cancelar</span><span class="sxs-lookup"><span data-stu-id="b53be-103">event: cancel</span></span>

> <span data-ttu-id="b53be-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b53be-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b53be-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b53be-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b53be-106">Esta acción permite al organizador de una reunión enviar un mensaje de cancelación y cancelar el evento.</span><span class="sxs-lookup"><span data-stu-id="b53be-106">This action allows the organizer of a meeting to send a cancellation message and cancel the event.</span></span> 

<span data-ttu-id="b53be-107">La acción mueve el evento a la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="b53be-107">The action moves the event to the Deleted Items folder.</span></span> <span data-ttu-id="b53be-108">El organizador también puede cancelar una repetición de una reunión periódica proporcionando el Id. de evento de repetición.</span><span class="sxs-lookup"><span data-stu-id="b53be-108">The organizer can also cancel an occurrence of a recurring meeting by providing the occurrence event ID.</span></span> <span data-ttu-id="b53be-109">Un asistente que realiza esta acción recibe un error (HTTP 400 Solicitud incorrecta) con el siguiente mensaje de error:</span><span class="sxs-lookup"><span data-stu-id="b53be-109">An attendee calling this action gets an error (HTTP 400 Bad Request), with the following error message:</span></span>

<span data-ttu-id="b53be-110">"Su solicitud no puede completarse.</span><span class="sxs-lookup"><span data-stu-id="b53be-110">"Your request can't be completed.</span></span> <span data-ttu-id="b53be-111">Debe ser un organizador para cancelar una reunión. "</span><span class="sxs-lookup"><span data-stu-id="b53be-111">You need to be an organizer to cancel a meeting."</span></span>

<span data-ttu-id="b53be-112">Esta acción difiere de [Eliminar](event-delete.md) en que **Cancelar** está disponible solo para el organizador y permite que el organizador envíe un mensaje personalizado a los asistentes sobre la cancelación.</span><span class="sxs-lookup"><span data-stu-id="b53be-112">This action differs from [Delete](event-delete.md) in that **Cancel** is available to only the organizer, and lets the organizer send a custom message to the attendees about the cancellation.</span></span>

## <a name="permissions"></a><span data-ttu-id="b53be-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="b53be-113">Permissions</span></span>
<span data-ttu-id="b53be-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b53be-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b53be-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b53be-116">Permission type</span></span>      | <span data-ttu-id="b53be-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b53be-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b53be-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b53be-118">Delegated (work or school account)</span></span> | <span data-ttu-id="b53be-119">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b53be-119">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="b53be-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b53be-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b53be-121">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b53be-121">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="b53be-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b53be-122">Application</span></span> | <span data-ttu-id="b53be-123">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b53be-123">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="b53be-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b53be-124">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/events/{id}/cancel
POST /users/{id | userPrincipalName}/events/{id}/cancel
POST /groups/{id}/events/{id}/cancel

POST /me/calendar/events/{id}/cancel
POST /users/{id | userPrincipalName}/calendar/events/{id}/cancel
POST /groups/{id}/calendar/events/{id}/cancel

POST /me/calendars/{id}/events/{id}/cancel
POST /users/{id | userPrincipalName}/calendars/{id}/events/{id}/cancel

POST /me/calendargroup/calendars/{id}/events/{id}/cancel
POST /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/cancel

POST /me/calendargroups/{id}/calendars/{id}/events/{id}/cancel
POST /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/cancel
```
## <a name="request-headers"></a><span data-ttu-id="b53be-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b53be-125">Request headers</span></span>
| <span data-ttu-id="b53be-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="b53be-126">Name</span></span>       | <span data-ttu-id="b53be-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="b53be-127">Type</span></span> | <span data-ttu-id="b53be-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="b53be-128">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="b53be-129">Autorización</span><span class="sxs-lookup"><span data-stu-id="b53be-129">Authorization</span></span>  | <span data-ttu-id="b53be-130">string</span><span class="sxs-lookup"><span data-stu-id="b53be-130">string</span></span>  | <span data-ttu-id="b53be-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b53be-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="b53be-133">Content-Type</span><span class="sxs-lookup"><span data-stu-id="b53be-133">Content-Type</span></span> | <span data-ttu-id="b53be-134">string</span><span class="sxs-lookup"><span data-stu-id="b53be-134">string</span></span>  | <span data-ttu-id="b53be-p106">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b53be-p106">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b53be-137">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b53be-137">Request body</span></span>
<span data-ttu-id="b53be-138">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="b53be-138">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="b53be-139">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b53be-139">Parameter</span></span>    | <span data-ttu-id="b53be-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="b53be-140">Type</span></span>   |<span data-ttu-id="b53be-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="b53be-141">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b53be-142">comment</span><span class="sxs-lookup"><span data-stu-id="b53be-142">comment</span></span>|<span data-ttu-id="b53be-143">String</span><span class="sxs-lookup"><span data-stu-id="b53be-143">String</span></span>|<span data-ttu-id="b53be-144">Un comentario sobre la cancelación enviado a todos los asistentes.</span><span class="sxs-lookup"><span data-stu-id="b53be-144">A comment about the cancellation sent to all the attendees.</span></span> <span data-ttu-id="b53be-145">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b53be-145">Optional.</span></span>|

## <a name="response"></a><span data-ttu-id="b53be-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b53be-146">Response</span></span>

<span data-ttu-id="b53be-p108">Si se ejecuta correctamente, este método devuelve el código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b53be-p108">If successful, this method returns `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b53be-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b53be-149">Example</span></span>
<span data-ttu-id="b53be-150">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="b53be-150">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="b53be-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b53be-151">Request</span></span>
<span data-ttu-id="b53be-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b53be-152">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "event_cancel"
}-->
```http
POST https://graph.microsoft.com/beta/me/events/{id}/cancel
Content-type: application/json

{
  "Comment": "Cancelling for this week due to all hands"
}
```

##### <a name="response"></a><span data-ttu-id="b53be-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b53be-153">Response</span></span>
<span data-ttu-id="b53be-154">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b53be-154">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 202 Accepted
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "event: cancel",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
