---
title: Tipo de recurso ChartAxisFormat
description: Encapsula las propiedades de formato del eje del gráfico.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: a219122141da1f384279d0ff4c612f62226612c9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27821269"
---
# <a name="chartaxisformat-resource-type"></a>Tipo de recurso ChartAxisFormat

Encapsula las propiedades de formato del eje del gráfico.


## <a name="methods"></a>Métodos
Ninguno
## <a name="properties"></a>Propiedades
Ninguno

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|font|[WorkbookChartFont](chartfont.md)|Representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) de un elemento del eje del gráfico. Solo lectura.|
|line|[WorkbookChartLineFormat](chartlineformat.md)|Representa el formato de línea de gráfico. Solo lectura.|


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartAxisFormat"
}-->

```json
{
  "font": {"@odata.type": "microsoft.graph.workbookChartFont"},
  "line": {"@odata.type": "microsoft.graph.workbookChartLineFormat"}
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartAxisFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
