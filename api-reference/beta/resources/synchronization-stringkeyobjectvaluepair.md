---
title: tipo de recurso stringKeyObjectValuePair
description: Representa un par de clave y valor donde la clave es una cadena y el valor es un objeto JSON arbitrario. Esto es un tipo abierto de OData que espera tener una propiedad denominada `value` es un objeto JSON válido.
localization_priority: Normal
ms.openlocfilehash: 8545a4ef5a4931d3b886c95b4f39218bc418f53d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27831454"
---
# <a name="stringkeyobjectvaluepair-resource-type"></a>tipo de recurso stringKeyObjectValuePair

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa un par de clave y valor donde la clave es una cadena y el valor es un objeto JSON arbitrario. Esto es un tipo abierto de OData que espera tener una propiedad denominada `value` es un objeto JSON válido.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|Key|Cadena|Clave.|
|valor|Cualquiera|Objeto JSON arbitrario.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.stringKeyObjectValuePair"
}-->

```json
{
  "key": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "stringKeyObjectValuePair resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
