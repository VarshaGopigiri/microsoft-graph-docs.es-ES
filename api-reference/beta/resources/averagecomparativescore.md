---
title: " tipo de recurso averageComparativeScore"
description: Este recurso contiene diversos calificaciones distintas en función de diferentes ámbitos (por ejemplo, promedio por industria vertical, promedio por tamaño de puestos de la empresa y así sucesivamente) y categoría de control (identidad, datos, dispositivos, aplicaciones, infraestructura).
ms.openlocfilehash: 08e4ec60788b21476d8f1491ab5548c7a4ca2e01
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084444"
---
#  <a name="averagecomparativescore-resource-type"></a><span data-ttu-id="2eb7a-103">tipo de recurso averageComparativeScore</span><span class="sxs-lookup"><span data-stu-id="2eb7a-103">averageComparativeScore resource type</span></span>

<span data-ttu-id="2eb7a-104">Este recurso contiene diversos calificaciones distintas en función de diferentes ámbitos (por ejemplo, promedio por industria vertical, promedio por tamaño de puestos de la empresa y así sucesivamente) y categoría de control (identidad, datos, dispositivos, aplicaciones, infraestructura).</span><span class="sxs-lookup"><span data-stu-id="2eb7a-104">This resource contains various different scores based by different scopes (for example, average by industry vertical, average by company seat size, and so on) and control category (Identity, Data, Device, Apps, Infrastructure).</span></span>

|<span data-ttu-id="2eb7a-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2eb7a-105">Property</span></span> |<span data-ttu-id="2eb7a-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="2eb7a-106">Type</span></span> |<span data-ttu-id="2eb7a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="2eb7a-107">Description</span></span> |
|:--|:--|:--|
|   <span data-ttu-id="2eb7a-108">base</span><span class="sxs-lookup"><span data-stu-id="2eb7a-108">basis</span></span>   |   <span data-ttu-id="2eb7a-109">String</span><span class="sxs-lookup"><span data-stu-id="2eb7a-109">String</span></span>  |   <span data-ttu-id="2eb7a-110">Tipo de ámbito (por AllTenants, TotalSeats, IndustryTypes).</span><span class="sxs-lookup"><span data-stu-id="2eb7a-110">Scope type (By AllTenants, TotalSeats, IndustryTypes).</span></span>  |
|   <span data-ttu-id="2eb7a-111">Promedio</span><span class="sxs-lookup"><span data-stu-id="2eb7a-111">averageScore</span></span>    |   <span data-ttu-id="2eb7a-112">Doble</span><span class="sxs-lookup"><span data-stu-id="2eb7a-112">Double</span></span>  | <span data-ttu-id="2eb7a-113">Promedio de la puntuación dentro de base especificado.</span><span class="sxs-lookup"><span data-stu-id="2eb7a-113">Average score within specified basis.</span></span> |
|   <span data-ttu-id="2eb7a-114">deviceScore</span><span class="sxs-lookup"><span data-stu-id="2eb7a-114">deviceScore</span></span> |   <span data-ttu-id="2eb7a-115">Doble</span><span class="sxs-lookup"><span data-stu-id="2eb7a-115">Double</span></span>  | <span data-ttu-id="2eb7a-116">Promedio de la puntuación dentro de base especificado.</span><span class="sxs-lookup"><span data-stu-id="2eb7a-116">Average score within specified basis.</span></span> |
|   <span data-ttu-id="2eb7a-117">dataScore</span><span class="sxs-lookup"><span data-stu-id="2eb7a-117">dataScore</span></span>   |   <span data-ttu-id="2eb7a-118">Doble</span><span class="sxs-lookup"><span data-stu-id="2eb7a-118">Double</span></span>  | <span data-ttu-id="2eb7a-119">Promedio de la puntuación dentro de base especificado.</span><span class="sxs-lookup"><span data-stu-id="2eb7a-119">Average score within specified basis.</span></span> |
|   <span data-ttu-id="2eb7a-120">identityScore</span><span class="sxs-lookup"><span data-stu-id="2eb7a-120">identityScore</span></span>   |   <span data-ttu-id="2eb7a-121">Doble</span><span class="sxs-lookup"><span data-stu-id="2eb7a-121">Double</span></span>  | <span data-ttu-id="2eb7a-122">Promedio de la puntuación dentro de base especificado.</span><span class="sxs-lookup"><span data-stu-id="2eb7a-122">Average score within specified basis.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="2eb7a-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2eb7a-123">JSON representation</span></span>

<span data-ttu-id="2eb7a-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="2eb7a-124">The following is a JSON representation of the resource.</span></span>

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
