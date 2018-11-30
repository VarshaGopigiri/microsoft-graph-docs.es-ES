---
title: tipo de recurso chatMessageReaction
description: 'Representa una reacción a una entidad de chatMessage. '
ms.openlocfilehash: 1ad1f7948405a8891ec9aa13065b71108e9c47c5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090853"
---
# <a name="chatmessagereaction-resource-type"></a>tipo de recurso chatMessageReaction

Representa una reacción a una entidad de [chatMessage](chatmessage.md) . 

Una entidad de tipo `chatMessageReaction` se devuelve como parte de los [mensajes del canal de obtener](../api/channel-get-message.md) API, como parte de la entidad [chatMessage](chatmessage.md) .

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
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
