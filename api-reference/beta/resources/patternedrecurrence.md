---
title: Tipo de recurso patternedRecurrence
description: Patrón e intervalo de periodicidad.
ms.openlocfilehash: 205c563d8b4cecc0a817dd1893a6c4f002eb4e06
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090991"
---
# <a name="patternedrecurrence-resource-type"></a><span data-ttu-id="19997-103">Tipo de recurso patternedRecurrence</span><span class="sxs-lookup"><span data-stu-id="19997-103">patternedRecurrence resource type</span></span>

> <span data-ttu-id="19997-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="19997-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="19997-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="19997-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="19997-106">Patrón e intervalo de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="19997-106">The recurrence pattern and range.</span></span>

## <a name="properties"></a><span data-ttu-id="19997-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="19997-107">Properties</span></span>
| <span data-ttu-id="19997-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="19997-108">Property</span></span>     | <span data-ttu-id="19997-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="19997-109">Type</span></span>   |<span data-ttu-id="19997-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="19997-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="19997-111">pattern</span><span class="sxs-lookup"><span data-stu-id="19997-111">pattern</span></span>|[<span data-ttu-id="19997-112">RecurrencePattern</span><span class="sxs-lookup"><span data-stu-id="19997-112">RecurrencePattern</span></span>](recurrencepattern.md)|<span data-ttu-id="19997-113">Frecuencia de un evento.</span><span class="sxs-lookup"><span data-stu-id="19997-113">The frequency of an event.</span></span>|
|<span data-ttu-id="19997-114">range</span><span class="sxs-lookup"><span data-stu-id="19997-114">range</span></span>|[<span data-ttu-id="19997-115">RecurrenceRange</span><span class="sxs-lookup"><span data-stu-id="19997-115">RecurrenceRange</span></span>](recurrencerange.md)|<span data-ttu-id="19997-116">Duración de un evento.</span><span class="sxs-lookup"><span data-stu-id="19997-116">The duration of an event.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="19997-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="19997-117">JSON representation</span></span>

<span data-ttu-id="19997-118">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="19997-118">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.patternedRecurrence"
}-->

```json
{
  "pattern": {"@odata.type": "microsoft.graph.recurrencePattern"},
  "range": {"@odata.type": "microsoft.graph.recurrenceRange"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "patternedRecurrence resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
