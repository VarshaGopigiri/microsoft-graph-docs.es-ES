---
title: tipo de recurso chatInfo
description: Información acerca de un mensaje en Microsoft Teams.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 840073d6882d6665be60e7386eaafe3168b70dbe
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27940753"
---
# <a name="chatinfo-resource-type"></a>tipo de recurso chatInfo

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Información acerca de un mensaje en Microsoft Teams.

## <a name="properties"></a>Propiedades

| Propiedad            | Tipo    | Descripción|
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
