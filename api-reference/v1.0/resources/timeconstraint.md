---
title: Tipo de recurso timeConstraint
description: Restringe las sugerencias de hora de reunión a ciertas horas y días de la semana según la naturaleza de la actividad especificada y las franjas horarias disponibles.
localization_priority: Normal
ms.openlocfilehash: b6e239abbd0d9f7b4f83df4a60625a2f88131476
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27815095"
---
# <a name="timeconstraint-resource-type"></a>Tipo de recurso timeConstraint

Restringe las sugerencias de hora de reunión a ciertas horas y días de la semana según la naturaleza de la actividad especificada y las franjas horarias disponibles.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.timeConstraint"
}-->

```json
{
  "activityDomain": "String",
  "timeslots": [{"@odata.type": "microsoft.graph.timeSlot"}]
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|activityDomain|activityDomain|La naturaleza de la actividad, de forma opcional. Los valores posibles son: `work`, `personal`, `unrestricted`, o `unknown`.|
|ranuras de intervalo de tiempo|Colección[timeSlot](timeslot.md)|Matriz de periodos de tiempo.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "timeConstraint resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
