---
title: Tipo de recurso ChartTitle
description: Representa un objeto de título de gráfico de un gráfico.
author: lumine2008
ms.openlocfilehash: b3d685c68b14ebe3f49eb3dd9186838c977c1cac
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27338104"
---
# <a name="charttitle-resource-type"></a>Tipo de recurso ChartTitle

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa un objeto de título de gráfico de un gráfico.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get ChartTitle](../api/charttitle-get.md) | [ChartTitle](charttitle.md) |Lee las propiedades y relaciones del objeto chartTitle.|
|[Actualizar](../api/charttitle-update.md) | [ChartTitle](charttitle.md)    |Actualiza el objeto ChartTitle. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|overlay|boolean|Valor booleano que representa si el título del gráfico se superpondrá al gráfico o no.|
|text|string|Representa el texto del título de un gráfico.|
|visible|boolean|Valor booleano que representa la visibilidad de un objeto de título del gráfico.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|format|[ChartTitleFormat](charttitleformat.md)|Representa el formato de un título del gráfico, que incluye el formato de relleno y de fuente. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chartTitle"
}-->

```json
{
  "overlay": true,
  "text": "string",
  "visible": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartTitle resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->