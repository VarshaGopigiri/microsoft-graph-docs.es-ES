---
title: Crear bookingStaffMember
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
ms.openlocfilehash: 43935dbeeda30fb5f69b799993f772ffffa3eeed
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27838776"
---
# <a name="create-bookingstaffmember"></a><span data-ttu-id="a2493-104">Crear bookingStaffMember</span><span class="sxs-lookup"><span data-stu-id="a2493-104">Create bookingStaffMember</span></span>

 > <span data-ttu-id="a2493-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a2493-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a2493-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a2493-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="a2493-107">Crear un nuevo [miembro del personal](../resources/bookingstaffmember.md) en el especificado [bookingbusiness](../resources/bookingbusiness.md).</span><span class="sxs-lookup"><span data-stu-id="a2493-107">Create a new [staff member](../resources/bookingstaffmember.md) in the specified [bookingbusiness](../resources/bookingbusiness.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="a2493-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="a2493-108">Permissions</span></span>
<span data-ttu-id="a2493-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a2493-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a2493-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a2493-111">Permission type</span></span>      | <span data-ttu-id="a2493-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a2493-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a2493-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a2493-113">Delegated (work or school account)</span></span> |  <span data-ttu-id="a2493-114">Bookings.ReadWrite.All, Bookings.Manage.All</span><span class="sxs-lookup"><span data-stu-id="a2493-114">Bookings.ReadWrite.All, Bookings.Manage.All</span></span>   |
|<span data-ttu-id="a2493-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a2493-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a2493-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a2493-116">Not supported.</span></span>   |
|<span data-ttu-id="a2493-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a2493-117">Application</span></span> | <span data-ttu-id="a2493-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a2493-118">Not supported.</span></span>  |

## <a name="http-request"></a><span data-ttu-id="a2493-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a2493-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /bookingBusinesses/{id}/staffMembers

```
## <a name="request-headers"></a><span data-ttu-id="a2493-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a2493-120">Request headers</span></span>
| <span data-ttu-id="a2493-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="a2493-121">Name</span></span>       | <span data-ttu-id="a2493-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2493-122">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="a2493-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="a2493-123">Authorization</span></span>  | <span data-ttu-id="a2493-124">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="a2493-124">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="a2493-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a2493-125">Request body</span></span>
<span data-ttu-id="a2493-126">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [bookingStaffMember](../resources/bookingstaffmember.md) .</span><span class="sxs-lookup"><span data-stu-id="a2493-126">In the request body, supply a JSON representation of [bookingStaffMember](../resources/bookingstaffmember.md) object.</span></span> <span data-ttu-id="a2493-127">Debe incluir las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="a2493-127">You must include the following properties:</span></span>

- <span data-ttu-id="a2493-128">**displayName**</span><span class="sxs-lookup"><span data-stu-id="a2493-128">**displayName**</span></span>
- <span data-ttu-id="a2493-129">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="a2493-129">**emailAddress**</span></span>
- <span data-ttu-id="a2493-130">**rol**</span><span class="sxs-lookup"><span data-stu-id="a2493-130">**role**</span></span>


## <a name="response"></a><span data-ttu-id="a2493-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2493-131">Response</span></span>
<span data-ttu-id="a2493-132">Si tiene éxito, este método devuelve `201, Created` objeto de código y [bookingStaffMember](../resources/bookingstaffmember.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2493-132">If successful, this method returns `201, Created` response code and [bookingStaffMember](../resources/bookingstaffmember.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a2493-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a2493-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a2493-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a2493-134">Request</span></span>
<span data-ttu-id="a2493-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a2493-135">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_bookingstaffmember_from_bookingbusiness"
}-->
```http
POST https://graph.microsoft.com/beta/bookingBusinesses/{id}/staffMembers
Content-type: application/json
Content-length: 309

