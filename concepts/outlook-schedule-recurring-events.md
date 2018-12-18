---
title: Programar citas repetidas como eventos periódicos en Outlook
description: Los eventos periódicos son una parte importante del Calendario de Outlook. Ya sea una reunión semanal personal con su jefe o una reunión de revisión de todo un departamento que tiene lugar el segundo martes de cada mes, los eventos periódicos facilitan la tarea al crear el evento una sola vez y que el servidor complete el resto de la serie.
author: angelgolfer-ms
ms.openlocfilehash: 85d856cd9f59ee7df643ff74ed4b3dd9f48ba3a4
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27340078"
---
# <a name="schedule-repeating-appointments-as-recurring-events-in-outlook"></a><span data-ttu-id="d2a7a-104">Programar citas repetidas como eventos periódicos en Outlook</span><span class="sxs-lookup"><span data-stu-id="d2a7a-104">Schedule repeating appointments as recurring events in Outlook</span></span>

<span data-ttu-id="d2a7a-105">Los eventos periódicos son una parte importante del Calendario de Outlook.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-105">Recurring events are an important part of Outlook calendaring.</span></span> <span data-ttu-id="d2a7a-106">Ya sea una reunión semanal personal con su jefe o una reunión de revisión de todo un departamento que tiene lugar el segundo martes de cada mes, los eventos periódicos facilitan la tarea al crear el evento una sola vez y que el servidor complete el resto de la serie.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-106">Whether it's a weekly one-on-one meeting with your manager, or a division-wide review meeting that happens on the second Tuesday of each month, recurring events make it easy to create the event once, and let the server fill in the rest of the series.</span></span>

<span data-ttu-id="d2a7a-107">La clave de información que permite a los eventos periódicos "expandirse" en las repeticiones periódicas individuales es la regla de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-107">The key bit of information that allows recurring events to "expand" into individual occurrences is the recurrence rule.</span></span> <span data-ttu-id="d2a7a-108">La regla especifica con qué frecuencia se repite un evento y durante cuánto tiempo.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-108">The rule specifies both how often an event repeats, and for how long.</span></span> <span data-ttu-id="d2a7a-109">Las API de REST de Outlook definen las reglas de periodicidad en la propiedad **recurrence** del [recurso de evento](/graph/api/resources/event?view=graph-rest-1.0).</span><span class="sxs-lookup"><span data-stu-id="d2a7a-109">The Outlook REST APIs model recurrence rules in the **recurrence** property of the [event resource](/graph/api/resources/event?view=graph-rest-1.0).</span></span> 

<span data-ttu-id="d2a7a-110">Cada recurrencia se compone de dos partes: el patrón de periodicidad (la frecuencia) y el intervalo de periodicidad (la duración).</span><span class="sxs-lookup"><span data-stu-id="d2a7a-110">Each recurrence is made up of two parts: the recurrence pattern (how often), and the recurrence range (for how long).</span></span>

## <a name="recurrence-patterns"></a><span data-ttu-id="d2a7a-111">Patrones de periodicidad</span><span class="sxs-lookup"><span data-stu-id="d2a7a-111">Recurrence patterns</span></span>

<span data-ttu-id="d2a7a-112">La primera parte de una repetición es el patrón.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-112">The first part of a recurrence is the pattern.</span></span> <span data-ttu-id="d2a7a-113">Especifica la frecuencia con que se repite el evento.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-113">This specifies how often the event repeats.</span></span> <span data-ttu-id="d2a7a-114">Por ejemplo, un evento podría repetirse "cada 3 días", "todos los jueves" o "el 22 de julio de cada año".</span><span class="sxs-lookup"><span data-stu-id="d2a7a-114">For example, an event could repeat "every 3 days," "every Thursday," or "on July 22 every year."</span></span> <span data-ttu-id="d2a7a-115">Un patrón se representa en la API con el [recurso recurrencePattern](/graph/api/resources/recurrencepattern?view=graph-rest-1.0).</span><span class="sxs-lookup"><span data-stu-id="d2a7a-115">A pattern is represented in the API by the [recurrencePattern resource](/graph/api/resources/recurrencepattern?view=graph-rest-1.0).</span></span>

<span data-ttu-id="d2a7a-116">Según el tipo de patrón, ciertos campos de **recurrencePattern** son obligatorios, opcionales u omitidos.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-116">Depending on the type of pattern, certain fields of the **recurrencePattern** are required, optional, or ignored.</span></span>

> <span data-ttu-id="d2a7a-117">**Nota**: Incluso si se omite un campo, también se valida.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-117">**Note**: Even if a field is ignored, it is still validated.</span></span> <span data-ttu-id="d2a7a-118">Si un campo tiene una lista determinada de valores posibles, utilizar un valor fuera del conjunto permitido provocará un error, incluso si ese campo se omite.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-118">If a field has a set list of possible values, using a value outside the allowed set causes an error, even if that field is ignored.</span></span>

<span data-ttu-id="d2a7a-119">Analicemos cada uno de los tipos de patrones posibles.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-119">Let's take a look at each of the possible pattern types.</span></span>

### <a name="daily"></a><span data-ttu-id="d2a7a-120">Diario</span><span class="sxs-lookup"><span data-stu-id="d2a7a-120">Daily</span></span>

<span data-ttu-id="d2a7a-121">El patrón de periodicidad diario hace que se repita basándose en el número de días que transcurre entre cada evento.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-121">The daily recurrence pattern causes an event to repeat based on a number of days between each occurrence.</span></span>

