---
title: tipo de recurso targetResourcePolicy
description: 'Indica la directiva que se ven afectada por la actividad de auditoría. Deriva el recurso targetResource.   '
localization_priority: Normal
ms.openlocfilehash: 355e6ac11741a2aa7aeb780bdac4b7be373092af
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27813142"
---
# <a name="targetresourcepolicy-resource-type"></a>tipo de recurso targetResourcePolicy
Indica la directiva que se ven afectada por la actividad de auditoría. Deriva el recurso [targetResource](targetresource.md) .   



## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|policyType|Cadena|Indica el nombre de directiva que ha cambiado o se ha diseñado para cambiar|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.targetResourcePolicy"
}-->

```json
{
  "policyType": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "targetResourcePolicy resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
