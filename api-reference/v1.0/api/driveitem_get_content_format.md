---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Convertir a otros formatos
ms.openlocfilehash: 3031500beaec2d765075abfd925a6333f50368f9
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="download-a-file-in-another-format"></a><span data-ttu-id="7d3fb-102">Descargar un archivo en otro formato</span><span class="sxs-lookup"><span data-stu-id="7d3fb-102">Download a file in another format</span></span>

<span data-ttu-id="7d3fb-103">Use esta API para recuperar el contenido de un elemento en un formato determinado.</span><span class="sxs-lookup"><span data-stu-id="7d3fb-103">Use this API to retrieve the contents of an item in a specific format.</span></span>
<span data-ttu-id="7d3fb-104">No todos los archivos pueden convertirse a todos los formatos.</span><span class="sxs-lookup"><span data-stu-id="7d3fb-104">Not all files can be converted into all formats.</span></span>

<span data-ttu-id="7d3fb-105">Para descargar el elemento en su formato original, vea [descargar el contenido de un elemento](driveitem_get_content.md).</span><span class="sxs-lookup"><span data-stu-id="7d3fb-105">To download the item in it's original format, see [download an item's contents](driveitem_get_content.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7d3fb-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7d3fb-106">Prerequisites</span></span>

<span data-ttu-id="7d3fb-107">Para llamar a esta API, al usuario se le debe haber concedido el acceso de lectura de la aplicación al archivo que la aplicación quiere convertir.</span><span class="sxs-lookup"><span data-stu-id="7d3fb-107">To call this API, the user must have granted the application read access to the file the app wishes to convert.</span></span>

## <a name="http-request"></a><span data-ttu-id="7d3fb-108">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7d3fb-108">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /drive/items/{item-id}/content?format={format}
GET /drive/root:/{path and filename}:/content?format={format}
```

### <a name="optional-request-headers"></a><span data-ttu-id="7d3fb-109">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="7d3fb-109">Optional request headers</span></span>

| <span data-ttu-id="7d3fb-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="7d3fb-110">Name</span></span>            | <span data-ttu-id="7d3fb-111">Valor</span><span class="sxs-lookup"><span data-stu-id="7d3fb-111">Value</span></span>   | <span data-ttu-id="7d3fb-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d3fb-112">Description</span></span>                                                                                                                                              |
|:----------------|:--------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d3fb-113">_if-none-match_</span><span class="sxs-lookup"><span data-stu-id="7d3fb-113">_if-none-match_</span></span> | <span data-ttu-id="7d3fb-114">String</span><span class="sxs-lookup"><span data-stu-id="7d3fb-114">String</span></span>  | <span data-ttu-id="7d3fb-115">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada coincide con la etiqueta actual del archivo, se devuelve una respuesta `HTTP 304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="7d3fb-115">If this request header is included and the eTag (or cTag) provided matches the current tag on the file, an `HTTP 304 Not Modified` response is returned.</span></span> |


### <a name="query-string-parameters"></a><span data-ttu-id="7d3fb-116">Parámetros de la cadena de consulta</span><span class="sxs-lookup"><span data-stu-id="7d3fb-116">Query string parameters</span></span>

| <span data-ttu-id="7d3fb-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="7d3fb-117">Name</span></span>      | <span data-ttu-id="7d3fb-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7d3fb-118">Value</span></span>  | <span data-ttu-id="7d3fb-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d3fb-119">Description</span></span>                                                    |
|:----------|:-------|:---------------------------------------------------------------|
| <span data-ttu-id="7d3fb-120">_format_</span><span class="sxs-lookup"><span data-stu-id="7d3fb-120">_format_</span></span>  | <span data-ttu-id="7d3fb-121">string</span><span class="sxs-lookup"><span data-stu-id="7d3fb-121">string</span></span> | <span data-ttu-id="7d3fb-122">Especifique el formato en el que debe descargarse el contenido del elemento.</span><span class="sxs-lookup"><span data-stu-id="7d3fb-122">Specify the format the item's content should be downloaded as.</span></span> |


<span data-ttu-id="7d3fb-123">Los siguientes valores son válidos para el parámetro **convert**:</span><span class="sxs-lookup"><span data-stu-id="7d3fb-123">The following values are valid for the **convert** parameter:</span></span>

| <span data-ttu-id="7d3fb-124">Valor</span><span class="sxs-lookup"><span data-stu-id="7d3fb-124">Value</span></span>   | <span data-ttu-id="7d3fb-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d3fb-125">Description</span></span>                        | <span data-ttu-id="7d3fb-126">Extensiones de origen compatibles</span><span class="sxs-lookup"><span data-stu-id="7d3fb-126">Supported source extensions</span></span> |
|:--------|:-----------------------------------|-----------------------------|
| <span data-ttu-id="7d3fb-127">**pdf**</span><span class="sxs-lookup"><span data-stu-id="7d3fb-127">**pdf**</span></span> | <span data-ttu-id="7d3fb-128">Convierte el elemento en formato PDF.</span><span class="sxs-lookup"><span data-stu-id="7d3fb-128">Converts the item into PDF format.</span></span> | <span data-ttu-id="7d3fb-129">csv, doc, docx, odp, ods, odt, pot, potm, potx, pps, ppsx, ppsxm, ppt, pptm, pptx, rtf, xls, xlsx</span><span class="sxs-lookup"><span data-stu-id="7d3fb-129">csv, doc, docx, odp, ods, odt, pot, potm, potx, pps, ppsx, ppsxm, ppt, pptm, pptx, rtf, xls, xlsx</span></span> | 

### <a name="example"></a><span data-ttu-id="7d3fb-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7d3fb-130">Example</span></span>

<!-- { "blockType": "request", "name": "convert-item-content", "scopes": "files.read" } -->

```http
GET /drive/items/{item-id}/content?format={format}
```

## <a name="response"></a><span data-ttu-id="7d3fb-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7d3fb-131">Response</span></span>

<span data-ttu-id="7d3fb-132">Devuelve una respuesta `302 Found` que redirige a una dirección URL de descarga autenticada previamente para el archivo convertido.</span><span class="sxs-lookup"><span data-stu-id="7d3fb-132">Returns a `302 Found` response redirecting to a pre-authenticated download URL for the converted file.</span></span>

<span data-ttu-id="7d3fb-133">Para descargar el archivo convertido, la aplicación debe seguir el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7d3fb-133">To download the converted file, your app must follow the `Location` header in the response.</span></span>

<span data-ttu-id="7d3fb-134">Las URL autenticadas previamente solo son válidas durante un breve período de tiempo (unos minutos) y no requieren un encabezado `Authorization` para tener acceso a ellas.</span><span class="sxs-lookup"><span data-stu-id="7d3fb-134">Pre-authenticated URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header to access.</span></span>

<!-- { "blockType": "response", "@odata.type": "stream" } -->

```http
HTTP/1.1 302 Found
Location: https://b0mpua-by3301.files.1drv.com/y23vmagahszhxzlcvhasdhasghasodfi
```

### <a name="error-responses"></a><span data-ttu-id="7d3fb-135">Respuestas de error</span><span class="sxs-lookup"><span data-stu-id="7d3fb-135">Error responses</span></span>

<span data-ttu-id="7d3fb-136">Vea [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="7d3fb-136">See [Error Responses][error-response] for more info about how errors are returned.</span></span>

[error-response]: ../../../concepts/errors.md
[file-facet]: ../resources/file.md

<!-- {
  "type": "#page.annotation",
  "description": "Convert the contents of an item in OneDrive to a different format.",
  "keywords": "convert,pdf,convert to pdf",
  "section": "documentation",
  "tocPath": "Items/Download formats"
} -->
