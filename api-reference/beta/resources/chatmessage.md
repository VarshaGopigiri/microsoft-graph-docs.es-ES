---
title: tipo de recurso chatMessage
description: Representa un mensaje de chat individuales dentro de una entidad de canal o chat. El mensaje puede ser un mensaje de raíz o parte de un subproceso que se define mediante la propiedad **replyToId** en el mensaje.
ms.openlocfilehash: 1fba27567d5a1c80a36a5758925ec427735504cf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083272"
---
# <a name="chatmessage-resource-type"></a>tipo de recurso chatMessage

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa un mensaje de chat individuales dentro de una entidad de [canal](channel.md) o chat. El mensaje puede ser un mensaje de raíz o parte de un subproceso que se define mediante la propiedad **replyToId** en el mensaje.

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Mensajes del canal de lista](../api/channel-list-messages.md) | colección de [chatmessage](chatmessage.md) | Obtener la lista de todos los mensajes de raíz en un canal.|
|[Mensaje de canal de Get](../api/channel-get-message.md) | [chatmessage](chatmessage.md) | Recibe un mensaje de raíz única de un canal.|
|[Lista de respuestas a un mensaje](../api/channel-list-messagereplies.md) | colección de [chatmessage](chatmessage.md)| Obtener la lista de todas las respuestas a un mensaje en el canal.|
|[Obtener una respuesta a un mensaje](../api/channel-get-messagereply.md) | [chatmessage](chatmessage.md)| Obtenga una sola respuesta a un mensaje en un canal.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|String| Solo lectura. Identificador único del mensaje.|
|replyToId| string | Identificador del mensaje de mensaje/raíz primario del subproceso |
|from|[identitySet](identityset.md)| Detalles del remitente del mensaje|
|etag| string | Número de versión del mensaje |
|messageType|String|Los valores de tipo de mensaje, actual admitido son: mensajes, chatEvent, escribir|
|createdDateTime|dateTimeOffset|Solo lectura. Marca de hora de cuándo se creó el mensaje|
|lastModifiedDateTime|dateTimeOffset|Solo lectura. Marca de hora de cuando el mensaje fue editado o actualizado|
|isDeleted|boolean|Representa si un mensaje se ha eliminado suave|
|deletedDateTime|dateTimeOffset|Solo lectura. Marca de tiempo en el que se ha eliminado el mensaje |
|subject|string|Línea de asunto del mensaje. Opcional|
|body|[itemBody](itembody.md)|Representación de texto sin formato o HTML del contenido del mensaje. Devuelve el texto sin formato de forma predeterminada, la aplicación elegir HTML como parte de un parámetro de consulta|
|Resumen|string|Texto del resumen del mensaje que se puedan usar para las notificaciones de inserción y vistas de resumen o vistas de atrás retroceso|
|menciones|colección de [chatMessageMention](chatmention.md)| Lista de entidades que se mencionan en el mensaje. Admite actualmente el usuario, bot, equipo, canal|
|importance| string | La importancia del mensaje: Normal, alta|
|reacciones| colección de [chatMessageReaction](chatreaction.md) | Las reacciones de este mensaje (como por ejemplo,)|
|configuración regional|string|Configuración regional del mensaje establecido por el cliente|
|attachments|colección de [chatMessageAttachment](chatattachment.md) |Archivos adjuntos|


## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "isDeleted",
    "deletedDateTime",
    "attachments",
    "importance",
    "reactions",
    "mentions",
    "subject",
    "summary"
  ],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.chatMessage"
}-->

```json
{
  "id": "string (identifier)",
  "replyToId": "string (identifier)",
  "from": {"@odata.type": "microsoft.graph.identitySet"},
  "etag": "string",
  "messageType": "string",
  "createdDateTime": "string (timestamp)",
  "lastModifiedDateTime": "string (timestamp)",
  "isDeleted": "boolean",
  "deletedDateTime": "string (timestamp)",
  "subject": "string",
  "body": {"@odata.type": "microsoft.graph.itemBody"},
  "summary": "string",
  "attachments": [{"@odata.type": "microsoft.graph.chatMessageAttachment"}],
  "mentions": [{"@odata.type": "microsoft.graph.chatMessageMention"}],
  "importance": "string",
  "reactions": [{"@odata.type": "microsoft.graph.chatMessageReaction"}],
  "locale": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "chat message resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
