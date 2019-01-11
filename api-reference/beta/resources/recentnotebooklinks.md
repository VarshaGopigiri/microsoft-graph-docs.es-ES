---
title: Tipo de recurso recentNotebookLinks
description: Vínculos para abrir un bloc de notas de OneNote. Este tipo de recurso existe como propiedad en un recurso recentNotebook.
localization_priority: Normal
ms.openlocfilehash: 5ccf861541526a1673d6174176cb8b2a62df6c23
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27812876"
---
# <a name="recentnotebooklinks-resource-type"></a><span data-ttu-id="b6913-104">Tipo de recurso recentNotebookLinks</span><span class="sxs-lookup"><span data-stu-id="b6913-104">recentNotebookLinks resource type</span></span>

> <span data-ttu-id="b6913-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b6913-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b6913-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b6913-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b6913-107">Vínculos para abrir un bloc de notas de OneNote.</span><span class="sxs-lookup"><span data-stu-id="b6913-107">Links to open a OneNote notebook.</span></span> <span data-ttu-id="b6913-108">Este tipo de recurso existe como propiedad en un recurso [recentNotebook](recentnotebook.md).</span><span class="sxs-lookup"><span data-stu-id="b6913-108">This resource type exists as a property on a [recentNotebook](recentnotebook.md) resource.</span></span>

## <a name="properties"></a><span data-ttu-id="b6913-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b6913-109">Properties</span></span>
| <span data-ttu-id="b6913-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b6913-110">Property</span></span>     | <span data-ttu-id="b6913-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="b6913-111">Type</span></span>   |<span data-ttu-id="b6913-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6913-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b6913-113">oneNoteClientUrl</span><span class="sxs-lookup"><span data-stu-id="b6913-113">oneNoteClientUrl</span></span>|[<span data-ttu-id="b6913-114">externalLink</span><span class="sxs-lookup"><span data-stu-id="b6913-114">externalLink</span></span>](externallink.md)|<span data-ttu-id="b6913-115">Se abre el Bloc de notas en el cliente de OneNote, si está instalado.</span><span class="sxs-lookup"><span data-stu-id="b6913-115">Opens the notebook in the OneNote client, if it's installed.</span></span>|
|<span data-ttu-id="b6913-116">oneNoteWebUrl</span><span class="sxs-lookup"><span data-stu-id="b6913-116">oneNoteWebUrl</span></span>|[<span data-ttu-id="b6913-117">externalLink</span><span class="sxs-lookup"><span data-stu-id="b6913-117">externalLink</span></span>](externallink.md)|<span data-ttu-id="b6913-118">Abre el bloc de notas en OneNote Online.</span><span class="sxs-lookup"><span data-stu-id="b6913-118">Opens the notebook in OneNote Online.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="b6913-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b6913-119">JSON representation</span></span>

<span data-ttu-id="b6913-120">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="b6913-120">The following is a JSON representation of the resource.</span></span>

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
