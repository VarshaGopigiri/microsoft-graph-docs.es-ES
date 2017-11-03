# <a name="list-messages"></a>Enumerar mensajes

Obtenga los mensajes del buzón del usuario que ha iniciado sesión (incluidas las carpetas Elementos eliminados y Otros correos).

Actualmente, esta operación devuelve los cuerpos de los mensajes solo en formato HTML.


### <a name="get-messages-in-another-users-message-folder"></a>Obtener mensajes en la carpeta de mensajes de otro usuario

Si dispone de permisos de la aplicación o si tiene los [permisos](#permissions) delegados apropiados de un usuario, es posible obtener los contactos de la carpeta de contactos de otro usuario. Esta sección se centra en escenarios que implican permisos delegados.

Por ejemplo, su aplicación ha adquirido permisos delegados del usuario John. Suponga que otro usuario, Garth, ha compartido una carpeta de mensajes con John. Puede obtener los mensajes de dicha carpeta compartida especificando el identificador de usuario de Garth (o su nombre principal de usuario) en la consulta de ejemplo que se muestra a continuación.

<!-- { "blockType": "ignored" } -->
```http
GET /users/{Garth-id | Garth-userPrincipalName}/messages
```

Esta capacidad se aplica a todas las operaciones de mensajes GET compatibles para un usuario individual, como se muestra en la sección [solicitud HTTP](#http-request) a continuación. También se aplica si Garth ha delegado todo el buzón en John.

Si Garth no ha compartido su carpeta de mensajes con John ni ha delegado su buzón en John, especificar el identificador de usuario del Garth o el nombre principal de usuario en esas operaciones GET devolverá un error. En tales casos, especificar un identificador de usuario o un nombre principal de usuario solo funciona para obtener los mensajes de las carpetas de mensajes del usuario que ha iniciado sesión, y la consulta es equivalente a usar el método abreviado de /me:

<!-- { "blockType": "ignored" } -->
```http
GET /me/messages
```

Esta capacidad solo está disponible en las operaciones GET de:

- Uso compartido de carpetas de contactos, calendarios y carpetas de mensajes 
- Contactos, eventos y mensajes en carpetas compartidas
- Los recursos anteriores en buzones delegados

Esta capacidad no está disponible en otras operaciones de contactos, eventos, mensajes y sus carpetas.


## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Mail.Read, Mail.ReadWrite    |
|Delegado (cuenta personal de Microsoft) | Mail.Read, Mail.ReadWrite    |
|Aplicación | Mail.Read, Mail.ReadWrite |

## <a name="http-request"></a>Solicitud HTTP

Para obtener todos los mensajes del buzón de un usuario:

<!-- { "blockType": "ignored" } -->
```http
GET /me/messages
GET /users/{id | userPrincipalName}/messages
```

Para obtener los mensajes de una carpeta específica del buzón del usuario:

<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/{id}/messages
GET /users/{id | userPrincipalName}/mailFolders/{id}/messages
```

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales
Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.
## <a name="request-headers"></a>Encabezados de solicitud
| Encabezado       | Valor |
|:---------------|:--------|
| Authorization  | {token} de portador. Obligatorio.  |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Message](../resources/message.md) en el cuerpo de la respuesta.

El tamaño de página predeterminada para esta solicitud es de 10 mensajes.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "get_messages"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages
```
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 317

{
  "value": [
    {
      "receivedDateTime": "datetime-value",
      "sentDateTime": "datetime-value",
      "hasAttachments": true,
      "subject": "subject-value",
      "body": {
        "contentType": "",
        "content": "content-value"
      },
      "bodyPreview": "bodyPreview-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List messages",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
