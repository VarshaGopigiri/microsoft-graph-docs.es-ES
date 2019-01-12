---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Enumerar unidades
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 5c85533a2c335158d953749ae329cc6cd2b7ec37
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27966233"
---
# <a name="list-available-drives"></a>List available drives

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Recupera la lista de recursos [Drive](../resources/drive.md) disponibles para un User, Group o [Site](../resources/site.md) de destino.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All    |
|Aplicación | Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All |

## <a name="list-a-groups-drives"></a>Enumerar las unidades de un grupo

Para enumerar las bibliotecas de documentos de un grupo, la aplicación solicita la relación **drives** en el grupo.

### <a name="http-request"></a>Solicitud HTTP

<!-- {"blockType": "request", "name": "group-list-drives", "scopes": "groups.read.all" } -->

```http
GET /groups/{groupId}/drives
```

## <a name="list-a-sites-drives"></a>Enumerar las unidades de un sitio

Para enumerar las bibliotecas de documentos de un sitio, la aplicación solicita la relación **drives** en el sitio.

<!-- {"blockType": "request", "name": "site-list-drives", "scopes": "sites.read.all" } -->

```http
GET /sites/{siteId}/drives
```

## <a name="list-a-users-drives"></a>Enumerar las unidades de un usuario

<!-- {"blockType": "request", "name": "user-list-drives", "scopes": "files.read.all" } -->

```http
GET /users/{userId}/drives
```

## <a name="list-the-current-users-drives"></a>Enumerar las unidades del usuario actual

<!-- {"blockType": "request", "name": "enum-drives", "scopes": "files.read" } -->

```http
GET /me/drives
```

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales

Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$expand`, `$select`, `$skipToken`, `$top` y `$orderby` para personalizar la respuesta.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Drive](../resources/drive.md) en el cuerpo de la respuesta.

<!-- { "blockType": "response", 
       "@odata.type": "Collection(microsoft.graph.drive)",
       "name": ["group-list-drives", "site-list-drives", "user-list-drives", "enum-drives"],
       "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "id": "942CAEB0-13AE-491B-85E4-7557CDC0F25F",
      "driveType": "documentLibrary",
      "name": "Shared Documents",
      "owner": {
        "user": {
          "id": "AE2A1EE9-81A7-423C-ABE4-B945F47509BB",
          "displayName": "Ryan Gregg"
        }
      }
    },
    {
      "id": "C1CD3ED9-0E98-4B0B-82D3-C8FB784B9DCC",
      "driveType": "documentLibrary",
      "name": "Contoso Project Files",
      "owner": {
        "user": {
          "id": "406B2281-18E8-4416-9857-38C531B904F1",
          "displayName": "Daron Spektor"
        }
      }
    }
  ]
}
```

## <a name="remarks"></a>Comentarios

La mayoría de los usuarios solo tendrán un único recurso Drive.

Puede que los grupos y los sitios tengan varios recursos Drive disponibles.

De manera predeterminada, las unidades con la faceta [system][] están ocultas.
Para obtener una lista de ellas, incluya `system` en su `$select` instrucción.

[system]: ../resources/systemfacet.md

<!-- {
  "type": "#page.annotation",
  "description": "List the available drives for a user, group, or site.",
  "keywords": "drive,onedrive.drive,list drives",
  "section": "documentation",
  "tocPath": "Drives/List drives"
} -->
