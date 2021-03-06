---
title: Tipo de recurso ChartSeries
description: Representa una serie de un gráfico.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: b9a857f127848f1ed0da8de673902527e3858ffe
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27970391"
---
# <a name="chartseries-resource-type"></a>Tipo de recurso ChartSeries

Representa una serie de un gráfico.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get ChartSeries](../api/chartseries-get.md) | [WorkbookChartSeries](chartseries.md) |Lee las propiedades y relaciones del objeto chartSeries.|
|[Create ChartPoints](../api/chartseries-post-points.md) |[ChartPoints](chartpoint.md)| Crea un nuevo ChartPoints publicándolo en la colección points.|
|[List points](../api/chartseries-list-points.md) |Colección [ChartPoints](chartpoint.md)| Obtiene la colección de objetos ChartPoints.|
|[Update](../api/chartseries-update.md) | [WorkbookChartSeries](chartseries.md) |Actualiza el objeto ChartSeries. |
|[List](../api/chartseries-list.md) | Colección de [WorkbookChartSeries](chartseries.md) |Obtiene la colección de objetos chartSeries. |
|[ItemAt](../api/chartseriescollection-itemat.md)|[WorkbookChartSeries](chartseries.md)|Recupera una serie en función de su posición en la colección.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|name|string|Representa el nombre de una serie de un gráfico.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|format|[WorkbookChartSeriesFormat](chartseriesformat.md)|Representa el formato de una serie del gráfico, que incluye el formato de relleno y de línea. Solo lectura.|
|points|Colección de [WorkbookChartPoint](chartpoint.md)|Representa una colección de todos los puntos de la serie. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookChartSeries"
}-->

```json
{
  "name": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartSeries resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
