---
title: Tipo de recurso plannerUser
description: El recurso **plannerUser** proporcionan acceso a los recursos de organizador para un usuario. No contiene todas las propiedades utilizables.
ms.openlocfilehash: 777886a61d702198ec03ea844fb9fced761047ba
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030688"
---
# <a name="planneruser-resource-type"></a>Tipo de recurso plannerUser

El recurso **plannerUser** proporciona acceso a los recursos Planner de un [usuario](user.md). No contiene ninguna propiedad utilizable.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Enumerar planes](../api/planneruser-list-plans.md) |Colección [plannerPlan](plannerplan.md)| Obtenga una colección de objetos **plannerPlan**.|
|[Enumerar tareas](../api/planneruser-list-tasks.md) |Colección [plannerTask](plannertask.md)| Obtenga una colección de objetos **plannerTask**.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|String| Solo lectura. Identificador del planenrUser|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|plans|Colección [plannerPlan](plannerplan.md)| Solo lectura. Admite valores NULL. Devuelve las [plannerTasks](plannertask.md) asignadas al usuario.|
|tasks|Colección [plannerTask](plannertask.md)| Solo lectura. Admite valores NULL. Devuelve los [plannerPlans](plannerplan.md) compartidos con el usuario.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerUser"
}-->

```json
{
  "id": "String (identifier)"
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