---
title: Tipo de recurso pageLinks
description: Vínculos para abrir una página de OneNote.
ms.openlocfilehash: 598e39f5cf2b6bbd722b07b72f4fa63ad7fd8302
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089933"
---
# <a name="pagelinks-resource-type"></a><span data-ttu-id="16705-103">Tipo de recurso pageLinks</span><span class="sxs-lookup"><span data-stu-id="16705-103">pageLinks resource type</span></span>

> <span data-ttu-id="16705-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="16705-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="16705-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="16705-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="16705-106">Vínculos para abrir una página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="16705-106">Links for opening a OneNote page.</span></span>

## <a name="json-representation"></a><span data-ttu-id="16705-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="16705-107">JSON representation</span></span>

<span data-ttu-id="16705-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="16705-108">Here is a JSON representation of the resource.</span></span>

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
## <a name="properties"></a><span data-ttu-id="16705-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="16705-109">Properties</span></span>
| <span data-ttu-id="16705-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="16705-110">Property</span></span>     | <span data-ttu-id="16705-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="16705-111">Type</span></span>   |<span data-ttu-id="16705-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="16705-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="16705-113">oneNoteClientUrl</span><span class="sxs-lookup"><span data-stu-id="16705-113">oneNoteClientUrl</span></span>|[<span data-ttu-id="16705-114">externalLink</span><span class="sxs-lookup"><span data-stu-id="16705-114">externalLink</span></span>](externallink.md)|<span data-ttu-id="16705-115">Abre la página en el cliente nativo de OneNote si está instalado.</span><span class="sxs-lookup"><span data-stu-id="16705-115">Opens the page in the OneNote native client if it's installed.</span></span>|
|<span data-ttu-id="16705-116">oneNoteWebUrl</span><span class="sxs-lookup"><span data-stu-id="16705-116">oneNoteWebUrl</span></span>|[<span data-ttu-id="16705-117">externalLink</span><span class="sxs-lookup"><span data-stu-id="16705-117">externalLink</span></span>](externallink.md)|<span data-ttu-id="16705-118">Abre la página en OneNote Online.</span><span class="sxs-lookup"><span data-stu-id="16705-118">Opens the page in OneNote Online.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "pageLinks resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->