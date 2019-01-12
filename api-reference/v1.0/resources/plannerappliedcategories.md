---
title: Tipo de recurso plannerAppliedCategories
description: El recurso **AppliedCategoriesCollection** representa la colección de categorías (y etiquetas) que se han aplicado a una tarea. Forma parte del objeto plannerTask.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: 604cf63d922ab59e038b5ccb8ea3b48a707a9bc0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27981605"
---
# <a name="plannerappliedcategories-resource-type"></a><span data-ttu-id="79f84-104">Tipo de recurso plannerAppliedCategories</span><span class="sxs-lookup"><span data-stu-id="79f84-104">plannerAppliedCategories resource type</span></span>


<span data-ttu-id="79f84-p102">El recurso **AppliedCategoriesCollection** representa la colección de categorías (o de etiquetas) que se han aplicado a una tarea. Forma parte del objeto [plannerTask](plannertask.md). Puede haber hasta 6 categorías aplicadas a una tarea. Las descripciones de las categorías (por ejemplo, `category1`, `category2`, etc.) forman parte del objeto [plan details](plannerplandetails.md). Este es un tipo abierto.</span><span class="sxs-lookup"><span data-stu-id="79f84-p102">The **AppliedCategoriesCollection** resource represents the collection of categories (or labels) that have been applied to a task. It is part of the [plannerTask](plannertask.md) object. There can be up to 6 categories applied to a task. Category descriptions, e.g. `category1`, `category2` etc., are part of the [plan details](plannerplandetails.md) object. This is an open type.</span></span>

## <a name="properties"></a><span data-ttu-id="79f84-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="79f84-110">Properties</span></span>
<span data-ttu-id="79f84-p103">El cliente puede definir las propiedades de un tipo abierto. En este caso, el cliente debe proporcionar `category1`, `category2`, `category3`, `category4`, `category5` o `category6` como propiedades con sus valores como booleano `true` cuando se apliquen las categorías correspondientes en la tarea. A continuación se muestra un ejemplo. Si no se aplican, las propiedades se quitan automáticamente estableciendo sus valores en el booleano `false`.</span><span class="sxs-lookup"><span data-stu-id="79f84-p103">Properties of an Open Type can be defined by the client. In this case though, the client must provide `category1`, `category2`, `category3`, `category4`, `category5` and/or `category6` as properties with their values being the `true` boolean when the corresponding categories are applied on the task. Example is shown below. When they do not apply, properties are automatically removed by setting their values to the `false` boolean.</span></span> 

## <a name="json-representation"></a><span data-ttu-id="79f84-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="79f84-115">JSON representation</span></span>

<span data-ttu-id="79f84-116">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="79f84-116">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "openType": true,
  "optionalProperties": [ "String-value" ],
  "@odata.type": "microsoft.graph.plannerAppliedCategories"
}-->

```json
{
  "String-value": true
}
```

<span data-ttu-id="79f84-117">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="79f84-117">Example:</span></span> 

```json
{
  "category1": true,
  "category3": true,
  "category5": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerAppliedCategories resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
