---
title: Tipo de recurso followupFlag
description: Permite establecer una marca para que el usuario realice más adelante el seguimiento en un elemento. Los elementos admitidos incluyen message y contact.
localization_priority: Normal
ms.openlocfilehash: aa056d141bfac82b9f039ed705f6de49893783fe
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27869383"
---
# <a name="followupflag-resource-type"></a><span data-ttu-id="4ed73-104">Tipo de recurso followupFlag</span><span class="sxs-lookup"><span data-stu-id="4ed73-104">followupFlag resource type</span></span>

> <span data-ttu-id="4ed73-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4ed73-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4ed73-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4ed73-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4ed73-107">Permite establecer una marca para que el usuario realice más adelante el seguimiento en un elemento.</span><span class="sxs-lookup"><span data-stu-id="4ed73-107">Allows setting a flag for the user to follow up on an item later.</span></span> <span data-ttu-id="4ed73-108">Los elementos admitidos incluyen [message](message.md) y [contact](contact.md).</span><span class="sxs-lookup"><span data-stu-id="4ed73-108">Supported items include [message](message.md) and [contact](contact.md).</span></span>

## <a name="properties"></a><span data-ttu-id="4ed73-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4ed73-109">Properties</span></span>
| <span data-ttu-id="4ed73-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4ed73-110">Property</span></span>     | <span data-ttu-id="4ed73-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="4ed73-111">Type</span></span>   |<span data-ttu-id="4ed73-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4ed73-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4ed73-113">completedDateTime</span><span class="sxs-lookup"><span data-stu-id="4ed73-113">completedDateTime</span></span>|[<span data-ttu-id="4ed73-114">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="4ed73-114">dateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="4ed73-115">Fecha y hora en que se finalizó el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="4ed73-115">The date and time that the follow-up was finished.</span></span>|
|<span data-ttu-id="4ed73-116">dueDateTime</span><span class="sxs-lookup"><span data-stu-id="4ed73-116">dueDateTime</span></span>|<span data-ttu-id="4ed73-117">**dateTimeTimeZone**</span><span class="sxs-lookup"><span data-stu-id="4ed73-117">**dateTimeTimeZone**</span></span>|<span data-ttu-id="4ed73-118">Fecha y hora en que se va a finalizar el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="4ed73-118">The date and time that the follow-up is to be finished.</span></span>|
|<span data-ttu-id="4ed73-119">flagStatus</span><span class="sxs-lookup"><span data-stu-id="4ed73-119">flagStatus</span></span>|<span data-ttu-id="4ed73-120">String</span><span class="sxs-lookup"><span data-stu-id="4ed73-120">String</span></span>|<span data-ttu-id="4ed73-121">Estado del seguimiento de un elemento.</span><span class="sxs-lookup"><span data-stu-id="4ed73-121">The status for follow-up for an item.</span></span> <span data-ttu-id="4ed73-122">Los valores posibles son: `notFlagged`, `complete` y `flagged`.</span><span class="sxs-lookup"><span data-stu-id="4ed73-122">Possible values are `notFlagged`, `complete`, and `flagged`.</span></span>|
|<span data-ttu-id="4ed73-123">startDateTime</span><span class="sxs-lookup"><span data-stu-id="4ed73-123">startDateTime</span></span>|<span data-ttu-id="4ed73-124">**dateTimeTimeZone**</span><span class="sxs-lookup"><span data-stu-id="4ed73-124">**dateTimeTimeZone**</span></span>|<span data-ttu-id="4ed73-125">Fecha y hora en que va a iniciarse el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="4ed73-125">The date and time that the follow-up is to begin.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="4ed73-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4ed73-126">JSON representation</span></span>

<span data-ttu-id="4ed73-127">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="4ed73-127">Here is a JSON representation of the resource</span></span>

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
