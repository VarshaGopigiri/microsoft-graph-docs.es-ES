---
title: Tipo de recurso sectionLinks
description: Vínculos para abrir una sección de OneNote.
ms.openlocfilehash: 4ca6221992c75f410839538d8080c084c8486903
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029653"
---
# <a name="sectionlinks-resource-type"></a><span data-ttu-id="b998d-103">Tipo de recurso sectionLinks</span><span class="sxs-lookup"><span data-stu-id="b998d-103">sectionLinks resource type</span></span>

<span data-ttu-id="b998d-104">Vínculos para abrir una sección de OneNote.</span><span class="sxs-lookup"><span data-stu-id="b998d-104">Links for opening a OneNote section.</span></span>

## <a name="json-representation"></a><span data-ttu-id="b998d-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b998d-105">JSON representation</span></span>

<span data-ttu-id="b998d-106">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b998d-106">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.sectionLinks"
}-->

```json
{
  "oneNoteClientUrl": {"@odata.type": "microsoft.graph.externalLink"},
  "oneNoteWebUrl": {"@odata.type": "microsoft.graph.externalLink"}
}

```
## <a name="properties"></a><span data-ttu-id="b998d-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b998d-107">Properties</span></span>
| <span data-ttu-id="b998d-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b998d-108">Property</span></span>     | <span data-ttu-id="b998d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="b998d-109">Type</span></span>   |<span data-ttu-id="b998d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b998d-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b998d-111">oneNoteClientUrl</span><span class="sxs-lookup"><span data-stu-id="b998d-111">oneNoteClientUrl</span></span>|[<span data-ttu-id="b998d-112">externalLink</span><span class="sxs-lookup"><span data-stu-id="b998d-112">externalLink</span></span>](externallink.md)|<span data-ttu-id="b998d-113">Abre la sección en el cliente nativo de OneNote si está instalado.</span><span class="sxs-lookup"><span data-stu-id="b998d-113">Opens the section in the OneNote native client if it's installed.</span></span>|
|<span data-ttu-id="b998d-114">oneNoteWebUrl</span><span class="sxs-lookup"><span data-stu-id="b998d-114">oneNoteWebUrl</span></span>|[<span data-ttu-id="b998d-115">externalLink</span><span class="sxs-lookup"><span data-stu-id="b998d-115">externalLink</span></span>](externallink.md)|<span data-ttu-id="b998d-116">Abre la sección en OneNote Online.</span><span class="sxs-lookup"><span data-stu-id="b998d-116">Opens the section in OneNote Online.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "sectionLinks resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->