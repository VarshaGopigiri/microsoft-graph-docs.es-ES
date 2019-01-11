---
title: tipo de recurso filterClause
description: Representa una aserción único que debe cumplir un objeto candidato y se evalúa alguna `true` (objeto cumple la aserción) o `false` (objeto no cumplen con la aserción).
localization_priority: Normal
ms.openlocfilehash: 89807a6086f661388c8d5b1d5f82bfe973c3af39
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27833862"
---
# <a name="filterclause-resource-type"></a>tipo de recurso filterClause

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa una aserción único que debe cumplir un objeto candidato y se evalúa alguna `true` (objeto cumple la aserción) o `false` (objeto no cumplen con la aserción).

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|operatorName|Cadena|Nombre del operador que se aplicará a los operandos de origen y de destino. Debe ser uno de los operadores compatibles. Se pueden detectar los operadores compatibles.|
|sourceOperandName|Cadena|Nombre del operando de origen (el operando que se está probando). El nombre del operando de origen debe coincidir con uno de los nombres de atributo en el objeto de origen.|
|targetOperand|[filterOperand](synchronization-filteroperand.md)|Valores que se probará contra el operando de origen.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.filterClause"
}-->

```json
{
  "operatorName": "String",
  "sourceOperandName": "String",
  "targetOperand": {"@odata.type": "microsoft.graph.filterOperand"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "filterClause resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
