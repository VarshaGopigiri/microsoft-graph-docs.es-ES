---
title: List instances
description: 'Obtener las instancias (repeticiones) de un evento para un intervalo de tiempo especificado. Si el evento es un `SeriesMaster` escriba, este parámetro devuelve el '
ms.openlocfilehash: 6a423efb2ff969e66ba54807c506a3b431b7ee32
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028783"
---
# <a name="list-instances"></a><span data-ttu-id="7f42c-104">List instances</span><span class="sxs-lookup"><span data-stu-id="7f42c-104">List instances</span></span>

<span data-ttu-id="7f42c-p102">Obtiene las instancias (repeticiones) de un evento durante un intervalo de tiempo especificado. Si el evento es de tipo `SeriesMaster`, devuelve las repeticiones y excepciones del evento en el intervalo de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="7f42c-p102">Get the instances (occurrences) of an event for a specified time range. If the event is a `SeriesMaster` type, this returns the occurrences and exceptions of the event in the specified time range.</span></span>

## <a name="permissions"></a><span data-ttu-id="7f42c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="7f42c-107">Permissions</span></span>
<span data-ttu-id="7f42c-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7f42c-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7f42c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7f42c-110">Permission type</span></span>      | <span data-ttu-id="7f42c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7f42c-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7f42c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7f42c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="7f42c-113">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="7f42c-113">Calendars.Read</span></span>    |
|<span data-ttu-id="7f42c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7f42c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7f42c-115">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="7f42c-115">Calendars.Read</span></span>    |
|<span data-ttu-id="7f42c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7f42c-116">Application</span></span> | <span data-ttu-id="7f42c-117">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="7f42c-117">Calendars.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="7f42c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7f42c-118">HTTP request</span></span>
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
## <a name="query-parameters"></a><span data-ttu-id="7f42c-119">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="7f42c-119">Query parameters</span></span>

<span data-ttu-id="7f42c-120">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta necesarios con valores.</span><span class="sxs-lookup"><span data-stu-id="7f42c-120">In the request URL, provide the following required query parameters with values.</span></span>

| <span data-ttu-id="7f42c-121">Parámetro</span><span class="sxs-lookup"><span data-stu-id="7f42c-121">Parameter</span></span>    | <span data-ttu-id="7f42c-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="7f42c-122">Type</span></span>   |<span data-ttu-id="7f42c-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="7f42c-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7f42c-124">startDateTime</span><span class="sxs-lookup"><span data-stu-id="7f42c-124">startDateTime</span></span>|<span data-ttu-id="7f42c-125">String</span><span class="sxs-lookup"><span data-stu-id="7f42c-125">String</span></span>|<span data-ttu-id="7f42c-p104">La fecha y hora de inicio del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T19:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="7f42c-p104">The start date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T19:00:00.0000000".</span></span>|
|<span data-ttu-id="7f42c-128">endDateTime</span><span class="sxs-lookup"><span data-stu-id="7f42c-128">endDateTime</span></span>|<span data-ttu-id="7f42c-129">String</span><span class="sxs-lookup"><span data-stu-id="7f42c-129">String</span></span>|<span data-ttu-id="7f42c-p105">La fecha y hora de finalización del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T20:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="7f42c-p105">The end date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T20:00:00.0000000".</span></span>|

<span data-ttu-id="7f42c-132">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7f42c-132">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="7f42c-133">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7f42c-133">Request headers</span></span>
| <span data-ttu-id="7f42c-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="7f42c-134">Name</span></span>       | <span data-ttu-id="7f42c-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="7f42c-135">Type</span></span> | <span data-ttu-id="7f42c-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="7f42c-136">Description</span></span> |
|:---------------|:--------|:--------|
| <span data-ttu-id="7f42c-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="7f42c-137">Authorization</span></span>  | <span data-ttu-id="7f42c-138">string</span><span class="sxs-lookup"><span data-stu-id="7f42c-138">string</span></span> | <span data-ttu-id="7f42c-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7f42c-p106">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="7f42c-141">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="7f42c-141">Prefer: outlook.timezone</span></span>  | <span data-ttu-id="7f42c-142">string</span><span class="sxs-lookup"><span data-stu-id="7f42c-142">string</span></span> | <span data-ttu-id="7f42c-143">Se usa para especificar la zona horaria de las horas de inicio y final de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7f42c-143">Use this to specify the time zone for start and end times in the response.</span></span> <span data-ttu-id="7f42c-144">Si no se especifican, estos valores de hora se devuelven en UTC.</span><span class="sxs-lookup"><span data-stu-id="7f42c-144">If not specified, those time values are returned in UTC.</span></span> <span data-ttu-id="7f42c-145">Opcional.</span><span class="sxs-lookup"><span data-stu-id="7f42c-145">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="7f42c-146">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7f42c-146">Request body</span></span>
<span data-ttu-id="7f42c-147">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7f42c-147">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7f42c-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7f42c-148">Response</span></span>

<span data-ttu-id="7f42c-149">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7f42c-149">If successful, this method returns a `200 OK` response code and collection of [Event](../resources/event.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="7f42c-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7f42c-150">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7f42c-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7f42c-151">Request</span></span>
<span data-ttu-id="7f42c-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7f42c-152">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_instances"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/events/{id}/instances
```
##### <a name="response"></a><span data-ttu-id="7f42c-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7f42c-153">Response</span></span>
<span data-ttu-id="7f42c-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7f42c-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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