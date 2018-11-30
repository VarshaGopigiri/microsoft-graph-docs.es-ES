---
title: 'calendario: getSchedule'
description: Obtenga la información de disponibilidad para una colección de los usuarios, las listas de distribución o de recursos, para un período de tiempo especificado.
ms.openlocfilehash: 5122cf34530f18f872e80863f259f348193d252e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084682"
---
# <a name="calendar-getschedule"></a><span data-ttu-id="baf41-103">calendario: getSchedule</span><span class="sxs-lookup"><span data-stu-id="baf41-103">calendar: getSchedule</span></span>

> <span data-ttu-id="baf41-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="baf41-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="baf41-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="baf41-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="baf41-106">Obtenga la información de disponibilidad para una colección de los usuarios, las listas de distribución o de recursos, para un período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="baf41-106">Get the free/busy availability information for a collection of users, distributions lists, or resources, for a specified time period.</span></span>

## <a name="permissions"></a><span data-ttu-id="baf41-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="baf41-107">Permissions</span></span>
<span data-ttu-id="baf41-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="baf41-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="baf41-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="baf41-110">Permission type</span></span>      | <span data-ttu-id="baf41-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="baf41-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="baf41-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="baf41-112">Delegated (work or school account)</span></span> | <span data-ttu-id="baf41-113">Calendar.Read, Calendar.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="baf41-113">Calendar.Read, Calendar.ReadWrite</span></span>    |
|<span data-ttu-id="baf41-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="baf41-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="baf41-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="baf41-115">Not supported.</span></span> |
|<span data-ttu-id="baf41-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="baf41-116">Application</span></span> | <span data-ttu-id="baf41-117">Calendar.Read, Calendar.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="baf41-117">Calendar.Read, Calendar.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="baf41-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="baf41-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/calendar/getSchedule 
POST /users/{id|userPrincipalName}/calendar/getSchedule
```

## <a name="request-headers"></a><span data-ttu-id="baf41-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="baf41-119">Request headers</span></span>
| <span data-ttu-id="baf41-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="baf41-120">Name</span></span>       | <span data-ttu-id="baf41-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="baf41-121">Type</span></span> | <span data-ttu-id="baf41-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="baf41-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="baf41-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="baf41-123">Authorization</span></span>  | <span data-ttu-id="baf41-124">string</span><span class="sxs-lookup"><span data-stu-id="baf41-124">string</span></span>  | <span data-ttu-id="baf41-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="baf41-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="baf41-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="baf41-127">Content-Type</span></span>  | <span data-ttu-id="baf41-128">string</span><span class="sxs-lookup"><span data-stu-id="baf41-128">string</span></span> | <span data-ttu-id="baf41-129">Naturaleza de los datos en el cuerpo de una entidad, que es application/json.</span><span class="sxs-lookup"><span data-stu-id="baf41-129">Nature of the data in the body of an entity, which is application/json.</span></span> <span data-ttu-id="baf41-130">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="baf41-130">Required.</span></span>  |
| <span data-ttu-id="baf41-131">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="baf41-131">Prefer: outlook.timezone</span></span> | <span data-ttu-id="baf41-132">string</span><span class="sxs-lookup"><span data-stu-id="baf41-132">string</span></span> | <span data-ttu-id="baf41-133">Se usa para especificar la zona horaria de las horas de inicio y final de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="baf41-133">Use this to specify the time zone for start and end times in the response.</span></span> <span data-ttu-id="baf41-134">Si no se especifican, estos valores de hora se devuelven en UTC.</span><span class="sxs-lookup"><span data-stu-id="baf41-134">If not specified, those time values are returned in UTC.</span></span> <span data-ttu-id="baf41-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="baf41-135">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="baf41-136">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="baf41-136">Request body</span></span>
<span data-ttu-id="baf41-137">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="baf41-137">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="baf41-138">Propiedad</span><span class="sxs-lookup"><span data-stu-id="baf41-138">Property</span></span>     | <span data-ttu-id="baf41-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="baf41-139">Type</span></span>   |<span data-ttu-id="baf41-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="baf41-140">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="baf41-141">availabilityViewInterval</span><span class="sxs-lookup"><span data-stu-id="baf41-141">availabilityViewInterval</span></span>|<span data-ttu-id="baf41-142">String</span><span class="sxs-lookup"><span data-stu-id="baf41-142">String</span></span>|<span data-ttu-id="baf41-143">Representa la duración de un intervalo de tiempo en un **availabilityView** en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="baf41-143">Represents the duration of a time slot in an **availabilityView** in the response.</span></span> <span data-ttu-id="baf41-144">El valor predeterminado es 30 minutos, como mínimo es 6, el máximo es 1440.</span><span class="sxs-lookup"><span data-stu-id="baf41-144">The default is 30 minutes, minimum is 6, maximum is 1440.</span></span> <span data-ttu-id="baf41-145">Opcional.</span><span class="sxs-lookup"><span data-stu-id="baf41-145">Optional.</span></span>|
|<span data-ttu-id="baf41-146">endTime</span><span class="sxs-lookup"><span data-stu-id="baf41-146">endTime</span></span>|[<span data-ttu-id="baf41-147">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="baf41-147">dateTimeTimeZone</span></span>](../resources/datetimetimezone.md)|<span data-ttu-id="baf41-148">La fecha, hora y zona horaria que termina el período.</span><span class="sxs-lookup"><span data-stu-id="baf41-148">The date, time, and time zone that the period ends.</span></span>|
|<span data-ttu-id="baf41-149">programaciones</span><span class="sxs-lookup"><span data-stu-id="baf41-149">schedules</span></span>|<span data-ttu-id="baf41-150">Colección String</span><span class="sxs-lookup"><span data-stu-id="baf41-150">String collection</span></span>|<span data-ttu-id="baf41-151">Una colección de direcciones SMTP de los usuarios, listas de distribución o recursos para obtener información de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="baf41-151">A collection of SMTP addresses of users, distribution lists, or resources to get availability information for.</span></span>|
|<span data-ttu-id="baf41-152">startTime</span><span class="sxs-lookup"><span data-stu-id="baf41-152">startTime</span></span>|[<span data-ttu-id="baf41-153">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="baf41-153">dateTimeTimeZone</span></span>](../resources/datetimetimezone.md)|<span data-ttu-id="baf41-154">La fecha, hora y zona horaria que se inicia el período.</span><span class="sxs-lookup"><span data-stu-id="baf41-154">The date, time, and time zone that the period starts.</span></span>|

## <a name="response"></a><span data-ttu-id="baf41-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="baf41-155">Response</span></span>

<span data-ttu-id="baf41-156">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos [scheduleInformation](../resources/scheduleinformation.md) para cada objeto en el `schedules` parámetro.</span><span class="sxs-lookup"><span data-stu-id="baf41-156">If successful, this method returns a `200 OK` response code and a collection of [scheduleInformation](../resources/scheduleinformation.md) objects for each object in the `schedules` parameter.</span></span>
## <a name="example"></a><span data-ttu-id="baf41-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="baf41-157">Example</span></span>
##### <a name="request"></a><span data-ttu-id="baf41-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="baf41-158">Request</span></span>
<span data-ttu-id="baf41-159">En el ejemplo siguiente se obtiene la información de disponibilidad para dos usuarios para la fecha especificada, la hora y la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="baf41-159">The following example gets the availability information for two users for the specified date, time, and time zone.</span></span>

<!-- {
  "blockType": "ignored",
  "name": "calendar_getSchedule"
}-->
```http
POST https://graph.microsoft.com/beta/me/calendar/getschedule 
Prefer: outlook.timezone="Pacific Standard Time"
Content-Type: application/json

