---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: ItemActivityStat
localization_priority: Normal
ms.openlocfilehash: d0917d0100d33abee1095e2a7d06a4732d382937
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27854253"
---
# <a name="itemactivitystat-resource-type"></a><span data-ttu-id="ff958-102">tipo de recurso itemActivityStat</span><span class="sxs-lookup"><span data-stu-id="ff958-102">itemActivityStat resource type</span></span>

> <span data-ttu-id="ff958-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ff958-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ff958-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ff958-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ff958-105">El recurso **itemActivityStat** proporciona información acerca de las actividades que tuvieron lugar dentro de un intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="ff958-105">The **itemActivityStat** resource provides information about activities that took place within an interval of time.</span></span>

## <a name="json-representation"></a><span data-ttu-id="ff958-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ff958-106">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="ff958-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ff958-107">Properties</span></span>

| <span data-ttu-id="ff958-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ff958-108">Property</span></span>         | <span data-ttu-id="ff958-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="ff958-109">Type</span></span>                    | <span data-ttu-id="ff958-110">Description</span><span class="sxs-lookup"><span data-stu-id="ff958-110">Description</span></span>
|:-----------------|:------------------------|:----------------------------------------
| <span data-ttu-id="ff958-111">incompleteData</span><span class="sxs-lookup"><span data-stu-id="ff958-111">incompleteData</span></span>   | <span data-ttu-id="ff958-112">[incompleteData][]</span><span class="sxs-lookup"><span data-stu-id="ff958-112">[incompleteData][]</span></span>      | <span data-ttu-id="ff958-113">Indica que las estadísticas de este intervalo están basadas en datos incompletos.</span><span class="sxs-lookup"><span data-stu-id="ff958-113">Indicates that the statistics in this interval are based on incomplete data.</span></span> <span data-ttu-id="ff958-114">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ff958-114">Read-only.</span></span>
| <span data-ttu-id="ff958-115">isTrending</span><span class="sxs-lookup"><span data-stu-id="ff958-115">isTrending</span></span>       | <span data-ttu-id="ff958-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="ff958-116">Boolean</span></span>                 | <span data-ttu-id="ff958-117">Indica si el elemento es "tendencias".</span><span class="sxs-lookup"><span data-stu-id="ff958-117">Indicates whether the item is "trending."</span></span> <span data-ttu-id="ff958-118">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ff958-118">Read-only.</span></span>
| <span data-ttu-id="ff958-119">startDateTime</span><span class="sxs-lookup"><span data-stu-id="ff958-119">startDateTime</span></span>    | <span data-ttu-id="ff958-120">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ff958-120">DateTimeOffset</span></span>          | <span data-ttu-id="ff958-121">Cuando se inicia el intervalo.</span><span class="sxs-lookup"><span data-stu-id="ff958-121">When the interval starts.</span></span> <span data-ttu-id="ff958-122">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ff958-122">Read-only.</span></span>
| <span data-ttu-id="ff958-123">endDateTime</span><span class="sxs-lookup"><span data-stu-id="ff958-123">endDateTime</span></span>      | <span data-ttu-id="ff958-124">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ff958-124">DateTimeOffset</span></span>          | <span data-ttu-id="ff958-125">Cuando finaliza el intervalo.</span><span class="sxs-lookup"><span data-stu-id="ff958-125">When the interval ends.</span></span> <span data-ttu-id="ff958-126">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ff958-126">Read-only.</span></span>
| <span data-ttu-id="ff958-127">create</span><span class="sxs-lookup"><span data-stu-id="ff958-127">create</span></span>           | <span data-ttu-id="ff958-128">[itemActionStat][]</span><span class="sxs-lookup"><span data-stu-id="ff958-128">[itemActionStat][]</span></span>      | <span data-ttu-id="ff958-129">Estadísticas sobre las acciones de **crear** en este intervalo.</span><span class="sxs-lookup"><span data-stu-id="ff958-129">Statistics about the **create** actions in this interval.</span></span> <span data-ttu-id="ff958-130">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ff958-130">Read-only.</span></span>
| <span data-ttu-id="ff958-131">edit</span><span class="sxs-lookup"><span data-stu-id="ff958-131">edit</span></span>             | <span data-ttu-id="ff958-132">[itemActionStat][]</span><span class="sxs-lookup"><span data-stu-id="ff958-132">[itemActionStat][]</span></span>      | <span data-ttu-id="ff958-133">Estadísticas sobre las acciones de **Edición** en este intervalo.</span><span class="sxs-lookup"><span data-stu-id="ff958-133">Statistics about the **edit** actions in this interval.</span></span> <span data-ttu-id="ff958-134">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ff958-134">Read-only.</span></span>
| <span data-ttu-id="ff958-135">delete</span><span class="sxs-lookup"><span data-stu-id="ff958-135">delete</span></span>           | <span data-ttu-id="ff958-136">[itemActionStat][]</span><span class="sxs-lookup"><span data-stu-id="ff958-136">[itemActionStat][]</span></span>      | <span data-ttu-id="ff958-137">Estadísticas sobre las acciones de **eliminación** en este intervalo.</span><span class="sxs-lookup"><span data-stu-id="ff958-137">Statistics about the **delete** actions in this interval.</span></span> <span data-ttu-id="ff958-138">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ff958-138">Read-only.</span></span>
| <span data-ttu-id="ff958-139">move</span><span class="sxs-lookup"><span data-stu-id="ff958-139">move</span></span>             | <span data-ttu-id="ff958-140">[itemActionStat][]</span><span class="sxs-lookup"><span data-stu-id="ff958-140">[itemActionStat][]</span></span>      | <span data-ttu-id="ff958-141">Estadísticas sobre las acciones de **mover** en este intervalo.</span><span class="sxs-lookup"><span data-stu-id="ff958-141">Statistics about the **move** actions in this interval.</span></span> <span data-ttu-id="ff958-142">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ff958-142">Read-only.</span></span>
| <span data-ttu-id="ff958-143">Access</span><span class="sxs-lookup"><span data-stu-id="ff958-143">access</span></span>           | <span data-ttu-id="ff958-144">[itemActionStat][]</span><span class="sxs-lookup"><span data-stu-id="ff958-144">[itemActionStat][]</span></span>      | <span data-ttu-id="ff958-145">Estadísticas sobre las acciones de **acceso** en este intervalo.</span><span class="sxs-lookup"><span data-stu-id="ff958-145">Statistics about the **access** actions in this interval.</span></span> <span data-ttu-id="ff958-146">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ff958-146">Read-only.</span></span>

