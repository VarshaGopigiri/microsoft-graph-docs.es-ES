# <a name="delete-open-extension"></a>Eliminar extensión abierta

Elimina una extensión abierta (objeto [openTypeExtension](../resources/openTypeExtension.md)) de la instancia especificada de un recurso. 

## <a name="permissions"></a>Permisos

Según el recurso desde el que elimine la extensión, se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|**Recurso admitido**|**Permiso**|**Recurso admitido**|**Permiso** |
|:-----|:-----|:-----|:-----|
| [dispositivo](../resources/device.md) | Device.ReadWrite.All | [evento](../resources/event.md) | Calendars.ReadWrite |
| [grupo](../resources/group.md) | Group.ReadWrite.All | [evento de grupo](../resources/event.md) | Group.ReadWrite.All |
| [publicación de grupo](../resources/post.md) | Group.ReadWrite.All | [mensaje](../resources/message.md) | Mail.ReadWrite |
| [organización](../resources/organization.md) | Directory.AccessAsUser.All | [contacto personal](../resources/contact.md) | Contacts.ReadWrite |
| [usuario](../resources/user.md) | Directory.AccessAsUser.All | | |

## <a name="http-request"></a>Solicitud HTTP
En la solicitud, identifique la instancia de recurso, utilice la propiedad de navegación **extensiones** de esa instancia para identificar y realizar un `DELETE` en esa instancia de extensión.

<!-- { "blockType": "ignored" } -->
```http
DELETE /devices/{Id}/extensions/{extensionId}
DELETE /users/{id|userPrincipalName}/events/{id}/extensions/{extensionId}
DELETE /groups/{id}/extensions/{extensionId}
DELETE /groups/{id}/events/{id}/extensions/{extensionId}
DELETE /groups/{id}/threads/{id}/posts/{id}/extensions/{extensionId}
DELETE /users/{id|userPrincipalName}/messages/{id}/extensions/{extensionId}
DELETE /organization/{Id}/extensions/{extensionId}
DELETE /users/{id|userPrincipalName}/contacts/{id}/extensions/{extensionId}
DELETE /users/{id|userPrincipalName}/extensions/{extensionId}
```

>**Nota:** La sintaxis anterior muestra algunas formas comunes para identificar una instancia del recurso, con el fin de eliminar una extensión de él. Todas las otras formas de sintaxis que le permiten identificar estas instancias de recursos admiten la eliminación de extensiones abiertas de ellas de una manera similar.

## <a name="parameters"></a>Parámetros
|**Parámetro**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|_Parámetros de dirección URL_|
|id|string|Un identificador único para una instancia en la colección correspondiente. Necesario.|
|extensionId|string|Puede ser un nombre de extensión, que es un identificador de texto único de la extensión, o un nombre completo que concatena el tipo de extensión y un identificador de texto único. Se devuelve el nombre completo de la propiedad `id` al crear la extensión. Necesario.|

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Valor |
|:---------------|:----------|
| Authorization | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
El primer ejemplo hace referencia a una extensión por su nombre y elimina la extensión en el mensaje especificado.
<!-- {
  "blockType": "request",
  "name": "delete_opentypeextension"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions('Com.Contoso.Referral')
```

El segundo ejemplo elimina una extensión en el evento de grupo especificado.

<!-- { "blockType": "ignored" } -->
```http
DELETE https://graph.microsoft.com/v1.0/groups('f5480dfd-7d77-4d0b-ba2e-3391953cc74a')/events('AAMkADVlN17IsAAA=')/extensions('Com.Contoso.Referral')
```

 

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta.
<!-- {
  "blockType": "response",
  "truncated": false
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete opentypeextension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->