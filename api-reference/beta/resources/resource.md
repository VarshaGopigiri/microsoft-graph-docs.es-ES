---
title: Tipo de recurso resource
description: 'Imagen u otro recurso de archivo en una página de OneNote. '
ms.openlocfilehash: 8e0e049cab613c7c1a72c8c96e21bac77c507ae1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088892"
---
# <a name="resource-resource-type"></a><span data-ttu-id="eda1c-103">Tipo de recurso resource</span><span class="sxs-lookup"><span data-stu-id="eda1c-103">resource resource type</span></span>

> <span data-ttu-id="eda1c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="eda1c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="eda1c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="eda1c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="eda1c-106">Imagen u otro recurso de archivo en una página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="eda1c-106">An image or other file resource on a OneNote page.</span></span> 

<span data-ttu-id="eda1c-107">Puede obtener los datos binarios de un recurso, pero no puede obtener una representación JSON de un objeto de recurso o una colección de recursos.</span><span class="sxs-lookup"><span data-stu-id="eda1c-107">You can get the binary data of a resource, but getting a JSON representation of a resource object or a resource collection is not supported.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onenoteResource"
}-->

<span data-ttu-id="eda1c-108">Obtenga los datos binarios de un recurso específico enviando una solicitud GET al punto de conexión `content` del recurso:</span><span class="sxs-lookup"><span data-stu-id="eda1c-108">Get the binary data of a specific resource by sending a GET request to the resource's `content` endpoint:</span></span>

```
GET ../onenote/resources/{id}/content
```

<span data-ttu-id="eda1c-109">El URI de recurso del archivo se devuelve al obtener el contenido HTML de una página mediante la siguiente solicitud:</span><span class="sxs-lookup"><span data-stu-id="eda1c-109">The file's resource URI is returned when you get a page's HTML content using the following request:</span></span>

```
GET ../onenote/pages/{id}/content
```

<span data-ttu-id="eda1c-110">En la página HTML, la etiqueta `img` incluye puntos de conexión del recurso de imagen original en el atributo `data-fullres-src` y de la imagen optimizada en el atributo `src`:</span><span class="sxs-lookup"><span data-stu-id="eda1c-110">In the page HTML, an `img` tag includes endpoints for the original image resource in the `data-fullres-src` attribute and the optimized image in the `src` attribute:</span></span>
```
<img 
    src="image-resource-url"  
    data-src-type="media-type"
    data-fullres-src="image-resource-url"  
    data-fullres-src-type="media-type" ... />
```

<span data-ttu-id="eda1c-111">La etiqueta `object` (que representa archivos como PDF, DOCX y PNG) incluye el punto de conexión del recurso de archivo en el atributo `data`:</span><span class="sxs-lookup"><span data-stu-id="eda1c-111">An `object` tag (which represents files such as PDF, DOCX, and PNG) includes the endpoint for the file resource in the `data` attribute:</span></span>

```
<object
    data="file-resource-url"
    data-attachment="file-name.file-type" 
    type="media-type" ... />
```

## <a name="properties"></a><span data-ttu-id="eda1c-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eda1c-112">Properties</span></span>
<span data-ttu-id="eda1c-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="eda1c-113">None.</span></span>

## <a name="relationships"></a><span data-ttu-id="eda1c-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="eda1c-114">Relationships</span></span>
<span data-ttu-id="eda1c-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="eda1c-115">None.</span></span>


## <a name="methods"></a><span data-ttu-id="eda1c-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="eda1c-116">Methods</span></span>
| <span data-ttu-id="eda1c-117">Método</span><span class="sxs-lookup"><span data-stu-id="eda1c-117">Method</span></span>           | <span data-ttu-id="eda1c-118">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eda1c-118">Return Type</span></span>    |<span data-ttu-id="eda1c-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="eda1c-119">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="eda1c-120">Obtener datos binarios de recursos</span><span class="sxs-lookup"><span data-stu-id="eda1c-120">Get resource binary data</span></span>](../api/resource-get.md) | <span data-ttu-id="eda1c-121">Secuencia</span><span class="sxs-lookup"><span data-stu-id="eda1c-121">Stream</span></span> |<span data-ttu-id="eda1c-122">Recuperar los datos binarios de un recurso de archivo o imagen.</span><span class="sxs-lookup"><span data-stu-id="eda1c-122">Retrieve the binary data of a file or image resource.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "resource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->