---
title: tipo de recurso teamGuestSettings
description: Configuración para configurar si los invitados pueden crear, actualizar o eliminar los canales en el equipo.
localization_priority: Normal
author: nkramer
ms.prod: microsoft-teams
ms.openlocfilehash: d601ac704734f4c46e8b7bef9e8d3feb45905384
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27987296"
---
# <a name="teamguestsettings-resource-type"></a><span data-ttu-id="2b9f3-103">tipo de recurso teamGuestSettings</span><span class="sxs-lookup"><span data-stu-id="2b9f3-103">teamGuestSettings resource type</span></span>

> <span data-ttu-id="2b9f3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2b9f3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2b9f3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2b9f3-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2b9f3-106">Configuración para configurar si los invitados pueden crear, actualizar o eliminar los canales en el [equipo](team.md).</span><span class="sxs-lookup"><span data-stu-id="2b9f3-106">Settings to configure whether guests can create, update, or delete channels in the [team](team.md).</span></span>

## <a name="properties"></a><span data-ttu-id="2b9f3-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2b9f3-107">Properties</span></span>
| <span data-ttu-id="2b9f3-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2b9f3-108">Property</span></span>     | <span data-ttu-id="2b9f3-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="2b9f3-109">Type</span></span>   |<span data-ttu-id="2b9f3-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b9f3-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2b9f3-111">allowCreateUpdateChannels</span><span class="sxs-lookup"><span data-stu-id="2b9f3-111">allowCreateUpdateChannels</span></span>|<span data-ttu-id="2b9f3-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="2b9f3-112">Boolean</span></span>|<span data-ttu-id="2b9f3-113">Si se establece en true, invitados puede agregar y actualizar los canales.</span><span class="sxs-lookup"><span data-stu-id="2b9f3-113">If set to true, guests can add and update channels.</span></span>|
|<span data-ttu-id="2b9f3-114">allowDeleteChannels</span><span class="sxs-lookup"><span data-stu-id="2b9f3-114">allowDeleteChannels</span></span>|<span data-ttu-id="2b9f3-115">Booleano</span><span class="sxs-lookup"><span data-stu-id="2b9f3-115">Boolean</span></span>|<span data-ttu-id="2b9f3-116">Si se establece en true, invitados puede eliminar canales.</span><span class="sxs-lookup"><span data-stu-id="2b9f3-116">If set to true, guests can delete channels.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="2b9f3-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2b9f3-117">JSON representation</span></span>

<span data-ttu-id="2b9f3-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="2b9f3-118">The following is a JSON representation of the resource.</span></span>

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
