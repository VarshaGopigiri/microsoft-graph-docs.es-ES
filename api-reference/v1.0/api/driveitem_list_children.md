---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Mostrar el contenido de una carpeta
ms.openlocfilehash: 31e20780379055b9ec8217bb90b4da26414a64e5
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23265221"
---
# <a name="list-children-of-a-driveitem"></a>Mostrar los elementos secundarios de un objeto driveItem

Devuelva una colección de objetos [DriveItem](../resources/driveitem.md) en la relación **children** de un objeto DriveItem.

Los objetos DriveItem con una faceta **folder** o **package** que no es null pueden tener uno o varios objetos DriveItem secundarios.


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
GET /drives/{drive-id}/items/{item-id}/children
GET /groups/{group-id}/drive/items/{item-id}/children
GET /me/drive/items/{item-id}/children
GET /sites/{site-id}/drive/items/{item-id}/children
GET /users/{user-id}/drive/items/{item-id}/children
```

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales

Este método admite los [parámetros de consulta OData](../../../concepts/query_parameters.md) `$expand`, `$select`, `$skipToken`, `$top` y `$orderby` para personalizar la respuesta.

### <a name="optional-request-headers"></a>Encabezados de solicitud opcionales

| Nombre     | Valor | Descripción                                                                                                                                              |
|:----------------|:------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| _if-none-match_ | ETag  | Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada coincide con la etiqueta actual del archivo, se devuelve una respuesta `HTTP 304 Not Modified`. |

## <a name="examples"></a>Ejemplos

### <a name="list-children-in-the-root-of-the-current-users-drive"></a>Mostrar los elementos secundarios de la raíz de la unidad del usuario actual

Para recuperar archivos en la raíz de la unidad, use la relación `root` en la unidad y, después, obtenga acceso a la relación secundaria.

<!-- { "blockType": "request", "name": "list-children-root", "scopes": "files.read", "tags": "service.graph" } -->

```http
GET /me/drive/root/children
```


### <a name="list-children-of-a-driveitem-with-a-known-id"></a>Mostrar los elementos secundarios de un objeto DriveItem con un identificador conocido

Para recuperar archivos en la raíz de la unidad, use la relación `root` en la unidad y, después, obtenga acceso a la relación secundaria.

<!-- { "blockType": "request", "name": "list-children", "scopes": "files.read" } -->

```http
GET /drives/{drive-id}/items/{item-id}/children
```

### <a name="list-children-of-a-driveitem-with-a-known-path"></a>Mostrar los elementos secundarios de un objeto DriveItem con una ruta de acceso conocida

<!-- { "blockType": "request", "name": "list-children-from-path", "scopes": "files.read" } -->

```http
GET /drives/{drive-id}/root:/{path-relative-to-root}:/children
```

## <a name="response"></a>Respuesta

Si se realiza correctamente, este método devuelve la lista de elementos en la colección de elemento secundarios del elemento de destino.
La colección de elementos secundarios estará formada por recursos [driveItem][item-resource].

<!-- { "blockType": "response", 
       "@odata.type": "Collection(microsoft.graph.driveItem)", 
       "truncated": true,
       "name": [ "list-children-root", "list-children", "list-children-from-path" ] } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {"name": "myfile.jpg", "size": 2048, "file": {} },
    {"name": "Documents", "folder": { "childCount": 4} },
    {"name": "Photos", "folder": { "childCount": 203} },
    {"name": "my sheet(1).xlsx", "size": 197 }
  ],
  "@odata.nextLink": "https://..."
}
```

**Nota:** Si una colección supera el tamaño de página predeterminado (200 elementos), se devuelve la propiedad **@odata.nextLink** en la respuesta para indicar que hay más elementos disponibles y proporcionar la dirección URL de solicitud de la siguiente página de elementos.

Puede controlar el tamaño de la página mediante los [parámetros de cadena de consulta opcionales](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters)

### <a name="error-responses"></a>Respuestas de error

Vea [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.

[error-response]: ../../../concepts/errors.md
[item-resource]: ../resources/driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "List the children of an item.",
  "keywords": "list,children,collection",
  "section": "documentation",
  "tocPath": "Items/List children"
} -->
