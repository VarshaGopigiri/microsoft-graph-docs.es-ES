---
title: tipo de recurso chatInfo
description: Información acerca de un mensaje en Microsoft Teams.
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: c2cc0dd288abdab7852017600c4c55b9a40b0aa7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27852944"
---
# <a name="chatinfo-resource-type"></a>tipo de recurso chatInfo

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Información acerca de un mensaje en Microsoft Teams.

## <a name="properties"></a>Propiedades

| Propiedad            | Tipo    | Description|
|:--------------------|:--------|:-----------|
| messageId           | Cadena  | El identificador único para un mensaje en un canal de Microsoft Teams. |
| replyChainMessageId | Cadena  | El identificador del mensaje de respuesta. |
| threadId            | Cadena  | El identificador único para un subproceso en Microsoft Teams. |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chatInfo"
}-->
```json
{
  "messageId": "String",
  "replyChainMessageId": "String",
  "threadId": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "chatInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
