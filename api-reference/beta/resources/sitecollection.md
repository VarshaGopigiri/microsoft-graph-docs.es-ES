---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SiteCollection
ms.openlocfilehash: d54246002c158270ae23cf81cdc93673f40bd78c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086885"
---
# <a name="sitecollection-resource"></a><span data-ttu-id="97067-102">Recurso SiteCollection</span><span class="sxs-lookup"><span data-stu-id="97067-102">SiteCollection resource</span></span>

> <span data-ttu-id="97067-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="97067-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="97067-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="97067-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="97067-105">El recurso **SiteCollection** proporciona más información acerca de una colección de sitios.</span><span class="sxs-lookup"><span data-stu-id="97067-105">The **siteCollection** resource provides more information about a site collection.</span></span>

<span data-ttu-id="97067-106">Si un recurso [**site**](site.md) tiene una propiedad **siteCollection** que no es NULL, site es un sitio raíz de una colección de sitios.</span><span class="sxs-lookup"><span data-stu-id="97067-106">If a [**site**](site.md) resource has a non-null **siteCollection** property, then the site is a root site for a site collection.</span></span>

## <a name="json-representation"></a><span data-ttu-id="97067-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="97067-107">JSON representation</span></span>

<span data-ttu-id="97067-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="97067-108">Here is a JSON representation of the resource.</span></span>

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

## <a name="properties"></a><span data-ttu-id="97067-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="97067-109">Properties</span></span>

| <span data-ttu-id="97067-110">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="97067-110">Property name</span></span>        | <span data-ttu-id="97067-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="97067-111">Type</span></span>     | <span data-ttu-id="97067-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="97067-112">Description</span></span>
|:---------------------|:---------|:---------------------------------------------------
| <span data-ttu-id="97067-113">**hostname**</span><span class="sxs-lookup"><span data-stu-id="97067-113">**hostname**</span></span>         | <span data-ttu-id="97067-114">string</span><span class="sxs-lookup"><span data-stu-id="97067-114">string</span></span>   | <span data-ttu-id="97067-p102">Nombre de host de la colección de sitios. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="97067-p102">The hostname for the site collection. Read-only.</span></span>
| <span data-ttu-id="97067-117">**dataLocationCode**</span><span class="sxs-lookup"><span data-stu-id="97067-117">**dataLocationCode**</span></span> | <span data-ttu-id="97067-118">string</span><span class="sxs-lookup"><span data-stu-id="97067-118">string</span></span>   | <span data-ttu-id="97067-119">El código de región geográfica para donde reside esta colección de sitios.</span><span class="sxs-lookup"><span data-stu-id="97067-119">The geographic region code for where this site collection resides.</span></span> <span data-ttu-id="97067-120">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="97067-120">Read-only.</span></span>
| <span data-ttu-id="97067-121">**root**</span><span class="sxs-lookup"><span data-stu-id="97067-121">**root**</span></span>             | <span data-ttu-id="97067-122">[root][]</span><span class="sxs-lookup"><span data-stu-id="97067-122">[root][]</span></span> | <span data-ttu-id="97067-123">Si está presente, indica que se trata de una colección de sitios raíz en SharePoint.</span><span class="sxs-lookup"><span data-stu-id="97067-123">If present, indicates that this is a root site collection in SharePoint.</span></span> <span data-ttu-id="97067-124">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="97067-124">Read-only.</span></span>

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
