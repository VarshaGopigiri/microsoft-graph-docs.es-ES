---
title: tipo de recurso bookingWorkTimeSlot
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
author: angelgolfer-ms
ms.prod: bookings
ms.openlocfilehash: 33dd856d678d2cf1ba9da2a747c0bd46f2fd4932
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27968487"
---
# <a name="bookingworktimeslot-resource-type"></a><span data-ttu-id="2409e-104">tipo de recurso bookingWorkTimeSlot</span><span class="sxs-lookup"><span data-stu-id="2409e-104">bookingWorkTimeSlot resource type</span></span>

 > <span data-ttu-id="2409e-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2409e-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2409e-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2409e-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="2409e-107">Las horas de inicio y finalización para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="2409e-107">The start and end times for work.</span></span>


## <a name="properties"></a><span data-ttu-id="2409e-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2409e-108">Properties</span></span>
| <span data-ttu-id="2409e-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2409e-109">Property</span></span>     | <span data-ttu-id="2409e-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="2409e-110">Type</span></span>   |<span data-ttu-id="2409e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2409e-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2409e-112">finalización</span><span class="sxs-lookup"><span data-stu-id="2409e-112">end</span></span>|<span data-ttu-id="2409e-113">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="2409e-113">TimeOfDay</span></span>|<span data-ttu-id="2409e-114">La hora del día que trabajo se inicia.</span><span class="sxs-lookup"><span data-stu-id="2409e-114">The time of the day that work starts.</span></span> <span data-ttu-id="2409e-115">Por ejemplo, 08:00:00.0000000.</span><span class="sxs-lookup"><span data-stu-id="2409e-115">For example, 08:00:00.0000000.</span></span>|
|<span data-ttu-id="2409e-116">start</span><span class="sxs-lookup"><span data-stu-id="2409e-116">start</span></span>|<span data-ttu-id="2409e-117">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="2409e-117">TimeOfDay</span></span>|<span data-ttu-id="2409e-118">La hora del día que trabajar se detiene.</span><span class="sxs-lookup"><span data-stu-id="2409e-118">The time of the day that work stops.</span></span> <span data-ttu-id="2409e-119">Por ejemplo, 17:00:00.0000000.</span><span class="sxs-lookup"><span data-stu-id="2409e-119">For example, 17:00:00.0000000.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="2409e-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2409e-120">JSON representation</span></span>

<span data-ttu-id="2409e-121">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="2409e-121">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.bookingWorkTimeSlot"
}-->

```json
{
  "end": "String (timestamp)",
  "start": "String (timestamp)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "bookingWorkTimeSlot resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
