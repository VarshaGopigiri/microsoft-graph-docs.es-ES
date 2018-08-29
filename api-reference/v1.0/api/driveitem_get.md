---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Obtener un archivo o carpeta
ms.openlocfilehash: 9d45cf345981eb3da638d2f25bb51428ec40b7f9
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23267986"
---
# <a name="get-a-driveitem-resource"></a>Get a DriveItem resource

Recupera los metadatos de un [DriveItem](../resources/driveitem.md) en un [Drive](../resources/drive.md) a través del identificador o ruta de acceso del sistema.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All    |
|Aplicación | Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
GET /drives/{drive-id}/items/{item-id}
GET /drives/{drive-id}/root:/{item-path}
GET /groups/{group-id}/drive/items/{item-id}
GET /groups/{group-id}/drive/root:/{item-path}
GET /me/drive/items/{item-id}
GET /me/drive/root:/{item-path}
GET /sites/{siteId}/drive/items/{itemId}
GET /sites/{siteId}/drive/root:/{item-path}
GET /users/{userId}/drive/items/{itemId}
GET /users/{userId}/drive/root:/{item-path}
```

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales

Este método admite los [parámetros de consulta OData](../../../concepts/query_parameters.md) `$expand` y `$select` para personalizar la respuesta.

Puede usar el [parámetro de cadena de consulta `$expand`](../../../concepts/query_parameters.md) para incluir los elementos secundarios de un elemento en la misma llamada al recuperar los metadatos de un elemento si el elemento tiene una relación **children**.

## <a name="optional-request-headers"></a>Encabezados de solicitud opcionales

| Nombre          | Valor  | Descripción                                                                                                                                              |
|:--------------|:-------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| if-none-match | String | Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada coincide con la etiqueta actual del archivo, se devuelve una respuesta `HTTP 304 Not Modified`. |

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el recurso [DriveItem](../resources/driveitem.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud a la carpeta raíz de OneDrive del usuario.

<!-- { "blockType": "request", "name": "get-drive-root", "tags": "service.graph" }-->

```http
GET /me/drive/root
```

## <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta.

<!-- { "blockType": "response", "truncated": true, "@odata.type": "microsoft.graph.driveItem" } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "createdBy": {
      "user": {
          "id": "efee1b77-fb3b-4f65-99d6-274c11914d12",
          "displayName": "Ryan Gregg"
      }
  },
  "createdDateTime": "2016-03-21T20:01:37Z",
  "cTag": "\"c:{86EB4C8E-D20D-46B9-AD41-23B8868DDA8A},0\"",
  "eTag": "\"{86EB4C8E-D20D-46B9-AD41-23B8868DDA8A},1\"",
  "folder": { "childCount": 120 },
  "id": "01NKDM7HMOJTVYMDOSXFDK2QJDXCDI3WUK",
  "lastModifiedBy": {
      "user": {
          "id": "efee1b77-fb3b-4f65-99d6-274c11914d12",
          "displayName": "Ryan Gregg"
      }
  },
  "lastModifiedDateTime": "2016-03-21T20:01:37Z",
  "name": "OneDrive",
  "root": { },
  "size": 157286400,
  "webUrl": "https://contoso-my.sharepoint.com/personal/rgregg_contoso_com/Documents"
}
```

## <a name="remarks"></a>Comentarios

Vea [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.

[error-response]: ../../../concepts/errors.md
[odata-parameters]: ../../../concepts/query_parameters.md
[item-resource]: ../resources/driveitem.md
[special-folder]: ../api/drive_get_specialfolder.md

<!-- {
  "type": "#page.annotation",
  "description": "Retrieve metadata about an item and its children in OneDrive",
  "keywords": "retrieve,item,metadata",
  "section": "documentation",
  "tocPath": "Items/Get item"
} -->
