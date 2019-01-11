---
title: tipo de recurso teamMemberSettings
description: Configuración para configurar si los miembros pueden realizar determinadas acciones, por ejemplo, creación de canales y agrega bots, en el equipo.
localization_priority: Normal
ms.openlocfilehash: 7b63bce5bc298f7d9599d8c6146d7962d319c79f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27826071"
---
# <a name="teammembersettings-resource-type"></a><span data-ttu-id="d6a9d-103">tipo de recurso teamMemberSettings</span><span class="sxs-lookup"><span data-stu-id="d6a9d-103">teamMemberSettings resource type</span></span>



<span data-ttu-id="d6a9d-104">Configuración para configurar si los miembros pueden realizar determinadas acciones, por ejemplo, creación de canales y agrega bots, en el [equipo](team.md).</span><span class="sxs-lookup"><span data-stu-id="d6a9d-104">Settings to configure whether members can perform certain actions, for example, create channels and add bots, in the [team](team.md).</span></span>

## <a name="properties"></a><span data-ttu-id="d6a9d-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d6a9d-105">Properties</span></span>
| <span data-ttu-id="d6a9d-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d6a9d-106">Property</span></span>     | <span data-ttu-id="d6a9d-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6a9d-107">Type</span></span>   |<span data-ttu-id="d6a9d-108">Description</span><span class="sxs-lookup"><span data-stu-id="d6a9d-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d6a9d-109">allowCreateUpdateChannels</span><span class="sxs-lookup"><span data-stu-id="d6a9d-109">allowCreateUpdateChannels</span></span>|<span data-ttu-id="d6a9d-110">Booleano</span><span class="sxs-lookup"><span data-stu-id="d6a9d-110">Boolean</span></span>|<span data-ttu-id="d6a9d-111">Si se establece a miembros es true, puede agregar y actualizar los canales.</span><span class="sxs-lookup"><span data-stu-id="d6a9d-111">If set to true, members can add and update channels.</span></span>|
|<span data-ttu-id="d6a9d-112">allowDeleteChannels</span><span class="sxs-lookup"><span data-stu-id="d6a9d-112">allowDeleteChannels</span></span>|<span data-ttu-id="d6a9d-113">Booleano</span><span class="sxs-lookup"><span data-stu-id="d6a9d-113">Boolean</span></span>|<span data-ttu-id="d6a9d-114">Si se establece en true, miembros puede eliminar canales.</span><span class="sxs-lookup"><span data-stu-id="d6a9d-114">If set to true, members can delete channels.</span></span>|
|<span data-ttu-id="d6a9d-115">allowAddRemoveApps</span><span class="sxs-lookup"><span data-stu-id="d6a9d-115">allowAddRemoveApps</span></span>|<span data-ttu-id="d6a9d-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="d6a9d-116">Boolean</span></span>|<span data-ttu-id="d6a9d-117">Si se establece a miembros es true, puede agregar y quitar aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d6a9d-117">If set to true, members can add and remove apps.</span></span>|
|<span data-ttu-id="d6a9d-118">allowCreateUpdateRemoveTabs</span><span class="sxs-lookup"><span data-stu-id="d6a9d-118">allowCreateUpdateRemoveTabs</span></span>|<span data-ttu-id="d6a9d-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="d6a9d-119">Boolean</span></span>|<span data-ttu-id="d6a9d-120">Si se establece en true, miembros puede agregar, actualizar y quitar las fichas.</span><span class="sxs-lookup"><span data-stu-id="d6a9d-120">If set to true, members can add, update, and remove tabs.</span></span> |
|<span data-ttu-id="d6a9d-121">allowCreateUpdateRemoveConnectors</span><span class="sxs-lookup"><span data-stu-id="d6a9d-121">allowCreateUpdateRemoveConnectors</span></span>|<span data-ttu-id="d6a9d-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="d6a9d-122">Boolean</span></span>|<span data-ttu-id="d6a9d-123">Si se establece en true, miembros puede agregar, actualizar y quitar conectores.</span><span class="sxs-lookup"><span data-stu-id="d6a9d-123">If set to true, members can add, update, and remove connectors.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d6a9d-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d6a9d-124">JSON representation</span></span>

<span data-ttu-id="d6a9d-125">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d6a9d-125">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamMemberSettings"
}-->

```json
{
  "allowCreateUpdateChannels": true,
  "allowDeleteChannels": true,
  "allowAddRemoveApps": true,
  "allowCreateUpdateRemoveTabs": true,
  "allowCreateUpdateRemoveConnectors": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "team's memberSettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
