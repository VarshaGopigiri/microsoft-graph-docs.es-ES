---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Buscar archivos
ms.openlocfilehash: 35349150847c86d1fc7198309c13d910290b9019
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23265235"
---
# <a name="search-for-a-driveitems-within-a-drive"></a>Buscar objetos DriveItem dentro de una unidad

Busque elementos que coincidan con una consulta en la jerarquía de elementos.
Puede buscar en una jerarquía de carpetas, en una unidad entera o en los archivos que se comparten con el usuario actual.

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
GET /drives/{drive-id}/root/search(q='{search-text}')
GET /groups/{group-id}/drive/root/search(q='{search-text}')
GET /me/drive/root/search(q='{search-text}')
GET /sites/{site-id}/drive/root/search(q='{search-text}')
GET /users/{user-id}/drive/root/search(q='{search-text}')
```

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales

Este método admite los [parámetros de consulta OData](../../../concepts/query_parameters.md) `$expand`, `$select`, `$skipToken`, `$top` y `$orderby` para personalizar la respuesta.

## <a name="function-parameters"></a>Parámetros de función

| Nombre | Valor  | Descripción                                                                                                                          |
|:-----|:-------|:-------------------------------------------------------------------------------------------------------------------------------------|
| `q`  | string | El texto de la consulta usado para buscar elementos. Los valores pueden coincidir en varios campos, como el nombre de archivo, los metadatos y el contenido de los archivos. |

## <a name="example"></a>Ejemplo

### <a name="request"></a>Solicitud

Este es un ejemplo de la solicitud buscando en el OneDrive del usuario actual

<!-- { "blockType": "request", "name": "item_search", "tags": "service.graph" }-->

```http
GET /me/drive/root/search(q='{search-query}')
```

### <a name="response"></a>Respuesta

Este método devuelve un objeto que contiene una colección de objetos [DriveItem](../resources/driveitem.md) que coinciden con los criterios de búsqueda. Si no se han encontrado elementos, se devuelve una colección vacía.

Si hay demasiadas coincidencias, se paginará la respuesta y una propiedad **@odata.nextLink** contendrá una dirección URL a la siguiente página de resultados. Puede usar el parámetro de consulta `$top` para especificar el número de elementos en la página.

<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.driveItem)", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
      {
        "id": "0123456789abc!123",
        "name": "Contoso Project",
        "folder": {},
        "searchResult": { "onClickTelemetryUrl": "https://bing.com/0123456789abc!123" }
      },
      {
        "id": "0123456789abc!456",
        "name": "Contoso Project 2016",
        "folder": {},
        "searchResult": { "onClickTelemetryUrl": "https://bing.com/0123456789abc!456" }
      }
    ],
    "@odata.nextLink": "https://graph.microsoft.com/v1.0/me/drive/root/search(query='contoso project')&skipToken=1asdlnjnkj1nalkm!asd"
}
```

## <a name="searching-for-items-a-user-can-access"></a>Buscar elementos a los que puede acceder un usuario

Además de buscar elementos de una unidad, la aplicación puede buscar de forma más amplia para incluir elementos que se comparten con el usuario actual. Para ampliar el ámbito de búsqueda, use el método **search** en el recurso [Drive](../resources/drive.md).

### <a name="example"></a>Ejemplo

<!-- { "blockType": "request", "name": "item_search_all", "tags": "service.graph" }-->

```http
GET /me/drive/search(q='{search-query}')
```

### <a name="response"></a>Respuesta

Las respuestas al buscar desde el recurso **Drive** pueden incluir elementos fuera de la unidad (elementos compartidos con el usuario actual). Estos elementos incluirán la faceta [**remoteItem**](../resources/remoteitem.md) para indicar que se almacenan fuera de la unidad de destino. 

<!-- { "blockType": "response", "truncated": true, "@odata.type": "Collection(microsoft.graph.driveItem)" } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
      {
        "id": "0123456789abc!123",
        "name": "Contoso Project",
        "folder": {},
        "searchResult": { "onClickTelemetryUrl": "https://bing.com/0123456789abc!123" },
        "remoteItem": { "id": "!23141901", "parentReference": { "driveId": "s!1020101jlkjl12lx" } }
      },
      {
        "id": "0123456789abc!456",
        "name": "Contoso Project 2016",
        "folder": {},
        "searchResult": { "onClickTelemetryUrl": "https://bing.com/0123456789abc!456" }
      }
    ],
    "@odata.nextLink": "https://graph.microsoft.com/v1.0/me/drive/root/search(query='contoso project')&skipToken=1asdlnjnkj1nalkm!asd"
}
```

## <a name="error-responses"></a>Respuestas de error

Vea [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.

[error-response]: ../../../concepts/errors.md
[item-resource]: ../resources/driveitem.md
[odata-query-parameters]: ../../../concepts/query_parameters.md

<!-- {
  "type": "#page.annotation",
  "description": "Search for a file across a OneDrive.",
  "keywords": "search,query,bing,filename,content",
  "section": "documentation",
  "tocPath": "Items/Search"
} -->
