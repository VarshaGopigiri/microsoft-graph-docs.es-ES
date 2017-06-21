# <a name="remove-acceptedsender"></a>Remove acceptedSender

Quita un usuario o grupo de la lista de acceptedSenders. 
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.ReadWrite.All*
## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/acceptedSenders/$ref?$id=<id>

```
## <a name="request-headers"></a>Encabezados de solicitud
| Encabezado       | Valor |
|:---------------|:--------|
| Authorization  | {token} de portador. Necesario.  |

## <a name="request-body"></a>Cuerpo de solicitud
No proporcione un cuerpo de solicitud para este método.


## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un par de ejemplos de la solicitud.
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_group"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groups/{id}/acceptedSenders/$ref?$id="users/{id}"

DELETE https://graph.microsoft.com/v1.0/groups/{id}/acceptedSenders/$ref?$id="groups/{id}"
```

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create acceptedSender",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->