---
title: Obtener bookingService
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: 25ced555f4962ef073f6f01c4eed4767ad1c9e01
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084093"
---
# <a name="get-bookingservice"></a><span data-ttu-id="e88b5-104">Obtener bookingService</span><span class="sxs-lookup"><span data-stu-id="e88b5-104">Get bookingService</span></span>

 > <span data-ttu-id="e88b5-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e88b5-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e88b5-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e88b5-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="e88b5-107">Obtener las propiedades y relaciones de un objeto [bookingService](../resources/bookingservice.md) en la [bookingbusiness](../resources/bookingbusiness.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="e88b5-107">Get the properties and relationships of a [bookingService](../resources/bookingservice.md) object in the specified [bookingbusiness](../resources/bookingbusiness.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="e88b5-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="e88b5-108">Permissions</span></span>
<span data-ttu-id="e88b5-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e88b5-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e88b5-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e88b5-111">Permission type</span></span>      | <span data-ttu-id="e88b5-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e88b5-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e88b5-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e88b5-113">Delegated (work or school account)</span></span> |  <span data-ttu-id="e88b5-114">Bookings.Read.All, BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span><span class="sxs-lookup"><span data-stu-id="e88b5-114">Bookings.Read.All, BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span></span>   |
|<span data-ttu-id="e88b5-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e88b5-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e88b5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e88b5-116">Not supported.</span></span>   |
|<span data-ttu-id="e88b5-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e88b5-117">Application</span></span> | <span data-ttu-id="e88b5-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e88b5-118">Not supported.</span></span>  | 

## <a name="http-request"></a><span data-ttu-id="e88b5-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e88b5-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /bookingBusinesses/{id}/services/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="e88b5-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e88b5-120">Optional query parameters</span></span>
<span data-ttu-id="e88b5-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e88b5-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="e88b5-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e88b5-122">Request headers</span></span>
| <span data-ttu-id="e88b5-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="e88b5-123">Name</span></span>      |<span data-ttu-id="e88b5-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="e88b5-124">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="e88b5-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="e88b5-125">Authorization</span></span>  | <span data-ttu-id="e88b5-126">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="e88b5-126">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="e88b5-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e88b5-127">Request body</span></span>
<span data-ttu-id="e88b5-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e88b5-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="e88b5-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e88b5-129">Response</span></span>
<span data-ttu-id="e88b5-130">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [bookingService](../resources/bookingservice.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e88b5-130">If successful, this method returns a `200 OK` response code and [bookingService](../resources/bookingservice.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e88b5-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e88b5-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e88b5-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e88b5-132">Request</span></span>
<span data-ttu-id="e88b5-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e88b5-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_bookingservice"
}-->
```http
GET https://graph.microsoft.com/beta/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/services/57da6774-a087-4d69-b0e6-6fb82c339976
```
##### <a name="response"></a><span data-ttu-id="e88b5-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e88b5-134">Response</span></span>
<span data-ttu-id="e88b5-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e88b5-135">The following is an example of the response.</span></span> <span data-ttu-id="e88b5-136">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="e88b5-136">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="e88b5-137">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e88b5-137">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.bookingService"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#bookingBusinesses('Contosolunchdelivery%40M365B489948.onmicrosoft.com')/services/$entity",
    "id": "57da6774-a087-4d69-b0e6-6fb82c339976",
    "displayName": "Bento",
    "defaultDuration": "PT30M",
    "defaultPrice": 10,
    "defaultPriceType": "fixedPrice",
    "description": "Individual bento box lunch delivery",
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
    "defaultReminders": [
        {
            "offset": "P1D",
            "recipients": "allAttendees",
            "message": "Please be reminded that this service is tomorrow."
        }
    ],
    "schedulingPolicy": {
        "timeSlotInterval": "PT1H",
        "minimumLeadTime": "PT10H",
        "maximumAdvance": "P10D",
        "sendConfirmationsToOwner": true,
        "allowStaffSelection": true
    }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get bookingService",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->