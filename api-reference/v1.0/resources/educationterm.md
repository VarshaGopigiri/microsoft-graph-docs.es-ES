---
title: Tipo de recurso educationTerm
description: Período. Representa una parte designada del año académico. Se usa en educationClass.
author: mmast-msft
ms.openlocfilehash: 319eedbaebde4f1e76c2f1b3e124c0dad2642538
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27353091"
---
# <a name="educationterm-resource-type"></a><span data-ttu-id="d9a2c-105">Tipo de recurso educationTerm</span><span class="sxs-lookup"><span data-stu-id="d9a2c-105">educationTerm resource type</span></span>

<span data-ttu-id="d9a2c-106">Período.</span><span class="sxs-lookup"><span data-stu-id="d9a2c-106">A term.</span></span> <span data-ttu-id="d9a2c-107">Representa una parte designada del año académico.</span><span class="sxs-lookup"><span data-stu-id="d9a2c-107">This represents a designated portion of the academic year.</span></span> <span data-ttu-id="d9a2c-108">Se usa en [educationClass](educationclass.md).</span><span class="sxs-lookup"><span data-stu-id="d9a2c-108">It is used within [educationClass](educationclass.md).</span></span>

## <a name="properties"></a><span data-ttu-id="d9a2c-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d9a2c-109">Properties</span></span>
| <span data-ttu-id="d9a2c-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d9a2c-110">Property</span></span>     | <span data-ttu-id="d9a2c-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="d9a2c-111">Type</span></span>   |<span data-ttu-id="d9a2c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9a2c-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d9a2c-113">displayName</span><span class="sxs-lookup"><span data-stu-id="d9a2c-113">displayName</span></span>| <span data-ttu-id="d9a2c-114">String</span><span class="sxs-lookup"><span data-stu-id="d9a2c-114">String</span></span>| <span data-ttu-id="d9a2c-115">Nombre para mostrar del período.</span><span class="sxs-lookup"><span data-stu-id="d9a2c-115">Display name of the term.</span></span>| 
|<span data-ttu-id="d9a2c-116">externalId</span><span class="sxs-lookup"><span data-stu-id="d9a2c-116">externalId</span></span>|<span data-ttu-id="d9a2c-117">String</span><span class="sxs-lookup"><span data-stu-id="d9a2c-117">String</span></span>| <span data-ttu-id="d9a2c-118">Identificador del período en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="d9a2c-118">ID of term in the syncing system.</span></span>|
|<span data-ttu-id="d9a2c-119">startDate</span><span class="sxs-lookup"><span data-stu-id="d9a2c-119">startDate</span></span>|<span data-ttu-id="d9a2c-120">Date</span><span class="sxs-lookup"><span data-stu-id="d9a2c-120">Date</span></span>|<span data-ttu-id="d9a2c-121">Inicio del período.</span><span class="sxs-lookup"><span data-stu-id="d9a2c-121">Start of the term.</span></span>|
|<span data-ttu-id="d9a2c-122">endDate</span><span class="sxs-lookup"><span data-stu-id="d9a2c-122">endDate</span></span>|<span data-ttu-id="d9a2c-123">Date</span><span class="sxs-lookup"><span data-stu-id="d9a2c-123">Date</span></span>|<span data-ttu-id="d9a2c-124">Final del período.</span><span class="sxs-lookup"><span data-stu-id="d9a2c-124">End of the term.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d9a2c-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d9a2c-125">JSON representation</span></span>

<span data-ttu-id="d9a2c-126">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d9a2c-126">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationTerm"
}-->

```json
{
  "displayName": "String",
  "externalId": "String",
  "startDate": "Date",
  "endDate": "Date"
}
```

<!-- uuid: 4e9d671f-3068-4e09-aba2-b39e81a0e452
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationTerm resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->