#### <a name="relevant-properties"></a><span data-ttu-id="d2a7a-122">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="d2a7a-122">Relevant properties</span></span>

| <span data-ttu-id="d2a7a-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d2a7a-123">Property</span></span> | <span data-ttu-id="d2a7a-124">Relevancia</span><span class="sxs-lookup"><span data-stu-id="d2a7a-124">Relevance</span></span> | <span data-ttu-id="d2a7a-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2a7a-125">Description</span></span> |
|----------|-----------|-------------|
| <span data-ttu-id="d2a7a-126">**interval**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-126">**interval**</span></span> | <span data-ttu-id="d2a7a-127">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-127">Required</span></span> | <span data-ttu-id="d2a7a-128">Especifica el número de días entre cada repetición.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-128">Specifies the number of days between each occurrence.</span></span> |
| <span data-ttu-id="d2a7a-129">**type**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-129">**type**</span></span> | <span data-ttu-id="d2a7a-130">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-130">Required</span></span> | <span data-ttu-id="d2a7a-131">Se debe establecer en `daily`.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-131">Must be set to `daily`.</span></span> |

#### <a name="examples"></a><span data-ttu-id="d2a7a-132">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d2a7a-132">Examples</span></span>

- <span data-ttu-id="d2a7a-133">Repetir este evento cada día</span><span class="sxs-lookup"><span data-stu-id="d2a7a-133">Repeat this event every day</span></span>

  ```json
    "pattern": {
      "type": "daily",
      "interval": 1
    }
  ```
- <span data-ttu-id="d2a7a-134">Repetir este evento cada tres días</span><span class="sxs-lookup"><span data-stu-id="d2a7a-134">Repeat this event every three days</span></span>

  ```json
    "pattern": {
      "type": "daily",
      "interval": 3
    }
  ```

### <a name="weekly"></a><span data-ttu-id="d2a7a-135">Semanal</span><span class="sxs-lookup"><span data-stu-id="d2a7a-135">Weekly</span></span>

<span data-ttu-id="d2a7a-136">El patrón de periodicidad semanal provoca que un evento se repita en el mismo día o días de la semana, en función del número de semanas que transcurren entre cada conjunto de eventos.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-136">The weekly recurrence pattern causes an event to repeat on the same day or days of the week, based on the number of weeks between each set of occurrences.</span></span>

#### <a name="relevant-properties"></a><span data-ttu-id="d2a7a-137">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="d2a7a-137">Relevant properties</span></span>

| <span data-ttu-id="d2a7a-138">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d2a7a-138">Property</span></span> | <span data-ttu-id="d2a7a-139">Relevancia</span><span class="sxs-lookup"><span data-stu-id="d2a7a-139">Relevance</span></span> | <span data-ttu-id="d2a7a-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2a7a-140">Description</span></span> |
|----------|-----------|-------------|
| <span data-ttu-id="d2a7a-141">**daysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-141">**daysOfWeek**</span></span> | <span data-ttu-id="d2a7a-142">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-142">Required</span></span> | <span data-ttu-id="d2a7a-143">Especifica en qué días de la semana se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-143">Specifies on which day(s) of the week the event occurs.</span></span> |
| <span data-ttu-id="d2a7a-144">**firstDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-144">**firstDayOfWeek**</span></span> | <span data-ttu-id="d2a7a-145">Opcional</span><span class="sxs-lookup"><span data-stu-id="d2a7a-145">Optional</span></span> | <span data-ttu-id="d2a7a-146">Especifica qué día se considera el primer día de la semana.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-146">Specifies which day is considered the first day of the week.</span></span> <span data-ttu-id="d2a7a-147">Valor predeterminado: `Sunday`.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-147">Default value: `Sunday`.</span></span> |
| <span data-ttu-id="d2a7a-148">**interval**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-148">**interval**</span></span> | <span data-ttu-id="d2a7a-149">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-149">Required</span></span> | <span data-ttu-id="d2a7a-150">Especifica el número de semanas entre cada conjunto de eventos.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-150">Specifies the number of weeks between each set of occurrences.</span></span> |
| <span data-ttu-id="d2a7a-151">**type**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-151">**type**</span></span> | <span data-ttu-id="d2a7a-152">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-152">Required</span></span> | <span data-ttu-id="d2a7a-153">Se debe establecer en `weekly`.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-153">Must be set to `weekly`.</span></span> |

#### <a name="examples"></a><span data-ttu-id="d2a7a-154">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d2a7a-154">Examples</span></span>

- <span data-ttu-id="d2a7a-155">Repetir este evento cada jueves</span><span class="sxs-lookup"><span data-stu-id="d2a7a-155">Repeat this event every Thursday</span></span>

  ```json
    "pattern": {
      "type": "weekly",
      "interval": 1,
      "daysOfWeek": [ "Thursday" ]
    }
  ```
- <span data-ttu-id="d2a7a-156">Repetir este evento lunes y martes cada dos semanas</span><span class="sxs-lookup"><span data-stu-id="d2a7a-156">Repeat this event every other Monday and Tuesday</span></span>

  ```json
    "pattern": {
      "type": "weekly",
      "interval": 2,
      "daysOfWeek": [
        "Monday",
        "Tuesday"
      ]
    }
  ```

### <a name="absolute-monthly"></a><span data-ttu-id="d2a7a-157">Mensual absoluto</span><span class="sxs-lookup"><span data-stu-id="d2a7a-157">Absolute monthly</span></span>

