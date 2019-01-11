---
title: Usar la API de reservas de Microsoft en Microsoft Graph
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Priority
ms.openlocfilehash: def9260654baafe1953d629265c4b76a2afd2748
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845538"
---
# <a name="use-the-microsoft-bookings-api-in-microsoft-graph"></a><span data-ttu-id="c2ca6-104">Usar la API de reservas de Microsoft en Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="c2ca6-104">Use the Microsoft Bookings API in Microsoft Graph</span></span>

 > <span data-ttu-id="c2ca6-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c2ca6-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c2ca6-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c2ca6-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="c2ca6-107">Microsoft Bookings permite a los propietarios de pequeñas empresas administrar reservas de cliente y la información con el programa de instalación mínima.</span><span class="sxs-lookup"><span data-stu-id="c2ca6-107">Microsoft Bookings lets small business owners manage customer bookings and information with minimal setup.</span></span> <span data-ttu-id="c2ca6-108">Propietario de una empresa puede crear una o varias empresas, con cada empresa que ofrece un conjunto de servicios.</span><span class="sxs-lookup"><span data-stu-id="c2ca6-108">A business owner can create one or more businesses, with each business offering a set of services.</span></span> <span data-ttu-id="c2ca6-109">El propietario puede configurar los miembros del personal y especificar los servicios que lleva a cabo en cada miembro del personal.</span><span class="sxs-lookup"><span data-stu-id="c2ca6-109">The owner can set up staff members, and specify the services that each staff member performs.</span></span> <span data-ttu-id="c2ca6-110">Un cliente puede reservar una cita para un servicio específico en que los negocios en una aplicación móvil o en línea.</span><span class="sxs-lookup"><span data-stu-id="c2ca6-110">A customer can book an appointment for a specific service in that business in an online or mobile app.</span></span> <span data-ttu-id="c2ca6-111">Las reservas se asegura de que la hora de la cita se mantiene actualizada para el negocio, los miembros del personal y clientes implicado.</span><span class="sxs-lookup"><span data-stu-id="c2ca6-111">Bookings ensures that the appointment time is kept up-to-date for the business, staff members, and customers involved.</span></span>

<span data-ttu-id="c2ca6-112">Mediante programación, un [bookingBusiness](bookingbusiness.md) de la API de reservas implica los siguientes objetos:</span><span class="sxs-lookup"><span data-stu-id="c2ca6-112">Programmatically, a [bookingBusiness](bookingbusiness.md) in the Bookings API involves the following objects:</span></span>
 
- <span data-ttu-id="c2ca6-113">Uno o más objetos [bookingStaffMember](bookingstaffmember.md)</span><span class="sxs-lookup"><span data-stu-id="c2ca6-113">One or more [bookingStaffMember](bookingstaffmember.md) objects</span></span>
- <span data-ttu-id="c2ca6-114">Uno o más objetos [bookingService](bookingservice.md)</span><span class="sxs-lookup"><span data-stu-id="c2ca6-114">One or more [bookingService](bookingservice.md) objects</span></span>
- <span data-ttu-id="c2ca6-115">Un conjunto de instancias de [bookingAppointment](bookingappointment.md)</span><span class="sxs-lookup"><span data-stu-id="c2ca6-115">A set of [bookingAppointment](bookingappointment.md) instances</span></span>
- <span data-ttu-id="c2ca6-116">Un conjunto de objetos de [bookingCustomer](bookingcustomer.md)</span><span class="sxs-lookup"><span data-stu-id="c2ca6-116">A set of [bookingCustomer](bookingcustomer.md) objects</span></span>

## <a name="using-the-bookings-rest-api"></a><span data-ttu-id="c2ca6-117">Uso de la API de REST de reservas</span><span class="sxs-lookup"><span data-stu-id="c2ca6-117">Using the Bookings REST API</span></span>

<span data-ttu-id="c2ca6-118">Eche un vistazo a través de los siguientes pasos antes de citas de cliente para una empresa de reserva por primera vez.</span><span class="sxs-lookup"><span data-stu-id="c2ca6-118">Walk through the following steps before booking customer appointments for a business the first time.</span></span> <span data-ttu-id="c2ca6-119">Asegúrese de que proporcionan los [tokens de acceso](/graph/auth-overview) de adecuada para las operaciones correspondientes.</span><span class="sxs-lookup"><span data-stu-id="c2ca6-119">Make sure you provide the appropriate [access tokens](/graph/auth-overview) for the corresponding operations.</span></span>

