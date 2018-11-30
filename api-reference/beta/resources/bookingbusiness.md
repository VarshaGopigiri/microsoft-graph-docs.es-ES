---
title: tipo de recurso bookingBusiness
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: 0ea11dcd16a129e6d6648be4b09435c5c052de9e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086756"
---
# <a name="bookingbusiness-resource-type"></a><span data-ttu-id="fa787-104">tipo de recurso bookingBusiness</span><span class="sxs-lookup"><span data-stu-id="fa787-104">bookingBusiness resource type</span></span>

 > <span data-ttu-id="fa787-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fa787-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fa787-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fa787-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="fa787-107">Representa una empresa en Microsoft Bookings.</span><span class="sxs-lookup"><span data-stu-id="fa787-107">Represents a business in Microsoft Bookings.</span></span> <span data-ttu-id="fa787-108">Esto es el objeto de nivel superior de la API de reservas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fa787-108">This is the top level object in the Microsoft Bookings API.</span></span> <span data-ttu-id="fa787-109">Contiene información de la empresa y los objetos de negocio relacionados, como las citas, los clientes, servicios y los miembros del personal.</span><span class="sxs-lookup"><span data-stu-id="fa787-109">It contains business information and related business objects such as appointments, customers, services, and staff members.</span></span>

## <a name="methods"></a><span data-ttu-id="fa787-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="fa787-110">Methods</span></span>

