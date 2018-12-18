---
title: Tipo de recurso conversationThread
description: Un recurso conversationThread es una colección de posts.
author: dkershaw10
ms.openlocfilehash: 1456b32a26b279b917930740ca220025e8858590
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27332175"
---
# <a name="conversationthread-resource-type"></a>Tipo de recurso conversationThread
Un recurso conversationThread es una colección de [posts](post.md).

La colección de destinatarios de la última publicación son los destinatarios agregados del hilo completo. Un hilo puede tener una colección creciente de destinatarios. Se crea un hilo al eliminar un destinatario del hilo.

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Enumerar hilos](../api/group-list-threads.md) | Colección [conversationThread](conversationthread.md) |Obtenga todos los hilos de un grupo.|
|[Crear hilo](../api/group-post-threads.md) | [conversationThread](conversationthread.md) |Inicie una nueva conversación creando primero un hilo. Se crean una conversación, un hilo de conversación y una publicación en el grupo.|
|[Obtener conversationThread](../api/conversationthread-get.md) | [conversationThread](conversationthread.md) |Obtenga un hilo específico que pertenece a un grupo. |
|[Actualizar](../api/conversationthread-update.md) | [conversationThread](conversationthread.md)  |Actualice el objeto conversationThread. |
|[Eliminar](../api/conversationthread-delete.md) | Ninguno |Elimine el objeto conversationThread. |
|[Responder](../api/conversationthread-reply.md)|Ninguno|Responda a este hilo mediante la creación de una nueva entidad Post.|
|[Enumerar publicaciones](../api/conversationthread-list-posts.md) |Colección [post](post.md)| Obtenga las publicaciones del hilo especificado. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|String| Solo lectura.|
|toRecipients|Colección [recipient](recipient.md)|Los destinatarios Para: del hilo.|
|ccRecipients|Colección [recipient](recipient.md)|Los destinatarios CC: del hilo.|
|topic|String|El tema de la conversación. Esta propiedad se puede establecer al crear la conversación, pero no se puede actualizar.||
|hasAttachments|Boolean|Indica si alguna de las publicaciones de este hilo tiene al menos un dato adjunto.|
|lastDeliveredDateTime|DateTimeOffset|El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|uniqueSenders|Colección String|Todos los usuarios que envían un mensaje a este hilo.|
|preview|String|Un breve resumen del cuerpo de la última publicación de esta conversación.|
|isLocked|Boolean|Indica si el hilo está bloqueado.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|posts|Colección [post](post.md)| Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!--{
  "blockType": "resource",
  "optionalProperties": [
    "posts"
  ],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.conversationThread",
  "@odata.annotations": [
    {
      "property": "posts",
      "capabilities": {
        "changeTracking": false,
        "deletable": false,
        "insertable": false,
        "searchable": false,
        "updatable": false
      }
    }
  ]
}-->

```json
{
  "ccRecipients": [{"@odata.type": "microsoft.graph.recipient"}],
  "hasAttachments": true,
  "id": "string (identifier)",
  "isLocked": true,
  "lastDeliveredDateTime": "String (timestamp)",
  "preview": "string",
  "toRecipients": [{"@odata.type": "microsoft.graph.recipient"}],
  "topic": "string",
  "uniqueSenders": ["string"]
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "conversationThread resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
