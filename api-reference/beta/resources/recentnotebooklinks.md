---
title: Tipo de recurso recentNotebookLinks
description: Vínculos para abrir un bloc de notas de OneNote. Este tipo de recurso existe como propiedad en un recurso recentNotebook.
ms.openlocfilehash: de13f25148425a1816a60f6cf5b9f4a09f61c7dc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086730"
---
# <a name="recentnotebooklinks-resource-type"></a><span data-ttu-id="13e48-104">Tipo de recurso recentNotebookLinks</span><span class="sxs-lookup"><span data-stu-id="13e48-104">recentNotebookLinks resource type</span></span>

> <span data-ttu-id="13e48-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="13e48-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="13e48-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="13e48-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="13e48-107">Vínculos para abrir un bloc de notas de OneNote.</span><span class="sxs-lookup"><span data-stu-id="13e48-107">Links to open a OneNote notebook.</span></span> <span data-ttu-id="13e48-108">Este tipo de recurso existe como propiedad en un recurso [recentNotebook](recentnotebook.md).</span><span class="sxs-lookup"><span data-stu-id="13e48-108">This resource type exists as a property on a [recentNotebook](recentnotebook.md) resource.</span></span>

## <a name="properties"></a><span data-ttu-id="13e48-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="13e48-109">Properties</span></span>
| <span data-ttu-id="13e48-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="13e48-110">Property</span></span>     | <span data-ttu-id="13e48-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="13e48-111">Type</span></span>   |<span data-ttu-id="13e48-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="13e48-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="13e48-113">oneNoteClientUrl</span><span class="sxs-lookup"><span data-stu-id="13e48-113">oneNoteClientUrl</span></span>|[<span data-ttu-id="13e48-114">externalLink</span><span class="sxs-lookup"><span data-stu-id="13e48-114">externalLink</span></span>](externallink.md)|<span data-ttu-id="13e48-115">Se abre el Bloc de notas en el cliente de OneNote, si está instalado.</span><span class="sxs-lookup"><span data-stu-id="13e48-115">Opens the notebook in the OneNote client, if it's installed.</span></span>|
|<span data-ttu-id="13e48-116">oneNoteWebUrl</span><span class="sxs-lookup"><span data-stu-id="13e48-116">oneNoteWebUrl</span></span>|[<span data-ttu-id="13e48-117">externalLink</span><span class="sxs-lookup"><span data-stu-id="13e48-117">externalLink</span></span>](externallink.md)|<span data-ttu-id="13e48-118">Abre el bloc de notas en OneNote Online.</span><span class="sxs-lookup"><span data-stu-id="13e48-118">Opens the notebook in OneNote Online.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="13e48-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="13e48-119">JSON representation</span></span>

<span data-ttu-id="13e48-120">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="13e48-120">The following is a JSON representation of the resource.</span></span>

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
