---
title: Tipo de recurso plannerOrderHintsByAssignee
description: El **plannerOrderHintsByAssignee** es un recurso que contiene sugerencias de ordenación para las personas asignadas en un recurso de plannerTask, para indicar el orden de la tarea en asignado a la vista del panel de tareas de.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: f678317d4ace4a86c4606668277c17c0bc547c8d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27925192"
---
# <a name="plannerorderhintsbyassignee-resource-type"></a><span data-ttu-id="36d9a-103">Tipo de recurso plannerOrderHintsByAssignee</span><span class="sxs-lookup"><span data-stu-id="36d9a-103">plannerOrderHintsByAssignee resource type</span></span>

> <span data-ttu-id="36d9a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="36d9a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="36d9a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="36d9a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="36d9a-p102">El recurso **plannerOrderHintsByAssignee** es un recurso que contiene [sugerencias de orden](planner-order-hint-format.md) para las personas asignadas en un recurso [plannerTask](plannertask.md), para indicar el orden de la tarea en la vista Asignado a del panel de tareas. Este tipo es un tipo abierto. Las propiedades son los identificadores de los usuarios asignados a la tarea, mientras que los valores son sugerencias de orden.</span><span class="sxs-lookup"><span data-stu-id="36d9a-p102">The **plannerOrderHintsByAssignee** is a resource that contains [ordering hints](planner-order-hint-format.md) for assignees in a [plannerTask](plannertask.md) resource, to indicate the order of the task in Assigned To view of the Task Board. This type is an open type. The properties are the ids of users assigned to the task, and the values are order hints.</span></span>

## <a name="properties"></a><span data-ttu-id="36d9a-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="36d9a-109">Properties</span></span>
<span data-ttu-id="36d9a-p103">El cliente puede definir las propiedades de un tipo abierto. En este caso, el cliente debe proporcionar los identificadores de los usuarios asignados a la tarea como nombres de propiedad, así como una [sugerencia de orden](planner-order-hint-format.md) válida como valor. Las propiedades no se pueden quitar de este tipo. El servicio quitará automáticamente los valores a medida que se actualicen las asignaciones de la [plannerTask](plannertask.md).</span><span class="sxs-lookup"><span data-stu-id="36d9a-p103">Properties of an Open Type can be defined by the client. In this case, the client must provide ids of users assigned to the task as property names, and a valid [order hint](planner-order-hint-format.md) as the value. Properties cannot be removed from this type. The service will automatically remove values as the assignments on the containing [plannerTask](plannertask.md) are updated.</span></span>

<span data-ttu-id="36d9a-114">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="36d9a-114">Example:</span></span>

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
