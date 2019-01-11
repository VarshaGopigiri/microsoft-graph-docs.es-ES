---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Convertir a otros formatos
localization_priority: Normal
ms.openlocfilehash: d27420153a295eac9d3f880910d63bd701525427
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27887440"
---
# <a name="download-a-file-in-another-format"></a><span data-ttu-id="84e4f-102">Descargar un archivo en otro formato</span><span class="sxs-lookup"><span data-stu-id="84e4f-102">Download a file in another format</span></span>

> <span data-ttu-id="84e4f-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="84e4f-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="84e4f-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="84e4f-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="84e4f-105">Use esta API para recuperar el contenido de un elemento en un formato determinado.</span><span class="sxs-lookup"><span data-stu-id="84e4f-105">Use this API to retrieve the contents of an item in a specific format.</span></span>
<span data-ttu-id="84e4f-106">No todos los archivos pueden convertirse a todos los formatos.</span><span class="sxs-lookup"><span data-stu-id="84e4f-106">Not all files can be converted into all formats.</span></span>

<span data-ttu-id="84e4f-107">Para descargar el elemento en su formato original, vea [Descargar contenido de un elemento](driveitem-get-content.md).</span><span class="sxs-lookup"><span data-stu-id="84e4f-107">To download the item in its original format, see [download an item's contents](driveitem-get-content.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="84e4f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="84e4f-108">Prerequisites</span></span>

<span data-ttu-id="84e4f-109">Para llamar a esta API, al usuario se le debe haber concedido el acceso de lectura de la aplicación al archivo que la aplicación quiere convertir.</span><span class="sxs-lookup"><span data-stu-id="84e4f-109">To call this API, the user must have granted the application read access to the file the app wishes to convert.</span></span>

## <a name="http-request"></a><span data-ttu-id="84e4f-110">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="84e4f-110">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /drive/items/{item-id}/content?format={format}
GET /drive/root:/{path and filename}:/content?format={format}
```

## <a name="query-parameters"></a><span data-ttu-id="84e4f-111">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="84e4f-111">Query parameters</span></span>

| <span data-ttu-id="84e4f-112">Parámetro</span><span class="sxs-lookup"><span data-stu-id="84e4f-112">Parameter</span></span>      | <span data-ttu-id="84e4f-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="84e4f-113">Type</span></span>  | <span data-ttu-id="84e4f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="84e4f-114">Description</span></span>                                                    |
|:----------|:-------|:---------------------------------------------------------------|
| <span data-ttu-id="84e4f-115">_format_</span><span class="sxs-lookup"><span data-stu-id="84e4f-115">_format_</span></span>  | <span data-ttu-id="84e4f-116">string</span><span class="sxs-lookup"><span data-stu-id="84e4f-116">string</span></span> | <span data-ttu-id="84e4f-117">Especifique el formato en el que debe descargarse el contenido del elemento.</span><span class="sxs-lookup"><span data-stu-id="84e4f-117">Specify the format the item's content should be downloaded as.</span></span> |


<span data-ttu-id="84e4f-118">Los siguientes valores son válidos para el parámetro **format** :</span><span class="sxs-lookup"><span data-stu-id="84e4f-118">The following values are valid for the **format** parameter:</span></span>

| <span data-ttu-id="84e4f-119">Valor</span><span class="sxs-lookup"><span data-stu-id="84e4f-119">Value</span></span> | <span data-ttu-id="84e4f-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="84e4f-120">Description</span></span>                        | <span data-ttu-id="84e4f-121">Extensiones de origen compatibles</span><span class="sxs-lookup"><span data-stu-id="84e4f-121">Supported source extensions</span></span>
|:------|:-----------------------------------|---------------------------------
| <span data-ttu-id="84e4f-122">GLB</span><span class="sxs-lookup"><span data-stu-id="84e4f-122">glb</span></span>   | <span data-ttu-id="84e4f-123">Convierte el elemento en formato GLB</span><span class="sxs-lookup"><span data-stu-id="84e4f-123">Converts the item into GLB format</span></span>  | <span data-ttu-id="84e4f-124">interesante, fbx, obj, hoja, stl, 3mf</span><span class="sxs-lookup"><span data-stu-id="84e4f-124">cool, fbx, obj, ply, stl, 3mf</span></span>
| <span data-ttu-id="84e4f-125">html</span><span class="sxs-lookup"><span data-stu-id="84e4f-125">html</span></span>  | <span data-ttu-id="84e4f-126">Convierte el elemento en formato HTML</span><span class="sxs-lookup"><span data-stu-id="84e4f-126">Converts the item into HTML format</span></span> | <span data-ttu-id="84e4f-127">EML, md, msg</span><span class="sxs-lookup"><span data-stu-id="84e4f-127">eml, md, msg</span></span>
| <span data-ttu-id="84e4f-128">jpg</span><span class="sxs-lookup"><span data-stu-id="84e4f-128">jpg</span></span>   | <span data-ttu-id="84e4f-129">Convierte el elemento en formato JPG</span><span class="sxs-lookup"><span data-stu-id="84e4f-129">Converts the item into JPG format</span></span>  | <span data-ttu-id="84e4f-130">3g 2, 3gp, 3gp2, 3gpp, 3mf, ai, arw, asf, avi, bas, fiesta, bat, bmp, c, cbl, cmd, interesante, cpp, cr2, crw, cs, css, csv, actual, dcm, dcm30, dic, dicm, dicom, dng, doc, docx, dwg, eml, epi, eps, epsf, epsi, epub, erf, fbx, fppx, gif, glb, h, hcp , heic, heif, htm, html, ico, icono, java, jfif, jpeg, jpg, js, json, clave, registro, m2ts, m4a, m4v, descuento, md, mef, mov, movie, mp3, mp4, mp4v, mrw, msg, mts, nef, nrw, números, obj, ODT, odt, ogg, orf, páginas, panorámico, pdf, pef, php, pict, pl, hoja, png, pot , potm, potx, pps, ppsx, ppsxm, ppt, pptm, pptx, ps, ps1, psb, psd, copiar, sin procesar, rb, rtf, rw1, rw2, sh, esboce, sql, sr2, stl, tif, tiff, ts, txt, vb, WBEM, wma, wmv, xaml, xbm, xcf, xd, xml, xpm, yaml, yml</span><span class="sxs-lookup"><span data-stu-id="84e4f-130">3g2, 3gp, 3gp2, 3gpp, 3mf, ai, arw, asf, avi, bas, bash, bat, bmp, c, cbl, cmd, cool, cpp, cr2, crw, cs, css, csv, cur, dcm, dcm30, dic, dicm, dicom, dng, doc, docx, dwg, eml, epi, eps, epsf, epsi, epub, erf, fbx, fppx, gif, glb, h, hcp, heic, heif, htm, html, ico, icon, java, jfif, jpeg, jpg, js, json, key, log, m2ts, m4a, m4v, markdown, md, mef, mov, movie, mp3, mp4, mp4v, mrw, msg, mts, nef, nrw, numbers, obj, odp, odt, ogg, orf, pages, pano, pdf, pef, php, pict, pl, ply, png, pot, potm, potx, pps, ppsx, ppsxm, ppt, pptm, pptx, ps, ps1, psb, psd, py, raw, rb, rtf, rw1, rw2, sh, sketch, sql, sr2, stl, tif, tiff, ts, txt, vb, webm, wma, wmv, xaml, xbm, xcf, xd, xml, xpm, yaml, yml</span></span>
| <span data-ttu-id="84e4f-131">PDF</span><span class="sxs-lookup"><span data-stu-id="84e4f-131">pdf</span></span>   | <span data-ttu-id="84e4f-132">Convierte el elemento en formato PDF</span><span class="sxs-lookup"><span data-stu-id="84e4f-132">Converts the item into PDF format</span></span>  | <span data-ttu-id="84e4f-133">doc, docx, epub, eml, htm, html, md, msg, ODT, ods, odt, pps, ppsx, ppt, pptx, rtf, tif, tiff, xls, xlsm, xlsx</span><span class="sxs-lookup"><span data-stu-id="84e4f-133">doc, docx, epub, eml, htm, html, md, msg, odp, ods, odt, pps, ppsx, ppt, pptx, rtf, tif, tiff, xls, xlsm, xlsx</span></span>

## <a name="optional-request-headers"></a><span data-ttu-id="84e4f-134">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="84e4f-134">Optional request headers</span></span>

| <span data-ttu-id="84e4f-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="84e4f-135">Name</span></span>            | <span data-ttu-id="84e4f-136">Valor</span><span class="sxs-lookup"><span data-stu-id="84e4f-136">Value</span></span>   | <span data-ttu-id="84e4f-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="84e4f-137">Description</span></span>                                                                                                                                              |
|:----------------|:--------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84e4f-138">_if-none-match_</span><span class="sxs-lookup"><span data-stu-id="84e4f-138">_if-none-match_</span></span> | <span data-ttu-id="84e4f-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="84e4f-139">String</span></span>  | <span data-ttu-id="84e4f-140">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada coincide con la etiqueta actual del archivo, se devuelve una respuesta `HTTP 304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="84e4f-140">If this request header is included and the eTag (or cTag) provided matches the current tag on the file, an `HTTP 304 Not Modified` response is returned.</span></span> |

## <a name="example"></a><span data-ttu-id="84e4f-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84e4f-141">Example</span></span>

<!-- { "blockType": "request", "name": "convert-item-content", "scopes": "files.read" } -->

```http
GET /drive/items/{item-id}/content?format={format}
```

## <a name="response"></a><span data-ttu-id="84e4f-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="84e4f-142">Response</span></span>

<span data-ttu-id="84e4f-143">Devuelve una respuesta `302 Found` que redirige a una dirección URL de descarga autenticada previamente para el archivo convertido.</span><span class="sxs-lookup"><span data-stu-id="84e4f-143">Returns a `302 Found` response redirecting to a pre-authenticated download URL for the converted file.</span></span>

<span data-ttu-id="84e4f-144">Para descargar el archivo convertido, la aplicación debe seguir el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="84e4f-144">To download the converted file, your app must follow the `Location` header in the response.</span></span>

<span data-ttu-id="84e4f-145">Las URL autenticadas previamente solo son válidas durante un breve período de tiempo (unos minutos) y no requieren un encabezado `Authorization` para tener acceso a ellas.</span><span class="sxs-lookup"><span data-stu-id="84e4f-145">Pre-authenticated URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header to access.</span></span>

<!-- { "blockType": "response", "@odata.type": "stream" } -->

```http
HTTP/1.1 302 Found
Location: https://b0mpua-by3301.files.1drv.com/y23vmagahszhxzlcvhasdhasghasodfi
```

### <a name="error-responses"></a><span data-ttu-id="84e4f-146">Respuestas de error</span><span class="sxs-lookup"><span data-stu-id="84e4f-146">Error responses</span></span>

<span data-ttu-id="84e4f-147">Vea [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="84e4f-147">See [Error Responses][error-response] for more information about how errors are returned.</span></span>

[error-response]: /graph/errors
[file-facet]: ../resources/file.md

<!-- {
  "type": "#page.annotation",
  "description": "Convert the contents of an item in OneDrive to a different format.",
  "keywords": "convert,pdf,convert to pdf",
  "section": "documentation",
  "tocPath": "Items/Download formats"
} -->
