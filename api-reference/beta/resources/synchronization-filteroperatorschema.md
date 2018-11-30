---
title: tipo de recurso filterOperatorSchema
description: Describe un operador que se puede usar en un filtro.
ms.openlocfilehash: 1a4e21aea2b65073a00c9797065f6788a66e2334
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084371"
---
# <a name="filteroperatorschema-resource-type"></a>tipo de recurso filterOperatorSchema

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Describe un operador que se puede usar en un [filtro](synchronization-filter.md).

## <a name="properties"></a>Propiedades

| Propiedad                   | Tipo                      | Descripción    |
|:---------------------------|:--------------------------|:---------------|
|aridad                       |String          |Aridad del operador. Los valores posibles son: `Binary` y `Unary`. El valor predeterminado es `Binary`.|
|multivaluedComparisonType   |scopeOperatorMultiValuedComparisonType          |Los valores posibles son: `All` y `Any`. Se aplica sólo a los atributos de múltiples valores. `All`significa que todos los valores deben satisfacer la condición. `Any`significa que tiene al menos un valor satisfacer la condición. El valor predeterminado es `All`.|
|name                        |String                     |Nombre del operador. |
|supportedAttributeTypes     |Colección String         |Tipos admitidos por el operador de atributo. Los valores posibles son: `Boolean`, `Binary`, `Reference`, `Integer` y `String`.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.filterOperatorSchema"
}-->

```json
{
  "arity": "String",
  "multivaluedComparisonType": "String",
  "name": "String",
  "supportedAttributeTypes": ["String"]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "filterOperatorSchema resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->