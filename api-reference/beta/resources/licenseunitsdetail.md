---
title: Tipo de recurso licenseUnitsDetail
description: La propiedad **prepaidUnits** de la entidad subscribedSku es de tipo **licenseUnitsDetail**.
ms.openlocfilehash: 5f3d62c39248739746923195945efbc3322d5686
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083208"
---
# <a name="licenseunitsdetail-resource-type"></a>Tipo de recurso licenseUnitsDetail

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

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
