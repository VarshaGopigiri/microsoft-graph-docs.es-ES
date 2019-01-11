---
title: Tipo de recurso plannerUser
description: 'El recurso **plannerUser** proporciona acceso a los recursos del organizador para un usuario. '
localization_priority: Normal
ms.openlocfilehash: 709b259c88d8fe0f02defaa57e77727a7b967cfd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27820807"
---
# <a name="planneruser-resource-type"></a>Tipo de recurso plannerUser

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **plannerUser** proporciona acceso a los recursos de organizador para un [usuario](user.md). 


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Enumerar tareas](../api/planneruser-list-tasks.md) |Colección [plannerTask](plannertask.md)| Obtenga el [plannerTasks](plannertask.md) asignados al usuario.|
|[Lista favoritePlans](../api/planneruser-list-favoriteplans.md) |Colección [plannerPlan](plannerplan.md)| Obtenga el [plannerPlans](plannerplan.md) marcados como favoritas por el usuario.|
|[Lista recentPlans](../api/planneruser-list-recentplans.md) |Colección [plannerPlan](plannerplan.md)| Obtenga el [plannerPlans](plannerplan.md) visto recientemente por el usuario.|
|[Update](../api/planneruser-update.md) | [plannerUser](planneruser.md)| Actualizar un objeto **plannerUser** . |


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|Cadena| Solo lectura. Identificador de la plannerUser|
|favoritePlanReferences|[plannerFavoritePlanReferenceCollection](plannerfavoriteplanreferencecollection.md)| Una colección que contiene las referencias a los planes de que el usuario ha marcado como favoritos.|
|recentPlanReferences|[plannerRecentPlanReferenceCollection](plannerrecentplanreferencecollection.md)| Una colección que contiene referencias a los planes que se han visto recientemente por el usuario en las aplicaciones que admiten los planes de recientes.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|tasks|Colección [plannerTask](plannertask.md)| Solo lectura. Admite valores NULL. Devuelve las [plannerTasks](plannertask.md) asignadas al usuario.|
|favoritePlans|Colección [plannerPlan](plannerplan.md)| Solo lectura. Admite valores NULL. Devuelve el [plannerPlans](plannerplan.md) que el usuario marcado como favoritos.|
|recentPlans|Colección [plannerPlan](plannerplan.md)| Solo lectura. Admite valores NULL. Devuelve el [plannerPlans](plannerplan.md) que se han visto recientemente por el usuario en las aplicaciones que admiten los planes de recientes. |

## <a name="json-representation"></a>Representación JSON
La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerUser"
}-->

```json
{
  "favoritePlanReferences": {"@odata.type": "microsoft.graph.plannerFavoritePlanReferenceCollection"},
  "id": "String (identifier)",
  "recentPlanReferences": {"@odata.type": "microsoft.graph.plannerRecentPlanReferenceCollection"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerUser resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
