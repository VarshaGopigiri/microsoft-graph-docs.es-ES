---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: ItemActivityTimeSet
localization_priority: Normal
ms.openlocfilehash: 2ff3e1a2356c43457fe251928728632bd2228b10
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27809895"
---
# <a name="itemactivitytimeset-resource-type"></a><span data-ttu-id="4a50d-102">Tipo de recurso ItemActivityTimeSet</span><span class="sxs-lookup"><span data-stu-id="4a50d-102">ItemActivityTimeSet resource type</span></span>

> <span data-ttu-id="4a50d-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4a50d-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4a50d-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4a50d-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4a50d-105">El recurso **ItemActivityTimeSet** proporciona información sobre cuándo se produjo una [actividad][activity] en un elemento.</span><span class="sxs-lookup"><span data-stu-id="4a50d-105">The **ItemActivityTimeSet** resource provides information about when an [activity][activity] on an item took place.</span></span>

[activity]: itemactivity.md

## <a name="json-representation"></a><span data-ttu-id="4a50d-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4a50d-106">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "keyProperty": "id",
  "@type": "microsoft.graph.itemActivityTimeSet",
  "@type.aka": "oneDrive.times",
  "@property.aka": "observedDateTime=observedTime recordedDateTime=recordedTime"
}-->

```json
{
  "observedDateTime": "String (timestamp)",
  "recordedDateTime": "String (timestamp)"
}
```

## <a name="properties"></a><span data-ttu-id="4a50d-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4a50d-107">Properties</span></span>

| <span data-ttu-id="4a50d-108">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="4a50d-108">Property name</span></span>    | <span data-ttu-id="4a50d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="4a50d-109">Type</span></span>           | <span data-ttu-id="4a50d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a50d-110">Description</span></span>
|:-----------------|:---------------|:-----------------------------------------
| <span data-ttu-id="4a50d-111">observedDateTime</span><span class="sxs-lookup"><span data-stu-id="4a50d-111">observedDateTime</span></span> | <span data-ttu-id="4a50d-112">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4a50d-112">DateTimeOffset</span></span> | <span data-ttu-id="4a50d-113">Cuándo se observó que se produjo la actividad.</span><span class="sxs-lookup"><span data-stu-id="4a50d-113">When the activity was observed to take place.</span></span>
| <span data-ttu-id="4a50d-114">recordedDateTime</span><span class="sxs-lookup"><span data-stu-id="4a50d-114">recordedDateTime</span></span> | <span data-ttu-id="4a50d-115">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4a50d-115">DateTimeOffset</span></span> | <span data-ttu-id="4a50d-116">Cuándo se registró la observación en el servicio.</span><span class="sxs-lookup"><span data-stu-id="4a50d-116">When the observation was recorded on the service.</span></span>

<span data-ttu-id="4a50d-117">La diferencia entre las horas **observed** y **recorded** es especialmente importante para los escenarios de colaboración sin conexión.</span><span class="sxs-lookup"><span data-stu-id="4a50d-117">The difference between **observed** and **recorded** times is especially important for offline collaboration scenarios.</span></span>
<span data-ttu-id="4a50d-118">Si un usuario comenta en un archivo mientras está sin conexión, la hora en que hizo el comentario se establece como **observedDateTime**.</span><span class="sxs-lookup"><span data-stu-id="4a50d-118">If a user comments on a file while offline, the time that they make the comment is set as the **observedDateTime**.</span></span>
<span data-ttu-id="4a50d-119">En un momento posterior, cuando el usuario se vuelve a conectar a la nube y se cargan los cambios, esa hora posterior se establece como **recordedDateTime**.</span><span class="sxs-lookup"><span data-stu-id="4a50d-119">At a later time when the user re-connects to the cloud and the changes get uploaded, that later time is set as the **recordedDateTime**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a50d-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4a50d-120">Remarks</span></span>

<span data-ttu-id="4a50d-121">Actualmente, los registros de actividad de elementos solo están disponibles en SharePoint y OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="4a50d-121">Item activity records are currently only available on SharePoint and OneDrive for Business.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The ItemActionSet object provides information about an activity that took place on an item.",
  "keywords": "activities,activity,action",
  "section": "documentation",
  "tocPath": "Resources/ItemActionSet"
} -->
