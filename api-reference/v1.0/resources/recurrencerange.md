---
title: Tipo de recurso recurrenceRange
description: 'Describe un intervalo de fechas durante el que se repite un evento periódico. '
localization_priority: Normal
ms.openlocfilehash: 4129b698e48b01e0208b88fbdc57fb777835cd4e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27872992"
---
# <a name="recurrencerange-resource-type"></a><span data-ttu-id="bc885-103">Tipo de recurso recurrenceRange</span><span class="sxs-lookup"><span data-stu-id="bc885-103">recurrenceRange resource type</span></span>

<span data-ttu-id="bc885-104">Describe un intervalo de fechas durante el que se repite un [evento](event.md) periódico.</span><span class="sxs-lookup"><span data-stu-id="bc885-104">Describes a date range over which a recurring [event](event.md) repeats.</span></span> 

<span data-ttu-id="bc885-105">Puede especificar el intervalo de fechas para un evento periódico de tres maneras según su situación.</span><span class="sxs-lookup"><span data-stu-id="bc885-105">You can specify the date range for a recurring event in one of 3 ways depending on your scenario.</span></span> <span data-ttu-id="bc885-106">Aunque siempre debe especificar un valor **startDate** para el intervalo de fechas, puede especificar un evento periódico que finaliza en una fecha específica, que no termina o que finaliza tras un número específico de repeticiones.</span><span class="sxs-lookup"><span data-stu-id="bc885-106">While you must always specify a **startDate** value for the date range, you can specify a recurring event that ends by a specific date, or that doesn't end, or that ends after a specific number of occurrences.</span></span> <span data-ttu-id="bc885-107">Tenga en cuenta que las repeticiones reales dentro del intervalo de fechas siempre seguirán el patrón de periodicidad que especifique para el evento periódico.</span><span class="sxs-lookup"><span data-stu-id="bc885-107">Note that the actual occurrences within the date range always follow the recurrence pattern that you specify for the recurring event.</span></span> <span data-ttu-id="bc885-108">Un evento periódico siempre se define por su valor [recurrencePattern](recurrencepattern.md) (con qué frecuencia se repite el evento) y su valor **recurrenceRange** (durante cuánto tiempo se repite el evento).</span><span class="sxs-lookup"><span data-stu-id="bc885-108">A recurring event is always defined by its [recurrencePattern](recurrencepattern.md) (how frequently the event repeats), and its **recurrenceRange** (for how long the event repeats).</span></span>

## <a name="properties"></a><span data-ttu-id="bc885-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bc885-109">Properties</span></span>

