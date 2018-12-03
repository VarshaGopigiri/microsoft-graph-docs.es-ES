---
title: tipo de recurso educationOneNoteResource
description: 'Una subclase de educationResource. Esto representa la ubicación de la página de OneNote.  '
ms.openlocfilehash: cfaaaf0a97e2dcea3a0a2a7384c761b678858f5b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087385"
---
# <a name="educationonenoteresource-resource-type"></a><span data-ttu-id="99471-104">tipo de recurso educationOneNoteResource</span><span class="sxs-lookup"><span data-stu-id="99471-104">educationOneNoteResource resource type</span></span>

> <span data-ttu-id="99471-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="99471-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="99471-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="99471-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="99471-107">Una subclase de [educationResource](educationresource.md).</span><span class="sxs-lookup"><span data-stu-id="99471-107">A subclass of [educationResource](educationresource.md).</span></span> <span data-ttu-id="99471-108">Esto representa la ubicación de la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="99471-108">This represents the location of the OneNote page.</span></span>  

## <a name="properties"></a><span data-ttu-id="99471-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="99471-109">Properties</span></span>
| <span data-ttu-id="99471-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="99471-110">Property</span></span>     | <span data-ttu-id="99471-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="99471-111">Type</span></span>   |<span data-ttu-id="99471-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="99471-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="99471-113">pageUrl</span><span class="sxs-lookup"><span data-stu-id="99471-113">pageUrl</span></span>|<span data-ttu-id="99471-114">String</span><span class="sxs-lookup"><span data-stu-id="99471-114">String</span></span>|<span data-ttu-id="99471-115">La dirección URL Microsoft Graph a la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="99471-115">The Microsoft Graph URL to the page in OneNote.</span></span>|
|<span data-ttu-id="99471-116">sectionName</span><span class="sxs-lookup"><span data-stu-id="99471-116">sectionName</span></span>|<span data-ttu-id="99471-117">String</span><span class="sxs-lookup"><span data-stu-id="99471-117">String</span></span>|<span data-ttu-id="99471-118">Nombre de la sección que se deben copiar en distribuciones o que se han copiado en.</span><span class="sxs-lookup"><span data-stu-id="99471-118">Section name that distributions should be copied into or were copied into.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="99471-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="99471-119">JSON representation</span></span>

<span data-ttu-id="99471-120">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="99471-120">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationOneNoteResource"
}-->

```json
{
  "pageUrl": "String",
  "sectionName": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationOneNoteResource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->