<span data-ttu-id="d2a7a-158">El patrón mensual absoluto hace que un evento se repita el mismo día del mes (por ejemplo, el día 15), en función del número de meses entre cada repetición.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-158">The absolute monthly pattern causes an event to repeat on the same day of the month (for example, the 15th), based on the number of months between each occurrence.</span></span>

#### <a name="relevant-properties"></a><span data-ttu-id="d2a7a-159">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="d2a7a-159">Relevant properties</span></span>

| <span data-ttu-id="d2a7a-160">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d2a7a-160">Property</span></span> | <span data-ttu-id="d2a7a-161">Relevancia</span><span class="sxs-lookup"><span data-stu-id="d2a7a-161">Relevance</span></span> | <span data-ttu-id="d2a7a-162">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2a7a-162">Description</span></span> |
|----------|-----------|-------------|
| <span data-ttu-id="d2a7a-163">**dayOfMonth**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-163">**dayOfMonth**</span></span> | <span data-ttu-id="d2a7a-164">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-164">Required</span></span> | <span data-ttu-id="d2a7a-165">Especifica el día del mes en que se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-165">Specifies on which day of the month the event occurs.</span></span> |
| <span data-ttu-id="d2a7a-166">**interval**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-166">**interval**</span></span> | <span data-ttu-id="d2a7a-167">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-167">Required</span></span> | <span data-ttu-id="d2a7a-168">Especifica el número de meses entre cada repetición.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-168">Specifies the number of months between each occurrence.</span></span> |
| <span data-ttu-id="d2a7a-169">**type**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-169">**type**</span></span> | <span data-ttu-id="d2a7a-170">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-170">Required</span></span> | <span data-ttu-id="d2a7a-171">Se debe establecer en `absoluteMonthly`.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-171">Must be set to `absoluteMonthly`.</span></span> |

#### <a name="examples"></a><span data-ttu-id="d2a7a-172">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d2a7a-172">Examples</span></span>

- <span data-ttu-id="d2a7a-173">Repetir este evento el día 15 de cada mes</span><span class="sxs-lookup"><span data-stu-id="d2a7a-173">Repeat this event on the 15th of every month</span></span>

  ```json
    "pattern": {
      "type": "absoluteMonthly",
      "interval": 1,
      "dayOfMonth": 15
    }
  ```
- <span data-ttu-id="d2a7a-174">Repetir este evento trimestralmente (cada 3 meses) el día 7</span><span class="sxs-lookup"><span data-stu-id="d2a7a-174">Repeat this event quarterly (every 3 months) on the 7th</span></span>

  ```json
    "pattern": {
      "type": "absoluteMonthly",
      "interval": 3,
      "dayOfMonth": 7
    }
  ```

### <a name="relative-monthly"></a><span data-ttu-id="d2a7a-175">Mensual relativo</span><span class="sxs-lookup"><span data-stu-id="d2a7a-175">Relative monthly</span></span>

<span data-ttu-id="d2a7a-176">El patrón mensual relativo hace que un evento se repita el mismo día de la semana en la misma posición relativa en el mes, en función del número de meses entre cada repetición.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-176">The relative monthly pattern causes an event to repeat on the same day of the week in the same relative position in the month, based on the number of months between each occurrence.</span></span> <span data-ttu-id="d2a7a-177">Por ejemplo, "cada segundo miércoles del mes".</span><span class="sxs-lookup"><span data-stu-id="d2a7a-177">For example, "every second Wednesday of the month."</span></span>

#### <a name="relevant-properties"></a><span data-ttu-id="d2a7a-178">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="d2a7a-178">Relevant properties</span></span>

| <span data-ttu-id="d2a7a-179">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d2a7a-179">Property</span></span> | <span data-ttu-id="d2a7a-180">Relevancia</span><span class="sxs-lookup"><span data-stu-id="d2a7a-180">Relevance</span></span> | <span data-ttu-id="d2a7a-181">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2a7a-181">Description</span></span> |
|----------|-----------|-------------|
| <span data-ttu-id="d2a7a-182">**daysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-182">**daysOfWeek**</span></span> | <span data-ttu-id="d2a7a-183">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-183">Required</span></span> | <span data-ttu-id="d2a7a-184">Especifica en qué días de la semana puede producirse el evento.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-184">Specifies on which day(s) of the week the event can occur.</span></span> <span data-ttu-id="d2a7a-185">Los eventos mensuales relativos sólo ocurren una vez al mes, por lo que si especifica más de un valor, el evento tendrá lugar en el primer día que se ajuste al patrón.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-185">Relative monthly events only occur once per month, so if more than one value is specified, the event falls on the first day that satisfies the pattern.</span></span> |
| <span data-ttu-id="d2a7a-186">**index**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-186">**index**</span></span> | <span data-ttu-id="d2a7a-187">Opcional</span><span class="sxs-lookup"><span data-stu-id="d2a7a-187">Optional</span></span> | <span data-ttu-id="d2a7a-188">Especifica en qué instancia de los días permitidos especificados en **daysOfsWeek** se produce el evento, contados a partir de la primera instancia del mes.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-188">Specifies on which instance of the allowed days specified in **daysOfsWeek** the event occurs, counted from the first instance in the month.</span></span> <span data-ttu-id="d2a7a-189">Valores posibles: `first`, `second`, `third`, `fourth` y `last`.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-189">Possible values: `first`, `second`, `third`, `fourth`, and `last`.</span></span> <span data-ttu-id="d2a7a-190">Valor predeterminado: `first`.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-190">Default value: `first`.</span></span> |
| <span data-ttu-id="d2a7a-191">**interval**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-191">**interval**</span></span> | <span data-ttu-id="d2a7a-192">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-192">Required</span></span> | <span data-ttu-id="d2a7a-193">Especifica el número de meses entre cada repetición.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-193">Specifies the number of months between each occurrence.</span></span> |
| <span data-ttu-id="d2a7a-194">**type**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-194">**type**</span></span> | <span data-ttu-id="d2a7a-195">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-195">Required</span></span> | <span data-ttu-id="d2a7a-196">Se debe establecer en `relativeMonthly`.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-196">Must be set to `relativeMonthly`.</span></span> |

