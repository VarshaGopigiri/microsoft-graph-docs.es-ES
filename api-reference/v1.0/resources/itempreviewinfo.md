---
author: kevinlam
ms.author: kevinlam
ms.date: 3/16/2018
title: ItemPreviewInfo
ms.openlocfilehash: 8b8f7a962e237cc20a42503efd31f083996ad715
ms.sourcegitcommit: ebac77d2ca32438e552831de0258fe5e86fa225a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/17/2018
ms.locfileid: "26606530"
---
# <a name="itempreviewinfo-resource-type"></a><span data-ttu-id="e2985-102">tipo de recurso itemPreviewInfo</span><span class="sxs-lookup"><span data-stu-id="e2985-102">itemPreviewInfo resource type</span></span>

<span data-ttu-id="e2985-103">El recurso **itemPreviewInfo** contiene información acerca de cómo incrustar una vista previa de una [driveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="e2985-103">The **itemPreviewInfo** resource contains information on how to embed a preview of a [driveItem](driveitem.md).</span></span>

## <a name="json-representation"></a><span data-ttu-id="e2985-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e2985-104">JSON representation</span></span>

```json
{
    "getUrl": "https://www.onedrive.com/embed?foo=bar&bar=baz",
    "postParameters": "param1=value&param2=another%20value",
    "postUrl": "https://www.onedrive.com/embed_by_post"
}
```

## <a name="properties"></a><span data-ttu-id="e2985-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e2985-105">Properties</span></span>

| <span data-ttu-id="e2985-106">Nombre</span><span class="sxs-lookup"><span data-stu-id="e2985-106">Name</span></span>           | <span data-ttu-id="e2985-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="e2985-107">Type</span></span>   | <span data-ttu-id="e2985-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2985-108">Description</span></span>
|:---------------|:-------|:---------------------------------------------------
| <span data-ttu-id="e2985-109">getUrl</span><span class="sxs-lookup"><span data-stu-id="e2985-109">getUrl</span></span>         | <span data-ttu-id="e2985-110">string</span><span class="sxs-lookup"><span data-stu-id="e2985-110">string</span></span> | <span data-ttu-id="e2985-111">Dirección URL adecuada para incrustar mediante HTTP GET (IFRAME, etcetera).</span><span class="sxs-lookup"><span data-stu-id="e2985-111">URL suitable for embedding using HTTP GET (iframes, etc.)</span></span>
| <span data-ttu-id="e2985-112">URL para exponer</span><span class="sxs-lookup"><span data-stu-id="e2985-112">postUrl</span></span>        | <span data-ttu-id="e2985-113">string</span><span class="sxs-lookup"><span data-stu-id="e2985-113">string</span></span> | <span data-ttu-id="e2985-114">Dirección URL adecuada para incrustar el uso de HTTP POST (de envío de formulario, JS, etcetera.)</span><span class="sxs-lookup"><span data-stu-id="e2985-114">URL suitable for embedding using HTTP POST (form post, JS, etc.)</span></span>
| <span data-ttu-id="e2985-115">postParameters</span><span class="sxs-lookup"><span data-stu-id="e2985-115">postParameters</span></span> | <span data-ttu-id="e2985-116">string</span><span class="sxs-lookup"><span data-stu-id="e2985-116">string</span></span> | <span data-ttu-id="e2985-117">Parámetros de entrada para incluir si usa URL para exponer</span><span class="sxs-lookup"><span data-stu-id="e2985-117">POST parameters to include if using postUrl</span></span>

<span data-ttu-id="e2985-118">Según el estado actual de compatibilidad con las opciones especificadas, se pueden devolver getUrl, URL para exponer o ambos.</span><span class="sxs-lookup"><span data-stu-id="e2985-118">Either getUrl, postUrl, or both may be returned depending on the current state of support for the specified options.</span></span>

<span data-ttu-id="e2985-119">postParameters es una cadena con formato como `application/x-www-form-urlencoded`, y si se realiza una entrada a la URL para exponer el tipo de contenido se debe establecer en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="e2985-119">postParameters is a string formatted as `application/x-www-form-urlencoded`, and if performing a POST to the postUrl the content-type should be set accordingly.</span></span> <span data-ttu-id="e2985-120">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e2985-120">For example:</span></span>
```
POST https://www.onedrive.com/embed_by_post
Content-Type: application/x-www-form-urlencoded

param1=value&param2=another%20value
```

<span data-ttu-id="e2985-121">Los formatos de direcciones URL y los parámetros deben considerarse opacos.</span><span class="sxs-lookup"><span data-stu-id="e2985-121">The formats of URLs and parameters should be considered opaque.</span></span>
