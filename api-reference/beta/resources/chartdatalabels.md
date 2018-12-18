---
title: Tipo de recurso ChartDataLabels
description: Representa una colección de todas las etiquetas de datos en un punto del gráfico.
author: lumine2008
ms.openlocfilehash: ef1880fcbf1f74f99f6b323c06b8fd35812f340a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27352181"
---
# <a name="chartdatalabels-resource-type"></a>Tipo de recurso ChartDataLabels

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa una colección de todas las etiquetas de datos en un punto del gráfico.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get ChartDataLabels](../api/chartdatalabels-get.md) | [ChartDataLabels](chartdatalabels.md) |Lee las propiedades y relaciones del objeto chartDataLabels.|
|[Actualizar](../api/chartdatalabels-update.md) | [ChartDataLabels](chartdatalabels.md) |Actualiza el objeto ChartDataLabels. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|position|string|Valor DataLabelPosition que representa la posición de la etiqueta de datos. Valores posibles: `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit`, `Callout`.|
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
|format|[ChartDataLabelFormat](chartdatalabelformat.md)|Representa el formato de las etiquetas de datos del gráfico, que incluye el formato de relleno y de fuente. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chartDataLabels"
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