#### <a name="examples"></a><span data-ttu-id="d2a7a-197">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d2a7a-197">Examples</span></span>

- <span data-ttu-id="d2a7a-198">Repetir este evento el segundo miércoles de cada mes</span><span class="sxs-lookup"><span data-stu-id="d2a7a-198">Repeat this event on the second Wednesday of every month</span></span>

  ```json
    "pattern": {
      "type": "relativeMonthly",
      "interval": 1,
      "daysOfWeek": [ "Wednesday" ],
      "index": "second"
    }
  ```
- <span data-ttu-id="d2a7a-199">Repetir este evento en el primer jueves o viernes de cada mes</span><span class="sxs-lookup"><span data-stu-id="d2a7a-199">Repeat this event on the first Thursday or Friday of every month</span></span>

  ```json
    "pattern": {
      "type": "relativeMonthly",
      "interval": 1,
      "daysOfWeek": [ "Thursday", "Friday" ],
      "index": "first"
    }
  ```

### <a name="absolute-yearly"></a><span data-ttu-id="d2a7a-200">Anual absoluto</span><span class="sxs-lookup"><span data-stu-id="d2a7a-200">Absolute yearly</span></span>

<span data-ttu-id="d2a7a-201">El patrón anual absoluto hace que un evento se repita en el mismo mes y día (por ejemplo, 15 de abril), basándose en el número de años entre cada repetición.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-201">The absolute yearly pattern causes an event to repeat on the same month and day (for example, April 15), based on the number of years between each occurrence.</span></span>

#### <a name="relevant-properties"></a><span data-ttu-id="d2a7a-202">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="d2a7a-202">Relevant properties</span></span>

| <span data-ttu-id="d2a7a-203">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d2a7a-203">Property</span></span> | <span data-ttu-id="d2a7a-204">Relevancia</span><span class="sxs-lookup"><span data-stu-id="d2a7a-204">Relevance</span></span> | <span data-ttu-id="d2a7a-205">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2a7a-205">Description</span></span> |
|----------|-----------|-------------|
| <span data-ttu-id="d2a7a-206">**dayOfMonth**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-206">**dayOfMonth**</span></span> | <span data-ttu-id="d2a7a-207">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-207">Required</span></span> | <span data-ttu-id="d2a7a-208">Especifica el día del mes en que se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-208">Specifies on which day of the month the event occurs.</span></span> |
| <span data-ttu-id="d2a7a-209">**month**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-209">**month**</span></span> | <span data-ttu-id="d2a7a-210">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-210">Required</span></span> | <span data-ttu-id="d2a7a-211">Especifica en qué mes se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-211">Specifies in which month the event occurs.</span></span> |
| <span data-ttu-id="d2a7a-212">**interval**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-212">**interval**</span></span> | <span data-ttu-id="d2a7a-213">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-213">Required</span></span> | <span data-ttu-id="d2a7a-214">Especifica el número de años entre cada repetición.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-214">Specifies the number of years between each occurrence.</span></span> |
| <span data-ttu-id="d2a7a-215">**type**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-215">**type**</span></span> | <span data-ttu-id="d2a7a-216">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-216">Required</span></span> | <span data-ttu-id="d2a7a-217">Se debe establecer en `absoluteYearly`.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-217">Must be set to `absoluteYearly`.</span></span> |

#### <a name="example"></a><span data-ttu-id="d2a7a-218">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d2a7a-218">Example</span></span>

- <span data-ttu-id="d2a7a-219">Repetir este evento el 15 de abril de cada año</span><span class="sxs-lookup"><span data-stu-id="d2a7a-219">Repeat this event on April 15 every year</span></span>

  ```json
    "pattern": {
      "type": "absoluteYearly",
      "interval": 1,
      "dayOfMonth": 15,
      "month": 4
    }
  ```

### <a name="relative-yearly"></a><span data-ttu-id="d2a7a-220">Anual relativo</span><span class="sxs-lookup"><span data-stu-id="d2a7a-220">Relative yearly</span></span>

<span data-ttu-id="d2a7a-221">El patrón anual relativo hace que un evento se repita el mismo día de la semana en la misma posición relativa de un mes concreto, en función del número de años entre cada repetición.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-221">The relative yearly pattern causes an event to repeat on the same day of the week in the same relative position in a specific month, based on the number of years between each occurrence.</span></span> <span data-ttu-id="d2a7a-222">Por ejemplo, "cada último miércoles de noviembre".</span><span class="sxs-lookup"><span data-stu-id="d2a7a-222">For example, "every last Wednesday of November."</span></span>

