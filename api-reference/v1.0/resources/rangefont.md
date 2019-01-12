---
title: Tipo de recurso RangeFont
description: Este objeto representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) de un objeto.
localization_priority: Normal
author: lumine2008
ms.prod: excel
ms.openlocfilehash: 829b391d561aae63ae94972c55039acfdf4c48d7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27962300"
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
