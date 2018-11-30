---
title: tipo de recurso teamMemberSettings
description: Configuración para configurar si los miembros pueden realizar determinadas acciones, por ejemplo, creación de canales y agrega bots, en el equipo.
ms.openlocfilehash: 74d88e1d87c65745fe98da9b1ee21b26824dc4e6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031348"
---
# <a name="teammembersettings-resource-type"></a><span data-ttu-id="3c611-103">tipo de recurso teamMemberSettings</span><span class="sxs-lookup"><span data-stu-id="3c611-103">teamMemberSettings resource type</span></span>



<span data-ttu-id="3c611-104">Configuración para configurar si los miembros pueden realizar determinadas acciones, por ejemplo, creación de canales y agrega bots, en el [equipo](team.md).</span><span class="sxs-lookup"><span data-stu-id="3c611-104">Settings to configure whether members can perform certain actions, for example, create channels and add bots, in the [team](team.md).</span></span>

## <a name="properties"></a><span data-ttu-id="3c611-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3c611-105">Properties</span></span>
| <span data-ttu-id="3c611-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3c611-106">Property</span></span>     | <span data-ttu-id="3c611-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="3c611-107">Type</span></span>   |<span data-ttu-id="3c611-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c611-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3c611-109">allowCreateUpdateChannels</span><span class="sxs-lookup"><span data-stu-id="3c611-109">allowCreateUpdateChannels</span></span>|<span data-ttu-id="3c611-110">Booleano</span><span class="sxs-lookup"><span data-stu-id="3c611-110">Boolean</span></span>|<span data-ttu-id="3c611-111">Si se establece a miembros es true, puede agregar y actualizar los canales.</span><span class="sxs-lookup"><span data-stu-id="3c611-111">If set to true, members can add and update channels.</span></span>|
|<span data-ttu-id="3c611-112">allowDeleteChannels</span><span class="sxs-lookup"><span data-stu-id="3c611-112">allowDeleteChannels</span></span>|<span data-ttu-id="3c611-113">Booleano</span><span class="sxs-lookup"><span data-stu-id="3c611-113">Boolean</span></span>|<span data-ttu-id="3c611-114">Si se establece en true, miembros puede eliminar canales.</span><span class="sxs-lookup"><span data-stu-id="3c611-114">If set to true, members can delete channels.</span></span>|
|<span data-ttu-id="3c611-115">allowAddRemoveApps</span><span class="sxs-lookup"><span data-stu-id="3c611-115">allowAddRemoveApps</span></span>|<span data-ttu-id="3c611-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="3c611-116">Boolean</span></span>|<span data-ttu-id="3c611-117">Si se establece a miembros es true, puede agregar y quitar aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="3c611-117">If set to true, members can add and remove apps.</span></span>|
|<span data-ttu-id="3c611-118">allowCreateUpdateRemoveTabs</span><span class="sxs-lookup"><span data-stu-id="3c611-118">allowCreateUpdateRemoveTabs</span></span>|<span data-ttu-id="3c611-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="3c611-119">Boolean</span></span>|<span data-ttu-id="3c611-120">Si se establece en true, miembros puede agregar, actualizar y quitar las fichas.</span><span class="sxs-lookup"><span data-stu-id="3c611-120">If set to true, members can add, update, and remove tabs.</span></span> |
|<span data-ttu-id="3c611-121">allowCreateUpdateRemoveConnectors</span><span class="sxs-lookup"><span data-stu-id="3c611-121">allowCreateUpdateRemoveConnectors</span></span>|<span data-ttu-id="3c611-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="3c611-122">Boolean</span></span>|<span data-ttu-id="3c611-123">Si se establece en true, miembros puede agregar, actualizar y quitar conectores.</span><span class="sxs-lookup"><span data-stu-id="3c611-123">If set to true, members can add, update, and remove connectors.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="3c611-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3c611-124">JSON representation</span></span>

<span data-ttu-id="3c611-125">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="3c611-125">The following is a JSON representation of the resource.</span></span>

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