| <span data-ttu-id="fa787-111">Método</span><span class="sxs-lookup"><span data-stu-id="fa787-111">Method</span></span>           | <span data-ttu-id="fa787-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fa787-112">Return Type</span></span>    |<span data-ttu-id="fa787-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa787-113">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="fa787-114">Lista bookingBusinesses</span><span class="sxs-lookup"><span data-stu-id="fa787-114">List bookingBusinesses</span></span>](../api/bookingbusiness-list.md) | <span data-ttu-id="fa787-115">colección de [bookingBusiness](bookingbusiness.md)</span><span class="sxs-lookup"><span data-stu-id="fa787-115">[bookingBusiness](bookingbusiness.md) collection</span></span> |<span data-ttu-id="fa787-116">Obtener una colección de objetos de bookingbusiness en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="fa787-116">Get a collection of bookingbusiness objects in the tenant.</span></span> |
|[<span data-ttu-id="fa787-117">Crear bookingBusiness</span><span class="sxs-lookup"><span data-stu-id="fa787-117">Create bookingBusiness</span></span>](../api/bookingbusiness-post-bookingbusinesses.md) | [<span data-ttu-id="fa787-118">bookingBusiness</span><span class="sxs-lookup"><span data-stu-id="fa787-118">bookingBusiness</span></span>](bookingbusiness.md) | <span data-ttu-id="fa787-119">Crear un nuevo negocio de Microsoft Bookings.</span><span class="sxs-lookup"><span data-stu-id="fa787-119">Create a new Microsoft Bookings business.</span></span> |
|[<span data-ttu-id="fa787-120">Obtener bookingBusiness</span><span class="sxs-lookup"><span data-stu-id="fa787-120">Get bookingBusiness</span></span>](../api/bookingbusiness-get.md) | [<span data-ttu-id="fa787-121">bookingBusiness</span><span class="sxs-lookup"><span data-stu-id="fa787-121">bookingBusiness</span></span>](bookingbusiness.md) |<span data-ttu-id="fa787-122">Leer las propiedades y las relaciones del objeto bookingBusiness.</span><span class="sxs-lookup"><span data-stu-id="fa787-122">Read properties and relationships of bookingBusiness object.</span></span>|
|[<span data-ttu-id="fa787-123">Update</span><span class="sxs-lookup"><span data-stu-id="fa787-123">Update</span></span>](../api/bookingbusiness-update.md) | [<span data-ttu-id="fa787-124">bookingBusiness</span><span class="sxs-lookup"><span data-stu-id="fa787-124">bookingBusiness</span></span>](bookingbusiness.md) |<span data-ttu-id="fa787-125">Actualizar las propiedades de un objeto **bookingBusiness** .</span><span class="sxs-lookup"><span data-stu-id="fa787-125">Update properties in a **bookingBusiness** object.</span></span> |
|[<span data-ttu-id="fa787-126">Delete</span><span class="sxs-lookup"><span data-stu-id="fa787-126">Delete</span></span>](../api/bookingbusiness-delete.md) | <span data-ttu-id="fa787-127">Ninguno</span><span class="sxs-lookup"><span data-stu-id="fa787-127">None</span></span> |<span data-ttu-id="fa787-128">Eliminar un objeto **bookingBusiness** .</span><span class="sxs-lookup"><span data-stu-id="fa787-128">Delete a **bookingBusiness** object.</span></span> |
|[<span data-ttu-id="fa787-129">Crear bookingAppointment</span><span class="sxs-lookup"><span data-stu-id="fa787-129">Create bookingAppointment</span></span>](../api/bookingbusiness-post-appointments.md) |[<span data-ttu-id="fa787-130">bookingAppointment</span><span class="sxs-lookup"><span data-stu-id="fa787-130">bookingAppointment</span></span>](bookingappointment.md)| <span data-ttu-id="fa787-131">Crear un nuevo bookingAppointment por la publicación de la colección de citas.</span><span class="sxs-lookup"><span data-stu-id="fa787-131">Create a new bookingAppointment by posting to the appointments collection.</span></span>|
|[<span data-ttu-id="fa787-132">Citas de lista</span><span class="sxs-lookup"><span data-stu-id="fa787-132">List appointments</span></span>](../api/bookingbusiness-list-appointments.md) |<span data-ttu-id="fa787-133">colección de [bookingAppointment](bookingappointment.md)</span><span class="sxs-lookup"><span data-stu-id="fa787-133">[bookingAppointment](bookingappointment.md) collection</span></span>| <span data-ttu-id="fa787-134">Obtener una colección de objetos bookingAppointment.</span><span class="sxs-lookup"><span data-stu-id="fa787-134">Get a bookingAppointment object collection.</span></span>|
|[<span data-ttu-id="fa787-135">Crear bookingCustomer</span><span class="sxs-lookup"><span data-stu-id="fa787-135">Create bookingCustomer</span></span>](../api/bookingbusiness-post-customers.md) |[<span data-ttu-id="fa787-136">bookingCustomer</span><span class="sxs-lookup"><span data-stu-id="fa787-136">bookingCustomer</span></span>](bookingcustomer.md)| <span data-ttu-id="fa787-137">Crear un nuevo bookingCustomer por la publicación de la colección de los clientes.</span><span class="sxs-lookup"><span data-stu-id="fa787-137">Create a new bookingCustomer by posting to the customers collection.</span></span>|
|[<span data-ttu-id="fa787-138">Clientes de la lista</span><span class="sxs-lookup"><span data-stu-id="fa787-138">List customers</span></span>](../api/bookingbusiness-list-customers.md) |<span data-ttu-id="fa787-139">colección de [bookingCustomer](bookingcustomer.md)</span><span class="sxs-lookup"><span data-stu-id="fa787-139">[bookingCustomer](bookingcustomer.md) collection</span></span>| <span data-ttu-id="fa787-140">Obtener una colección de objetos bookingCustomer.</span><span class="sxs-lookup"><span data-stu-id="fa787-140">Get a bookingCustomer object collection.</span></span>|
|[<span data-ttu-id="fa787-141">Crear bookingService</span><span class="sxs-lookup"><span data-stu-id="fa787-141">Create bookingService</span></span>](../api/bookingbusiness-post-services.md) |[<span data-ttu-id="fa787-142">bookingService</span><span class="sxs-lookup"><span data-stu-id="fa787-142">bookingService</span></span>](bookingservice.md)| <span data-ttu-id="fa787-143">Crear un nuevo bookingService por la publicación de la colección de servicios.</span><span class="sxs-lookup"><span data-stu-id="fa787-143">Create a new bookingService by posting to the services collection.</span></span>|
|[<span data-ttu-id="fa787-144">Servicios de la lista</span><span class="sxs-lookup"><span data-stu-id="fa787-144">List services</span></span>](../api/bookingbusiness-list-services.md) |<span data-ttu-id="fa787-145">colección de [bookingService](bookingservice.md)</span><span class="sxs-lookup"><span data-stu-id="fa787-145">[bookingService](bookingservice.md) collection</span></span>| <span data-ttu-id="fa787-146">Obtener una colección de objetos bookingService.</span><span class="sxs-lookup"><span data-stu-id="fa787-146">Get a bookingService object collection.</span></span>|
|[<span data-ttu-id="fa787-147">Crear bookingStaffMember</span><span class="sxs-lookup"><span data-stu-id="fa787-147">Create bookingStaffMember</span></span>](../api/bookingbusiness-post-staffmembers.md) |[<span data-ttu-id="fa787-148">bookingStaffMember</span><span class="sxs-lookup"><span data-stu-id="fa787-148">bookingStaffMember</span></span>](bookingstaffmember.md)| <span data-ttu-id="fa787-149">Crear un nuevo bookingStaffMember por la publicación de la colección staffMembers.</span><span class="sxs-lookup"><span data-stu-id="fa787-149">Create a new bookingStaffMember by posting to the staffMembers collection.</span></span>|
|[<span data-ttu-id="fa787-150">Lista staffMembers</span><span class="sxs-lookup"><span data-stu-id="fa787-150">List staffMembers</span></span>](../api/bookingbusiness-list-staffmembers.md) |<span data-ttu-id="fa787-151">colección de [bookingStaffMember](bookingstaffmember.md)</span><span class="sxs-lookup"><span data-stu-id="fa787-151">[bookingStaffMember](bookingstaffmember.md) collection</span></span>| <span data-ttu-id="fa787-152">Obtener una colección de objetos bookingStaffMember.</span><span class="sxs-lookup"><span data-stu-id="fa787-152">Get a bookingStaffMember object collection.</span></span>|
|[<span data-ttu-id="fa787-153">Lista de calendarView</span><span class="sxs-lookup"><span data-stu-id="fa787-153">List calendarView</span></span>](../api/bookingbusiness-list-calendarview.md)|<span data-ttu-id="fa787-154">colección de [bookingAppointment](bookingappointment.md)</span><span class="sxs-lookup"><span data-stu-id="fa787-154">[bookingAppointment](bookingappointment.md) collection</span></span>|<span data-ttu-id="fa787-155">Obtener la colección de objetos **bookingAppointment** que se produce en el intervalo de fechas especificado.</span><span class="sxs-lookup"><span data-stu-id="fa787-155">Get the collection of **bookingAppointment** objects that occurs in the specified date range.</span></span>|
|[<span data-ttu-id="fa787-156">publicar</span><span class="sxs-lookup"><span data-stu-id="fa787-156">publish</span></span>](../api/bookingbusiness-publish.md)|<span data-ttu-id="fa787-157">Ninguno</span><span class="sxs-lookup"><span data-stu-id="fa787-157">None</span></span>|<span data-ttu-id="fa787-158">Ponga la página programación de este negocio a disposición de los clientes externos.</span><span class="sxs-lookup"><span data-stu-id="fa787-158">Make the scheduling page of this business available to external customers.</span></span> <span data-ttu-id="fa787-159">Establezca la propiedad **isPublished** en true y la propiedad **publicUrl** a la dirección URL de la página de programación.</span><span class="sxs-lookup"><span data-stu-id="fa787-159">Set the **isPublished** property to true, and **publicUrl** property to the URL of the scheduling page.</span></span>|
|[<span data-ttu-id="fa787-160">Cancelar la publicación</span><span class="sxs-lookup"><span data-stu-id="fa787-160">unpublish</span></span>](../api/bookingbusiness-unpublish.md)|<span data-ttu-id="fa787-161">Ninguno</span><span class="sxs-lookup"><span data-stu-id="fa787-161">None</span></span>| <span data-ttu-id="fa787-162">Hacer que la página programación de esta empresa no está disponible para los clientes externos.</span><span class="sxs-lookup"><span data-stu-id="fa787-162">Make the scheduling page of this business not available to external customers.</span></span> <span data-ttu-id="fa787-163">Establezca la propiedad **isPublished** en false y la propiedad **publicUrl** en null.</span><span class="sxs-lookup"><span data-stu-id="fa787-163">Set the **isPublished** property to false, and **publicUrl** property to null.</span></span>|

