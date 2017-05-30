# <a name="create-thread"></a>Crear hilo

Cree un nuevo hilo en la conversación especificada. 

Se crean un hilo y una publicación como se ha especificado. Use [responder hilo](conversationthread_reply.md) para agregar publicaciones al hilo. O, si tiene el identificador de la publicación, también puede [responder](post_reply.md) a esa publicación en ese hilo.

Nota: También puede [crear primero un hilo para iniciar una nueva conversación](group_post_threads.md).

## <a name="prerequisites"></a>Requisitos previos
Se requieren los siguientes **ámbitos** para ejecutar esta API: *Group.ReadWrite.All*
## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/conversations/{id}/threads
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:---------------|:--------|:----------|
| Authorization  | string  | Portador de <token>. Necesario. |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione una representación JSON del objeto [ConversationThread](../resources/conversationthread.md).


## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `201, Created` y el objeto [ConversationThread](../resources/conversationthread.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "create_conversationthread_from_conversation"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/conversations/{id}/threads
Content-type: application/json

{
  "topic": "topic-value",
  "posts": [{
      "body": {
        "contentType": "html",
        "content": "this is body content"
      }
  }]
}
```
En el cuerpo de la solicitud, proporcione una representación JSON del objeto [conversationThread](../resources/conversationthread.md).
##### <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `201, Created` y el `id` del nuevo hilo en el cuerpo de la respuesta. Aquí tiene un ejemplo de la respuesta. 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversationThread"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 346

{
  "id": "thread-id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create thread",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
