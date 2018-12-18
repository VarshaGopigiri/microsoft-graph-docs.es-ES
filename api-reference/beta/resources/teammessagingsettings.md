---
title: tipo de recurso teamMessagingSettings
description: La configuración de mensajería y menciones en el equipo.
author: nkramer
ms.openlocfilehash: 94a102e6d0937651c990e61f4895c715b3c4bd95
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27344250"
---
# <a name="teammessagingsettings-resource-type"></a><span data-ttu-id="46069-103">tipo de recurso teamMessagingSettings</span><span class="sxs-lookup"><span data-stu-id="46069-103">teamMessagingSettings resource type</span></span>

> <span data-ttu-id="46069-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="46069-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="46069-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="46069-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="46069-106">La configuración de mensajería y menciones en el [equipo](team.md).</span><span class="sxs-lookup"><span data-stu-id="46069-106">Settings to configure messaging and mentions in the [team](team.md).</span></span>

## <a name="properties"></a><span data-ttu-id="46069-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="46069-107">Properties</span></span>
| <span data-ttu-id="46069-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="46069-108">Property</span></span>     | <span data-ttu-id="46069-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="46069-109">Type</span></span>   |<span data-ttu-id="46069-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="46069-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="46069-111">allowUserEditMessages</span><span class="sxs-lookup"><span data-stu-id="46069-111">allowUserEditMessages</span></span>|<span data-ttu-id="46069-112">Boolean</span><span class="sxs-lookup"><span data-stu-id="46069-112">Boolean</span></span>|<span data-ttu-id="46069-113">Si se establece en true, los usuarios puede editar sus mensajes.</span><span class="sxs-lookup"><span data-stu-id="46069-113">If set to true, users can edit their messages.</span></span>|
|<span data-ttu-id="46069-114">allowUserDeleteMessages</span><span class="sxs-lookup"><span data-stu-id="46069-114">allowUserDeleteMessages</span></span>|<span data-ttu-id="46069-115">Boolean</span><span class="sxs-lookup"><span data-stu-id="46069-115">Boolean</span></span>|<span data-ttu-id="46069-116">Si se establece en true, los usuarios puede eliminar sus mensajes.</span><span class="sxs-lookup"><span data-stu-id="46069-116">If set to true, users can delete their messages.</span></span>|
|<span data-ttu-id="46069-117">allowOwnerDeleteMessages</span><span class="sxs-lookup"><span data-stu-id="46069-117">allowOwnerDeleteMessages</span></span>|<span data-ttu-id="46069-118">Boolean</span><span class="sxs-lookup"><span data-stu-id="46069-118">Boolean</span></span>|<span data-ttu-id="46069-119">Si se establece en true, propietarios puede eliminar cualquier mensaje.</span><span class="sxs-lookup"><span data-stu-id="46069-119">If set to true, owners can delete any message.</span></span>|
|<span data-ttu-id="46069-120">allowTeamMentions</span><span class="sxs-lookup"><span data-stu-id="46069-120">allowTeamMentions</span></span>|<span data-ttu-id="46069-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="46069-121">Boolean</span></span>|<span data-ttu-id="46069-122">Si establece en true, se permiten menciones de @team.</span><span class="sxs-lookup"><span data-stu-id="46069-122">If set to true, @team mentions are allowed.</span></span>|
|<span data-ttu-id="46069-123">allowChannelMentions</span><span class="sxs-lookup"><span data-stu-id="46069-123">allowChannelMentions</span></span>|<span data-ttu-id="46069-124">Boolean</span><span class="sxs-lookup"><span data-stu-id="46069-124">Boolean</span></span>|<span data-ttu-id="46069-125">Si establece en true, se permiten menciones de @channel.</span><span class="sxs-lookup"><span data-stu-id="46069-125">If set to true, @channel mentions are allowed.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="46069-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="46069-126">JSON representation</span></span>

<span data-ttu-id="46069-127">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="46069-127">The following is a JSON representation of the resource.</span></span>

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
