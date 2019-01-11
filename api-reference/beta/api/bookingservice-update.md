---
title: Actualizar bookingservice
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
ms.openlocfilehash: 6eee5949d5d8cee23821d726563b4687febd77a7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27838923"
---
# <a name="update-bookingservice"></a><span data-ttu-id="cd45e-104">Actualizar bookingservice</span><span class="sxs-lookup"><span data-stu-id="cd45e-104">Update bookingservice</span></span>

 > <span data-ttu-id="cd45e-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cd45e-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cd45e-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cd45e-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="cd45e-107">Actualizar las propiedades de un objeto [bookingService](../resources/bookingservice.md) en la [bookingbusiness](../resources/bookingbusiness.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="cd45e-107">Update the properties of a [bookingService](../resources/bookingservice.md) object in the specified [bookingbusiness](../resources/bookingbusiness.md).</span></span>

<span data-ttu-id="cd45e-108">Los siguientes son algunos ejemplos que se pueden personalizar para un servicio:</span><span class="sxs-lookup"><span data-stu-id="cd45e-108">The following are some examples you can customize for a service:</span></span>
- <span data-ttu-id="cd45e-109">Precio</span><span class="sxs-lookup"><span data-stu-id="cd45e-109">Price</span></span>
- <span data-ttu-id="cd45e-110">Longitud típica de una cita</span><span class="sxs-lookup"><span data-stu-id="cd45e-110">Typical length of an appointment</span></span>
- <span data-ttu-id="cd45e-111">Reminders</span><span class="sxs-lookup"><span data-stu-id="cd45e-111">Reminders</span></span>
- <span data-ttu-id="cd45e-112">Búfer para configurar antes o terminar después el servicio en cualquier momento</span><span class="sxs-lookup"><span data-stu-id="cd45e-112">Any time buffer to set up before or finish up after the service</span></span>
- <span data-ttu-id="cd45e-113">Parámetros de [programación de directiva](../resources/bookingschedulingpolicy.md) como mínimo de notificación a Libreta o cancelar, y si los clientes pueden seleccionar los miembros del personal específico para una cita.</span><span class="sxs-lookup"><span data-stu-id="cd45e-113">[Scheduling policy](../resources/bookingschedulingpolicy.md) parameters such as minimum notice to book or cancel, and whether customers can select specific staff members for an appointment.</span></span>

## <a name="permissions"></a><span data-ttu-id="cd45e-114">Permisos</span><span class="sxs-lookup"><span data-stu-id="cd45e-114">Permissions</span></span>
<span data-ttu-id="cd45e-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cd45e-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cd45e-117">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cd45e-117">Permission type</span></span>      | <span data-ttu-id="cd45e-118">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cd45e-118">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="cd45e-119">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cd45e-119">Delegated (work or school account)</span></span> |  <span data-ttu-id="cd45e-120">Bookings.ReadWrite.All, Bookings.Manage.All</span><span class="sxs-lookup"><span data-stu-id="cd45e-120">Bookings.ReadWrite.All, Bookings.Manage.All</span></span>   |
|<span data-ttu-id="cd45e-121">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cd45e-121">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cd45e-122">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cd45e-122">Not supported.</span></span>   |
|<span data-ttu-id="cd45e-123">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cd45e-123">Application</span></span> | <span data-ttu-id="cd45e-124">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cd45e-124">Not supported.</span></span>  |

