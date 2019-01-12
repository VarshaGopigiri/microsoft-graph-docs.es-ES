---
title: Tipo de recurso ChartDataLabels
description: Representa una colección de todas las etiquetas de datos en un punto del gráfico.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 48d6cb0d35e82fc0117a24aad1c5e171bc869870
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27961422"
---
# <a name="chartdatalabels-resource-type"></a>Tipo de recurso ChartDataLabels

Representa una colección de todas las etiquetas de datos en un punto del gráfico.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get ChartDataLabels](../api/chartdatalabels-get.md) | [WorkbookChartDataLabels](chartdatalabels.md) |Lee las propiedades y relaciones del objeto chartDataLabels.|
|[Update](../api/chartdatalabels-update.md) | [WorkbookChartDataLabels](chartdatalabels.md) |Actualiza el objeto ChartDataLabels. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|position|string|Valor de DataLabelPosition que representa la posición de la etiqueta de datos. Los valores posibles son: `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit`, `Callout`.|
|separator|string|Cadena que representa el separador empleado para las etiquetas de datos de un gráfico.|
|showBubbleSize|boolean|Valor booleano que representa si el tamaño de la burbuja de la etiqueta de datos es visible o no.|
|showCategoryName|boolean|Valor booleano que representa si el nombre de categoría de la etiqueta de datos es visible o no.|
|showLegendKey|boolean|Valor booleano que representa si la clave de leyenda de la etiqueta de datos es visible o no.|
|showPercentage|boolean|Valor booleano que representa si el porcentaje de la etiqueta de datos es visible o no.|
|showSeriesName|boolean|Valor booleano que representa si el nombre de serie de la etiqueta de datos es visible o no.|
|showValue|boolean|Valor booleano que representa si el valor de la etiqueta de datos es visible o no.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|format|[WorkbookChartDataLabelFormat](chartdatalabelformat.md)|Representa el formato de las etiquetas de datos del gráfico, que incluye el formato de relleno y de fuente. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [],
  "@odata.type": "microsoft.graph.workbookChartDataLabels"
}-->

```json
{
  "position": "string",
  "separator": "string",
  "showBubbleSize": true,
  "showCategoryName": true,
  "showLegendKey": true,
  "showPercentage": true,
  "showSeriesName": true,
  "showValue": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartDataLabels resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
