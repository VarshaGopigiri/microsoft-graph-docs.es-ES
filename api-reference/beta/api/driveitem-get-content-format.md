---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Convertir a otros formatos
ms.openlocfilehash: 70558e7c0497c71f620481ff67b7d07cc255cd95
ms.sourcegitcommit: 12c6e82f1417022540e534ebadbd0e8d7fb5abde
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/08/2018
ms.locfileid: "27209722"
---
# <a name="download-a-file-in-another-format"></a>Descargar un archivo en otro formato

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

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


Los siguientes valores son válidos para el parámetro **format** :

| Valor | Descripción                        | Extensiones de origen compatibles
|:------|:-----------------------------------|---------------------------------
| GLB   | Convierte el elemento en formato GLB  | interesante, fbx, obj, hoja, stl, 3mf
| html  | Convierte el elemento en formato HTML | EML, md, msg
| jpg   | Convierte el elemento en formato JPG  | 3g 2, 3gp, 3gp2, 3gpp, 3mf, ai, arw, asf, avi, bas, fiesta, bat, bmp, c, cbl, cmd, interesante, cpp, cr2, crw, cs, css, csv, actual, dcm, dcm30, dic, dicm, dicom, dng, doc, docx, dwg, eml, epi, eps, epsf, epsi, epub, erf, fbx, fppx, gif, glb, h, hcp , heic, heif, htm, html, ico, icono, java, jfif, jpeg, jpg, js, json, clave, registro, m2ts, m4a, m4v, descuento, md, mef, mov, movie, mp3, mp4, mp4v, mrw, msg, mts, nef, nrw, números, obj, ODT, odt, ogg, orf, páginas, panorámico, pdf, pef, php, pict, pl, hoja, png, pot , potm, potx, pps, ppsx, ppsxm, ppt, pptm, pptx, ps, ps1, psb, psd, copiar, sin procesar, rb, rtf, rw1, rw2, sh, esboce, sql, sr2, stl, tif, tiff, ts, txt, vb, WBEM, wma, wmv, xaml, xbm, xcf, xd, xml, xpm, yaml, yml
| PDF   | Convierte el elemento en formato PDF  | doc, docx, epub, eml, htm, html, md, msg, ODT, ods, odt, pps, ppsx, ppt, pptx, rtf, tif, tiff, xls, xlsm, xlsx

## <a name="optional-request-headers"></a>Encabezados de solicitud opcionales

| Nombre            | Valor   | Descripción                                                                                                                                              |
|:----------------|:--------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| _if-none-match_ | String  | Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada coincide con la etiqueta actual del archivo, se devuelve una respuesta `HTTP 304 Not Modified`. |

## <a name="example"></a>Ejemplo

<!-- { "blockType": "request", "name": "convert-item-content", "scopes": "files.read" } -->

```http
GET /drive/items/{item-id}/content?format={format}
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
