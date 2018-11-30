---
title: Tipo de recurso daylightTimeZoneOffset
description: Especifica cuándo una zona horaria cambia de la hora estándar al horario de verano.
ms.openlocfilehash: bab5be49e88de1c71c7d13f53c15158e4a253a6a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028586"
---
# <a name="daylighttimezoneoffset-resource-type"></a><span data-ttu-id="5a81c-103">Tipo de recurso daylightTimeZoneOffset</span><span class="sxs-lookup"><span data-stu-id="5a81c-103">daylightTimeZoneOffset resource type</span></span>

<span data-ttu-id="5a81c-104">Especifica cuándo una zona horaria cambia de la hora estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="5a81c-104">Specifies when a time zone switches from standard time to daylight saving time.</span></span>

<span data-ttu-id="5a81c-105">Por ejemplo, si se especifica una zona horaria con las propiedades siguientes:</span><span class="sxs-lookup"><span data-stu-id="5a81c-105">For example, if a time zone is specified with the following properties:</span></span>

- <span data-ttu-id="5a81c-106">**bias** es 300.</span><span class="sxs-lookup"><span data-stu-id="5a81c-106">**bias** is 300</span></span>
- <span data-ttu-id="5a81c-107">**daylightBias** es -100.</span><span class="sxs-lookup"><span data-stu-id="5a81c-107">**daylightBias** is -100</span></span>
- <span data-ttu-id="5a81c-108">**dayOccurrence** es 4.</span><span class="sxs-lookup"><span data-stu-id="5a81c-108">**dayOccurrence** is 4</span></span>
- <span data-ttu-id="5a81c-109">**dayOfWeek** es "Domingo".</span><span class="sxs-lookup"><span data-stu-id="5a81c-109">**dayOfWeek** is "sunday"</span></span>
- <span data-ttu-id="5a81c-110">**month** es 5.</span><span class="sxs-lookup"><span data-stu-id="5a81c-110">**month** is 5</span></span>
- <span data-ttu-id="5a81c-111">**time** es 02:00:00 y **year** es 0. Esto significa que la hora durante el horario de verano es +300-100 = 200 minutos de antelación a UTC.</span><span class="sxs-lookup"><span data-stu-id="5a81c-111">**time** is 02:00:00 _ **year** is 0 That means the time during daylight saving time is +300-100=200 minutes ahead of UTC.</span></span> <span data-ttu-id="5a81c-112">La transición del horario de verano al estándar se produce todos los años a las 2:00 del cuarto domingo de mayo.</span><span class="sxs-lookup"><span data-stu-id="5a81c-112">The time zone transition from daylight saving time to standard occurs at 2 AM on the fourth Sunday of May, every year.</span></span>


## <a name="properties"></a><span data-ttu-id="5a81c-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5a81c-113">Properties</span></span>
| <span data-ttu-id="5a81c-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5a81c-114">Property</span></span>     | <span data-ttu-id="5a81c-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="5a81c-115">Type</span></span>   |<span data-ttu-id="5a81c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a81c-116">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="5a81c-117">daylightBias</span><span class="sxs-lookup"><span data-stu-id="5a81c-117">daylightBias</span></span> | <span data-ttu-id="5a81c-118">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="5a81c-118">Edm.Int32</span></span> | <span data-ttu-id="5a81c-119">Diferencia horaria con respecto a la hora universal coordinada (UTC) durante el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="5a81c-119">The time offset from Coordinated Universal Time (UTC) for daylight saving time.</span></span> <span data-ttu-id="5a81c-120">Este valor está en minutos.</span><span class="sxs-lookup"><span data-stu-id="5a81c-120">This value is in minutes.</span></span>  |
| <span data-ttu-id="5a81c-121">dayOccurrence</span><span class="sxs-lookup"><span data-stu-id="5a81c-121">dayOccurrence</span></span> | <span data-ttu-id="5a81c-122">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="5a81c-122">Edm.Int32</span></span> | <span data-ttu-id="5a81c-123">Representa la enésima repetición del día de la semana en que se produce la transición de la hora estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="5a81c-123">Represents the nth occurrence of the day of week that the transition from standard time to daylight saving time occurs.</span></span> |
| <span data-ttu-id="5a81c-124">dayOfWeek</span><span class="sxs-lookup"><span data-stu-id="5a81c-124">dayOfWeek</span></span> | <span data-ttu-id="5a81c-125">string</span><span class="sxs-lookup"><span data-stu-id="5a81c-125">string</span></span> | <span data-ttu-id="5a81c-126">Representa el día de la semana en el que se produce la transición de la hora estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="5a81c-126">Represents the day of the week when the transition from standard time to daylight saving time occurs.</span></span> |
| <span data-ttu-id="5a81c-127">month</span><span class="sxs-lookup"><span data-stu-id="5a81c-127">month</span></span> | <span data-ttu-id="5a81c-128">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="5a81c-128">Edm.Int32</span></span> | <span data-ttu-id="5a81c-129">Representa el mes del año en el que se produce la transición de la hora estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="5a81c-129">Represents the month of the year when the transition from standard time to daylight saving time occurs.</span></span> |
| <span data-ttu-id="5a81c-130">time</span><span class="sxs-lookup"><span data-stu-id="5a81c-130">time</span></span> | <span data-ttu-id="5a81c-131">Edm.TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="5a81c-131">Edm.TimeOfDay</span></span> | <span data-ttu-id="5a81c-132">Representa la hora del día en la que se produce la transición de la hora estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="5a81c-132">Represents the time of day when the transition from standard time to daylight saving time occurs.</span></span> |
| <span data-ttu-id="5a81c-133">year</span><span class="sxs-lookup"><span data-stu-id="5a81c-133">year</span></span> | <span data-ttu-id="5a81c-134">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="5a81c-134">Edm.Int32</span></span> | <span data-ttu-id="5a81c-135">Representa la frecuencia en términos de años con que se produce el cambio de la hora estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="5a81c-135">Represents how frequently in terms of years the change from standard time to daylight saving time occurs.</span></span> <span data-ttu-id="5a81c-136">Por ejemplo, un valor 0 significa todos los años.</span><span class="sxs-lookup"><span data-stu-id="5a81c-136">For example, a value of 0 means every year.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="5a81c-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5a81c-137">JSON representation</span></span>

<span data-ttu-id="5a81c-138">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5a81c-138">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "baseType": "microsoft.graph.standardTimeZoneOffset",
  "@odata.type": "microsoft.graph.daylightTimeZoneOffset"
}-->

```json
{
  "daylightBias": "Int32",
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
  "description": "daylightTimeZoneOffset resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->