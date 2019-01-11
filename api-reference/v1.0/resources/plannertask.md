---
title: Tipo de recurso plannerTask
description: El recurso **plannerTask** representa un plan de Office 365. Una tarea de Planner está contenida en una plan y puede asignarse a un depósito en un plan. Cada objeto de la tarea tiene un objeto details (detalles), que puede contener más información sobre la tarea. Vea Resumen para obtener más información sobre las relaciones entre grupo, plan y tarea.
localization_priority: Priority
ms.openlocfilehash: a4c9ffc9c3bcd3e4a7b9df3348cdfe355a648a8d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27832259"
---
# <a name="plannertask-resource-type"></a>Tipo de recurso plannerTask

El recurso **plannerTask** representa un plan de Office 365. Una tarea de Planner está contenida en una [plan](plannerplan.md) y puede asignarse a un [depósito](plannerbucket.md) en un plan. Cada objeto de la tarea tiene un objeto [details](plannertaskdetails.md) (detalles), que puede contener más información sobre la tarea. Vea [Resumen](planner-overview.md) para obtener más información sobre las relaciones entre grupo, plan y tarea.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get plannerTask](../api/plannertask-get.md) | [plannerTask](plannertask.md) |Leer las propiedades y las relaciones del objeto **plannerTask**.|
|[Update](../api/plannertask-update.md) | [plannerTask](plannertask.md) |Actualizar el objeto **plannerTask**. |
|[Delete](../api/plannertask-delete.md) | Ninguno |Eliminar el objeto **plannerTask**. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|activeChecklistItemCount|Int32|Número de elementos de la lista de comprobación con el valor establecido en "false", que representan elementos incompletos.|
|appliedCategories|[plannerAppliedCategories](plannerappliedcategories.md)|Categorías a las que se ha aplicado la tarea. Consulte [las categorías aplicadas](plannerappliedcategories.md) para ver los posibles valores.|
|assigneePriority|Cadena|Sugerencia que se usa para ordenar los elementos de este tipo en una vista de lista. El formato se define tal como se describe [aquí](planner-order-hint-format.md).|
|assignments|[plannerAssignments](plannerassignments.md)|Conjunto de usuarios al que se asigna la tarea.|
|bucketId|Cadena|Identificador de cubo al que pertenece la tarea. Debe estar en el plan de que la tarea se encuentra en el cubo. Es 28 caracteres de largo y entre mayúsculas y minúsculas. [Validación de formato](planner-identifiers-disclaimer.md) se realiza en el servicio. |
|checklistItemCount|Int32|Número de elementos de lista de comprobación que están presentes en la tarea.|
|completedBy|[identitySet](identityset.md)|Identidad del usuario que ha completado la tarea.|
|completedDateTime|DateTimeOffset|Solo lectura. Fecha y hora en que `'percentComplete'` de la tarea se establece en `'100'`. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|conversationThreadId|Cadena|Id. de subproceso de la conversación en la tarea. Es el id. del objeto de subproceso de conversación creado en el grupo.|
|createdBy|[identitySet](identityset.md)|Identidad del usuario que ha creado la tarea.|
|createdDateTime|DateTimeOffset|Solo lectura. Fecha y hora en que se crea la tarea. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|dueDateTime|DateTimeOffset|Fecha y hora en que vence la tarea. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, la medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|hasDescription|Boolean|Solo lectura. El valor es `true` si el objeto de detalles de la tarea tiene una descripción que no está vacía y `false` lo contrario.|
|id|Cadena|Solo lectura. Identificador de la tarea. Es 28 caracteres de largo y entre mayúsculas y minúsculas. [Validación de formato](planner-identifiers-disclaimer.md) se realiza en el servicio.|
|orderHint|Cadena|Sugerencia que se usa para ordenar los elementos de este tipo en una vista de lista. El formato se define tal como se describe [aquí](planner-order-hint-format.md).|
|percentComplete|Int32|Porcentaje de finalización de la tarea. Si se establece en `100`, la tarea se considera finalizada. |
|planId|Cadena|Id. de plan al que pertenece la tarea.|
|previewType|plannerPreviewType|Esto establece el tipo de vista previa que se muestra en la tarea. Los valores posibles son: `automatic`, `noPreview`, `checklist`, `description`, `reference`.|
|referenceCount|Int32|Número de referencias externas que existen en la tarea.|
|startDateTime|DateTimeOffset|Fecha y hora en que comienza la tarea. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|title|Cadena|Título de la tarea.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|assignedToTaskBoardFormat|[plannerAssignedToTaskBoardTaskFormat](plannerassignedtotaskboardtaskformat.md)| Solo lectura. Admite valores NULL. Se utiliza para representar la tarea correctamente en la vista del panel de la tarea cuando se agrupan por assignedTo.|
|bucketTaskBoardFormat|[plannerBucketTaskBoardTaskFormat](plannerbuckettaskboardtaskformat.md)| Solo lectura. Admite valores NULL. Se utiliza para representar la tarea correctamente en la vista del panel de la tarea cuando se agrupan por depósito.|
|details|[plannerTaskDetails](plannertaskdetails.md)| Solo lectura. Admite valores NULL. Detalles adicionales sobre la tarea.|
|progressTaskBoardFormat|[plannerProgressTaskBoardTaskFormat](plannerprogresstaskboardtaskformat.md)| Solo lectura. Admite valores NULL. Se utiliza para representar la tarea correctamente en la vista del panel de la tarea cuando se agrupan por progreso.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerTask"
}-->

```json
{
  "activeChecklistItemCount": 1024,
  "appliedCategories": {"@odata.type": "microsoft.graph.plannerAppliedCategories"},
  "assigneePriority": "String",
  "assignments": {"@odata.type": "microsoft.graph.plannerAssignments"},
  "bucketId": "String",
  "checklistItemCount": 1024,
  "completedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "completedDateTime": "String (timestamp)",
  "conversationThreadId": "String",
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "dueDateTime": "String (timestamp)",
  "hasDescription": true,
  "id": "String (identifier)",
  "orderHint": "String",
  "percentComplete": 1024,
  "planId": "String",
  "previewType": "string",
  "referenceCount": 1024,
  "startDateTime": "String (timestamp)",
  "title": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerTask resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