| <span data-ttu-id="bc885-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bc885-110">Property</span></span>     | <span data-ttu-id="bc885-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc885-111">Type</span></span>   |<span data-ttu-id="bc885-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc885-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bc885-113">endDate</span><span class="sxs-lookup"><span data-stu-id="bc885-113">endDate</span></span>|<span data-ttu-id="bc885-114">Fecha</span><span class="sxs-lookup"><span data-stu-id="bc885-114">Date</span></span>|<span data-ttu-id="bc885-115">Fecha en la que se detiene la aplicación del patrón de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="bc885-115">The date to stop applying the recurrence pattern.</span></span> <span data-ttu-id="bc885-116">Según el patrón de periodicidad del evento, la última repetición de la reunión no puede ser esta fecha.</span><span class="sxs-lookup"><span data-stu-id="bc885-116">Depending on the recurrence pattern of the event, the last occurrence of the meeting may not be this date.</span></span> <span data-ttu-id="bc885-117">Se requiere si **type** es `endDate`.</span><span class="sxs-lookup"><span data-stu-id="bc885-117">Required if **type** is `endDate`.</span></span>|
|<span data-ttu-id="bc885-118">numberOfOccurrences</span><span class="sxs-lookup"><span data-stu-id="bc885-118">numberOfOccurrences</span></span>|<span data-ttu-id="bc885-119">Int32</span><span class="sxs-lookup"><span data-stu-id="bc885-119">Int32</span></span>|<span data-ttu-id="bc885-120">Número de veces que se repite el evento.</span><span class="sxs-lookup"><span data-stu-id="bc885-120">The number of times to repeat the event.</span></span> <span data-ttu-id="bc885-121">Se requiere y debe ser positivo si **type** es `numbered`.</span><span class="sxs-lookup"><span data-stu-id="bc885-121">Required and must be positive if **type** is `numbered`.</span></span>|
|<span data-ttu-id="bc885-122">recurrenceTimeZone</span><span class="sxs-lookup"><span data-stu-id="bc885-122">recurrenceTimeZone</span></span>|<span data-ttu-id="bc885-123">String</span><span class="sxs-lookup"><span data-stu-id="bc885-123">String</span></span> |<span data-ttu-id="bc885-124">Zona horaria de las propiedades **startDate** y **endDate**.</span><span class="sxs-lookup"><span data-stu-id="bc885-124">Time zone for the **startDate** and **endDate** properties.</span></span> <span data-ttu-id="bc885-125">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bc885-125">Optional.</span></span> <span data-ttu-id="bc885-126">Si no se especifica, se usa la zona horaria del evento.</span><span class="sxs-lookup"><span data-stu-id="bc885-126">If not specified, the time zone of the event is used.</span></span>|
|<span data-ttu-id="bc885-127">startDate</span><span class="sxs-lookup"><span data-stu-id="bc885-127">startDate</span></span>|<span data-ttu-id="bc885-128">Fecha</span><span class="sxs-lookup"><span data-stu-id="bc885-128">Date</span></span>|<span data-ttu-id="bc885-129">Fecha en la que se inicia la aplicación del patrón de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="bc885-129">The date to start applying the recurrence pattern.</span></span> <span data-ttu-id="bc885-130">La primera repetición de la reunión puede ser esta fecha o una posterior, en función del patrón de periodicidad del evento.</span><span class="sxs-lookup"><span data-stu-id="bc885-130">The first occurrence of the meeting may be this date or later, depending on the recurrence pattern of the event.</span></span> <span data-ttu-id="bc885-131">Debe ser el mismo valor que la propiedad **start** del [evento](event.md) periódico.</span><span class="sxs-lookup"><span data-stu-id="bc885-131">Must be the same value as the **start** property of the recurring [event](event.md).</span></span> <span data-ttu-id="bc885-132">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bc885-132">Required.</span></span>|
|<span data-ttu-id="bc885-133">type</span><span class="sxs-lookup"><span data-stu-id="bc885-133">type</span></span>|<span data-ttu-id="bc885-134">recurrenceRangeType</span><span class="sxs-lookup"><span data-stu-id="bc885-134">recurrenceRangeType</span></span>|<span data-ttu-id="bc885-135">Intervalo de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="bc885-135">The recurrence range.</span></span> <span data-ttu-id="bc885-136">Los valores posibles son: `endDate`, `noEnd`, `numbered`.</span><span class="sxs-lookup"><span data-stu-id="bc885-136">The possible values are: `endDate`, `noEnd`, `numbered`.</span></span> <span data-ttu-id="bc885-137">Necesario.</span><span class="sxs-lookup"><span data-stu-id="bc885-137">Required.</span></span>|

<span data-ttu-id="bc885-138">Use la propiedad **type** para especificar los diferentes tipos de **recurrenceRange**.</span><span class="sxs-lookup"><span data-stu-id="bc885-138">Use the **type** property to specify the different types of **recurrenceRange**.</span></span> <span data-ttu-id="bc885-139">Tenga en cuenta las propiedades necesarias para cada tipo, tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="bc885-139">Note the required properties for each type, as described in the following table.</span></span>

