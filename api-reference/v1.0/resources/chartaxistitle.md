---
title: Tipo de recurso ChartAxisTitle
description: Representa el título del eje de un gráfico.
author: lumine2008
ms.openlocfilehash: 785caa4d48cf32c5892d05238b4137691fd0f5c7
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27317265"
---
# <a name="chartaxistitle-resource-type"></a>Tipo de recurso ChartAxisTitle

Representa el título del eje de un gráfico.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get ChartAxisTitle](../api/chartaxistitle-get.md) | [WorkbookChartAxisTitle](chartaxistitle.md) |Lee las propiedades y relaciones del objeto chartAxisTitle.|
|[Actualizar](../api/chartaxistitle-update.md) | [WorkbookChartAxisTitle](chartaxistitle.md)    |Actualiza el objeto ChartAxisTitle. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|text|string|Representa el título del eje.|
|visible|boolean|Valor booleano que especifica la visibilidad del título de un eje.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|format|[WorkbookChartAxisTitleFormat](chartaxistitleformat.md)|Representa el formato del título del eje del gráfico. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [],
  "@odata.type": "microsoft.graph.workbookChartAxisTitle"
}-->

```json
{
  "text": "string",
  "visible": true,
  "format": {"@odata.type":"microsoft.graph.workbookChartAxisTitleFormat"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartAxisTitle resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->