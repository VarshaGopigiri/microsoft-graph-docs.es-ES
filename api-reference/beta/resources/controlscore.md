---
title: " tipo de recurso controlScore"
description: Este recurso contiene una puntuación de inquilinos y una descripción para un control individual.
ms.openlocfilehash: 67059c1a7382416411709f02c609c90b20a673b4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084476"
---
#  <a name="controlscore-resource-type"></a><span data-ttu-id="12dd4-103">tipo de recurso controlScore</span><span class="sxs-lookup"><span data-stu-id="12dd4-103">controlScore resource type</span></span>

<span data-ttu-id="12dd4-104">Este recurso contiene una puntuación de inquilinos y una descripción para un control individual.</span><span class="sxs-lookup"><span data-stu-id="12dd4-104">This resource contains a tenant score and description for an individual control.</span></span>

|<span data-ttu-id="12dd4-105">Nombre</span><span class="sxs-lookup"><span data-stu-id="12dd4-105">Name</span></span> |<span data-ttu-id="12dd4-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="12dd4-106">Type</span></span> |<span data-ttu-id="12dd4-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="12dd4-107">Description</span></span> |
|:--|:--|:--|
|   <span data-ttu-id="12dd4-108">controlName</span><span class="sxs-lookup"><span data-stu-id="12dd4-108">controlName</span></span> |   <span data-ttu-id="12dd4-109">String</span><span class="sxs-lookup"><span data-stu-id="12dd4-109">String</span></span>  |   <span data-ttu-id="12dd4-110">Nombre único de control</span><span class="sxs-lookup"><span data-stu-id="12dd4-110">Control unique name</span></span> |
|   <span data-ttu-id="12dd4-111">score</span><span class="sxs-lookup"><span data-stu-id="12dd4-111">score</span></span>   |   <span data-ttu-id="12dd4-112">Doble</span><span class="sxs-lookup"><span data-stu-id="12dd4-112">Double</span></span>  |  <span data-ttu-id="12dd4-113">Inquilino de lograr la puntuación para el control (día a día varía, dependiendo de las operaciones del inquilino en el control).</span><span class="sxs-lookup"><span data-stu-id="12dd4-113">Tenant achieved score for the control (it varies day by day depending on tenant operations on the control).</span></span> |
|   <span data-ttu-id="12dd4-114">controlCategory</span><span class="sxs-lookup"><span data-stu-id="12dd4-114">controlCategory</span></span> |   <span data-ttu-id="12dd4-115">String</span><span class="sxs-lookup"><span data-stu-id="12dd4-115">String</span></span>  |  <span data-ttu-id="12dd4-116">Categoría de acción de control (identidad, datos, dispositivos, aplicaciones, infraestructura).</span><span class="sxs-lookup"><span data-stu-id="12dd4-116">Control action category (Identity, Data, Device, Apps, Infrastructure).</span></span> |
|   <span data-ttu-id="12dd4-117">descripción</span><span class="sxs-lookup"><span data-stu-id="12dd4-117">description</span></span> |   <span data-ttu-id="12dd4-118">String</span><span class="sxs-lookup"><span data-stu-id="12dd4-118">String</span></span>  |  <span data-ttu-id="12dd4-119">Descripción del control.</span><span class="sxs-lookup"><span data-stu-id="12dd4-119">Description of the control.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="12dd4-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="12dd4-120">JSON representation</span></span>

<span data-ttu-id="12dd4-121">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="12dd4-121">The following is a JSON representation of the resource.</span></span>

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
