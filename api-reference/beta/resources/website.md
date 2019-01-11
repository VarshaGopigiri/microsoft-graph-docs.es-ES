---
title: Tipo de recurso website
description: Representa un sitio web.
localization_priority: Normal
ms.openlocfilehash: 15cc926ad1c251fd169ccdb0b1374df7f434a645
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27826120"
---
# <a name="website-resource-type"></a><span data-ttu-id="8f95b-103">Tipo de recurso website</span><span class="sxs-lookup"><span data-stu-id="8f95b-103">website resource type</span></span>

> <span data-ttu-id="8f95b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8f95b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8f95b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8f95b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8f95b-106">Representa un sitio web.</span><span class="sxs-lookup"><span data-stu-id="8f95b-106">Represents a web site.</span></span>


## <a name="properties"></a><span data-ttu-id="8f95b-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8f95b-107">Properties</span></span>
| <span data-ttu-id="8f95b-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8f95b-108">Property</span></span>     | <span data-ttu-id="8f95b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="8f95b-109">Type</span></span>   |<span data-ttu-id="8f95b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f95b-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8f95b-111">type</span><span class="sxs-lookup"><span data-stu-id="8f95b-111">type</span></span>|<span data-ttu-id="8f95b-112">String</span><span class="sxs-lookup"><span data-stu-id="8f95b-112">String</span></span>| <span data-ttu-id="8f95b-113">Valores posibles: `other`, `home`, `work`, `blog`, `profile`.</span><span class="sxs-lookup"><span data-stu-id="8f95b-113">Possible values are: `other`, `home`, `work`, `blog`, `profile`.</span></span>|
|<span data-ttu-id="8f95b-114">address</span><span class="sxs-lookup"><span data-stu-id="8f95b-114">address</span></span>|<span data-ttu-id="8f95b-115">string</span><span class="sxs-lookup"><span data-stu-id="8f95b-115">string</span></span>|<span data-ttu-id="8f95b-116">Dirección URL del sitio web.</span><span class="sxs-lookup"><span data-stu-id="8f95b-116">The URL of the website.</span></span>|
|<span data-ttu-id="8f95b-117">displayName</span><span class="sxs-lookup"><span data-stu-id="8f95b-117">displayName</span></span>|<span data-ttu-id="8f95b-118">string</span><span class="sxs-lookup"><span data-stu-id="8f95b-118">string</span></span>|<span data-ttu-id="8f95b-119">Nombre para mostrar del sitio web.</span><span class="sxs-lookup"><span data-stu-id="8f95b-119">The display name of the web site.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="8f95b-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8f95b-120">JSON representation</span></span>

<span data-ttu-id="8f95b-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8f95b-121">Here is a JSON representation of the resource.</span></span>

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
