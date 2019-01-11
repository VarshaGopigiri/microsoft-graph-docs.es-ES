---
title: 'event: snoozeReminder'
description: Posponer un aviso para un evento en un calendario de usuario hasta una nueva hora.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: c432eda53b575e1aaf1b48bfb8f6f38db9693ab6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27821696"
---
# <a name="event-snoozereminder"></a><span data-ttu-id="da7a3-103">event: snoozeReminder</span><span class="sxs-lookup"><span data-stu-id="da7a3-103">event: snoozeReminder</span></span>

<span data-ttu-id="da7a3-104">Posponer un aviso para un [evento](../resources/event.md) en un [calendario](../resources/calendar.md) de usuario hasta una nueva hora.</span><span class="sxs-lookup"><span data-stu-id="da7a3-104">Postpone a reminder for an [event](../resources/event.md) in a user [calendar](../resources/calendar.md) until a new time.</span></span>

## <a name="permissions"></a><span data-ttu-id="da7a3-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="da7a3-105">Permissions</span></span>
<span data-ttu-id="da7a3-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="da7a3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="da7a3-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="da7a3-108">Permission type</span></span>      | <span data-ttu-id="da7a3-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="da7a3-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="da7a3-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="da7a3-110">Delegated (work or school account)</span></span> | <span data-ttu-id="da7a3-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="da7a3-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="da7a3-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="da7a3-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="da7a3-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="da7a3-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="da7a3-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="da7a3-114">Application</span></span> | <span data-ttu-id="da7a3-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="da7a3-115">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="da7a3-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="da7a3-116">HTTP request</span></span>
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
## <a name="request-headers"></a><span data-ttu-id="da7a3-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="da7a3-117">Request headers</span></span>
| <span data-ttu-id="da7a3-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="da7a3-118">Name</span></span>       | <span data-ttu-id="da7a3-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="da7a3-119">Type</span></span> | <span data-ttu-id="da7a3-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="da7a3-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="da7a3-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="da7a3-121">Authorization</span></span>  | <span data-ttu-id="da7a3-122">string</span><span class="sxs-lookup"><span data-stu-id="da7a3-122">string</span></span>  | <span data-ttu-id="da7a3-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="da7a3-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="da7a3-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="da7a3-125">Content-Type</span></span> | <span data-ttu-id="da7a3-126">string</span><span class="sxs-lookup"><span data-stu-id="da7a3-126">string</span></span>  | <span data-ttu-id="da7a3-p103">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="da7a3-p103">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="da7a3-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="da7a3-129">Request body</span></span>
<span data-ttu-id="da7a3-130">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="da7a3-130">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="da7a3-131">Parámetro</span><span class="sxs-lookup"><span data-stu-id="da7a3-131">Parameter</span></span>    | <span data-ttu-id="da7a3-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="da7a3-132">Type</span></span>   |<span data-ttu-id="da7a3-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="da7a3-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="da7a3-134">newReminderTime</span><span class="sxs-lookup"><span data-stu-id="da7a3-134">newReminderTime</span></span>|<span data-ttu-id="da7a3-135">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="da7a3-135">DateTimeTimeZone</span></span>|<span data-ttu-id="da7a3-136">Nueva fecha y hora para desencadenar el aviso.</span><span class="sxs-lookup"><span data-stu-id="da7a3-136">The new date and time to trigger the reminder.</span></span>|

## <a name="response"></a><span data-ttu-id="da7a3-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="da7a3-137">Response</span></span>

<span data-ttu-id="da7a3-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="da7a3-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="da7a3-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="da7a3-140">Example</span></span>
<span data-ttu-id="da7a3-141">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="da7a3-141">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="da7a3-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="da7a3-142">Request</span></span>
<span data-ttu-id="da7a3-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="da7a3-143">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="da7a3-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="da7a3-144">Response</span></span>
<span data-ttu-id="da7a3-145">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="da7a3-145">Here is an example of the response.</span></span>
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
