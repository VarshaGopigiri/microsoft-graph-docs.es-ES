---
title: Obtener bookingStaffMember
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
author: angelgolfer-ms
ms.prod: bookings
ms.openlocfilehash: ad550bbcc1608d3770d8047f6081fc20fd419822
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27956895"
---
# <a name="get-bookingstaffmember"></a><span data-ttu-id="df118-104">Obtener bookingStaffMember</span><span class="sxs-lookup"><span data-stu-id="df118-104">Get bookingStaffMember</span></span>

 > <span data-ttu-id="df118-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="df118-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="df118-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="df118-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="df118-107">Obtener las propiedades y relaciones de un [bookingStaffMember](../resources/bookingstaffmember.md) en la [bookingbusiness](../resources/bookingbusiness.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="df118-107">Get the properties and relationships of a [bookingStaffMember](../resources/bookingstaffmember.md) in the specified [bookingbusiness](../resources/bookingbusiness.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="df118-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="df118-108">Permissions</span></span>
<span data-ttu-id="df118-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="df118-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="df118-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="df118-111">Permission type</span></span>      | <span data-ttu-id="df118-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="df118-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="df118-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="df118-113">Delegated (work or school account)</span></span> |  <span data-ttu-id="df118-114">Bookings.Read.All, BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span><span class="sxs-lookup"><span data-stu-id="df118-114">Bookings.Read.All, BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All</span></span>   |
|<span data-ttu-id="df118-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="df118-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="df118-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="df118-116">Not supported.</span></span>   |
|<span data-ttu-id="df118-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="df118-117">Application</span></span> | <span data-ttu-id="df118-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="df118-118">Not supported.</span></span>  | 

## <a name="http-request"></a><span data-ttu-id="df118-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="df118-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /bookingBusinesses/{id}/staffMembers/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="df118-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="df118-120">Optional query parameters</span></span>
<span data-ttu-id="df118-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="df118-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="df118-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="df118-122">Request headers</span></span>
| <span data-ttu-id="df118-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="df118-123">Name</span></span>      |<span data-ttu-id="df118-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="df118-124">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="df118-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="df118-125">Authorization</span></span>  | <span data-ttu-id="df118-126">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="df118-126">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="df118-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="df118-127">Request body</span></span>
<span data-ttu-id="df118-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="df118-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="df118-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="df118-129">Response</span></span>
<span data-ttu-id="df118-130">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [bookingStaffMember](../resources/bookingstaffmember.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="df118-130">If successful, this method returns a `200 OK` response code and [bookingStaffMember](../resources/bookingstaffmember.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="df118-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="df118-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="df118-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="df118-132">Request</span></span>
<span data-ttu-id="df118-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="df118-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_bookingstaffmember"
}-->
```http
GET https://graph.microsoft.com/beta/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/staffmembers/71d64d0e-7225-49b6-b0b1-070d476cda51
```
##### <a name="response"></a><span data-ttu-id="df118-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="df118-134">Response</span></span>
<span data-ttu-id="df118-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="df118-135">The following is an example of the response.</span></span> <span data-ttu-id="df118-136">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="df118-136">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="df118-137">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="df118-137">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.bookingStaffMember"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#bookingBusinesses('Contosolunchdelivery%40M365B489948.onmicrosoft.com')/staffMembers/$entity",
    "id": "71d64d0e-7225-49b6-b0b1-070d476cda51",
    "displayName": "Samantha Booth",
    "emailAddress": "samanthab@M365B489948.OnMicrosoft.com",
    "availabilityIsAffectedByPersonalCalendar": true,
    "colorIndex": 0,
    "role": "administrator",
    "useBusinessHours": true,
    "workingHours": [
        {
            "day": "monday",
            "timeSlots": [
                {
                    "start": "08:00:00.0000000",
                    "end": "17:00:00.0000000"
                }
            ]
        },
        {
            "day": "tuesday",
            "timeSlots": [
                {
                    "start": "08:00:00.0000000",
                    "end": "17:00:00.0000000"
                }
            ]
        },
        {
            "day": "wednesday",
            "timeSlots": [
                {
                    "start": "08:00:00.0000000",
                    "end": "17:00:00.0000000"
                }
            ]
        },
        {
            "day": "thursday",
            "timeSlots": [
                {
                    "start": "08:00:00.0000000",
                    "end": "17:00:00.0000000"
                }
            ]
        },
        {
            "day": "friday",
            "timeSlots": [
                {
                    "start": "08:00:00.0000000",
                    "end": "17:00:00.0000000"
                }
            ]
        },
        {
            "day": "saturday",
            "timeSlots": []
        },
        {
            "day": "sunday",
            "timeSlots": []
        }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get bookingStaffMember",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
