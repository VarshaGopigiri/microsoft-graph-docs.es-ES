---
title: Tipo de recurso website
description: Representa un sitio web.
ms.openlocfilehash: 14934aae418581f4c75c880be67bf51fd0bc293c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029132"
---
# <a name="website-resource-type"></a><span data-ttu-id="256cb-103">Tipo de recurso website</span><span class="sxs-lookup"><span data-stu-id="256cb-103">website resource type</span></span>

<span data-ttu-id="256cb-104">Representa un sitio web.</span><span class="sxs-lookup"><span data-stu-id="256cb-104">Represents a website.</span></span>


## <a name="properties"></a><span data-ttu-id="256cb-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="256cb-105">Properties</span></span>
| <span data-ttu-id="256cb-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="256cb-106">Property</span></span>     | <span data-ttu-id="256cb-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="256cb-107">Type</span></span>   |<span data-ttu-id="256cb-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="256cb-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="256cb-109">type</span><span class="sxs-lookup"><span data-stu-id="256cb-109">type</span></span>|<span data-ttu-id="256cb-110">websiteType</span><span class="sxs-lookup"><span data-stu-id="256cb-110">websiteType</span></span>| <span data-ttu-id="256cb-111">Los valores posibles son: `other`, `home`, `work`, `blog`, `profile`.</span><span class="sxs-lookup"><span data-stu-id="256cb-111">The possible values are: `other`, `home`, `work`, `blog`, `profile`.</span></span>|
|<span data-ttu-id="256cb-112">address</span><span class="sxs-lookup"><span data-stu-id="256cb-112">address</span></span>|<span data-ttu-id="256cb-113">string</span><span class="sxs-lookup"><span data-stu-id="256cb-113">string</span></span>|<span data-ttu-id="256cb-114">Dirección URL del sitio web.</span><span class="sxs-lookup"><span data-stu-id="256cb-114">The URL of the website.</span></span>|
|<span data-ttu-id="256cb-115">displayName</span><span class="sxs-lookup"><span data-stu-id="256cb-115">displayName</span></span>|<span data-ttu-id="256cb-116">string</span><span class="sxs-lookup"><span data-stu-id="256cb-116">string</span></span>|<span data-ttu-id="256cb-117">Nombre para mostrar del sitio web.</span><span class="sxs-lookup"><span data-stu-id="256cb-117">The display name of the web site.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="256cb-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="256cb-118">JSON representation</span></span>

<span data-ttu-id="256cb-119">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="256cb-119">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.website"
}-->

```json
{
  "type": "String",
  "address": "string",
  "displayName": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "webSite resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
