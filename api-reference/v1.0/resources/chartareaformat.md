---
title: Tipo de recurso ChartAreaFormat
description: Encapsula las propiedades de formato del área del gráfico en general.
author: lumine2008
ms.openlocfilehash: d9db44fefeff00ae6f7363126de35d4028964d14
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27310006"
---
# <a name="chartareaformat-resource-type"></a>Tipo de recurso ChartAreaFormat

Encapsula las propiedades de formato del área del gráfico en general.


## <a name="methods"></a>Métodos
Ninguno

## <a name="properties"></a>Propiedades
Ninguno

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|fill|[WorkbookChartFill](chartfill.md)|Representa el formato de relleno de un objeto, que incluye información del formato de fondo. Solo lectura.|
|font|[WorkbookChartFont](chartfont.md)|Representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) del objeto actual. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartAreaFormat"
}-->

```json
{
  "fill": {"@odata.type": "microsoft.graph.workbookChartFill"},
  "font": {"@odata.type": "microsoft.graph.workbookChartFont"}
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartAreaFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->