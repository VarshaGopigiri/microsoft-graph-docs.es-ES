---
title: Tipo de recurso educationTerm
description: Período. Representa una parte designada del año académico. Se usa en educationClass.
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: bc068df7a31c1b3903e8735ba1255cc3a6f0ae73
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27962761"
---
# <a name="educationterm-resource-type"></a><span data-ttu-id="13400-105">Tipo de recurso educationTerm</span><span class="sxs-lookup"><span data-stu-id="13400-105">educationTerm resource type</span></span>

> <span data-ttu-id="13400-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="13400-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="13400-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="13400-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="13400-108">Período.</span><span class="sxs-lookup"><span data-stu-id="13400-108">A term.</span></span> <span data-ttu-id="13400-109">Representa una parte designada del año académico.</span><span class="sxs-lookup"><span data-stu-id="13400-109">This represents a designated portion of the academic year.</span></span> <span data-ttu-id="13400-110">Se usa en [educationClass](educationclass.md).</span><span class="sxs-lookup"><span data-stu-id="13400-110">It is used within [educationClass](educationclass.md).</span></span>

## <a name="properties"></a><span data-ttu-id="13400-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="13400-111">Properties</span></span>
| <span data-ttu-id="13400-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="13400-112">Property</span></span>     | <span data-ttu-id="13400-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="13400-113">Type</span></span>   |<span data-ttu-id="13400-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="13400-114">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="13400-115">displayName</span><span class="sxs-lookup"><span data-stu-id="13400-115">displayName</span></span>| <span data-ttu-id="13400-116">String</span><span class="sxs-lookup"><span data-stu-id="13400-116">String</span></span>| <span data-ttu-id="13400-117">Nombre para mostrar del período.</span><span class="sxs-lookup"><span data-stu-id="13400-117">Display name of the term.</span></span>| 
|<span data-ttu-id="13400-118">externalId</span><span class="sxs-lookup"><span data-stu-id="13400-118">externalId</span></span>|<span data-ttu-id="13400-119">String</span><span class="sxs-lookup"><span data-stu-id="13400-119">String</span></span>| <span data-ttu-id="13400-120">Identificador del período en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="13400-120">ID of term in the syncing system.</span></span>|
|<span data-ttu-id="13400-121">startDate</span><span class="sxs-lookup"><span data-stu-id="13400-121">startDate</span></span>|<span data-ttu-id="13400-122">Date</span><span class="sxs-lookup"><span data-stu-id="13400-122">Date</span></span>|<span data-ttu-id="13400-123">Inicio del período.</span><span class="sxs-lookup"><span data-stu-id="13400-123">Start of the term.</span></span>|
|<span data-ttu-id="13400-124">endDate</span><span class="sxs-lookup"><span data-stu-id="13400-124">endDate</span></span>|<span data-ttu-id="13400-125">Date</span><span class="sxs-lookup"><span data-stu-id="13400-125">Date</span></span>|<span data-ttu-id="13400-126">Final del período.</span><span class="sxs-lookup"><span data-stu-id="13400-126">End of the term.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="13400-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="13400-127">JSON representation</span></span>

<span data-ttu-id="13400-128">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="13400-128">The following is a JSON representation of the resource.</span></span>

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
