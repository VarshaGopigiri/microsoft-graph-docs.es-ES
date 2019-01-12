---
title: Tipo de recurso workbookSessionInfo
description: Proporciona información sobre la sesión del libro.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: a2975fdf58d0f1d3a72f1f76853125d0a98bb485
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27962453"
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

