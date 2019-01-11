---
title: Tipo de recurso educationTerm
description: Período. Representa una parte designada del año académico. Se usa en educationClass.
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: af11aa6b4a110417152c76dd606245a18ad51c28
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27851453"
---
# <a name="educationterm-resource-type"></a><span data-ttu-id="5c673-105">Tipo de recurso educationTerm</span><span class="sxs-lookup"><span data-stu-id="5c673-105">educationTerm resource type</span></span>

<span data-ttu-id="5c673-106">Período.</span><span class="sxs-lookup"><span data-stu-id="5c673-106">A term.</span></span> <span data-ttu-id="5c673-107">Representa una parte designada del año académico.</span><span class="sxs-lookup"><span data-stu-id="5c673-107">This represents a designated portion of the academic year.</span></span> <span data-ttu-id="5c673-108">Se usa en [educationClass](educationclass.md).</span><span class="sxs-lookup"><span data-stu-id="5c673-108">It is used within [educationClass](educationclass.md).</span></span>

## <a name="properties"></a><span data-ttu-id="5c673-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5c673-109">Properties</span></span>
| <span data-ttu-id="5c673-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5c673-110">Property</span></span>     | <span data-ttu-id="5c673-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="5c673-111">Type</span></span>   |<span data-ttu-id="5c673-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c673-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5c673-113">displayName</span><span class="sxs-lookup"><span data-stu-id="5c673-113">displayName</span></span>| <span data-ttu-id="5c673-114">String</span><span class="sxs-lookup"><span data-stu-id="5c673-114">String</span></span>| <span data-ttu-id="5c673-115">Nombre para mostrar del período.</span><span class="sxs-lookup"><span data-stu-id="5c673-115">Display name of the term.</span></span>| 
|<span data-ttu-id="5c673-116">externalId</span><span class="sxs-lookup"><span data-stu-id="5c673-116">externalId</span></span>|<span data-ttu-id="5c673-117">String</span><span class="sxs-lookup"><span data-stu-id="5c673-117">String</span></span>| <span data-ttu-id="5c673-118">Identificador del período en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="5c673-118">ID of term in the syncing system.</span></span>|
|<span data-ttu-id="5c673-119">startDate</span><span class="sxs-lookup"><span data-stu-id="5c673-119">startDate</span></span>|<span data-ttu-id="5c673-120">Date</span><span class="sxs-lookup"><span data-stu-id="5c673-120">Date</span></span>|<span data-ttu-id="5c673-121">Inicio del período.</span><span class="sxs-lookup"><span data-stu-id="5c673-121">Start of the term.</span></span>|
|<span data-ttu-id="5c673-122">endDate</span><span class="sxs-lookup"><span data-stu-id="5c673-122">endDate</span></span>|<span data-ttu-id="5c673-123">Date</span><span class="sxs-lookup"><span data-stu-id="5c673-123">Date</span></span>|<span data-ttu-id="5c673-124">Final del período.</span><span class="sxs-lookup"><span data-stu-id="5c673-124">End of the term.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="5c673-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5c673-125">JSON representation</span></span>

<span data-ttu-id="5c673-126">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="5c673-126">The following is a JSON representation of the resource.</span></span>

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