{        
    "schedules": ["AdeleV@contoso.onmicrosoft.com", "AlexW@contoso.OnMicrosoft.com"],
    "startTime": {
        "dateTime": "2018-08-06T09:00:00",
        "timeZone": "Pacific Standard Time"
    },
    "endTime": {
        "dateTime": "2018-08-06T18:00:00",
        "timeZone": "Pacific Standard Time"
    },
    "availabilityViewInterval": "15"
}
```

##### <a name="response"></a><span data-ttu-id="baf41-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="baf41-160">Response</span></span>
<span data-ttu-id="baf41-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="baf41-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.scheduleInformation",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.scheduleInformation)",
    "value":[
        {
            "scheduleId":"AdeleV@contoso.onmicrosoft.com",
            "availabilityView":"222222000022000000000000000000000000",
            "scheduleItems":[
                {
                    "isPrivate":false,
                    "status":"Busy",
                    "subject":"Admininstrators debrief",
                    "location":"Foyer",
                    "start":{
                        "dateTime":"2018-08-06T09:00:00.0000000",
                        "timeZone":"Pacific Standard Time"
                    },
                    "end":{
                        "dateTime":"2018-08-06T10:30:00.0000000",
                        "timeZone":"Pacific Standard Time"
                    }
                },
                {
                    "isPrivate":false,
                    "status":"Busy",
                    "subject":"Lunch yoga",
                    "location":"Courtyard",
                    "start":{
                        "dateTime":"2018-08-06T11:30:00.0000000",
                        "timeZone":"Pacific Standard Time"
                    },
                    "end":{
                        "dateTime":"2018-08-06T12:00:00.0000000",
                        "timeZone":"Pacific Standard Time"
                    }
                }
            ],
            "workingHours":{
                "daysOfWeek":[
                    "monday",
                    "tuesday",
                    "wednesday",
                    "thursday",
                    "friday"
                ],
                "startTime":"08:00:00.0000000",
                "endTime":"17:00:00.0000000",
                "timeZone":{
                    "@odata.type":"#microsoft.graph.customTimeZone",
                    "bias":480,
                    "name":"Customized Time Zone",
                    "standardOffset":{
                        "time":"02:00:00.0000000",
                        "dayOccurrence":1,
                        "dayOfWeek":"sunday",
                        "month":11,
                        "year":0
                    },
                    "daylightOffset":{
                        "daylightBias":-60,
                        "time":"02:00:00.0000000",
                        "dayOccurrence":2,
                        "dayOfWeek":"sunday",
                        "month":3,
                        "year":0
                    }
                }
            }
        },
        {
            "scheduleId":"AlexW@contoso.OnMicrosoft.com",
            "availabilityView":"111111002222222200000000000000000000",
            "scheduleItems":[
                {
                    "isPrivate":false,
                    "status":"Tentative",
                    "subject":"Admininstrators debrief",
                    "location":"Foyer",
                    "start":{
                        "dateTime":"2018-08-06T09:00:00.0000000",
                        "timeZone":"Pacific Standard Time"
                    },
                    "end":{
                        "dateTime":"2018-08-06T10:30:00.0000000",
                        "timeZone":"Pacific Standard Time"
                    }
                },
                {
                    "isPrivate":false,
                    "status":"Busy",
                    "subject":"Q4 planning",
                    "location":"Big Bear",
                    "start":{
                        "dateTime":"2018-08-06T11:00:00.0000000",
                        "timeZone":"Pacific Standard Time"
                    },
                    "end":{
                        "dateTime":"2018-08-06T13:00:00.0000000",
                        "timeZone":"Pacific Standard Time"
                    }
                }
            ],
            "workingHours":{
                "daysOfWeek":[
                    "monday",
                    "tuesday",
                    "wednesday",
                    "thursday",
                    "friday"
                ],
                "startTime":"08:00:00.0000000",
                "endTime":"17:00:00.0000000",
                "timeZone":{
                    "@odata.type":"#microsoft.graph.customTimeZone",
                    "bias":480,
                    "name":"Customized Time Zone",
                    "standardOffset":{
                        "time":"02:00:00.0000000",
                        "dayOccurrence":1,
                        "dayOfWeek":"sunday",
                        "month":11,
                        "year":0
                    },
                    "daylightOffset":{
                        "daylightBias":-60,
                        "time":"02:00:00.0000000",
                        "dayOccurrence":2,
                        "dayOfWeek":"sunday",
                        "month":3,
                        "year":0
                    }
                }
            }
        }
    ]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "calendar: getSchedule",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->