---
title: " tipo de recurso controlScore"
description: Este recurso contiene una puntuación de inquilinos y una descripción para un control individual.
localization_priority: Normal
ms.openlocfilehash: d8c2d73205f00a9dd5f2f28fcee3c33778bb3276
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27891472"
---
#  <a name="controlscore-resource-type"></a><span data-ttu-id="48554-103">tipo de recurso controlScore</span><span class="sxs-lookup"><span data-stu-id="48554-103">controlScore resource type</span></span>

<span data-ttu-id="48554-104">Este recurso contiene una puntuación de inquilinos y una descripción para un control individual.</span><span class="sxs-lookup"><span data-stu-id="48554-104">This resource contains a tenant score and description for an individual control.</span></span>

|<span data-ttu-id="48554-105">Nombre</span><span class="sxs-lookup"><span data-stu-id="48554-105">Name</span></span> |<span data-ttu-id="48554-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="48554-106">Type</span></span> |<span data-ttu-id="48554-107">Description</span><span class="sxs-lookup"><span data-stu-id="48554-107">Description</span></span> |
|:--|:--|:--|
|   <span data-ttu-id="48554-108">controlName</span><span class="sxs-lookup"><span data-stu-id="48554-108">controlName</span></span> |   <span data-ttu-id="48554-109">Cadena</span><span class="sxs-lookup"><span data-stu-id="48554-109">String</span></span>  |   <span data-ttu-id="48554-110">Nombre único de control</span><span class="sxs-lookup"><span data-stu-id="48554-110">Control unique name</span></span> |
|   <span data-ttu-id="48554-111">score</span><span class="sxs-lookup"><span data-stu-id="48554-111">score</span></span>   |   <span data-ttu-id="48554-112">Doble</span><span class="sxs-lookup"><span data-stu-id="48554-112">Double</span></span>  |  <span data-ttu-id="48554-113">Inquilino de lograr la puntuación para el control (día a día varía, dependiendo de las operaciones del inquilino en el control).</span><span class="sxs-lookup"><span data-stu-id="48554-113">Tenant achieved score for the control (it varies day by day depending on tenant operations on the control).</span></span> |
|   <span data-ttu-id="48554-114">controlCategory</span><span class="sxs-lookup"><span data-stu-id="48554-114">controlCategory</span></span> |   <span data-ttu-id="48554-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="48554-115">String</span></span>  |  <span data-ttu-id="48554-116">Categoría de acción de control (identidad, datos, dispositivos, aplicaciones, infraestructura).</span><span class="sxs-lookup"><span data-stu-id="48554-116">Control action category (Identity, Data, Device, Apps, Infrastructure).</span></span> |
|   <span data-ttu-id="48554-117">descripción</span><span class="sxs-lookup"><span data-stu-id="48554-117">description</span></span> |   <span data-ttu-id="48554-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="48554-118">String</span></span>  |  <span data-ttu-id="48554-119">Descripción del control.</span><span class="sxs-lookup"><span data-stu-id="48554-119">Description of the control.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="48554-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="48554-120">JSON representation</span></span>

<span data-ttu-id="48554-121">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="48554-121">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.controlScore"
}-->

```json
{
  "controlName": "String",
  "score": "String",
  "controlCategory": "String",
  "description": "String"
}

```


<!-- {
  "type": "#page.annotation",
  "description": "controlScore resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
