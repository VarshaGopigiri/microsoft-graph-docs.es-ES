---
title: Tipo de recurso OneNoteResource
description: 'Imagen u otro recurso de archivo en una página de OneNote. '
localization_priority: Normal
ms.openlocfilehash: ed2fb0dd4b6e68c24da1f2441a157f734a5025f6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27855107"
---
# <a name="onenoteresource-resource-type"></a><span data-ttu-id="e24dd-103">Tipo de recurso OneNoteResource</span><span class="sxs-lookup"><span data-stu-id="e24dd-103">OneNoteResource resource type</span></span>

<span data-ttu-id="e24dd-104">Imagen u otro recurso de archivo en una página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="e24dd-104">An image or other file resource on a OneNote page.</span></span> 

<span data-ttu-id="e24dd-105">Puede obtener los datos binarios de un recurso, pero no puede obtener una representación JSON de un objeto de recurso o una colección de recursos.</span><span class="sxs-lookup"><span data-stu-id="e24dd-105">You can get the binary data of a resource, but getting a JSON representation of a resource object or a resource collection is not supported.</span></span>

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.onenoteEntityBaseModel",
  "optionalProperties": [],
  "isMediaEntity": true,
  "@odata.type": "microsoft.graph.onenoteResource"
}-->

```json
{
  "content": { "@odata.type": "Edm.Stream" },
  "contentUrl": "string (url)"
}
```

<span data-ttu-id="e24dd-106">Obtenga los datos binarios de un recurso específico enviando una solicitud GET al punto de conexión `content` del recurso:</span><span class="sxs-lookup"><span data-stu-id="e24dd-106">Get the binary data of a specific resource by sending a GET request to the resource's `content` endpoint:</span></span>

```
GET ../onenote/resources/{id}/content
```

<span data-ttu-id="e24dd-107">El URI de recurso del archivo se devuelve al obtener el contenido HTML de una página mediante la siguiente solicitud:</span><span class="sxs-lookup"><span data-stu-id="e24dd-107">The file's resource URI is returned when you get a page's HTML content using the following request:</span></span>

```
GET ../onenote/pages/{id}/content
```

<span data-ttu-id="e24dd-108">En la página HTML, la etiqueta `img` incluye puntos de conexión del recurso de imagen original en el atributo `data-fullres-src` y de la imagen optimizada en el atributo `src`:</span><span class="sxs-lookup"><span data-stu-id="e24dd-108">In the page HTML, an `img` tag includes endpoints for the original image resource in the `data-fullres-src` attribute and the optimized image in the `src` attribute:</span></span>
```
<img 
    src="image-resource-url"  
    data-src-type="media-type"
    data-fullres-src="image-resource-url"  
    data-fullres-src-type="media-type" ... />
```

<span data-ttu-id="e24dd-109">La etiqueta `object` (que representa archivos como PDF, DOCX y PNG) incluye el punto de conexión del recurso de archivo en el atributo `data`:</span><span class="sxs-lookup"><span data-stu-id="e24dd-109">An `object` tag (which represents files such as PDF, DOCX, and PNG) includes the endpoint for the file resource in the `data` attribute:</span></span>

```
<object
    data="file-resource-url"
    data-attachment="file-name.file-type" 
    type="media-type" ... />
```

## <a name="properties"></a><span data-ttu-id="e24dd-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e24dd-110">Properties</span></span>

| <span data-ttu-id="e24dd-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e24dd-111">Property</span></span>             | <span data-ttu-id="e24dd-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="e24dd-112">Type</span></span>            | <span data-ttu-id="e24dd-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="e24dd-113">Description</span></span>
|:---------------------|:----------------|:---------------------------------
| <span data-ttu-id="e24dd-114">content</span><span class="sxs-lookup"><span data-stu-id="e24dd-114">content</span></span>              | <span data-ttu-id="e24dd-115">Stream</span><span class="sxs-lookup"><span data-stu-id="e24dd-115">Stream</span></span>          | <span data-ttu-id="e24dd-116">La secuencia de contenido</span><span class="sxs-lookup"><span data-stu-id="e24dd-116">The content stream</span></span>
| <span data-ttu-id="e24dd-117">contentUrl</span><span class="sxs-lookup"><span data-stu-id="e24dd-117">contentUrl</span></span>           | <span data-ttu-id="e24dd-118">Cadena (dirección url)</span><span class="sxs-lookup"><span data-stu-id="e24dd-118">String (url)</span></span>    | <span data-ttu-id="e24dd-119">La dirección URL para descargar el contenido</span><span class="sxs-lookup"><span data-stu-id="e24dd-119">The URL for downloading the content</span></span>

## <a name="relationships"></a><span data-ttu-id="e24dd-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e24dd-120">Relationships</span></span>
<span data-ttu-id="e24dd-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e24dd-121">None.</span></span>


## <a name="methods"></a><span data-ttu-id="e24dd-122">Métodos</span><span class="sxs-lookup"><span data-stu-id="e24dd-122">Methods</span></span>
| <span data-ttu-id="e24dd-123">Método</span><span class="sxs-lookup"><span data-stu-id="e24dd-123">Method</span></span>           | <span data-ttu-id="e24dd-124">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e24dd-124">Return Type</span></span>    |<span data-ttu-id="e24dd-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="e24dd-125">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="e24dd-126">Obtener datos binarios de recursos</span><span class="sxs-lookup"><span data-stu-id="e24dd-126">Get resource binary data</span></span>](../api/resource-get.md) | <span data-ttu-id="e24dd-127">Secuencia</span><span class="sxs-lookup"><span data-stu-id="e24dd-127">Stream</span></span> |<span data-ttu-id="e24dd-128">Recuperar los datos binarios de un recurso de archivo o imagen.</span><span class="sxs-lookup"><span data-stu-id="e24dd-128">Retrieve the binary data of a file or image resource.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "resource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
