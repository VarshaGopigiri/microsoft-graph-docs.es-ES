---
title: Tipo de recurso notebookLinks
description: Vínculos para abrir un bloc de notas de OneNote.
author: Jewan-microsoft
localization_priority: Normal
ms.openlocfilehash: 9c3012abd5b7ca7b9e7b4a1ce2b36159bcd4d966
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27884381"
---
# <a name="notebooklinks-resource-type"></a><span data-ttu-id="e8050-103">Tipo de recurso notebookLinks</span><span class="sxs-lookup"><span data-stu-id="e8050-103">notebookLinks resource type</span></span>

> <span data-ttu-id="e8050-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e8050-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e8050-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e8050-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e8050-106">Vínculos para abrir un bloc de notas de OneNote.</span><span class="sxs-lookup"><span data-stu-id="e8050-106">Links for opening a OneNote notebook.</span></span>

## <a name="json-representation"></a><span data-ttu-id="e8050-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e8050-107">JSON representation</span></span>

<span data-ttu-id="e8050-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e8050-108">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.notebookLinks"
}-->

```json
{
  "oneNoteClientUrl": {"@odata.type": "microsoft.graph.externalLink"},
  "oneNoteWebUrl": {"@odata.type": "microsoft.graph.externalLink"}
}

```
## <a name="properties"></a><span data-ttu-id="e8050-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e8050-109">Properties</span></span>
| <span data-ttu-id="e8050-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e8050-110">Property</span></span>     | <span data-ttu-id="e8050-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="e8050-111">Type</span></span>   |<span data-ttu-id="e8050-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8050-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e8050-113">oneNoteClientUrl</span><span class="sxs-lookup"><span data-stu-id="e8050-113">oneNoteClientUrl</span></span>|[<span data-ttu-id="e8050-114">externalLink</span><span class="sxs-lookup"><span data-stu-id="e8050-114">externalLink</span></span>](externallink.md)|<span data-ttu-id="e8050-115">Abre el bloc de notas en el cliente nativo de OneNote si está instalado.</span><span class="sxs-lookup"><span data-stu-id="e8050-115">Opens the notebook in the OneNote native client if it's installed.</span></span>|
|<span data-ttu-id="e8050-116">oneNoteWebUrl</span><span class="sxs-lookup"><span data-stu-id="e8050-116">oneNoteWebUrl</span></span>|[<span data-ttu-id="e8050-117">externalLink</span><span class="sxs-lookup"><span data-stu-id="e8050-117">externalLink</span></span>](externallink.md)|<span data-ttu-id="e8050-118">Abre el bloc de notas en OneNote Online.</span><span class="sxs-lookup"><span data-stu-id="e8050-118">Opens the notebook in OneNote Online.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "notebookLinks resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
