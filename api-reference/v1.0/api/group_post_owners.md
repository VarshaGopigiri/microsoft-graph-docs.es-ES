# <a name="add-group-owner"></a>Añadir propietario de grupo
Agrega un usuario a los propietarios del grupo. Los propietarios son un conjunto de usuarios no administradores que tienen permiso para modificar el objeto de grupo.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | Group.ReadWrite.All y User.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/owners/$ref
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:---------------|:--------|:----------|
| Authorization  | cadena  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md) que se va a agregar.

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
#### <a name="request"></a>Solicitud
Este es un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_group"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/owners/$ref
Content-type: application/json
Content-length: 30

{
  "@odata.id": "https://graph.microsoft.com/v1.0/users/{id}"
}
```
En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md) que se va a agregar.

#### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta.
>**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create owner",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
