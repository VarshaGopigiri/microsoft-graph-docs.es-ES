---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Obtener unidad
localization_priority: Priority
ms.prod: sharepoint
ms.openlocfilehash: aaa670111b61fe0ecd1c111e5fd3be650d115435
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27978679"
---
# <a name="get-drive"></a>Obtener unidad

Recupere las propiedades y relaciones de un recurso [Drive](../resources/drive.md).

Un recurso Drive es el contenedor de nivel superior de un sistema de archivos, como bibliotecas de documentos de OneDrive o SharePoint.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All    |
|Aplicación | Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All |

## <a name="get-current-users-onedrive"></a>Obtener el OneDrive del usuario actual

Se puede tener acceso a la unidad del usuario que ha iniciado sesión (si se usa la autenticación delegada) desde el singleton `me`.

Si no se ha aprovisionado el OneDrive de un usuario pero este tiene una licencia para usar OneDrive, esta solicitud aprovisionará de forma automática la unidad del usuario, cuando se usa la autenticación delegada.

### <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "request", "name": "get-drive-default", "scopes": "files.read", "tags": "service.graph" } -->

```http
GET /me/drive
```

## <a name="get-a-users-onedrive"></a>Obtener la cuenta de OneDrive de un usuario

Para obtener acceso al OneDrive o OneDrive para la Empresa de un usuario, la aplicación debe solicitar la relación **drive** en el recurso User.

Si no se ha aprovisionado el OneDrive de un usuario pero este tiene una licencia para usar OneDrive, esta solicitud aprovisionará de forma automática la unidad del usuario, cuando se usa la autenticación delegada.

### <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "request", "name": "get-drive-by-user", "scopes": "files.read.all", "tags": "service.graph" } -->

```http
GET /users/{idOrUserPrincipalName}/drive
```

### <a name="path-parameters"></a>Parámetros de ruta de acceso

| Nombre del parámetro | Valor  | Descripción                                       |
|:---------------|:-------|:--------------------------------------------------|
| _idOrUserPrincipalName_     | string | Obligatorio. El identificador del objeto de usuario que es el propietario del OneDrive. |

## <a name="get-the-document-library-associated-with-a-group"></a>Obtener la biblioteca de documentos asociada a un grupo

Para obtener acceso a la biblioteca de documentos predeterminada de un grupo, la aplicación solicita la relación **drive** en el grupo.

### <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "request", "name": "get-drive-by-group", "scopes": "group.read.all", "tags": "service.graph" } -->

```http
GET /groups/{groupId}/drive
```

### <a name="path-parameters"></a>Parámetros de ruta de acceso

| Nombre del parámetro | Valor  | Descripción                                       |
|:---------------|:-------|:--------------------------------------------------|
| _groupId_      | string | Obligatorio. El identificador del grupo que es el propietario de la biblioteca de documentos. |

## <a name="get-the-document-library-for-a-site"></a>Obtener la biblioteca de documentos de un sitio

Para obtener acceso a la biblioteca de documentos predeterminada de un [sitio](../resources/site.md), la aplicación solicita la relación **drive** en el sitio.

### <a name="http-request"></a>Solicitud HTTP

```http
GET /sites/{siteId}/drive
```

### <a name="path-parameters"></a>Parámetros de ruta de acceso

| Nombre del parámetro | Valor  | Descripción                                       |
|:---------------|:-------|:--------------------------------------------------|
| _siteId_       | string | Obligatorio. El identificador del sitio que contiene la biblioteca de documentos. |

## <a name="get-a-drive-by-id"></a>Obtener una unidad por su identificador

Si tiene el identificador único de una unidad, puede tener acceso a ella directamente desde la colección de unidades de nivel superior.

### <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "request", "name": "get-drive-by-id", "scopes": "files.read" } -->

```http
GET /drives/{drive-id}
```

### <a name="path-parameters"></a>Parámetros de ruta de acceso

| Nombre del parámetro | Valor  | Descripción                                       |
|:---------------|:-------|:--------------------------------------------------|
| _driveId_      | string | Obligatorio. El identificador de la unidad que se ha solicitado. |

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales

Este método admite el [parámetro de consulta $select][odata-query-parameters] para dar forma a la respuesta.

## <a name="response"></a>Respuesta

Cada uno de estos métodos devuelve un [recurso Drive][drive-resource] para la unidad coincidente en el cuerpo de la respuesta.

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.drive", "truncated": true, "name": ["get-drive-by-id", "get-drive-by-group", "get-drive-by-user", "get-drive-default"] } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "id": "b!t18F8ybsHUq1z3LTz8xvZqP8zaSWjkFNhsME-Fepo75dTf9vQKfeRblBZjoSQrd7",
    "driveType": "business",
    "owner": {
        "user": {
            "id": "efee1b77-fb3b-4f65-99d6-274c11914d12",
            "displayName": "Ryan Gregg"
        }
    },
    "quota": {
        "deleted": 256938,
        "remaining": 1099447353539,
        "state": "normal",
        "total": 1099511627776
    }
}
```

### <a name="error-response-codes"></a>Códigos de respuesta de error

Si la unidad no existe y no se puede aprovisionar automáticamente (al usar la autenticación delegada) se devolverá una respuesta `HTTP 404`.

[drive-resource]: ../resources/drive.md
[odata-query-parameters]: /graph/query-parameters

<!-- {
  "type": "#page.annotation",
  "description": "Get metadata for a OneDrive, OneDrive for Business, or Office 365 group drive",
  "keywords": "drive,onedrive,default drive,group drive",
  "section": "documentation",
  "suppressions": [
      "Warning: /api-reference/v1.0/api/drive-get.md:
        Unable to map some markdown elements into schema.
            Unmapped methods:
        get-drive-default, get-drive-by-user, get-drive-by-group, get-drive-by-id
            Unmapped tables:
        Permissions - AuthScopes, Path parameters - PathParameters, Path parameters - PathParameters, Path parameters - PathParameters, Path parameters - PathParameters"
  ],
  "tocPath": "Drives/Get drive"
} -->
