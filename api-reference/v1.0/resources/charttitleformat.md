---
title: Tipo de recurso ChartTitleFormat
description: Encapsula las propiedades de formato del título del gráfico.
ms.openlocfilehash: 7e84412adb46981a0a2b8570ed28c62d36936e36
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029457"
---
# <a name="charttitleformat-resource-type"></a>Tipo de recurso ChartTitleFormat

Encapsula las propiedades de formato del título del gráfico.


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
  "@odata.type": "microsoft.graph.workbookChartTitleFormat"
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
