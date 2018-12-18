---
title: Tipo de recurso ChartSeries
description: Representa una serie de un gráfico.
author: lumine2008
ms.openlocfilehash: 443b6b3dfea54b59ff92babc2776d9624bd28b20
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27325287"
---
# <a name="chartseries-resource-type"></a>Tipo de recurso ChartSeries

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa una serie de un gráfico.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get ChartSeries](../api/chartseries-get.md) | [ChartSeries](chartseries.md) |Lee las propiedades y relaciones del objeto chartSeries.|
|[Create ChartPoints](../api/chartseries-post-points.md) |[ChartPoints](chartpoint.md)| Crea un nuevo ChartPoints publicándolo en la colección points.|
|[List points](../api/chartseries-list-points.md) |Colección [ChartPoints](chartpoint.md)| Obtiene la colección de objetos ChartPoints.|
|[Actualizar](../api/chartseries-update.md) | [ChartSeries](chartseries.md) |Actualiza el objeto ChartSeries. |
|[List](../api/chartseries-list.md) | Colección [ChartSeries](chartseries.md) |Obtiene la colección de objetos chartSeries. |
|[Itemat](../api/chartseriescollection-itemat.md)|[ChartSeries](chartseries.md)|Recupera una serie en función de su posición en la colección.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|name|string|Representa el nombre de una serie de un gráfico.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|format|[ChartSeriesFormat](chartseriesformat.md)|Representa el formato de una serie del gráfico, que incluye el formato de relleno y de línea. Solo lectura.|
|points|Colección [ChartPoints](chartpoint.md)|Representa una colección de todos los puntos de la serie. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chartSeries"
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