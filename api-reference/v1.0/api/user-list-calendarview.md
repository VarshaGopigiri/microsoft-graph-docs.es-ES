---
title: List calendarView
description: 'Obtenga las repeticiones, excepciones e instancias únicas de eventos en una vista de calendario definida por un intervalo de tiempo, desde el calendario del usuario de forma predeterminada, '
ms.openlocfilehash: db2c0b4d5fe2b3929aab7c30e00aff0f30dff5b5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029468"
---
# <a name="list-calendarview"></a><span data-ttu-id="7e359-103">List calendarView</span><span class="sxs-lookup"><span data-stu-id="7e359-103">List calendarView</span></span>

<span data-ttu-id="7e359-104">Obtiene las repeticiones, excepciones e instancias únicas de eventos en una vista de calendario definida por un intervalo de tiempo del calendario predeterminado de un usuario, o alguno de los otros calendarios del usuario.</span><span class="sxs-lookup"><span data-stu-id="7e359-104">Get the occurrences, exceptions, and single instances of events in a calendar view defined by a time range, from the user's default calendar, or from some other calendar of the user's.</span></span>
## <a name="permissions"></a><span data-ttu-id="7e359-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="7e359-105">Permissions</span></span>
<span data-ttu-id="7e359-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7e359-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7e359-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7e359-108">Permission type</span></span>      | <span data-ttu-id="7e359-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7e359-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7e359-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7e359-110">Delegated (work or school account)</span></span> | <span data-ttu-id="7e359-111">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7e359-111">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="7e359-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7e359-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7e359-113">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7e359-113">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="7e359-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7e359-114">Application</span></span> | <span data-ttu-id="7e359-115">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7e359-115">Calendars.Read, Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="7e359-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7e359-116">HTTP request</span></span>

<span data-ttu-id="7e359-117">[calendar](../resources/calendar.md) predeterminado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="7e359-117">A user's default [calendar](../resources/calendar.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendar/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

<span data-ttu-id="7e359-118">[calendar](../resources/calendar.md) de un usuario del [calendarGroup](../resources/calendargroup.md) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7e359-118">A user's [calendar](../resources/calendar.md) in the default [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}

GET /me/calendarGroup/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendarGroup/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

<span data-ttu-id="7e359-119">[calendar](../resources/calendar.md) de un usuario de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="7e359-119">A user's [calendar](../resources/calendar.md) in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendarGroups/{id}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

## <a name="query-parameters"></a><span data-ttu-id="7e359-120">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="7e359-120">Query parameters</span></span>

<span data-ttu-id="7e359-121">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta necesarios con valores.</span><span class="sxs-lookup"><span data-stu-id="7e359-121">In the request URL, provide the following required query parameters with values.</span></span>

| <span data-ttu-id="7e359-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="7e359-122">Parameter</span></span>    | <span data-ttu-id="7e359-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="7e359-123">Type</span></span>   |<span data-ttu-id="7e359-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e359-124">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7e359-125">startDateTime</span><span class="sxs-lookup"><span data-stu-id="7e359-125">startDateTime</span></span>|<span data-ttu-id="7e359-126">String</span><span class="sxs-lookup"><span data-stu-id="7e359-126">String</span></span>|<span data-ttu-id="7e359-p102">La fecha y hora de inicio del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T19:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="7e359-p102">The start date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T19:00:00.0000000".</span></span>|
|<span data-ttu-id="7e359-129">endDateTime</span><span class="sxs-lookup"><span data-stu-id="7e359-129">endDateTime</span></span>|<span data-ttu-id="7e359-130">String</span><span class="sxs-lookup"><span data-stu-id="7e359-130">String</span></span>|<span data-ttu-id="7e359-p103">La fecha y hora de finalización del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T20:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="7e359-p103">The end date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T20:00:00.0000000".</span></span>|

<span data-ttu-id="7e359-133">Este método también admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7e359-133">This method also supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="7e359-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7e359-134">Request headers</span></span>
| <span data-ttu-id="7e359-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="7e359-135">Name</span></span>       | <span data-ttu-id="7e359-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="7e359-136">Type</span></span> | <span data-ttu-id="7e359-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e359-137">Description</span></span> |
|:---------------|:--------|:--------|
| <span data-ttu-id="7e359-138">Authorization</span><span class="sxs-lookup"><span data-stu-id="7e359-138">Authorization</span></span>  | <span data-ttu-id="7e359-139">string</span><span class="sxs-lookup"><span data-stu-id="7e359-139">string</span></span> | <span data-ttu-id="7e359-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7e359-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="7e359-142">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="7e359-142">Prefer: outlook.timezone</span></span>  | <span data-ttu-id="7e359-143">string</span><span class="sxs-lookup"><span data-stu-id="7e359-143">string</span></span> | <span data-ttu-id="7e359-144">Se usa para especificar la zona horaria de las horas de inicio y final de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7e359-144">Use this to specify the time zone for start and end times in the response.</span></span> <span data-ttu-id="7e359-145">Si no se especifican, estos valores de hora se devuelven en UTC.</span><span class="sxs-lookup"><span data-stu-id="7e359-145">If not specified, those time values are returned in UTC.</span></span> <span data-ttu-id="7e359-146">Opcional.</span><span class="sxs-lookup"><span data-stu-id="7e359-146">Optional.</span></span> |
| <span data-ttu-id="7e359-147">Prefer: outlook.body-content-type</span><span class="sxs-lookup"><span data-stu-id="7e359-147">Prefer: outlook.body-content-type</span></span> | <span data-ttu-id="7e359-148">string</span><span class="sxs-lookup"><span data-stu-id="7e359-148">string</span></span> | <span data-ttu-id="7e359-149">Formato de la propiedad **body** que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="7e359-149">The format of the **body** property to be returned in.</span></span> <span data-ttu-id="7e359-150">Los valores pueden ser "text" o "html".</span><span class="sxs-lookup"><span data-stu-id="7e359-150">Values can be "text" or "html".</span></span> <span data-ttu-id="7e359-151">Se devuelve un encabezado `Preference-Applied` como confirmación si se especifica este encabezado `Prefer`.</span><span class="sxs-lookup"><span data-stu-id="7e359-151">A `Preference-Applied` header is returned as confirmation if this `Prefer` header is specified.</span></span> <span data-ttu-id="7e359-152">Si no se especifica el encabezado, la propiedad **body** se devuelve en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="7e359-152">If the header is not specified, the **body** property is returned in HTML format.</span></span> <span data-ttu-id="7e359-153">Opcional.</span><span class="sxs-lookup"><span data-stu-id="7e359-153">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="7e359-154">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7e359-154">Request body</span></span>
<span data-ttu-id="7e359-155">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7e359-155">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7e359-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7e359-156">Response</span></span>

<span data-ttu-id="7e359-157">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7e359-157">If successful, this method returns a `200 OK` response code and collection of [Event](../resources/event.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="7e359-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7e359-158">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7e359-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7e359-159">Request</span></span>
<span data-ttu-id="7e359-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7e359-160">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_calendarview"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendarView?startDateTime=2016-01-01T19:00:00.0000000&endDateTime=2016-10-01T19:00:00.0000000 
```
##### <a name="response"></a><span data-ttu-id="7e359-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7e359-161">Response</span></span>
<span data-ttu-id="7e359-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7e359-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "List calendarView",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
