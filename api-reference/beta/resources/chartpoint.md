---
title: Tipo de recurso ChartPoint
description: Representa un punto de una serie de un gráfico.
ms.openlocfilehash: 3d1bcc26fdc78bd7b844c870d40346a5f1f0496f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087852"
---
# <a name="chartpoint-resource-type"></a>Tipo de recurso ChartPoint

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa un punto de una serie de un gráfico.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get ChartPoint](../api/chartpoint-get.md) | [ChartPoint](chartpoint.md) |Lee las propiedades y relaciones del objeto chartPoint.|
|[List](../api/chartpoint-list.md) | Colección [ChartPoint](chartpoint.md) |Obtiene la colección de objetos chartPoint. |
|[Itemat](../api/chartpointscollection-itemat.md)|[ChartPoint](chartpoint.md)|Recupera un punto en función de su posición dentro de la serie.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|valor|object|Devuelve el valor de un punto del gráfico. Solo lectura.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|format|[ChartPointFormat](chartpointformat.md)|Encapsula las propiedades de formato del punto del gráfico. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chartPoint"
}-->

```json
{
  "value": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartPoint resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->