---
title: Tipo de recurso notebookLinks
description: Vínculos para abrir un bloc de notas de OneNote.
author: jewan-microsoft
localization_priority: Normal
ms.prod: onenote
ms.openlocfilehash: d3def81fb9bb3b7f657be3ed04230a65235db5f3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27984258"
---
# <a name="notebooklinks-resource-type"></a><span data-ttu-id="7ab5c-103">Tipo de recurso notebookLinks</span><span class="sxs-lookup"><span data-stu-id="7ab5c-103">notebookLinks resource type</span></span>

<span data-ttu-id="7ab5c-104">Vínculos para abrir un bloc de notas de OneNote.</span><span class="sxs-lookup"><span data-stu-id="7ab5c-104">Links for opening a OneNote notebook.</span></span>

## <a name="json-representation"></a><span data-ttu-id="7ab5c-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7ab5c-105">JSON representation</span></span>

<span data-ttu-id="7ab5c-106">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7ab5c-106">Here is a JSON representation of the resource.</span></span>

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
## <a name="properties"></a><span data-ttu-id="7ab5c-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7ab5c-107">Properties</span></span>
| <span data-ttu-id="7ab5c-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7ab5c-108">Property</span></span>     | <span data-ttu-id="7ab5c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="7ab5c-109">Type</span></span>   |<span data-ttu-id="7ab5c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ab5c-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7ab5c-111">oneNoteClientUrl</span><span class="sxs-lookup"><span data-stu-id="7ab5c-111">oneNoteClientUrl</span></span>|[<span data-ttu-id="7ab5c-112">externalLink</span><span class="sxs-lookup"><span data-stu-id="7ab5c-112">externalLink</span></span>](externallink.md)|<span data-ttu-id="7ab5c-113">Abre el bloc de notas en el cliente nativo de OneNote si está instalado.</span><span class="sxs-lookup"><span data-stu-id="7ab5c-113">Opens the notebook in the OneNote native client if it's installed.</span></span>|
|<span data-ttu-id="7ab5c-114">oneNoteWebUrl</span><span class="sxs-lookup"><span data-stu-id="7ab5c-114">oneNoteWebUrl</span></span>|[<span data-ttu-id="7ab5c-115">externalLink</span><span class="sxs-lookup"><span data-stu-id="7ab5c-115">externalLink</span></span>](externallink.md)|<span data-ttu-id="7ab5c-116">Abre el bloc de notas en OneNote Online.</span><span class="sxs-lookup"><span data-stu-id="7ab5c-116">Opens the notebook in OneNote Online.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "notebookLinks resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