{
    "@odata.type":"#microsoft.graph.bookingStaffMember",
    "colorIndex":1,
    "displayName":"Dana Swope",
    "emailAddress":"danas@contoso.com",
    "role@odata.type":"#microsoft.graph.bookingStaffRole",
    "role":"externalGuest",
    "useBusinessHours":true,
    "workingHours@odata.type":"#Collection(microsoft.graph.bookingWorkHours)",
    "workingHours":[
        {
            "@odata.type":"#microsoft.graph.bookingWorkHours",
            "day@odata.type":"#microsoft.graph.dayOfWeek",
            "day":"monday",
            "timeSlots@odata.type":"#Collection(microsoft.graph.bookingWorkTimeSlot)",
            "timeSlots":[
                {
                    "@odata.type":"#microsoft.graph.bookingWorkTimeSlot",
                    "end":"17:00:00.0000000",
                    "start":"08:00:00.0000000"
                }
            ]
        },
        {
            "@odata.type":"#microsoft.graph.bookingWorkHours",
            "day@odata.type":"#microsoft.graph.dayOfWeek",
            "day":"tuesday",
            "timeSlots@odata.type":"#Collection(microsoft.graph.bookingWorkTimeSlot)",
            "timeSlots":[
                {
                    "@odata.type":"#microsoft.graph.bookingWorkTimeSlot",
                    "end":"17:00:00.0000000",
                    "start":"08:00:00.0000000"
                }
            ]
        },
        {
            "@odata.type":"#microsoft.graph.bookingWorkHours",
            "day@odata.type":"#microsoft.graph.dayOfWeek",
            "day":"wednesday",
            "timeSlots@odata.type":"#Collection(microsoft.graph.bookingWorkTimeSlot)",
            "timeSlots":[
                {
                    "@odata.type":"#microsoft.graph.bookingWorkTimeSlot",
                    "end":"17:00:00.0000000",
                    "start":"08:00:00.0000000"
                }
            ]
        },
        {
            "@odata.type":"#microsoft.graph.bookingWorkHours",
            "day@odata.type":"#microsoft.graph.dayOfWeek",
            "day":"thursday",
            "timeSlots@odata.type":"#Collection(microsoft.graph.bookingWorkTimeSlot)",
            "timeSlots":[
                {
                    "@odata.type":"#microsoft.graph.bookingWorkTimeSlot",
                    "end":"17:00:00.0000000",
                    "start":"08:00:00.0000000"
                }
            ]
        },
        {
            "@odata.type":"#microsoft.graph.bookingWorkHours",
            "day@odata.type":"#microsoft.graph.dayOfWeek",
            "day":"friday",
            "timeSlots@odata.type":"#Collection(microsoft.graph.bookingWorkTimeSlot)",
            "timeSlots":[
                {
                    "@odata.type":"#microsoft.graph.bookingWorkTimeSlot",
                    "end":"17:00:00.0000000",
                    "start":"08:00:00.0000000"
                }
            ]
        }
    ]
}
```
<span data-ttu-id="a2493-136">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [bookingStaffMember](../resources/bookingstaffmember.md) .</span><span class="sxs-lookup"><span data-stu-id="a2493-136">In the request body, supply a JSON representation of [bookingStaffMember](../resources/bookingstaffmember.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="a2493-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2493-137">Response</span></span>
<span data-ttu-id="a2493-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2493-138">The following is an example of the response.</span></span> <span data-ttu-id="a2493-139">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="a2493-139">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="a2493-140">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a2493-140">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.bookingStaffMember"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#bookingBusinesses('Contosolunchdelivery%40M365B489948.onmicrosoft.com')/staffMembers/$entity",
    "id":"8ee1c803-a1fa-406d-8259-7ab53233f148",
    "displayName":"Dana Swope",
    "emailAddress":"danas@contoso.com",
    "availabilityIsAffectedByPersonalCalendar":false,
    "colorIndex":1,
    "role":"externalGuest",
    "useBusinessHours":true,
    "workingHours":[
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
        }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create bookingStaffMember",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
