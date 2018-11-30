---
title: tipo de recurso synchronizationQuarantine
description: Proporciona información sobre el estado de la cuarentena de un synchronizationJob.
ms.openlocfilehash: b29da9644968ffe17abb02010f8aa5c304ca7905
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083942"
---
# <a name="synchronizationquarantine-resource-type"></a><span data-ttu-id="5350b-103">tipo de recurso synchronizationQuarantine</span><span class="sxs-lookup"><span data-stu-id="5350b-103">synchronizationQuarantine resource type</span></span>

> <span data-ttu-id="5350b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5350b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5350b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5350b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5350b-106">Proporciona información sobre el estado de la cuarentena de un [synchronizationJob](synchronization-synchronizationjob.md).</span><span class="sxs-lookup"><span data-stu-id="5350b-106">Provides information about the quarantine state of a [synchronizationJob](synchronization-synchronizationjob.md).</span></span>

## <a name="properties"></a><span data-ttu-id="5350b-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5350b-107">Properties</span></span>
| <span data-ttu-id="5350b-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5350b-108">Property</span></span>     | <span data-ttu-id="5350b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="5350b-109">Type</span></span>   |<span data-ttu-id="5350b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5350b-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5350b-111">currentBegan</span><span class="sxs-lookup"><span data-stu-id="5350b-111">currentBegan</span></span>|<span data-ttu-id="5350b-112">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5350b-112">DateTimeOffset</span></span>|<span data-ttu-id="5350b-113">Fecha y hora cuando la cuarentena por última vez evalúan e imponen.</span><span class="sxs-lookup"><span data-stu-id="5350b-113">Date and time when the quarantine was last evaluated and imposed.</span></span> <span data-ttu-id="5350b-114">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="5350b-114">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="5350b-115">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="5350b-115">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="5350b-116">nextAttempt</span><span class="sxs-lookup"><span data-stu-id="5350b-116">nextAttempt</span></span>|<span data-ttu-id="5350b-117">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5350b-117">DateTimeOffset</span></span>|<span data-ttu-id="5350b-118">Fecha y hora en la que se realizó el siguiente intento para volver a evaluar la cuarentena.</span><span class="sxs-lookup"><span data-stu-id="5350b-118">Date and time when the next attempt to re-evaluate the quarantine will be made.</span></span> <span data-ttu-id="5350b-119">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="5350b-119">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="5350b-120">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="5350b-120">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="5350b-121">motivo</span><span class="sxs-lookup"><span data-stu-id="5350b-121">reason</span></span>|<span data-ttu-id="5350b-122">String</span><span class="sxs-lookup"><span data-stu-id="5350b-122">String</span></span>|<span data-ttu-id="5350b-123">Un código que indica la razón por la que se impone la cuarentena.</span><span class="sxs-lookup"><span data-stu-id="5350b-123">A code that signifies why the quarantine was imposed.</span></span> <span data-ttu-id="5350b-124">Los valores posibles son: `EncounteredBaseEscrowThreshold`, `EncounteredTotalEscrowThreshold`, `EncounteredEscrowProportionThreshold`, `EncounteredQuarantineException` y `Unknown`.</span><span class="sxs-lookup"><span data-stu-id="5350b-124">Possible values are: `EncounteredBaseEscrowThreshold`, `EncounteredTotalEscrowThreshold`, `EncounteredEscrowProportionThreshold`, `EncounteredQuarantineException`, `Unknown`.</span></span>|
|<span data-ttu-id="5350b-125">seriesBegan</span><span class="sxs-lookup"><span data-stu-id="5350b-125">seriesBegan</span></span>|<span data-ttu-id="5350b-126">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5350b-126">DateTimeOffset</span></span>|<span data-ttu-id="5350b-127">Fecha y hora cuando la cuarentena en primer lugar se impone en esta serie (una serie se inicia cuando una cuarentena se impone en primer lugar y se restablece tan pronto como se eleva la cuarentena).</span><span class="sxs-lookup"><span data-stu-id="5350b-127">Date and time when the quarantine was first imposed in this series (a series starts when a quarantine is first imposed, and is reset as soon as the quarantine is lifted).</span></span> <span data-ttu-id="5350b-128">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="5350b-128">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="5350b-129">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="5350b-129">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="5350b-130">seriesCount</span><span class="sxs-lookup"><span data-stu-id="5350b-130">seriesCount</span></span>|<span data-ttu-id="5350b-131">Int64</span><span class="sxs-lookup"><span data-stu-id="5350b-131">Int64</span></span>|<span data-ttu-id="5350b-132">Número de veces en esta serie de la cuarentena se vuelve a evaluar y en vigor izquierda (una serie se inicia cuando se impone en primer lugar la cuarentena y se restablece tan pronto como se eleva cuarentena).</span><span class="sxs-lookup"><span data-stu-id="5350b-132">Number of times in this series the quarantine was re-evaluated and left in effect (a series starts when quarantine is first imposed, and is reset as soon as quarantine is lifted).</span></span>|

## <a name="json-representation"></a><span data-ttu-id="5350b-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5350b-133">JSON representation</span></span>

<span data-ttu-id="5350b-134">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="5350b-134">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.synchronizationQuarantine"
}-->

```json
{
  "currentBegan": "String (timestamp)",
  "nextAttempt": "String (timestamp)",
  "reason": "String",
  "seriesBegan": "String (timestamp)",
  "seriesCount": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationQuarantine resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->