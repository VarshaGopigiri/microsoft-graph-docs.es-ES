# <a name="listing-versions-of-a-driveitem"></a>Lista de versiones de un DriveItem

OneDrive y SharePoint se pueden configurar para mantener el historial de archivos.
En función del servicio y la configuración, se puede crear una versión para cada edición, cada vez que se guarda el archivo, manualmente, o nunca.

Las versiones anteriores de un documento pueden conservarse durante un período limitado de tiempo, en función de la configuración del administrador que puede ser única para cada usuario o ubicación.

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
GET /drives/{drive-id}/items/{item-id}/versions
GET /groups/{group-id}/drive/{item-id}/versions
GET /me/drive/items/{item-id}/versions
GET /sites/{site-id}/drive/items/{item-id}/versions
GET /users/{user-id}/drive/items/{item-id}/versions
```

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [DriveItemVersion](../resources/driveitemversion.md) en el cuerpo de la respuesta.


## <a name="example"></a>Ejemplo

Este ejemplo recupera las versiones de un archivo en la unidad del usuario actual.

### <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "request", "name": "get-previous-versions", "scopes": "files.read", "tags": "service.graph" } -->

```http
GET /me/drive/items/{item-id}/versions
```

### <a name="response"></a>Respuesta

Devuelve una colección de versiones:

<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.driveItemVersion)", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value":
  [
    {
      "id": "3.0",
      "lastModifiedBy": {
        "user": {
          "id": "CE251278-EF9E-4FE5-833C-1D89EEAE68E0",
          "displayName": "Ryan Gregg"
        }
      },
      "lastModifiedDateTime": "2017-09-14T12:34:53.912Z",
      "size": 123
    },
    {
      "id": "2.0",
      "lastModifiedBy": {
        "user": {
          "id": "CE251278-EF9E-4FE5-833C-1D89EEAE68E0",
          "displayName": "Ryan Gregg"
        }
      },
      "lastModifiedDateTime": "2017-09-11T10:21:03.000Z",
      "size": 62
    },
    {
      "id": "1.0",
      "lastModifiedBy": {
        "user": {
          "id": "CE251278-EF9E-4FE5-833C-1D89EEAE68E0",
          "displayName": "Ryan Gregg"
        }
      },
      "lastModifiedDateTime": "2017-09-10T15:20:01.125Z",
      "size": 16
    }
  ]
}
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
