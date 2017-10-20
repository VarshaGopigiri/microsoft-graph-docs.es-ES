---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Enumerar archivos compartidos conmigo
ms.openlocfilehash: df6ae423c1c474f8707c71379970c51153eee5c2
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="list-items-shared-with-the-signed-in-user"></a>Enumerar elementos compartidos con el usuario que ha iniciado sesión

Recupere una colección de recursos [DriveItem](../resources/driveitem.md) que se han compartido con el propietario del [Drive](../resources/drive.md).

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | Files.Read.All, Files.ReadWrite.All    |
|Aplicación | Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All |

**Nota:** Aunque la solicitud de /sharedWithMe será correcta con los permisos Files.Read o Files.ReadWrite, pueden perderse algunas propiedades.
Además, sin uno de los permisos **Todo**, los elementos compartidos devueltos desde esta API no serán accesibles.

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "request", "name": "shared-with-me", "scopes": "files.read", "target": "action" } -->

```http
GET /me/drive/sharedWithMe
```

## <a name="response"></a>Respuesta

Devuelve una colección de recursos [DriveItem](../resources/driveitem.md) que contiene los recursos DriveItem compartidos con el propietario de la unidad. En este ejemplo, ya que la unidad es la unidad predeterminada del usuario, devuelve elementos compartidos con el usuario que ha iniciado sesión.

<!-- {"blockType": "response", "@odata.type": "Collection(microsoft.graph.driveItem)", "truncated": true} -->

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

<!-- { "blockType": "ignored", "name": "drives-get-remoteitem" } -->

```http
GET /drives/{remoteItem-driveId}/items/{remoteItem-id}
```

<!-- {
  "type": "#page.annotation",
  "description": "List the items shared with the owner of a drive.",
  "keywords": "drive,onedrive.drive,default drive",
  "section": "documentation",
  "tocPath": "Sharing/Shared with me"
} -->
