---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Convertir a otros formatos
ms.openlocfilehash: f3dfe3b01cac66754b9a8151a2bb46adee157741
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029867"
---
# <a name="download-a-file-in-another-format"></a><span data-ttu-id="ddaa2-102">Descargar un archivo en otro formato</span><span class="sxs-lookup"><span data-stu-id="ddaa2-102">Download a file in another format</span></span>

<span data-ttu-id="ddaa2-103">Use esta API para recuperar el contenido de un elemento en un formato determinado.</span><span class="sxs-lookup"><span data-stu-id="ddaa2-103">Use this API to retrieve the contents of an item in a specific format.</span></span>
<span data-ttu-id="ddaa2-104">No todos los archivos pueden convertirse a todos los formatos.</span><span class="sxs-lookup"><span data-stu-id="ddaa2-104">Not all files can be converted into all formats.</span></span>

<span data-ttu-id="ddaa2-105">Para descargar el elemento en su formato original, vea [descargar el contenido de un elemento](driveitem-get-content.md).</span><span class="sxs-lookup"><span data-stu-id="ddaa2-105">To download the item in it's original format, see [download an item's contents](driveitem-get-content.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ddaa2-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ddaa2-106">Prerequisites</span></span>

<span data-ttu-id="ddaa2-107">Para llamar a esta API, al usuario se le debe haber concedido el acceso de lectura de la aplicación al archivo que la aplicación quiere convertir.</span><span class="sxs-lookup"><span data-stu-id="ddaa2-107">To call this API, the user must have granted the application read access to the file the app wishes to convert.</span></span>

## <a name="http-request"></a><span data-ttu-id="ddaa2-108">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ddaa2-108">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /drive/items/{item-id}/content?format={format}
GET /drive/root:/{path and filename}:/content?format={format}
```

## <a name="query-parameters"></a><span data-ttu-id="ddaa2-109">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="ddaa2-109">Query parameters</span></span>

| <span data-ttu-id="ddaa2-110">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ddaa2-110">Parameter</span></span>      | <span data-ttu-id="ddaa2-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="ddaa2-111">Type</span></span>  | <span data-ttu-id="ddaa2-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddaa2-112">Description</span></span>                                                    |
|:----------|:-------|:---------------------------------------------------------------|
| <span data-ttu-id="ddaa2-113">_format_</span><span class="sxs-lookup"><span data-stu-id="ddaa2-113">_format_</span></span>  | <span data-ttu-id="ddaa2-114">string</span><span class="sxs-lookup"><span data-stu-id="ddaa2-114">string</span></span> | <span data-ttu-id="ddaa2-115">Especifique el formato en el que debe descargarse el contenido del elemento.</span><span class="sxs-lookup"><span data-stu-id="ddaa2-115">Specify the format the item's content should be downloaded as.</span></span> |


### <a name="format-options"></a><span data-ttu-id="ddaa2-116">Opciones de formato</span><span class="sxs-lookup"><span data-stu-id="ddaa2-116">Format options</span></span>

<span data-ttu-id="ddaa2-117">Los siguientes valores son válidos para el parámetro **format** :</span><span class="sxs-lookup"><span data-stu-id="ddaa2-117">The following values are valid for the **format** parameter:</span></span>

| <span data-ttu-id="ddaa2-118">Valor de formato</span><span class="sxs-lookup"><span data-stu-id="ddaa2-118">Format value</span></span> | <span data-ttu-id="ddaa2-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddaa2-119">Description</span></span>                        | <span data-ttu-id="ddaa2-120">Extensiones de origen compatibles</span><span class="sxs-lookup"><span data-stu-id="ddaa2-120">Supported source extensions</span></span>
|:-------------|:-----------------------------------|----------------------------
| <span data-ttu-id="ddaa2-121">pdf</span><span class="sxs-lookup"><span data-stu-id="ddaa2-121">pdf</span></span>          | <span data-ttu-id="ddaa2-122">Convierte el elemento en formato PDF.</span><span class="sxs-lookup"><span data-stu-id="ddaa2-122">Converts the item into PDF format.</span></span> | <span data-ttu-id="ddaa2-123">csv, doc, docx, odp, ods, odt, pot, potm, potx, pps, ppsx, ppsxm, ppt, pptm, pptx, rtf, xls, xlsx</span><span class="sxs-lookup"><span data-stu-id="ddaa2-123">csv, doc, docx, odp, ods, odt, pot, potm, potx, pps, ppsx, ppsxm, ppt, pptm, pptx, rtf, xls, xlsx</span></span>

## <a name="optional-request-headers"></a><span data-ttu-id="ddaa2-124">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="ddaa2-124">Optional request headers</span></span>

| <span data-ttu-id="ddaa2-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="ddaa2-125">Name</span></span>            | <span data-ttu-id="ddaa2-126">Valor</span><span class="sxs-lookup"><span data-stu-id="ddaa2-126">Value</span></span>   | <span data-ttu-id="ddaa2-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddaa2-127">Description</span></span>                                                                                                                                              |
|:----------------|:--------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddaa2-128">_if-none-match_</span><span class="sxs-lookup"><span data-stu-id="ddaa2-128">_if-none-match_</span></span> | <span data-ttu-id="ddaa2-129">String</span><span class="sxs-lookup"><span data-stu-id="ddaa2-129">String</span></span>  | <span data-ttu-id="ddaa2-130">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada coincide con la etiqueta actual del archivo, se devuelve una respuesta `HTTP 304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="ddaa2-130">If this request header is included and the eTag (or cTag) provided matches the current tag on the file, an `HTTP 304 Not Modified` response is returned.</span></span> |

## <a name="example"></a><span data-ttu-id="ddaa2-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ddaa2-131">Example</span></span>

<!-- { "blockType": "request", "name": "convert-item-content", "scopes": "files.read" } -->

```http
GET /me/drive/items/{item-id}/content?format={format}
```

## <a name="response"></a><span data-ttu-id="ddaa2-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ddaa2-132">Response</span></span>

<span data-ttu-id="ddaa2-133">Devuelve una respuesta `302 Found` que redirige a una dirección URL de descarga autenticada previamente para el archivo convertido.</span><span class="sxs-lookup"><span data-stu-id="ddaa2-133">Returns a `302 Found` response redirecting to a pre-authenticated download URL for the converted file.</span></span>

<span data-ttu-id="ddaa2-134">Para descargar el archivo convertido, la aplicación debe seguir el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ddaa2-134">To download the converted file, your app must follow the `Location` header in the response.</span></span>

<span data-ttu-id="ddaa2-135">Las URL autenticadas previamente solo son válidas durante un breve período de tiempo (unos minutos) y no requieren un encabezado `Authorization` para tener acceso a ellas.</span><span class="sxs-lookup"><span data-stu-id="ddaa2-135">Pre-authenticated URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header to access.</span></span>

<!-- { "blockType": "response", "@odata.type": "stream" } -->

```http
HTTP/1.1 302 Found
Location: https://b0mpua-by3301.files.1drv.com/y23vmagahszhxzlcvhasdhasghasodfi
```

### <a name="error-responses"></a><span data-ttu-id="ddaa2-136">Respuestas de error</span><span class="sxs-lookup"><span data-stu-id="ddaa2-136">Error responses</span></span>

<span data-ttu-id="ddaa2-137">Vea [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="ddaa2-137">See [Error Responses][error-response] for more info about how errors are returned.</span></span>

[error-response]: /graph/errors
[file-facet]: ../resources/file.md

<!-- {
  "type": "#page.annotation",
  "description": "Convert the contents of an item in OneDrive to a different format.",
  "keywords": "convert,pdf,convert to pdf",
  "section": "documentation",
  "tocPath": "Items/Download formats"
} -->