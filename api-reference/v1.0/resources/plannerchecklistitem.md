---
title: Tipo de recurso plannerChecklistItem
description: El recurso **plannerChecklistItem** representa un elemento de la lista de comprobación de una tarea. La lista de comprobación en una tarea está representado por el objeto de comprobación.
ms.openlocfilehash: b3c4f9c7e7429487c1a9d44ba76ce1ef0a551f9c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032574"
---
# <a name="plannerchecklistitem-resource-type"></a><span data-ttu-id="c34d3-104">Tipo de recurso plannerChecklistItem</span><span class="sxs-lookup"><span data-stu-id="c34d3-104">plannerChecklistItem resource type</span></span>


<span data-ttu-id="c34d3-p102">El recurso **plannerChecklistItem** representa un elemento de la lista de comprobación de una tarea. La lista de comprobación de una tarea está representada por el objeto [checklistItems](plannerchecklistitems.md).</span><span class="sxs-lookup"><span data-stu-id="c34d3-p102">The **plannerChecklistItem** resource represents an item in the checklist of a task. The checklist on a task is represented by the [checklistItems object](plannerchecklistitems.md).</span></span>


## <a name="properties"></a><span data-ttu-id="c34d3-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c34d3-107">Properties</span></span>
| <span data-ttu-id="c34d3-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c34d3-108">Property</span></span>     | <span data-ttu-id="c34d3-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="c34d3-109">Type</span></span>   |<span data-ttu-id="c34d3-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c34d3-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c34d3-111">isChecked</span><span class="sxs-lookup"><span data-stu-id="c34d3-111">isChecked</span></span>|<span data-ttu-id="c34d3-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="c34d3-112">Boolean</span></span>|<span data-ttu-id="c34d3-113">El valor es `true` si el elemento está activado o `false` si no lo está.</span><span class="sxs-lookup"><span data-stu-id="c34d3-113">Value is `true` if the item is checked and `false` otherwise.</span></span>|
|<span data-ttu-id="c34d3-114">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="c34d3-114">lastModifiedBy</span></span>|[<span data-ttu-id="c34d3-115">identitySet</span><span class="sxs-lookup"><span data-stu-id="c34d3-115">identitySet</span></span>](identityset.md)| <span data-ttu-id="c34d3-p103">Solo lectura. Id. del usuario que lo modificó por última vez.</span><span class="sxs-lookup"><span data-stu-id="c34d3-p103">Read-only. User ID by which this is last modified.</span></span>|
|<span data-ttu-id="c34d3-118">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="c34d3-118">lastModifiedDateTime</span></span>|<span data-ttu-id="c34d3-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c34d3-119">DateTimeOffset</span></span>|<span data-ttu-id="c34d3-p104">Solo lectura. Fecha y hora en que se modificó por última vez. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, la medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="c34d3-p104">Read-only. Date and time at which this is last modified. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="c34d3-124">orderHint</span><span class="sxs-lookup"><span data-stu-id="c34d3-124">orderHint</span></span>|<span data-ttu-id="c34d3-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="c34d3-125">String</span></span>|<span data-ttu-id="c34d3-p105">Se usa para establecer el orden relativo de los elementos de la lista de comprobación. El formato se define tal como se describe [aquí](planner-order-hint-format.md).</span><span class="sxs-lookup"><span data-stu-id="c34d3-p105">Used to set the relative order of items in the checklist. The format is defined as outlined [here](planner-order-hint-format.md).</span></span>|
|<span data-ttu-id="c34d3-128">title</span><span class="sxs-lookup"><span data-stu-id="c34d3-128">title</span></span>|<span data-ttu-id="c34d3-129">String</span><span class="sxs-lookup"><span data-stu-id="c34d3-129">String</span></span>|<span data-ttu-id="c34d3-130">Título del elemento de la lista de comprobación</span><span class="sxs-lookup"><span data-stu-id="c34d3-130">Title of the checklist item</span></span>|

## <a name="json-representation"></a><span data-ttu-id="c34d3-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c34d3-131">JSON representation</span></span>
<span data-ttu-id="c34d3-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c34d3-132">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerChecklistItem"
}-->

```json
{
  "isChecked": true,
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)",
  "orderHint": "String",
  "title": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerChecklistItem resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->