[itemActionStat]: itemactionstat.md
[incompleteData]: incompletedata.md

## <a name="relationships"></a><span data-ttu-id="ff958-149">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ff958-149">Relationships</span></span>

| <span data-ttu-id="ff958-150">Nombre de la relación</span><span class="sxs-lookup"><span data-stu-id="ff958-150">Relationship name</span></span> | <span data-ttu-id="ff958-151">Tipo</span><span class="sxs-lookup"><span data-stu-id="ff958-151">Type</span></span>                        | <span data-ttu-id="ff958-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff958-152">Description</span></span>
|:------------------|:----------------------------|:---------------------------
| <span data-ttu-id="ff958-153">activities</span><span class="sxs-lookup"><span data-stu-id="ff958-153">activities</span></span>        | <span data-ttu-id="ff958-154">Colección [itemActivity][]</span><span class="sxs-lookup"><span data-stu-id="ff958-154">[itemActivity][] collection</span></span> | <span data-ttu-id="ff958-155">Expone la **itemActivities** representado en este recurso **itemActivityStat** .</span><span class="sxs-lookup"><span data-stu-id="ff958-155">Exposes the **itemActivities** represented in this **itemActivityStat** resource.</span></span>

[itemActivity]: itemactivity.md

## <a name="remarks"></a><span data-ttu-id="ff958-157">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff958-157">Remarks</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The ItemActivityStat object provides information about activities that took place on an item.",
  "keywords": "activities,activity,action,analytics",
  "section": "documentation",
  "tocPath": "Resources/ItemActivityStat"
} -->
