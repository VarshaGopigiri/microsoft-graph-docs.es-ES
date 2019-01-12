---
title: tipo de recurso educationOneNoteResource
description: 'Una subclase de educationResource. Esto representa la ubicación de la página de OneNote.  '
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: b10bef551cdc2dd29a8a20c69d2c4657ee66af4e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27927922"
---
# <a name="educationonenoteresource-resource-type"></a><span data-ttu-id="a278b-104">tipo de recurso educationOneNoteResource</span><span class="sxs-lookup"><span data-stu-id="a278b-104">educationOneNoteResource resource type</span></span>

> <span data-ttu-id="a278b-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a278b-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a278b-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a278b-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a278b-107">Una subclase de [educationResource](educationresource.md).</span><span class="sxs-lookup"><span data-stu-id="a278b-107">A subclass of [educationResource](educationresource.md).</span></span> <span data-ttu-id="a278b-108">Esto representa la ubicación de la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="a278b-108">This represents the location of the OneNote page.</span></span>  

## <a name="properties"></a><span data-ttu-id="a278b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a278b-109">Properties</span></span>
| <span data-ttu-id="a278b-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a278b-110">Property</span></span>     | <span data-ttu-id="a278b-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="a278b-111">Type</span></span>   |<span data-ttu-id="a278b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a278b-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a278b-113">pageUrl</span><span class="sxs-lookup"><span data-stu-id="a278b-113">pageUrl</span></span>|<span data-ttu-id="a278b-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="a278b-114">String</span></span>|<span data-ttu-id="a278b-115">La dirección URL Microsoft Graph a la página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="a278b-115">The Microsoft Graph URL to the page in OneNote.</span></span>|
|<span data-ttu-id="a278b-116">sectionName</span><span class="sxs-lookup"><span data-stu-id="a278b-116">sectionName</span></span>|<span data-ttu-id="a278b-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="a278b-117">String</span></span>|<span data-ttu-id="a278b-118">Nombre de la sección que se deben copiar en distribuciones o que se han copiado en.</span><span class="sxs-lookup"><span data-stu-id="a278b-118">Section name that distributions should be copied into or were copied into.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="a278b-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a278b-119">JSON representation</span></span>

<span data-ttu-id="a278b-120">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="a278b-120">The following is a JSON representation of the resource.</span></span>

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
