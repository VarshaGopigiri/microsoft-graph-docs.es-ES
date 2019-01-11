---
title: Tipo de recurso daylightTimeZoneOffset
description: Especifica cuándo una zona horaria cambia de la hora estándar al horario de verano.
localization_priority: Normal
ms.openlocfilehash: 37e08ec0e695fd245678510ac4a40bc978b1a93e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27825609"
---
# <a name="daylighttimezoneoffset-resource-type"></a><span data-ttu-id="31aed-103">Tipo de recurso daylightTimeZoneOffset</span><span class="sxs-lookup"><span data-stu-id="31aed-103">daylightTimeZoneOffset resource type</span></span>

> <span data-ttu-id="31aed-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="31aed-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="31aed-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="31aed-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="31aed-106">Especifica cuándo una zona horaria cambia de la hora estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="31aed-106">Specifies when a time zone switches from standard time to daylight saving time.</span></span>

<span data-ttu-id="31aed-107">Por ejemplo, si se especifica una zona horaria con las propiedades siguientes:</span><span class="sxs-lookup"><span data-stu-id="31aed-107">For example, if a time zone is specified with the following properties:</span></span>

- <span data-ttu-id="31aed-108">**bias** es 300.</span><span class="sxs-lookup"><span data-stu-id="31aed-108">**bias** is 300</span></span>
- <span data-ttu-id="31aed-109">**daylightBias** es -100.</span><span class="sxs-lookup"><span data-stu-id="31aed-109">**daylightBias** is -100</span></span>
- <span data-ttu-id="31aed-110">**dayOccurrence** es 4.</span><span class="sxs-lookup"><span data-stu-id="31aed-110">**dayOccurrence** is 4</span></span>
- <span data-ttu-id="31aed-111">**dayOfWeek** es "Domingo".</span><span class="sxs-lookup"><span data-stu-id="31aed-111">**dayOfWeek** is "sunday"</span></span>
- <span data-ttu-id="31aed-112">**month** es 5.</span><span class="sxs-lookup"><span data-stu-id="31aed-112">**month** is 5</span></span>
- <span data-ttu-id="31aed-113">**time** es 02:00:00 y **year** es 0. Esto significa que la hora durante el horario de verano es +300-100 = 200 minutos de antelación a UTC.</span><span class="sxs-lookup"><span data-stu-id="31aed-113">**time** is 02:00:00 _ **year** is 0 That means the time during daylight saving time is +300-100=200 minutes ahead of UTC.</span></span> <span data-ttu-id="31aed-114">La transición del horario de verano al estándar se produce todos los años a las 2:00 del cuarto domingo de mayo.</span><span class="sxs-lookup"><span data-stu-id="31aed-114">The time zone transition from daylight saving time to standard occurs at 2 AM on the fourth Sunday of May, every year.</span></span>


## <a name="properties"></a><span data-ttu-id="31aed-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="31aed-115">Properties</span></span>
| <span data-ttu-id="31aed-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="31aed-116">Property</span></span>     | <span data-ttu-id="31aed-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="31aed-117">Type</span></span>   |<span data-ttu-id="31aed-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="31aed-118">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="31aed-119">daylightBias</span><span class="sxs-lookup"><span data-stu-id="31aed-119">daylightBias</span></span> | <span data-ttu-id="31aed-120">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="31aed-120">Edm.Int32</span></span> | <span data-ttu-id="31aed-121">Diferencia horaria con respecto a la hora universal coordinada (UTC) durante el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="31aed-121">The time offset from Coordinated Universal Time (UTC) for daylight saving time.</span></span> <span data-ttu-id="31aed-122">Este valor está en minutos.</span><span class="sxs-lookup"><span data-stu-id="31aed-122">This value is in minutes.</span></span>  |
| <span data-ttu-id="31aed-123">dayOccurrence</span><span class="sxs-lookup"><span data-stu-id="31aed-123">dayOccurrence</span></span> | <span data-ttu-id="31aed-124">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="31aed-124">Edm.Int32</span></span> | <span data-ttu-id="31aed-125">Representa la enésima repetición del día de la semana en que se produce la transición de la hora estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="31aed-125">Represents the nth occurrence of the day of week that the transition from standard time to daylight saving time occurs.</span></span> |
| <span data-ttu-id="31aed-126">dayOfWeek</span><span class="sxs-lookup"><span data-stu-id="31aed-126">dayOfWeek</span></span> | <span data-ttu-id="31aed-127">string</span><span class="sxs-lookup"><span data-stu-id="31aed-127">string</span></span> | <span data-ttu-id="31aed-128">Representa el día de la semana en el que se produce la transición de la hora estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="31aed-128">Represents the day of the week when the transition from standard time to daylight saving time occurs.</span></span> |
| <span data-ttu-id="31aed-129">month</span><span class="sxs-lookup"><span data-stu-id="31aed-129">month</span></span> | <span data-ttu-id="31aed-130">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="31aed-130">Edm.Int32</span></span> | <span data-ttu-id="31aed-131">Representa el mes del año en el que se produce la transición de la hora estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="31aed-131">Represents the month of the year when the transition from standard time to daylight saving time occurs.</span></span> |
| <span data-ttu-id="31aed-132">time</span><span class="sxs-lookup"><span data-stu-id="31aed-132">time</span></span> | <span data-ttu-id="31aed-133">Edm.TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="31aed-133">Edm.TimeOfDay</span></span> | <span data-ttu-id="31aed-134">Representa la hora del día en la que se produce la transición de la hora estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="31aed-134">Represents the time of day when the transition from standard time to daylight saving time occurs.</span></span> |
| <span data-ttu-id="31aed-135">year</span><span class="sxs-lookup"><span data-stu-id="31aed-135">year</span></span> | <span data-ttu-id="31aed-136">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="31aed-136">Edm.Int32</span></span> | <span data-ttu-id="31aed-137">Representa la frecuencia en términos de años con que se produce el cambio de la hora estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="31aed-137">Represents how frequently in terms of years the change from standard time to daylight saving time occurs.</span></span> <span data-ttu-id="31aed-138">Por ejemplo, un valor 0 significa todos los años.</span><span class="sxs-lookup"><span data-stu-id="31aed-138">For example, a value of 0 means every year.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="31aed-139">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="31aed-139">JSON representation</span></span>

<span data-ttu-id="31aed-140">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="31aed-140">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
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
