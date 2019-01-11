---
title: Tipo de recurso standardTimeZoneOffset
description: Especifica cuándo una zona horaria cambia del horario de verano a la hora estándar.
localization_priority: Normal
ms.openlocfilehash: 5e224865f201041b72fb943bc3a76e8a67f7975a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27875848"
---
# <a name="standardtimezoneoffset-resource-type"></a><span data-ttu-id="0ccbe-103">Tipo de recurso standardTimeZoneOffset</span><span class="sxs-lookup"><span data-stu-id="0ccbe-103">standardTimeZoneOffset resource type</span></span>

<span data-ttu-id="0ccbe-104">Especifica cuándo una zona horaria cambia del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="0ccbe-104">Specifies when a time zone switches from daylight saving time to standard time.</span></span>

<span data-ttu-id="0ccbe-105">Por ejemplo, si se especifica una zona horaria con las propiedades siguientes:</span><span class="sxs-lookup"><span data-stu-id="0ccbe-105">For example, if a time zone is specified with the following properties:</span></span>

- <span data-ttu-id="0ccbe-106">**dayOccurrence** es 3.</span><span class="sxs-lookup"><span data-stu-id="0ccbe-106">**dayOccurrence** is 3</span></span>
- <span data-ttu-id="0ccbe-107">**dayOfWeek** es "Domingo".</span><span class="sxs-lookup"><span data-stu-id="0ccbe-107">**dayOfWeek** is "Sunday"</span></span>
- <span data-ttu-id="0ccbe-108">**month** es 10.</span><span class="sxs-lookup"><span data-stu-id="0ccbe-108">**month** is 10</span></span>
- <span data-ttu-id="0ccbe-109">**time** es 02:00:00 y **year** es 0. Eso significa que la transición del horario de verano al estándar se produce todos los años a las 2:00 del tercer domingo de octubre.</span><span class="sxs-lookup"><span data-stu-id="0ccbe-109">**time** is 02:00:00 _ **year** is 0 That means the transition from daylight saving time to standard occurs at 2 AM on the third Sunday of October, every year.</span></span>

## <a name="properties"></a><span data-ttu-id="0ccbe-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0ccbe-110">Properties</span></span>
| <span data-ttu-id="0ccbe-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0ccbe-111">Property</span></span>     | <span data-ttu-id="0ccbe-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ccbe-112">Type</span></span>   |<span data-ttu-id="0ccbe-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ccbe-113">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="0ccbe-114">dayOccurrence</span><span class="sxs-lookup"><span data-stu-id="0ccbe-114">dayOccurrence</span></span> | <span data-ttu-id="0ccbe-115">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="0ccbe-115">Edm.Int32</span></span> | <span data-ttu-id="0ccbe-116">Representa la enésima repetición del día de la semana en el que se produce la transición del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="0ccbe-116">Represents the nth occurrence of the day of week that the transition from daylight saving time to standard time occurs.</span></span> |
| <span data-ttu-id="0ccbe-117">dayOfWeek</span><span class="sxs-lookup"><span data-stu-id="0ccbe-117">dayOfWeek</span></span> | <span data-ttu-id="0ccbe-118">dayOfWeek</span><span class="sxs-lookup"><span data-stu-id="0ccbe-118">dayOfWeek</span></span> | <span data-ttu-id="0ccbe-119">Representa el día de la semana en el que se produce la transición del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="0ccbe-119">Represents the day of the week when the transition from daylight saving time to standard time.</span></span> |
| <span data-ttu-id="0ccbe-120">month</span><span class="sxs-lookup"><span data-stu-id="0ccbe-120">month</span></span> | <span data-ttu-id="0ccbe-121">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="0ccbe-121">Edm.Int32</span></span> | <span data-ttu-id="0ccbe-122">Representa el mes del año en el que se produce la transición del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="0ccbe-122">Represents the month of the year when the transition from daylight saving time to standard time occurs.</span></span> |
| <span data-ttu-id="0ccbe-123">time</span><span class="sxs-lookup"><span data-stu-id="0ccbe-123">time</span></span> | <span data-ttu-id="0ccbe-124">Edm.TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="0ccbe-124">Edm.TimeOfDay</span></span> | <span data-ttu-id="0ccbe-125">Representa la hora del día en la que se produce la transición del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="0ccbe-125">Represents the time of day when the transition from daylight saving time to standard time occurs.</span></span> |
| <span data-ttu-id="0ccbe-126">year</span><span class="sxs-lookup"><span data-stu-id="0ccbe-126">year</span></span> | <span data-ttu-id="0ccbe-127">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="0ccbe-127">Edm.Int32</span></span> | <span data-ttu-id="0ccbe-128">Representa la frecuencia en términos de años con que se produce el cambio del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="0ccbe-128">Represents how frequently in terms of years the change from daylight saving time to standard time occurs.</span></span> <span data-ttu-id="0ccbe-129">Por ejemplo, un valor 0 significa todos los años.</span><span class="sxs-lookup"><span data-stu-id="0ccbe-129">For example, a value of 0 means every year.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="0ccbe-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0ccbe-130">JSON representation</span></span>

<span data-ttu-id="0ccbe-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0ccbe-131">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.standardTimeZoneOffset"
}-->

```json
{
  "dayOccurrence": "Int32",
  "dayOfWeek": "string",
  "month": "Int32",
  "time": "TimeOfDay",
  "year": "Int32"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "standardTimeZoneOffset resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
