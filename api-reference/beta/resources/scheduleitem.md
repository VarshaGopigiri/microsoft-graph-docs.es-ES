---
title: tipo de recurso scheduleItem
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
ms.openlocfilehash: e5d14826a27153af27648484554ec864d62ed6c7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27890436"
---
# <a name="scheduleitem-resource-type"></a><span data-ttu-id="7b9dc-104">tipo de recurso scheduleItem</span><span class="sxs-lookup"><span data-stu-id="7b9dc-104">scheduleItem resource type</span></span>

 > <span data-ttu-id="7b9dc-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7b9dc-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7b9dc-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7b9dc-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="7b9dc-107">Un elemento que se describe la disponibilidad de un usuario correspondiente a un evento real en el calendario del usuario de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7b9dc-107">An item that describes the availability of a user corresponding to an actual event on the user's default calendar.</span></span> <span data-ttu-id="7b9dc-108">En este artículo se aplica a así como un recurso.</span><span class="sxs-lookup"><span data-stu-id="7b9dc-108">This item applies to a resource as well.</span></span>

## <a name="properties"></a><span data-ttu-id="7b9dc-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7b9dc-109">Properties</span></span>
| <span data-ttu-id="7b9dc-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7b9dc-110">Property</span></span>     | <span data-ttu-id="7b9dc-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="7b9dc-111">Type</span></span>   |<span data-ttu-id="7b9dc-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b9dc-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7b9dc-113">finalización</span><span class="sxs-lookup"><span data-stu-id="7b9dc-113">end</span></span> |[<span data-ttu-id="7b9dc-114">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="7b9dc-114">dateTimeTimeZone</span></span>](datetimetimezone.md) |<span data-ttu-id="7b9dc-115">La fecha, hora y zona horaria que finaliza el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7b9dc-115">The date, time, and time zone that the corresponding event ends.</span></span> |
|<span data-ttu-id="7b9dc-116">isPrivate</span><span class="sxs-lookup"><span data-stu-id="7b9dc-116">isPrivate</span></span> |<span data-ttu-id="7b9dc-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="7b9dc-117">Boolean</span></span> |<span data-ttu-id="7b9dc-118">La sensibilidad del evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7b9dc-118">The sensitivity of the corresponding event.</span></span> <span data-ttu-id="7b9dc-119">Es True si el evento está marcado como `private`, false en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7b9dc-119">True if the event is marked `private`, false otherwise.</span></span> |
|<span data-ttu-id="7b9dc-120">location</span><span class="sxs-lookup"><span data-stu-id="7b9dc-120">location</span></span> |<span data-ttu-id="7b9dc-121">String</span><span class="sxs-lookup"><span data-stu-id="7b9dc-121">String</span></span> | <span data-ttu-id="7b9dc-122">La ubicación donde se conservan o atendido desde el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7b9dc-122">The location where the corresponding event is held or attended from.</span></span> <span data-ttu-id="7b9dc-123">Opcional.</span><span class="sxs-lookup"><span data-stu-id="7b9dc-123">Optional.</span></span>|
|<span data-ttu-id="7b9dc-124">inicio</span><span class="sxs-lookup"><span data-stu-id="7b9dc-124">start</span></span> |[<span data-ttu-id="7b9dc-125">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="7b9dc-125">dateTimeTimeZone</span></span>](datetimetimezone.md) |<span data-ttu-id="7b9dc-126">La fecha, hora y zona horaria que se inicia el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7b9dc-126">The date, time, and time zone that the corresponding event starts.</span></span> |
|<span data-ttu-id="7b9dc-127">status</span><span class="sxs-lookup"><span data-stu-id="7b9dc-127">status</span></span> |<span data-ttu-id="7b9dc-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="7b9dc-128">String</span></span> | <span data-ttu-id="7b9dc-129">El estado de disponibilidad del usuario o recurso durante el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7b9dc-129">The availability status of the user or resource during the corresponding event.</span></span> <span data-ttu-id="7b9dc-130">Los valores posibles son: `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`.</span><span class="sxs-lookup"><span data-stu-id="7b9dc-130">The possible values are: `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`.</span></span> |
|<span data-ttu-id="7b9dc-131">subject</span><span class="sxs-lookup"><span data-stu-id="7b9dc-131">subject</span></span> |<span data-ttu-id="7b9dc-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="7b9dc-132">String</span></span> | <span data-ttu-id="7b9dc-133">Línea de asunto del evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7b9dc-133">The corresponding event's subject line.</span></span> <span data-ttu-id="7b9dc-134">Opcional.</span><span class="sxs-lookup"><span data-stu-id="7b9dc-134">Optional.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="7b9dc-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7b9dc-135">JSON representation</span></span>

<span data-ttu-id="7b9dc-136">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="7b9dc-136">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.scheduleItem"
}-->

```json
{
  "end": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "isPrivate": true,
  "location": "String",
  "start": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "status": "String",
  "subject": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "scheduleItem resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
