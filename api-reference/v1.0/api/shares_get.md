# <a name="accessing-shared-driveitems"></a>Acceder a objetos DriveItem compartidos

Acceda a un objeto [DriveItem](../resources/driveitem.md) compartido o a una colección de elementos compartidos mediante el uso de un **shareId** o una dirección URL para compartir.

Para usar una dirección URL para compartir con esta API, la aplicación debe [transformar la dirección URL en un token para compartir](#transform-a-sharing-url).

## <a name="prerequisites"></a>Requisitos previos

Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:

  * Files.ReadWrite

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->
```http
GET /shares/{sharingIdOrUrl}
```

## <a name="request-body"></a>Cuerpo de solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un recurso [sharedDriveItem](../resources/shareddriveitem.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud

Este es un ejemplo de la solicitud para recuperar un elemento compartido:

<!-- {
  "blockType": "request",
  "name": "get_shares_by_url"
}-->
```http
GET https://graph.microsoft.com/v1.0/shares/{shareIdOrUrl}
```
##### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.sharedDriveItem"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "id": "B64397C8-07AE-43E4-920E-32BFB4331A5B",
  "name": "contoso project.docx",
  "owner": {
    "user": {
      "id": "98E88F1C-F8DC-47CC-A406-C090248B30E5",
      "displayName": "Ryan Gregg"
    }
  }
}
```

## <a name="access-the-shared-item-directly"></a>Acceder directamente al elemento compartido

Mientras que [**SharedDriveItem**](../resources/shareddriveitem.md) contiene alguna información útil, la mayoría de las aplicaciones querrán acceder directamente al objeto [DriveItem](../resources/driveitem.md) compartido. El recurso **SharedDriveItem** incluye un **root** y relaciones de **items** que pueden acceder al contenido del ámbito del elemento compartido.

### <a name="exmaple-single-file"></a>Ejemplo (archivo único)

##### <a name="request"></a>Solicitud

Al solicitar la relación **root**, se devolverá el objeto **DriveItem** compartido.

```http
GET https://graph.microsoft.com/v1.0/shares/{shareIdOrUrl}/root
```

##### <a name="response"></a>Respuesta

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "id": "9FFFDB3C-5B87-4062-9606-1B008CA88E44",
  "name": "contoso project.docx",
  "eTag": "2246BD2D-7811-4660-BD0F-1CF36133677B,1",
  "file": {},
  "size": 109112
}
```

### <a name="exmaple-shared-folder"></a>Ejemplo (carpeta compartida)

##### <a name="request"></a>Solicitud

Al solicitar la relación **root** y expandir la colección **children**, se devolverá el objeto **DriveItem** compartido junto con los archivos de la carpeta compartida.

```http
GET https://graph.microsoft.com/v1.0/shares/{shareIdOrUrl}/root?$expand=children
```

##### <a name="response"></a>Respuesta

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "id": "9FFFDB3C-5B87-4062-9606-1B008CA88E44",
  "name": "Contoso Project",
  "eTag": "2246BD2D-7811-4660-BD0F-1CF36133677B,1",
  "folder": {}
  "size": 10911212,
  "children": [
    {
      "id": "AFBBDD79-868E-452D-AD4D-24697D4A4044",
      "name": "Propsoal.docx",
      "file": {},
      "size": 19001
    },
    {
      "id": "A91FE90A-2F2C-4EE6-B412-C4FFBA3F71A6",
      "name": "Update to Proposal.docx",
      "file": {},
      "size": 91001
    }
  ]
}
```

## <a name="transform-a-sharing-url"></a>Transformar una dirección URL para compartir

Para acceder a una dirección URL para compartir mediante la API **shares**, la dirección URL debe transformarse en un token para compartir.

Para transformar una dirección URL en un token para compartir:

1. Codifique en base64 la dirección URL para compartir.
2. Convierta los datos codificados en base64 en [formato base64url sin rellenar](https://en.wikipedia.org/wiki/Base64); para ello:
  1. Quite los caracteres `=` finales de la cadena
  2. Reemplace los caracteres inseguros de dirección URL con un carácter equivalente; reemplace `/` con `_` y `+` con `-`.
3. Anexe `u!` al principio de la cadena.

Por ejemplo, el siguiente método C# transforma una cadena de entrada en un token para compartir:

```csharp
string UrlToSharingToken(string inputUrl) {
  var base64Value = System.Convert.ToBase64String(System.Text.Encoding.UTF8.GetBytes(inputUrl));
  return "u!" + base64Value.TrimEnd('=').Replace('/','_').Replace('+','-');
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update permission",
  "keywords": "",
  "section": "documentation",
  "tocPath": "OneDrive/Item/Update permission"
}-->
