---
title: tipo de recurso bookingSchedulingPolicy
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: 7a16e9a2ec4e64978dd3c20f7510cfd42d76e826
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086568"
---
# <a name="bookingschedulingpolicy-resource-type"></a><span data-ttu-id="5fa5b-104">tipo de recurso bookingSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="5fa5b-104">bookingSchedulingPolicy resource type</span></span>

 > <span data-ttu-id="5fa5b-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5fa5b-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5fa5b-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5fa5b-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="5fa5b-107">Representa el conjunto de directivas que determinan cómo se deben crear citas en un calendario de Microsoft Bookings.</span><span class="sxs-lookup"><span data-stu-id="5fa5b-107">Represents the set of policies that determine how appointments should be created in a Microsoft Bookings calendar.</span></span>

## <a name="properties"></a><span data-ttu-id="5fa5b-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5fa5b-108">Properties</span></span>
| <span data-ttu-id="5fa5b-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5fa5b-109">Property</span></span>     | <span data-ttu-id="5fa5b-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="5fa5b-110">Type</span></span>   |<span data-ttu-id="5fa5b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5fa5b-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5fa5b-112">allowStaffSelection</span><span class="sxs-lookup"><span data-stu-id="5fa5b-112">allowStaffSelection</span></span>|<span data-ttu-id="5fa5b-113">Booleano</span><span class="sxs-lookup"><span data-stu-id="5fa5b-113">Boolean</span></span>|<span data-ttu-id="5fa5b-114">True si se debe permitir a los clientes elegir a una persona específica para la reserva.</span><span class="sxs-lookup"><span data-stu-id="5fa5b-114">True if to allow customers to choose a specific person for the booking.</span></span>|
|<span data-ttu-id="5fa5b-115">maximumAdvance</span><span class="sxs-lookup"><span data-stu-id="5fa5b-115">maximumAdvance</span></span>|<span data-ttu-id="5fa5b-116">Duración</span><span class="sxs-lookup"><span data-stu-id="5fa5b-116">Duration</span></span>|<span data-ttu-id="5fa5b-117">Número máximo de días de antelación que se puede realizar una reserva.</span><span class="sxs-lookup"><span data-stu-id="5fa5b-117">Maximum number of days in advance that a booking can be made.</span></span> <span data-ttu-id="5fa5b-118">Sigue el formato [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) .</span><span class="sxs-lookup"><span data-stu-id="5fa5b-118">It follows the [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format.</span></span>|
|<span data-ttu-id="5fa5b-119">minimumLeadTime</span><span class="sxs-lookup"><span data-stu-id="5fa5b-119">minimumLeadTime</span></span>|<span data-ttu-id="5fa5b-120">Duración</span><span class="sxs-lookup"><span data-stu-id="5fa5b-120">Duration</span></span>|<span data-ttu-id="5fa5b-121">La cantidad mínima de tiempo antes de la cual se deben realizar reservas y cancelaciones.</span><span class="sxs-lookup"><span data-stu-id="5fa5b-121">The minimum amount of time before which bookings and cancellations must be made.</span></span> <span data-ttu-id="5fa5b-122">Sigue el formato [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) .</span><span class="sxs-lookup"><span data-stu-id="5fa5b-122">It follows the [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format.</span></span>|
|<span data-ttu-id="5fa5b-123">sendConfirmationsToOwner</span><span class="sxs-lookup"><span data-stu-id="5fa5b-123">sendConfirmationsToOwner</span></span>|<span data-ttu-id="5fa5b-124">Booleano</span><span class="sxs-lookup"><span data-stu-id="5fa5b-124">Boolean</span></span>| <span data-ttu-id="5fa5b-125">True para notificar a la empresa a través de correo electrónico cuando se cree o modifique una reserva.</span><span class="sxs-lookup"><span data-stu-id="5fa5b-125">True to notify the business via email when a booking is created or changed.</span></span> <span data-ttu-id="5fa5b-126">Utilice la dirección de correo electrónico especificada en la propiedad de **correo electrónico** de la entidad **bookingBusiness** para el negocio.</span><span class="sxs-lookup"><span data-stu-id="5fa5b-126">Use the email address specified in the **email** property of the **bookingBusiness** entity for the business.</span></span> |
|<span data-ttu-id="5fa5b-127">timeSlotInterval</span><span class="sxs-lookup"><span data-stu-id="5fa5b-127">timeSlotInterval</span></span>|<span data-ttu-id="5fa5b-128">Duración</span><span class="sxs-lookup"><span data-stu-id="5fa5b-128">Duration</span></span>|<span data-ttu-id="5fa5b-129">Duración de cada franja horaria, indicada en formato [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) .</span><span class="sxs-lookup"><span data-stu-id="5fa5b-129">Duration of each time slot, denoted in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="5fa5b-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5fa5b-130">JSON representation</span></span>

<span data-ttu-id="5fa5b-131">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="5fa5b-131">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.bookingSchedulingPolicy"
}-->

```json
{
  "allowStaffSelection": true,
  "maximumAdvance": "String (timestamp)",
  "minimumLeadTime": "String (timestamp)",
  "sendConfirmationsToOwner": true,
  "timeSlotInterval": "String (timestamp)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "bookingSchedulingPolicy resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->