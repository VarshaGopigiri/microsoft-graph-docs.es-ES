---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SiteCollection
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 7fb11fc9dc2f55b853ec512255ffa06f8a53cef6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27933676"
---
# <a name="sitecollection-resource"></a><span data-ttu-id="a32b6-102">Recurso SiteCollection</span><span class="sxs-lookup"><span data-stu-id="a32b6-102">SiteCollection resource</span></span>

> <span data-ttu-id="a32b6-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a32b6-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a32b6-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a32b6-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a32b6-105">El recurso **SiteCollection** proporciona más información acerca de una colección de sitios.</span><span class="sxs-lookup"><span data-stu-id="a32b6-105">The **siteCollection** resource provides more information about a site collection.</span></span>

<span data-ttu-id="a32b6-106">Si un recurso [**site**](site.md) tiene una propiedad **siteCollection** que no es NULL, site es un sitio raíz de una colección de sitios.</span><span class="sxs-lookup"><span data-stu-id="a32b6-106">If a [**site**](site.md) resource has a non-null **siteCollection** property, then the site is a root site for a site collection.</span></span>

## <a name="json-representation"></a><span data-ttu-id="a32b6-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a32b6-107">JSON representation</span></span>

<span data-ttu-id="a32b6-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a32b6-108">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "dataLocationCode", "root"
  ],
  "@odata.type": "microsoft.graph.siteCollection"
}-->

```json
{
  "hostname": "contoso.sharepoint.com",
  "dataLocationCode": "EUR",
  "root": { "@odata.type": "microsoft.graph.root" }
}
```

## <a name="properties"></a><span data-ttu-id="a32b6-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a32b6-109">Properties</span></span>

| <span data-ttu-id="a32b6-110">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="a32b6-110">Property name</span></span>        | <span data-ttu-id="a32b6-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="a32b6-111">Type</span></span>     | <span data-ttu-id="a32b6-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a32b6-112">Description</span></span>
|:---------------------|:---------|:---------------------------------------------------
| <span data-ttu-id="a32b6-113">**hostname**</span><span class="sxs-lookup"><span data-stu-id="a32b6-113">**hostname**</span></span>         | <span data-ttu-id="a32b6-114">string</span><span class="sxs-lookup"><span data-stu-id="a32b6-114">string</span></span>   | <span data-ttu-id="a32b6-p102">Nombre de host de la colección de sitios. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a32b6-p102">The hostname for the site collection. Read-only.</span></span>
| <span data-ttu-id="a32b6-117">**dataLocationCode**</span><span class="sxs-lookup"><span data-stu-id="a32b6-117">**dataLocationCode**</span></span> | <span data-ttu-id="a32b6-118">string</span><span class="sxs-lookup"><span data-stu-id="a32b6-118">string</span></span>   | <span data-ttu-id="a32b6-119">El código de región geográfica para donde reside esta colección de sitios.</span><span class="sxs-lookup"><span data-stu-id="a32b6-119">The geographic region code for where this site collection resides.</span></span> <span data-ttu-id="a32b6-120">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a32b6-120">Read-only.</span></span>
| <span data-ttu-id="a32b6-121">**root**</span><span class="sxs-lookup"><span data-stu-id="a32b6-121">**root**</span></span>             | <span data-ttu-id="a32b6-122">[root][]</span><span class="sxs-lookup"><span data-stu-id="a32b6-122">[root][]</span></span> | <span data-ttu-id="a32b6-123">Si está presente, indica que se trata de una colección de sitios raíz en SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a32b6-123">If present, indicates that this is a root site collection in SharePoint.</span></span> <span data-ttu-id="a32b6-124">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a32b6-124">Read-only.</span></span>

[root]: root.md

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
