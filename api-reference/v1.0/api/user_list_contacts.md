# <a name="list-contacts"></a>List contacts

Obtiene una colección de contactos de la carpeta de contactos predeterminada del usuario que inició sesión.


### <a name="get-contacts-in-another-users-contact-folder"></a>Obtener los contactos de la carpeta de contactos de otro usuario

Si dispone de permisos de la aplicación o si tiene los [permisos](#permissions) delegados apropiados de un usuario, es posible obtener los contactos de la carpeta de contactos de otro usuario. Esta sección se centra en escenarios que implican permisos delegados.

Por ejemplo, su aplicación ha adquirido permisos delegados del usuario John. Suponga que otro usuario, Garth, ha compartido una carpeta de contactos con John. Puede obtener los contactos de dicha carpeta compartida especificando el identificador de usuario de Garth (o su nombre principal de usuario) en la consulta de ejemplo que se muestra a continuación.

<!-- { "blockType": "ignored" } -->
```http
GET /users/{Garth-id | Garth-userPrincipalName}/contacts
```

Esta capacidad se aplica a todas las operaciones de contactos GET compatibles para un usuario individual, como se muestra en la sección [solicitud HTTP](#http-request) a continuación. También se aplica si Garth ha delegado todo el buzón en John.

Si Garth no ha compartido su carpeta de contactos con John ni ha delegado su buzón en John, especificar el identificador de usuario del Garth o el nombre principal de usuario en esas operaciones GET devolverá un error. En tales casos, especificar un identificador de usuario o un nombre principal de usuario solo funciona para obtener los contactos de las carpetas de contactos del usuario que ha iniciado sesión, y la consulta es equivalente a usar el método abreviado de /me:

<!-- { "blockType": "ignored" } -->
```http
GET /me/contacts
```

Esta capacidad solo está disponible en las operaciones GET de:

- Carpetas de contactos compartidas
- Calendarios compartidos
- Contactos y eventos en carpetas compartidas
- Los recursos anteriores en buzones delegados

Esta capacidad no está disponible en otras operaciones de contactos, eventos y sus carpetas.


## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Contacts.Read, Contacts.ReadWrite    |
|Delegado (cuenta personal de Microsoft) | Contacts.Read, Contacts.ReadWrite    |
|Aplicación | Contacts.Read, Contacts.ReadWrite |

## <a name="http-request"></a>Solicitud HTTP

Para obtener todos los contactos del buzón del usuario:

<!-- { "blockType": "ignored" } -->
```http
GET /me/contacts
GET /users/{id | userPrincipalName}/contacts
```

Para obtener los contactos de una carpeta específica del buzón del usuario:

<!-- { "blockType": "ignored" } -->
```http
GET /me/contactfolders/{Id}/contacts
GET /users/{id | userPrincipalName}/contactfolders/{id}/contacts

GET /me/contactFolder/{id}/childFolders/{id}/.../contacts
GET /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts
```
## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales
Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.

Por ejemplo, puede usar el parámetro de consulta `$filter` para filtrar contactos en función del dominio de sus direcciones de correo:

`https://graph.microsoft.com/v1.0/me/contacts?$filter=emailAddresses/any(a:a/address eq '@domain.com')`



## <a name="request-headers"></a>Encabezados de solicitud
| Encabezado       | Valor |
|:---------------|:--------|
| Authorization  | {token} de portador. Obligatorio.  |
| Content-Type   | application/json  |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Contact](../resources/contact.md) en el cuerpo de la respuesta.
## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "get_contacts"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/contacts
```


##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contact",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 263

{
  "value": [
    {
      "parentFolderId": "parentFolderId-value",
      "birthday": "datetime-value",
      "fileAs": "fileAs-value",
      "displayName": "displayName-value",
      "givenName": "givenName-value",
      "initials": "initials-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List contacts",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
