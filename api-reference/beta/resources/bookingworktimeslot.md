---
title: tipo de recurso bookingWorkTimeSlot
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
ms.openlocfilehash: 69a802e4addd3c0cb821a630707a62724ea984a2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27839560"
---
# <a name="bookingworktimeslot-resource-type"></a><span data-ttu-id="7a705-104">tipo de recurso bookingWorkTimeSlot</span><span class="sxs-lookup"><span data-stu-id="7a705-104">bookingWorkTimeSlot resource type</span></span>

 > <span data-ttu-id="7a705-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7a705-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7a705-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7a705-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="7a705-107">Las horas de inicio y finalización para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="7a705-107">The start and end times for work.</span></span>


## <a name="properties"></a><span data-ttu-id="7a705-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7a705-108">Properties</span></span>
| <span data-ttu-id="7a705-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7a705-109">Property</span></span>     | <span data-ttu-id="7a705-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="7a705-110">Type</span></span>   |<span data-ttu-id="7a705-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a705-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7a705-112">finalización</span><span class="sxs-lookup"><span data-stu-id="7a705-112">end</span></span>|<span data-ttu-id="7a705-113">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="7a705-113">TimeOfDay</span></span>|<span data-ttu-id="7a705-114">La hora del día que trabajo se inicia.</span><span class="sxs-lookup"><span data-stu-id="7a705-114">The time of the day that work starts.</span></span> <span data-ttu-id="7a705-115">Por ejemplo, 08:00:00.0000000.</span><span class="sxs-lookup"><span data-stu-id="7a705-115">For example, 08:00:00.0000000.</span></span>|
|<span data-ttu-id="7a705-116">start</span><span class="sxs-lookup"><span data-stu-id="7a705-116">start</span></span>|<span data-ttu-id="7a705-117">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="7a705-117">TimeOfDay</span></span>|<span data-ttu-id="7a705-118">La hora del día que trabajar se detiene.</span><span class="sxs-lookup"><span data-stu-id="7a705-118">The time of the day that work stops.</span></span> <span data-ttu-id="7a705-119">Por ejemplo, 17:00:00.0000000.</span><span class="sxs-lookup"><span data-stu-id="7a705-119">For example, 17:00:00.0000000.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="7a705-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7a705-120">JSON representation</span></span>

<span data-ttu-id="7a705-121">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="7a705-121">The following is a JSON representation of the resource.</span></span>

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
