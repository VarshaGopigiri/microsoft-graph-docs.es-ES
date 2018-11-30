---
author: kevinlam
ms.author: kevinlam
ms.date: 3/16/2018
title: ItemPreviewInfo - OneDrive para la API
ms.openlocfilehash: 3fa9d10ae3aade7be96e81168b34df84698da1c1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084804"
---
# <a name="itempreviewinfo-resource-type"></a><span data-ttu-id="a893d-102">Tipo de recurso ItemPreviewInfo</span><span class="sxs-lookup"><span data-stu-id="a893d-102">ItemPreviewInfo resource type</span></span>

> <span data-ttu-id="a893d-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a893d-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a893d-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a893d-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a893d-105">El recurso **ItemPreviewInfo** contiene información acerca de cómo incrustar una vista previa de una [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="a893d-105">The **ItemPreviewInfo** resource contains information on how to embed a preview of a [DriveItem](driveitem.md).</span></span>

## <a name="json-representation"></a><span data-ttu-id="a893d-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a893d-106">JSON representation</span></span>

```json
{
    "getUrl": "https://www.onedrive.com/embed?foo=bar&bar=baz",
    "postParameters": "param1=value&param2=another%20value",
    "postUrl": "https://www.onedrive.com/embed_by_post"
}
```

## <a name="properties"></a><span data-ttu-id="a893d-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a893d-107">Properties</span></span>

| <span data-ttu-id="a893d-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="a893d-108">Name</span></span>           | <span data-ttu-id="a893d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a893d-109">Type</span></span>   | <span data-ttu-id="a893d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a893d-110">Description</span></span>
|:---------------|:-------|:---------------------------------------------------
| <span data-ttu-id="a893d-111">getUrl</span><span class="sxs-lookup"><span data-stu-id="a893d-111">getUrl</span></span>         | <span data-ttu-id="a893d-112">string</span><span class="sxs-lookup"><span data-stu-id="a893d-112">string</span></span> | <span data-ttu-id="a893d-113">Dirección URL adecuada para incrustar mediante HTTP GET (IFRAME, etcetera).</span><span class="sxs-lookup"><span data-stu-id="a893d-113">URL suitable for embedding using HTTP GET (iframes, etc.)</span></span>
| <span data-ttu-id="a893d-114">URL para exponer</span><span class="sxs-lookup"><span data-stu-id="a893d-114">postUrl</span></span>        | <span data-ttu-id="a893d-115">string</span><span class="sxs-lookup"><span data-stu-id="a893d-115">string</span></span> | <span data-ttu-id="a893d-116">Dirección URL adecuada para incrustar el uso de HTTP POST (de envío de formulario, JS, etcetera.)</span><span class="sxs-lookup"><span data-stu-id="a893d-116">URL suitable for embedding using HTTP POST (form post, JS, etc.)</span></span>
| <span data-ttu-id="a893d-117">postParameters</span><span class="sxs-lookup"><span data-stu-id="a893d-117">postParameters</span></span> | <span data-ttu-id="a893d-118">string</span><span class="sxs-lookup"><span data-stu-id="a893d-118">string</span></span> | <span data-ttu-id="a893d-119">Parámetros de entrada para incluir si usa URL para exponer</span><span class="sxs-lookup"><span data-stu-id="a893d-119">POST parameters to include if using postUrl</span></span>

<span data-ttu-id="a893d-120">Según el estado actual de compatibilidad con las opciones especificadas, se pueden devolver getUrl, URL para exponer o ambos.</span><span class="sxs-lookup"><span data-stu-id="a893d-120">Either getUrl, postUrl, or both may be returned depending on the current state of support for the specified options.</span></span>

<span data-ttu-id="a893d-121">postParameters es una cadena con formato como `application/x-www-form-urlencoded`, y si se realiza una entrada a la URL para exponer el tipo de contenido se debe establecer en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="a893d-121">postParameters is a string formatted as `application/x-www-form-urlencoded`, and if performing a POST to the postUrl the content-type should be set accordingly.</span></span> <span data-ttu-id="a893d-122">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="a893d-122">For example:</span></span>
```
POST https://www.onedrive.com/embed_by_post
Content-Type: application/x-www-form-urlencoded

param1=value&param2=another%20value
```

<span data-ttu-id="a893d-123">Los formatos de direcciones URL y los parámetros deben considerarse opacos.</span><span class="sxs-lookup"><span data-stu-id="a893d-123">The formats of URLs and parameters should be considered opaque.</span></span>