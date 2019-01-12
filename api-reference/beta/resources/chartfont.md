---
title: Tipo de recurso ChartFont
description: Este objeto representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) de un objeto de gráfico.
localization_priority: Normal
author: lumine2008
ms.prod: excel
ms.openlocfilehash: 4187d2837835520864ec3a1ef5c47b578b3d3da4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27920950"
---
# <a name="chartfont-resource-type"></a>Tipo de recurso ChartFont

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Este objeto representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) de un objeto de gráfico.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get ChartFont](../api/chartfont-get.md) | [ChartFont](chartfont.md) |Lee las propiedades y relaciones del objeto chartFont.|
|[Update](../api/chartfont-update.md) | [ChartFont](chartfont.md)   |Actualiza el objeto ChartFont. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|bold|boolean|Representa el estado de negrita de la fuente.|
|color|string|Representación del código de color HTML del color del texto. Por ejemplo, #FF0000 representa el rojo.|
|italic|boolean|Representa el estado de cursiva de la fuente.|
|name|string|Nombre de fuente (por ejemplo, "Calibri")|
|Tamaño|Double|Tamaño de la fuente (por ejemplo, 11).|
|underline|string|Tipo de subrayado aplicado a la fuente. Valores posibles: `None`, `Single`.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chartFont"
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
  "description": "ChartFont resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
