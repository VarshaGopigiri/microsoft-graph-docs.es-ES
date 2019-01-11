---
title: Tipo de recurso timeConstraint
description: Restringe las sugerencias de hora de reunión a ciertas horas y días de la semana según la naturaleza de la actividad especificada y las franjas horarias disponibles.
localization_priority: Normal
ms.openlocfilehash: 6e3cc56f1495eae60bb84c458caa25c79557e033
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27832910"
---
# <a name="timeconstraint-resource-type"></a>Tipo de recurso timeConstraint

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Restringe las sugerencias de hora de reunión a ciertas horas y días de la semana según la naturaleza de la actividad especificada y las franjas horarias disponibles.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.timeconstraint"
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
|activityDomain|Cadena|La naturaleza de la actividad, opcional. Los valores posibles son: `work`, `personal`, `unrestricted` o `unknown`.|
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
