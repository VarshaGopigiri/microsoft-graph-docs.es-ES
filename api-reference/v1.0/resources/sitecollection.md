---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SiteCollection
ms.openlocfilehash: 98f7b9d930ccf7f1f0e1a6a0e1ad0353d49cf2bf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030805"
---
# <a name="sitecollection-resource"></a><span data-ttu-id="d76b2-102">Recurso SiteCollection</span><span class="sxs-lookup"><span data-stu-id="d76b2-102">SiteCollection resource</span></span>

<span data-ttu-id="d76b2-103">El recurso **SiteCollection** proporciona más información acerca de una colección de sitios.</span><span class="sxs-lookup"><span data-stu-id="d76b2-103">The **siteCollection** resource provides more information about a site collection.</span></span>

<span data-ttu-id="d76b2-104">Si un recurso [**site**](site.md) tiene una propiedad **siteCollection** que no es NULL, site es un sitio raíz de una colección de sitios.</span><span class="sxs-lookup"><span data-stu-id="d76b2-104">If a [**site**](site.md) resource has a non-null **siteCollection** property, then the site is a root site for a site collection.</span></span>

## <a name="json-representation"></a><span data-ttu-id="d76b2-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d76b2-105">JSON representation</span></span>

<span data-ttu-id="d76b2-106">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d76b2-106">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
  ],
  "@odata.type": "microsoft.graph.siteCollection"
}-->

```json
{
  "hostname": "contoso.sharepoint.com",
  "root": { "@odata.type": "microsoft.graph.root" }
}
```

## <a name="properties"></a><span data-ttu-id="d76b2-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d76b2-107">Properties</span></span>

| <span data-ttu-id="d76b2-108">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="d76b2-108">Property name</span></span>        | <span data-ttu-id="d76b2-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="d76b2-109">Type</span></span>     | <span data-ttu-id="d76b2-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d76b2-110">Description</span></span>
|:---------------------|:---------|:---------------------------------------------------
| <span data-ttu-id="d76b2-111">**hostname**</span><span class="sxs-lookup"><span data-stu-id="d76b2-111">**hostname**</span></span>         | <span data-ttu-id="d76b2-112">string</span><span class="sxs-lookup"><span data-stu-id="d76b2-112">string</span></span>   | <span data-ttu-id="d76b2-p101">Nombre de host de la colección de sitios. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d76b2-p101">The hostname for the site collection. Read-only.</span></span>
| <span data-ttu-id="d76b2-115">**root**</span><span class="sxs-lookup"><span data-stu-id="d76b2-115">**root**</span></span>             | <span data-ttu-id="d76b2-116">[root][]</span><span class="sxs-lookup"><span data-stu-id="d76b2-116">[root][]</span></span> | <span data-ttu-id="d76b2-117">Si está presente, indica que se trata de una colección de sitios raíz en SharePoint.</span><span class="sxs-lookup"><span data-stu-id="d76b2-117">If present, indicates that this is a root site collection in SharePoint.</span></span> <span data-ttu-id="d76b2-118">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d76b2-118">Read-only.</span></span>

[root]: root.md

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Facets/SiteCollection"
}-->
