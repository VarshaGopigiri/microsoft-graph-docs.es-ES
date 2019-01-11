---
title: tipo de recurso callRoute
description: El tipo de callRoute.
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: e417a7e814b5a2a80da1fa9cd7a551f82e0c37db
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27815088"
---
# <a name="callroute-resource-type"></a>tipo de recurso callRoute

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El tipo de callRoute.

## <a name="properties"></a>Propiedades

| Propiedad            | Tipo                          | Description                                                  |
| :------------------ | :---------------------------- | :----------------------------------------------------------- |
| final               | [identitySet](identityset.md) | La identidad que se ha resuelta para en la llamada.               |
| Texto original en            | [identitySet](identityset.md) | La identidad que se usó originalmente en la llamada.           |
| routingType         | Cadena                        | Los valores posibles son: `forwarded`, `lookup` y `selfFork`.  |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.callRoute"
}-->
```json
{
  "final": {"@odata.type": "#microsoft.graph.identitySet"},
  "original": {"@odata.type": "#microsoft.graph.identitySet"},
  "routingType": "forwarded | lookup | selfFork"
}
```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "callRoute resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
