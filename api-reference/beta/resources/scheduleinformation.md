---
title: tipo de recurso scheduleInformation
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: 0b7bbd861a044b28cd22603fd0ccc27d20f46fba
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086471"
---
# <a name="scheduleinformation-resource-type"></a><span data-ttu-id="5067f-104">tipo de recurso scheduleInformation</span><span class="sxs-lookup"><span data-stu-id="5067f-104">scheduleInformation resource type</span></span>

 > <span data-ttu-id="5067f-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5067f-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5067f-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5067f-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="5067f-107">Representa la disponibilidad de un usuario, una lista de distribución o un recurso para un período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="5067f-107">Represents the availability of a user, distribution list, or resource for a specified time period.</span></span>

## <a name="properties"></a><span data-ttu-id="5067f-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5067f-108">Properties</span></span>
| <span data-ttu-id="5067f-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5067f-109">Property</span></span>     | <span data-ttu-id="5067f-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="5067f-110">Type</span></span>   |<span data-ttu-id="5067f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5067f-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5067f-112">availabilityView</span><span class="sxs-lookup"><span data-stu-id="5067f-112">availabilityView</span></span> |<span data-ttu-id="5067f-113">String</span><span class="sxs-lookup"><span data-stu-id="5067f-113">String</span></span> |<span data-ttu-id="5067f-114">Representa una vista combinada de disponibilidad de todos los elementos en `scheduleItems`.</span><span class="sxs-lookup"><span data-stu-id="5067f-114">Represents a merged view of availability of all the items in `scheduleItems`.</span></span> <span data-ttu-id="5067f-115">La vista se compone de intervalos de tiempo.</span><span class="sxs-lookup"><span data-stu-id="5067f-115">The view consists of time slots.</span></span> <span data-ttu-id="5067f-116">Disponibilidad durante cada franja horaria se indica con: `0`= gratis, `1`= provisional, `2`= ocupado, `3`= fuera de la oficina, `4`= trabajar en otro lugar.</span><span class="sxs-lookup"><span data-stu-id="5067f-116">Availability during each time slot is indicated with: `0`= free, `1`= tentative, `2`= busy, `3`= out of office, `4`= working elsewhere.</span></span>|
|<span data-ttu-id="5067f-117">error</span><span class="sxs-lookup"><span data-stu-id="5067f-117">error</span></span> |[<span data-ttu-id="5067f-118">freeBusyError</span><span class="sxs-lookup"><span data-stu-id="5067f-118">freeBusyError</span></span>](freebusyerror.md) |<span data-ttu-id="5067f-119">Información de error al intentar obtener la disponibilidad del usuario, la lista de distribución o el recurso.</span><span class="sxs-lookup"><span data-stu-id="5067f-119">Error information from attempting to get the availability of the user, distribution list, or resource.</span></span> |
|<span data-ttu-id="5067f-120">scheduleId</span><span class="sxs-lookup"><span data-stu-id="5067f-120">scheduleId</span></span> |<span data-ttu-id="5067f-121">String</span><span class="sxs-lookup"><span data-stu-id="5067f-121">String</span></span> |<span data-ttu-id="5067f-122">Una dirección SMTP del usuario, la lista de distribución o el recurso, que identifica una instancia de **scheduleInformation**.</span><span class="sxs-lookup"><span data-stu-id="5067f-122">An SMTP address of the user, distribution list, or resource, identifying an instance of **scheduleInformation**.</span></span> |
|<span data-ttu-id="5067f-123">scheduleItems</span><span class="sxs-lookup"><span data-stu-id="5067f-123">scheduleItems</span></span> |<span data-ttu-id="5067f-124">colección [scheduleItem](scheduleitem.md)</span><span class="sxs-lookup"><span data-stu-id="5067f-124">[scheduleItem](scheduleitem.md) collection</span></span> |<span data-ttu-id="5067f-125">Contiene los elementos que describen la disponibilidad del usuario o recurso.</span><span class="sxs-lookup"><span data-stu-id="5067f-125">Contains the items that describe the availability of the user or resource.</span></span> |
|<span data-ttu-id="5067f-126">workingHours</span><span class="sxs-lookup"><span data-stu-id="5067f-126">workingHours</span></span> |[<span data-ttu-id="5067f-127">workingHours</span><span class="sxs-lookup"><span data-stu-id="5067f-127">workingHours</span></span>](workinghours.md) |<span data-ttu-id="5067f-128">Días de la semana y horas de la zona horaria específica en la que trabaja el usuario.</span><span class="sxs-lookup"><span data-stu-id="5067f-128">The days of the week and hours in a specific time zone that the user works.</span></span> <span data-ttu-id="5067f-129">Estos se establecen como parte de del usuario [mailboxSettings](mailboxsettings.md).</span><span class="sxs-lookup"><span data-stu-id="5067f-129">These are set as part of the user's [mailboxSettings](mailboxsettings.md).</span></span>|


## <a name="json-representation"></a><span data-ttu-id="5067f-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5067f-130">JSON representation</span></span>

<span data-ttu-id="5067f-131">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="5067f-131">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.scheduleInformation"
}-->

```json
{
  "availabilityView": "String",
  "error": {"@odata.type": "microsoft.graph.freeBusyError"},
  "scheduleId": "String",
  "scheduleItems": [{"@odata.type": "microsoft.graph.scheduleItem"}],
  "workingHours": {"@odata.type": "microsoft.graph.workingHours"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "scheduleInformation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->