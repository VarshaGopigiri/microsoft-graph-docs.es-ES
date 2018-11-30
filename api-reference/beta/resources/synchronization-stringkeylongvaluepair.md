---
title: tipo de recurso stringKeyLongValuePair
description: Representa un par de clave y valor donde la clave es una cadena y el valor es un valor Int64.
ms.openlocfilehash: 0ceafbc4ab683469e616e068c0abc00804578908
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089756"
---
# <a name="stringkeylongvaluepair-resource-type"></a>tipo de recurso stringKeyLongValuePair

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa un par de clave y valor donde la clave es una cadena y el valor es un valor Int64.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|Key|String|Clave.|
|valor|Int64|Valor.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.stringKeyLongValuePair"
}-->

```json
{
  "key": "String",
  "value": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "stringKeyLongValuePair resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->