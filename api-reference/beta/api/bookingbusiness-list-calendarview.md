---
title: Lista reservas calendarView
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
author: angelgolfer-ms
ms.prod: bookings
ms.openlocfilehash: 96da0d02d58f9ea4a3503e08c0733f4394dbbd6a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27956944"
---
# <a name="list-bookings-calendarview"></a><span data-ttu-id="727da-104">Lista reservas calendarView</span><span class="sxs-lookup"><span data-stu-id="727da-104">List Bookings calendarView</span></span>

 > <span data-ttu-id="727da-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="727da-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="727da-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="727da-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="727da-107">Obtener la colección de objetos [bookingAppointment](../resources/bookingappointment.md) para un [bookingBusiness](../resources/bookingbusiness.md), que se produce en el intervalo de fechas especificado.</span><span class="sxs-lookup"><span data-stu-id="727da-107">Get the collection of [bookingAppointment](../resources/bookingappointment.md) objects for a [bookingBusiness](../resources/bookingbusiness.md), that occurs in the specified date range.</span></span>

## <a name="permissions"></a><span data-ttu-id="727da-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="727da-108">Permissions</span></span>
<span data-ttu-id="727da-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="727da-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="727da-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="727da-111">Permission type</span></span>      | <span data-ttu-id="727da-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="727da-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="727da-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="727da-113">Delegated (work or school account)</span></span> |  <span data-ttu-id="727da-114">Bookings.Read.All, BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span><span class="sxs-lookup"><span data-stu-id="727da-114">Bookings.Read.All, BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span></span>   |
|<span data-ttu-id="727da-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="727da-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="727da-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="727da-116">Not supported.</span></span>   |
|<span data-ttu-id="727da-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="727da-117">Application</span></span> | <span data-ttu-id="727da-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="727da-118">Not supported.</span></span>  | 

## <a name="http-request"></a><span data-ttu-id="727da-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="727da-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /bookingBusinesses/{id}/calendarView?start={start-value}&end={end-value}

