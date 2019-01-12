---
title: tipo de recurso educationFeedback
description: Comentarios de un profesor para un estudiante. Esta propiedad representa la parte de texto de los comentarios junto con la que.
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: 96f1e0f4d6be070548d984786042a801d764ece9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27962691"
---
# <a name="educationfeedback-resource-type"></a><span data-ttu-id="1db50-104">tipo de recurso educationFeedback</span><span class="sxs-lookup"><span data-stu-id="1db50-104">educationFeedback resource type</span></span>

> <span data-ttu-id="1db50-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1db50-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1db50-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1db50-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1db50-107">Comentarios de un profesor para un estudiante.</span><span class="sxs-lookup"><span data-stu-id="1db50-107">Feedback from a teacher to a student.</span></span> <span data-ttu-id="1db50-108">Esta propiedad representa la parte de texto de los comentarios junto con la que.</span><span class="sxs-lookup"><span data-stu-id="1db50-108">This property represents both the text part of the feedback along with the who.</span></span>


## <a name="properties"></a><span data-ttu-id="1db50-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1db50-109">Properties</span></span>
| <span data-ttu-id="1db50-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1db50-110">Property</span></span>     | <span data-ttu-id="1db50-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="1db50-111">Type</span></span>   |<span data-ttu-id="1db50-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1db50-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1db50-113">feedbackBy</span><span class="sxs-lookup"><span data-stu-id="1db50-113">feedbackBy</span></span>|[<span data-ttu-id="1db50-114">identitySet</span><span class="sxs-lookup"><span data-stu-id="1db50-114">identitySet</span></span>](identityset.md)|<span data-ttu-id="1db50-115">Usuario que creó los comentarios.</span><span class="sxs-lookup"><span data-stu-id="1db50-115">User who created the feedback.</span></span>|
|<span data-ttu-id="1db50-116">feedbackDateTime</span><span class="sxs-lookup"><span data-stu-id="1db50-116">feedbackDateTime</span></span>|<span data-ttu-id="1db50-117">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1db50-117">DateTimeOffset</span></span>|<span data-ttu-id="1db50-118">Momento en el tiempo cuando se asignó los comentarios.</span><span class="sxs-lookup"><span data-stu-id="1db50-118">Moment in time when the feedback was given.</span></span> <span data-ttu-id="1db50-119">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="1db50-119">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="1db50-120">Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="1db50-120">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="1db50-121">text</span><span class="sxs-lookup"><span data-stu-id="1db50-121">text</span></span>|[<span data-ttu-id="1db50-122">itemBody</span><span class="sxs-lookup"><span data-stu-id="1db50-122">itemBody</span></span>](itembody.md)|<span data-ttu-id="1db50-123">Comentarios.</span><span class="sxs-lookup"><span data-stu-id="1db50-123">Feedback.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="1db50-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1db50-124">JSON representation</span></span>

<span data-ttu-id="1db50-125">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="1db50-125">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationFeedback"
}-->

```json
{
  "feedbackBy": {"@odata.type": "microsoft.graph.identitySet"},
  "feedbackDateTime": "String (timestamp)",
  "text": {"@odata.type": "microsoft.graph.itemBody"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationFeedback resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
