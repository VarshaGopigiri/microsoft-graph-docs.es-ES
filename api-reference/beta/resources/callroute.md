---
title: tipo de recurso callRoute
description: El tipo de callRoute.
ms.openlocfilehash: d2a85d34fe755c6e725abc9a1308a3837f0acf3e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085375"
---
# <a name="callroute-resource-type"></a>tipo de recurso callRoute

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El tipo de callRoute.

## <a name="properties"></a>Propiedades

| Propiedad            | Tipo                          | Descripción                                                  |
| :------------------ | :---------------------------- | :----------------------------------------------------------- |
| final               | [identitySet](identityset.md) | La identidad que se ha resuelta para en la llamada.               |
| Texto original en            | [identitySet](identityset.md) | La identidad que se usó originalmente en la llamada.           |
| routingType         | String                        | Los valores posibles son: `forwarded`, `lookup` y `selfFork`.  |

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