## <a name="http-request"></a><span data-ttu-id="cd45e-125">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cd45e-125">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /bookingBusinesses/{id}/services/{id}
```
## <a name="optional-request-headers"></a><span data-ttu-id="cd45e-126">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="cd45e-126">Optional request headers</span></span>
| <span data-ttu-id="cd45e-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="cd45e-127">Name</span></span>       | <span data-ttu-id="cd45e-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd45e-128">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="cd45e-129">Autorización</span><span class="sxs-lookup"><span data-stu-id="cd45e-129">Authorization</span></span>  | <span data-ttu-id="cd45e-130">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="cd45e-130">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="cd45e-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cd45e-131">Request body</span></span>
<span data-ttu-id="cd45e-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="cd45e-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="cd45e-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cd45e-135">Property</span></span>     | <span data-ttu-id="cd45e-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd45e-136">Type</span></span>   |<span data-ttu-id="cd45e-137">Description</span><span class="sxs-lookup"><span data-stu-id="cd45e-137">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="cd45e-138">defaultDuration</span><span class="sxs-lookup"><span data-stu-id="cd45e-138">defaultDuration</span></span>|<span data-ttu-id="cd45e-139">Duración</span><span class="sxs-lookup"><span data-stu-id="cd45e-139">Duration</span></span>|<span data-ttu-id="cd45e-140">La longitud predeterminada del servicio, representado en número de días, horas, minutos y segundos.</span><span class="sxs-lookup"><span data-stu-id="cd45e-140">The default length of the service, represented in numbers of days, hours, minutes, and seconds.</span></span> <span data-ttu-id="cd45e-141">Por ejemplo, P11D23H59M59.999999999999S.</span><span class="sxs-lookup"><span data-stu-id="cd45e-141">For example, P11D23H59M59.999999999999S.</span></span> |
|<span data-ttu-id="cd45e-142">defaultLocation</span><span class="sxs-lookup"><span data-stu-id="cd45e-142">defaultLocation</span></span>|[<span data-ttu-id="cd45e-143">location</span><span class="sxs-lookup"><span data-stu-id="cd45e-143">location</span></span>](../resources/location.md)|<span data-ttu-id="cd45e-144">La ubicación física de forma predeterminada para el servicio.</span><span class="sxs-lookup"><span data-stu-id="cd45e-144">The default physical location for the service.</span></span>|
|<span data-ttu-id="cd45e-145">defaultPrice</span><span class="sxs-lookup"><span data-stu-id="cd45e-145">defaultPrice</span></span>|<span data-ttu-id="cd45e-146">Doble</span><span class="sxs-lookup"><span data-stu-id="cd45e-146">Double</span></span>|<span data-ttu-id="cd45e-147">El precio monetarios predeterminado para el servicio.</span><span class="sxs-lookup"><span data-stu-id="cd45e-147">The default monetary price for the service.</span></span>|
|<span data-ttu-id="cd45e-148">defaultPriceType</span><span class="sxs-lookup"><span data-stu-id="cd45e-148">defaultPriceType</span></span>|<span data-ttu-id="cd45e-149">string</span><span class="sxs-lookup"><span data-stu-id="cd45e-149">string</span></span>|<span data-ttu-id="cd45e-150">Se carga el modo predeterminado en el servicio.</span><span class="sxs-lookup"><span data-stu-id="cd45e-150">The default way the service is charged.</span></span> <span data-ttu-id="cd45e-151">Los valores posibles son: `undefined`, `fixedPrice`, `startingAt`, `hourly`, `free`, `priceVaries`, `callUs` y `notSet`.</span><span class="sxs-lookup"><span data-stu-id="cd45e-151">Possible values are: `undefined`, `fixedPrice`, `startingAt`, `hourly`, `free`, `priceVaries`, `callUs`, `notSet`.</span></span>|
|<span data-ttu-id="cd45e-152">defaultReminders</span><span class="sxs-lookup"><span data-stu-id="cd45e-152">defaultReminders</span></span>|<span data-ttu-id="cd45e-153">colección de [bookingReminder](../resources/bookingreminder.md)</span><span class="sxs-lookup"><span data-stu-id="cd45e-153">[bookingReminder](../resources/bookingreminder.md) collection</span></span>|<span data-ttu-id="cd45e-154">Establece el valor predeterminado de avisos para una cita de este servicio.</span><span class="sxs-lookup"><span data-stu-id="cd45e-154">The default set of reminders for an appointment of this service.</span></span> <span data-ttu-id="cd45e-155">El valor de esta propiedad está disponible sólo cuando se lee este **bookingService** por su identificador.</span><span class="sxs-lookup"><span data-stu-id="cd45e-155">The value of this property is available only when reading this **bookingService** by its ID.</span></span>|
|<span data-ttu-id="cd45e-156">descripción</span><span class="sxs-lookup"><span data-stu-id="cd45e-156">description</span></span>|<span data-ttu-id="cd45e-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="cd45e-157">String</span></span>|<span data-ttu-id="cd45e-158">Una descripción de texto para el servicio.</span><span class="sxs-lookup"><span data-stu-id="cd45e-158">A text description for the service.</span></span>|
|<span data-ttu-id="cd45e-159">displayName</span><span class="sxs-lookup"><span data-stu-id="cd45e-159">displayName</span></span>|<span data-ttu-id="cd45e-160">Cadena</span><span class="sxs-lookup"><span data-stu-id="cd45e-160">String</span></span>|<span data-ttu-id="cd45e-161">Un nombre de servicio.</span><span class="sxs-lookup"><span data-stu-id="cd45e-161">A service name.</span></span>|
|<span data-ttu-id="cd45e-162">emailAddress</span><span class="sxs-lookup"><span data-stu-id="cd45e-162">emailAddress</span></span>|<span data-ttu-id="cd45e-163">Cadena</span><span class="sxs-lookup"><span data-stu-id="cd45e-163">String</span></span>|<span data-ttu-id="cd45e-164">Una dirección de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="cd45e-164">An email address</span></span>|
|<span data-ttu-id="cd45e-165">id</span><span class="sxs-lookup"><span data-stu-id="cd45e-165">id</span></span>|<span data-ttu-id="cd45e-166">Cadena</span><span class="sxs-lookup"><span data-stu-id="cd45e-166">String</span></span>| <span data-ttu-id="cd45e-167">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cd45e-167">Read-only.</span></span>|
|<span data-ttu-id="cd45e-168">isHiddenFromCustomers</span><span class="sxs-lookup"><span data-stu-id="cd45e-168">isHiddenFromCustomers</span></span>|<span data-ttu-id="cd45e-169">Booleano</span><span class="sxs-lookup"><span data-stu-id="cd45e-169">Boolean</span></span>|<span data-ttu-id="cd45e-170">True significa que este servicio no está disponible para los clientes de reserva.</span><span class="sxs-lookup"><span data-stu-id="cd45e-170">True means this service is not available to customers for booking.</span></span>|
|<span data-ttu-id="cd45e-171">notas</span><span class="sxs-lookup"><span data-stu-id="cd45e-171">notes</span></span>|<span data-ttu-id="cd45e-172">Cadena</span><span class="sxs-lookup"><span data-stu-id="cd45e-172">String</span></span>|<span data-ttu-id="cd45e-173">Obtener información adicional acerca de este servicio.</span><span class="sxs-lookup"><span data-stu-id="cd45e-173">Additional information about this service.</span></span>|
|<span data-ttu-id="cd45e-174">postBuffer</span><span class="sxs-lookup"><span data-stu-id="cd45e-174">postBuffer</span></span>|<span data-ttu-id="cd45e-175">Duración</span><span class="sxs-lookup"><span data-stu-id="cd45e-175">Duration</span></span>|<span data-ttu-id="cd45e-176">Finaliza el tiempo de búfer después de una cita para este servicio y antes de la siguiente cita del cliente se puede reservar.</span><span class="sxs-lookup"><span data-stu-id="cd45e-176">The time to buffer after an appointment for this service ends, and before the next customer appointment can be booked.</span></span>|
|<span data-ttu-id="cd45e-177">Búfer</span><span class="sxs-lookup"><span data-stu-id="cd45e-177">preBuffer</span></span>|<span data-ttu-id="cd45e-178">Duración</span><span class="sxs-lookup"><span data-stu-id="cd45e-178">Duration</span></span>|<span data-ttu-id="cd45e-179">El tiempo para poder iniciar una cita para este servicio de búfer.</span><span class="sxs-lookup"><span data-stu-id="cd45e-179">The time to buffer before an appointment for this service can start.</span></span>|
|<span data-ttu-id="cd45e-180">schedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="cd45e-180">schedulingPolicy</span></span>|[<span data-ttu-id="cd45e-181">bookingSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="cd45e-181">bookingSchedulingPolicy</span></span>](../resources/bookingschedulingpolicy.md)|<span data-ttu-id="cd45e-182">El conjunto de directivas que determinan cómo deben crearse y administrarse citas para este tipo de servicio.</span><span class="sxs-lookup"><span data-stu-id="cd45e-182">The set of policies that determine how appointments for this type of service should be created and managed.</span></span>|
|<span data-ttu-id="cd45e-183">staffMemberIds</span><span class="sxs-lookup"><span data-stu-id="cd45e-183">staffMemberIds</span></span>|<span data-ttu-id="cd45e-184">Colección String</span><span class="sxs-lookup"><span data-stu-id="cd45e-184">String collection</span></span>|<span data-ttu-id="cd45e-185">Representa los [miembros del personal](../resources/bookingstaffmember.md) que proporcionar este servicio.</span><span class="sxs-lookup"><span data-stu-id="cd45e-185">Represents those [staff members](../resources/bookingstaffmember.md) who provide this service.</span></span> |

## <a name="response"></a><span data-ttu-id="cd45e-186">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cd45e-186">Response</span></span>
<span data-ttu-id="cd45e-p108">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cd45e-p108">If successful, this method returns a `204 No content` response code. It does not return anything in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="cd45e-189">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd45e-189">Example</span></span>
##### <a name="request"></a><span data-ttu-id="cd45e-190">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cd45e-190">Request</span></span>
<span data-ttu-id="cd45e-191">En el ejemplo siguiente se actualiza la duración del servicio especificado.</span><span class="sxs-lookup"><span data-stu-id="cd45e-191">The following example updates the duration of the specified service.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_bookingservice"
}-->
```http
PATCH https://graph.microsoft.com/beta/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/services/57da6774-a087-4d69-b0e6-6fb82c339976
Content-type: application/json

{
    "@odata.type":"#microsoft.graph.bookingService",
    "defaultDuration":"PT30M"
}
```
##### <a name="response"></a><span data-ttu-id="cd45e-192">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cd45e-192">Response</span></span>
<span data-ttu-id="cd45e-193">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cd45e-193">The following is an example of the response.</span></span> 
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
  "description": "Update bookingservice",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
