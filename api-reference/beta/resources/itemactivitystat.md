---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: ItemActivityStat
ms.openlocfilehash: 067cf88773b5f5d69b2b3538a2ddeab6741631a8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083469"
---
# <a name="itemactivitystat-resource-type"></a><span data-ttu-id="5aa75-102">tipo de recurso itemActivityStat</span><span class="sxs-lookup"><span data-stu-id="5aa75-102">itemActivityStat resource type</span></span>

> <span data-ttu-id="5aa75-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5aa75-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5aa75-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5aa75-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5aa75-105">El recurso **itemActivityStat** proporciona información acerca de las actividades que tuvieron lugar dentro de un intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="5aa75-105">The **itemActivityStat** resource provides information about activities that took place within an interval of time.</span></span>

## <a name="json-representation"></a><span data-ttu-id="5aa75-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5aa75-106">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "baseType": "microsoft.graph.entity",
  "@type": "microsoft.graph.itemActivityStat",
}-->

```json
{
  "activities": [{"@odata.type": "microsoft.graph.itemActivity"}],
  "incompleteData": {"@odata.type": "microsoft.graph.incompleteData"},
  "isTrending": true,
  "startDateTime": "String (timestamp)",
  "endDateTime": "String (timestamp)",
  "create": {"@odata.type": "microsoft.graph.itemActionStat"},
  "delete": {"@odata.type": "microsoft.graph.itemActionStat"},
  "edit": {"@odata.type": "microsoft.graph.itemActionStat"},
  "move": {"@odata.type": "microsoft.graph.itemActionStat"},
  "access": {"@odata.type": "microsoft.graph.itemActionStat"}
}
```

## <a name="properties"></a><span data-ttu-id="5aa75-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5aa75-107">Properties</span></span>

