---
title: Tipo de recurso workbookSessionInfo
description: Proporciona información sobre la sesión del libro.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 900ebdcefbdfa83e7b72b1c926a441f1c497626a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27826932"
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
| persistChanges | boolean |  `true` para la sesión persistente. `false` para la sesión no persistente (modo de visualización) |

