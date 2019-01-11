---
title: Create Event
description: Usa esta API para crear un evento nuevo en el calendario especificado o el predeterminado.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: 52a8db47af0adb9850d46400b77eb1e997e31fc9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27838853"
---
# <a name="create-event"></a><span data-ttu-id="d8ac2-103">Crear evento</span><span class="sxs-lookup"><span data-stu-id="d8ac2-103">Create Event</span></span>

> <span data-ttu-id="d8ac2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d8ac2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d8ac2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d8ac2-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d8ac2-106">Usa esta API para crear un evento nuevo en el calendario especificado o el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d8ac2-106">Use this API to create a new Event in the default or the specified calendar.</span></span>
## <a name="permissions"></a><span data-ttu-id="d8ac2-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="d8ac2-107">Permissions</span></span>
<span data-ttu-id="d8ac2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d8ac2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d8ac2-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d8ac2-110">Permission type</span></span>      | <span data-ttu-id="d8ac2-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d8ac2-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d8ac2-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d8ac2-112">Delegated (work or school account)</span></span> | <span data-ttu-id="d8ac2-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d8ac2-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="d8ac2-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d8ac2-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d8ac2-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d8ac2-115">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="d8ac2-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d8ac2-116">Application</span></span> | <span data-ttu-id="d8ac2-117">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d8ac2-117">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="d8ac2-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d8ac2-118">HTTP request</span></span>
<span data-ttu-id="d8ac2-119"><!-- { "blockType": "ignored" } -->Un usuario o del grupo predeterminado de [calendario](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="d8ac2-119"><!-- { "blockType": "ignored" } --> A user's or group's default [calendar](../resources/calendar.md).</span></span>
```http
POST /me/calendar/events
POST /users/{id | userPrincipalName}/calendar/events
POST /groups/{id}/calendar/events
```
<span data-ttu-id="d8ac2-120">[calendar](../resources/calendar.md) de un usuario del [calendarGroup](../resources/calendargroup.md) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d8ac2-120">A user's [calendar](../resources/calendar.md) in the default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
POST /me/calendars/{id}/events
POST /users/{id | userPrincipalName}/calendars/{id}/events

POST /me/calendarGroup/calendars/{id}/events
POST /users/{id | userPrincipalName}/calendarGroup/calendars/{id}/events
```
<span data-ttu-id="d8ac2-121">[calendar](../resources/calendar.md) de un usuario de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="d8ac2-121">A user's [calendar](../resources/calendar.md) in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
```http
POST /me/calendarGroups/{id}/calendars/{id}/events
POST /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}/events
```
## <a name="request-headers"></a><span data-ttu-id="d8ac2-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d8ac2-122">Request headers</span></span>
| <span data-ttu-id="d8ac2-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d8ac2-123">Header</span></span>       | <span data-ttu-id="d8ac2-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d8ac2-124">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="d8ac2-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="d8ac2-125">Authorization</span></span>  | <span data-ttu-id="d8ac2-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d8ac2-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="d8ac2-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d8ac2-128">Content-Type</span></span>  | <span data-ttu-id="d8ac2-p104">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d8ac2-p104">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="d8ac2-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d8ac2-131">Request body</span></span>
<span data-ttu-id="d8ac2-132">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="d8ac2-132">In the request body, supply a JSON representation of [Event](../resources/event.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="d8ac2-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d8ac2-133">Response</span></span>

<span data-ttu-id="d8ac2-134">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [Event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d8ac2-134">If successful, this method returns `201 Created` response code and [Event](../resources/event.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d8ac2-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d8ac2-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d8ac2-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d8ac2-136">Request</span></span>
<span data-ttu-id="d8ac2-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d8ac2-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_event_from_calendar"
}-->
```http
POST https://graph.microsoft.com/beta/me/calendar/events
Content-type: application/json
Content-length: 285

{
  "originalStartTimeZone": "originalStartTimeZone-value",
  "originalEndTimeZone": "originalEndTimeZone-value",
  "responseStatus": {
    "response": "",
    "time": "2016-10-19T10:37:00Z"
  },
  "reminderMinutesBeforeStart": 99,
  "isReminderOn": true
}
```
<span data-ttu-id="d8ac2-138">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="d8ac2-138">In the request body, supply a JSON representation of [event](../resources/event.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="d8ac2-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d8ac2-139">Response</span></span>
<span data-ttu-id="d8ac2-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d8ac2-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.event"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 285

{
  "originalStartTimeZone": "originalStartTimeZone-value",
  "originalEndTimeZone": "originalEndTimeZone-value",
  "responseStatus": {
    "response": "",
    "time": "2016-10-19T10:37:00Z"
  },
  "uid": "iCalUId-value",
  "reminderMinutesBeforeStart": 99,
  "isReminderOn": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Event",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
