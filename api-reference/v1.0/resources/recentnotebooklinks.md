---
title: Tipo de recurso recentNotebookLinks
description: Vínculos para abrir un bloc de notas de OneNote. Este tipo de recurso existe como propiedad en un recurso recentNotebook.
localization_priority: Normal
ms.openlocfilehash: 846047bd602d19cb4745e0a63f0326aaf7bfb512
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27810587"
---
# <a name="recentnotebooklinks-resource-type"></a><span data-ttu-id="96ac4-104">Tipo de recurso recentNotebookLinks</span><span class="sxs-lookup"><span data-stu-id="96ac4-104">recentNotebookLinks resource type</span></span>

<span data-ttu-id="96ac4-105">Vínculos para abrir un bloc de notas de OneNote.</span><span class="sxs-lookup"><span data-stu-id="96ac4-105">Links for opening a OneNote notebook.</span></span> <span data-ttu-id="96ac4-106">Este tipo de recurso existe como propiedad en un recurso [recentNotebook](recentnotebook.md).</span><span class="sxs-lookup"><span data-stu-id="96ac4-106">This resource type exists as a property on a [recentNotebook](recentnotebook.md) resource.</span></span>

## <a name="properties"></a><span data-ttu-id="96ac4-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="96ac4-107">Properties</span></span>
| <span data-ttu-id="96ac4-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="96ac4-108">Property</span></span>     | <span data-ttu-id="96ac4-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="96ac4-109">Type</span></span>   |<span data-ttu-id="96ac4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="96ac4-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="96ac4-111">oneNoteClientUrl</span><span class="sxs-lookup"><span data-stu-id="96ac4-111">oneNoteClientUrl</span></span>|[<span data-ttu-id="96ac4-112">externalLink</span><span class="sxs-lookup"><span data-stu-id="96ac4-112">externalLink</span></span>](externallink.md)|<span data-ttu-id="96ac4-113">Abre el bloc de notas en el cliente nativo de OneNote si está instalado.</span><span class="sxs-lookup"><span data-stu-id="96ac4-113">Opens the notebook in the OneNote native client if it's installed.</span></span>|
|<span data-ttu-id="96ac4-114">oneNoteWebUrl</span><span class="sxs-lookup"><span data-stu-id="96ac4-114">oneNoteWebUrl</span></span>|[<span data-ttu-id="96ac4-115">externalLink</span><span class="sxs-lookup"><span data-stu-id="96ac4-115">externalLink</span></span>](externallink.md)|<span data-ttu-id="96ac4-116">Abre el bloc de notas en OneNote Online.</span><span class="sxs-lookup"><span data-stu-id="96ac4-116">Opens the notebook in OneNote Online.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="96ac4-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="96ac4-117">JSON representation</span></span>

<span data-ttu-id="96ac4-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="96ac4-118">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.recentNotebookLinks"
}-->

```json
{
  "oneNoteClientUrl": {"@odata.type": "microsoft.graph.externalLink"},
  "oneNoteWebUrl": {"@odata.type": "microsoft.graph.externalLink"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "recentNotebookLinks resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
