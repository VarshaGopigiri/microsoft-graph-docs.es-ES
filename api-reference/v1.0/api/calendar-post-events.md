---
title: Create Event
description: Usa esta API para crear un evento nuevo en el calendario especificado o el predeterminado.
author: angelgolfer-ms
localization_priority: Priority
ms.prod: outlook
ms.openlocfilehash: ea5cc094b3d81c544f4a20cfffc1771b417999ac
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27969404"
---
# <a name="create-event"></a><span data-ttu-id="5cc13-103">Create Event</span><span class="sxs-lookup"><span data-stu-id="5cc13-103">Create Event</span></span>

<span data-ttu-id="5cc13-104">Usa esta API para crear un evento nuevo en el calendario especificado o el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5cc13-104">Use this API to create a new Event in the default or the specified calendar.</span></span>
## <a name="permissions"></a><span data-ttu-id="5cc13-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="5cc13-105">Permissions</span></span>
<span data-ttu-id="5cc13-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5cc13-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5cc13-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5cc13-108">Permission type</span></span>      | <span data-ttu-id="5cc13-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5cc13-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5cc13-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5cc13-110">Delegated (work or school account)</span></span> | <span data-ttu-id="5cc13-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5cc13-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="5cc13-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5cc13-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5cc13-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5cc13-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="5cc13-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5cc13-114">Application</span></span> | <span data-ttu-id="5cc13-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5cc13-115">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="5cc13-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5cc13-116">HTTP request</span></span>
<span data-ttu-id="5cc13-117"><!-- { "blockType": "ignored" } -->Un usuario o del grupo predeterminado de [calendario](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="5cc13-117"><!-- { "blockType": "ignored" } --> A user's or group's default [calendar](../resources/calendar.md).</span></span>
```http
POST /me/calendar/events
POST /users/{id | userPrincipalName}/calendar/events
POST /groups/{id}/calendar/events
```
<span data-ttu-id="5cc13-118">[calendar](../resources/calendar.md) de un usuario del [calendarGroup](../resources/calendargroup.md) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5cc13-118">A user's [calendar](../resources/calendar.md) in the default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
POST /me/calendars/{id}/events
POST /users/{id | userPrincipalName}/calendars/{id}/events

POST /me/calendarGroup/calendars/{id}/events
POST /users/{id | userPrincipalName}/calendarGroup/calendars/{id}/events
```
<span data-ttu-id="5cc13-119">[calendar](../resources/calendar.md) de un usuario de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="5cc13-119">A user's [calendar](../resources/calendar.md) in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
```http
POST /me/calendarGroups/{id}/calendars/{id}/events
POST /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}/events
```
## <a name="request-headers"></a><span data-ttu-id="5cc13-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5cc13-120">Request headers</span></span>
| <span data-ttu-id="5cc13-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5cc13-121">Header</span></span>       | <span data-ttu-id="5cc13-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5cc13-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="5cc13-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="5cc13-123">Authorization</span></span>  | <span data-ttu-id="5cc13-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5cc13-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="5cc13-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="5cc13-126">Content-Type</span></span>  | <span data-ttu-id="5cc13-p103">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5cc13-p103">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="5cc13-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5cc13-129">Request body</span></span>
<span data-ttu-id="5cc13-130">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="5cc13-130">In the request body, supply a JSON representation of [Event](../resources/event.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="5cc13-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5cc13-131">Response</span></span>

<span data-ttu-id="5cc13-132">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [Event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5cc13-132">If successful, this method returns `201 Created` response code and [Event](../resources/event.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5cc13-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5cc13-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="5cc13-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5cc13-134">Request</span></span>
<span data-ttu-id="5cc13-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5cc13-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_event_from_calendar"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/calendar/events
Content-type: application/json
Content-length: 285

{
  "originalStartTimeZone": "originalStartTimeZone-value",
  "originalEndTimeZone": "originalEndTimeZone-value",
  "responseStatus": {
    "response": "",
    "time": "datetime-value"
  },
  "reminderMinutesBeforeStart": 99,
  "isReminderOn": true
}
```
<span data-ttu-id="5cc13-136">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="5cc13-136">In the request body, supply a JSON representation of [event](../resources/event.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="5cc13-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5cc13-137">Response</span></span>
<span data-ttu-id="5cc13-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5cc13-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
    "time": "datetime-value"
  },
  "iCalUId": "iCalUId-value",
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
