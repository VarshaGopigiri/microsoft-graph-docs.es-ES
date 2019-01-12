---
title: 'event: snoozeReminder'
description: Posponer un aviso para un evento en un calendario de usuario hasta una nueva hora.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 4197a231872341b7ba9c14057e32569b5c0f0c8e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27966079"
---
# <a name="event-snoozereminder"></a><span data-ttu-id="59421-103">event: snoozeReminder</span><span class="sxs-lookup"><span data-stu-id="59421-103">event: snoozeReminder</span></span>

> <span data-ttu-id="59421-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="59421-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="59421-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="59421-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="59421-106">Posponer un aviso para un [evento](../resources/event.md) en un [calendario](../resources/calendar.md) de usuario hasta una nueva hora.</span><span class="sxs-lookup"><span data-stu-id="59421-106">Postpone a reminder for an [event](../resources/event.md) in a user [calendar](../resources/calendar.md) until a new time.</span></span>

## <a name="permissions"></a><span data-ttu-id="59421-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="59421-107">Permissions</span></span>
<span data-ttu-id="59421-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="59421-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="59421-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="59421-110">Permission type</span></span>      | <span data-ttu-id="59421-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="59421-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="59421-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="59421-112">Delegated (work or school account)</span></span> | <span data-ttu-id="59421-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="59421-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="59421-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="59421-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="59421-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="59421-115">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="59421-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="59421-116">Application</span></span> | <span data-ttu-id="59421-117">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="59421-117">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="59421-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="59421-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/events/{id}/snoozeReminder
POST /users/{id | userPrincipalName}/events/{id}/snoozeReminder

POST /me/calendar/events/{id}/snoozeReminder
POST /users/{id | userPrincipalName}/calendar/events/{id}/snoozeReminder

POST /me/calendars/{id}/events/{id}/snoozeReminder
POST /users/{id | userPrincipalName}/calendars/{id}/events/{id}/snoozeReminder

POST /me/calendargroup/calendars/{id}/events/{id}/snoozeReminder
POST /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/snoozeReminder

POST /me/calendargroups/{id}/calendars/{id}/events/{id}/snoozeReminder
POST /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/snoozeReminder
```
## <a name="request-headers"></a><span data-ttu-id="59421-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="59421-119">Request headers</span></span>
| <span data-ttu-id="59421-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="59421-120">Name</span></span>       | <span data-ttu-id="59421-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="59421-121">Type</span></span> | <span data-ttu-id="59421-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="59421-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="59421-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="59421-123">Authorization</span></span>  | <span data-ttu-id="59421-124">string</span><span class="sxs-lookup"><span data-stu-id="59421-124">string</span></span>  | <span data-ttu-id="59421-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="59421-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="59421-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="59421-127">Content-Type</span></span> | <span data-ttu-id="59421-128">string</span><span class="sxs-lookup"><span data-stu-id="59421-128">string</span></span>  | <span data-ttu-id="59421-p104">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="59421-p104">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="59421-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="59421-131">Request body</span></span>
<span data-ttu-id="59421-132">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="59421-132">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="59421-133">Parámetro</span><span class="sxs-lookup"><span data-stu-id="59421-133">Parameter</span></span>    | <span data-ttu-id="59421-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="59421-134">Type</span></span>   |<span data-ttu-id="59421-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="59421-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="59421-136">newReminderTime</span><span class="sxs-lookup"><span data-stu-id="59421-136">newReminderTime</span></span>|<span data-ttu-id="59421-137">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="59421-137">DateTimeTimeZone</span></span>|<span data-ttu-id="59421-138">Nueva fecha y hora para desencadenar el aviso.</span><span class="sxs-lookup"><span data-stu-id="59421-138">The new date and time to trigger the reminder.</span></span>|

## <a name="response"></a><span data-ttu-id="59421-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="59421-139">Response</span></span>

<span data-ttu-id="59421-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="59421-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="59421-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="59421-142">Example</span></span>
<span data-ttu-id="59421-143">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="59421-143">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="59421-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="59421-144">Request</span></span>
<span data-ttu-id="59421-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="59421-145">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "event_snoozereminder"
}-->
```http
POST https://graph.microsoft.com/beta/me/events/{id}/snoozeReminder
Content-type: application/json
Content-length: 97

{
  "newReminderTime": {
    "dateTime": "2016-10-19T10:37:00Z",
    "timeZone": "timeZone-value"
  }
}
```

##### <a name="response"></a><span data-ttu-id="59421-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="59421-146">Response</span></span>
<span data-ttu-id="59421-147">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="59421-147">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "event: snoozeReminder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
