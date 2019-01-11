---
title: List calendarView
description: Obtenga las repeticiones, excepciones e instancias únicas de eventos en una vista de calendario definida por un intervalo de tiempo,
localization_priority: Priority
ms.openlocfilehash: 48ec49eb5038e7a4c977af0248443e1ca7241cb6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27857704"
---
# <a name="list-calendarview"></a><span data-ttu-id="58e85-103">List calendarView</span><span class="sxs-lookup"><span data-stu-id="58e85-103">List calendarView</span></span>

<span data-ttu-id="58e85-104">Obtiene las repeticiones, excepciones e instancias únicas de eventos en una vista de calendario definida por un intervalo de tiempo del calendario predeterminado `(../me/calendarview)` de un usuario o grupo, o alguno de los otros calendarios del usuario.</span><span class="sxs-lookup"><span data-stu-id="58e85-104">Get the occurrences, exceptions, and single instances of events in a calendar view defined by a time range, from the default calendar `(../me/calendarview)` of a user or group, or some other calendar of the user's.</span></span>

## <a name="permissions"></a><span data-ttu-id="58e85-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="58e85-105">Permissions</span></span>
<span data-ttu-id="58e85-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="58e85-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

* <span data-ttu-id="58e85-108">Eventos en el calendario de un usuario: Calendars.Read o Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="58e85-108">Events in a user's calendar: Calendars.Read or Calendars.ReadWrite</span></span>
* <span data-ttu-id="58e85-109">Eventos de un calendario de grupo: Group.Read.All o Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="58e85-109">Events in a group calendar: Group.Read.All or Group.ReadWrite.All</span></span>

## <a name="http-request"></a><span data-ttu-id="58e85-110">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="58e85-110">HTTP request</span></span>

<span data-ttu-id="58e85-111">[calendar](../resources/calendar.md) predeterminado de un usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="58e85-111">A user's or group's default [calendar](../resources/calendar.md).</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/calendar/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendar/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /groups/{id}/calendar/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

<span data-ttu-id="58e85-112">[calendar](../resources/calendar.md) de un usuario del [calendarGroup](../resources/calendargroup.md) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="58e85-112">A user's [calendar](../resources/calendar.md) in the default [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}

GET /me/calendarGroup/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendarGroup/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

<span data-ttu-id="58e85-113">[calendar](../resources/calendar.md) de un usuario de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="58e85-113">A user's [calendar](../resources/calendar.md) in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendarGroups/{id}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

## <a name="query-parameters"></a><span data-ttu-id="58e85-114">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="58e85-114">Query parameters</span></span>

<span data-ttu-id="58e85-115">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta necesarios con valores.</span><span class="sxs-lookup"><span data-stu-id="58e85-115">In the request URL, provide the following required query parameters with values.</span></span>

| <span data-ttu-id="58e85-116">Parámetro</span><span class="sxs-lookup"><span data-stu-id="58e85-116">Parameter</span></span>    | <span data-ttu-id="58e85-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="58e85-117">Type</span></span>   |<span data-ttu-id="58e85-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="58e85-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="58e85-119">startDateTime</span><span class="sxs-lookup"><span data-stu-id="58e85-119">startDateTime</span></span>|<span data-ttu-id="58e85-120">String</span><span class="sxs-lookup"><span data-stu-id="58e85-120">String</span></span>|<span data-ttu-id="58e85-p102">La fecha y hora de inicio del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T19:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="58e85-p102">The start date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T19:00:00.0000000".</span></span>|
|<span data-ttu-id="58e85-123">endDateTime</span><span class="sxs-lookup"><span data-stu-id="58e85-123">endDateTime</span></span>|<span data-ttu-id="58e85-124">String</span><span class="sxs-lookup"><span data-stu-id="58e85-124">String</span></span>|<span data-ttu-id="58e85-p103">La fecha y hora de finalización del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T20:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="58e85-p103">The end date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T20:00:00.0000000".</span></span>|

<span data-ttu-id="58e85-127">Este método también admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="58e85-127">This method also supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="58e85-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="58e85-128">Request headers</span></span>
| <span data-ttu-id="58e85-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="58e85-129">Name</span></span>       | <span data-ttu-id="58e85-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="58e85-130">Type</span></span> | <span data-ttu-id="58e85-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="58e85-131">Description</span></span> |
|:---------------|:--------|:--------|
| <span data-ttu-id="58e85-132">Autorización</span><span class="sxs-lookup"><span data-stu-id="58e85-132">Authorization</span></span>  | <span data-ttu-id="58e85-133">string</span><span class="sxs-lookup"><span data-stu-id="58e85-133">string</span></span> | <span data-ttu-id="58e85-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="58e85-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="58e85-136">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="58e85-136">Prefer: outlook.timezone</span></span>  | <span data-ttu-id="58e85-137">string</span><span class="sxs-lookup"><span data-stu-id="58e85-137">string</span></span> | <span data-ttu-id="58e85-138">Se usa para especificar la zona horaria de las horas de inicio y final de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="58e85-138">Use this to specify the time zone for start and end times in the response.</span></span> <span data-ttu-id="58e85-139">Si no se especifican, estos valores de hora se devuelven en UTC.</span><span class="sxs-lookup"><span data-stu-id="58e85-139">If not specified, those time values are returned in UTC.</span></span> <span data-ttu-id="58e85-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="58e85-140">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="58e85-141">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="58e85-141">Request body</span></span>
<span data-ttu-id="58e85-142">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="58e85-142">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="58e85-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="58e85-143">Response</span></span>

<span data-ttu-id="58e85-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="58e85-144">If successful, this method returns a `200 OK` response code and collection of [Event](../resources/event.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="58e85-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="58e85-145">Example</span></span>
##### <a name="request"></a><span data-ttu-id="58e85-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="58e85-146">Request</span></span>
<span data-ttu-id="58e85-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="58e85-147">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_calendarview"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendar/calendarView?startDateTime=2017-01-01T19:00:00.0000000&endDateTime=2017-01-07T19:00:00.0000000
```
##### <a name="response"></a><span data-ttu-id="58e85-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="58e85-148">Response</span></span>
<span data-ttu-id="58e85-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="58e85-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
        "response": "response-value",
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
  "description": "List calendarView",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
