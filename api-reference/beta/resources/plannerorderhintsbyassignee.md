---
title: Tipo de recurso plannerOrderHintsByAssignee
description: El **plannerOrderHintsByAssignee** es un recurso que contiene sugerencias de ordenación para las personas asignadas en un recurso de plannerTask, para indicar el orden de la tarea en asignado a la vista del panel de tareas de.
ms.openlocfilehash: a15a1f81b348958e5c38189db10743b83d72050f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084870"
---
# <a name="plannerorderhintsbyassignee-resource-type"></a>Tipo de recurso plannerOrderHintsByAssignee

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **plannerOrderHintsByAssignee** es un recurso que contiene [sugerencias de orden](planner-order-hint-format.md) para las personas asignadas en un recurso [plannerTask](plannertask.md), para indicar el orden de la tarea en la vista Asignado a del panel de tareas. Este tipo es un tipo abierto. Las propiedades son los identificadores de los usuarios asignados a la tarea, mientras que los valores son sugerencias de orden.

## <a name="properties"></a>Propiedades
El cliente puede definir las propiedades de un tipo abierto. En este caso, el cliente debe proporcionar los identificadores de los usuarios asignados a la tarea como nombres de propiedad, así como una [sugerencia de orden](planner-order-hint-format.md) válida como valor. Las propiedades no se pueden quitar de este tipo. El servicio quitará automáticamente los valores a medida que se actualicen las asignaciones de la [plannerTask](plannertask.md).

Ejemplo:

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerOrderHintsByAssignee"
}-->

```json
{
  "ca2a1df2-e36b-4987-9f6b-0ea462f4eb47": "String",
  "4e98f8f1-bb03-4015-b8e0-19bb370949d8": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerOrderHintsByAssignee resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->