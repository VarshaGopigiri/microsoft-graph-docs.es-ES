---
title: Citas de lista
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
author: angelgolfer-ms
ms.prod: bookings
ms.openlocfilehash: 3334e4db060868fa7b514d50d1d879e4d0182b08
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27946845"
---
# <a name="list-appointments"></a><span data-ttu-id="fda8b-104">Citas de lista</span><span class="sxs-lookup"><span data-stu-id="fda8b-104">List appointments</span></span>

 > <span data-ttu-id="fda8b-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fda8b-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fda8b-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fda8b-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="fda8b-107">Obtener una lista de objetos de [bookingAppointment](../resources/bookingappointment.md) para el [bookingbusiness](../resources/bookingbusiness.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="fda8b-107">Get a list of [bookingAppointment](../resources/bookingappointment.md) objects for the specified [bookingbusiness](../resources/bookingbusiness.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="fda8b-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="fda8b-108">Permissions</span></span>
<span data-ttu-id="fda8b-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fda8b-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fda8b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fda8b-111">Permission type</span></span>      | <span data-ttu-id="fda8b-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fda8b-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fda8b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fda8b-113">Delegated (work or school account)</span></span> |  <span data-ttu-id="fda8b-114">Bookings.Read.All, BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span><span class="sxs-lookup"><span data-stu-id="fda8b-114">Bookings.Read.All, BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span></span>   |
|<span data-ttu-id="fda8b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fda8b-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fda8b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fda8b-116">Not supported.</span></span>   |
|<span data-ttu-id="fda8b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fda8b-117">Application</span></span> | <span data-ttu-id="fda8b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fda8b-118">Not supported.</span></span>  | 

## <a name="http-request"></a><span data-ttu-id="fda8b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fda8b-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /bookingBusinesses/{id}/appointments
```
## <a name="optional-query-parameters"></a><span data-ttu-id="fda8b-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="fda8b-120">Optional query parameters</span></span>
<span data-ttu-id="fda8b-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fda8b-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="fda8b-122">Para obtener el conjunto de citas de una empresa de reservas dentro de un intervalo de fechas, en lugar de `$filter`, [obtener el calendarView](bookingbusiness-list-calendarview.md) para ese intervalo de fechas.</span><span class="sxs-lookup"><span data-stu-id="fda8b-122">To get the set of appointments of a Bookings business within a date range, instead of `$filter`, [get the calendarView](bookingbusiness-list-calendarview.md) for that date range.</span></span> 

## <a name="request-headers"></a><span data-ttu-id="fda8b-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fda8b-123">Request headers</span></span>
| <span data-ttu-id="fda8b-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="fda8b-124">Name</span></span>      |<span data-ttu-id="fda8b-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="fda8b-125">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="fda8b-126">Autorización</span><span class="sxs-lookup"><span data-stu-id="fda8b-126">Authorization</span></span>  | <span data-ttu-id="fda8b-127">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="fda8b-127">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="fda8b-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fda8b-128">Request body</span></span>
<span data-ttu-id="fda8b-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="fda8b-129">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="fda8b-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fda8b-130">Response</span></span>
<span data-ttu-id="fda8b-131">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [bookingAppointment](../resources/bookingappointment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fda8b-131">If successful, this method returns a `200 OK` response code and collection of [bookingAppointment](../resources/bookingappointment.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="fda8b-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fda8b-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="fda8b-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fda8b-133">Request</span></span>
<span data-ttu-id="fda8b-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fda8b-134">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_appointments"
}-->
```http
GET https://graph.microsoft.com/beta/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/appointments
```
##### <a name="response"></a><span data-ttu-id="fda8b-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fda8b-135">Response</span></span>
<span data-ttu-id="fda8b-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fda8b-136">The following is an example of the response.</span></span> <span data-ttu-id="fda8b-137">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="fda8b-137">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="fda8b-138">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fda8b-138">All of the properties will be returned from an actual call.</span></span>
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
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#bookingBusinesses('Contosolunchdelivery%40M365B489948.onmicrosoft.com')/appointments",
    "value": [
        {
            "id": "AAMkADKoAAA=",
            "selfServiceAppointmentId": "00000000-0000-0000-0000-000000000000",
            "customerId": "829e3cb5-3d4d-4319-a8de-1953aedaa166",
            "customerName": "Bob Kelly",
            "customerEmailAddress": "bobk@tailspintoys.com",
            "customerPhone": "213-555-0108",
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
            "invoiceId": "1002",
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
                "dateTime": "2018-04-30T13:00:00.0000000Z",
                "timeZone": "UTC"
            },
            "end": {
                "dateTime": "2018-04-30T13:30:00.0000000Z",
                "timeZone": "UTC"
            },
            "serviceLocation": {
                "displayName": "Customer location (987 Third Avenue, Buffalo, NY 98052, USA)",
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
                "dateTime": "2018-04-30T13:30:00.0000000Z",
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
                "dateTime": "2018-05-01T12:00:00.0000000Z",
                "timeZone": "UTC"
            },
            "end": {
                "dateTime": "2018-05-01T12:30:00.0000000Z",
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
                "dateTime": "2018-05-01T12:30:00.0000000Z",
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
  "description": "List appointments",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
