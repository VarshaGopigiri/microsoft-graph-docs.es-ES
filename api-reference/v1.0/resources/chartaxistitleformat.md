---
title: Tipo de recurso ChartAxisTitleFormat
description: Representa el formato de título del eje del gráfico.
ms.openlocfilehash: 417c594096ae19c0a223eaeaa543827f91306e8c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031215"
---
# <a name="chartaxistitleformat-resource-type"></a>Tipo de recurso ChartAxisTitleFormat

Representa el formato de título del eje del gráfico.


## <a name="methods"></a>Métodos
Ninguno

## <a name="properties"></a>Propiedades
Ninguno

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|font|[WorkbookChartFont](chartfont.md)|Representa los atributos de fuente (por ejemplo, nombre de fuente, tamaño de fuente, color, etc.) de un objeto de título del eje del gráfico. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartAxisTitleFormat"
}-->

```json
{
  "font": {"@odata.type": "microsoft.graph.workbookChartFont"}
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartAxisTitleFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->