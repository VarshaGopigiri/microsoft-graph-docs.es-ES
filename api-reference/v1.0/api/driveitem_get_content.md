---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Descargar un archivo
ms.openlocfilehash: efed0b12484c3656e5b2b4b9cbe8fb84cdc27006
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23268091"
---
# <a name="download-the-contents-of-a-driveitem"></a>Descargar el contenido de un objeto DriveItem

Descargue el contenido de la secuencia principal (archivo) de un DriveItem. Solo se pueden descargar objetos driveItem con la propiedad **file**.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All y Sites.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | Files.Read, Files.ReadWrite, Files.Read.All y Files.ReadWrite.All    |
|Aplicación | Files.Read.All, Files.ReadWrite.All, Sites.Read.All y Sites.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
GET /drives/{drive-id}/items/{item-id}/content
GET /groups/{group-id}/drive/items/{item-id}/content
GET /me/drive/root:/{item-path}:/content
GET /me/drive/items/{item-id}/content
GET /sites/{siteId}/drive/items/{item-id}/content
GET /users/{userId}/drive/items/{item-id}/content
```

## <a name="optional-request-headers"></a>Encabezados de solicitud opcionales

| Nombre          | Valor  | Descripción                                                                                                                                              |
|:--------------|:-------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| if-none-match | Cadena | Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada coincide con la etiqueta actual del archivo, se devuelve una respuesta `HTTP 304 Not Modified`. |

## <a name="example"></a>Ejemplo

Este es un ejemplo para descargar un archivo completo.


<!-- { "blockType": "request", "name": "download-item-content", "scopes": "files.read" } -->

```http
GET /me/drive/items/{item-id}/content
```

### <a name="response"></a>Respuesta

Devuelve una respuesta `302 Found` que redirige a una URL de descarga autenticada previamente para el archivo. Se trata de la misma dirección URL disponible mediante la propiedad `@microsoft.graph.downloadUrl` del objeto DriveItem.

Para descargar el contenido del archivo, la aplicación tendrá que seguir el encabezado `Location` de la respuesta.
Muchas bibliotecas de cliente HTTP seguirán automáticamente el redireccionamiento 302 e iniciarán inmediatamente la descarga del archivo.

Las URL de descarga autenticadas previamente solo son válidas durante un breve período de tiempo (unos minutos) y no requieren un encabezado `Authorization` para descargarlas.

<!-- { "blockType": "response", "@odata.type": "stream" } -->

```http
HTTP/1.1 302 Found
Location: https://b0mpua-by3301.files.1drv.com/y23vmagahszhxzlcvhasdhasghasodfi
```

## <a name="partial-range-downloads"></a>Descargas de rango parcial

Para descargar un rango parcial de bytes del archivo, la aplicación puede usar el encabezado `Range` como se especifica en [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt). Tenga en cuenta que debe anexar el encabezado `Range` a la dirección URL `@microsoft.graph.downloadUrl` real y no a la solicitud de `/content`.

<!-- { "blockType": "request", "opaqueUrl": true, "name": "download-item-partial", "scopes": "files.read" } -->

```http
GET https://b0mpua-by3301.files.1drv.com/y23vmag
Range: bytes=0-1023
```

Esto devolverá una respuesta `HTTP 206 Partial Content` con el rango de solicitud de bytes del archivo. Si no se puede generar el rango, se puede omitir el encabezado Range y se devolverá una respuesta `HTTP 200` con el contenido completo del archivo.

<!-- { "blockType": "response", "name": "download-item-partial", "@odata.type": "stream" } -->

```http
HTTP/1.1 206 Partial Content
Content-Range: bytes 0-1023/2048
Content-Type: application/octet-stream

<first 1024 bytes of file>
```

### <a name="error-responses"></a>Respuestas de error

Vea [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.

[error-response]: ../../../concepts/errors.md

<!-- {
  "type": "#page.annotation",
  "description": "Download the contents of a DriveItem.",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Items/Download"
} -->
