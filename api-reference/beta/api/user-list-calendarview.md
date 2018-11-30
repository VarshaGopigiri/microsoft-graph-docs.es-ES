---
title: List calendarView
description: Obtenga las repeticiones, excepciones e instancias únicas de eventos en una vista de calendario definida por un intervalo de tiempo, desde el calendario del usuario de forma predeterminada,
ms.openlocfilehash: 393dd98077dffead9567115d440eb695e12dbac3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083153"
---
# <a name="list-calendarview"></a><span data-ttu-id="fc01e-103">List calendarView</span><span class="sxs-lookup"><span data-stu-id="fc01e-103">List calendarView</span></span>

> <span data-ttu-id="fc01e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fc01e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fc01e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fc01e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fc01e-106">Obtiene las repeticiones, excepciones e instancias únicas de eventos en una vista de calendario definida por un intervalo de tiempo del calendario predeterminado de un usuario, o alguno de los otros calendarios del usuario.</span><span class="sxs-lookup"><span data-stu-id="fc01e-106">Get the occurrences, exceptions, and single instances of events in a calendar view defined by a time range, from the user's default calendar, or from some other calendar of the user's.</span></span>
## <a name="permissions"></a><span data-ttu-id="fc01e-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="fc01e-107">Permissions</span></span>
<span data-ttu-id="fc01e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fc01e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fc01e-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fc01e-110">Permission type</span></span>      | <span data-ttu-id="fc01e-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fc01e-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fc01e-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fc01e-112">Delegated (work or school account)</span></span> | <span data-ttu-id="fc01e-113">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fc01e-113">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="fc01e-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fc01e-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fc01e-115">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fc01e-115">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="fc01e-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fc01e-116">Application</span></span> | <span data-ttu-id="fc01e-117">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fc01e-117">Calendars.Read, Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="fc01e-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fc01e-118">HTTP request</span></span>
<span data-ttu-id="fc01e-119">[calendar](../resources/calendar.md) predeterminado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="fc01e-119">A user's default [calendar](../resources/calendar.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendar/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

<span data-ttu-id="fc01e-120">[calendar](../resources/calendar.md) de un usuario del [calendarGroup](../resources/calendargroup.md) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="fc01e-120">A user's [calendar](../resources/calendar.md) in the default [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}

GET /me/calendarGroup/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendarGroup/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

<span data-ttu-id="fc01e-121">[calendar](../resources/calendar.md) de un usuario de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="fc01e-121">A user's [calendar](../resources/calendar.md) in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendarGroups/{id}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

## <a name="query-parameters"></a><span data-ttu-id="fc01e-122">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="fc01e-122">Query parameters</span></span>

<span data-ttu-id="fc01e-123">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta necesarios con valores.</span><span class="sxs-lookup"><span data-stu-id="fc01e-123">In the request URL, provide the following required query parameters with values.</span></span>

| <span data-ttu-id="fc01e-124">Parámetro</span><span class="sxs-lookup"><span data-stu-id="fc01e-124">Parameter</span></span>    | <span data-ttu-id="fc01e-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="fc01e-125">Type</span></span>   |<span data-ttu-id="fc01e-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc01e-126">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fc01e-127">startDateTime</span><span class="sxs-lookup"><span data-stu-id="fc01e-127">startDateTime</span></span>|<span data-ttu-id="fc01e-128">String</span><span class="sxs-lookup"><span data-stu-id="fc01e-128">String</span></span>|<span data-ttu-id="fc01e-p103">La fecha y hora de inicio del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T19:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="fc01e-p103">The start date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T19:00:00.0000000".</span></span>|
|<span data-ttu-id="fc01e-131">endDateTime</span><span class="sxs-lookup"><span data-stu-id="fc01e-131">endDateTime</span></span>|<span data-ttu-id="fc01e-132">String</span><span class="sxs-lookup"><span data-stu-id="fc01e-132">String</span></span>|<span data-ttu-id="fc01e-p104">La fecha y hora de finalización del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T20:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="fc01e-p104">The end date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T20:00:00.0000000".</span></span>|

