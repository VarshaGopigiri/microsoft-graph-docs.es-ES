---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Convertir a otros formatos
localization_priority: Priority
ms.prod: sharepoint
ms.openlocfilehash: d33e03df0abcc9417c0fe5bc241e654185bd4313
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27978553"
---
# <a name="download-a-file-in-another-format"></a>Descargar un archivo en otro formato

Use esta API para recuperar el contenido de un elemento en un formato determinado.
No todos los archivos pueden convertirse a todos los formatos.

Para descargar el elemento en su formato original, vea [Descargar contenido de un elemento](driveitem-get-content.md).

## <a name="prerequisites"></a>Requisitos previos

Para llamar a esta API, al usuario se le debe haber concedido el acceso de lectura de la aplicación al archivo que la aplicación quiere convertir.

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
GET /drive/items/{item-id}/content?format={format}
GET /drive/root:/{path and filename}:/content?format={format}
```

## <a name="query-parameters"></a>Parámetros de consulta

| Parámetro      | Tipo  | Descripción                                                    |
|:----------|:-------|:---------------------------------------------------------------|
| _format_  | string | Especifique el formato en el que debe descargarse el contenido del elemento. |


### <a name="format-options"></a>Opciones de formato

Los siguientes valores son válidos para el parámetro **format** :

| Valor de formato | Descripción                        | Extensiones de origen compatibles
|:-------------|:-----------------------------------|----------------------------
| pdf          | Convierte el elemento en formato PDF. | csv, doc, docx, odp, ods, odt, pot, potm, potx, pps, ppsx, ppsxm, ppt, pptm, pptx, rtf, xls, xlsx

## <a name="optional-request-headers"></a>Encabezados de solicitud opcionales

| Nombre            | Valor   | Descripción                                                                                                                                              |
|:----------------|:--------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| _if-none-match_ | String  | Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada coincide con la etiqueta actual del archivo, se devuelve una respuesta `HTTP 304 Not Modified`. |

## <a name="example"></a>Ejemplo

<!-- { "blockType": "request", "name": "convert-item-content", "scopes": "files.read" } -->

```http
GET /me/drive/items/{item-id}/content?format={format}
```

## <a name="response"></a>Respuesta

Devuelve una respuesta `302 Found` que redirige a una dirección URL de descarga autenticada previamente para el archivo convertido.

Para descargar el archivo convertido, la aplicación debe seguir el encabezado `Location` de la respuesta.

Las URL autenticadas previamente solo son válidas durante un breve período de tiempo (unos minutos) y no requieren un encabezado `Authorization` para tener acceso a ellas.

<!-- { "blockType": "response", "@odata.type": "stream" } -->

```http
HTTP/1.1 302 Found
Location: https://b0mpua-by3301.files.1drv.com/y23vmagahszhxzlcvhasdhasghasodfi
```

### <a name="error-responses"></a>Respuestas de error

Vea [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.

[error-response]: /graph/errors
[file-facet]: ../resources/file.md

<!-- {
  "type": "#page.annotation",
  "description": "Convert the contents of an item in OneDrive to a different format.",
  "keywords": "convert,pdf,convert to pdf",
  "section": "documentation",
  "tocPath": "Items/Download formats"
} -->
