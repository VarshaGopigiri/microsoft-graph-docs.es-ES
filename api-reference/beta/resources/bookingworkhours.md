---
title: tipo de recurso bookingWorkHours
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
ms.openlocfilehash: 94920287cd7358c68686da2d0969c676e3c481ee
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888959"
---
# <a name="bookingworkhours-resource-type"></a><span data-ttu-id="46dc0-104">tipo de recurso bookingWorkHours</span><span class="sxs-lookup"><span data-stu-id="46dc0-104">bookingWorkHours resource type</span></span>

 > <span data-ttu-id="46dc0-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="46dc0-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="46dc0-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="46dc0-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="46dc0-107">Representa el conjunto de horas de trabajo en un solo día de la semana, para un [bookingBusiness](bookingbusiness.md) o [bookingStaffMember](bookingstaffmember.md).</span><span class="sxs-lookup"><span data-stu-id="46dc0-107">Represents the set of working hours in a single day of the week, for a [bookingBusiness](bookingbusiness.md) or [bookingStaffMember](bookingstaffmember.md).</span></span>

## <a name="properties"></a><span data-ttu-id="46dc0-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="46dc0-108">Properties</span></span>
| <span data-ttu-id="46dc0-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="46dc0-109">Property</span></span>     | <span data-ttu-id="46dc0-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="46dc0-110">Type</span></span>   |<span data-ttu-id="46dc0-111">Description</span><span class="sxs-lookup"><span data-stu-id="46dc0-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="46dc0-112">día</span><span class="sxs-lookup"><span data-stu-id="46dc0-112">day</span></span>|<span data-ttu-id="46dc0-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="46dc0-113">String</span></span>| <span data-ttu-id="46dc0-114">El día de la semana representado por esta instancia.</span><span class="sxs-lookup"><span data-stu-id="46dc0-114">The day of the week represented by this instance.</span></span> <span data-ttu-id="46dc0-115">Los valores posibles son: `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday` y `saturday`.</span><span class="sxs-lookup"><span data-stu-id="46dc0-115">Possible values are: `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday`, `saturday`.</span></span>|
|<span data-ttu-id="46dc0-116">intervalos de tiempo</span><span class="sxs-lookup"><span data-stu-id="46dc0-116">timeSlots</span></span>|<span data-ttu-id="46dc0-117">colección de [bookingWorkTimeSlot](bookingworktimeslot.md)</span><span class="sxs-lookup"><span data-stu-id="46dc0-117">[bookingWorkTimeSlot](bookingworktimeslot.md) collection</span></span>|<span data-ttu-id="46dc0-118">Una lista de horas de inicio y fin durante un día.</span><span class="sxs-lookup"><span data-stu-id="46dc0-118">A list of start/end times during a day.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="46dc0-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="46dc0-119">JSON representation</span></span>

<span data-ttu-id="46dc0-120">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="46dc0-120">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.bookingWorkHours"
}-->

```json
{
  "day": "String",
  "timeSlots": [{"@odata.type": "microsoft.graph.bookingWorkTimeSlot"}]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "bookingWorkHours resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
