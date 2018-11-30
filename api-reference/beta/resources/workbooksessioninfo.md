---
title: Tipo de recurso workbookSessionInfo
description: Proporciona información sobre la sesión del libro.
ms.openlocfilehash: c04afe17c10edd8b136465d6d7ae3dbedb6307ed
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086496"
---
# <a name="workbooksessioninfo-resource-type"></a>Tipo de recurso workbookSessionInfo

Proporciona información sobre la sesión del libro.


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [  ],
  "@odata.type": "microsoft.graph.workbookSessionInfo"
}-->

```json
{
  "id": "string",
  "persistChanges": true
}
```

## <a name="properties"></a>Propiedades

| Propiedad | Tipo  | Descripción                               |
|:---------|:------|:------------------------------------------|
| id  | string | Identificador de la sesión del libro. |
| persistChanges | string |  `true` para la sesión persistente. `false` para la sesión no persistente (modo de visualización) |

