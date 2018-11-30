---
title: Tipo de recurso plannerPlan
description: El recurso **plannerPlan** representa un plan en Office 365. Un plan de puede pertenecer a un grupo y contiene una colección de plannerTasks. También puede tener una colección de plannerBuckets. Cada objeto de plan tiene un objeto de detalles que puede contener más información acerca del plan. Para obtener más información acerca de las relaciones entre los grupos, los planes y tareas, vea organizador.
ms.openlocfilehash: 236b6cb5d35e11a30bcb4371e0563b56ac93de8f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085348"
---
# <a name="plannerplan-resource-type"></a>Tipo de recurso plannerPlan

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **plannerPlan** representa un plan en Office 365. Un plan de puede pertenecer a un [grupo](group.md) y contiene una colección de [plannerTasks](plannertask.md). También puede tener una colección de [plannerBuckets](plannerbucket.md). Cada objeto de plan tiene un objeto de [Detalles](plannerplandetails.md) que puede contener más información acerca del plan. Para obtener más información acerca de las relaciones entre los grupos, los planes y tareas, vea [Organizador](planner-overview.md).



## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener plannerPlan](../api/plannerplan-get.md) | [plannerPlan](plannerplan.md) |Leer las propiedades y las relaciones del objeto **plannerPlan**.|
|[Enumerar depósitos](../api/plannerplan-list-buckets.md) |Colección [plannerBucket](plannerbucket.md)| Obtenga una colección de objetos **plannerBucket**.|
|[Enumerar tareas](../api/plannerplan-list-tasks.md) |Colección [plannerTask](plannertask.md)| Obtenga una colección de objetos **plannerTask**.|
|[Update](../api/plannerplan-update.md) | [plannerPlan](plannerplan.md) |Actualizar el objeto **plannerPlan**. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|createdDateTime|DateTimeOffset|Solo lectura. Fecha y hora en que se creó el plan. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|id|String| Solo lectura. Identificador del plan. Es 28 caracteres de largo y entre mayúsculas y minúsculas. [Validación de formato](tasks-identifiers-disclaimer.md) se realiza en el servicio.|
|owner|String|Identificador del [grupo](group.md) que posee el plan. Un grupo válido debe existir antes de que se puede establecer en este campo. Una vez establecida, esta propiedad no se puede actualizar.|
|title|String|Obligatorio. Título del plan.|
|createdBy|[identitySet](identityset.md)|Solo lectura. El usuario que creó el plan.|
|contextos|[plannerPlanContextCollection](plannerplancontextcollection.md)| Solo lectura. Experiencias de usuario adicionales en el que se usa este plan, representado como entradas de [plannerPlanContext](plannerplancontext.md) .|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|buckets|Colección [plannerBucket](plannerbucket.md)| Solo lectura. Admite valores NULL. Colección de depósitos del plan.|
|details|[plannerPlanDetails](plannerplandetails.md)| Solo lectura. Admite valores NULL. Detalles adicionales sobre el plan.|
|tasks|Colección [plannerTask](plannertask.md)| Solo lectura. Admite valores NULL. Colección de tareas en el plan.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerPlan"
}-->

```json
{
  "contexts": {
    "48#19%3Ad128c63941b24733951ea7defd81e550%40thread%2Eskype19%3Ad128c63941b24733951ea7defd81e550%40thread%2Eskype": {
        "@odata.type": "#microsoft.graph.plannerPlanContext",
        "associationType": "Board",
        "createdDateTime": "2015-10-14T00:57:28.4698344Z",
        "displayNameSegments": [
            "Finance Team",
            "Budget Plans"
        ],
        "ownerAppId": "5e3ce6c0-2b1f-4285-8d4b-75ee78787346"
    }
  },
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "owner": "String",
  "title": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerPlan resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->