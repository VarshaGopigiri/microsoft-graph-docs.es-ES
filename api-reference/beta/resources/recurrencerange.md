---
title: Tipo de recurso recurrenceRange
description: 'Describe un intervalo de fechas durante el que se repite un evento periódico. '
ms.openlocfilehash: f3d627606dc9d0d41dd52f735ab87052d731af0d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086240"
---
# <a name="recurrencerange-resource-type"></a><span data-ttu-id="9c64a-103">Tipo de recurso recurrenceRange</span><span class="sxs-lookup"><span data-stu-id="9c64a-103">recurrenceRange resource type</span></span>

> <span data-ttu-id="9c64a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9c64a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9c64a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9c64a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9c64a-106">Describe un intervalo de fechas durante el que se repite un [evento](event.md) periódico.</span><span class="sxs-lookup"><span data-stu-id="9c64a-106">Describes a date range over which a recurring [event](event.md) repeats.</span></span> 

<span data-ttu-id="9c64a-107">Puede especificar el intervalo de fechas para un evento periódico de tres maneras según su situación.</span><span class="sxs-lookup"><span data-stu-id="9c64a-107">You can specify the date range for a recurring event in one of 3 ways depending on your scenario.</span></span> <span data-ttu-id="9c64a-108">Aunque siempre debe especificar un valor **startDate** para el intervalo de fechas, puede especificar un evento periódico que finaliza en una fecha específica, que no termina o que finaliza tras un número específico de repeticiones.</span><span class="sxs-lookup"><span data-stu-id="9c64a-108">While you must always specify a **startDate** value for the date range, you can specify a recurring event that ends by a specific date, or that doesn't end, or that ends after a specific number of occurrences.</span></span> <span data-ttu-id="9c64a-109">Tenga en cuenta que las repeticiones reales dentro del intervalo de fechas siempre seguirán el patrón de periodicidad que especifique para el evento periódico.</span><span class="sxs-lookup"><span data-stu-id="9c64a-109">Note that the actual occurrences within the date range always follow the recurrence pattern that you specify for the recurring event.</span></span> <span data-ttu-id="9c64a-110">Un evento periódico siempre se define por su valor [recurrencePattern](recurrencepattern.md) (con qué frecuencia se repite el evento) y su valor **recurrenceRange** (durante cuánto tiempo se repite el evento).</span><span class="sxs-lookup"><span data-stu-id="9c64a-110">A recurring event is always defined by its [recurrencePattern](recurrencepattern.md) (how frequently the event repeats), and its **recurrenceRange** (for how long the event repeats).</span></span>


## <a name="properties"></a><span data-ttu-id="9c64a-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9c64a-111">Properties</span></span>

