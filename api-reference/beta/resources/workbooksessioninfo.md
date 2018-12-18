---
title: Tipo de recurso workbookSessionInfo
description: Proporciona información sobre la sesión del libro.
author: lumine2008
ms.openlocfilehash: 5a86fd4dfd653f16445eeccad8478db56db0ac5f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27316845"
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