| <span data-ttu-id="5aa75-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5aa75-108">Property</span></span>         | <span data-ttu-id="5aa75-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="5aa75-109">Type</span></span>                    | <span data-ttu-id="5aa75-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5aa75-110">Description</span></span>
|:-----------------|:------------------------|:----------------------------------------
| <span data-ttu-id="5aa75-111">incompleteData</span><span class="sxs-lookup"><span data-stu-id="5aa75-111">incompleteData</span></span>   | <span data-ttu-id="5aa75-112">[incompleteData][]</span><span class="sxs-lookup"><span data-stu-id="5aa75-112">[incompleteData][]</span></span>      | <span data-ttu-id="5aa75-113">Indica que las estadísticas de este intervalo están basadas en datos incompletos.</span><span class="sxs-lookup"><span data-stu-id="5aa75-113">Indicates that the statistics in this interval are based on incomplete data.</span></span> <span data-ttu-id="5aa75-114">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5aa75-114">Read-only.</span></span>
| <span data-ttu-id="5aa75-115">isTrending</span><span class="sxs-lookup"><span data-stu-id="5aa75-115">isTrending</span></span>       | <span data-ttu-id="5aa75-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="5aa75-116">Boolean</span></span>                 | <span data-ttu-id="5aa75-117">Indica si el elemento es "tendencias".</span><span class="sxs-lookup"><span data-stu-id="5aa75-117">Indicates whether the item is "trending."</span></span> <span data-ttu-id="5aa75-118">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5aa75-118">Read-only.</span></span>
| <span data-ttu-id="5aa75-119">startDateTime</span><span class="sxs-lookup"><span data-stu-id="5aa75-119">startDateTime</span></span>    | <span data-ttu-id="5aa75-120">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5aa75-120">DateTimeOffset</span></span>          | <span data-ttu-id="5aa75-121">Cuando se inicia el intervalo.</span><span class="sxs-lookup"><span data-stu-id="5aa75-121">When the interval starts.</span></span> <span data-ttu-id="5aa75-122">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5aa75-122">Read-only.</span></span>
| <span data-ttu-id="5aa75-123">endDateTime</span><span class="sxs-lookup"><span data-stu-id="5aa75-123">endDateTime</span></span>      | <span data-ttu-id="5aa75-124">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5aa75-124">DateTimeOffset</span></span>          | <span data-ttu-id="5aa75-125">Cuando finaliza el intervalo.</span><span class="sxs-lookup"><span data-stu-id="5aa75-125">When the interval ends.</span></span> <span data-ttu-id="5aa75-126">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5aa75-126">Read-only.</span></span>
| <span data-ttu-id="5aa75-127">create</span><span class="sxs-lookup"><span data-stu-id="5aa75-127">create</span></span>           | <span data-ttu-id="5aa75-128">[itemActionStat][]</span><span class="sxs-lookup"><span data-stu-id="5aa75-128">[itemActionStat][]</span></span>      | <span data-ttu-id="5aa75-129">Estadísticas sobre las acciones de **crear** en este intervalo.</span><span class="sxs-lookup"><span data-stu-id="5aa75-129">Statistics about the **create** actions in this interval.</span></span> <span data-ttu-id="5aa75-130">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5aa75-130">Read-only.</span></span>
| <span data-ttu-id="5aa75-131">edit</span><span class="sxs-lookup"><span data-stu-id="5aa75-131">edit</span></span>             | <span data-ttu-id="5aa75-132">[itemActionStat][]</span><span class="sxs-lookup"><span data-stu-id="5aa75-132">[itemActionStat][]</span></span>      | <span data-ttu-id="5aa75-133">Estadísticas sobre las acciones de **Edición** en este intervalo.</span><span class="sxs-lookup"><span data-stu-id="5aa75-133">Statistics about the **edit** actions in this interval.</span></span> <span data-ttu-id="5aa75-134">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5aa75-134">Read-only.</span></span>
| <span data-ttu-id="5aa75-135">delete</span><span class="sxs-lookup"><span data-stu-id="5aa75-135">delete</span></span>           | <span data-ttu-id="5aa75-136">[itemActionStat][]</span><span class="sxs-lookup"><span data-stu-id="5aa75-136">[itemActionStat][]</span></span>      | <span data-ttu-id="5aa75-137">Estadísticas sobre las acciones de **eliminación** en este intervalo.</span><span class="sxs-lookup"><span data-stu-id="5aa75-137">Statistics about the **delete** actions in this interval.</span></span> <span data-ttu-id="5aa75-138">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5aa75-138">Read-only.</span></span>
| <span data-ttu-id="5aa75-139">move</span><span class="sxs-lookup"><span data-stu-id="5aa75-139">move</span></span>             | <span data-ttu-id="5aa75-140">[itemActionStat][]</span><span class="sxs-lookup"><span data-stu-id="5aa75-140">[itemActionStat][]</span></span>      | <span data-ttu-id="5aa75-141">Estadísticas sobre las acciones de **mover** en este intervalo.</span><span class="sxs-lookup"><span data-stu-id="5aa75-141">Statistics about the **move** actions in this interval.</span></span> <span data-ttu-id="5aa75-142">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5aa75-142">Read-only.</span></span>
| <span data-ttu-id="5aa75-143">Access</span><span class="sxs-lookup"><span data-stu-id="5aa75-143">access</span></span>           | <span data-ttu-id="5aa75-144">[itemActionStat][]</span><span class="sxs-lookup"><span data-stu-id="5aa75-144">[itemActionStat][]</span></span>      | <span data-ttu-id="5aa75-145">Estadísticas sobre las acciones de **acceso** en este intervalo.</span><span class="sxs-lookup"><span data-stu-id="5aa75-145">Statistics about the **access** actions in this interval.</span></span> <span data-ttu-id="5aa75-146">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5aa75-146">Read-only.</span></span>

[itemActionStat]: itemactionstat.md
[incompleteData]: incompletedata.md

## <a name="relationships"></a><span data-ttu-id="5aa75-149">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5aa75-149">Relationships</span></span>

| <span data-ttu-id="5aa75-150">Nombre de la relación</span><span class="sxs-lookup"><span data-stu-id="5aa75-150">Relationship name</span></span> | <span data-ttu-id="5aa75-151">Tipo</span><span class="sxs-lookup"><span data-stu-id="5aa75-151">Type</span></span>                        | <span data-ttu-id="5aa75-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="5aa75-152">Description</span></span>
|:------------------|:----------------------------|:---------------------------
| <span data-ttu-id="5aa75-153">activities</span><span class="sxs-lookup"><span data-stu-id="5aa75-153">activities</span></span>        | <span data-ttu-id="5aa75-154">Colección [itemActivity][]</span><span class="sxs-lookup"><span data-stu-id="5aa75-154">[itemActivity][] collection</span></span> | <span data-ttu-id="5aa75-155">Expone la **itemActivities** representado en este recurso **itemActivityStat** .</span><span class="sxs-lookup"><span data-stu-id="5aa75-155">Exposes the **itemActivities** represented in this **itemActivityStat** resource.</span></span>

[itemActivity]: itemactivity.md

## <a name="remarks"></a><span data-ttu-id="5aa75-157">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5aa75-157">Remarks</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The ItemActivityStat object provides information about activities that took place on an item.",
  "keywords": "activities,activity,action,analytics",
  "section": "documentation",
  "tocPath": "Resources/ItemActivityStat"
} -->
