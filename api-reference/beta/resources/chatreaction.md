---
title: tipo de recurso chatMessageReaction
description: 'Representa una reacción a una entidad de chatMessage. '
localization_priority: Normal
ms.openlocfilehash: 5020653ef02c1604aece46f3ff2c7ea1c82a75ec
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27810069"
---
# <a name="chatmessagereaction-resource-type"></a>tipo de recurso chatMessageReaction

Representa una reacción a una entidad de [chatMessage](chatmessage.md) . 

Una entidad de tipo `chatMessageReaction` se devuelve como parte de los [mensajes del canal de obtener](../api/channel-get-message.md) API, como parte de la entidad [chatMessage](chatmessage.md) .

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|reactionType|string| El tipo de reacción. Los valores planeados incluyen: <br><ul><li>Al igual que - como un mensaje, contenido está en blanco en este caso.</li><li>Emoji - Emoji reacción. Contenido se establece en el valor de la emoji unicode.</li><li>Etiqueta - contenido está establecido en la cadena de la etiqueta.</li></ul>|
|createdDateTime|dateTimeOffset|Marca de tiempo UTC del mensaje raíz en formato ISO 8601.|
|usuario|identitySet|El usuario que reacciona al mensaje.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "content"
  ],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.chatMessageReaction"
}-->

```json
{
  "reactionType": "string ",
  "createdDateTime": "string (timestamp)",
  "user": {"@odata.type": "microsoft.graph.identitySet"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "chat message reaction resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
