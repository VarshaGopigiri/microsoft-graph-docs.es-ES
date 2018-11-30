---
title: Tipo de recurso RangeFont
description: Este objeto representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) de un objeto.
ms.openlocfilehash: bafb7c052458c7b3f4001d7e999acc14c7aaabee
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031529"
---
# <a name="rangefont-resource-type"></a>Tipo de recurso RangeFont

Este objeto representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) de un objeto.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get RangeFont](../api/rangefont-get.md) | [WorkbookRangeFont](rangefont.md) |Lee las propiedades y relaciones del objeto rangeFont.|
|[Update](../api/rangefont-update.md) | [WorkbookRangeFont](rangefont.md)   |Actualiza el objeto RangeFont. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|bold|boolean|Representa el estado de negrita de la fuente.|
|color|string|Representación del código de color HTML del color del texto. Por ejemplo, #FF0000 representa el rojo.|
|italic|boolean|Representa el estado de cursiva de la fuente.|
|name|string|Nombre de fuente (por ejemplo, "Calibri")|
|Tamaño|Double|Tamaño de fuente|
|underline|string|Tipo de subrayado aplicado a la fuente. Los valores posibles son: `None`, `Single`, `Double`, `SingleAccountant`, `DoubleAccountant`.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookRangeFont"
}-->

```json
{
  "bold": true,
  "color": "string",
  "italic": true,
  "name": "string",
  "size": 1024,
  "underline": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "RangeFont resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->