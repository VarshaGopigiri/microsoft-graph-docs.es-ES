---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SiteCollection
ms.openlocfilehash: 6b36f3a0c2d958081f1b5663231a541f2e8a000f
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="sitecollection-resource"></a><span data-ttu-id="a0ce1-102">Recurso SiteCollection</span><span class="sxs-lookup"><span data-stu-id="a0ce1-102">SiteCollection resource</span></span>

<span data-ttu-id="a0ce1-103">El recurso **SiteCollection** proporciona más información acerca de una colección de sitios.</span><span class="sxs-lookup"><span data-stu-id="a0ce1-103">The **siteCollection** resource provides more information about a site collection.</span></span>

<span data-ttu-id="a0ce1-104">Si un recurso [**site**](site.md) tiene una propiedad **siteCollection** que no es NULL, site es un sitio raíz de una colección de sitios.</span><span class="sxs-lookup"><span data-stu-id="a0ce1-104">If a [**site**](site.md) resource has a non-null **siteCollection** property, then the site is a root site for a site collection.</span></span>

## <a name="json-representation"></a><span data-ttu-id="a0ce1-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a0ce1-105">JSON representation</span></span>

<span data-ttu-id="a0ce1-106">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a0ce1-106">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
  ],
  "@odata.type": "microsoft.graph.siteCollection"
}-->

```json
{
  "hostname": "contoso.sharepoint.com"
}
```

## <a name="properties"></a><span data-ttu-id="a0ce1-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a0ce1-107">Properties</span></span>

| <span data-ttu-id="a0ce1-108">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="a0ce1-108">Property name</span></span> | <span data-ttu-id="a0ce1-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a0ce1-109">Type</span></span>    | <span data-ttu-id="a0ce1-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0ce1-110">Description</span></span>                                                                                                                  |
|:--------------|:--------|:---------------------------------------------------
| <span data-ttu-id="a0ce1-111">**hostname**</span><span class="sxs-lookup"><span data-stu-id="a0ce1-111">**hostname**</span></span>  | <span data-ttu-id="a0ce1-112">string</span><span class="sxs-lookup"><span data-stu-id="a0ce1-112">string</span></span>  | <span data-ttu-id="a0ce1-p101">Nombre de host de la colección de sitios. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a0ce1-p101">The hostname for the site collection. Read-only.</span></span>


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Facets/SiteCollection"
}-->
