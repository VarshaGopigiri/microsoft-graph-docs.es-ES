---
title: Tipo de recurso plannerChecklistItem
description: El recurso **plannerChecklistItem** representa un elemento de la lista de comprobación de una tarea. La lista de comprobación en una tarea está representado por el objeto de comprobación.
ms.openlocfilehash: 846c1877fb421c9070eff7c041983367a7beb29b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086430"
---
# <a name="plannerchecklistitem-resource-type"></a><span data-ttu-id="ccd84-104">Tipo de recurso plannerChecklistItem</span><span class="sxs-lookup"><span data-stu-id="ccd84-104">plannerChecklistItem resource type</span></span>

> <span data-ttu-id="ccd84-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ccd84-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ccd84-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ccd84-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ccd84-p103">El recurso **plannerChecklistItem** representa un elemento de la lista de comprobación de una tarea. La lista de comprobación de una tarea está representada por el objeto [checklistItems](plannerchecklistitems.md).</span><span class="sxs-lookup"><span data-stu-id="ccd84-p103">The **plannerChecklistItem** resource represents an item in the checklist of a task. The checklist on a task is represented by the [checklistItems object](plannerchecklistitems.md).</span></span>


## <a name="properties"></a><span data-ttu-id="ccd84-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ccd84-109">Properties</span></span>
| <span data-ttu-id="ccd84-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ccd84-110">Property</span></span>     | <span data-ttu-id="ccd84-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="ccd84-111">Type</span></span>   |<span data-ttu-id="ccd84-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ccd84-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ccd84-113">isChecked</span><span class="sxs-lookup"><span data-stu-id="ccd84-113">isChecked</span></span>|<span data-ttu-id="ccd84-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="ccd84-114">Boolean</span></span>|<span data-ttu-id="ccd84-115">El valor es `true` si el elemento está activado o `false` si no lo está.</span><span class="sxs-lookup"><span data-stu-id="ccd84-115">Value is `true` if the item is checked and `false` otherwise.</span></span>|
|<span data-ttu-id="ccd84-116">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="ccd84-116">lastModifiedBy</span></span>|[<span data-ttu-id="ccd84-117">identitySet</span><span class="sxs-lookup"><span data-stu-id="ccd84-117">identitySet</span></span>](identityset.md)| <span data-ttu-id="ccd84-p104">Solo lectura. Id. del usuario que lo modificó por última vez.</span><span class="sxs-lookup"><span data-stu-id="ccd84-p104">Read-only. User ID by which this is last modified.</span></span>|
|<span data-ttu-id="ccd84-120">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="ccd84-120">lastModifiedDateTime</span></span>|<span data-ttu-id="ccd84-121">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ccd84-121">DateTimeOffset</span></span>|<span data-ttu-id="ccd84-p105">Solo lectura. Fecha y hora en que se modificó por última vez. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, la medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="ccd84-p105">Read-only. Date and time at which this is last modified. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="ccd84-126">orderHint</span><span class="sxs-lookup"><span data-stu-id="ccd84-126">orderHint</span></span>|<span data-ttu-id="ccd84-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="ccd84-127">String</span></span>|<span data-ttu-id="ccd84-p106">Se usa para establecer el orden relativo de los elementos de la lista de comprobación. El formato se define tal como se describe [aquí](planner-order-hint-format.md).</span><span class="sxs-lookup"><span data-stu-id="ccd84-p106">Used to set the relative order of items in the checklist. The format is defined as outlined [here](planner-order-hint-format.md).</span></span>|
|<span data-ttu-id="ccd84-130">title</span><span class="sxs-lookup"><span data-stu-id="ccd84-130">title</span></span>|<span data-ttu-id="ccd84-131">String</span><span class="sxs-lookup"><span data-stu-id="ccd84-131">String</span></span>|<span data-ttu-id="ccd84-132">Título del elemento de la lista de comprobación</span><span class="sxs-lookup"><span data-stu-id="ccd84-132">Title of the checklist item</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ccd84-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ccd84-133">JSON representation</span></span>
<span data-ttu-id="ccd84-134">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ccd84-134">Here is a JSON representation of the resource.</span></span>

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