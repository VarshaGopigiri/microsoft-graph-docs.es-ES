---
title: tipo de recurso bookingStaffMember
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
ms.openlocfilehash: 382da1b0710b691a6563a40c03ed62397262911d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27884458"
---
# <a name="bookingstaffmember-resource-type"></a><span data-ttu-id="599e6-104">tipo de recurso bookingStaffMember</span><span class="sxs-lookup"><span data-stu-id="599e6-104">bookingStaffMember resource type</span></span>

 > <span data-ttu-id="599e6-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="599e6-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="599e6-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="599e6-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="599e6-107">Representa a un miembro del personal que proporciona servicios en un [bookingBusiness](bookingbusiness.md).</span><span class="sxs-lookup"><span data-stu-id="599e6-107">Represents a staff member who provides services in a [bookingBusiness](bookingbusiness.md).</span></span>

<span data-ttu-id="599e6-108">Los miembros del personal pueden formar parte del inquilino de Office 355 donde está configurado el negocio de reserva, o bien pueden usar servicios de correo electrónico de otros proveedores de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="599e6-108">Staff members can be part of the Office 355 tenant where the booking business is configured, or they can use email services from other email providers.</span></span>

<span data-ttu-id="599e6-109">Cuando las citas de reserva, la API de reservas tiene en cuenta la siguiente configuración para determinar la disponibilidad de un miembro del personal:</span><span class="sxs-lookup"><span data-stu-id="599e6-109">When booking appointments, the Bookings API considers the following settings to determine a staff member's availability:</span></span> 

