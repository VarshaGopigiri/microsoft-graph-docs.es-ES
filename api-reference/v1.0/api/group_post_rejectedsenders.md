# <a name="create-rejectedsender"></a>Create rejectedSender

Agrega un nuevo usuario o grupo a la lista de rejectedSender.

En el cuerpo de la solicitud, especifique el usuario o grupo en `@odata.id`. Los usuarios de la lista de remitentes rechazados no pueden publicar conversaciones del grupo (identificado en la dirección URL de solicitud POST). Asegúrese de no especificar el mismo usuario o grupo en las listas de remitentes rechazados y de remitentes aceptados, de lo contrario se producirá un error.
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.ReadWrite.All*
## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/rejectedSenders/$ref
```
## <a name="request-headers"></a>Encabezados de solicitud
| Encabezado       | Valor |
|:---------------|:--------|
| Authorization  | {token} de portador. Necesario.  |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione el identificador de un objeto de usuario o grupo.


## <a name="response"></a>Respuesta
Este método devuelve el código de respuesta `204, No Content` y ningún cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_group"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/rejectedSenders/$ref
Content-type: application/json
Content-length: 30

{
  "@odata.id":"https://graph.microsoft.com/v1.0/users/alexd@contoso.com"
}
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
  "description": "Create rejectedSender",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
