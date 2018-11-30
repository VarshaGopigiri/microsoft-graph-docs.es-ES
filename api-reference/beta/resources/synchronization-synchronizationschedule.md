---
title: tipo de recurso synchronizationSchedule
description: Define la programación que se usa para ejecutar un synchronizationJob.
ms.openlocfilehash: c0435b3957f138751f34a1e0e522683b352294da
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086902"
---
# <a name="synchronizationschedule-resource-type"></a><span data-ttu-id="73599-103">tipo de recurso synchronizationSchedule</span><span class="sxs-lookup"><span data-stu-id="73599-103">synchronizationSchedule resource type</span></span>

> <span data-ttu-id="73599-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="73599-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="73599-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="73599-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="73599-106">Define la programación que se usa para ejecutar un [synchronizationJob](synchronization-synchronizationjob.md).</span><span class="sxs-lookup"><span data-stu-id="73599-106">Defines the schedule used to run a [synchronizationJob](synchronization-synchronizationjob.md).</span></span>

## <a name="properties"></a><span data-ttu-id="73599-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="73599-107">Properties</span></span>
| <span data-ttu-id="73599-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="73599-108">Property</span></span>     | <span data-ttu-id="73599-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="73599-109">Type</span></span>   |<span data-ttu-id="73599-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="73599-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="73599-111">expiración</span><span class="sxs-lookup"><span data-stu-id="73599-111">expiration</span></span>|<span data-ttu-id="73599-112">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="73599-112">DateTimeOffset</span></span>|<span data-ttu-id="73599-113">Fecha y hora de caducidad de este trabajo.</span><span class="sxs-lookup"><span data-stu-id="73599-113">Date and time when this job will expire.</span></span> <span data-ttu-id="73599-114">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="73599-114">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="73599-115">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="73599-115">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="73599-116">interval</span><span class="sxs-lookup"><span data-stu-id="73599-116">interval</span></span>|<span data-ttu-id="73599-117">Duración</span><span class="sxs-lookup"><span data-stu-id="73599-117">Duration</span></span>|<span data-ttu-id="73599-118">El intervalo entre iteraciones de sincronización.</span><span class="sxs-lookup"><span data-stu-id="73599-118">The interval between synchronization iterations.</span></span>|
|<span data-ttu-id="73599-119">estado</span><span class="sxs-lookup"><span data-stu-id="73599-119">state</span></span>|<span data-ttu-id="73599-120">String</span><span class="sxs-lookup"><span data-stu-id="73599-120">String</span></span>| <span data-ttu-id="73599-121">Los valores posibles son: `Active` y `Disabled`.</span><span class="sxs-lookup"><span data-stu-id="73599-121">Possible values are: `Active`, `Disabled`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="73599-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="73599-122">JSON representation</span></span>

<span data-ttu-id="73599-123">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="73599-123">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.synchronizationSchedule"
}-->

```json
{
  "expiration": "String (timestamp)",
  "interval": "String (duration)",
  "state": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationSchedule resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->