---
title: Tipo de recurso sectionLinks
description: Vínculos para abrir una sección de OneNote.
localization_priority: Normal
ms.openlocfilehash: 190842708979d62430a4716a8785fd40309cb189
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27858943"
---
# <a name="sectionlinks-resource-type"></a><span data-ttu-id="526db-103">Tipo de recurso sectionLinks</span><span class="sxs-lookup"><span data-stu-id="526db-103">sectionLinks resource type</span></span>

> <span data-ttu-id="526db-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="526db-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="526db-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="526db-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="526db-106">Vínculos para abrir una sección de OneNote.</span><span class="sxs-lookup"><span data-stu-id="526db-106">Links for opening a OneNote section.</span></span>

## <a name="json-representation"></a><span data-ttu-id="526db-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="526db-107">JSON representation</span></span>

<span data-ttu-id="526db-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="526db-108">Here is a JSON representation of the resource.</span></span>

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
## <a name="properties"></a><span data-ttu-id="526db-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="526db-109">Properties</span></span>
| <span data-ttu-id="526db-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="526db-110">Property</span></span>     | <span data-ttu-id="526db-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="526db-111">Type</span></span>   |<span data-ttu-id="526db-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="526db-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="526db-113">oneNoteClientUrl</span><span class="sxs-lookup"><span data-stu-id="526db-113">oneNoteClientUrl</span></span>|[<span data-ttu-id="526db-114">externalLink</span><span class="sxs-lookup"><span data-stu-id="526db-114">externalLink</span></span>](externallink.md)|<span data-ttu-id="526db-115">Abre la sección en el cliente nativo de OneNote si está instalado.</span><span class="sxs-lookup"><span data-stu-id="526db-115">Opens the section in the OneNote native client if it's installed.</span></span>|
|<span data-ttu-id="526db-116">oneNoteWebUrl</span><span class="sxs-lookup"><span data-stu-id="526db-116">oneNoteWebUrl</span></span>|[<span data-ttu-id="526db-117">externalLink</span><span class="sxs-lookup"><span data-stu-id="526db-117">externalLink</span></span>](externallink.md)|<span data-ttu-id="526db-118">Abre la sección en OneNote Online.</span><span class="sxs-lookup"><span data-stu-id="526db-118">Opens the section in OneNote Online.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "sectionLinks resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
