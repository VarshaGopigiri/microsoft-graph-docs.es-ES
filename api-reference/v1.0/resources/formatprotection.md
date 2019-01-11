---
title: Tipo de recurso FormatProtection
description: Representa la protección de formato de un objeto range.
localization_priority: Normal
ms.openlocfilehash: e4c32c8be8f6ef3aeaaf763ee88998bcbe235503
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876779"
---
# <a name="formatprotection-resource-type"></a>Tipo de recurso FormatProtection

Representa la protección de formato de un objeto range.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get FormatProtection](../api/formatprotection-get.md) | [FormatProtection](formatprotection.md) |Lee las propiedades y relaciones del objeto formatProtection.|
|[Update](../api/formatprotection-update.md) | [FormatProtection](formatprotection.md)  |Actualiza el objeto FormatProtection. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|formulaHidden|boolean|Indica si Excel oculta la fórmula de las celdas del rango. Un valor null indica que el rango no tiene una configuración de fórmula oculta uniforme.|
|locked|boolean|Indica si Excel bloquea las celdas del objeto. Un valor nulo indica que todo el rango no tiene una configuración de bloqueo uniforme.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookFormatProtection"
}-->

```json
{
  "formulaHidden": true,
  "locked": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "FormatProtection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