```
## <a name="request-headers"></a><span data-ttu-id="727da-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="727da-120">Request headers</span></span>
| <span data-ttu-id="727da-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="727da-121">Name</span></span>       | <span data-ttu-id="727da-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="727da-122">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="727da-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="727da-123">Authorization</span></span>  | <span data-ttu-id="727da-124">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="727da-124">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="727da-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="727da-125">Request body</span></span>
<span data-ttu-id="727da-126">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="727da-126">In the request URL, provide following query parameters with values.</span></span>

| <span data-ttu-id="727da-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="727da-127">Parameter</span></span>    | <span data-ttu-id="727da-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="727da-128">Type</span></span>   |<span data-ttu-id="727da-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="727da-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="727da-130">start</span><span class="sxs-lookup"><span data-stu-id="727da-130">start</span></span>|<span data-ttu-id="727da-131">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="727da-131">DateTimeOffset</span></span>|<span data-ttu-id="727da-132">La fecha de inicio y la hora de un intervalo de tiempo, se representan en formato ISO 8601, como UTC o un desplazamiento de la hora UTC.</span><span class="sxs-lookup"><span data-stu-id="727da-132">The start date and time of a time range, represented in ISO 8601 format, as UTC or an offset from UTC.</span></span> <span data-ttu-id="727da-133">Por ejemplo, medianoche UTC del 1 de enero de 2018 tendrá este aspecto: ' 2018-01-01T00:00:00Z', y el mismo tiempo en PST tendría el siguiente aspecto: ' 2017-12-31T16:00:00-08:00 '.</span><span class="sxs-lookup"><span data-stu-id="727da-133">For example, midnight UTC on Jan 1, 2018 would look like this: '2018-01-01T00:00:00Z', and the same time in PST would look like this: '2017-12-31T16:00:00-08:00'.</span></span>|
|<span data-ttu-id="727da-134">end</span><span class="sxs-lookup"><span data-stu-id="727da-134">end</span></span>|<span data-ttu-id="727da-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="727da-135">DateTimeOffset</span></span>|<span data-ttu-id="727da-136">La fecha y hora finales de un intervalo de tiempo, se representan en formato ISO 8601, como UTC o un desplazamiento de la hora UTC.</span><span class="sxs-lookup"><span data-stu-id="727da-136">The end date and time of a time range, represented in ISO 8601 format, as UTC or an offset from UTC.</span></span> <span data-ttu-id="727da-137">Por ejemplo, 3 am UTC en 1 de enero de 2018 tendría el siguiente aspecto: ' 2018-01-01T03:00:00Z', y el mismo tiempo en PST tendría el siguiente aspecto: ' 2017-12-31T19:00:00-08:00 '.</span><span class="sxs-lookup"><span data-stu-id="727da-137">For example, 3am UTC on Jan 1, 2018 would look like this: '2018-01-01T03:00:00Z', and the same time in PST would look like this: '2017-12-31T19:00:00-08:00'.</span></span>|

## <a name="response"></a><span data-ttu-id="727da-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="727da-138">Response</span></span>
<span data-ttu-id="727da-139">Si tiene éxito, este método devuelve `200, OK` objeto de colección de respuesta código y [bookingAppointment](../resources/bookingappointment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="727da-139">If successful, this method returns `200, OK` response code and [bookingAppointment](../resources/bookingappointment.md) collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="727da-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="727da-140">Example</span></span>
<span data-ttu-id="727da-141">Este es un ejemplo de cómo realizar una llamada a esta API.</span><span class="sxs-lookup"><span data-stu-id="727da-141">The following is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="727da-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="727da-142">Request</span></span>
<span data-ttu-id="727da-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="727da-143">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "bookingbusiness_getcalendarview"
}-->
```http
GET https://graph.microsoft.com/beta/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/calendarView?start=2018-04-30T00:00:00Z&end=2018-05-10T00:00:00Z
```

##### <a name="response"></a><span data-ttu-id="727da-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="727da-144">Response</span></span>
<span data-ttu-id="727da-145">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="727da-145">The following is an example of the response.</span></span> <span data-ttu-id="727da-146">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="727da-146">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="727da-147">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="727da-147">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.bookingAppointment",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#bookingBusinesses('Contosolunchdelivery%40M365B489948.onmicrosoft.com')/calendarView",
    "value": [
        {
            "id": "AAMkADKpAAA=",
            "selfServiceAppointmentId": "00000000-0000-0000-0000-000000000000",
            "customerId": "80b5ddda-1e3b-4c9d-abe2-d606cc075e2e",
            "customerName": "Adele Vance",
            "customerEmailAddress": "adelev@proseware.com",
            "customerPhone": "213-555-0156",
            "customerNotes": null,
            "serviceId": "57da6774-a087-4d69-b0e6-6fb82c339976",
            "serviceName": "Catered bento",
            "duration": "PT30M",
            "preBuffer": "PT5M",
            "postBuffer": "PT10M",
            "priceType": "fixedPrice",
            "price": 10,
            "serviceNotes": null,
            "optOutOfCustomerEmail": false,
            "staffMemberIds": [],
            "invoiceAmount": 10,
            "invoiceId": "1003",
            "invoiceStatus": "open",
            "invoiceUrl": "theInvoiceUrl",
            "customerLocation": {
                "displayName": "Customer",
                "locationEmailAddress": null,
                "locationUri": "",
                "locationType": null,
                "uniqueId": null,
                "uniqueIdType": null,
                "address": {
                    "type": "home",
                    "postOfficeBox": "",
                    "street": "",
                    "city": "",
                    "state": "",
                    "countryOrRegion": "",
                    "postalCode": ""
                },
                "coordinates": {
                    "altitude": null,
                    "latitude": null,
                    "longitude": null,
                    "accuracy": null,
                    "altitudeAccuracy": null
                }
            },
            "start": {
                "dateTime": "2018-05-05T12:00:00.0000000Z",
                "timeZone": "UTC"
            },
            "end": {
                "dateTime": "2018-05-05T12:30:00.0000000Z",
                "timeZone": "UTC"
            },
            "serviceLocation": {
                "displayName": "Customer location (876 Tenth Avenue, Buffalo, NY 98052, USA)",
                "locationEmailAddress": null,
                "locationUri": "",
                "locationType": null,
                "uniqueId": null,
                "uniqueIdType": null,
                "address": {
                    "type": "home",
                    "postOfficeBox": "",
                    "street": "",
                    "city": "",
                    "state": "",
                    "countryOrRegion": "",
                    "postalCode": ""
                },
                "coordinates": {
                    "altitude": null,
                    "latitude": null,
                    "longitude": null,
                    "accuracy": null,
                    "altitudeAccuracy": null
                }
            },
            "reminders": [],
            "invoiceDate": {
                "dateTime": "2018-05-05T12:30:00.0000000Z",
                "timeZone": "UTC"
            }
        },
        {
            "id": "AAMkADKnAAA=",
            "selfServiceAppointmentId": "00000000-0000-0000-0000-000000000000",
            "customerId": "7ed53fa5-9ef2-4f2f-975b-27447440bc09",
            "customerName": "Jordan Miller",
            "customerEmailAddress": "jordanm@contoso.com",
            "customerPhone": "213-555-0199",
            "customerNotes": null,
            "serviceId": "57da6774-a087-4d69-b0e6-6fb82c339976",
            "serviceName": "Catered bento",
            "duration": "PT30M",
            "preBuffer": "PT5M",
            "postBuffer": "PT10M",
            "priceType": "fixedPrice",
            "price": 10,
            "serviceNotes": null,
            "optOutOfCustomerEmail": false,
            "staffMemberIds": [],
            "invoiceAmount": 10,
            "invoiceId": "1001",
            "invoiceStatus": "open",
            "invoiceUrl": "theInvoiceUrl",
            "customerLocation": {
                "displayName": "Customer",
                "locationEmailAddress": null,
                "locationUri": "",
                "locationType": null,
                "uniqueId": null,
                "uniqueIdType": null,
                "address": {
                    "type": "home",
                    "postOfficeBox": "",
                    "street": "",
                    "city": "",
                    "state": "",
                    "countryOrRegion": "",
                    "postalCode": ""
                },
                "coordinates": {
                    "altitude": null,
                    "latitude": null,
                    "longitude": null,
                    "accuracy": null,
                    "altitudeAccuracy": null
                }
            },
            "start": {
                "dateTime": "2018-05-06T12:00:00.0000000Z",
                "timeZone": "UTC"
            },
            "end": {
                "dateTime": "2018-05-06T12:30:00.0000000Z",
                "timeZone": "UTC"
            },
            "serviceLocation": {
                "displayName": "Customer location (123 First Avenue, Buffalo, NY 98052, USA)",
                "locationEmailAddress": null,
                "locationUri": "",
                "locationType": null,
                "uniqueId": null,
                "uniqueIdType": null,
                "address": {
                    "type": "home",
                    "postOfficeBox": "",
                    "street": "",
                    "city": "",
                    "state": "",
                    "countryOrRegion": "",
                    "postalCode": ""
                },
                "coordinates": {
                    "altitude": null,
                    "latitude": null,
                    "longitude": null,
                    "accuracy": null,
                    "altitudeAccuracy": null
                }
            },
            "reminders": [],
            "invoiceDate": {
                "dateTime": "2018-05-06T12:30:00.0000000Z",
                "timeZone": "UTC"
            }
        }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "bookingBusiness: getCalendarView",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
