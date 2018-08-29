# <a name="add-directory-role-member"></a>Add directory role member

Usa esta API para crear un miembro de rol de directorio.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Directory.AccessAsUser.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | No admitida. |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /directoryRoles/{id}/members/$ref

```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:---------------|:--------|:----------|
| Authorization  | cadena  | {token} de portador. Obligatorio. |
| Content-Type  | string  | application/json  |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione una representación JSON de un objeto [directoryObject](../resources/directoryobject.md) o [user](../resources/user.md) que se va a agregar.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud

<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_directoryrole"
}-->
```http
POST https://graph.microsoft.com/v1.0/directoryRoles/{id}/members/$ref
Content-type: application/json

{
  "@odata.id": "https://graph.microsoft.com/v1.0/directoryObjects/{id}"
}
```

##### <a name="response"></a>Respuesta
Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject"
} -->
```http
HTTP/1.1 204 No Content
Content-type: text/plain

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create member",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->