---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Obtener acceso a elementos compartidos
ms.openlocfilehash: 15a15dbc2e8ed5e864ef1e2cb649b87711ff1c23
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030318"
---
# <a name="accessing-shared-driveitems"></a>Acceder a objetos DriveItem compartidos

Acceda a un objeto [DriveItem](../resources/driveitem.md) compartido o a una colección de elementos compartidos mediante el uso de un **shareId** o una dirección URL para compartir.

Para usar una dirección URL para compartir con esta API, la aplicación debe [transformar la dirección URL en un token para compartir](#encoding-sharing-urls).

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | Files.ReadWrite, Files.ReadWrite.All    |
|Aplicación | Files.ReadWrite.All, Sites.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
GET /shares/{shareIdOrEncodedSharingUrl}
```

### <a name="path-parameters"></a>Parámetros de ruta de acceso

| Nombre del parámetro        | Valor    | Descripción                                                                         |
|:----------------------|:---------|:------------------------------------------------------------------------------------|
| **sharingTokenOrUrl** | `string` | Obligatorio. Un token para compartir como se devuelve mediante la API o una dirección URL para compartir codificada correctamente. |

### <a name="encoding-sharing-urls"></a>Codificar direcciones URL para compartir

Para codificar una dirección URL para compartir, use la lógica siguiente:

1. Primero, use base64 para codificar la dirección URL.
2. Convierta el resultado codificado en base64 en [formato unpadded base64url](https://en.wikipedia.org/wiki/Base64) quitando los caracteres `=` del final del valor, reemplazando `/` por `_` y `+` por `-`).
3. Anexe `u!` al principio de la cadena.

Como ejemplo, para codificar una dirección URL en C#:

```csharp
string sharingUrl = "https://onedrive.live.com/redir?resid=1231244193912!12&authKey=1201919!12921!1";
string base64Value = System.Convert.ToBase64String(System.Text.Encoding.UTF8.GetBytes(sharingUrl));
string encodedUrl = "u!" + base64Value.TrimEnd('=').Replace('/','_').Replace('+','-');
```

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un recurso [sharedDriveItem](../resources/shareddriveitem.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

### <a name="request"></a>Solicitud

Este es un ejemplo de la solicitud para recuperar un elemento compartido:

<!-- { "blockType": "request", "name": "get-shared-root" } -->

```http
GET /shares/{shareIdOrEncodedSharingUrl}
```

### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta.

<!-- { "blockType": "response", "truncated": true, "@odata.type": "microsoft.graph.sharedDriveItem" } -->

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

## <a name="example-single-file"></a>Ejemplo (archivo único)

### <a name="request"></a>Solicitud

Al solicitar la relación **driveItem**, se devolverá el objeto **DriveItem** compartido.

<!-- { "blockType": "request", "name": "get-shared-driveitem" } -->

```http
GET /shares/{shareIdOrUrl}/driveItem
```

### <a name="response"></a>Respuesta

<!-- { "blockType": "response", "truncated": true, "@odata.type": "microsoft.graph.driveItem" } -->

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

## <a name="example-shared-folder"></a>Ejemplo (carpeta compartida)

### <a name="request"></a>Solicitud

Al solicitar la relación **driveItem** y expandir la colección **children**, se devolverá el objeto **DriveItem** compartido junto con los archivos de la carpeta compartida.

<!-- { "blockType": "request", "name": "get-shared-driveitem-expand-children" } -->

```http
GET /shares/{shareIdOrUrl}/driveItem?$expand=children
```

### <a name="response"></a>Respuesta

<!-- { "blockType": "response", "truncated": true, "@odata.type": "microsoft.graph.driveItem" } -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "id": "9FFFDB3C-5B87-4062-9606-1B008CA88E44",
  "name": "Contoso Project",
  "eTag": "2246BD2D-7811-4660-BD0F-1CF36133677B,1",
  "folder": {},
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

## <a name="error-responses"></a>Respuestas de error

Lea el tema [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.

## <a name="remarks"></a>Comentarios

* Para OneDrive para la Empresa y SharePoint, la API de recursos compartidos siempre requiere autenticación y no puede usarse para tener acceso a contenido compartido de manera anónima sin un contexto de usuario.

[error-response]: /graph/errors

<!-- {
  "type": "#page.annotation",
  "description": "Access the contents of a sharing link with the OneDrive API.",
  "keywords": "shares,shared,sharing,share link, sharing link, share id, share token",
  "section": "documentation",
  "tocPath": "Sharing/Use a link"
} -->
