---
title: Tipo de recurso followupFlag
description: 'Permite establecer un indicador en un elemento para el usuario realizar el seguimiento más adelante. '
ms.openlocfilehash: 5aa9d82fc90d7142717ac5ef05f9d837bac371ba
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032155"
---
# <a name="followupflag-resource-type"></a><span data-ttu-id="157d9-103">Tipo de recurso followupFlag</span><span class="sxs-lookup"><span data-stu-id="157d9-103">followupFlag resource type</span></span>


<span data-ttu-id="157d9-104">Permite establecer un indicador en un elemento para el usuario realizar el seguimiento más adelante.</span><span class="sxs-lookup"><span data-stu-id="157d9-104">Allows setting a flag in an item for the user to follow up on later.</span></span> 

## <a name="properties"></a><span data-ttu-id="157d9-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="157d9-105">Properties</span></span>
| <span data-ttu-id="157d9-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="157d9-106">Property</span></span>     | <span data-ttu-id="157d9-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="157d9-107">Type</span></span>   |<span data-ttu-id="157d9-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="157d9-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="157d9-109">completedDateTime</span><span class="sxs-lookup"><span data-stu-id="157d9-109">completedDateTime</span></span>|[<span data-ttu-id="157d9-110">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="157d9-110">dateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="157d9-111">Fecha y hora en que se finalizó el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="157d9-111">The date and time that the follow-up was finished.</span></span>|
|<span data-ttu-id="157d9-112">dueDateTime</span><span class="sxs-lookup"><span data-stu-id="157d9-112">dueDateTime</span></span>|<span data-ttu-id="157d9-113">**dateTimeTimeZone**</span><span class="sxs-lookup"><span data-stu-id="157d9-113">**dateTimeTimeZone**</span></span>|<span data-ttu-id="157d9-114">Fecha y hora en que se va a finalizar el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="157d9-114">The date and time that the follow-up is to be finished.</span></span>|
|<span data-ttu-id="157d9-115">flagStatus</span><span class="sxs-lookup"><span data-stu-id="157d9-115">flagStatus</span></span>|<span data-ttu-id="157d9-116">followupFlagStatus</span><span class="sxs-lookup"><span data-stu-id="157d9-116">followupFlagStatus</span></span>|<span data-ttu-id="157d9-117">Estado del seguimiento de un elemento.</span><span class="sxs-lookup"><span data-stu-id="157d9-117">The status for follow-up for an item.</span></span> <span data-ttu-id="157d9-118">Los valores posibles son: `notFlagged`, `complete` y `flagged`.</span><span class="sxs-lookup"><span data-stu-id="157d9-118">Possible values are `notFlagged`, `complete`, and `flagged`.</span></span>|
|<span data-ttu-id="157d9-119">startDateTime</span><span class="sxs-lookup"><span data-stu-id="157d9-119">startDateTime</span></span>|<span data-ttu-id="157d9-120">**dateTimeTimeZone**</span><span class="sxs-lookup"><span data-stu-id="157d9-120">**dateTimeTimeZone**</span></span>|<span data-ttu-id="157d9-121">Fecha y hora en que va a iniciarse el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="157d9-121">The date and time that the follow-up is to begin.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="157d9-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="157d9-122">JSON representation</span></span>

<span data-ttu-id="157d9-123">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="157d9-123">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.followupFlag"
}-->

```json
{
  "completedDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "dueDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "flagStatus": "String",
  "startDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "followupFlag resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
