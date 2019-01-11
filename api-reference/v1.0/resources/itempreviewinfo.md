---
author: kevinlam
ms.author: kevinlam
ms.date: 3/16/2018
title: ItemPreviewInfo
localization_priority: Normal
ms.openlocfilehash: e7df636f9c406a499baa5ef3be1748273920cac4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27885480"
---
# <a name="itempreviewinfo-resource-type"></a><span data-ttu-id="16633-102">tipo de recurso itemPreviewInfo</span><span class="sxs-lookup"><span data-stu-id="16633-102">itemPreviewInfo resource type</span></span>

<span data-ttu-id="16633-103">El recurso **itemPreviewInfo** contiene información acerca de cómo incrustar una vista previa de una [driveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="16633-103">The **itemPreviewInfo** resource contains information on how to embed a preview of a [driveItem](driveitem.md).</span></span>

## <a name="json-representation"></a><span data-ttu-id="16633-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="16633-104">JSON representation</span></span>

```json
{
    "getUrl": "https://www.onedrive.com/embed?foo=bar&bar=baz",
    "postParameters": "param1=value&param2=another%20value",
    "postUrl": "https://www.onedrive.com/embed_by_post"
}
```

## <a name="properties"></a><span data-ttu-id="16633-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="16633-105">Properties</span></span>

| <span data-ttu-id="16633-106">Nombre</span><span class="sxs-lookup"><span data-stu-id="16633-106">Name</span></span>           | <span data-ttu-id="16633-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="16633-107">Type</span></span>   | <span data-ttu-id="16633-108">Description</span><span class="sxs-lookup"><span data-stu-id="16633-108">Description</span></span>
|:---------------|:-------|:---------------------------------------------------
| <span data-ttu-id="16633-109">getUrl</span><span class="sxs-lookup"><span data-stu-id="16633-109">getUrl</span></span>         | <span data-ttu-id="16633-110">string</span><span class="sxs-lookup"><span data-stu-id="16633-110">string</span></span> | <span data-ttu-id="16633-111">Dirección URL adecuada para incrustar mediante HTTP GET (IFRAME, etcetera).</span><span class="sxs-lookup"><span data-stu-id="16633-111">URL suitable for embedding using HTTP GET (iframes, etc.)</span></span>
| <span data-ttu-id="16633-112">URL para exponer</span><span class="sxs-lookup"><span data-stu-id="16633-112">postUrl</span></span>        | <span data-ttu-id="16633-113">string</span><span class="sxs-lookup"><span data-stu-id="16633-113">string</span></span> | <span data-ttu-id="16633-114">Dirección URL adecuada para incrustar el uso de HTTP POST (de envío de formulario, JS, etcetera.)</span><span class="sxs-lookup"><span data-stu-id="16633-114">URL suitable for embedding using HTTP POST (form post, JS, etc.)</span></span>
| <span data-ttu-id="16633-115">postParameters</span><span class="sxs-lookup"><span data-stu-id="16633-115">postParameters</span></span> | <span data-ttu-id="16633-116">string</span><span class="sxs-lookup"><span data-stu-id="16633-116">string</span></span> | <span data-ttu-id="16633-117">Parámetros de entrada para incluir si usa URL para exponer</span><span class="sxs-lookup"><span data-stu-id="16633-117">POST parameters to include if using postUrl</span></span>

<span data-ttu-id="16633-118">Según el estado actual de compatibilidad con las opciones especificadas, se pueden devolver getUrl, URL para exponer o ambos.</span><span class="sxs-lookup"><span data-stu-id="16633-118">Either getUrl, postUrl, or both may be returned depending on the current state of support for the specified options.</span></span>

<span data-ttu-id="16633-119">postParameters es una cadena con formato como `application/x-www-form-urlencoded`, y si se realiza una entrada a la URL para exponer el tipo de contenido se debe establecer en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="16633-119">postParameters is a string formatted as `application/x-www-form-urlencoded`, and if performing a POST to the postUrl the content-type should be set accordingly.</span></span> <span data-ttu-id="16633-120">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="16633-120">For example:</span></span>
```
POST https://www.onedrive.com/embed_by_post
Content-Type: application/x-www-form-urlencoded

param1=value&param2=another%20value
```

<span data-ttu-id="16633-121">Los formatos de direcciones URL y los parámetros deben considerarse opacos.</span><span class="sxs-lookup"><span data-stu-id="16633-121">The formats of URLs and parameters should be considered opaque.</span></span>
