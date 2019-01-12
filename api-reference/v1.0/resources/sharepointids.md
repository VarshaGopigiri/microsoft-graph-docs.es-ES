---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SharePointIds
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: d65700806c24b0d82d61d05e1e409292bce010a2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27919165"
---
# <a name="sharepointids-resource-type"></a><span data-ttu-id="16513-102">Tipo de recurso SharePointIds</span><span class="sxs-lookup"><span data-stu-id="16513-102">SharePointIds resource type</span></span>

<span data-ttu-id="16513-103">El recurso **SharePointIds** agrupa en una sola estructura los distintos identificadores de un elemento almacenado en un sitio de SharePoint o en OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="16513-103">The **SharePointIds** resource groups the various identifiers for an item stored in a SharePoint site or OneDrive for Business into a single structure.</span></span>

<span data-ttu-id="16513-104">**Nota:** los elementos devueltos de OneDrive Personal no incluyen una faceta **SharePointIds**.</span><span class="sxs-lookup"><span data-stu-id="16513-104">**Note:** items returned from OneDrive personal will not include a **SharePointIds** facet.</span></span>

## <a name="json-representation"></a><span data-ttu-id="16513-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="16513-105">JSON representation</span></span>

<span data-ttu-id="16513-106">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="16513-106">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "listId", "listItemId", "listItemUniqueId", "siteId", "siteUrl", "webId" ],
  "@odata.type": "microsoft.graph.sharepointIds"
}-->

```json
{
    "listId": "string",
    "listItemId": "string",
    "listItemUniqueId": "string",
    "siteId": "string",
    "siteUrl": "url",
    "webId": "string"
}
```

## <a name="properties"></a><span data-ttu-id="16513-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="16513-107">Properties</span></span>

| <span data-ttu-id="16513-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="16513-108">Property</span></span>         | <span data-ttu-id="16513-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="16513-109">Type</span></span>         | <span data-ttu-id="16513-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="16513-110">Description</span></span>
|:-----------------|:-------------|:-------------------------------------------
| <span data-ttu-id="16513-111">listId</span><span class="sxs-lookup"><span data-stu-id="16513-111">listId</span></span>           | <span data-ttu-id="16513-112">string</span><span class="sxs-lookup"><span data-stu-id="16513-112">string</span></span>       | <span data-ttu-id="16513-113">Identificador único (guid) de la lista del elemento en SharePoint.</span><span class="sxs-lookup"><span data-stu-id="16513-113">The unique identifier (guid) for the item's list in SharePoint.</span></span>
| <span data-ttu-id="16513-114">listItemId</span><span class="sxs-lookup"><span data-stu-id="16513-114">listItemId</span></span>       | <span data-ttu-id="16513-115">string</span><span class="sxs-lookup"><span data-stu-id="16513-115">string</span></span>       | <span data-ttu-id="16513-116">Identificador entero del elemento en la lista que lo contiene.</span><span class="sxs-lookup"><span data-stu-id="16513-116">An integer identifier for the item within the containing list.</span></span>
| <span data-ttu-id="16513-117">listItemUniqueId</span><span class="sxs-lookup"><span data-stu-id="16513-117">listItemUniqueId</span></span> | <span data-ttu-id="16513-118">string</span><span class="sxs-lookup"><span data-stu-id="16513-118">string</span></span>       | <span data-ttu-id="16513-119">Identificador único (GUID) del elemento contenido en OneDrive para la Empresa o en un sitio de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="16513-119">The unique identifier (guid) for the item within OneDrive for Business or a SharePoint site.</span></span>
| <span data-ttu-id="16513-120">siteId</span><span class="sxs-lookup"><span data-stu-id="16513-120">siteId</span></span>           | <span data-ttu-id="16513-121">cadena</span><span class="sxs-lookup"><span data-stu-id="16513-121">string</span></span>       | <span data-ttu-id="16513-122">Identificador único (guid) de la colección de sitios del elemento (SPSite).</span><span class="sxs-lookup"><span data-stu-id="16513-122">The unique identifier (guid) for the item's site collection (SPSite).</span></span>
| <span data-ttu-id="16513-123">siteUrl</span><span class="sxs-lookup"><span data-stu-id="16513-123">siteUrl</span></span>          | <span data-ttu-id="16513-124">string (URL)</span><span class="sxs-lookup"><span data-stu-id="16513-124">string (url)</span></span> | <span data-ttu-id="16513-125">La URL de SharePoint del sitio que contiene el elemento.</span><span class="sxs-lookup"><span data-stu-id="16513-125">The SharePoint URL for the site that contains the item.</span></span>
| <span data-ttu-id="16513-126">webId</span><span class="sxs-lookup"><span data-stu-id="16513-126">webId</span></span>            | <span data-ttu-id="16513-127">cadena</span><span class="sxs-lookup"><span data-stu-id="16513-127">string</span></span>       | <span data-ttu-id="16513-128">Identificador único (guid) del sitio del elemento (SPWeb).</span><span class="sxs-lookup"><span data-stu-id="16513-128">The unique identifier (guid) for the item's site (SPWeb).</span></span>

## <a name="remarks"></a><span data-ttu-id="16513-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16513-129">Remarks</span></span>

<span data-ttu-id="16513-130">Para obtener más información sobre las facetas de **driveItem**, consulte [**driveItem**](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="16513-130">For more information about the facets on a **driveItem**, see [**driveItem**](driveitem.md).</span></span>



<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "The SharepointIds facet provides Sharepoint ids associated with an item.",
  "keywords": "item, unique, id, csom, facet",
  "section": "documentation",
  "tocPath": "Facets/SharepointIds"
} -->
