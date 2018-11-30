---
title: Tipo de recurso plannerProgressTaskBoardTaskFormat
description: El recurso **plannerProgressTaskBoardTaskFormat** representa la información usada para procesar una tarea correctamente en la vista Progreso del panel de tareas (una vista organizada por el estado del campo PorcentajeCompletado en el objeto de la tarea, con columnas para No iniciado, En curso y Completado). Cada task tendrá un objeto **plannerProgressTaskBoardTaskFormat** asociado.
ms.openlocfilehash: 8ff6f536920bafb8734f63ef9fe9b72f8c2b1acb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085328"
---
# <a name="plannerprogresstaskboardtaskformat-resource-type"></a>Tipo de recurso plannerProgressTaskBoardTaskFormat

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **plannerProgressTaskBoardTaskFormat** representa la información usada para procesar una tarea correctamente en la vista Progreso del panel de tareas (una vista organizada por el estado del campo PorcentajeCompletado en el objeto de la tarea, con columnas para No iniciado, En curso y Completado). Cada [task](plannertask.md) tendrá un objeto **plannerProgressTaskBoardTaskFormat** asociado.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener plannerProgressTaskBoardTaskFormat](../api/plannerprogresstaskboardtaskformat-get.md) | [plannerProgressTaskBoardTaskFormat](plannerprogresstaskboardtaskformat.md) |Leer las propiedades y las relaciones del objeto **plannerProgressTaskBoardTaskFormat**.|
|[Update](../api/plannerprogresstaskboardtaskformat-update.md) | [plannerProgressTaskBoardTaskFormat](plannerprogresstaskboardtaskformat.md)    |Actualizar el objeto **plannerProgressTaskBoardTaskFormat**. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|String| Solo lectura. Identificador del recurso. Es 28 caracteres de largo y entre mayúsculas y minúsculas. [Validación de formato](tasks-identifiers-disclaimer.md) se realiza en el servicio.|
|orderHint|String|Valor de sugerencia usado para ordenar la tarea en la vista Progreso del panel de tareas. El formato se define tal como se describe [aquí](planner-order-hint-format.md).|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerProgressTaskBoardTaskFormat"
}-->

```json
{
  "id": "String (identifier)",
  "orderHint": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerProgressTaskBoardTaskFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->