## <a name="properties"></a><span data-ttu-id="fa787-164">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fa787-164">Properties</span></span>
| <span data-ttu-id="fa787-165">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fa787-165">Property</span></span>     | <span data-ttu-id="fa787-166">Tipo</span><span class="sxs-lookup"><span data-stu-id="fa787-166">Type</span></span>   |<span data-ttu-id="fa787-167">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa787-167">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fa787-168">address</span><span class="sxs-lookup"><span data-stu-id="fa787-168">address</span></span>|[<span data-ttu-id="fa787-169">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="fa787-169">physicalAddress</span></span>](physicaladdress.md)|<span data-ttu-id="fa787-170">La dirección de la empresa.</span><span class="sxs-lookup"><span data-stu-id="fa787-170">The street address of the business.</span></span> <span data-ttu-id="fa787-171">La propiedad **address** , junto con el **teléfono** y **webSiteUrl**, aparecen en el pie de página de un página de programación de negocio.</span><span class="sxs-lookup"><span data-stu-id="fa787-171">The **address** property, together with **phone** and **webSiteUrl**, appear in the footer of a business scheduling page.</span></span>|
|<span data-ttu-id="fa787-172">businessHours</span><span class="sxs-lookup"><span data-stu-id="fa787-172">businessHours</span></span>|<span data-ttu-id="fa787-173">colección de [bookingWorkHours](bookingworkhours.md)</span><span class="sxs-lookup"><span data-stu-id="fa787-173">[bookingWorkHours](bookingworkhours.md) collection</span></span>|<span data-ttu-id="fa787-174">Las horas de operación para la empresa.</span><span class="sxs-lookup"><span data-stu-id="fa787-174">The hours of operation for the business.</span></span>|
|<span data-ttu-id="fa787-175">businessType</span><span class="sxs-lookup"><span data-stu-id="fa787-175">businessType</span></span>|<span data-ttu-id="fa787-176">String</span><span class="sxs-lookup"><span data-stu-id="fa787-176">String</span></span>|<span data-ttu-id="fa787-177">El tipo de negocio.</span><span class="sxs-lookup"><span data-stu-id="fa787-177">The type of business.</span></span>|
|<span data-ttu-id="fa787-178">defaultCurrencyIso</span><span class="sxs-lookup"><span data-stu-id="fa787-178">defaultCurrencyIso</span></span>|<span data-ttu-id="fa787-179">String</span><span class="sxs-lookup"><span data-stu-id="fa787-179">String</span></span>|<span data-ttu-id="fa787-180">El código para la moneda que la empresa opera en Microsoft Bookings.</span><span class="sxs-lookup"><span data-stu-id="fa787-180">The code for the currency that the business operates in on Microsoft Bookings.</span></span>|
|<span data-ttu-id="fa787-181">displayName</span><span class="sxs-lookup"><span data-stu-id="fa787-181">displayName</span></span>|<span data-ttu-id="fa787-182">String</span><span class="sxs-lookup"><span data-stu-id="fa787-182">String</span></span>|<span data-ttu-id="fa787-183">El nombre de la empresa, las interfaces con los clientes.</span><span class="sxs-lookup"><span data-stu-id="fa787-183">The name of the business, which interfaces with customers.</span></span> <span data-ttu-id="fa787-184">Este nombre aparece en la parte superior de la página de programación de empresa.</span><span class="sxs-lookup"><span data-stu-id="fa787-184">This name appears at the top of the business scheduling page.</span></span>|
|<span data-ttu-id="fa787-185">email</span><span class="sxs-lookup"><span data-stu-id="fa787-185">email</span></span>|<span data-ttu-id="fa787-186">String</span><span class="sxs-lookup"><span data-stu-id="fa787-186">String</span></span>|<span data-ttu-id="fa787-187">La dirección de correo electrónico para el negocio.</span><span class="sxs-lookup"><span data-stu-id="fa787-187">The email address for the business.</span></span>|
|<span data-ttu-id="fa787-188">id</span><span class="sxs-lookup"><span data-stu-id="fa787-188">id</span></span>|<span data-ttu-id="fa787-189">String</span><span class="sxs-lookup"><span data-stu-id="fa787-189">String</span></span>|<span data-ttu-id="fa787-190">Un identificador de programación único para el negocio.</span><span class="sxs-lookup"><span data-stu-id="fa787-190">A unique programmatic identifier for the business.</span></span> <span data-ttu-id="fa787-191">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fa787-191">Read-only.</span></span>|
|<span data-ttu-id="fa787-192">isPublished</span><span class="sxs-lookup"><span data-stu-id="fa787-192">isPublished</span></span>|<span data-ttu-id="fa787-193">Booleano</span><span class="sxs-lookup"><span data-stu-id="fa787-193">Boolean</span></span>|<span data-ttu-id="fa787-194">La página de programación se realizó disponible para los clientes externos.</span><span class="sxs-lookup"><span data-stu-id="fa787-194">The scheduling page has been made available to external customers.</span></span> <span data-ttu-id="fa787-195">Use las acciones de **Publicar** y **Cancelar la publicación** para establecer esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="fa787-195">Use the **publish** and **unpublish** actions to set this property.</span></span> <span data-ttu-id="fa787-196">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fa787-196">Read-only.</span></span>|
|<span data-ttu-id="fa787-197">phone</span><span class="sxs-lookup"><span data-stu-id="fa787-197">phone</span></span>|<span data-ttu-id="fa787-198">String</span><span class="sxs-lookup"><span data-stu-id="fa787-198">String</span></span>|<span data-ttu-id="fa787-199">El número de teléfono para el negocio.</span><span class="sxs-lookup"><span data-stu-id="fa787-199">The telephone number for the business.</span></span> <span data-ttu-id="fa787-200">La propiedad de **teléfono** , junto con la **dirección** y **webSiteUrl**, aparecen en el pie de página de un página de programación de negocio.</span><span class="sxs-lookup"><span data-stu-id="fa787-200">The **phone** property, together with **address** and **webSiteUrl**, appear in the footer of a business scheduling page.</span></span>|
|<span data-ttu-id="fa787-201">publicUrl</span><span class="sxs-lookup"><span data-stu-id="fa787-201">publicUrl</span></span>|<span data-ttu-id="fa787-202">String</span><span class="sxs-lookup"><span data-stu-id="fa787-202">String</span></span>|<span data-ttu-id="fa787-203">La dirección URL de la página de programación, que se establece después de [Publicar](../api/bookingbusiness-publish.md) o [Cancelar la publicación de](../api/bookingbusiness-unpublish.md) la página.</span><span class="sxs-lookup"><span data-stu-id="fa787-203">The URL for the scheduling page, which is set after you [publish](../api/bookingbusiness-publish.md) or [unpublish](../api/bookingbusiness-unpublish.md) the page.</span></span> <span data-ttu-id="fa787-204">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fa787-204">Read-only.</span></span>|
|<span data-ttu-id="fa787-205">schedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="fa787-205">schedulingPolicy</span></span>|[<span data-ttu-id="fa787-206">bookingSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="fa787-206">bookingSchedulingPolicy</span></span>](bookingschedulingpolicy.md)|<span data-ttu-id="fa787-207">Especifica cómo se pueden crear reservas para este negocio.</span><span class="sxs-lookup"><span data-stu-id="fa787-207">Specifies how bookings can be created for this business.</span></span>|
|<span data-ttu-id="fa787-208">webSiteUrl</span><span class="sxs-lookup"><span data-stu-id="fa787-208">webSiteUrl</span></span>|<span data-ttu-id="fa787-209">String</span><span class="sxs-lookup"><span data-stu-id="fa787-209">String</span></span>|<span data-ttu-id="fa787-210">La dirección URL del sitio web de negocio.</span><span class="sxs-lookup"><span data-stu-id="fa787-210">The URL of the business web site.</span></span> <span data-ttu-id="fa787-211">La propiedad **webSiteUrl** , junto con la **dirección**, **teléfono**, aparecen en el pie de página de una página de programación de negocio.</span><span class="sxs-lookup"><span data-stu-id="fa787-211">The **webSiteUrl** property, together with **address**, **phone**, appear in the footer of a business scheduling page.</span></span>|

