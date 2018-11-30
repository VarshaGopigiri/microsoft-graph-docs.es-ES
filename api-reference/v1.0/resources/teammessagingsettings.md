---
title: tipo de recurso teamMessagingSettings
description: La configuración de mensajería y menciones en el equipo.
ms.openlocfilehash: 6d1ca12b473f2773d4f56e12405b17e21b0bd0ca
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029783"
---
# <a name="teammessagingsettings-resource-type"></a><span data-ttu-id="e2c56-103">tipo de recurso teamMessagingSettings</span><span class="sxs-lookup"><span data-stu-id="e2c56-103">teamMessagingSettings resource type</span></span>



<span data-ttu-id="e2c56-104">La configuración de mensajería y menciones en el [equipo](team.md).</span><span class="sxs-lookup"><span data-stu-id="e2c56-104">Settings to configure messaging and mentions in the [team](team.md).</span></span>

## <a name="properties"></a><span data-ttu-id="e2c56-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e2c56-105">Properties</span></span>
| <span data-ttu-id="e2c56-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e2c56-106">Property</span></span>     | <span data-ttu-id="e2c56-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="e2c56-107">Type</span></span>   |<span data-ttu-id="e2c56-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2c56-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e2c56-109">allowUserEditMessages</span><span class="sxs-lookup"><span data-stu-id="e2c56-109">allowUserEditMessages</span></span>|<span data-ttu-id="e2c56-110">Booleano</span><span class="sxs-lookup"><span data-stu-id="e2c56-110">Boolean</span></span>|<span data-ttu-id="e2c56-111">Si se establece en true, los usuarios puede editar sus mensajes.</span><span class="sxs-lookup"><span data-stu-id="e2c56-111">If set to true, users can edit their messages.</span></span>|
|<span data-ttu-id="e2c56-112">allowUserDeleteMessages</span><span class="sxs-lookup"><span data-stu-id="e2c56-112">allowUserDeleteMessages</span></span>|<span data-ttu-id="e2c56-113">Booleano</span><span class="sxs-lookup"><span data-stu-id="e2c56-113">Boolean</span></span>|<span data-ttu-id="e2c56-114">Si se establece en true, los usuarios puede eliminar sus mensajes.</span><span class="sxs-lookup"><span data-stu-id="e2c56-114">If set to true, users can delete their messages.</span></span>|
|<span data-ttu-id="e2c56-115">allowOwnerDeleteMessages</span><span class="sxs-lookup"><span data-stu-id="e2c56-115">allowOwnerDeleteMessages</span></span>|<span data-ttu-id="e2c56-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="e2c56-116">Boolean</span></span>|<span data-ttu-id="e2c56-117">Si se establece en true, propietarios puede eliminar cualquier mensaje.</span><span class="sxs-lookup"><span data-stu-id="e2c56-117">If set to true, owners can delete any message.</span></span>|
|<span data-ttu-id="e2c56-118">allowTeamMentions</span><span class="sxs-lookup"><span data-stu-id="e2c56-118">allowTeamMentions</span></span>|<span data-ttu-id="e2c56-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="e2c56-119">Boolean</span></span>|<span data-ttu-id="e2c56-120">Si establece en true, se permiten menciones de @team.</span><span class="sxs-lookup"><span data-stu-id="e2c56-120">If set to true, @team mentions are allowed.</span></span>|
|<span data-ttu-id="e2c56-121">allowChannelMentions</span><span class="sxs-lookup"><span data-stu-id="e2c56-121">allowChannelMentions</span></span>|<span data-ttu-id="e2c56-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="e2c56-122">Boolean</span></span>|<span data-ttu-id="e2c56-123">Si establece en true, se permiten menciones de @channel.</span><span class="sxs-lookup"><span data-stu-id="e2c56-123">If set to true, @channel mentions are allowed.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="e2c56-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e2c56-124">JSON representation</span></span>

<span data-ttu-id="e2c56-125">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="e2c56-125">The following is a JSON representation of the resource.</span></span>

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
