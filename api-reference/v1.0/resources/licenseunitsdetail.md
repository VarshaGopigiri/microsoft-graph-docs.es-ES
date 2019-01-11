---
title: Tipo de recurso licenseUnitsDetail
description: La propiedad **prepaidUnits** de la entidad subscribedSku es de tipo **licenseUnitsDetail**.
localization_priority: Normal
ms.openlocfilehash: 8c2a4e995c7e1afa63b7f9daea6b61cbaf974958
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27810699"
---
# <a name="licenseunitsdetail-resource-type"></a>Tipo de recurso licenseUnitsDetail

La propiedad **prepaidUnits** de la entidad [subscribedSku](subscribedsku.md) es de tipo **licenseUnitsDetail**.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:-------------|:-----|:----------|
|enabled|Int32| El número de unidades habilitadas. |
|suspended|Int32| El número de unidades suspendidas. |
|warning|Int32| El número de unidades que se encuentran en estado de advertencia. |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.licenseUnitsDetail"
}-->

```json
{
  "enabled": 1024,
  "suspended": 1024,
  "warning": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "licenseUnitsDetail resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
