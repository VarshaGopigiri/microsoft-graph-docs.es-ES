---
title: tipo de recurso bookingService
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
ms.openlocfilehash: 63eae84249501426c43ad73326cbf005009753be
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27815445"
---
# <a name="bookingservice-resource-type"></a><span data-ttu-id="fa055-104">tipo de recurso bookingService</span><span class="sxs-lookup"><span data-stu-id="fa055-104">bookingService resource type</span></span>

 > <span data-ttu-id="fa055-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fa055-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fa055-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fa055-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="fa055-107">Representa información sobre un determinado servicio proporcionado por un [bookingBusiness](bookingbusiness.md), como el nombre de servicio, precio y el personal que normalmente proporciona dicho servicio.</span><span class="sxs-lookup"><span data-stu-id="fa055-107">Represents information about a particular service provided by a [bookingBusiness](bookingbusiness.md), such as the service name, price, and the staff that usually provides such service.</span></span>

## <a name="methods"></a><span data-ttu-id="fa055-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="fa055-108">Methods</span></span>

| <span data-ttu-id="fa055-109">Método</span><span class="sxs-lookup"><span data-stu-id="fa055-109">Method</span></span>           | <span data-ttu-id="fa055-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fa055-110">Return Type</span></span>    |<span data-ttu-id="fa055-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa055-111">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="fa055-112">Servicios de la lista</span><span class="sxs-lookup"><span data-stu-id="fa055-112">List services</span></span>](../api/bookingbusiness-list-services.md) | <span data-ttu-id="fa055-113">colección de [bookingService](bookingservice.md)</span><span class="sxs-lookup"><span data-stu-id="fa055-113">[bookingService](bookingservice.md) collection</span></span> | <span data-ttu-id="fa055-114">Para obtener una lista de objetos de **bookingService** en el especificado [bookingbusiness](../resources/bookingbusiness.md).</span><span class="sxs-lookup"><span data-stu-id="fa055-114">Get a list of **bookingService** objects in the specified [bookingbusiness](../resources/bookingbusiness.md).</span></span>|
|[<span data-ttu-id="fa055-115">Crear bookingService</span><span class="sxs-lookup"><span data-stu-id="fa055-115">Create bookingService</span></span>](../api/bookingbusiness-post-services.md) | [<span data-ttu-id="fa055-116">bookingService</span><span class="sxs-lookup"><span data-stu-id="fa055-116">bookingService</span></span>](bookingservice.md) | <span data-ttu-id="fa055-117">Crear un **bookingService** para el [bookingbusiness](../resources/bookingbusiness.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="fa055-117">Create a **bookingService** for the specified [bookingbusiness](../resources/bookingbusiness.md).</span></span> |
|[<span data-ttu-id="fa055-118">Obtener bookingService</span><span class="sxs-lookup"><span data-stu-id="fa055-118">Get bookingService</span></span>](../api/bookingservice-get.md) | [<span data-ttu-id="fa055-119">bookingService</span><span class="sxs-lookup"><span data-stu-id="fa055-119">bookingService</span></span>](bookingservice.md) |<span data-ttu-id="fa055-120">Obtener las propiedades y relaciones de un objeto **bookingService** en la [bookingbusiness](../resources/bookingbusiness.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="fa055-120">Get the properties and relationships of a **bookingService** object in the specified [bookingbusiness](../resources/bookingbusiness.md).</span></span>|
|[<span data-ttu-id="fa055-121">Update</span><span class="sxs-lookup"><span data-stu-id="fa055-121">Update</span></span>](../api/bookingservice-update.md) | [<span data-ttu-id="fa055-122">bookingService</span><span class="sxs-lookup"><span data-stu-id="fa055-122">bookingService</span></span>](bookingservice.md)    |<span data-ttu-id="fa055-123">Actualizar un objeto **bookingService** en la [bookingbusiness](../resources/bookingbusiness.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="fa055-123">Update a **bookingService** object in the specified [bookingbusiness](../resources/bookingbusiness.md).</span></span> |
|[<span data-ttu-id="fa055-124">Delete</span><span class="sxs-lookup"><span data-stu-id="fa055-124">Delete</span></span>](../api/bookingservice-delete.md) | <span data-ttu-id="fa055-125">Ninguno</span><span class="sxs-lookup"><span data-stu-id="fa055-125">None</span></span> |<span data-ttu-id="fa055-126">Eliminar un objeto **bookingService** en la [bookingbusiness](../resources/bookingbusiness.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="fa055-126">Delete a **bookingService** object in the specified [bookingbusiness](../resources/bookingbusiness.md).</span></span> |

## <a name="properties"></a><span data-ttu-id="fa055-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fa055-127">Properties</span></span>
| <span data-ttu-id="fa055-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fa055-128">Property</span></span>     | <span data-ttu-id="fa055-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="fa055-129">Type</span></span>   |<span data-ttu-id="fa055-130">Description</span><span class="sxs-lookup"><span data-stu-id="fa055-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fa055-131">defaultDuration</span><span class="sxs-lookup"><span data-stu-id="fa055-131">defaultDuration</span></span>|<span data-ttu-id="fa055-132">Duración</span><span class="sxs-lookup"><span data-stu-id="fa055-132">Duration</span></span>|<span data-ttu-id="fa055-133">La longitud predeterminada del servicio, representado en número de días, horas, minutos y segundos.</span><span class="sxs-lookup"><span data-stu-id="fa055-133">The default length of the service, represented in numbers of days, hours, minutes, and seconds.</span></span> <span data-ttu-id="fa055-134">Por ejemplo, P11D23H59M59.999999999999S.</span><span class="sxs-lookup"><span data-stu-id="fa055-134">For example, P11D23H59M59.999999999999S.</span></span> |
|<span data-ttu-id="fa055-135">defaultLocation</span><span class="sxs-lookup"><span data-stu-id="fa055-135">defaultLocation</span></span>|[<span data-ttu-id="fa055-136">location</span><span class="sxs-lookup"><span data-stu-id="fa055-136">location</span></span>](location.md)|<span data-ttu-id="fa055-137">La ubicación física de forma predeterminada para el servicio.</span><span class="sxs-lookup"><span data-stu-id="fa055-137">The default physical location for the service.</span></span>|
|<span data-ttu-id="fa055-138">defaultPrice</span><span class="sxs-lookup"><span data-stu-id="fa055-138">defaultPrice</span></span>|<span data-ttu-id="fa055-139">Doble</span><span class="sxs-lookup"><span data-stu-id="fa055-139">Double</span></span>|<span data-ttu-id="fa055-140">El precio monetarios predeterminado para el servicio.</span><span class="sxs-lookup"><span data-stu-id="fa055-140">The default monetary price for the service.</span></span>|
|<span data-ttu-id="fa055-141">defaultPriceType</span><span class="sxs-lookup"><span data-stu-id="fa055-141">defaultPriceType</span></span>|<span data-ttu-id="fa055-142">string</span><span class="sxs-lookup"><span data-stu-id="fa055-142">string</span></span>|<span data-ttu-id="fa055-143">Se carga el modo predeterminado en el servicio.</span><span class="sxs-lookup"><span data-stu-id="fa055-143">The default way the service is charged.</span></span> <span data-ttu-id="fa055-144">Los valores posibles son: `undefined`, `fixedPrice`, `startingAt`, `hourly`, `free`, `priceVaries`, `callUs` y `notSet`.</span><span class="sxs-lookup"><span data-stu-id="fa055-144">Possible values are: `undefined`, `fixedPrice`, `startingAt`, `hourly`, `free`, `priceVaries`, `callUs`, `notSet`.</span></span>|
|<span data-ttu-id="fa055-145">defaultReminders</span><span class="sxs-lookup"><span data-stu-id="fa055-145">defaultReminders</span></span>|<span data-ttu-id="fa055-146">colección de [bookingReminder](bookingreminder.md)</span><span class="sxs-lookup"><span data-stu-id="fa055-146">[bookingReminder](bookingreminder.md) collection</span></span>|<span data-ttu-id="fa055-147">Establece el valor predeterminado de avisos para una cita de este servicio.</span><span class="sxs-lookup"><span data-stu-id="fa055-147">The default set of reminders for an appointment of this service.</span></span> <span data-ttu-id="fa055-148">El valor de esta propiedad está disponible sólo cuando se lee este **bookingService** por su identificador.</span><span class="sxs-lookup"><span data-stu-id="fa055-148">The value of this property is available only when reading this **bookingService** by its ID.</span></span>|
|<span data-ttu-id="fa055-149">descripción</span><span class="sxs-lookup"><span data-stu-id="fa055-149">description</span></span>|<span data-ttu-id="fa055-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="fa055-150">String</span></span>|<span data-ttu-id="fa055-151">Una descripción de texto para el servicio.</span><span class="sxs-lookup"><span data-stu-id="fa055-151">A text description for the service.</span></span>|
|<span data-ttu-id="fa055-152">displayName</span><span class="sxs-lookup"><span data-stu-id="fa055-152">displayName</span></span>|<span data-ttu-id="fa055-153">Cadena</span><span class="sxs-lookup"><span data-stu-id="fa055-153">String</span></span>|<span data-ttu-id="fa055-154">Un nombre de servicio.</span><span class="sxs-lookup"><span data-stu-id="fa055-154">A service name.</span></span>|
|<span data-ttu-id="fa055-155">emailAddress</span><span class="sxs-lookup"><span data-stu-id="fa055-155">emailAddress</span></span>|<span data-ttu-id="fa055-156">Cadena</span><span class="sxs-lookup"><span data-stu-id="fa055-156">String</span></span>|<span data-ttu-id="fa055-157">Una dirección de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="fa055-157">An email address</span></span>|
|<span data-ttu-id="fa055-158">id</span><span class="sxs-lookup"><span data-stu-id="fa055-158">id</span></span>|<span data-ttu-id="fa055-159">Cadena</span><span class="sxs-lookup"><span data-stu-id="fa055-159">String</span></span>|<span data-ttu-id="fa055-160">El identificador de ese servicio, en un formato GUID.</span><span class="sxs-lookup"><span data-stu-id="fa055-160">The ID of that service, in a GUID format.</span></span> <span data-ttu-id="fa055-161">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fa055-161">Read-only.</span></span>|
|<span data-ttu-id="fa055-162">isHiddenFromCustomers</span><span class="sxs-lookup"><span data-stu-id="fa055-162">isHiddenFromCustomers</span></span>|<span data-ttu-id="fa055-163">Booleano</span><span class="sxs-lookup"><span data-stu-id="fa055-163">Boolean</span></span>|<span data-ttu-id="fa055-164">True significa que este servicio no está disponible para los clientes de reserva.</span><span class="sxs-lookup"><span data-stu-id="fa055-164">True means this service is not available to customers for booking.</span></span>|
|<span data-ttu-id="fa055-165">notas</span><span class="sxs-lookup"><span data-stu-id="fa055-165">notes</span></span>|<span data-ttu-id="fa055-166">Cadena</span><span class="sxs-lookup"><span data-stu-id="fa055-166">String</span></span>|<span data-ttu-id="fa055-167">Obtener información adicional acerca de este servicio.</span><span class="sxs-lookup"><span data-stu-id="fa055-167">Additional information about this service.</span></span>|
|<span data-ttu-id="fa055-168">postBuffer</span><span class="sxs-lookup"><span data-stu-id="fa055-168">postBuffer</span></span>|<span data-ttu-id="fa055-169">Duración</span><span class="sxs-lookup"><span data-stu-id="fa055-169">Duration</span></span>|<span data-ttu-id="fa055-170">Finaliza el tiempo de búfer después de una cita para este servicio y antes de la siguiente cita del cliente se puede reservar.</span><span class="sxs-lookup"><span data-stu-id="fa055-170">The time to buffer after an appointment for this service ends, and before the next customer appointment can be booked.</span></span>|
|<span data-ttu-id="fa055-171">Búfer</span><span class="sxs-lookup"><span data-stu-id="fa055-171">preBuffer</span></span>|<span data-ttu-id="fa055-172">Duración</span><span class="sxs-lookup"><span data-stu-id="fa055-172">Duration</span></span>|<span data-ttu-id="fa055-173">El tiempo para poder iniciar una cita para este servicio de búfer.</span><span class="sxs-lookup"><span data-stu-id="fa055-173">The time to buffer before an appointment for this service can start.</span></span>|
|<span data-ttu-id="fa055-174">schedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="fa055-174">schedulingPolicy</span></span>|[<span data-ttu-id="fa055-175">bookingSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="fa055-175">bookingSchedulingPolicy</span></span>](bookingschedulingpolicy.md)|<span data-ttu-id="fa055-176">El conjunto de directivas que determinan cómo deben crearse y administrarse citas para este tipo de servicio.</span><span class="sxs-lookup"><span data-stu-id="fa055-176">The set of policies that determine how appointments for this type of service should be created and managed.</span></span>|
|<span data-ttu-id="fa055-177">staffMemberIds</span><span class="sxs-lookup"><span data-stu-id="fa055-177">staffMemberIds</span></span>|<span data-ttu-id="fa055-178">Colección String</span><span class="sxs-lookup"><span data-stu-id="fa055-178">String collection</span></span>|<span data-ttu-id="fa055-179">Representa los [miembros del personal](bookingstaffmember.md) que proporcionar este servicio.</span><span class="sxs-lookup"><span data-stu-id="fa055-179">Represents those [staff members](bookingstaffmember.md) who provide this service.</span></span> |

## <a name="relationships"></a><span data-ttu-id="fa055-180">Relaciones</span><span class="sxs-lookup"><span data-stu-id="fa055-180">Relationships</span></span>
<span data-ttu-id="fa055-181">Ninguno</span><span class="sxs-lookup"><span data-stu-id="fa055-181">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="fa055-182">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fa055-182">JSON representation</span></span>

<span data-ttu-id="fa055-183">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="fa055-183">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.bookingService"
}-->

```json
{
  "defaultDuration": "String (timestamp)",
  "defaultLocation": {"@odata.type": "microsoft.graph.location"},
  "defaultPrice": 1024,
  "defaultPriceType": "string",
  "defaultReminders": [{"@odata.type": "microsoft.graph.bookingReminder"}],
  "description": "String",
  "displayName": "String",
  "emailAddress": "String",
  "id": "String (identifier)",
  "isHiddenFromCustomers": true,
  "notes": "String",
  "postBuffer": "String (timestamp)",
  "preBuffer": "String (timestamp)",
  "schedulingPolicy": {"@odata.type": "microsoft.graph.bookingSchedulingPolicy"},
  "staffMemberIds": ["String"]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "bookingService resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