1. <span data-ttu-id="599e6-110">De forma predeterminada, las horas de operación de la empresa (la propiedad **businessHours** de la entidad [bookingBusiness](bookingbusiness.md) ) representa la disponibilidad general de los empleados.</span><span class="sxs-lookup"><span data-stu-id="599e6-110">By default, the hours of operation of the business (the **businessHours** property of the [bookingBusiness](bookingbusiness.md) entity) represents the general availability of the staff member.</span></span>
2. <span data-ttu-id="599e6-111">Si **useBusinessHours** es false, horas de trabajo específicos de los empleados (**workingHours** (propiedad) de la entidad **bookingStaffmember** ) representa la disponibilidad general de dicho miembro.</span><span class="sxs-lookup"><span data-stu-id="599e6-111">If **useBusinessHours** is false, then the staff member's specific work hours (**workingHours** property of the **bookingStaffmember** entity) represents that member's general availability.</span></span>
3. <span data-ttu-id="599e6-112">Si **availabilityIsAffectedByPersonalCalendar** es true, a continuación, la API de reservas tendría en primer lugar buscar generalmente disponibles de las horas de los empleados (según determine #1 o 2 #) y comprobar la disponibilidad durante las horas de personal de los empleados calendario, antes de realizar una reserva.</span><span class="sxs-lookup"><span data-stu-id="599e6-112">If **availabilityIsAffectedByPersonalCalendar** is true, then the Bookings API would first look at the staff member's generally available hours (as determined by either #1 or #2), and verify availability during those hours in the staff member's personal calendar, before making a booking.</span></span>

## <a name="methods"></a><span data-ttu-id="599e6-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="599e6-113">Methods</span></span>

| <span data-ttu-id="599e6-114">Método</span><span class="sxs-lookup"><span data-stu-id="599e6-114">Method</span></span>           | <span data-ttu-id="599e6-115">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="599e6-115">Return Type</span></span>    |<span data-ttu-id="599e6-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="599e6-116">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="599e6-117">Miembros del personal de lista</span><span class="sxs-lookup"><span data-stu-id="599e6-117">List staff members</span></span>](../api/bookingbusiness-list-staffmembers.md) | <span data-ttu-id="599e6-118">colección de [bookingStaffMember](bookingstaffmember.md)</span><span class="sxs-lookup"><span data-stu-id="599e6-118">[bookingStaffMember](bookingstaffmember.md) collection</span></span> | <span data-ttu-id="599e6-119">Para obtener una lista de objetos de **bookingStaffMember** en el especificado [bookingbusiness](../resources/bookingbusiness.md).</span><span class="sxs-lookup"><span data-stu-id="599e6-119">Get a list of **bookingStaffMember** objects in the specified [bookingbusiness](../resources/bookingbusiness.md).</span></span> |
|[<span data-ttu-id="599e6-120">Crear bookingStaff</span><span class="sxs-lookup"><span data-stu-id="599e6-120">Create bookingStaff</span></span>](../api/bookingbusiness-post-staffmembers.md) | <span data-ttu-id="599e6-121">colección de [bookingStaffMember](bookingstaffmember.md)</span><span class="sxs-lookup"><span data-stu-id="599e6-121">[bookingStaffMember](bookingstaffmember.md) collection</span></span> | <span data-ttu-id="599e6-122">Crear un nuevo **bookingStaffMember** en la [bookingbusiness](../resources/bookingbusiness.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="599e6-122">Create a new **bookingStaffMember** in the specified [bookingbusiness](../resources/bookingbusiness.md).</span></span> |
|[<span data-ttu-id="599e6-123">Obtener bookingStaffMember</span><span class="sxs-lookup"><span data-stu-id="599e6-123">Get bookingStaffMember</span></span>](../api/bookingstaffmember-get.md) | [<span data-ttu-id="599e6-124">bookingStaffMember</span><span class="sxs-lookup"><span data-stu-id="599e6-124">bookingStaffMember</span></span>](bookingstaffmember.md) |<span data-ttu-id="599e6-125">Obtener las propiedades y relaciones de un **bookingStaffMember** en la [bookingbusiness](../resources/bookingbusiness.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="599e6-125">Get the properties and relationships of a **bookingStaffMember** in the specified [bookingbusiness](../resources/bookingbusiness.md).</span></span>|
|[<span data-ttu-id="599e6-126">Update</span><span class="sxs-lookup"><span data-stu-id="599e6-126">Update</span></span>](../api/bookingstaffmember-update.md) | [<span data-ttu-id="599e6-127">bookingStaffMember</span><span class="sxs-lookup"><span data-stu-id="599e6-127">bookingStaffMember</span></span>](bookingstaffmember.md)    |<span data-ttu-id="599e6-128">Actualizar las propiedades de un **bookingStaffMember** en la [bookingbusiness](../resources/bookingbusiness.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="599e6-128">Update the properties of a **bookingStaffMember** in the specified [bookingbusiness](../resources/bookingbusiness.md).</span></span>|
|[<span data-ttu-id="599e6-129">Delete</span><span class="sxs-lookup"><span data-stu-id="599e6-129">Delete</span></span>](../api/bookingstaffmember-delete.md) | <span data-ttu-id="599e6-130">Ninguno</span><span class="sxs-lookup"><span data-stu-id="599e6-130">None</span></span> |<span data-ttu-id="599e6-131">Eliminar a un miembro del personal en el especificado [bookingbusiness](../resources/bookingbusiness.md).</span><span class="sxs-lookup"><span data-stu-id="599e6-131">Delete a staff member in the specified [bookingbusiness](../resources/bookingbusiness.md).</span></span> |

## <a name="properties"></a><span data-ttu-id="599e6-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="599e6-132">Properties</span></span>
| <span data-ttu-id="599e6-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="599e6-133">Property</span></span>     | <span data-ttu-id="599e6-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="599e6-134">Type</span></span>   |<span data-ttu-id="599e6-135">Description</span><span class="sxs-lookup"><span data-stu-id="599e6-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="599e6-136">availabilityIsAffectedByPersonalCalendar</span><span class="sxs-lookup"><span data-stu-id="599e6-136">availabilityIsAffectedByPersonalCalendar</span></span>|<span data-ttu-id="599e6-137">Booleano</span><span class="sxs-lookup"><span data-stu-id="599e6-137">Boolean</span></span>|<span data-ttu-id="599e6-138">True significa que si el miembro del personal es un usuario de Office 365, la API de reservas debería comprobar disponibilidad de los empleados en su calendario personal en Office 365, antes de realizar una reserva.</span><span class="sxs-lookup"><span data-stu-id="599e6-138">True means that if the staff member is an Office 365 user, the Bookings API would verify the staff member's availability in their personal calendar in Office 365, before making a booking.</span></span> |
|<span data-ttu-id="599e6-139">colorIndex</span><span class="sxs-lookup"><span data-stu-id="599e6-139">colorIndex</span></span>|<span data-ttu-id="599e6-140">Int32</span><span class="sxs-lookup"><span data-stu-id="599e6-140">Int32</span></span>|<span data-ttu-id="599e6-141">Identifica un color para representar al miembro del personal.</span><span class="sxs-lookup"><span data-stu-id="599e6-141">Identifies a color to represent the staff member.</span></span> <span data-ttu-id="599e6-142">El color se corresponde con la paleta de colores en la página de **Detalles del personal** en la aplicación de reservas.</span><span class="sxs-lookup"><span data-stu-id="599e6-142">The color corresponds to the color palette in the **Staff details** page in the Bookings app.</span></span>|
|<span data-ttu-id="599e6-143">displayName</span><span class="sxs-lookup"><span data-stu-id="599e6-143">displayName</span></span>|<span data-ttu-id="599e6-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="599e6-144">String</span></span>|<span data-ttu-id="599e6-145">El nombre del miembro del personal, tal como se muestra a los clientes.</span><span class="sxs-lookup"><span data-stu-id="599e6-145">The name of the staff member, as displayed to customers.</span></span> <span data-ttu-id="599e6-146">Necesario.</span><span class="sxs-lookup"><span data-stu-id="599e6-146">Required.</span></span>|
|<span data-ttu-id="599e6-147">emailAddress</span><span class="sxs-lookup"><span data-stu-id="599e6-147">emailAddress</span></span>|<span data-ttu-id="599e6-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="599e6-148">String</span></span>|<span data-ttu-id="599e6-149">La dirección de correo electrónico del miembro del personal.</span><span class="sxs-lookup"><span data-stu-id="599e6-149">The email address of the staff member.</span></span> <span data-ttu-id="599e6-150">Esto puede ser en el mismo arrendatario de Office 365 como la empresa o en un dominio de correo electrónico diferentes.</span><span class="sxs-lookup"><span data-stu-id="599e6-150">This can be in the same Office 365 tenant as the business, or in a different email domain.</span></span> <span data-ttu-id="599e6-151">Se puede usar esta dirección de correo electrónico si la propiedad **sendConfirmationsToOwner** está establecida en true en la directiva de programación de la empresa.</span><span class="sxs-lookup"><span data-stu-id="599e6-151">This email address can be used if the **sendConfirmationsToOwner** property is set to true in the scheduling policy of the business.</span></span> <span data-ttu-id="599e6-152">Necesario.</span><span class="sxs-lookup"><span data-stu-id="599e6-152">Required.</span></span>|
|<span data-ttu-id="599e6-153">id</span><span class="sxs-lookup"><span data-stu-id="599e6-153">id</span></span>|<span data-ttu-id="599e6-154">Cadena</span><span class="sxs-lookup"><span data-stu-id="599e6-154">String</span></span>| <span data-ttu-id="599e6-155">El identificador del miembro del personal, en un formato GUID.</span><span class="sxs-lookup"><span data-stu-id="599e6-155">The ID of the staff member, in a GUID format.</span></span> <span data-ttu-id="599e6-156">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="599e6-156">Read-only.</span></span>|
|<span data-ttu-id="599e6-157">role</span><span class="sxs-lookup"><span data-stu-id="599e6-157">role</span></span>|<span data-ttu-id="599e6-158">string</span><span class="sxs-lookup"><span data-stu-id="599e6-158">string</span></span>| <span data-ttu-id="599e6-159">La función del miembro del personal de la empresa.</span><span class="sxs-lookup"><span data-stu-id="599e6-159">The role of the staff member in the business.</span></span> <span data-ttu-id="599e6-160">Los valores posibles son: `guest`, `administrator`, `viewer` y `externalGuest`.</span><span class="sxs-lookup"><span data-stu-id="599e6-160">Possible values are: `guest`, `administrator`, `viewer`, `externalGuest`.</span></span> <span data-ttu-id="599e6-161">Necesario.</span><span class="sxs-lookup"><span data-stu-id="599e6-161">Required.</span></span>|
|<span data-ttu-id="599e6-162">useBusinessHours</span><span class="sxs-lookup"><span data-stu-id="599e6-162">useBusinessHours</span></span>|<span data-ttu-id="599e6-163">Booleano</span><span class="sxs-lookup"><span data-stu-id="599e6-163">Boolean</span></span>|<span data-ttu-id="599e6-164">True significa que la disponibilidad de los empleados es como especificado en la propiedad **businessHours** de la empresa.</span><span class="sxs-lookup"><span data-stu-id="599e6-164">True means the staff member's availability is as specified in the **businessHours** property of the business.</span></span> <span data-ttu-id="599e6-165">False significa que la disponibilidad está determinada por el valor de la propiedad **workingHours** de los empleados.</span><span class="sxs-lookup"><span data-stu-id="599e6-165">False means the availability is determined by the staff member's **workingHours** property setting.</span></span>|
|<span data-ttu-id="599e6-166">workingHours</span><span class="sxs-lookup"><span data-stu-id="599e6-166">workingHours</span></span>|<span data-ttu-id="599e6-167">colección de [bookingWorkHours](bookingworkhours.md)</span><span class="sxs-lookup"><span data-stu-id="599e6-167">[bookingWorkHours](bookingworkhours.md) collection</span></span>|<span data-ttu-id="599e6-168">El intervalo de horas de cada día de la semana en los que el miembro del personal está disponible para reserva.</span><span class="sxs-lookup"><span data-stu-id="599e6-168">The range of hours each day of the week that the staff member is available for booking.</span></span> <span data-ttu-id="599e6-169">De forma predeterminada, se inicializan para ser la misma que la propiedad **businessHours** de la empresa.</span><span class="sxs-lookup"><span data-stu-id="599e6-169">By default, they are initialized to be the same as the **businessHours** property of the business.</span></span>|

## <a name="relationships"></a><span data-ttu-id="599e6-170">Relaciones</span><span class="sxs-lookup"><span data-stu-id="599e6-170">Relationships</span></span>
<span data-ttu-id="599e6-171">Ninguno</span><span class="sxs-lookup"><span data-stu-id="599e6-171">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="599e6-172">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="599e6-172">JSON representation</span></span>

<span data-ttu-id="599e6-173">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="599e6-173">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.bookingStaffMember"
}-->

```json
{
  "availabilityIsAffectedByPersonalCalendar": true,
  "colorIndex": 1024,
  "displayName": "String",
  "emailAddress": "String",
  "id": "String (identifier)",
  "role": "string",
  "useBusinessHours": true,
  "workingHours": [{"@odata.type": "microsoft.graph.bookingWorkHours"}]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "bookingStaffMember resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
