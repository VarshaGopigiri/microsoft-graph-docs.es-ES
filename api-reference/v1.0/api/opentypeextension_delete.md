# <a name="delete-open-extension"></a>Eliminar extensión abierta

Elimine una extensión abierta (objeto [openTypeExtension](../resources/openTypeExtension.md)) de la instancia especificada de un recurso. 

## <a name="prerequisites"></a>Requisitos previos

Según el recurso desde el que elimine la extensión, se requiere uno de los siguientes **permisos** para ejecutar esta API:

|**Recurso admitido**|**Permiso**|**Recurso admitido**|**Permiso** |
|:-----|:-----|:-----|:-----|
| [device](../resources/device.md) | _Device.ReadWrite.All_ | [event](../resources/event.md) | _Calendars.ReadWrite_ |
| [group](../resources/group.md) | _Group.ReadWrite.All_ | [group event](../resources/event.md) | _Group.ReadWrite.All_ |
| [group post](../resources/post.md) | _Group.ReadWrite.All_ | [mensaje](../resources/message.md) | _Mail.ReadWrite_ |
| [organization](../resources/organization.md) | _Directory.AccessAsUser.All_ | [personal contact](../resources/contact.md) | _Contacts.ReadWrite_ |
| [user](../resources/user.md) | _Directory.AccessAsUser.All_ | | |

 
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
| Authorization | Bearer %token%|


## <a name="request-body"></a>Cuerpo de solicitud
No proporcione un cuerpo de solicitud para este método.


## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.

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