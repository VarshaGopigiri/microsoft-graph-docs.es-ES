---
title: tipo de recurso targetResourceGroup
description: 'Indica el tipo de grupo que se ven afectado debido a la actividad de auditoría. Incluye los valores como los grupos unificados frente a Azure AD '
localization_priority: Normal
ms.openlocfilehash: 2cc7e0adb1a93394b64375d05dfb6a6e349bac55
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27851187"
---
# <a name="targetresourcegroup-resource-type"></a>tipo de recurso targetResourceGroup
Indica el tipo de grupo que se ven afectado debido a la actividad de auditoría. Incluye los valores como los grupos unificados frente a Azure AD 



## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|groupType|Cadena| Los valores posibles son: `unifiedGroups`, `azureAD` y `unknownFutureValue`.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.targetResourceGroup"
}-->

```json
{
  "groupType": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "targetResourceGroup resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