#### <a name="relevant-properties"></a><span data-ttu-id="d2a7a-223">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="d2a7a-223">Relevant properties</span></span>

| <span data-ttu-id="d2a7a-224">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d2a7a-224">Property</span></span> | <span data-ttu-id="d2a7a-225">Relevancia</span><span class="sxs-lookup"><span data-stu-id="d2a7a-225">Relevance</span></span> | <span data-ttu-id="d2a7a-226">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2a7a-226">Description</span></span> |
|----------|-----------|-------------|
| <span data-ttu-id="d2a7a-227">**daysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-227">**daysOfWeek**</span></span> | <span data-ttu-id="d2a7a-228">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-228">Required</span></span> | <span data-ttu-id="d2a7a-229">Especifica en qué días de la semana puede producirse el evento.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-229">Specifies on which day(s) of the week the event can occur.</span></span> <span data-ttu-id="d2a7a-230">Los eventos anuales relativos sólo ocurren una vez al año, por lo que si especifica más de un valor, el evento tendrá lugar en el primer día que se ajuste al patrón.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-230">Relative yearly events only occur once per year, so if more than one value is specified, the event falls on the first day that satisfies the pattern.</span></span> |
| <span data-ttu-id="d2a7a-231">**index**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-231">**index**</span></span> | <span data-ttu-id="d2a7a-232">Opcional</span><span class="sxs-lookup"><span data-stu-id="d2a7a-232">Optional</span></span> | <span data-ttu-id="d2a7a-233">Especifica en qué instancia de los días permitidos especificados en **daysOfsWeek** se produce el evento, contados a partir de la primera instancia del mes.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-233">Specifies on which instance of the allowed days specified in **daysOfsWeek** the event occurs, counted from the first instance in the month.</span></span> <span data-ttu-id="d2a7a-234">Valores posibles: `first`, `second`, `third`, `fourth` y `last`.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-234">Possible values: `first`, `second`, `third`, `fourth`, and `last`.</span></span> <span data-ttu-id="d2a7a-235">Valor predeterminado: `first`.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-235">Default value: `first`.</span></span> |
| <span data-ttu-id="d2a7a-236">**month**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-236">**month**</span></span> | <span data-ttu-id="d2a7a-237">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-237">Required</span></span> | <span data-ttu-id="d2a7a-238">Especifica en qué mes se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-238">Specifies in which month the event occurs.</span></span> |
| <span data-ttu-id="d2a7a-239">**interval**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-239">**interval**</span></span> | <span data-ttu-id="d2a7a-240">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-240">Required</span></span> | <span data-ttu-id="d2a7a-241">Especifica el número de años entre cada repetición.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-241">Specifies the number of years between each occurrence.</span></span> |
| <span data-ttu-id="d2a7a-242">**type**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-242">**type**</span></span> | <span data-ttu-id="d2a7a-243">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-243">Required</span></span> | <span data-ttu-id="d2a7a-244">Se debe establecer en `relativeMonthly`.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-244">Must be set to `relativeMonthly`.</span></span> |

#### <a name="examples"></a><span data-ttu-id="d2a7a-245">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d2a7a-245">Examples</span></span>

- <span data-ttu-id="d2a7a-246">Repetir este evento el último miércoles de noviembre de cada año</span><span class="sxs-lookup"><span data-stu-id="d2a7a-246">Repeat this event on the last Wednesday of November every year</span></span>

  ```json
    "pattern": {
      "type": "relativeYearly",
      "interval": 1,
      "daysOfWeek": [ "Wednesday" ],
      "index": "last",
      "month": 11
    }
  ```

## <a name="recurrence-ranges"></a><span data-ttu-id="d2a7a-247">Intervalos de periodicidad</span><span class="sxs-lookup"><span data-stu-id="d2a7a-247">Recurrence ranges</span></span>

<span data-ttu-id="d2a7a-248">La segunda parte de una repetición es el rango.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-248">The second part of a recurrence is the range.</span></span> <span data-ttu-id="d2a7a-249">Especifica cuánto tiempo se repite el patrón.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-249">This specifies how long the pattern repeats.</span></span> <span data-ttu-id="d2a7a-250">Por ejemplo, un evento podría terminar después de 10 repeticiones, en una fecha específica, o podría no tener fin.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-250">For example, an event could end after 10 occurrences, by a specific date, or could have no end.</span></span> <span data-ttu-id="d2a7a-251">Un intervalo se representa en la API por el [recurso recurrenceRange](/graph/api/resources/recurrencepattern?view=graph-rest-1.0).</span><span class="sxs-lookup"><span data-stu-id="d2a7a-251">A range is represented in the API by the [recurrenceRange resource](/graph/api/resources/recurrencepattern?view=graph-rest-1.0).</span></span>

<span data-ttu-id="d2a7a-252">Según el tipo de intervalo, ciertos campos de **recurrenceRange** son obligatorios o ignorados.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-252">Depending on the type of range, certain fields of **recurrenceRange** are required or ignored.</span></span>

> <span data-ttu-id="d2a7a-253">**Nota**: Incluso si se omite un campo, también se valida.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-253">**Note**: Even if a field is ignored, it is still validated.</span></span> <span data-ttu-id="d2a7a-254">Si un campo tiene una lista determinada de valores posibles, utilizar un valor fuera del conjunto permitido provocará un error, incluso si ese campo se omite.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-254">If a field has a set list of possible values, using a value outside the allowed set causes an error, even if that field is ignored.</span></span>

