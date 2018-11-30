---
title: tipo de recurso targetResourceGroup
description: 'Indica el tipo de grupo que se ven afectado debido a la actividad de auditoría. Incluye los valores como los grupos unificados frente a Azure AD '
ms.openlocfilehash: 3427f2401a0e93767f0c563842be323f66d9f21b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086424"
---
# <a name="targetresourcegroup-resource-type"></a>tipo de recurso targetResourceGroup
Indica el tipo de grupo que se ven afectado debido a la actividad de auditoría. Incluye los valores como los grupos unificados frente a Azure AD 



## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|groupType|String| Los valores posibles son: `unifiedGroups`, `azureAD` y `unknownFutureValue`.|

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