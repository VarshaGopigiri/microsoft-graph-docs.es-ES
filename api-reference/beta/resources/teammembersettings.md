---
title: tipo de recurso teamMemberSettings
description: Configuración para configurar si los miembros pueden realizar determinadas acciones, por ejemplo, creación de canales y agrega bots, en el equipo.
localization_priority: Normal
author: nkramer
ms.prod: microsoft-teams
ms.openlocfilehash: 3854481e89f04fa727b77c6b4f8699c62a16d739
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27978252"
---
# <a name="teammembersettings-resource-type"></a><span data-ttu-id="d4a6f-103">tipo de recurso teamMemberSettings</span><span class="sxs-lookup"><span data-stu-id="d4a6f-103">teamMemberSettings resource type</span></span>

> <span data-ttu-id="d4a6f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d4a6f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d4a6f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d4a6f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d4a6f-106">Configuración para configurar si los miembros pueden realizar determinadas acciones, por ejemplo, creación de canales y agrega bots, en el [equipo](team.md).</span><span class="sxs-lookup"><span data-stu-id="d4a6f-106">Settings to configure whether members can perform certain actions, for example, create channels and add bots, in the [team](team.md).</span></span>

## <a name="properties"></a><span data-ttu-id="d4a6f-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d4a6f-107">Properties</span></span>
| <span data-ttu-id="d4a6f-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d4a6f-108">Property</span></span>     | <span data-ttu-id="d4a6f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="d4a6f-109">Type</span></span>   |<span data-ttu-id="d4a6f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4a6f-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d4a6f-111">allowCreateUpdateChannels</span><span class="sxs-lookup"><span data-stu-id="d4a6f-111">allowCreateUpdateChannels</span></span>|<span data-ttu-id="d4a6f-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="d4a6f-112">Boolean</span></span>|<span data-ttu-id="d4a6f-113">Si se establece a miembros es true, puede agregar y actualizar los canales.</span><span class="sxs-lookup"><span data-stu-id="d4a6f-113">If set to true, members can add and update channels.</span></span>|
|<span data-ttu-id="d4a6f-114">allowDeleteChannels</span><span class="sxs-lookup"><span data-stu-id="d4a6f-114">allowDeleteChannels</span></span>|<span data-ttu-id="d4a6f-115">Booleano</span><span class="sxs-lookup"><span data-stu-id="d4a6f-115">Boolean</span></span>|<span data-ttu-id="d4a6f-116">Si se establece en true, miembros puede eliminar canales.</span><span class="sxs-lookup"><span data-stu-id="d4a6f-116">If set to true, members can delete channels.</span></span>|
|<span data-ttu-id="d4a6f-117">allowAddRemoveApps</span><span class="sxs-lookup"><span data-stu-id="d4a6f-117">allowAddRemoveApps</span></span>|<span data-ttu-id="d4a6f-118">Booleano</span><span class="sxs-lookup"><span data-stu-id="d4a6f-118">Boolean</span></span>|<span data-ttu-id="d4a6f-119">Si se establece a miembros es true, puede agregar y quitar aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d4a6f-119">If set to true, members can add and remove apps.</span></span>|
|<span data-ttu-id="d4a6f-120">allowCreateUpdateRemoveTabs</span><span class="sxs-lookup"><span data-stu-id="d4a6f-120">allowCreateUpdateRemoveTabs</span></span>|<span data-ttu-id="d4a6f-121">Booleano</span><span class="sxs-lookup"><span data-stu-id="d4a6f-121">Boolean</span></span>|<span data-ttu-id="d4a6f-122">Si se establece en true, miembros puede agregar, actualizar y quitar las fichas.</span><span class="sxs-lookup"><span data-stu-id="d4a6f-122">If set to true, members can add, update, and remove tabs.</span></span> |
|<span data-ttu-id="d4a6f-123">allowCreateUpdateRemoveConnectors</span><span class="sxs-lookup"><span data-stu-id="d4a6f-123">allowCreateUpdateRemoveConnectors</span></span>|<span data-ttu-id="d4a6f-124">Booleano</span><span class="sxs-lookup"><span data-stu-id="d4a6f-124">Boolean</span></span>|<span data-ttu-id="d4a6f-125">Si se establece en true, miembros puede agregar, actualizar y quitar conectores.</span><span class="sxs-lookup"><span data-stu-id="d4a6f-125">If set to true, members can add, update, and remove connectors.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d4a6f-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d4a6f-126">JSON representation</span></span>

<span data-ttu-id="d4a6f-127">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d4a6f-127">The following is a JSON representation of the resource.</span></span>

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
