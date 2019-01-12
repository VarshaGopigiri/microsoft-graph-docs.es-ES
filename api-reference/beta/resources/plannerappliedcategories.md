---
title: Tipo de recurso plannerAppliedCategories
description: El recurso **AppliedCategoriesCollection** representa la colección de categorías (y etiquetas) que se han aplicado a una tarea. Forma parte del objeto plannerTask.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: b237f5f395ce592829e8abfee152caf07e417b0c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27933033"
---
# <a name="plannerappliedcategories-resource-type"></a>Tipo de recurso plannerAppliedCategories

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **AppliedCategoriesCollection** representa la colección de categorías (o de etiquetas) que se han aplicado a una tarea. Forma parte del objeto [plannerTask](plannertask.md). Puede haber hasta 6 categorías aplicadas a una tarea. Las descripciones de las categorías (por ejemplo, `category1`, `category2`, etc.) forman parte del objeto [plan details](plannerplandetails.md). Este es un tipo abierto.

## <a name="properties"></a>Propiedades
El cliente puede definir las propiedades de un tipo abierto. En este caso, el cliente debe proporcionar `category1`, `category2`, `category3`, `category4`, `category5` o `category6` como propiedades con sus valores como booleano `true` cuando se apliquen las categorías correspondientes en la tarea. A continuación se muestra un ejemplo. Si no se aplican, las propiedades se quitan automáticamente estableciendo sus valores en el booleano `false`. 

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerAppliedCategories"
}-->

```json
{
  "String-value": true
}
```

Ejemplo: 

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
