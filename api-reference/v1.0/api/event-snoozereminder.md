---
title: 'event: snoozeReminder'
description: Posponer un aviso para un evento en un calendario de usuario hasta una nueva hora.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: d3f8ffab576182f5e67dad49e34c67d886fe0bde
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27932416"
---
# <a name="event-snoozereminder"></a><span data-ttu-id="dac95-103">event: snoozeReminder</span><span class="sxs-lookup"><span data-stu-id="dac95-103">event: snoozeReminder</span></span>

<span data-ttu-id="dac95-104">Posponer un aviso para un [evento](../resources/event.md) en un [calendario](../resources/calendar.md) de usuario hasta una nueva hora.</span><span class="sxs-lookup"><span data-stu-id="dac95-104">Postpone a reminder for an [event](../resources/event.md) in a user [calendar](../resources/calendar.md) until a new time.</span></span>

## <a name="permissions"></a><span data-ttu-id="dac95-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="dac95-105">Permissions</span></span>
<span data-ttu-id="dac95-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dac95-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dac95-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dac95-108">Permission type</span></span>      | <span data-ttu-id="dac95-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dac95-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="dac95-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dac95-110">Delegated (work or school account)</span></span> | <span data-ttu-id="dac95-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="dac95-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="dac95-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dac95-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dac95-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="dac95-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="dac95-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dac95-114">Application</span></span> | <span data-ttu-id="dac95-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="dac95-115">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="dac95-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dac95-116">HTTP request</span></span>
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
## <a name="request-headers"></a><span data-ttu-id="dac95-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dac95-117">Request headers</span></span>
| <span data-ttu-id="dac95-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="dac95-118">Name</span></span>       | <span data-ttu-id="dac95-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="dac95-119">Type</span></span> | <span data-ttu-id="dac95-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="dac95-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="dac95-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="dac95-121">Authorization</span></span>  | <span data-ttu-id="dac95-122">string</span><span class="sxs-lookup"><span data-stu-id="dac95-122">string</span></span>  | <span data-ttu-id="dac95-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dac95-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="dac95-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="dac95-125">Content-Type</span></span> | <span data-ttu-id="dac95-126">string</span><span class="sxs-lookup"><span data-stu-id="dac95-126">string</span></span>  | <span data-ttu-id="dac95-p103">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dac95-p103">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="dac95-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dac95-129">Request body</span></span>
<span data-ttu-id="dac95-130">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="dac95-130">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="dac95-131">Parámetro</span><span class="sxs-lookup"><span data-stu-id="dac95-131">Parameter</span></span>    | <span data-ttu-id="dac95-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="dac95-132">Type</span></span>   |<span data-ttu-id="dac95-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="dac95-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="dac95-134">newReminderTime</span><span class="sxs-lookup"><span data-stu-id="dac95-134">newReminderTime</span></span>|<span data-ttu-id="dac95-135">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="dac95-135">DateTimeTimeZone</span></span>|<span data-ttu-id="dac95-136">Nueva fecha y hora para desencadenar el aviso.</span><span class="sxs-lookup"><span data-stu-id="dac95-136">The new date and time to trigger the reminder.</span></span>|

## <a name="response"></a><span data-ttu-id="dac95-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dac95-137">Response</span></span>

<span data-ttu-id="dac95-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dac95-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="dac95-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dac95-140">Example</span></span>
<span data-ttu-id="dac95-141">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="dac95-141">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="dac95-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dac95-142">Request</span></span>
<span data-ttu-id="dac95-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dac95-143">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "event_snoozereminder"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/events/{id}/snoozeReminder
Content-type: application/json
Content-length: 97

{
  "newReminderTime": {
    "dateTime": "dateTime-value",
    "timeZone": "timeZone-value"
  }
}
```

##### <a name="response"></a><span data-ttu-id="dac95-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dac95-144">Response</span></span>
<span data-ttu-id="dac95-145">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dac95-145">Here is an example of the response.</span></span>
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
