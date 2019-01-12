---
title: Tipo de recurso ChartGridlines
description: Representa las líneas de cuadrícula principales o secundarias del eje de un gráfico.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 7347ac1b7ff251b12764534df217cd883ba730b3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27956951"
---
# <a name="chartgridlines-resource-type"></a>Tipo de recurso ChartGridlines

Representa las líneas de cuadrícula principales o secundarias del eje de un gráfico.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get ChartGridlines](../api/chartgridlines-get.md) | [WorkbookChartGridlines](chartgridlines.md) |Lee las propiedades y relaciones del objeto chartGridlines.|
|[Update](../api/chartgridlines-update.md) | [WorkbookChartGridlines](chartgridlines.md)    |Actualiza el objeto ChartGridlines. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|visible|boolean|Valor booleano que representa si las líneas de cuadrícula del eje están visibles o no.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|format|[WorkbookChartGridlinesFormat](chartgridlinesformat.md)|Representa el formato de las líneas de cuadrícula del gráfico. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookChartGridlines"
}-->

```json
{
  "visible": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartGridlines resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
