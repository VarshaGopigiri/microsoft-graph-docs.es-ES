---
title: Tipo de recurso plannerBucketTaskBoardTaskFormat
description: El recurso **plannerBucketTaskBoardTaskFormat** representa la información usada para procesar una tarea correctamente en la vista Depósitos del panel de tareas (una vista organizada por tareas dentro de los depósitos a los que están asignadas). Cada task tendrá un objeto **plannerBucketTaskBoardTaskFormat** asociado.
localization_priority: Normal
ms.openlocfilehash: a4fae04147bb97a7128f7b8ad881ac9b34cb7d8c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27836081"
---
# <a name="plannerbuckettaskboardtaskformat-resource-type"></a>Tipo de recurso plannerBucketTaskBoardTaskFormat

El recurso **plannerBucketTaskBoardTaskFormat** representa la información usada para procesar una tarea correctamente en la vista Depósitos del panel de tareas (una vista organizada por tareas dentro de los depósitos a los que están asignadas). Cada [task](plannertask.md) tendrá un objeto **plannerBucketTaskBoardTaskFormat** asociado.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener plannerBucketTaskBoardTaskFormat](../api/plannerbuckettaskboardtaskformat-get.md) | [plannerBucketTaskBoardTaskFormat](plannerbuckettaskboardtaskformat.md) |Leer las propiedades y las relaciones del objeto **plannerBucketTaskBoardTaskFormat**.|
|[Update](../api/plannerbuckettaskboardtaskformat-update.md) | [plannerBucketTaskBoardTaskFormat](plannerbuckettaskboardtaskformat.md)  |Actualizar el objeto **plannerBucketTaskBoardTaskFormat**. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|Cadena| Solo lectura. Identificador del recurso. Es 28 caracteres de largo y entre mayúsculas y minúsculas. [Validación de formato](planner-identifiers-disclaimer.md) se realiza en el servicio.|
|orderHint|Cadena|Sugerencia usada para ordenar tareas en la vista Depósito del panel de tareas. El formato se define tal como se describe [aquí](planner-order-hint-format.md).|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.plannerBucketTaskBoardTaskFormat"
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
  "description": "plannerBucketTaskBoardTaskFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
