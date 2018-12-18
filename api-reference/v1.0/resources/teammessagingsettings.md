---
title: tipo de recurso teamMessagingSettings
description: La configuración de mensajería y menciones en el equipo.
author: nkramer
ms.openlocfilehash: 387c2e3ccedc6f11f17d4868b1b0d3eaf67624fa
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27304553"
---
# <a name="teammessagingsettings-resource-type"></a><span data-ttu-id="e15db-103">tipo de recurso teamMessagingSettings</span><span class="sxs-lookup"><span data-stu-id="e15db-103">teamMessagingSettings resource type</span></span>



<span data-ttu-id="e15db-104">La configuración de mensajería y menciones en el [equipo](team.md).</span><span class="sxs-lookup"><span data-stu-id="e15db-104">Settings to configure messaging and mentions in the [team](team.md).</span></span>

## <a name="properties"></a><span data-ttu-id="e15db-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e15db-105">Properties</span></span>
| <span data-ttu-id="e15db-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e15db-106">Property</span></span>     | <span data-ttu-id="e15db-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="e15db-107">Type</span></span>   |<span data-ttu-id="e15db-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e15db-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e15db-109">allowUserEditMessages</span><span class="sxs-lookup"><span data-stu-id="e15db-109">allowUserEditMessages</span></span>|<span data-ttu-id="e15db-110">Boolean</span><span class="sxs-lookup"><span data-stu-id="e15db-110">Boolean</span></span>|<span data-ttu-id="e15db-111">Si se establece en true, los usuarios puede editar sus mensajes.</span><span class="sxs-lookup"><span data-stu-id="e15db-111">If set to true, users can edit their messages.</span></span>|
|<span data-ttu-id="e15db-112">allowUserDeleteMessages</span><span class="sxs-lookup"><span data-stu-id="e15db-112">allowUserDeleteMessages</span></span>|<span data-ttu-id="e15db-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="e15db-113">Boolean</span></span>|<span data-ttu-id="e15db-114">Si se establece en true, los usuarios puede eliminar sus mensajes.</span><span class="sxs-lookup"><span data-stu-id="e15db-114">If set to true, users can delete their messages.</span></span>|
|<span data-ttu-id="e15db-115">allowOwnerDeleteMessages</span><span class="sxs-lookup"><span data-stu-id="e15db-115">allowOwnerDeleteMessages</span></span>|<span data-ttu-id="e15db-116">Boolean</span><span class="sxs-lookup"><span data-stu-id="e15db-116">Boolean</span></span>|<span data-ttu-id="e15db-117">Si se establece en true, propietarios puede eliminar cualquier mensaje.</span><span class="sxs-lookup"><span data-stu-id="e15db-117">If set to true, owners can delete any message.</span></span>|
|<span data-ttu-id="e15db-118">allowTeamMentions</span><span class="sxs-lookup"><span data-stu-id="e15db-118">allowTeamMentions</span></span>|<span data-ttu-id="e15db-119">Boolean</span><span class="sxs-lookup"><span data-stu-id="e15db-119">Boolean</span></span>|<span data-ttu-id="e15db-120">Si establece en true, se permiten menciones de @team.</span><span class="sxs-lookup"><span data-stu-id="e15db-120">If set to true, @team mentions are allowed.</span></span>|
|<span data-ttu-id="e15db-121">allowChannelMentions</span><span class="sxs-lookup"><span data-stu-id="e15db-121">allowChannelMentions</span></span>|<span data-ttu-id="e15db-122">Boolean</span><span class="sxs-lookup"><span data-stu-id="e15db-122">Boolean</span></span>|<span data-ttu-id="e15db-123">Si establece en true, se permiten menciones de @channel.</span><span class="sxs-lookup"><span data-stu-id="e15db-123">If set to true, @channel mentions are allowed.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="e15db-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e15db-124">JSON representation</span></span>

<span data-ttu-id="e15db-125">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="e15db-125">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamMessagingSettings"
}-->

```json
{
  "allowUserEditMessages": true,
  "allowUserDeleteMessages": true,
  "allowOwnerDeleteMessages": true,
  "allowTeamMentions": true,
  "allowChannelMentions": true    
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "team's messagingSettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
