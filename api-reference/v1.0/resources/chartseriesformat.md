---
title: Tipo de recurso ChartSeriesFormat
description: Encapsula las propiedades de formato de la serie del gráfico.
ms.openlocfilehash: 81b79331580c2d7edbc52f19d1c4c9cfd57db0cf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029988"
---
# <a name="chartseriesformat-resource-type"></a>Tipo de recurso ChartSeriesFormat

Encapsula las propiedades de formato de la serie del gráfico.


## <a name="methods"></a>Métodos
Ninguno

## <a name="properties"></a>Propiedades
Ninguno

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|fill|[WorkbookChartFill](chartfill.md)|Representa el formato de relleno de una serie del gráfico, que incluye información del formato de fondo. Solo lectura.|
|line|[WorkbookChartLineFormat](chartlineformat.md)|Representa el formato de línea. Solo lectura.|


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartSeriesFormat"
}-->

```json
{
  "fill": {"@odata.type": "microsoft.graph.workbookChartFill"},
  "line": {"@odata.type": "microsoft.graph.workbookChartLineFormat"}
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartSeriesFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->