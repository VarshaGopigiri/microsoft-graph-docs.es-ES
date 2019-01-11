---
title: tipo de recurso stringKeyAttributeMappingSourceValuePair
description: Representa un par de clave y valor donde la clave es una cadena y el valor es attributeMappingSource.
localization_priority: Normal
ms.openlocfilehash: 24695cc64fd3c240d5416a7b37e9a5d373e5a88a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805092"
---
# <a name="stringkeyattributemappingsourcevaluepair-resource-type"></a>tipo de recurso stringKeyAttributeMappingSourceValuePair

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa un par de clave y valor donde la clave es una cadena y el valor es [attributeMappingSource](synchronization-attributemappingsource.md).

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|Key|Cadena|Nombre del parámetro.|
|valor|[attributeMappingSource](synchronization-attributemappingsource.md)|El valor del parámetro.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.stringKeyAttributeMappingSourceValuePair"
}-->

```json
{
  "key": "String",
  "value": {"@odata.type": "microsoft.graph.attributeMappingSource"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "stringKeyAttributeMappingSourceValuePair resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
