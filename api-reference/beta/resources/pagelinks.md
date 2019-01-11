---
title: Tipo de recurso pageLinks
description: Vínculos para abrir una página de OneNote.
localization_priority: Normal
ms.openlocfilehash: 9bee1b4d3d327118dbf1deec83a37787bd4b18e2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27832630"
---
# <a name="pagelinks-resource-type"></a><span data-ttu-id="a2bf1-103">Tipo de recurso pageLinks</span><span class="sxs-lookup"><span data-stu-id="a2bf1-103">pageLinks resource type</span></span>

> <span data-ttu-id="a2bf1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a2bf1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a2bf1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a2bf1-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a2bf1-106">Vínculos para abrir una página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="a2bf1-106">Links for opening a OneNote page.</span></span>

## <a name="json-representation"></a><span data-ttu-id="a2bf1-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a2bf1-107">JSON representation</span></span>

<span data-ttu-id="a2bf1-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a2bf1-108">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.pageLinks"
}-->

```json
{
  "oneNoteClientUrl": {"@odata.type": "microsoft.graph.externalLink"},
  "oneNoteWebUrl": {"@odata.type": "microsoft.graph.externalLink"}
}

```
## <a name="properties"></a><span data-ttu-id="a2bf1-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a2bf1-109">Properties</span></span>
| <span data-ttu-id="a2bf1-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a2bf1-110">Property</span></span>     | <span data-ttu-id="a2bf1-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="a2bf1-111">Type</span></span>   |<span data-ttu-id="a2bf1-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2bf1-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a2bf1-113">oneNoteClientUrl</span><span class="sxs-lookup"><span data-stu-id="a2bf1-113">oneNoteClientUrl</span></span>|[<span data-ttu-id="a2bf1-114">externalLink</span><span class="sxs-lookup"><span data-stu-id="a2bf1-114">externalLink</span></span>](externallink.md)|<span data-ttu-id="a2bf1-115">Abre la página en el cliente nativo de OneNote si está instalado.</span><span class="sxs-lookup"><span data-stu-id="a2bf1-115">Opens the page in the OneNote native client if it's installed.</span></span>|
|<span data-ttu-id="a2bf1-116">oneNoteWebUrl</span><span class="sxs-lookup"><span data-stu-id="a2bf1-116">oneNoteWebUrl</span></span>|[<span data-ttu-id="a2bf1-117">externalLink</span><span class="sxs-lookup"><span data-stu-id="a2bf1-117">externalLink</span></span>](externallink.md)|<span data-ttu-id="a2bf1-118">Abre la página en OneNote Online.</span><span class="sxs-lookup"><span data-stu-id="a2bf1-118">Opens the page in OneNote Online.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "pageLinks resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
