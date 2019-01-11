---
title: List instances
description: 'Obtener las instancias (repeticiones) de un evento para un intervalo de tiempo especificado. Si el evento es un `SeriesMaster` escriba, este parámetro devuelve el '
localization_priority: Normal
ms.openlocfilehash: 194d911b6c5ea05eb0d3f797287773c516da9ee3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27811399"
---
# <a name="list-instances"></a><span data-ttu-id="3a369-104">List instances</span><span class="sxs-lookup"><span data-stu-id="3a369-104">List instances</span></span>

<span data-ttu-id="3a369-p102">Obtiene las instancias (repeticiones) de un evento durante un intervalo de tiempo especificado. Si el evento es de tipo `SeriesMaster`, devuelve las repeticiones y excepciones del evento en el intervalo de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="3a369-p102">Get the instances (occurrences) of an event for a specified time range. If the event is a `SeriesMaster` type, this returns the occurrences and exceptions of the event in the specified time range.</span></span>

## <a name="permissions"></a><span data-ttu-id="3a369-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="3a369-107">Permissions</span></span>
<span data-ttu-id="3a369-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3a369-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3a369-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3a369-110">Permission type</span></span>      | <span data-ttu-id="3a369-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3a369-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3a369-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3a369-112">Delegated (work or school account)</span></span> | <span data-ttu-id="3a369-113">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="3a369-113">Calendars.Read</span></span>    |
|<span data-ttu-id="3a369-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3a369-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3a369-115">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="3a369-115">Calendars.Read</span></span>    |
|<span data-ttu-id="3a369-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3a369-116">Application</span></span> | <span data-ttu-id="3a369-117">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="3a369-117">Calendars.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="3a369-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3a369-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/events/{id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/events/{id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /groups/{id}/events/{id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}

GET /me/calendar/events/{id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendar/events/{id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /groups/{id}/calendar/events/{id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}

GET /me/calendars/{id}/events/{id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendars/{id}/events/{id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}

GET /me/calendargroup/calendars/{id}/events/{id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}

GET /me/calendargroups/{id}/calendars/{id}/events/{id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}
```
## <a name="query-parameters"></a><span data-ttu-id="3a369-119">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="3a369-119">Query parameters</span></span>

<span data-ttu-id="3a369-120">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta necesarios con valores.</span><span class="sxs-lookup"><span data-stu-id="3a369-120">In the request URL, provide the following required query parameters with values.</span></span>

| <span data-ttu-id="3a369-121">Parámetro</span><span class="sxs-lookup"><span data-stu-id="3a369-121">Parameter</span></span>    | <span data-ttu-id="3a369-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="3a369-122">Type</span></span>   |<span data-ttu-id="3a369-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a369-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3a369-124">startDateTime</span><span class="sxs-lookup"><span data-stu-id="3a369-124">startDateTime</span></span>|<span data-ttu-id="3a369-125">String</span><span class="sxs-lookup"><span data-stu-id="3a369-125">String</span></span>|<span data-ttu-id="3a369-p104">La fecha y hora de inicio del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T19:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="3a369-p104">The start date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T19:00:00.0000000".</span></span>|
|<span data-ttu-id="3a369-128">endDateTime</span><span class="sxs-lookup"><span data-stu-id="3a369-128">endDateTime</span></span>|<span data-ttu-id="3a369-129">String</span><span class="sxs-lookup"><span data-stu-id="3a369-129">String</span></span>|<span data-ttu-id="3a369-p105">La fecha y hora de finalización del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T20:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="3a369-p105">The end date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T20:00:00.0000000".</span></span>|

<span data-ttu-id="3a369-132">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3a369-132">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="3a369-133">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3a369-133">Request headers</span></span>
| <span data-ttu-id="3a369-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="3a369-134">Name</span></span>       | <span data-ttu-id="3a369-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="3a369-135">Type</span></span> | <span data-ttu-id="3a369-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a369-136">Description</span></span> |
|:---------------|:--------|:--------|
| <span data-ttu-id="3a369-137">Autorización</span><span class="sxs-lookup"><span data-stu-id="3a369-137">Authorization</span></span>  | <span data-ttu-id="3a369-138">string</span><span class="sxs-lookup"><span data-stu-id="3a369-138">string</span></span> | <span data-ttu-id="3a369-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3a369-p106">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="3a369-141">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="3a369-141">Prefer: outlook.timezone</span></span>  | <span data-ttu-id="3a369-142">string</span><span class="sxs-lookup"><span data-stu-id="3a369-142">string</span></span> | <span data-ttu-id="3a369-143">Se usa para especificar la zona horaria de las horas de inicio y final de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3a369-143">Use this to specify the time zone for start and end times in the response.</span></span> <span data-ttu-id="3a369-144">Si no se especifican, estos valores de hora se devuelven en UTC.</span><span class="sxs-lookup"><span data-stu-id="3a369-144">If not specified, those time values are returned in UTC.</span></span> <span data-ttu-id="3a369-145">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3a369-145">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="3a369-146">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3a369-146">Request body</span></span>
<span data-ttu-id="3a369-147">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3a369-147">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3a369-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3a369-148">Response</span></span>

<span data-ttu-id="3a369-149">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3a369-149">If successful, this method returns a `200 OK` response code and collection of [Event](../resources/event.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="3a369-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3a369-150">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3a369-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3a369-151">Request</span></span>
<span data-ttu-id="3a369-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3a369-152">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_instances"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/events/{id}/instances
```
##### <a name="response"></a><span data-ttu-id="3a369-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3a369-153">Response</span></span>
<span data-ttu-id="3a369-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3a369-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "List instances",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
