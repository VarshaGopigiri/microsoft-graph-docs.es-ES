# <a name="download-contents-of-a-driveitemversion-resource"></a>Descargar contenido de un recurso DriveItemVersion

Recupere el contenido de una versión específica de un recurso [DriveItem](../resources/driveitem.md).

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All y Sites.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | Files.Read, Files.ReadWrite, Files.Read.All y Files.ReadWrite.All    |
|Aplicación | Files.Read.All, Files.ReadWrite.All, Sites.Read.All y Sites.ReadWrite.All |


## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored"} -->

```http
GET /drives/{drive-id}/items/{item-id}/versions/{version-id}/content
GET /groups/{group-id}/drive/{item-id}/versions/{version-id}/content
GET /me/drive/items/{item-id}/versions/{version-id}/content
GET /sites/{site-id}/drive/items/{item-id}/versions/{version-id}/content
GET /users/{user-id}/drive/items/{item-id}/versions/{version-id}/content
```

## <a name="response"></a>Respuesta

Devuelve una respuesta `302 Found` que redirige a una dirección URL de descarga autenticada previamente para los bytes del archivo.

Para descargar el contenido del archivo, la aplicación tendrá que seguir el encabezado `Location` de la respuesta. Muchas bibliotecas de cliente HTTP seguirán de forma automática el redireccionamiento 302 e iniciarán la descarga del archivo de forma inmediata.

Las URL de descarga autenticadas previamente solo son válidas durante un breve período de tiempo (unos minutos) y no requieren un encabezado `Authorization` para descargarlas.

## <a name="example"></a>Ejemplo

Este ejemplo recupera una versión de un archivo en la unidad del usuario actual.

### <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "request", "name": "get-version-contents", "scopes": "files.read", "tags": "service.graph" } -->

```http
GET /me/drive/items/{item-id}/versions/{version-id}/content
```

### <a name="response"></a>Respuesta

Esto devuelve una redirección donde se puede descargar el contenido de la versión.

<!-- { "blockType": "response", "isEmpty": true  } -->

```http
HTTP/1.1 302 Found
Location: https://onedrive.com/34FF49D6...
```


## <a name="remarks"></a>Comentarios

OneDrive no conserva todos los metadatos de las versiones anteriores de un archivo.

Cuando la aplicación recupera la lista de versiones disponibles de un archivo, se devuelve un recurso [DriveItemVersion](../resources/driveItemVersion.md) que proporciona la información disponible sobre la versión específica.

<!-- {
  "type": "#page.annotation",
  "description": "List, review, and download previous versions of a driveItem",
  "keywords": "version, version history, versions",
  "section": "documentation",
  "tocPath": "Items/Version history"
} -->