| <span data-ttu-id="9c64a-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9c64a-112">Property</span></span>     | <span data-ttu-id="9c64a-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="9c64a-113">Type</span></span>   |<span data-ttu-id="9c64a-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c64a-114">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9c64a-115">endDate</span><span class="sxs-lookup"><span data-stu-id="9c64a-115">endDate</span></span>|<span data-ttu-id="9c64a-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="9c64a-116">Date</span></span>|<span data-ttu-id="9c64a-117">Fecha en la que se detiene la aplicación del patrón de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="9c64a-117">The date to stop applying the recurrence pattern.</span></span> <span data-ttu-id="9c64a-118">Según el patrón de periodicidad del evento, la última repetición de la reunión no puede ser esta fecha.</span><span class="sxs-lookup"><span data-stu-id="9c64a-118">Depending on the recurrence pattern of the event, the last occurrence of the meeting may not be this date.</span></span> <span data-ttu-id="9c64a-119">Se requiere si **type** es `endDate`.</span><span class="sxs-lookup"><span data-stu-id="9c64a-119">Required if **type** is `endDate`.</span></span>|
|<span data-ttu-id="9c64a-120">numberOfOccurrences</span><span class="sxs-lookup"><span data-stu-id="9c64a-120">numberOfOccurrences</span></span>|<span data-ttu-id="9c64a-121">Int32</span><span class="sxs-lookup"><span data-stu-id="9c64a-121">Int32</span></span>|<span data-ttu-id="9c64a-122">Número de veces que se repite el evento.</span><span class="sxs-lookup"><span data-stu-id="9c64a-122">The number of times to repeat the event.</span></span> <span data-ttu-id="9c64a-123">Se requiere y debe ser positivo si **type** es `numbered`.</span><span class="sxs-lookup"><span data-stu-id="9c64a-123">Required and must be positive if **type** is `numbered`.</span></span>|
|<span data-ttu-id="9c64a-124">recurrenceTimeZone</span><span class="sxs-lookup"><span data-stu-id="9c64a-124">recurrenceTimeZone</span></span>|<span data-ttu-id="9c64a-125">String</span><span class="sxs-lookup"><span data-stu-id="9c64a-125">String</span></span> |<span data-ttu-id="9c64a-126">Zona horaria de las propiedades **startDate** y **endDate**.</span><span class="sxs-lookup"><span data-stu-id="9c64a-126">Time zone for the **startDate** and **endDate** properties.</span></span> <span data-ttu-id="9c64a-127">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9c64a-127">Optional.</span></span> <span data-ttu-id="9c64a-128">Si no se especifica, se usa la zona horaria del evento.</span><span class="sxs-lookup"><span data-stu-id="9c64a-128">If not specified, the time zone of the event is used.</span></span>|
|<span data-ttu-id="9c64a-129">startDate</span><span class="sxs-lookup"><span data-stu-id="9c64a-129">startDate</span></span>|<span data-ttu-id="9c64a-130">Fecha</span><span class="sxs-lookup"><span data-stu-id="9c64a-130">Date</span></span>|<span data-ttu-id="9c64a-131">Fecha en la que se inicia la aplicación del patrón de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="9c64a-131">The date to start applying the recurrence pattern.</span></span> <span data-ttu-id="9c64a-132">La primera repetición de la reunión puede ser esta fecha o una posterior, en función del patrón de periodicidad del evento.</span><span class="sxs-lookup"><span data-stu-id="9c64a-132">The first occurrence of the meeting may be this date or later, depending on the recurrence pattern of the event.</span></span> <span data-ttu-id="9c64a-133">Debe ser el mismo valor que la propiedad **start** del [evento](event.md) periódico.</span><span class="sxs-lookup"><span data-stu-id="9c64a-133">Must be the same value as the **start** property of the recurring [event](event.md).</span></span> <span data-ttu-id="9c64a-134">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9c64a-134">Required.</span></span>|
|<span data-ttu-id="9c64a-135">type</span><span class="sxs-lookup"><span data-stu-id="9c64a-135">type</span></span>|<span data-ttu-id="9c64a-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="9c64a-136">String</span></span>|<span data-ttu-id="9c64a-137">Intervalo de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="9c64a-137">The recurrence range.</span></span> <span data-ttu-id="9c64a-138">Valores posibles: `endDate`, `noEnd`, `numbered`.</span><span class="sxs-lookup"><span data-stu-id="9c64a-138">Possible values are: `endDate`, `noEnd`, `numbered`.</span></span> <span data-ttu-id="9c64a-139">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9c64a-139">Required.</span></span>|

<span data-ttu-id="9c64a-140">Use la propiedad **type** para especificar los diferentes tipos de **recurrenceRange**.</span><span class="sxs-lookup"><span data-stu-id="9c64a-140">Use the **type** property to specify the different types of **recurrenceRange**.</span></span> <span data-ttu-id="9c64a-141">Tenga en cuenta las propiedades necesarias para cada tipo, tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="9c64a-141">Note the required properties for each type, as described in the following table.</span></span>

