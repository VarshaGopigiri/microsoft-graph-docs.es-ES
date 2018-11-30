---
title: Tipo de recurso standardTimeZoneOffset
description: Especifica cuándo una zona horaria cambia del horario de verano a la hora estándar.
ms.openlocfilehash: 53c02a231d31dbdd1723fb0d8b476c988ff1d4ec
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031175"
---
# <a name="standardtimezoneoffset-resource-type"></a><span data-ttu-id="b5845-103">Tipo de recurso standardTimeZoneOffset</span><span class="sxs-lookup"><span data-stu-id="b5845-103">standardTimeZoneOffset resource type</span></span>

<span data-ttu-id="b5845-104">Especifica cuándo una zona horaria cambia del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="b5845-104">Specifies when a time zone switches from daylight saving time to standard time.</span></span>

<span data-ttu-id="b5845-105">Por ejemplo, si se especifica una zona horaria con las propiedades siguientes:</span><span class="sxs-lookup"><span data-stu-id="b5845-105">For example, if a time zone is specified with the following properties:</span></span>

- <span data-ttu-id="b5845-106">**dayOccurrence** es 3.</span><span class="sxs-lookup"><span data-stu-id="b5845-106">**dayOccurrence** is 3</span></span>
- <span data-ttu-id="b5845-107">**dayOfWeek** es "Domingo".</span><span class="sxs-lookup"><span data-stu-id="b5845-107">**dayOfWeek** is "Sunday"</span></span>
- <span data-ttu-id="b5845-108">**month** es 10.</span><span class="sxs-lookup"><span data-stu-id="b5845-108">**month** is 10</span></span>
- <span data-ttu-id="b5845-109">**time** es 02:00:00 y **year** es 0. Eso significa que la transición del horario de verano al estándar se produce todos los años a las 2:00 del tercer domingo de octubre.</span><span class="sxs-lookup"><span data-stu-id="b5845-109">**time** is 02:00:00 _ **year** is 0 That means the transition from daylight saving time to standard occurs at 2 AM on the third Sunday of October, every year.</span></span>

## <a name="properties"></a><span data-ttu-id="b5845-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b5845-110">Properties</span></span>
| <span data-ttu-id="b5845-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b5845-111">Property</span></span>     | <span data-ttu-id="b5845-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="b5845-112">Type</span></span>   |<span data-ttu-id="b5845-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5845-113">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="b5845-114">dayOccurrence</span><span class="sxs-lookup"><span data-stu-id="b5845-114">dayOccurrence</span></span> | <span data-ttu-id="b5845-115">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="b5845-115">Edm.Int32</span></span> | <span data-ttu-id="b5845-116">Representa la enésima repetición del día de la semana en el que se produce la transición del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="b5845-116">Represents the nth occurrence of the day of week that the transition from daylight saving time to standard time occurs.</span></span> |
| <span data-ttu-id="b5845-117">dayOfWeek</span><span class="sxs-lookup"><span data-stu-id="b5845-117">dayOfWeek</span></span> | <span data-ttu-id="b5845-118">dayOfWeek</span><span class="sxs-lookup"><span data-stu-id="b5845-118">dayOfWeek</span></span> | <span data-ttu-id="b5845-119">Representa el día de la semana en el que se produce la transición del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="b5845-119">Represents the day of the week when the transition from daylight saving time to standard time.</span></span> |
| <span data-ttu-id="b5845-120">month</span><span class="sxs-lookup"><span data-stu-id="b5845-120">month</span></span> | <span data-ttu-id="b5845-121">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="b5845-121">Edm.Int32</span></span> | <span data-ttu-id="b5845-122">Representa el mes del año en el que se produce la transición del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="b5845-122">Represents the month of the year when the transition from daylight saving time to standard time occurs.</span></span> |
| <span data-ttu-id="b5845-123">time</span><span class="sxs-lookup"><span data-stu-id="b5845-123">time</span></span> | <span data-ttu-id="b5845-124">Edm.TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="b5845-124">Edm.TimeOfDay</span></span> | <span data-ttu-id="b5845-125">Representa la hora del día en la que se produce la transición del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="b5845-125">Represents the time of day when the transition from daylight saving time to standard time occurs.</span></span> |
| <span data-ttu-id="b5845-126">year</span><span class="sxs-lookup"><span data-stu-id="b5845-126">year</span></span> | <span data-ttu-id="b5845-127">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="b5845-127">Edm.Int32</span></span> | <span data-ttu-id="b5845-128">Representa la frecuencia en términos de años con que se produce el cambio del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="b5845-128">Represents how frequently in terms of years the change from daylight saving time to standard time occurs.</span></span> <span data-ttu-id="b5845-129">Por ejemplo, un valor 0 significa todos los años.</span><span class="sxs-lookup"><span data-stu-id="b5845-129">For example, a value of 0 means every year.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="b5845-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b5845-130">JSON representation</span></span>

<span data-ttu-id="b5845-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b5845-131">Here is a JSON representation of the resource.</span></span>

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