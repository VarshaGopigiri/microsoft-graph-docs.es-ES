---
title: tipo de recurso teamGuestSettings
description: Configuración para configurar si los invitados pueden crear, actualizar o eliminar los canales en el equipo.
localization_priority: Normal
ms.openlocfilehash: f0947101fc8de83d1a56ffa922d9b1e2d79d520f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27844880"
---
# <a name="teamguestsettings-resource-type"></a><span data-ttu-id="057c0-103">tipo de recurso teamGuestSettings</span><span class="sxs-lookup"><span data-stu-id="057c0-103">teamGuestSettings resource type</span></span>



<span data-ttu-id="057c0-104">Configuración para configurar si los invitados pueden crear, actualizar o eliminar los canales en el [equipo](team.md).</span><span class="sxs-lookup"><span data-stu-id="057c0-104">Settings to configure whether guests can create, update, or delete channels in the [team](team.md).</span></span>

## <a name="properties"></a><span data-ttu-id="057c0-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="057c0-105">Properties</span></span>
| <span data-ttu-id="057c0-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="057c0-106">Property</span></span>     | <span data-ttu-id="057c0-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="057c0-107">Type</span></span>   |<span data-ttu-id="057c0-108">Description</span><span class="sxs-lookup"><span data-stu-id="057c0-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="057c0-109">allowCreateUpdateChannels</span><span class="sxs-lookup"><span data-stu-id="057c0-109">allowCreateUpdateChannels</span></span>|<span data-ttu-id="057c0-110">Booleano</span><span class="sxs-lookup"><span data-stu-id="057c0-110">Boolean</span></span>|<span data-ttu-id="057c0-111">Si se establece en true, invitados puede agregar y actualizar los canales.</span><span class="sxs-lookup"><span data-stu-id="057c0-111">If set to true, guests can add and update channels.</span></span>|
|<span data-ttu-id="057c0-112">allowDeleteChannels</span><span class="sxs-lookup"><span data-stu-id="057c0-112">allowDeleteChannels</span></span>|<span data-ttu-id="057c0-113">Booleano</span><span class="sxs-lookup"><span data-stu-id="057c0-113">Boolean</span></span>|<span data-ttu-id="057c0-114">Si se establece en true, invitados puede eliminar canales.</span><span class="sxs-lookup"><span data-stu-id="057c0-114">If set to true, guests can delete channels.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="057c0-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="057c0-115">JSON representation</span></span>

<span data-ttu-id="057c0-116">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="057c0-116">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamGuestSettings"
}-->

```json
{
  "allowCreateUpdateChannels": true,
  "allowDeleteChannels": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "team's guestSettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
