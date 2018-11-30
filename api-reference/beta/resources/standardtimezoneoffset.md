---
title: Tipo de recurso standardTimeZoneOffset
description: Especifica cuándo una zona horaria cambia del horario de verano a la hora estándar.
ms.openlocfilehash: 167ff45f4ccf1615c1560c3f2ba130cdc7747043
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086492"
---
# <a name="standardtimezoneoffset-resource-type"></a><span data-ttu-id="2152e-103">Tipo de recurso standardTimeZoneOffset</span><span class="sxs-lookup"><span data-stu-id="2152e-103">standardTimeZoneOffset resource type</span></span>

> <span data-ttu-id="2152e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2152e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2152e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2152e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2152e-106">Especifica cuándo una zona horaria cambia del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="2152e-106">Specifies when a time zone switches from daylight saving time to standard time.</span></span>

<span data-ttu-id="2152e-107">Por ejemplo, si se especifica una zona horaria con las propiedades siguientes:</span><span class="sxs-lookup"><span data-stu-id="2152e-107">For example, if a time zone is specified with the following properties:</span></span>

- <span data-ttu-id="2152e-108">**dayOccurrence** es 3.</span><span class="sxs-lookup"><span data-stu-id="2152e-108">**dayOccurrence** is 3</span></span>
- <span data-ttu-id="2152e-109">**dayOfWeek** es "Domingo".</span><span class="sxs-lookup"><span data-stu-id="2152e-109">**dayOfWeek** is "Sunday"</span></span>
- <span data-ttu-id="2152e-110">**month** es 10.</span><span class="sxs-lookup"><span data-stu-id="2152e-110">**month** is 10</span></span>
- <span data-ttu-id="2152e-111">**time** es 02:00:00 y **year** es 0. Eso significa que la transición del horario de verano al estándar se produce todos los años a las 2:00 del tercer domingo de octubre.</span><span class="sxs-lookup"><span data-stu-id="2152e-111">**time** is 02:00:00 _ **year** is 0 That means the transition from daylight saving time to standard occurs at 2 AM on the third Sunday of October, every year.</span></span>

## <a name="properties"></a><span data-ttu-id="2152e-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2152e-112">Properties</span></span>
| <span data-ttu-id="2152e-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2152e-113">Property</span></span>     | <span data-ttu-id="2152e-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="2152e-114">Type</span></span>   |<span data-ttu-id="2152e-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="2152e-115">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="2152e-116">dayOccurrence</span><span class="sxs-lookup"><span data-stu-id="2152e-116">dayOccurrence</span></span> | <span data-ttu-id="2152e-117">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="2152e-117">Edm.Int32</span></span> | <span data-ttu-id="2152e-118">Representa la enésima repetición del día de la semana en el que se produce la transición del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="2152e-118">Represents the nth occurrence of the day of week that the transition from daylight saving time to standard time occurs.</span></span> |
| <span data-ttu-id="2152e-119">dayOfWeek</span><span class="sxs-lookup"><span data-stu-id="2152e-119">dayOfWeek</span></span> | <span data-ttu-id="2152e-120">string</span><span class="sxs-lookup"><span data-stu-id="2152e-120">string</span></span> | <span data-ttu-id="2152e-121">Representa el día de la semana en el que se produce la transición del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="2152e-121">Represents the day of the week when the transition from daylight saving time to standard time.</span></span> |
| <span data-ttu-id="2152e-122">month</span><span class="sxs-lookup"><span data-stu-id="2152e-122">month</span></span> | <span data-ttu-id="2152e-123">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="2152e-123">Edm.Int32</span></span> | <span data-ttu-id="2152e-124">Representa el mes del año en el que se produce la transición del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="2152e-124">Represents the month of the year when the transition from daylight saving time to standard time occurs.</span></span> |
| <span data-ttu-id="2152e-125">time</span><span class="sxs-lookup"><span data-stu-id="2152e-125">time</span></span> | <span data-ttu-id="2152e-126">Edm.TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="2152e-126">Edm.TimeOfDay</span></span> | <span data-ttu-id="2152e-127">Representa la hora del día en la que se produce la transición del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="2152e-127">Represents the time of day when the transition from daylight saving time to standard time occurs.</span></span> |
| <span data-ttu-id="2152e-128">year</span><span class="sxs-lookup"><span data-stu-id="2152e-128">year</span></span> | <span data-ttu-id="2152e-129">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="2152e-129">Edm.Int32</span></span> | <span data-ttu-id="2152e-130">Representa la frecuencia en términos de años con que se produce el cambio del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="2152e-130">Represents how frequently in terms of years the change from daylight saving time to standard time occurs.</span></span> <span data-ttu-id="2152e-131">Por ejemplo, un valor 0 significa todos los años.</span><span class="sxs-lookup"><span data-stu-id="2152e-131">For example, a value of 0 means every year.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="2152e-132">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2152e-132">JSON representation</span></span>

<span data-ttu-id="2152e-133">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2152e-133">Here is a JSON representation of the resource.</span></span>

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