<span data-ttu-id="d2a7a-255">Analicemos cada uno de los tipos de intervalo posibles.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-255">Let's take a look at each of the possible range types.</span></span>

### <a name="numbered-range"></a><span data-ttu-id="d2a7a-256">Rango numerado</span><span class="sxs-lookup"><span data-stu-id="d2a7a-256">Numbered range</span></span>

<span data-ttu-id="d2a7a-257">El rango numerado hace que un evento se produzca un número fijo de veces (según el modelo) desde la fecha de inicio.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-257">The numbered range causes an event to occur a fixed number of times (based on the pattern) from a start date.</span></span>

#### <a name="relevant-properties"></a><span data-ttu-id="d2a7a-258">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="d2a7a-258">Relevant properties</span></span>

| <span data-ttu-id="d2a7a-259">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d2a7a-259">Property</span></span> | <span data-ttu-id="d2a7a-260">Relevancia</span><span class="sxs-lookup"><span data-stu-id="d2a7a-260">Relevance</span></span> | <span data-ttu-id="d2a7a-261">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2a7a-261">Description</span></span> |
|----------|-----------|-------------|
| <span data-ttu-id="d2a7a-262">**numberOfOccurences**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-262">**numberOfOccurences**</span></span> | <span data-ttu-id="d2a7a-263">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-263">Required</span></span> | <span data-ttu-id="d2a7a-264">Especifica el número de repeticiones.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-264">Specifies the number of occurrences.</span></span> <span data-ttu-id="d2a7a-265">Debe ser un número entero positivo.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-265">Must be a positive integer.</span></span> |
| <span data-ttu-id="d2a7a-266">**recurrenceTimeZone**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-266">**recurrenceTimeZone**</span></span> | <span data-ttu-id="d2a7a-267">Opcional</span><span class="sxs-lookup"><span data-stu-id="d2a7a-267">Optional</span></span> | <span data-ttu-id="d2a7a-268">Especifica la zona horaria de la propiedad **startDate**.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-268">Specifies the time zone for the **startDate** property.</span></span> <span data-ttu-id="d2a7a-269">Si no se especifica, se usa la zona horaria del evento.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-269">If not specified, the time zone of the event is used.</span></span> |
| <span data-ttu-id="d2a7a-270">**startDate**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-270">**startDate**</span></span> | <span data-ttu-id="d2a7a-271">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-271">Required</span></span> | <span data-ttu-id="d2a7a-272">Especifica la fecha para comenzar a aplicar el patrón.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-272">Specifies the date to start applying the pattern.</span></span> <span data-ttu-id="d2a7a-273">El valor de **startDate** DEBE corresponderse con el valor de la fecha de la propiedad **start** en el [recurso de evento](/graph/api/resources/event?view=graph-rest-1.0).</span><span class="sxs-lookup"><span data-stu-id="d2a7a-273">The value of **startDate** MUST correspond to the date value of the **start** property on the [event resource](/graph/api/resources/event?view=graph-rest-1.0).</span></span> <span data-ttu-id="d2a7a-274">Tenga en cuenta que no puede producirse la primera aparición de la reunión en esta fecha si no encaja en el patrón.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-274">Note that the first occurrence of the meeting may not occur on this date if it does not fit the pattern.</span></span> |
| <span data-ttu-id="d2a7a-275">**type**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-275">**type**</span></span> | <span data-ttu-id="d2a7a-276">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-276">Required</span></span> | <span data-ttu-id="d2a7a-277">Se debe establecer en `numbered`.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-277">Must be set to `numbered`.</span></span> |

#### <a name="examples"></a><span data-ttu-id="d2a7a-278">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d2a7a-278">Examples</span></span>

- <span data-ttu-id="d2a7a-279">Repetir este evento 10 veces</span><span class="sxs-lookup"><span data-stu-id="d2a7a-279">Repeat this event 10 times</span></span>

  ```json
    "range": {
      "type": "numbered",
      "startDate": "2017-04-02",
      "numberOfOccurrences": 10
    }
  ```

### <a name="end-date-range"></a><span data-ttu-id="d2a7a-280">Intervalo de fecha de finalización</span><span class="sxs-lookup"><span data-stu-id="d2a7a-280">End date range</span></span>

<span data-ttu-id="d2a7a-281">El intervalo de fecha de finalización hace que un evento se repita todos los días que encajan en el patrón aplicable entre una fecha inicial y una fecha de finalización.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-281">The end date range causes an event to occur on all days that fit the applicable pattern between a start date and an end date.</span></span>

#### <a name="relevant-properties"></a><span data-ttu-id="d2a7a-282">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="d2a7a-282">Relevant properties</span></span>

