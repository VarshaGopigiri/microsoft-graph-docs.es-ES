---
title: Tipo de recurso plannerAssignedToTaskBoardTaskFormat
description: El recurso **plannerAssignedToTaskBoardTaskFormat** representa la información usada para procesar una tarea correctamente en la vista AsignadoA del panel de tareas (una vista organizada por usuarios a los que se asignan las tareas). Cada task tendrá un objeto **plannerAssignedToTaskBoardTaskFormat** asociado.
ms.openlocfilehash: 35aaf5d93e4190fead1234131864e7fab11b96b5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031159"
---
# <a name="plannerassignedtotaskboardtaskformat-resource-type"></a>Tipo de recurso plannerAssignedToTaskBoardTaskFormat

El recurso **plannerAssignedToTaskBoardTaskFormat** representa la información usada para procesar una tarea correctamente en la vista AsignadoA del panel de tareas (una vista organizada por usuarios a los que se asignan las tareas). Cada [task](plannertask.md) tendrá un objeto **plannerAssignedToTaskBoardTaskFormat** asociado.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener plannerAssignedToTaskBoardTaskFormat](../api/plannerassignedtotaskboardtaskformat-get.md) | [plannerAssignedToTaskBoardTaskFormat](plannerassignedtotaskboardtaskformat.md) |Leer las propiedades y las relaciones del objeto **plannerAssignedToTaskBoardTaskFormat**.|
|[Update](../api/plannerassignedtotaskboardtaskformat-update.md) | [plannerAssignedToTaskBoardTaskFormat](plannerassignedtotaskboardtaskformat.md)  |Actualizar el objeto **plannerAssignedToTaskBoardTaskFormat**. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|String| Solo lectura. Identificador del recurso. Es 28 caracteres de largo y entre mayúsculas y minúsculas. [Validación de formato](planner-identifiers-disclaimer.md) se realiza en el servicio.|
|orderHintsByAssignee|[plannerOrderHintsByAssignee](plannerorderhintsbyassignee.md)|Diccionario de sugerencias usadas para ordenar las tareas en la vista AsignadoA del panel de tareas. La clave de cada entrada es uno de los usuarios a los que se ha asignado la tarea, mientras que el valor es la sugerencia de orden. El formato de cada valor se define tal como se describe [aquí](planner-order-hint-format.md).|
|unassignedOrderHint|String|Valor de sugerencia usado para ordenar la tarea en la vista AsignadoA del panel de tareas si la tarea no está asignada a nadie, o si el diccionario orderHintsByAssignee no proporciona ninguna sugerencia de orden para el usuario al que se ha asignado la tarea. El formato se define tal como se describe [aquí](planner-order-hint-format.md).|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.plannerAssignedToTaskBoardTaskFormat"
}-->

```json
{
  "id": "String (identifier)",
  "orderHintsByAssignee": {"@odata.type": "microsoft.graph.plannerOrderHintsByAssignee"},
  "unassignedOrderHint": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerAssignedToTaskBoardTaskFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->