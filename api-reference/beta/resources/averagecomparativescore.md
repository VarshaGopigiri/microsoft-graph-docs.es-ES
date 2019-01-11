---
title: " tipo de recurso averageComparativeScore"
description: Este recurso contiene diversos calificaciones distintas en función de diferentes ámbitos (por ejemplo, promedio por industria vertical, promedio por tamaño de puestos de la empresa y así sucesivamente) y categoría de control (identidad, datos, dispositivos, aplicaciones, infraestructura).
localization_priority: Normal
ms.openlocfilehash: c32c1349edd70e80c1bf0fb12a36bd07e06ed39f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27834597"
---
#  <a name="averagecomparativescore-resource-type"></a><span data-ttu-id="add82-103">tipo de recurso averageComparativeScore</span><span class="sxs-lookup"><span data-stu-id="add82-103">averageComparativeScore resource type</span></span>

<span data-ttu-id="add82-104">Este recurso contiene diversos calificaciones distintas en función de diferentes ámbitos (por ejemplo, promedio por industria vertical, promedio por tamaño de puestos de la empresa y así sucesivamente) y categoría de control (identidad, datos, dispositivos, aplicaciones, infraestructura).</span><span class="sxs-lookup"><span data-stu-id="add82-104">This resource contains various different scores based by different scopes (for example, average by industry vertical, average by company seat size, and so on) and control category (Identity, Data, Device, Apps, Infrastructure).</span></span>

|<span data-ttu-id="add82-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="add82-105">Property</span></span> |<span data-ttu-id="add82-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="add82-106">Type</span></span> |<span data-ttu-id="add82-107">Description</span><span class="sxs-lookup"><span data-stu-id="add82-107">Description</span></span> |
|:--|:--|:--|
|   <span data-ttu-id="add82-108">base</span><span class="sxs-lookup"><span data-stu-id="add82-108">basis</span></span>   |   <span data-ttu-id="add82-109">Cadena</span><span class="sxs-lookup"><span data-stu-id="add82-109">String</span></span>  |   <span data-ttu-id="add82-110">Tipo de ámbito (por AllTenants, TotalSeats, IndustryTypes).</span><span class="sxs-lookup"><span data-stu-id="add82-110">Scope type (By AllTenants, TotalSeats, IndustryTypes).</span></span>  |
|   <span data-ttu-id="add82-111">Promedio</span><span class="sxs-lookup"><span data-stu-id="add82-111">averageScore</span></span>    |   <span data-ttu-id="add82-112">Doble</span><span class="sxs-lookup"><span data-stu-id="add82-112">Double</span></span>  | <span data-ttu-id="add82-113">Promedio de la puntuación dentro de base especificado.</span><span class="sxs-lookup"><span data-stu-id="add82-113">Average score within specified basis.</span></span> |
|   <span data-ttu-id="add82-114">deviceScore</span><span class="sxs-lookup"><span data-stu-id="add82-114">deviceScore</span></span> |   <span data-ttu-id="add82-115">Doble</span><span class="sxs-lookup"><span data-stu-id="add82-115">Double</span></span>  | <span data-ttu-id="add82-116">Promedio de la puntuación dentro de base especificado.</span><span class="sxs-lookup"><span data-stu-id="add82-116">Average score within specified basis.</span></span> |
|   <span data-ttu-id="add82-117">dataScore</span><span class="sxs-lookup"><span data-stu-id="add82-117">dataScore</span></span>   |   <span data-ttu-id="add82-118">Doble</span><span class="sxs-lookup"><span data-stu-id="add82-118">Double</span></span>  | <span data-ttu-id="add82-119">Promedio de la puntuación dentro de base especificado.</span><span class="sxs-lookup"><span data-stu-id="add82-119">Average score within specified basis.</span></span> |
|   <span data-ttu-id="add82-120">identityScore</span><span class="sxs-lookup"><span data-stu-id="add82-120">identityScore</span></span>   |   <span data-ttu-id="add82-121">Doble</span><span class="sxs-lookup"><span data-stu-id="add82-121">Double</span></span>  | <span data-ttu-id="add82-122">Promedio de la puntuación dentro de base especificado.</span><span class="sxs-lookup"><span data-stu-id="add82-122">Average score within specified basis.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="add82-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="add82-123">JSON representation</span></span>

<span data-ttu-id="add82-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="add82-124">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.averageComparativeScore"
}-->

```json
{
  "basis": "String",
  "averageScore": "Double",
  "deviceScore": "Double",
  "dataScore": "Double",
  "identityScore": "Double"
}

```


<!-- {
  "type": "#page.annotation",
  "description": "averageComparativeScore resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
