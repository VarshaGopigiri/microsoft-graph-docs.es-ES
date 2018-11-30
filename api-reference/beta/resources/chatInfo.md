---
title: tipo de recurso chatInfo
description: Información acerca de un mensaje en Microsoft Teams.
ms.openlocfilehash: d7e90cf2cdf5180f6483675d919b4e635a1cd5fa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083146"
---
# <a name="chatinfo-resource-type"></a>tipo de recurso chatInfo

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Información acerca de un mensaje en Microsoft Teams.

## <a name="properties"></a>Propiedades

| Propiedad            | Tipo    | Descripción|
|:--------------------|:--------|:-----------|
| messageId           | String  | El identificador único para un mensaje en un canal de Microsoft Teams. |
| replyChainMessageId | String  | El identificador del mensaje de respuesta. |
| threadId            | String  | El identificador único para un subproceso en Microsoft Teams. |

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
