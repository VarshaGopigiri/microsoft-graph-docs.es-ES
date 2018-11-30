---
title: Tipo de recurso ChartGridlines
description: Representa las líneas de cuadrícula principales o secundarias del eje de un gráfico.
ms.openlocfilehash: c09580b2c669710d8aabf60e31c3c36965bfaa6a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083188"
---
# <a name="chartgridlines-resource-type"></a>Tipo de recurso ChartGridlines

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa las líneas de división principales o secundarias del eje de un gráfico.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get ChartGridlines](../api/chartgridlines-get.md) | [ChartGridlines](chartgridlines.md) |Lee las propiedades y relaciones del objeto chartGridlines.|
|[Update](../api/chartgridlines-update.md) | [ChartGridlines](chartgridlines.md)    |Actualiza el objeto ChartGridlines. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|visible|boolean|Valor booleano que representa si las líneas de cuadrícula del eje están visibles o no.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|format|[ChartGridlinesFormat](chartgridlinesformat.md)|Representa el formato de las líneas de cuadrícula del gráfico. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chartGridLines"
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