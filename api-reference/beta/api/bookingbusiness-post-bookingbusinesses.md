---
title: Crear bookingBusiness
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
author: angelgolfer-ms
ms.prod: bookings
ms.openlocfilehash: aa5c4b9eaa2426736d23f42856d19ab14e6a1a43
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27922322"
---
# <a name="create-bookingbusiness"></a><span data-ttu-id="2e57f-104">Crear bookingBusiness</span><span class="sxs-lookup"><span data-stu-id="2e57f-104">Create bookingBusiness</span></span>

 > <span data-ttu-id="2e57f-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2e57f-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2e57f-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2e57f-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="2e57f-107">Crear un nuevo negocio de Microsoft Bookings en un inquilino.</span><span class="sxs-lookup"><span data-stu-id="2e57f-107">Create a new Microsoft Bookings business in a tenant.</span></span> 

<span data-ttu-id="2e57f-108">Esto es el primer paso en la configuración de una empresa de reservas donde debe especificar el nombre para mostrar de negocio.</span><span class="sxs-lookup"><span data-stu-id="2e57f-108">This is the first step in setting up a Bookings business where you must specify the business display name.</span></span> <span data-ttu-id="2e57f-109">Puede incluir otra información como la dirección de la empresa, la dirección del sitio web y la directiva de programación, o establecer esa información más adelante mediante la [actualización de](bookingbusiness-update.md) la **bookingBusiness**.</span><span class="sxs-lookup"><span data-stu-id="2e57f-109">You can include other information such as business address, web site address, and scheduling policy, or set that information later by [updating](bookingbusiness-update.md) the **bookingBusiness**.</span></span>
## <a name="permissions"></a><span data-ttu-id="2e57f-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="2e57f-110">Permissions</span></span>
<span data-ttu-id="2e57f-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2e57f-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2e57f-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2e57f-113">Permission type</span></span>      | <span data-ttu-id="2e57f-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2e57f-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2e57f-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2e57f-115">Delegated (work or school account)</span></span> |  <span data-ttu-id="2e57f-116">Bookings.Manage.All</span><span class="sxs-lookup"><span data-stu-id="2e57f-116">Bookings.Manage.All</span></span>  |
|<span data-ttu-id="2e57f-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2e57f-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2e57f-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2e57f-118">Not supported.</span></span>   |
|<span data-ttu-id="2e57f-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2e57f-119">Application</span></span> | <span data-ttu-id="2e57f-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2e57f-120">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="2e57f-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2e57f-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /bookingBusinesses

```
## <a name="request-headers"></a><span data-ttu-id="2e57f-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2e57f-122">Request headers</span></span>
| <span data-ttu-id="2e57f-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="2e57f-123">Name</span></span>       | <span data-ttu-id="2e57f-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e57f-124">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="2e57f-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="2e57f-125">Authorization</span></span>  | <span data-ttu-id="2e57f-126">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="2e57f-126">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="2e57f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2e57f-127">Request body</span></span>
<span data-ttu-id="2e57f-128">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [bookingBusiness](../resources/bookingbusiness.md) .</span><span class="sxs-lookup"><span data-stu-id="2e57f-128">In the request body, supply a JSON representation of [bookingBusiness](../resources/bookingbusiness.md) object.</span></span>


## <a name="response"></a><span data-ttu-id="2e57f-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2e57f-129">Response</span></span>
<span data-ttu-id="2e57f-130">Si tiene éxito, este método devuelve `201, Created` objeto de código y [bookingBusiness](../resources/bookingbusiness.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2e57f-130">If successful, this method returns `201, Created` response code and [bookingBusiness](../resources/bookingbusiness.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2e57f-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2e57f-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2e57f-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2e57f-132">Request</span></span>
<span data-ttu-id="2e57f-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2e57f-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_bookingbusiness_from_bookingbusinesses"
}-->
```http
POST https://graph.microsoft.com/beta/bookingBusinesses
Content-type: application/json

{
    "displayName":"Fourth Coffee",
    "address":{
        "type":"mall",
        "postOfficeBox":"P.O. Box 123",
        "street":"4567 Main Street",
        "city":"Buffalo",
        "state":"NY",
        "countryOrRegion":"USA",
        "postalCode":"98052"
    },
    "phone":"206-555-0100",
    "email":"manager@fourthcoffee.com",
    "webSiteUrl":"https://www.fourthcoffee.com",
    "defaultCurrencyIso":"USD"
}
```
<span data-ttu-id="2e57f-134">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [bookingBusiness](../resources/bookingbusiness.md) .</span><span class="sxs-lookup"><span data-stu-id="2e57f-134">In the request body, supply a JSON representation of [bookingBusiness](../resources/bookingbusiness.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="2e57f-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2e57f-135">Response</span></span>
<span data-ttu-id="2e57f-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2e57f-136">The following is an example of the response.</span></span> <span data-ttu-id="2e57f-137">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="2e57f-137">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="2e57f-138">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2e57f-138">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.bookingBusiness"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#bookingBusinesses/$entity",
    "id":"fourthcoffee@M365B489948.onmicrosoft.com",
    "displayName":"Fourth Coffee",
    "businessType":"",
    "phone":"206-555-0100",
    "email":"manager@fourthcoffee.com",
    "webSiteUrl":"https://www.fourthcoffee.com",
    "defaultCurrencyIso":"USD",
    "isPublished":false,
    "publicUrl":null,
    "address":{
        "type":"mall",
        "postOfficeBox":"P.O. Box 123",
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
  "description": "Create bookingBusiness",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
