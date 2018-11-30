---
author: kevinlam
ms.author: kevinlam
ms.date: 3/16/2018
title: ItemPreviewInfo
ms.openlocfilehash: 8b8f7a962e237cc20a42503efd31f083996ad715
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031034"
---
# <a name="itempreviewinfo-resource-type"></a><span data-ttu-id="249c3-102">tipo de recurso itemPreviewInfo</span><span class="sxs-lookup"><span data-stu-id="249c3-102">itemPreviewInfo resource type</span></span>

<span data-ttu-id="249c3-103">El recurso **itemPreviewInfo** contiene información acerca de cómo incrustar una vista previa de una [driveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="249c3-103">The **itemPreviewInfo** resource contains information on how to embed a preview of a [driveItem](driveitem.md).</span></span>

## <a name="json-representation"></a><span data-ttu-id="249c3-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="249c3-104">JSON representation</span></span>

```json
{
    "getUrl": "https://www.onedrive.com/embed?foo=bar&bar=baz",
    "postParameters": "param1=value&param2=another%20value",
    "postUrl": "https://www.onedrive.com/embed_by_post"
}
```

## <a name="properties"></a><span data-ttu-id="249c3-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="249c3-105">Properties</span></span>

| <span data-ttu-id="249c3-106">Nombre</span><span class="sxs-lookup"><span data-stu-id="249c3-106">Name</span></span>           | <span data-ttu-id="249c3-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="249c3-107">Type</span></span>   | <span data-ttu-id="249c3-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="249c3-108">Description</span></span>
|:---------------|:-------|:---------------------------------------------------
| <span data-ttu-id="249c3-109">getUrl</span><span class="sxs-lookup"><span data-stu-id="249c3-109">getUrl</span></span>         | <span data-ttu-id="249c3-110">string</span><span class="sxs-lookup"><span data-stu-id="249c3-110">string</span></span> | <span data-ttu-id="249c3-111">Dirección URL adecuada para incrustar mediante HTTP GET (IFRAME, etcetera).</span><span class="sxs-lookup"><span data-stu-id="249c3-111">URL suitable for embedding using HTTP GET (iframes, etc.)</span></span>
| <span data-ttu-id="249c3-112">URL para exponer</span><span class="sxs-lookup"><span data-stu-id="249c3-112">postUrl</span></span>        | <span data-ttu-id="249c3-113">string</span><span class="sxs-lookup"><span data-stu-id="249c3-113">string</span></span> | <span data-ttu-id="249c3-114">Dirección URL adecuada para incrustar el uso de HTTP POST (de envío de formulario, JS, etcetera.)</span><span class="sxs-lookup"><span data-stu-id="249c3-114">URL suitable for embedding using HTTP POST (form post, JS, etc.)</span></span>
| <span data-ttu-id="249c3-115">postParameters</span><span class="sxs-lookup"><span data-stu-id="249c3-115">postParameters</span></span> | <span data-ttu-id="249c3-116">string</span><span class="sxs-lookup"><span data-stu-id="249c3-116">string</span></span> | <span data-ttu-id="249c3-117">Parámetros de entrada para incluir si usa URL para exponer</span><span class="sxs-lookup"><span data-stu-id="249c3-117">POST parameters to include if using postUrl</span></span>

<span data-ttu-id="249c3-118">Según el estado actual de compatibilidad con las opciones especificadas, se pueden devolver getUrl, URL para exponer o ambos.</span><span class="sxs-lookup"><span data-stu-id="249c3-118">Either getUrl, postUrl, or both may be returned depending on the current state of support for the specified options.</span></span>

<span data-ttu-id="249c3-119">postParameters es una cadena con formato como `application/x-www-form-urlencoded`, y si se realiza una entrada a la URL para exponer el tipo de contenido se debe establecer en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="249c3-119">postParameters is a string formatted as `application/x-www-form-urlencoded`, and if performing a POST to the postUrl the content-type should be set accordingly.</span></span> <span data-ttu-id="249c3-120">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="249c3-120">For example:</span></span>
```
POST https://www.onedrive.com/embed_by_post
Content-Type: application/x-www-form-urlencoded

param1=value&param2=another%20value
```

<span data-ttu-id="249c3-121">Los formatos de direcciones URL y los parámetros deben considerarse opacos.</span><span class="sxs-lookup"><span data-stu-id="249c3-121">The formats of URLs and parameters should be considered opaque.</span></span>