## <a name="relationships"></a><span data-ttu-id="fa787-212">Relaciones</span><span class="sxs-lookup"><span data-stu-id="fa787-212">Relationships</span></span>
| <span data-ttu-id="fa787-213">Relación</span><span class="sxs-lookup"><span data-stu-id="fa787-213">Relationship</span></span> | <span data-ttu-id="fa787-214">Tipo</span><span class="sxs-lookup"><span data-stu-id="fa787-214">Type</span></span>   |<span data-ttu-id="fa787-215">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa787-215">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fa787-216">appointments</span><span class="sxs-lookup"><span data-stu-id="fa787-216">appointments</span></span>|<span data-ttu-id="fa787-217">colección de [bookingAppointment](bookingappointment.md)</span><span class="sxs-lookup"><span data-stu-id="fa787-217">[bookingAppointment](bookingappointment.md) collection</span></span>| <span data-ttu-id="fa787-218">Todas las citas de esta empresa.</span><span class="sxs-lookup"><span data-stu-id="fa787-218">All the appointments of this business.</span></span> <span data-ttu-id="fa787-219">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fa787-219">Read-only.</span></span> <span data-ttu-id="fa787-220">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="fa787-220">Nullable.</span></span>|
|<span data-ttu-id="fa787-221">calendarView</span><span class="sxs-lookup"><span data-stu-id="fa787-221">calendarView</span></span>|<span data-ttu-id="fa787-222">colección de [bookingAppointment](bookingappointment.md)</span><span class="sxs-lookup"><span data-stu-id="fa787-222">[bookingAppointment](bookingappointment.md) collection</span></span>| <span data-ttu-id="fa787-223">El conjunto de citas de esta empresa en un intervalo de fechas especificado.</span><span class="sxs-lookup"><span data-stu-id="fa787-223">The set of appointments of this business in a specified date range.</span></span> <span data-ttu-id="fa787-224">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fa787-224">Read-only.</span></span> <span data-ttu-id="fa787-225">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="fa787-225">Nullable.</span></span>|
|<span data-ttu-id="fa787-226">clientes</span><span class="sxs-lookup"><span data-stu-id="fa787-226">customers</span></span>|<span data-ttu-id="fa787-227">colección de [bookingCustomer](bookingcustomer.md)</span><span class="sxs-lookup"><span data-stu-id="fa787-227">[bookingCustomer](bookingcustomer.md) collection</span></span>| <span data-ttu-id="fa787-228">Todos los clientes de este negocio.</span><span class="sxs-lookup"><span data-stu-id="fa787-228">All the customers of this business.</span></span> <span data-ttu-id="fa787-229">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fa787-229">Read-only.</span></span> <span data-ttu-id="fa787-230">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="fa787-230">Nullable.</span></span>|
|<span data-ttu-id="fa787-231">servicios</span><span class="sxs-lookup"><span data-stu-id="fa787-231">services</span></span>|<span data-ttu-id="fa787-232">colección de [bookingService](bookingservice.md)</span><span class="sxs-lookup"><span data-stu-id="fa787-232">[bookingService](bookingservice.md) collection</span></span>| <span data-ttu-id="fa787-233">Todos los servicios ofrecidos por esta empresa.</span><span class="sxs-lookup"><span data-stu-id="fa787-233">All the services offered by this business.</span></span> <span data-ttu-id="fa787-234">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fa787-234">Read-only.</span></span> <span data-ttu-id="fa787-235">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="fa787-235">Nullable.</span></span>|
|<span data-ttu-id="fa787-236">staffMembers</span><span class="sxs-lookup"><span data-stu-id="fa787-236">staffMembers</span></span>|<span data-ttu-id="fa787-237">colección de [bookingStaffMember](bookingstaffmember.md)</span><span class="sxs-lookup"><span data-stu-id="fa787-237">[bookingStaffMember](bookingstaffmember.md) collection</span></span>| <span data-ttu-id="fa787-238">Todos los personal miembros que proporcionan servicios en este negocio.</span><span class="sxs-lookup"><span data-stu-id="fa787-238">All the staff members that provide services in this business.</span></span> <span data-ttu-id="fa787-239">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fa787-239">Read-only.</span></span> <span data-ttu-id="fa787-240">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="fa787-240">Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="fa787-241">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fa787-241">JSON representation</span></span>

<span data-ttu-id="fa787-242">Esta es una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="fa787-242">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.bookingBusiness"
}-->

```json
{
  "address": {"@odata.type": "microsoft.graph.physicalAddress"},
  "businessHours": [{"@odata.type": "microsoft.graph.bookingWorkHours"}],
  "businessType": "String",
  "defaultCurrencyIso": "String",
  "displayName": "String",
  "email": "String",
  "id": "String (identifier)",
  "isPublished": true,
  "phone": "String",
  "publicUrl": "String",
  "schedulingPolicy": {"@odata.type": "microsoft.graph.bookingSchedulingPolicy"},
  "webSiteUrl": "String"
}

```

## <a name="see-also"></a><span data-ttu-id="fa787-243">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa787-243">See also</span></span>


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "bookingBusiness resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->