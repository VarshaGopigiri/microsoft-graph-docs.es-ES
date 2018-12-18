---
title: Tipo de recurso ChartLegend
description: Representa la leyenda de un gráfico.
author: lumine2008
ms.openlocfilehash: 27dc0ea751cff47adaa077f824f619630341cdc0
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27326092"
---
# <a name="chartlegend-resource-type"></a>Tipo de recurso ChartLegend

Representa la leyenda de un gráfico.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get ChartLegend](../api/chartlegend-get.md) | [WorkbookChartLegend](chartlegend.md) |Lee las propiedades y relaciones del objeto chartLegend.|
|[Actualizar](../api/chartlegend-update.md) | [WorkbookChartLegend](chartlegend.md) |Actualiza el objeto ChartLegend. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|overlay|boolean|Valor booleano que indica si la leyenda del gráfico debe superponerse al cuerpo principal del gráfico.|
|position|string|Representa la posición de la leyenda del gráfico. Los valores posibles son: `Top`, `Bottom`, `Left`, `Right`, `Corner`, `Custom`.|
|visible|boolean|Valor booleano que representa la visibilidad de un objeto ChartLegend.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|format|[WorkbookChartLegendFormat](chartlegendformat.md)|Representa el formato de una leyenda del gráfico, que incluye el formato de relleno y de fuente. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookChartLegend"
}-->

```json
{
  "overlay": true,
  "position": "string",
  "visible": true,
  "format": {"@odata.type":"microsoft.graph.workbookChartLegendFormat"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartLegend resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->