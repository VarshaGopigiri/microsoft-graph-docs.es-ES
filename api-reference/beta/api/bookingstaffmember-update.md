---
title: Actualizar bookingstaffmember
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: 99501f31ccd2b810d6a0c7f836d5b70bb98f223b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084125"
---
# <a name="update-bookingstaffmember"></a><span data-ttu-id="de222-104">Actualizar bookingstaffmember</span><span class="sxs-lookup"><span data-stu-id="de222-104">Update bookingstaffmember</span></span>

 > <span data-ttu-id="de222-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="de222-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="de222-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="de222-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="de222-107">Actualizar las propiedades de un [bookingStaffMember](../resources/bookingstaffmember.md) en la [bookingbusiness](../resources/bookingbusiness.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="de222-107">Update the properties of a [bookingStaffMember](../resources/bookingstaffmember.md) in the specified [bookingbusiness](../resources/bookingbusiness.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="de222-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="de222-108">Permissions</span></span>
<span data-ttu-id="de222-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="de222-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="de222-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="de222-111">Permission type</span></span>      | <span data-ttu-id="de222-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="de222-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="de222-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="de222-113">Delegated (work or school account)</span></span> |  <span data-ttu-id="de222-114">Bookings.ReadWrite.All, Bookings.Manage.All</span><span class="sxs-lookup"><span data-stu-id="de222-114">Bookings.ReadWrite.All, Bookings.Manage.All</span></span>   |
|<span data-ttu-id="de222-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="de222-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="de222-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="de222-116">Not supported.</span></span>   |
|<span data-ttu-id="de222-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="de222-117">Application</span></span> | <span data-ttu-id="de222-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="de222-118">Not supported.</span></span>  | 

## <a name="http-request"></a><span data-ttu-id="de222-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="de222-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /bookingBusinesses/{id}/staffMembers/{id}
```
## <a name="optional-request-headers"></a><span data-ttu-id="de222-120">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="de222-120">Optional request headers</span></span>
| <span data-ttu-id="de222-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="de222-121">Name</span></span>       | <span data-ttu-id="de222-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="de222-122">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="de222-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="de222-123">Authorization</span></span>  | <span data-ttu-id="de222-124">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="de222-124">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="de222-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="de222-125">Request body</span></span>
<span data-ttu-id="de222-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="de222-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="de222-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="de222-129">Property</span></span>     | <span data-ttu-id="de222-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="de222-130">Type</span></span>   |<span data-ttu-id="de222-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="de222-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="de222-132">availabilityIsAffectedByPersonalCalendar</span><span class="sxs-lookup"><span data-stu-id="de222-132">availabilityIsAffectedByPersonalCalendar</span></span>|<span data-ttu-id="de222-133">Booleano</span><span class="sxs-lookup"><span data-stu-id="de222-133">Boolean</span></span>|<span data-ttu-id="de222-134">True significa que, si el miembro del personal es un usuario de Office 365, la API de reservas usa calendario personal de los empleados en Office 365, así como la propiedad **workingHours** para determinar la disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="de222-134">True means that if the staff member is an Office 365 user, the Bookings API uses the staff member's personal calendar in Office 365 as well as the **workingHours** property to determine availability.</span></span> |
|<span data-ttu-id="de222-135">colorIndex</span><span class="sxs-lookup"><span data-stu-id="de222-135">colorIndex</span></span>|<span data-ttu-id="de222-136">Int32</span><span class="sxs-lookup"><span data-stu-id="de222-136">Int32</span></span>|<span data-ttu-id="de222-137">Identifica un color para representar al miembro del personal.</span><span class="sxs-lookup"><span data-stu-id="de222-137">Identifies a color to represent the staff member.</span></span> <span data-ttu-id="de222-138">El color se corresponde con la paleta de colores en la página de **Detalles del personal** en la aplicación de reservas.</span><span class="sxs-lookup"><span data-stu-id="de222-138">The color corresponds to the color palette in the **Staff details** page in the Bookings app.</span></span>|
|<span data-ttu-id="de222-139">displayName</span><span class="sxs-lookup"><span data-stu-id="de222-139">displayName</span></span>|<span data-ttu-id="de222-140">String</span><span class="sxs-lookup"><span data-stu-id="de222-140">String</span></span>|<span data-ttu-id="de222-141">El nombre del miembro del personal, tal como se muestra a los clientes.</span><span class="sxs-lookup"><span data-stu-id="de222-141">The name of the staff member, as displayed to customers.</span></span>|
|<span data-ttu-id="de222-142">emailAddress</span><span class="sxs-lookup"><span data-stu-id="de222-142">emailAddress</span></span>|<span data-ttu-id="de222-143">String</span><span class="sxs-lookup"><span data-stu-id="de222-143">String</span></span>|<span data-ttu-id="de222-144">La dirección de correo electrónico del miembro del personal.</span><span class="sxs-lookup"><span data-stu-id="de222-144">The email address of the staff member.</span></span> <span data-ttu-id="de222-145">Esto puede ser en el mismo arrendatario de Office 365 como la empresa o en un dominio de correo electrónico diferentes.</span><span class="sxs-lookup"><span data-stu-id="de222-145">This can be in the same Office 365 tenant as the business, or in a different email domain.</span></span> <span data-ttu-id="de222-146">Se utiliza esta dirección de correo electrónico si la propiedad **sendConfirmationsToOwner** está establecida en true en la directiva de programación de la empresa.</span><span class="sxs-lookup"><span data-stu-id="de222-146">This email address is used if the **sendConfirmationsToOwner** property is set to true in the scheduling policy of the business.</span></span>|
|<span data-ttu-id="de222-147">role</span><span class="sxs-lookup"><span data-stu-id="de222-147">role</span></span>|<span data-ttu-id="de222-148">string</span><span class="sxs-lookup"><span data-stu-id="de222-148">string</span></span>| <span data-ttu-id="de222-149">La función del miembro del personal de la empresa.</span><span class="sxs-lookup"><span data-stu-id="de222-149">The role of the staff member in the business.</span></span> <span data-ttu-id="de222-150">Los valores posibles son: `guest`, `administrator`, `viewer` y `externalGuest`.</span><span class="sxs-lookup"><span data-stu-id="de222-150">Possible values are: `guest`, `administrator`, `viewer`, `externalGuest`.</span></span>|
|<span data-ttu-id="de222-151">useBusinessHours</span><span class="sxs-lookup"><span data-stu-id="de222-151">useBusinessHours</span></span>|<span data-ttu-id="de222-152">Booleano</span><span class="sxs-lookup"><span data-stu-id="de222-152">Boolean</span></span>|<span data-ttu-id="de222-153">True significa que la disponibilidad de los empleados se determina por la propiedad **businessHours** de la empresa.</span><span class="sxs-lookup"><span data-stu-id="de222-153">True means the staff member's availability is determined by the **businessHours** property of the business.</span></span> <span data-ttu-id="de222-154">False significa que la disponibilidad está determinada por el valor de la propiedad **workingHouse** de los empleados.</span><span class="sxs-lookup"><span data-stu-id="de222-154">False means the availability is determined by the staff member's **workingHouse** property setting.</span></span>|
|<span data-ttu-id="de222-155">workingHours</span><span class="sxs-lookup"><span data-stu-id="de222-155">workingHours</span></span>|<span data-ttu-id="de222-156">colección de [bookingWorkHours](../resources/bookingworkhours.md)</span><span class="sxs-lookup"><span data-stu-id="de222-156">[bookingWorkHours](../resources/bookingworkhours.md) collection</span></span>|<span data-ttu-id="de222-157">El intervalo de horas de cada día de la semana en los que el miembro del personal está disponible para reserva.</span><span class="sxs-lookup"><span data-stu-id="de222-157">The range of hours each day of the week that the staff member is available for booking.</span></span>|

## <a name="response"></a><span data-ttu-id="de222-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="de222-158">Response</span></span>
<span data-ttu-id="de222-p109">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="de222-p109">If successful, this method returns a `204 No content` response code. It does not return anything in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="de222-161">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="de222-161">Example</span></span>
##### <a name="request"></a><span data-ttu-id="de222-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="de222-162">Request</span></span>
<span data-ttu-id="de222-163">En el ejemplo siguiente se cambia la programación de los empleados tengan el lunes.</span><span class="sxs-lookup"><span data-stu-id="de222-163">The following example changes the staff member's schedule to have Mondays off.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_bookingstaffmember"
}-->
```http
PATCH https://graph.microsoft.com/beta/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/staffmembers/8ee1c803-a1fa-406d-8259-7ab53233f148
Content-type: application/json

{
    "workingHours":[
        {
            "@odata.type":"#microsoft.graph.bookingWorkHours",
            "day@odata.type":"#microsoft.graph.dayOfWeek",
            "day":"monday",
            "timeSlots@odata.type":"#Collection(microsoft.graph.bookingWorkTimeSlot)",
            "timeSlots":[
   
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
##### <a name="response"></a><span data-ttu-id="de222-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="de222-164">Response</span></span>
<span data-ttu-id="de222-165">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="de222-165">The following is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update bookingstaffmember",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->