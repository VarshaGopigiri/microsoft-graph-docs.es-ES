---
title: Tipo de recurso ChartLineFormat
description: Encapsula las opciones de formato para los elementos de línea.
ms.openlocfilehash: 6e43818bc55972585deff5aa2add1d513f031360
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029427"
---
# <a name="chartlineformat-resource-type"></a>Tipo de recurso ChartLineFormat

Encapsula las opciones de formato para los elementos de línea.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get ChartLineFormat](../api/chartlineformat-get.md) | [WorkbookChartLineFormat](chartlineformat.md) |Lee las propiedades y relaciones del objeto chartLineFormat.|
|[Update](../api/chartlineformat-update.md) | [WorkbookChartLineFormat](chartlineformat.md) |Actualiza el objeto ChartLineFormat. |
|[Clear](../api/chartlineformat-clear.md)|None|Borra el formato de línea de un elemento de gráfico.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|color|string|Código de color HTML que representa el color de las líneas del gráfico.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [],
  "@odata.type": "microsoft.graph.workbookChartLineFormat"
}-->

```json
{
  "color": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartLineFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->