| <span data-ttu-id="9c64a-142">Propiedad type</span><span class="sxs-lookup"><span data-stu-id="9c64a-142">type property</span></span>  | <span data-ttu-id="9c64a-143">Tipo de intervalo de frecuencia</span><span class="sxs-lookup"><span data-stu-id="9c64a-143">Type of recurrence range</span></span> | <span data-ttu-id="9c64a-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c64a-144">Description</span></span> | <span data-ttu-id="9c64a-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9c64a-145">Example</span></span> | <span data-ttu-id="9c64a-146">Propiedades requeridas</span><span class="sxs-lookup"><span data-stu-id="9c64a-146">Required properties</span></span> |
|:-------|:---------------|:--------|:--------|:--------|
|`endDate` |<span data-ttu-id="9c64a-147">Rango con fecha final</span><span class="sxs-lookup"><span data-stu-id="9c64a-147">Range with end date</span></span> | <span data-ttu-id="9c64a-148">El evento se repetirá durante todos los días que formen parte del patrón de frecuencia correspondiente, entre los valores **startDate** y **endDate**, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="9c64a-148">Event repeats on all the days that fit the corresponding recurrence pattern between the **startDate** and **endDate** inclusive.</span></span> | <span data-ttu-id="9c64a-149">Repite el evento en el intervalo de fechas entre el 1 de junio de 2017 y el 15 de junio de 2017.</span><span class="sxs-lookup"><span data-stu-id="9c64a-149">Repeat event in the date range between June 1, 2017 and June 15, 2017.</span></span> | <span data-ttu-id="9c64a-150">**type**, **startDate**, **endDate**</span><span class="sxs-lookup"><span data-stu-id="9c64a-150">**type**, **startDate**, **endDate**</span></span> | 
|`noEnd`   |<span data-ttu-id="9c64a-151">Intervalo sin fecha final</span><span class="sxs-lookup"><span data-stu-id="9c64a-151">Range without an end date</span></span> | <span data-ttu-id="9c64a-152">El evento se repetirá todos los días que formen parte del patrón de frecuencia correspondiente, que empieza el **startDate**.</span><span class="sxs-lookup"><span data-stu-id="9c64a-152">Event repeats on all the days that fit the corresponding recurrence pattern beginning on the **startDate**.</span></span> | <span data-ttu-id="9c64a-153">Repite indefinidamente el evento en el intervalo de fechas a partir del 1 de junio de 2017.</span><span class="sxs-lookup"><span data-stu-id="9c64a-153">Repeat event in the date range starting on June 1, 2017 indefinitely.</span></span> | <span data-ttu-id="9c64a-154">**type**, **startDate**</span><span class="sxs-lookup"><span data-stu-id="9c64a-154">**type**, **startDate**</span></span> |
|`numbered`|<span data-ttu-id="9c64a-155">Intervalo con un número de repeticiones concreto</span><span class="sxs-lookup"><span data-stu-id="9c64a-155">Range with specific number of occurrences</span></span> | <span data-ttu-id="9c64a-156">El evento se repite según el valor **numberOfOccurrences**, que se basa en el patrón de frecuencia que empieza en el momento especificado en **startDate**.</span><span class="sxs-lookup"><span data-stu-id="9c64a-156">Event repeats for the **numberOfOccurrences** based on the recurrence pattern beginning on the **startDate**.</span></span> | <span data-ttu-id="9c64a-157">Repita el evento 10 veces en el intervalo de fechas a partir del 1 de junio de 2017.</span><span class="sxs-lookup"><span data-stu-id="9c64a-157">Repeat event in the date range starting on June 1, 2017, for 10 occurrences.</span></span>  | <span data-ttu-id="9c64a-158">**type**, **startDate**, **numberOfOccurrences**</span><span class="sxs-lookup"><span data-stu-id="9c64a-158">**type**, **startDate**, **numberOfOccurrences**</span></span> |

## <a name="json-representation"></a><span data-ttu-id="9c64a-159">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9c64a-159">JSON representation</span></span>

<span data-ttu-id="9c64a-160">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="9c64a-160">Here is a JSON representation of the resource</span></span>

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
      "Warning: /api-reference/beta/resources/recurrencerange.md:
      Failed to parse any rows out of table with headers: | type property  | Type of recurrence range | Description | Example | Required properties |"
  ],
  "tocPath": ""
}-->