<span data-ttu-id="fc01e-135">Este método también admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fc01e-135">This method also supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="fc01e-136">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fc01e-136">Request headers</span></span>
| <span data-ttu-id="fc01e-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="fc01e-137">Name</span></span>       | <span data-ttu-id="fc01e-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="fc01e-138">Type</span></span> | <span data-ttu-id="fc01e-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc01e-139">Description</span></span> |
|:---------------|:--------|:--------|
| <span data-ttu-id="fc01e-140">Authorization</span><span class="sxs-lookup"><span data-stu-id="fc01e-140">Authorization</span></span>  | <span data-ttu-id="fc01e-141">string</span><span class="sxs-lookup"><span data-stu-id="fc01e-141">string</span></span> | <span data-ttu-id="fc01e-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fc01e-p105">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="fc01e-144">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="fc01e-144">Prefer: outlook.timezone</span></span>  | <span data-ttu-id="fc01e-145">string</span><span class="sxs-lookup"><span data-stu-id="fc01e-145">string</span></span> | <span data-ttu-id="fc01e-146">Se usa para especificar la zona horaria de las horas de inicio y final de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fc01e-146">Use this to specify the time zone for start and end times in the response.</span></span> <span data-ttu-id="fc01e-147">Si no se especifican, estos valores de hora se devuelven en UTC.</span><span class="sxs-lookup"><span data-stu-id="fc01e-147">If not specified, those time values are returned in UTC.</span></span> <span data-ttu-id="fc01e-148">Opcional.</span><span class="sxs-lookup"><span data-stu-id="fc01e-148">Optional.</span></span> |
| <span data-ttu-id="fc01e-149">Prefer: outlook.body-content-type</span><span class="sxs-lookup"><span data-stu-id="fc01e-149">Prefer: outlook.body-content-type</span></span> | <span data-ttu-id="fc01e-150">string</span><span class="sxs-lookup"><span data-stu-id="fc01e-150">string</span></span> | <span data-ttu-id="fc01e-151">Formato de la propiedad **body** que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="fc01e-151">The format of the **body** property to be returned in.</span></span> <span data-ttu-id="fc01e-152">Los valores pueden ser "text" o "html".</span><span class="sxs-lookup"><span data-stu-id="fc01e-152">Values can be "text" or "html".</span></span> <span data-ttu-id="fc01e-153">Se devuelve un encabezado `Preference-Applied` como confirmación si se especifica este encabezado `Prefer`.</span><span class="sxs-lookup"><span data-stu-id="fc01e-153">A `Preference-Applied` header is returned as confirmation if this `Prefer` header is specified.</span></span> <span data-ttu-id="fc01e-154">Si no se especifica el encabezado, la propiedad **body** se devuelve en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="fc01e-154">If the header is not specified, the **body** property is returned in HTML format.</span></span> <span data-ttu-id="fc01e-155">Opcional.</span><span class="sxs-lookup"><span data-stu-id="fc01e-155">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="fc01e-156">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fc01e-156">Request body</span></span>
<span data-ttu-id="fc01e-157">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="fc01e-157">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="fc01e-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc01e-158">Response</span></span>

<span data-ttu-id="fc01e-159">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fc01e-159">If successful, this method returns a `200 OK` response code and collection of [Event](../resources/event.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="fc01e-160">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fc01e-160">Example</span></span>
##### <a name="request"></a><span data-ttu-id="fc01e-161">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fc01e-161">Request</span></span>
<span data-ttu-id="fc01e-162">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fc01e-162">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_calendarview"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendarView?startDateTime=2016-01-01T19:00:00.0000000&endDateTime=2016-10-01T19:00:00.0000000
```
##### <a name="response"></a><span data-ttu-id="fc01e-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc01e-163">Response</span></span>
<span data-ttu-id="fc01e-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fc01e-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
        "time": "2016-10-19T10:37:00Z"
      },
      "uid": "iCalUId-value",
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
  "keywords": "calendar",
  "section": "documentation",
  "tocPath": ""
}-->
