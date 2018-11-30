---
title: tipo de recurso targetResourcePolicy
description: 'Indica la directiva que se ven afectada por la actividad de auditoría. Deriva el recurso targetResource.   '
ms.openlocfilehash: 20486c535d0df4b3745f5cfc3414b320a9374075
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088424"
---
# <a name="targetresourcepolicy-resource-type"></a>tipo de recurso targetResourcePolicy
Indica la directiva que se ven afectada por la actividad de auditoría. Deriva el recurso [targetResource](targetresource.md) .   



## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|policyType|String|Indica el nombre de directiva que ha cambiado o se ha diseñado para cambiar|

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