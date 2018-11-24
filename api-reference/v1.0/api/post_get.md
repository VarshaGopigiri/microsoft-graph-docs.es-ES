# <a name="get-post"></a>Obtener publicación

Obtiene las propiedades y relaciones de una publicación de un hilo determinado. Puede especificar la conversación primaria y el hilo, o bien, especificar el hilo sin hacer referencia a la conversación primaria.

Dado que el recurso **post** admite [extensiones](../../../concepts/extensibility_overview.md), también puede utilizar la operación `GET` para obtener propiedades personalizadas y datos de extensión en una instancia **post**.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Group.Read.All, Group.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | Group.Read.All, Group.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/threads/{id}/posts/{id}
GET /groups/{id}/conversations/{id}/threads/{id}/posts/{id}
```
## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales
Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.
## <a name="request-headers"></a>Encabezados de solicitud
| Encabezado       | Valor |
|:---------------|:--------|
| Authorization  | {token} de portador. Obligatorio.  |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [post](../resources/post.md) en el cuerpo de la respuesta.
## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "get_post"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/threads/{id}/posts/{id}
```
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.post"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 414

{
  "body": {
    "contentType": "",
    "content": "content-value"
  },
  "receivedDateTime": "datetime-value",
  "hasAttachments": true,
  "from": {
    "emailAddress": {
      "name": "name-value",
      "address": "address-value"
    }
  },
  "sender": {
    "emailAddress": {
      "name": "name-value",
      "address": "address-value"
    }
  }
}
```

## <a name="see-also"></a>Vea también

- [Agregar datos personalizados a los recursos mediante extensiones](../../../concepts/extensibility_overview.md)
- [Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)](../../../concepts/extensibility_open_users.md)
<!--
- [Add custom data to groups using schema extensions (preview)](../../../concepts/extensibility_schema_groups.md)
-->


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get post",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
