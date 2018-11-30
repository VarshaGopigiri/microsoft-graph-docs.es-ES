---
title: Obtener bookingBusiness
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: 809bfad0685f595b4b8076210c6345760b22f3bc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085343"
---
# <a name="get-bookingbusiness"></a><span data-ttu-id="ff7f0-104">Obtener bookingBusiness</span><span class="sxs-lookup"><span data-stu-id="ff7f0-104">Get bookingBusiness</span></span>

 > <span data-ttu-id="ff7f0-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ff7f0-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ff7f0-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ff7f0-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="ff7f0-107">Obtener las propiedades y relaciones de un objeto [bookingBusiness](../resources/bookingbusiness.md) .</span><span class="sxs-lookup"><span data-stu-id="ff7f0-107">Get the properties and relationships of a [bookingBusiness](../resources/bookingbusiness.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="ff7f0-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="ff7f0-108">Permissions</span></span>
<span data-ttu-id="ff7f0-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ff7f0-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ff7f0-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ff7f0-111">Permission type</span></span>      | <span data-ttu-id="ff7f0-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ff7f0-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ff7f0-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ff7f0-113">Delegated (work or school account)</span></span> |  <span data-ttu-id="ff7f0-114">Bookings.Read.All, BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span><span class="sxs-lookup"><span data-stu-id="ff7f0-114">Bookings.Read.All, BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span></span>   |
|<span data-ttu-id="ff7f0-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ff7f0-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ff7f0-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ff7f0-116">Not supported.</span></span>   |
|<span data-ttu-id="ff7f0-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ff7f0-117">Application</span></span> | <span data-ttu-id="ff7f0-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ff7f0-118">Not supported.</span></span>  | 

## <a name="http-request"></a><span data-ttu-id="ff7f0-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ff7f0-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /bookingBusinesses/<id>
```
## <a name="optional-query-parameters"></a><span data-ttu-id="ff7f0-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ff7f0-120">Optional query parameters</span></span>
<span data-ttu-id="ff7f0-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ff7f0-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="ff7f0-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ff7f0-122">Request headers</span></span>
| <span data-ttu-id="ff7f0-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="ff7f0-123">Name</span></span>      |<span data-ttu-id="ff7f0-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff7f0-124">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="ff7f0-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="ff7f0-125">Authorization</span></span>  | <span data-ttu-id="ff7f0-126">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="ff7f0-126">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="ff7f0-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ff7f0-127">Request body</span></span>
<span data-ttu-id="ff7f0-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ff7f0-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="ff7f0-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ff7f0-129">Response</span></span>
<span data-ttu-id="ff7f0-130">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [bookingBusiness](../resources/bookingbusiness.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ff7f0-130">If successful, this method returns a `200 OK` response code and [bookingBusiness](../resources/bookingbusiness.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ff7f0-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ff7f0-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ff7f0-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ff7f0-132">Request</span></span>
<span data-ttu-id="ff7f0-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ff7f0-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_bookingbusiness"
}-->
```http
GET https://graph.microsoft.com/beta/bookingBusinesses/Fabrikam@M365B489948.onmicrosoft.com
```
##### <a name="response"></a><span data-ttu-id="ff7f0-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ff7f0-134">Response</span></span>
<span data-ttu-id="ff7f0-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ff7f0-135">The following is an example of the response.</span></span> <span data-ttu-id="ff7f0-136">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="ff7f0-136">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="ff7f0-137">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ff7f0-137">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.bookingBusiness"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#bookingBusinesses/$entity",
    "id":"Fabrikam@M365B489948.onmicrosoft.com",
    "displayName":"Fabrikam",
    "businessType":"",
    "phone":"206-555-0100",
    "email":"manager@fabrikam.com",
    "webSiteUrl":"https://www.fabrikam.com/",
    "defaultCurrencyIso":"USD",
    "isPublished":false,
    "publicUrl":null,
    "address":{
        "type":"home",
        "postOfficeBox":"",
        "street":"4567 Main Street",
        "city":"Buffalo",
        "state":"NY",
        "countryOrRegion":"USA",
        "postalCode":"98052"
    },
    "businessHours":[
        {
            "day":"monday",
            "timeSlots":[
                {
                    "start":"08:00:00.0000000",
                    "end":"17:00:00.0000000"
                }
            ]
        },
        {
            "day":"tuesday",
            "timeSlots":[
                {
                    "start":"08:00:00.0000000",
                    "end":"17:00:00.0000000"
                }
            ]
        },
        {
            "day":"wednesday",
            "timeSlots":[
                {
                    "start":"08:00:00.0000000",
                    "end":"17:00:00.0000000"
                }
            ]
        },
        {
            "day":"thursday",
            "timeSlots":[
                {
                    "start":"08:00:00.0000000",
                    "end":"17:00:00.0000000"
                }
            ]
        },
        {
            "day":"friday",
            "timeSlots":[
                {
                    "start":"08:00:00.0000000",
                    "end":"17:00:00.0000000"
                }
            ]
        },
        {
            "day":"saturday",
            "timeSlots":[

            ]
        },
        {
            "day":"sunday",
            "timeSlots":[

            ]
        }
    ],
    "schedulingPolicy":{
        "timeSlotInterval":"PT30M",
        "minimumLeadTime":"P1D",
        "maximumAdvance":"P365D",
        "sendConfirmationsToOwner":true,
        "allowStaffSelection":true
    }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get bookingBusiness",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->