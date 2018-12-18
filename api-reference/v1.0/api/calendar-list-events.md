---
title: List events
description: Recupera una lista de eventos de un calendario.  La lista contiene patrones de serie y reuniones de instancia única.
author: angelgolfer-ms
ms.openlocfilehash: d0be013693b387cf94929fe30b31d7672c3c89d2
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27305449"
---
# <a name="list-events"></a><span data-ttu-id="be6dd-104">List events</span><span class="sxs-lookup"><span data-stu-id="be6dd-104">List events</span></span>

<span data-ttu-id="be6dd-p102">Recupera una lista de eventos de un calendario.  La lista contiene patrones de serie y reuniones de instancia única.</span><span class="sxs-lookup"><span data-stu-id="be6dd-p102">Retrieve a list of events in a calendar.  The list contains single instance meetings and series masters.</span></span>

<span data-ttu-id="be6dd-107">Para obtener instancias de evento de expansión, puede [obtener la vista de calendario](calendar-list-calendarview.md) o bien [obtener las instancias de un evento](event-list-instances.md).</span><span class="sxs-lookup"><span data-stu-id="be6dd-107">To get expanded event instances, you can [get the calendar view](calendar-list-calendarview.md), or [get the instances of an event](event-list-instances.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="be6dd-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="be6dd-108">Permissions</span></span>
<span data-ttu-id="be6dd-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="be6dd-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="be6dd-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="be6dd-111">Permission type</span></span>      | <span data-ttu-id="be6dd-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="be6dd-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="be6dd-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="be6dd-113">Delegated (work or school account)</span></span> | <span data-ttu-id="be6dd-114">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="be6dd-114">Calendars.Read</span></span>    |
|<span data-ttu-id="be6dd-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="be6dd-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="be6dd-116">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="be6dd-116">Calendars.Read</span></span>    |
|<span data-ttu-id="be6dd-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="be6dd-117">Application</span></span> | <span data-ttu-id="be6dd-118">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="be6dd-118">Calendars.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="be6dd-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="be6dd-119">HTTP request</span></span>
<span data-ttu-id="be6dd-120"><!-- { "blockType": "ignored" } -->Un usuario o del grupo predeterminado de [calendario](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="be6dd-120"><!-- { "blockType": "ignored" } --> A user's or group's default [calendar](../resources/calendar.md).</span></span>
```http
GET /me/calendar/events
GET /users/{id | userPrincipalName}/calendar/events
GET /groups/{id}/calendar/events
```
<span data-ttu-id="be6dd-121">[calendar](../resources/calendar.md) de un usuario del [calendarGroup](../resources/calendargroup.md) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="be6dd-121">A user's [calendar](../resources/calendar.md) in the default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
GET /me/calendars/{id}/events
GET /users/{id | userPrincipalName}/calendars/{id}/events

GET /me/calendarGroup/calendars/{id}/events
GET /users/{id | userPrincipalName}/calendarGroup/calendars/{id}/events
```
<span data-ttu-id="be6dd-122">[calendar](../resources/calendar.md) de un usuario de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="be6dd-122">A user's [calendar](../resources/calendar.md) in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
```http
GET /me/calendarGroups/{id}/calendars/{id}/events
GET /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}/events
```
## <a name="optional-query-parameters"></a><span data-ttu-id="be6dd-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="be6dd-123">Optional query parameters</span></span>
<span data-ttu-id="be6dd-124">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="be6dd-124">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="be6dd-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="be6dd-125">Request headers</span></span>
| <span data-ttu-id="be6dd-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="be6dd-126">Name</span></span>       | <span data-ttu-id="be6dd-127">Type</span><span class="sxs-lookup"><span data-stu-id="be6dd-127">Type</span></span> | <span data-ttu-id="be6dd-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="be6dd-128">Description</span></span> |
|:---------------|:--------|:--------|
| <span data-ttu-id="be6dd-129">Autorización</span><span class="sxs-lookup"><span data-stu-id="be6dd-129">Authorization</span></span>  | <span data-ttu-id="be6dd-130">string</span><span class="sxs-lookup"><span data-stu-id="be6dd-130">string</span></span> | <span data-ttu-id="be6dd-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="be6dd-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="be6dd-133">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="be6dd-133">Prefer: outlook.timezone</span></span>  | <span data-ttu-id="be6dd-134">string</span><span class="sxs-lookup"><span data-stu-id="be6dd-134">string</span></span> | <span data-ttu-id="be6dd-135">Se usa para especificar la zona horaria de las horas de inicio y final de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="be6dd-135">Use this to specify the time zone for start and end times in the response.</span></span> <span data-ttu-id="be6dd-136">Si no se especifican, estos valores de hora se devuelven en UTC.</span><span class="sxs-lookup"><span data-stu-id="be6dd-136">If not specified, those time values are returned in UTC.</span></span> <span data-ttu-id="be6dd-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="be6dd-137">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="be6dd-138">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="be6dd-138">Request body</span></span>
<span data-ttu-id="be6dd-139">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="be6dd-139">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="be6dd-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="be6dd-140">Response</span></span>

<span data-ttu-id="be6dd-141">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="be6dd-141">If successful, this method returns a `200 OK` response code and collection of [Event](../resources/event.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="be6dd-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="be6dd-142">Example</span></span>
##### <a name="request"></a><span data-ttu-id="be6dd-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="be6dd-143">Request</span></span>
<span data-ttu-id="be6dd-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="be6dd-144">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_events"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendar/events
```
##### <a name="response"></a><span data-ttu-id="be6dd-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="be6dd-145">Response</span></span>
<span data-ttu-id="be6dd-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="be6dd-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.event",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 354

{
  "value": [
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
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List events",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
