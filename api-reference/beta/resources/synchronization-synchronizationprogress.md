---
title: tipo de recurso synchronizationProgress
description: Representa el progreso de un synchronizationJob hasta su finalización.
localization_priority: Normal
ms.openlocfilehash: 3c1168cdac6a073842cb5e08d165572591d2d8e0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27885389"
---
# <a name="synchronizationprogress-resource-type"></a><span data-ttu-id="7730d-103">tipo de recurso synchronizationProgress</span><span class="sxs-lookup"><span data-stu-id="7730d-103">synchronizationProgress resource type</span></span>

> <span data-ttu-id="7730d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7730d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7730d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7730d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7730d-106">Representa el progreso de un [synchronizationJob](synchronization-synchronizationjob.md) hasta su finalización.</span><span class="sxs-lookup"><span data-stu-id="7730d-106">Represents the progress of a [synchronizationJob](synchronization-synchronizationjob.md) toward completion.</span></span>

## <a name="properties"></a><span data-ttu-id="7730d-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7730d-107">Properties</span></span>

| <span data-ttu-id="7730d-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7730d-108">Property</span></span>                              | <span data-ttu-id="7730d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="7730d-109">Type</span></span>      | <span data-ttu-id="7730d-110">Description</span><span class="sxs-lookup"><span data-stu-id="7730d-110">Description</span></span>    |
|:--------------------------------------|:----------|:---------------|
|<span data-ttu-id="7730d-111">completedUnits</span><span class="sxs-lookup"><span data-stu-id="7730d-111">completedUnits</span></span>|<span data-ttu-id="7730d-112">Int32</span><span class="sxs-lookup"><span data-stu-id="7730d-112">Int32</span></span>|<span data-ttu-id="7730d-113">El numerador de una relación de progreso; el número de unidades de cambios ya procesados.</span><span class="sxs-lookup"><span data-stu-id="7730d-113">The numerator of a progress ratio; the number of units of changes already processed.</span></span>|
|<span data-ttu-id="7730d-114">progressObservationDateTime</span><span class="sxs-lookup"><span data-stu-id="7730d-114">progressObservationDateTime</span></span>|<span data-ttu-id="7730d-115">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7730d-115">DateTimeOffset</span></span>|<span data-ttu-id="7730d-116">La hora de una observación de progreso como un desplazamiento en minutos de la hora UTC.</span><span class="sxs-lookup"><span data-stu-id="7730d-116">The time of a progress observation as an offset in minutes from UTC.</span></span>|
|<span data-ttu-id="7730d-117">totalUnits</span><span class="sxs-lookup"><span data-stu-id="7730d-117">totalUnits</span></span>|<span data-ttu-id="7730d-118">Int32</span><span class="sxs-lookup"><span data-stu-id="7730d-118">Int32</span></span>|<span data-ttu-id="7730d-119">El denominador de una relación de progreso; un número de unidades de los cambios que va a procesar para llevar a cabo la sincronización.</span><span class="sxs-lookup"><span data-stu-id="7730d-119">The denominator of a progress ratio; a number of units of changes to be processed to accomplish synchronization.</span></span>|
|<span data-ttu-id="7730d-120">unidades</span><span class="sxs-lookup"><span data-stu-id="7730d-120">units</span></span>|<span data-ttu-id="7730d-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="7730d-121">String</span></span>|<span data-ttu-id="7730d-122">Una descripción opcional de las unidades.</span><span class="sxs-lookup"><span data-stu-id="7730d-122">An optional description of the units.</span></span>|

<!-- The troubleshootingUrl property is missing a description -->

## <a name="json-representation"></a><span data-ttu-id="7730d-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7730d-123">JSON representation</span></span>

<span data-ttu-id="7730d-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="7730d-124">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.synchronizationStatus"
}-->

```json
{
  "completedUnits": 1025,
  "progressObservationDateTime": "2017-10-10T17:00:00Z",
  "totalUnits": 3024,
  "units": "pages"
}

```

<!-- uuid: 15571993-7e2f-4842-84d5-01ceb67cdc05
20185-08-14 22:30:00 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationProcess resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
