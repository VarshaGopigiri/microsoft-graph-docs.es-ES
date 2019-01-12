---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SharePointIds
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 641b4f5b8d78a38324b7b19c9136e8a53532a9d4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27979939"
---
# <a name="sharepointids-resource-type"></a><span data-ttu-id="15c48-102">Tipo de recurso SharePointIds</span><span class="sxs-lookup"><span data-stu-id="15c48-102">SharePointIds resource type</span></span>

> <span data-ttu-id="15c48-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="15c48-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="15c48-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="15c48-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="15c48-105">El recurso **SharePointIds** agrupa en una sola estructura los distintos identificadores de un elemento almacenado en un sitio de SharePoint o en OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="15c48-105">The **SharePointIds** resource groups the various identifiers for an item stored in a SharePoint site or OneDrive for Business into a single structure.</span></span>

<span data-ttu-id="15c48-106">**Nota:** los elementos devueltos de OneDrive Personal no incluyen una faceta **SharePointIds**.</span><span class="sxs-lookup"><span data-stu-id="15c48-106">**Note:** items returned from OneDrive personal will not include a **SharePointIds** facet.</span></span>

## <a name="json-representation"></a><span data-ttu-id="15c48-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="15c48-107">JSON representation</span></span>

<span data-ttu-id="15c48-108">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="15c48-108">Here is a JSON representation of the resource</span></span>

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
    "tenantId": "string",
    "webId": "string"
}
```

## <a name="properties"></a><span data-ttu-id="15c48-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="15c48-109">Properties</span></span>

| <span data-ttu-id="15c48-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="15c48-110">Property</span></span>         | <span data-ttu-id="15c48-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="15c48-111">Type</span></span>         | <span data-ttu-id="15c48-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="15c48-112">Description</span></span>
|:-----------------|:-------------|:-------------------------------------------
| <span data-ttu-id="15c48-113">listId</span><span class="sxs-lookup"><span data-stu-id="15c48-113">listId</span></span>           | <span data-ttu-id="15c48-114">string</span><span class="sxs-lookup"><span data-stu-id="15c48-114">string</span></span>       | <span data-ttu-id="15c48-115">Identificador único (guid) de la lista del elemento en SharePoint.</span><span class="sxs-lookup"><span data-stu-id="15c48-115">The unique identifier (guid) for the item's list in SharePoint.</span></span>
| <span data-ttu-id="15c48-116">listItemId</span><span class="sxs-lookup"><span data-stu-id="15c48-116">listItemId</span></span>       | <span data-ttu-id="15c48-117">string</span><span class="sxs-lookup"><span data-stu-id="15c48-117">string</span></span>       | <span data-ttu-id="15c48-118">Identificador entero del elemento en la lista que lo contiene.</span><span class="sxs-lookup"><span data-stu-id="15c48-118">An integer identifier for the item within the containing list.</span></span>
| <span data-ttu-id="15c48-119">listItemUniqueId</span><span class="sxs-lookup"><span data-stu-id="15c48-119">listItemUniqueId</span></span> | <span data-ttu-id="15c48-120">string</span><span class="sxs-lookup"><span data-stu-id="15c48-120">string</span></span>       | <span data-ttu-id="15c48-121">Identificador único (GUID) del elemento contenido en OneDrive para la Empresa o en un sitio de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="15c48-121">The unique identifier (guid) for the item within OneDrive for Business or a SharePoint site.</span></span>
| <span data-ttu-id="15c48-122">siteId</span><span class="sxs-lookup"><span data-stu-id="15c48-122">siteId</span></span>           | <span data-ttu-id="15c48-123">string</span><span class="sxs-lookup"><span data-stu-id="15c48-123">string</span></span>       | <span data-ttu-id="15c48-124">Identificador único (guid) de la colección de sitios del elemento (SPSite).</span><span class="sxs-lookup"><span data-stu-id="15c48-124">The unique identifier (guid) for the item's site collection (SPSite).</span></span>
| <span data-ttu-id="15c48-125">siteUrl</span><span class="sxs-lookup"><span data-stu-id="15c48-125">siteUrl</span></span>          | <span data-ttu-id="15c48-126">string (URL)</span><span class="sxs-lookup"><span data-stu-id="15c48-126">string (url)</span></span> | <span data-ttu-id="15c48-127">La URL de SharePoint del sitio que contiene el elemento.</span><span class="sxs-lookup"><span data-stu-id="15c48-127">The SharePoint URL for the site that contains the item.</span></span>
| <span data-ttu-id="15c48-128">tenantId</span><span class="sxs-lookup"><span data-stu-id="15c48-128">tenantId</span></span>         | <span data-ttu-id="15c48-129">string</span><span class="sxs-lookup"><span data-stu-id="15c48-129">string</span></span>       | <span data-ttu-id="15c48-130">Identificador único (guid) del arrendamiento.</span><span class="sxs-lookup"><span data-stu-id="15c48-130">The unique identifier (guid) for the tenancy.</span></span>
| <span data-ttu-id="15c48-131">webId</span><span class="sxs-lookup"><span data-stu-id="15c48-131">webId</span></span>            | <span data-ttu-id="15c48-132">string</span><span class="sxs-lookup"><span data-stu-id="15c48-132">string</span></span>       | <span data-ttu-id="15c48-133">Identificador único (guid) del sitio del elemento (SPWeb).</span><span class="sxs-lookup"><span data-stu-id="15c48-133">The unique identifier (guid) for the item's site (SPWeb).</span></span>

## <a name="remarks"></a><span data-ttu-id="15c48-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="15c48-134">Remarks</span></span>

<span data-ttu-id="15c48-135">Para obtener más información sobre las facetas de **driveItem**, consulte [**driveItem**](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="15c48-135">For more information about the facets on a **driveItem**, see [**driveItem**](driveitem.md).</span></span>



<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "The SharepointIds facet provides Sharepoint ids associated with an item.",
  "keywords": "item, unique, id, csom, facet",
  "section": "documentation",
  "tocPath": "Facets/SharepointIds"
} -->
