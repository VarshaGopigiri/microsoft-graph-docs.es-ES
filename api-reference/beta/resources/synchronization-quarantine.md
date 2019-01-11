---
title: tipo de recurso synchronizationQuarantine
description: Proporciona información sobre el estado de la cuarentena de un synchronizationJob.
localization_priority: Normal
ms.openlocfilehash: fba0077d48e69ed4c2c190d0b50a6fcfc1749626
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27849731"
---
# <a name="synchronizationquarantine-resource-type"></a><span data-ttu-id="54b79-103">tipo de recurso synchronizationQuarantine</span><span class="sxs-lookup"><span data-stu-id="54b79-103">synchronizationQuarantine resource type</span></span>

> <span data-ttu-id="54b79-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="54b79-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="54b79-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="54b79-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="54b79-106">Proporciona información sobre el estado de la cuarentena de un [synchronizationJob](synchronization-synchronizationjob.md).</span><span class="sxs-lookup"><span data-stu-id="54b79-106">Provides information about the quarantine state of a [synchronizationJob](synchronization-synchronizationjob.md).</span></span>

## <a name="properties"></a><span data-ttu-id="54b79-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="54b79-107">Properties</span></span>
| <span data-ttu-id="54b79-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="54b79-108">Property</span></span>     | <span data-ttu-id="54b79-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="54b79-109">Type</span></span>   |<span data-ttu-id="54b79-110">Description</span><span class="sxs-lookup"><span data-stu-id="54b79-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="54b79-111">currentBegan</span><span class="sxs-lookup"><span data-stu-id="54b79-111">currentBegan</span></span>|<span data-ttu-id="54b79-112">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="54b79-112">DateTimeOffset</span></span>|<span data-ttu-id="54b79-113">Fecha y hora cuando la cuarentena por última vez evalúan e imponen.</span><span class="sxs-lookup"><span data-stu-id="54b79-113">Date and time when the quarantine was last evaluated and imposed.</span></span> <span data-ttu-id="54b79-114">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="54b79-114">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="54b79-115">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="54b79-115">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="54b79-116">nextAttempt</span><span class="sxs-lookup"><span data-stu-id="54b79-116">nextAttempt</span></span>|<span data-ttu-id="54b79-117">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="54b79-117">DateTimeOffset</span></span>|<span data-ttu-id="54b79-118">Fecha y hora en la que se realizó el siguiente intento para volver a evaluar la cuarentena.</span><span class="sxs-lookup"><span data-stu-id="54b79-118">Date and time when the next attempt to re-evaluate the quarantine will be made.</span></span> <span data-ttu-id="54b79-119">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="54b79-119">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="54b79-120">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="54b79-120">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="54b79-121">motivo</span><span class="sxs-lookup"><span data-stu-id="54b79-121">reason</span></span>|<span data-ttu-id="54b79-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="54b79-122">String</span></span>|<span data-ttu-id="54b79-123">Un código que indica la razón por la que se impone la cuarentena.</span><span class="sxs-lookup"><span data-stu-id="54b79-123">A code that signifies why the quarantine was imposed.</span></span> <span data-ttu-id="54b79-124">Los valores posibles son: `EncounteredBaseEscrowThreshold`, `EncounteredTotalEscrowThreshold`, `EncounteredEscrowProportionThreshold`, `EncounteredQuarantineException` y `Unknown`.</span><span class="sxs-lookup"><span data-stu-id="54b79-124">Possible values are: `EncounteredBaseEscrowThreshold`, `EncounteredTotalEscrowThreshold`, `EncounteredEscrowProportionThreshold`, `EncounteredQuarantineException`, `Unknown`.</span></span>|
|<span data-ttu-id="54b79-125">seriesBegan</span><span class="sxs-lookup"><span data-stu-id="54b79-125">seriesBegan</span></span>|<span data-ttu-id="54b79-126">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="54b79-126">DateTimeOffset</span></span>|<span data-ttu-id="54b79-127">Fecha y hora cuando la cuarentena en primer lugar se impone en esta serie (una serie se inicia cuando una cuarentena se impone en primer lugar y se restablece tan pronto como se eleva la cuarentena).</span><span class="sxs-lookup"><span data-stu-id="54b79-127">Date and time when the quarantine was first imposed in this series (a series starts when a quarantine is first imposed, and is reset as soon as the quarantine is lifted).</span></span> <span data-ttu-id="54b79-128">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="54b79-128">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="54b79-129">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="54b79-129">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="54b79-130">seriesCount</span><span class="sxs-lookup"><span data-stu-id="54b79-130">seriesCount</span></span>|<span data-ttu-id="54b79-131">Int64</span><span class="sxs-lookup"><span data-stu-id="54b79-131">Int64</span></span>|<span data-ttu-id="54b79-132">Número de veces en esta serie de la cuarentena se vuelve a evaluar y en vigor izquierda (una serie se inicia cuando se impone en primer lugar la cuarentena y se restablece tan pronto como se eleva cuarentena).</span><span class="sxs-lookup"><span data-stu-id="54b79-132">Number of times in this series the quarantine was re-evaluated and left in effect (a series starts when quarantine is first imposed, and is reset as soon as quarantine is lifted).</span></span>|

## <a name="json-representation"></a><span data-ttu-id="54b79-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="54b79-133">JSON representation</span></span>

<span data-ttu-id="54b79-134">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="54b79-134">The following is a JSON representation of the resource.</span></span>

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
