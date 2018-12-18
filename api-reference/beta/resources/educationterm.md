---
title: Tipo de recurso educationTerm
description: Período. Representa una parte designada del año académico. Se usa en educationClass.
author: mmast-msft
ms.openlocfilehash: 31925f336dbb0ce0f83ffd6b36b38e7a0916cdb5
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27303454"
---
# <a name="educationterm-resource-type"></a><span data-ttu-id="7f6f5-105">Tipo de recurso educationTerm</span><span class="sxs-lookup"><span data-stu-id="7f6f5-105">educationTerm resource type</span></span>

> <span data-ttu-id="7f6f5-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7f6f5-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7f6f5-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7f6f5-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7f6f5-108">Período.</span><span class="sxs-lookup"><span data-stu-id="7f6f5-108">A term.</span></span> <span data-ttu-id="7f6f5-109">Representa una parte designada del año académico.</span><span class="sxs-lookup"><span data-stu-id="7f6f5-109">This represents a designated portion of the academic year.</span></span> <span data-ttu-id="7f6f5-110">Se usa en [educationClass](educationclass.md).</span><span class="sxs-lookup"><span data-stu-id="7f6f5-110">It is used within [educationClass](educationclass.md).</span></span>

## <a name="properties"></a><span data-ttu-id="7f6f5-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7f6f5-111">Properties</span></span>
| <span data-ttu-id="7f6f5-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7f6f5-112">Property</span></span>     | <span data-ttu-id="7f6f5-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="7f6f5-113">Type</span></span>   |<span data-ttu-id="7f6f5-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="7f6f5-114">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7f6f5-115">displayName</span><span class="sxs-lookup"><span data-stu-id="7f6f5-115">displayName</span></span>| <span data-ttu-id="7f6f5-116">String</span><span class="sxs-lookup"><span data-stu-id="7f6f5-116">String</span></span>| <span data-ttu-id="7f6f5-117">Nombre para mostrar del período.</span><span class="sxs-lookup"><span data-stu-id="7f6f5-117">Display name of the term.</span></span>| 
|<span data-ttu-id="7f6f5-118">externalId</span><span class="sxs-lookup"><span data-stu-id="7f6f5-118">externalId</span></span>|<span data-ttu-id="7f6f5-119">String</span><span class="sxs-lookup"><span data-stu-id="7f6f5-119">String</span></span>| <span data-ttu-id="7f6f5-120">Identificador del período en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="7f6f5-120">ID of term in the syncing system.</span></span>|
|<span data-ttu-id="7f6f5-121">startDate</span><span class="sxs-lookup"><span data-stu-id="7f6f5-121">startDate</span></span>|<span data-ttu-id="7f6f5-122">Date</span><span class="sxs-lookup"><span data-stu-id="7f6f5-122">Date</span></span>|<span data-ttu-id="7f6f5-123">Inicio del período.</span><span class="sxs-lookup"><span data-stu-id="7f6f5-123">Start of the term.</span></span>|
|<span data-ttu-id="7f6f5-124">endDate</span><span class="sxs-lookup"><span data-stu-id="7f6f5-124">endDate</span></span>|<span data-ttu-id="7f6f5-125">Date</span><span class="sxs-lookup"><span data-stu-id="7f6f5-125">Date</span></span>|<span data-ttu-id="7f6f5-126">Final del período.</span><span class="sxs-lookup"><span data-stu-id="7f6f5-126">End of the term.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="7f6f5-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7f6f5-127">JSON representation</span></span>

<span data-ttu-id="7f6f5-128">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="7f6f5-128">The following is a JSON representation of the resource.</span></span>

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