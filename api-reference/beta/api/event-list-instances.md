---
title: List instances
description: Obtener las instancias (repeticiones) de un evento para un intervalo de tiempo especificado. Si el evento es un `SeriesMaster` escriba, este parámetro devuelve el
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 7a40e6f468c8541748adbc7d8dd588541318c30c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27980933"
---
# <a name="list-instances"></a><span data-ttu-id="4a966-104">Instancias de lista</span><span class="sxs-lookup"><span data-stu-id="4a966-104">List instances</span></span>

> <span data-ttu-id="4a966-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4a966-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4a966-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4a966-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4a966-p103">Obtiene las instancias (repeticiones) de un evento durante un intervalo de tiempo especificado. Si el evento es de tipo `SeriesMaster`, devuelve las repeticiones y excepciones del evento en el intervalo de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="4a966-p103">Get the instances (occurrences) of an event for a specified time range. If the event is a `SeriesMaster` type, this returns the occurrences and exceptions of the event in the specified time range.</span></span>

## <a name="permissions"></a><span data-ttu-id="4a966-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="4a966-109">Permissions</span></span>
<span data-ttu-id="4a966-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4a966-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4a966-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4a966-112">Permission type</span></span>      | <span data-ttu-id="4a966-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4a966-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4a966-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4a966-114">Delegated (work or school account)</span></span> | <span data-ttu-id="4a966-115">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="4a966-115">Calendars.Read</span></span>    |
|<span data-ttu-id="4a966-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4a966-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4a966-117">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="4a966-117">Calendars.Read</span></span>    |
|<span data-ttu-id="4a966-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4a966-118">Application</span></span> | <span data-ttu-id="4a966-119">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="4a966-119">Calendars.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="4a966-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4a966-120">HTTP request</span></span>
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
## <a name="query-parameters"></a><span data-ttu-id="4a966-121">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="4a966-121">Query parameters</span></span>

<span data-ttu-id="4a966-122">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta necesarios con valores.</span><span class="sxs-lookup"><span data-stu-id="4a966-122">In the request URL, provide the following required query parameters with values.</span></span>

| <span data-ttu-id="4a966-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4a966-123">Parameter</span></span>    | <span data-ttu-id="4a966-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="4a966-124">Type</span></span>   |<span data-ttu-id="4a966-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a966-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4a966-126">startDateTime</span><span class="sxs-lookup"><span data-stu-id="4a966-126">startDateTime</span></span>|<span data-ttu-id="4a966-127">String</span><span class="sxs-lookup"><span data-stu-id="4a966-127">String</span></span>|<span data-ttu-id="4a966-p105">La fecha y hora de inicio del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T19:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="4a966-p105">The start date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T19:00:00.0000000".</span></span>|
|<span data-ttu-id="4a966-130">endDateTime</span><span class="sxs-lookup"><span data-stu-id="4a966-130">endDateTime</span></span>|<span data-ttu-id="4a966-131">String</span><span class="sxs-lookup"><span data-stu-id="4a966-131">String</span></span>|<span data-ttu-id="4a966-p106">La fecha y hora de finalización del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T20:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="4a966-p106">The end date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T20:00:00.0000000".</span></span>|

<span data-ttu-id="4a966-134">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4a966-134">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="4a966-135">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4a966-135">Request headers</span></span>
| <span data-ttu-id="4a966-136">Nombre</span><span class="sxs-lookup"><span data-stu-id="4a966-136">Name</span></span>       | <span data-ttu-id="4a966-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="4a966-137">Type</span></span> | <span data-ttu-id="4a966-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a966-138">Description</span></span> |
|:---------------|:--------|:--------|
| <span data-ttu-id="4a966-139">Autorización</span><span class="sxs-lookup"><span data-stu-id="4a966-139">Authorization</span></span>  | <span data-ttu-id="4a966-140">string</span><span class="sxs-lookup"><span data-stu-id="4a966-140">string</span></span> | <span data-ttu-id="4a966-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4a966-p107">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="4a966-143">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="4a966-143">Prefer: outlook.timezone</span></span>  | <span data-ttu-id="4a966-144">string</span><span class="sxs-lookup"><span data-stu-id="4a966-144">string</span></span> | <span data-ttu-id="4a966-145">Se usa para especificar la zona horaria de las horas de inicio y final de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4a966-145">Use this to specify the time zone for start and end times in the response.</span></span> <span data-ttu-id="4a966-146">Si no se especifican, estos valores de hora se devuelven en UTC.</span><span class="sxs-lookup"><span data-stu-id="4a966-146">If not specified, those time values are returned in UTC.</span></span> <span data-ttu-id="4a966-147">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4a966-147">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4a966-148">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4a966-148">Request body</span></span>
<span data-ttu-id="4a966-149">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4a966-149">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4a966-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4a966-150">Response</span></span>

<span data-ttu-id="4a966-151">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4a966-151">If successful, this method returns a `200 OK` response code and collection of [Event](../resources/event.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="4a966-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4a966-152">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4a966-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4a966-153">Request</span></span>
<span data-ttu-id="4a966-154">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4a966-154">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_instances"
}-->
```http
GET https://graph.microsoft.com/beta/me/events/{id}/instances
```
##### <a name="response"></a><span data-ttu-id="4a966-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4a966-155">Response</span></span>
<span data-ttu-id="4a966-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4a966-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "List instances",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