| <span data-ttu-id="bc885-140">Propiedad type</span><span class="sxs-lookup"><span data-stu-id="bc885-140">type property</span></span>  | <span data-ttu-id="bc885-141">Tipo de intervalo de frecuencia</span><span class="sxs-lookup"><span data-stu-id="bc885-141">Type of recurrence range</span></span> | <span data-ttu-id="bc885-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc885-142">Description</span></span> | <span data-ttu-id="bc885-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bc885-143">Example</span></span> | <span data-ttu-id="bc885-144">Propiedades requeridas</span><span class="sxs-lookup"><span data-stu-id="bc885-144">Required properties</span></span> |
|:-------|:---------------|:--------|:--------|:--------|
|`endDate` |<span data-ttu-id="bc885-145">Rango con fecha final</span><span class="sxs-lookup"><span data-stu-id="bc885-145">Range with end date</span></span> | <span data-ttu-id="bc885-146">El evento se repetirá durante todos los días que formen parte del patrón de frecuencia correspondiente, entre los valores **startDate** y **endDate**, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="bc885-146">Event repeats on all the days that fit the corresponding recurrence pattern between the **startDate** and **endDate** inclusive.</span></span> | <span data-ttu-id="bc885-147">Repite el evento en el intervalo de fechas entre el 1 de junio de 2017 y el 15 de junio de 2017.</span><span class="sxs-lookup"><span data-stu-id="bc885-147">Repeat event in the date range between June 1, 2017 and June 15, 2017.</span></span> | <span data-ttu-id="bc885-148">**type**, **startDate**, **endDate**</span><span class="sxs-lookup"><span data-stu-id="bc885-148">**type**, **startDate**, **endDate**</span></span> | 
|`noEnd`  |<span data-ttu-id="bc885-149">Intervalo sin fecha final</span><span class="sxs-lookup"><span data-stu-id="bc885-149">Range without an end date</span></span> | <span data-ttu-id="bc885-150">El evento se repetirá todos los días que formen parte del patrón de frecuencia correspondiente, que empieza el **startDate**.</span><span class="sxs-lookup"><span data-stu-id="bc885-150">Event repeats on all the days that fit the corresponding recurrence pattern beginning on the **startDate**.</span></span> | <span data-ttu-id="bc885-151">Repite indefinidamente el evento en el intervalo de fechas a partir del 1 de junio de 2017.</span><span class="sxs-lookup"><span data-stu-id="bc885-151">Repeat event in the date range starting on June 1, 2017 indefinitely.</span></span> | <span data-ttu-id="bc885-152">**type**, **startDate**</span><span class="sxs-lookup"><span data-stu-id="bc885-152">**type**, **startDate**</span></span> |
|`numbered`|<span data-ttu-id="bc885-153">Intervalo con un número de repeticiones concreto</span><span class="sxs-lookup"><span data-stu-id="bc885-153">Range with specific number of occurrences</span></span> | <span data-ttu-id="bc885-154">El evento se repite según el valor **numberOfOccurrences**, que se basa en el patrón de frecuencia que empieza en el momento especificado en **startDate**.</span><span class="sxs-lookup"><span data-stu-id="bc885-154">Event repeats for the **numberOfOccurrences** based on the recurrence pattern beginning on the **startDate**.</span></span> | <span data-ttu-id="bc885-155">Repita el evento 10 veces en el intervalo de fechas a partir del 1 de junio de 2017.</span><span class="sxs-lookup"><span data-stu-id="bc885-155">Repeat event in the date range starting on June 1, 2017, for 10 occurrences.</span></span>  | <span data-ttu-id="bc885-156">**type**, **startDate**, **numberOfOccurrences**</span><span class="sxs-lookup"><span data-stu-id="bc885-156">**type**, **startDate**, **numberOfOccurrences**</span></span> |


## <a name="json-representation"></a><span data-ttu-id="bc885-157">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bc885-157">JSON representation</span></span>

<span data-ttu-id="bc885-158">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="bc885-158">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.recurrenceRange"
}-->

```json
{
  "endDate": "String (timestamp)",
  "numberOfOccurrences": 1024,
  "recurrenceTimeZone": "string",
  "startDate": "String (timestamp)",
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "recurrenceRange resource",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
      "Warning: /api-reference/v1.0/resources/recurrencerange.md:
      Failed to parse any rows out of table with headers: | type property  | Type of recurrence range | Description | Example | Required properties |"
  ],
  "tocPath": ""
}-->
