# <a name="list-items-shared-with-the-signed-in-user"></a>Enumerar elementos compartidos con el usuario que ha iniciado sesión

Recupere una colección de recursos [DriveItem](../resources/driveitem.md) que se han compartido con el propietario del [Drive](../resources/drive.md).

## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:

  * Files.Read.All
  * Files.ReadWrite.All

**Nota:** aunque la solicitud de /sharedWithMe será correcta con los ámbitos Files.Read o Files.ReadWrite, pueden perderse algunas propiedades. Además, sin uno de estos ámbitos **Todo**, los elementos compartidos devueltos a esta API no serán accesibles.

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->
```
GET /me/drive/sharedWithMe
```

## <a name="request-body"></a>Cuerpo de solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="example"></a>Ejemplo

<!-- { "blockType": "request", "name": "drive-sharedwithme", "scopes": "files.read" } -->
```http
GET https://graph.microsoft.com/v1.0/me/drive/sharedWithMe
```

## <a name="response"></a>Respuesta

Devuelve una colección de recursos [DriveItem](../resources/driveitem.md) que contiene los recursos DriveItem compartidos con el propietario de la unidad. En este ejemplo, ya que la unidad es la unidad predeterminada del usuario, devuelve elementos compartidos con el usuario que ha iniciado sesión.


<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "isCollection": true, "truncated": true } -->
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "id": "1312abc",
      "remoteItem": {
        "id": "1991210caf!192",
        "name": "March Proposal.docx",
        "file": { },
        "size": 19121,
        "parentReference": {
          "driveId": "1991210caf",
          "id": "1991210caf!104"
        }
      }
    },
    {
      "id": "1312def",
      "remoteItem": {
        "id": "1991210caf!1991",
        "name": "Team Roster.xlsx",
        "file": { },
        "size": 37619,
        "parentReference": {
          "driveId": "1991210caf",
          "id": "1991210caf!104"
        }
      }
    }
  ]
}
```

## <a name="remarks"></a>Comentarios

Los recursos driveItem devueltos de la acción **sharedWithMe** incluirán siempre la faceta [**remoteItem**](../resources/remoteitem.md) que indica que son elementos de otra unidad. Para acceder al recurso driveItem compartido, deberá realizar una solicitud con la información proporcionada en **remoteItem** en el siguiente formato:

<!-- {"blockType": "ignored"} -->
```http
GET https://graph.microsoft.com/v1.0/drives/{remoteItem.parentReference.driveId}/items/{remoteItem.id}
```

<!-- {
  "type": "#page.annotation",
  "description": "Retrieve a list of files shared with the signed-in user.",
  "keywords": "sharedWithMe onedrive shared files",
  "section": "documentation",
  "tocPath": "OneDrive/Drive/Shared with me"
} -->