1. <span data-ttu-id="c2ca6-120">Asegúrese de que la empresa tiene una suscripción a [Office 365 Business Premium](https://products.office.com/en-us/business/office-365-business-premium) .</span><span class="sxs-lookup"><span data-stu-id="c2ca6-120">Make sure the business has an [Office 365 Business Premium](https://products.office.com/en-us/business/office-365-business-premium) subscription.</span></span>
2. <span data-ttu-id="c2ca6-121">Crear un nuevo **bookingBusiness** mediante el envío de una operación de entrada para el conjunto de entidades.</span><span class="sxs-lookup"><span data-stu-id="c2ca6-121">Create a new **bookingBusiness** by sending a POST operation to the entity set.</span></span> <span data-ttu-id="c2ca6-122">Como mínimo, debe especificar un nombre para el nuevo negocio que verán los clientes:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="c2ca6-122">At minimum, you should specify a name for the new business that customers will see: <!-- { "blockType": "ignored" } --></span></span>
```http
POST https://graph.microsoft.com/beta/bookingBusinesses
Authorization: Bearer {access token}
Content-Type: application/json

{
    "displayName":"Contoso"
}
```
<span data-ttu-id="c2ca6-123">Utilice la propiedad **id** de la nueva **bookingBusiness** devuelto en la respuesta de entrada para continuar para [Personalizar](../api/bookingbusiness-update.md) la configuración del negocio y agregar los miembros del personal y servicios para la empresa.</span><span class="sxs-lookup"><span data-stu-id="c2ca6-123">Use the **id** property of the new **bookingBusiness** returned in the POST response to continue to [customize](../api/bookingbusiness-update.md) business settings, and add staff members and services for the business.</span></span>

3. <span data-ttu-id="c2ca6-124">Agregar a los miembros del personal individuales para el negocio:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="c2ca6-124">Add individual staff members for the business: <!-- { "blockType": "ignored" } --></span></span>
```http
POST https://graph.microsoft.com/beta/bookingBusinesses/{id}/staffMembers
Authorization: Bearer {access token}
Content-Type: application/json

{
    "displayName":"Dana Swope",
    "emailAddress": "danas@contoso.com",
    "role": "externalGuest"
}
```
4. <span data-ttu-id="c2ca6-125">Definir cada servicio ofrecido por la empresa:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="c2ca6-125">Define each service offered by the business: <!-- { "blockType": "ignored" } --></span></span>
```http
POST https://graph.microsoft.com/beta/bookingBusinesses/{id}/services
Authorization: Bearer {access token}
Content-Type: application/json

{
    "displayName":"Bento"
}
```
5. <span data-ttu-id="c2ca6-126">Publicar la página de programación de la empresa, para permitir que a los clientes y los operadores de empresas iniciar citas de reserva:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="c2ca6-126">Publish the scheduling page for the business, to let customers and business operators start booking appointments: <!-- { "blockType": "ignored" } --></span></span>
```http
POST https://graph.microsoft.com/beta/bookingBusinesses/{id}/publish
Authorization: Bearer {access token}
```

<span data-ttu-id="c2ca6-127">En general, una lista de todas las empresas de reserva en el inquilino de Office 365:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="c2ca6-127">In general, to list all the booking businesses in the Office 365 tenant: <!-- { "blockType": "ignored" } --></span></span>
```http
GET https://graph.microsoft.com/beta/bookingBusinesses
Authorization: Bearer {access token}
```

## <a name="common-use-cases"></a><span data-ttu-id="c2ca6-128">Casos de uso común</span><span class="sxs-lookup"><span data-stu-id="c2ca6-128">Common use cases</span></span> 

<span data-ttu-id="c2ca6-129">En la siguiente tabla se enumera las operaciones comunes para una empresa de la API de reservas.</span><span class="sxs-lookup"><span data-stu-id="c2ca6-129">The following table lists the common operations for a business in the Bookings API.</span></span>

| <span data-ttu-id="c2ca6-130">Casos de uso</span><span class="sxs-lookup"><span data-stu-id="c2ca6-130">Use cases</span></span>        | <span data-ttu-id="c2ca6-131">Recursos de REST</span><span class="sxs-lookup"><span data-stu-id="c2ca6-131">REST resources</span></span> | <span data-ttu-id="c2ca6-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2ca6-132">See also</span></span> |
|:---------------|:--------|:----------|
| <span data-ttu-id="c2ca6-133">Crear, obtener, actualizar o eliminar una empresa</span><span class="sxs-lookup"><span data-stu-id="c2ca6-133">Create, get, update, or delete a business</span></span> | [<span data-ttu-id="c2ca6-134">bookingBusiness</span><span class="sxs-lookup"><span data-stu-id="c2ca6-134">bookingBusiness</span></span>](bookingbusiness.md) | [<span data-ttu-id="c2ca6-135">Métodos de bookingBusiness</span><span class="sxs-lookup"><span data-stu-id="c2ca6-135">Methods of bookingBusiness</span></span>](bookingbusiness.md#methods) |
| <span data-ttu-id="c2ca6-136">Actualización de la directiva de programación</span><span class="sxs-lookup"><span data-stu-id="c2ca6-136">Update the scheduling policy</span></span> | [<span data-ttu-id="c2ca6-137">bookingSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="c2ca6-137">bookingSchedulingPolicy</span></span>](bookingschedulingpolicy.md) | [<span data-ttu-id="c2ca6-138">Actualizar un bookingBusiness</span><span class="sxs-lookup"><span data-stu-id="c2ca6-138">Update a bookingBusiness</span></span>](../api/bookingbusiness-update.md) |
| <span data-ttu-id="c2ca6-139">Agregar, obtener, actualizar o eliminar a los miembros del personal</span><span class="sxs-lookup"><span data-stu-id="c2ca6-139">Add, get, update, or delete staff members</span></span> | [<span data-ttu-id="c2ca6-140">bookingStaffMember</span><span class="sxs-lookup"><span data-stu-id="c2ca6-140">bookingStaffMember</span></span>](bookingstaffmember.md) | [<span data-ttu-id="c2ca6-141">Métodos de bookingStaffMember</span><span class="sxs-lookup"><span data-stu-id="c2ca6-141">Methods of bookingStaffMember</span></span>](bookingstaffmember.md#methods)  |
| <span data-ttu-id="c2ca6-142">Agregar, obtener, actualizar o eliminar los servicios</span><span class="sxs-lookup"><span data-stu-id="c2ca6-142">Add, get, update, or delete services</span></span> | [<span data-ttu-id="c2ca6-143">bookingService</span><span class="sxs-lookup"><span data-stu-id="c2ca6-143">bookingService</span></span>](bookingservice.md) | [<span data-ttu-id="c2ca6-144">Métodos de bookingService</span><span class="sxs-lookup"><span data-stu-id="c2ca6-144">Methods of bookingService</span></span>](bookingservice.md#methods)  |
| <span data-ttu-id="c2ca6-145">Publicar o cancelar la publicación de la página de programación</span><span class="sxs-lookup"><span data-stu-id="c2ca6-145">Publish or unpublish the scheduling page</span></span> | [<span data-ttu-id="c2ca6-146">bookingBusiness</span><span class="sxs-lookup"><span data-stu-id="c2ca6-146">bookingBusiness</span></span>](bookingbusiness.md) | [<span data-ttu-id="c2ca6-147">publicar</span><span class="sxs-lookup"><span data-stu-id="c2ca6-147">publish</span></span>](../api/bookingbusiness-publish.md) <br> [<span data-ttu-id="c2ca6-148">Cancelar la publicación</span><span class="sxs-lookup"><span data-stu-id="c2ca6-148">unpublish</span></span>](../api/bookingbusiness-unpublish.md) |
| <span data-ttu-id="c2ca6-149">Crear, obtener, actualizar, eliminar o cancelar una cita</span><span class="sxs-lookup"><span data-stu-id="c2ca6-149">Create, get, update, delete, or cancel an appointment</span></span> | [<span data-ttu-id="c2ca6-150">bookingAppointment</span><span class="sxs-lookup"><span data-stu-id="c2ca6-150">bookingAppointment</span></span>](bookingappointment.md) | [<span data-ttu-id="c2ca6-151">Métodos de bookingAppointment</span><span class="sxs-lookup"><span data-stu-id="c2ca6-151">Methods of bookingAppointment</span></span>](bookingappointment.md#methods)  |
| <span data-ttu-id="c2ca6-152">Obtener las citas en un intervalo de fechas</span><span class="sxs-lookup"><span data-stu-id="c2ca6-152">Get appointments in a date range</span></span> | [<span data-ttu-id="c2ca6-153">bookingBusiness</span><span class="sxs-lookup"><span data-stu-id="c2ca6-153">bookingBusiness</span></span>](bookingbusiness.md) | [<span data-ttu-id="c2ca6-154">Lista reservas calendarView</span><span class="sxs-lookup"><span data-stu-id="c2ca6-154">List Bookings calendarView</span></span>](../api/bookingbusiness-list-calendarview.md) |
| <span data-ttu-id="c2ca6-155">Obtener moneda</span><span class="sxs-lookup"><span data-stu-id="c2ca6-155">Get currency</span></span> | [<span data-ttu-id="c2ca6-156">bookingCurrency</span><span class="sxs-lookup"><span data-stu-id="c2ca6-156">bookingCurrency</span></span>](bookingcurrency.md) | [<span data-ttu-id="c2ca6-157">Métodos de bookingCurrency</span><span class="sxs-lookup"><span data-stu-id="c2ca6-157">Methods of bookingCurrency</span></span>](bookingcurrency.md#methods) |


## <a name="see-also"></a><span data-ttu-id="c2ca6-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2ca6-158">See also</span></span>

- <span data-ttu-id="c2ca6-159">Pruebe la API en el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).</span><span class="sxs-lookup"><span data-stu-id="c2ca6-159">Try the API in the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer).</span></span>
- <span data-ttu-id="c2ca6-160">Vea [cómo algunos de nuestros socios usan Microsoft Graph](https://developer.microsoft.com/graph/graph/examples#partners).</span><span class="sxs-lookup"><span data-stu-id="c2ca6-160">See [how some of our partners are using Microsoft Graph](https://developer.microsoft.com/graph/graph/examples#partners).</span></span>
- <span data-ttu-id="c2ca6-161">Obtenga información sobre cómo elegir [los permisos](/graph/permissions-reference) en Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="c2ca6-161">Learn how to choose [permissions](/graph/permissions-reference) in Microsoft Graph.</span></span>
