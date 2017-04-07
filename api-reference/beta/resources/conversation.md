# <a name="conversation-resource-type"></a>Tipo de recurso conversation

Una conversación es una colección de [hilos](conversationthread.md) y un hilo contiene publicaciones de ese hilo. Todos los hilos y publicaciones de una conversación comparten el mismo asunto.

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Enumerar conversaciones](../api/group_list_conversations.md) | Colección [conversation](conversation.md) |Obtenga la lista de conversaciones en este grupo.|
|[Crear](../api/group_post_conversations.md) |[conversation](conversation.md)| Cree una conversación al incluir un hilo y una publicación.|
|[Obtener conversación](../api/conversation_get.md) | [conversation](conversation.md) |Lea las propiedades y las relaciones del objeto de conversación.|
|[Eliminar](../api/conversation_delete.md) | Ninguno |Elimine el objeto de conversación. |
|[Enumerar hilos de conversación](../api/conversation_list_threads.md) |Colección [conversationThread](conversationthread.md)| Obtenga todos los hilos de una conversación de grupo.|
|[Crear hilo de conversación](../api/conversation_post_threads.md) |Colección [conversationThread](conversationthread.md)| Cree un hilo en la conversación especificada.|


## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|hasAttachments|Boolean|Indica si alguna de las publicaciones de esta conversación tiene al menos un dato adjunto.|
|id|String|El identificador único de las conversaciones. Solo lectura.|
|lastDeliveredDateTime|DateTimeOffset|El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|preview|String|Un breve resumen del cuerpo de la última publicación de esta conversación.|
|topic|String|El tema de la conversación. Esta propiedad se puede establecer al crear la conversación, pero no se puede actualizar.|
|uniqueSenders|Colección String|Todos los usuarios que envían un mensaje a esta conversación.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo    |Descripción|
|:---------------|:--------|:----------|
|threads|Colección [conversationThread](conversationthread.md)|Una colección de todos los hilos de la conversación. Una propiedad de navegación. Solo lectura. Admite valores NULL.|


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "threads"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.conversation"
}-->

```json
{
  "hasAttachments": true,
  "id": "string (identifier)",
  "lastDeliveredDateTime": "String (timestamp)",
  "preview": "string",
  "topic": "string",
  "uniqueSenders": ["string"]
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "conversation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
