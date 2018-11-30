---
title: Tipo de recurso patternedRecurrence
description: Patrón e intervalo de periodicidad.
ms.openlocfilehash: 10a90db032cd7461e28bc096fd6213df44f3ea45
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029602"
---
# <a name="patternedrecurrence-resource-type"></a><span data-ttu-id="a5d7f-103">Tipo de recurso patternedRecurrence</span><span class="sxs-lookup"><span data-stu-id="a5d7f-103">patternedRecurrence resource type</span></span>

<span data-ttu-id="a5d7f-104">Patrón e intervalo de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="a5d7f-104">The recurrence pattern and range.</span></span>

## <a name="properties"></a><span data-ttu-id="a5d7f-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a5d7f-105">Properties</span></span>
| <span data-ttu-id="a5d7f-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a5d7f-106">Property</span></span>     | <span data-ttu-id="a5d7f-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="a5d7f-107">Type</span></span>   |<span data-ttu-id="a5d7f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5d7f-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a5d7f-109">pattern</span><span class="sxs-lookup"><span data-stu-id="a5d7f-109">pattern</span></span>|[<span data-ttu-id="a5d7f-110">RecurrencePattern</span><span class="sxs-lookup"><span data-stu-id="a5d7f-110">RecurrencePattern</span></span>](recurrencepattern.md)|<span data-ttu-id="a5d7f-111">Frecuencia de un evento.</span><span class="sxs-lookup"><span data-stu-id="a5d7f-111">The frequency of an event.</span></span>|
|<span data-ttu-id="a5d7f-112">range</span><span class="sxs-lookup"><span data-stu-id="a5d7f-112">range</span></span>|[<span data-ttu-id="a5d7f-113">RecurrenceRange</span><span class="sxs-lookup"><span data-stu-id="a5d7f-113">RecurrenceRange</span></span>](recurrencerange.md)|<span data-ttu-id="a5d7f-114">Duración de un evento.</span><span class="sxs-lookup"><span data-stu-id="a5d7f-114">The duration of an event.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="a5d7f-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a5d7f-115">JSON representation</span></span>

<span data-ttu-id="a5d7f-116">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="a5d7f-116">Here is a JSON representation of the resource</span></span>

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
