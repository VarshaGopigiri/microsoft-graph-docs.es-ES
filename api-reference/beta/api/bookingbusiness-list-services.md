---
title: Servicios de la lista
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
author: angelgolfer-ms
ms.prod: bookings
ms.openlocfilehash: 9f00ca7be7c3e6e3633a69a4a21df5e9a556096d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27941712"
---
# <a name="list-services"></a><span data-ttu-id="c0969-104">Servicios de la lista</span><span class="sxs-lookup"><span data-stu-id="c0969-104">List services</span></span>

 > <span data-ttu-id="c0969-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c0969-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c0969-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c0969-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="c0969-107">Para obtener una lista de objetos de [bookingService](../resources/bookingservice.md) en el especificado [bookingbusiness](../resources/bookingbusiness.md).</span><span class="sxs-lookup"><span data-stu-id="c0969-107">Get a list of [bookingService](../resources/bookingservice.md) objects in the specified [bookingbusiness](../resources/bookingbusiness.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="c0969-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="c0969-108">Permissions</span></span>
<span data-ttu-id="c0969-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c0969-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c0969-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c0969-111">Permission type</span></span>      | <span data-ttu-id="c0969-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c0969-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c0969-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c0969-113">Delegated (work or school account)</span></span> |  <span data-ttu-id="c0969-114">Bookings.Read.All, BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span><span class="sxs-lookup"><span data-stu-id="c0969-114">Bookings.Read.All, BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span></span>   |
|<span data-ttu-id="c0969-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c0969-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c0969-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c0969-116">Not supported.</span></span>   |
|<span data-ttu-id="c0969-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c0969-117">Application</span></span> | <span data-ttu-id="c0969-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c0969-118">Not supported.</span></span>  | 

## <a name="http-request"></a><span data-ttu-id="c0969-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c0969-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /bookingBusinesses/{id}/services
```
## <a name="optional-query-parameters"></a><span data-ttu-id="c0969-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c0969-120">Optional query parameters</span></span>
<span data-ttu-id="c0969-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0969-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="c0969-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c0969-122">Request headers</span></span>
| <span data-ttu-id="c0969-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="c0969-123">Name</span></span>      |<span data-ttu-id="c0969-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0969-124">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="c0969-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="c0969-125">Authorization</span></span>  | <span data-ttu-id="c0969-126">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="c0969-126">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="c0969-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c0969-127">Request body</span></span>
<span data-ttu-id="c0969-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c0969-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="c0969-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c0969-129">Response</span></span>
<span data-ttu-id="c0969-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [bookingService](../resources/bookingservice.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0969-130">If successful, this method returns a `200 OK` response code and collection of [bookingService](../resources/bookingservice.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c0969-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c0969-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c0969-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c0969-132">Request</span></span>
<span data-ttu-id="c0969-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c0969-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_services"
}-->
```http
GET https://graph.microsoft.com/beta/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/services
```
##### <a name="response"></a><span data-ttu-id="c0969-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c0969-134">Response</span></span>
<span data-ttu-id="c0969-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0969-135">The following is an example of the response.</span></span> <span data-ttu-id="c0969-136">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="c0969-136">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="c0969-137">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c0969-137">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.bookingService",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#bookingBusinesses('Contosolunchdelivery%40M365B489948.onmicrosoft.com')/services",
    "value": [
        {
            "id": "f9b9121f-aed7-4c8c-bb3a-a1796a0b0b2d",
            "displayName": "Initial service",
            "defaultDuration": "PT10M",
            "defaultPrice": 0,
            "defaultPriceType": "notSet",
            "description": "Not sure how to choose? Let us introduce you to our traditional family recipes.",
            "isHiddenFromCustomers": false,
            "notes": "This is where you can add notes about this service that only you and your staff see.",
            "preBuffer": "PT0S",
            "postBuffer": "PT0S",
            "staffMemberIds": [],
            "schedulingPolicy": null,
            "defaultLocation": {
                "displayName": "Contoso Lunch Delivery",
                "locationEmailAddress": null,
                "locationUri": "",
                "locationType": null,
                "uniqueId": null,
                "uniqueIdType": null,
                "address": {
                    "type": "home",
                    "postOfficeBox": "",
                    "street": "4567 First Street",
                    "city": "Buffalo",
                    "state": "NY",
                    "countryOrRegion": "USA",
                    "postalCode": "98052"
                },
                "coordinates": {
                    "altitude": null,
                    "latitude": null,
                    "longitude": null,
                    "accuracy": null,
                    "altitudeAccuracy": null
                }
            },
            "defaultReminders": []
        },
        {
            "id": "57da6774-a087-4d69-b0e6-6fb82c339976",
            "displayName": "Catered bento",
            "defaultDuration": "PT30M",
            "defaultPrice": 10,
            "defaultPriceType": "fixedPrice",
            "description": "Catered individual bento box lunch",
            "isHiddenFromCustomers": false,
            "notes": "Home-cooked special",
            "preBuffer": "PT5M",
            "postBuffer": "PT10M",
            "staffMemberIds": [],
            "defaultLocation": {
                "displayName": "Contoso Lunch Delivery",
                "locationEmailAddress": null,
                "locationUri": "",
                "locationType": null,
                "uniqueId": null,
                "uniqueIdType": null,
                "address": {
                    "type": "home",
                    "postOfficeBox": "",
                    "street": "4567 First Street",
                    "city": "Buffalo",
                    "state": "NY",
                    "countryOrRegion": "USA",
                    "postalCode": "98052"
                },
                "coordinates": {
                    "altitude": null,
                    "latitude": null,
                    "longitude": null,
                    "accuracy": null,
                    "altitudeAccuracy": null
                }
            },
            "defaultReminders": [],
            "schedulingPolicy": {
                "timeSlotInterval": "PT1H",
                "minimumLeadTime": "PT10H",
                "maximumAdvance": "P10D",
                "sendConfirmationsToOwner": true,
                "allowStaffSelection": true
            }
        },
        {
            "id": "635a7b7c-4230-4d3b-a42b-698e89927528",
            "displayName": "Kaiseki",
            "defaultDuration": "PT1H30M",
            "defaultPrice": 30,
            "defaultPriceType": "fixedPrice",
            "description": "Individual kaiseki lunch delivery",
            "isHiddenFromCustomers": false,
            "notes": "Home-cooked special",
            "preBuffer": "PT5M",
            "postBuffer": "PT10M",
            "staffMemberIds": [],
            "defaultLocation": {
                "displayName": "Contoso Lunch Delivery",
                "locationEmailAddress": null,
                "locationUri": "",
                "locationType": null,
                "uniqueId": null,
                "uniqueIdType": null,
                "address": {
                    "type": "home",
                    "postOfficeBox": "",
                    "street": "4567 First Street",
                    "city": "Buffalo",
                    "state": "NY",
                    "countryOrRegion": "USA",
                    "postalCode": "98052"
                },
                "coordinates": {
                    "altitude": null,
                    "latitude": null,
                    "longitude": null,
                    "accuracy": null,
                    "altitudeAccuracy": null
                }
            },
            "defaultReminders": [],
            "schedulingPolicy": {
                "timeSlotInterval": "PT1H",
                "minimumLeadTime": "PT10H",
                "maximumAdvance": "P10D",
                "sendConfirmationsToOwner": true,
                "allowStaffSelection": true
            }
        }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List services",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
