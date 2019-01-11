---
title: tipo de recurso parseExpressionResponse
description: 'Representa la respuesta de la [synchronizationSchema: parseExpression](../api/synchronization_synchronizationschema_parseexpression.md) acción.'
localization_priority: Normal
ms.openlocfilehash: 550a46b0c27c2ca8d2d4c01baa975d8a204546f2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27832952"
---
# <a name="parseexpressionresponse-resource-type"></a>tipo de recurso parseExpressionResponse

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa la respuesta de la [synchronizationSchema: parseExpression](../api/synchronization_synchronizationschema_parseexpression.md) acción.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|error|OData.Error|Detalles del error, si como resultado de la evaluación de expresiones en un error.|
|evaluationResult|Colección String|Una colección de valores generados por la evaluación de la expresión.|
|evaluationSucceeded|Booleano|`true`Si la evaluación se realizó correctamente.|
|parsedExpression|[attributeMappingSource](synchronization-attributemappingsource.md)|Un objeto [attributeMappingSource](synchronization-attributemappingsource.md) que representa la expresión analizada.|
|parsingSucceeded|Booleano|`true`Si la expresión se ha analizado correctamente.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.parseExpressionResponse"
}-->

```json
{
  "error": {"@odata.type": "microsoft.graph.publicError"},
  "evaluationResult": ["String"],
  "evaluationSucceeded": true,
  "parsedExpression": {"@odata.type": "microsoft.graph.attributeMappingSource"},
  "parsingSucceeded": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "parseExpressionResponse resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