| <span data-ttu-id="d2a7a-283">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d2a7a-283">Property</span></span> | <span data-ttu-id="d2a7a-284">Relevancia</span><span class="sxs-lookup"><span data-stu-id="d2a7a-284">Relevance</span></span> | <span data-ttu-id="d2a7a-285">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2a7a-285">Description</span></span> |
|----------|-----------|-------------|
| <span data-ttu-id="d2a7a-286">**endDate**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-286">**endDate**</span></span> | <span data-ttu-id="d2a7a-287">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-287">Required</span></span> | <span data-ttu-id="d2a7a-288">Especifica la fecha para dejar de aplicar el patrón.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-288">Specifies the date to stop applying the pattern.</span></span> <span data-ttu-id="d2a7a-289">Tenga en cuenta que no puede producirse la última aparición de la reunión en esta fecha si no encaja en el patrón.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-289">Note that the last occurrence of the meeting may not occur on this date if it does not fit the pattern.</span></span> |
| <span data-ttu-id="d2a7a-290">**recurrenceTimeZone**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-290">**recurrenceTimeZone**</span></span> | <span data-ttu-id="d2a7a-291">Opcional</span><span class="sxs-lookup"><span data-stu-id="d2a7a-291">Optional</span></span> | <span data-ttu-id="d2a7a-292">Especifica la zona horaria de las propiedades **startDate** y **endDate**.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-292">Specifies the time zone for the **startDate** and **endDate** properties.</span></span> <span data-ttu-id="d2a7a-293">Si no se especifica, se usa la zona horaria del evento.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-293">If not specified, the time zone of the event is used.</span></span> |
| <span data-ttu-id="d2a7a-294">**startDate**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-294">**startDate**</span></span> | <span data-ttu-id="d2a7a-295">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-295">Required</span></span> | <span data-ttu-id="d2a7a-296">Especifica la fecha para comenzar a aplicar el patrón.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-296">Specifies the date to start applying the pattern.</span></span> <span data-ttu-id="d2a7a-297">El valor de **startDate** DEBE corresponderse con el valor de la fecha de la propiedad **start** en el [recurso de evento](/graph/api/resources/event?view=graph-rest-1.0).</span><span class="sxs-lookup"><span data-stu-id="d2a7a-297">The value of **startDate** MUST correspond to the date value of the **start** property on the [event resource](/graph/api/resources/event?view=graph-rest-1.0).</span></span> <span data-ttu-id="d2a7a-298">Tenga en cuenta que no puede producirse la primera aparición de la reunión en esta fecha si no encaja en el patrón.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-298">Note that the first occurrence of the meeting may not occur on this date if it does not fit the pattern.</span></span> |
| <span data-ttu-id="d2a7a-299">**type**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-299">**type**</span></span> | <span data-ttu-id="d2a7a-300">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-300">Required</span></span> | <span data-ttu-id="d2a7a-301">Se debe establecer en **endDate**.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-301">Must be set to **endDate**.</span></span> |

#### <a name="examples"></a><span data-ttu-id="d2a7a-302">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d2a7a-302">Examples</span></span>

- <span data-ttu-id="d2a7a-303">Repetir este evento desde el 1 de julio de 2017 hasta el 31 de julio de 2017</span><span class="sxs-lookup"><span data-stu-id="d2a7a-303">Repeat this event from July 1, 2017, to July 31, 2017</span></span>

  ```json
    "range": {
      "type": "endDate",
      "startDate": "2017-07-01",
      "endDate": "2017-07-31"
    }
  ```

### <a name="no-end-range"></a><span data-ttu-id="d2a7a-304">Sin fecha de finalización</span><span class="sxs-lookup"><span data-stu-id="d2a7a-304">No end range</span></span>

<span data-ttu-id="d2a7a-305">Sin fecha de finalización hace que un evento se repita todos los días que encajen en el patrón aplicable después de una fecha de inicio.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-305">The no end range causes an event to occur on all days that fit the applicable pattern after a start date.</span></span>

#### <a name="relevant-properties"></a><span data-ttu-id="d2a7a-306">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="d2a7a-306">Relevant properties</span></span>

| <span data-ttu-id="d2a7a-307">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d2a7a-307">Property</span></span> | <span data-ttu-id="d2a7a-308">Relevancia</span><span class="sxs-lookup"><span data-stu-id="d2a7a-308">Relevance</span></span> | <span data-ttu-id="d2a7a-309">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2a7a-309">Description</span></span> |
|----------|-----------|-------------|
| <span data-ttu-id="d2a7a-310">**recurrenceTimeZone**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-310">**recurrenceTimeZone**</span></span> | <span data-ttu-id="d2a7a-311">Opcional</span><span class="sxs-lookup"><span data-stu-id="d2a7a-311">Optional</span></span> | <span data-ttu-id="d2a7a-312">Especifica la zona horaria de la propiedad **startDate**.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-312">Specifies the time zone for the **startDate** property.</span></span> <span data-ttu-id="d2a7a-313">Si no se especifica, se usa la zona horaria del evento.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-313">If not specified, the time zone of the event is used.</span></span> |
| <span data-ttu-id="d2a7a-314">**startDate**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-314">**startDate**</span></span> | <span data-ttu-id="d2a7a-315">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-315">Required</span></span> | <span data-ttu-id="d2a7a-316">Especifica la fecha para comenzar a aplicar el patrón.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-316">Specifies the date to start applying the pattern.</span></span> <span data-ttu-id="d2a7a-317">El valor de **startDate** DEBE corresponderse con el valor de la fecha de la propiedad **start** en el [recurso de evento](/graph/api/resources/event?view=graph-rest-1.0).</span><span class="sxs-lookup"><span data-stu-id="d2a7a-317">The value of **startDate** MUST correspond to the date value of the **start** property on the [event resource](/graph/api/resources/event?view=graph-rest-1.0).</span></span> <span data-ttu-id="d2a7a-318">Tenga en cuenta que no puede producirse la primera aparición de la reunión en esta fecha si no encaja en el patrón.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-318">Note that the first occurrence of the meeting may not occur on this date if it does not fit the pattern.</span></span> |
| <span data-ttu-id="d2a7a-319">**type**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-319">**type**</span></span> | <span data-ttu-id="d2a7a-320">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d2a7a-320">Required</span></span> | <span data-ttu-id="d2a7a-321">Se debe establecer en `noEnd`.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-321">Must be set to `noEnd`.</span></span> |

#### <a name="examples"></a><span data-ttu-id="d2a7a-322">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d2a7a-322">Examples</span></span>

- <span data-ttu-id="d2a7a-323">Repetir este evento desde 15 de mayo de 2017 para siempre</span><span class="sxs-lookup"><span data-stu-id="d2a7a-323">Repeat this event from May 15, 2017, forever</span></span>

  ```json
    "range": {
      "type": "noEnd",
      "startDate": "2017-05-15"
    }
  ```

## <a name="using-patterns-and-ranges-to-create-recurring-events"></a><span data-ttu-id="d2a7a-324">Usar patrones y rangos para crear eventos periódicos</span><span class="sxs-lookup"><span data-stu-id="d2a7a-324">Using patterns and ranges to create recurring events</span></span>

<span data-ttu-id="d2a7a-325">Ahora que hemos visto los patrones y rangos por separado, analicemos cómo funcionan e interactúan con las propiedades **start** y **end** en el evento.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-325">Now that we've looked at patterns and ranges separately, let's look at how they work together and how they interact with the **start** and **end** properties on the event.</span></span>

### <a name="creating-a-recurrence-rule"></a><span data-ttu-id="d2a7a-326">Crear una regla de periodicidad</span><span class="sxs-lookup"><span data-stu-id="d2a7a-326">Creating a recurrence rule</span></span>

<span data-ttu-id="d2a7a-327">Para crear una regla de periodicidad, debe especificar tanto un patrón como un rango.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-327">To create a recurrence rule, you must specify both a pattern and a range.</span></span> <span data-ttu-id="d2a7a-328">Cualquier tipo de patrón puede funcionar con cualquier tipo de rango.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-328">Any pattern type can work with any range type.</span></span> <span data-ttu-id="d2a7a-329">A continuación, se muestran algunos ejemplos.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-329">Here are a few examples.</span></span>

#### <a name="examples"></a><span data-ttu-id="d2a7a-330">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d2a7a-330">Examples</span></span>

- <span data-ttu-id="d2a7a-331">**Reunión de 13:00 a 13:30 todos los lunes a partir del 4 de septiembre de 2017 hasta el final del año**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-331">**Meet from 1:00 PM to 1:30 PM every Monday starting September 4, 2017, until the end of the year**</span></span>

  - <span data-ttu-id="d2a7a-332">El requisito "cada lunes" se cumple fácilmente por el tipo de patrón de periodicidad `weekly`.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-332">The "every Monday" requirement is easily met by the `weekly` recurrence pattern type.</span></span>
  - <span data-ttu-id="d2a7a-333">El requisito "hasta el final del año" indica un tipo de intervalo de repetición `endDate`.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-333">The "until the end of the year" requirement indicates an `endDate` recurrence range type.</span></span>

  ```json
    "recurrence": {
      "pattern": {
        "type": "weekly",
        "interval": 1,
        "daysOfWeek": [ "Monday" ]
      },
      "range": {
        "type": "endDate",
        "startDate": "2017-09-04",
        "endDate": "2017-12-31"
      }
    }
  ```

  <span data-ttu-id="d2a7a-334">Dado que el 31 de diciembre de 2017 es domingo, la última aparición en esta serie será el lunes 25 de diciembre.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-334">Because December 31, 2017, is on a Sunday, the last occurrence in this series will be on Monday, December 25.</span></span>

- <span data-ttu-id="d2a7a-335">**Reunión de 14:00 a 15:00 el primer jueves de meses alternos a partir del 29 de agosto de 2017**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-335">**Meet from 2:00 PM to 3:00 PM on the first Thursday of every other month starting August 29, 2017**</span></span>

  - <span data-ttu-id="d2a7a-336">El requisito "primer jueves de meses alternos" se consigue estableciendo un patrón mensual relativo.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-336">The "first Thursday of every other month" requirement is achievable by using a relative monthly pattern.</span></span> <span data-ttu-id="d2a7a-337">La parte "de meses alternos" indica que **interval** debe establecerse en `2`.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-337">The "every other month" portion indicates that the **interval** should be set to `2`.</span></span>
  - <span data-ttu-id="d2a7a-338">Dado que no hay ningún requisito de fecha de finalización, puede usarse un tipo de rango `noEnd`.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-338">Because there is no requirement on an end date, a `noEnd` range type can be used.</span></span>

  ```json
    "recurrence": {
      "pattern": {
        "type": "relativeMonthly",
        "interval": 2,
        "daysOfWeek": [ "Thursday" ],
        "index": "first"
      },
      "range": {
        "type": "noEnd",
        "startDate": "2017-08-29"
      }
    }
  ```

  <span data-ttu-id="d2a7a-339">Dado que el valor de **startDate** comienza tras el primer jueves de agosto, la primera aparición de esta serie será en septiembre.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-339">Because the value of **startDate** is after the first Thursday in August, the first occurrence of this series will be in September.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d2a7a-340">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="d2a7a-340">Next steps</span></span>
    
<span data-ttu-id="d2a7a-341">Obtenga más información sobre la [integración con el Calendario de Outlook](outlook-calendar-concept-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d2a7a-341">Find out more about [integrating with Outlook calendar](outlook-calendar-concept-overview.md).</span></span>
