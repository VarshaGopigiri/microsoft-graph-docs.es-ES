# <a name="schedule-repeating-appointments-as-recurring-events-in-outlook"></a><span data-ttu-id="06325-101">Programar citas repetidas como eventos periódicos en Outlook</span><span class="sxs-lookup"><span data-stu-id="06325-101">Schedule repeating appointments as recurring events in Outlook</span></span>

<span data-ttu-id="06325-102">Los eventos periódicos son una parte importante del Calendario de Outlook.</span><span class="sxs-lookup"><span data-stu-id="06325-102">Recurring events are an important part of Outlook calendaring.</span></span> <span data-ttu-id="06325-103">Ya sea una reunión semanal personal con su jefe o una reunión de revisión de todo un departamento que tiene lugar el segundo martes de cada mes, los eventos periódicos facilitan la tarea al crear el evento una sola vez y que el servidor complete el resto de la serie.</span><span class="sxs-lookup"><span data-stu-id="06325-103">Whether it's a weekly one-on-one meeting with your manager, or a division-wide review meeting that happens on the second Tuesday of each month, recurring events make it easy to create the event once, and let the server fill in the rest of the series.</span></span>

<span data-ttu-id="06325-104">La clave de información que permite a los eventos periódicos "expandirse" en las repeticiones periódicas individuales es la regla de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="06325-104">The key bit of information that allows recurring events to "expand" into individual occurrences is the recurrence rule.</span></span> <span data-ttu-id="06325-105">La regla especifica con qué frecuencia se repite un evento y durante cuánto tiempo.</span><span class="sxs-lookup"><span data-stu-id="06325-105">The rule specifies both how often an event repeats, and for how long.</span></span> <span data-ttu-id="06325-106">Las API de REST de Outlook definen las reglas de periodicidad en la propiedad **recurrence** del [recurso de evento](../api-reference/v1.0/resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="06325-106">The Outlook REST APIs model recurrence rules in the **recurrence** property of the [event resource](../api-reference/v1.0/resources/event.md).</span></span> 

<span data-ttu-id="06325-107">Cada recurrencia se compone de dos partes: el patrón de periodicidad (la frecuencia) y el intervalo de periodicidad (la duración).</span><span class="sxs-lookup"><span data-stu-id="06325-107">Each recurrence is made up of two parts: the recurrence pattern (how often), and the recurrence range (for how long).</span></span>

## <a name="recurrence-patterns"></a><span data-ttu-id="06325-108">Patrones de periodicidad</span><span class="sxs-lookup"><span data-stu-id="06325-108">Recurrence patterns</span></span>

<span data-ttu-id="06325-109">La primera parte de una repetición es el patrón.</span><span class="sxs-lookup"><span data-stu-id="06325-109">The first part of a recurrence is the pattern.</span></span> <span data-ttu-id="06325-110">Especifica la frecuencia con que se repite el evento.</span><span class="sxs-lookup"><span data-stu-id="06325-110">This specifies how often the event repeats.</span></span> <span data-ttu-id="06325-111">Por ejemplo, un evento podría repetirse "cada 3 días", "todos los jueves" o "el 22 de julio de cada año".</span><span class="sxs-lookup"><span data-stu-id="06325-111">For example, an event could repeat "every 3 days," "every Thursday," or "on July 22 every year."</span></span> <span data-ttu-id="06325-112">Un patrón se representa en la API con el [recurso recurrencePattern](../api-reference/v1.0/resources/recurrencepattern.md).</span><span class="sxs-lookup"><span data-stu-id="06325-112">A pattern is represented in the API by the [recurrencePattern resource](../api-reference/v1.0/resources/recurrencepattern.md).</span></span>

<span data-ttu-id="06325-113">Según el tipo de patrón, ciertos campos de **recurrencePattern** son obligatorios, opcionales u omitidos.</span><span class="sxs-lookup"><span data-stu-id="06325-113">Depending on the type of pattern, certain fields of the **recurrencePattern** are required, optional, or ignored.</span></span>

> <span data-ttu-id="06325-114">**Nota**: Incluso si se omite un campo, también se valida.</span><span class="sxs-lookup"><span data-stu-id="06325-114">**Note**: Even if a field is ignored, it is still validated.</span></span> <span data-ttu-id="06325-115">Si un campo tiene una lista determinada de valores posibles, utilizar un valor fuera del conjunto permitido provocará un error, incluso si ese campo se omite.</span><span class="sxs-lookup"><span data-stu-id="06325-115">If a field has a set list of possible values, using a value outside the allowed set causes an error, even if that field is ignored.</span></span>

<span data-ttu-id="06325-116">Analicemos cada uno de los tipos de patrones posibles.</span><span class="sxs-lookup"><span data-stu-id="06325-116">Let's take a look at each of the possible pattern types.</span></span>

### <a name="daily"></a><span data-ttu-id="06325-117">Diario</span><span class="sxs-lookup"><span data-stu-id="06325-117">Daily</span></span>

<span data-ttu-id="06325-118">El patrón de periodicidad diario hace que se repita basándose en el número de días que transcurre entre cada evento.</span><span class="sxs-lookup"><span data-stu-id="06325-118">The daily recurrence pattern causes an event to repeat based on a number of days between each occurrence.</span></span>

#### <a name="relevant-properties"></a><span data-ttu-id="06325-119">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="06325-119">Relevant properties</span></span>

| <span data-ttu-id="06325-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="06325-120">Property</span></span> | <span data-ttu-id="06325-121">Relevancia</span><span class="sxs-lookup"><span data-stu-id="06325-121">Relevance</span></span> | <span data-ttu-id="06325-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="06325-122">Description</span></span> |
|----------|-----------|-------------|
| <span data-ttu-id="06325-123">**interval**</span><span class="sxs-lookup"><span data-stu-id="06325-123">**interval**</span></span> | <span data-ttu-id="06325-124">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-124">Required</span></span> | <span data-ttu-id="06325-125">Especifica el número de días entre cada repetición.</span><span class="sxs-lookup"><span data-stu-id="06325-125">Specifies the number of days between each occurrence.</span></span> |
| <span data-ttu-id="06325-126">**type**</span><span class="sxs-lookup"><span data-stu-id="06325-126">**type**</span></span> | <span data-ttu-id="06325-127">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-127">Required</span></span> | <span data-ttu-id="06325-128">Se debe establecer en `daily`.</span><span class="sxs-lookup"><span data-stu-id="06325-128">Must be set to `daily`.</span></span> |

#### <a name="examples"></a><span data-ttu-id="06325-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="06325-129">Examples</span></span>

- <span data-ttu-id="06325-130">Repetir este evento cada día</span><span class="sxs-lookup"><span data-stu-id="06325-130">Repeat this event every day</span></span>

  ```json
    "pattern": {
      "type": "daily",
      "interval": 1
    }
  ```
- <span data-ttu-id="06325-131">Repetir este evento cada tres días</span><span class="sxs-lookup"><span data-stu-id="06325-131">Repeat this event every three days</span></span>

  ```json
    "pattern": {
      "type": "daily",
      "interval": 3
    }
  ```

### <a name="weekly"></a><span data-ttu-id="06325-132">Semanal</span><span class="sxs-lookup"><span data-stu-id="06325-132">Weekly</span></span>

<span data-ttu-id="06325-133">El patrón de periodicidad semanal provoca que un evento se repita en el mismo día o días de la semana, en función del número de semanas que transcurren entre cada conjunto de eventos.</span><span class="sxs-lookup"><span data-stu-id="06325-133">The weekly recurrence pattern causes an event to repeat on the same day or days of the week, based on the number of weeks between each set of occurrences.</span></span>

#### <a name="relevant-properties"></a><span data-ttu-id="06325-134">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="06325-134">Relevant properties</span></span>

| <span data-ttu-id="06325-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="06325-135">Property</span></span> | <span data-ttu-id="06325-136">Relevancia</span><span class="sxs-lookup"><span data-stu-id="06325-136">Relevance</span></span> | <span data-ttu-id="06325-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="06325-137">Description</span></span> |
|----------|-----------|-------------|
| <span data-ttu-id="06325-138">**daysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="06325-138">**daysOfWeek**</span></span> | <span data-ttu-id="06325-139">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-139">Required</span></span> | <span data-ttu-id="06325-140">Especifica en qué días de la semana se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="06325-140">Specifies on which day(s) of the week the event occurs.</span></span> |
| <span data-ttu-id="06325-141">**firstDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="06325-141">**firstDayOfWeek**</span></span> | <span data-ttu-id="06325-142">Opcional</span><span class="sxs-lookup"><span data-stu-id="06325-142">Optional</span></span> | <span data-ttu-id="06325-143">Especifica qué día se considera el primer día de la semana.</span><span class="sxs-lookup"><span data-stu-id="06325-143">Specifies which day is considered the first day of the week.</span></span> <span data-ttu-id="06325-144">Valor predeterminado: `Sunday`.</span><span class="sxs-lookup"><span data-stu-id="06325-144">Default value: `Sunday`.</span></span> |
| <span data-ttu-id="06325-145">**interval**</span><span class="sxs-lookup"><span data-stu-id="06325-145">**interval**</span></span> | <span data-ttu-id="06325-146">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-146">Required</span></span> | <span data-ttu-id="06325-147">Especifica el número de semanas entre cada conjunto de eventos.</span><span class="sxs-lookup"><span data-stu-id="06325-147">Specifies the number of weeks between each set of occurrences.</span></span> |
| <span data-ttu-id="06325-148">**type**</span><span class="sxs-lookup"><span data-stu-id="06325-148">**type**</span></span> | <span data-ttu-id="06325-149">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-149">Required</span></span> | <span data-ttu-id="06325-150">Se debe establecer en `weekly`.</span><span class="sxs-lookup"><span data-stu-id="06325-150">Must be set to `weekly`.</span></span> |

#### <a name="examples"></a><span data-ttu-id="06325-151">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="06325-151">Examples</span></span>

- <span data-ttu-id="06325-152">Repetir este evento cada jueves</span><span class="sxs-lookup"><span data-stu-id="06325-152">Repeat this event every Thursday</span></span>

  ```json
    "pattern": {
      "type": "weekly",
      "interval": 1,
      "daysOfWeek": [ "Thursday" ]
    }
  ```
- <span data-ttu-id="06325-153">Repetir este evento lunes y martes cada dos semanas</span><span class="sxs-lookup"><span data-stu-id="06325-153">Repeat this event every other Monday and Tuesday</span></span>

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

### <a name="absolute-monthly"></a><span data-ttu-id="06325-154">Mensual absoluto</span><span class="sxs-lookup"><span data-stu-id="06325-154">Absolute monthly</span></span>

<span data-ttu-id="06325-155">El patrón mensual absoluto hace que un evento se repita el mismo día del mes (por ejemplo, el día 15), en función del número de meses entre cada repetición.</span><span class="sxs-lookup"><span data-stu-id="06325-155">The absolute monthly pattern causes an event to repeat on the same day of the month (for example, the 15th), based on the number of months between each occurrence.</span></span>

#### <a name="relevant-properties"></a><span data-ttu-id="06325-156">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="06325-156">Relevant properties</span></span>

| <span data-ttu-id="06325-157">Propiedad</span><span class="sxs-lookup"><span data-stu-id="06325-157">Property</span></span> | <span data-ttu-id="06325-158">Relevancia</span><span class="sxs-lookup"><span data-stu-id="06325-158">Relevance</span></span> | <span data-ttu-id="06325-159">Descripción</span><span class="sxs-lookup"><span data-stu-id="06325-159">Description</span></span> |
|----------|-----------|-------------|
| <span data-ttu-id="06325-160">**dayOfMonth**</span><span class="sxs-lookup"><span data-stu-id="06325-160">**dayOfMonth**</span></span> | <span data-ttu-id="06325-161">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-161">Required</span></span> | <span data-ttu-id="06325-162">Especifica el día del mes en que se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="06325-162">Specifies on which day of the month the event occurs.</span></span> |
| <span data-ttu-id="06325-163">**interval**</span><span class="sxs-lookup"><span data-stu-id="06325-163">**interval**</span></span> | <span data-ttu-id="06325-164">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-164">Required</span></span> | <span data-ttu-id="06325-165">Especifica el número de meses entre cada repetición.</span><span class="sxs-lookup"><span data-stu-id="06325-165">Specifies the number of months between each occurrence.</span></span> |
| <span data-ttu-id="06325-166">**type**</span><span class="sxs-lookup"><span data-stu-id="06325-166">**type**</span></span> | <span data-ttu-id="06325-167">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-167">Required</span></span> | <span data-ttu-id="06325-168">Se debe establecer en `absoluteMonthly`.</span><span class="sxs-lookup"><span data-stu-id="06325-168">Must be set to `absoluteMonthly`.</span></span> |

#### <a name="examples"></a><span data-ttu-id="06325-169">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="06325-169">Examples</span></span>

- <span data-ttu-id="06325-170">Repetir este evento el día 15 de cada mes</span><span class="sxs-lookup"><span data-stu-id="06325-170">Repeat this event on the 15th of every month</span></span>

  ```json
    "pattern": {
      "type": "absoluteMonthly",
      "interval": 1,
      "dayOfMonth": 15
    }
  ```
- <span data-ttu-id="06325-171">Repetir este evento trimestralmente (cada 3 meses) el día 7</span><span class="sxs-lookup"><span data-stu-id="06325-171">Repeat this event quarterly (every 3 months) on the 7th</span></span>

  ```json
    "pattern": {
      "type": "absoluteMonthly",
      "interval": 3,
      "dayOfMonth": 7
    }
  ```

### <a name="relative-monthly"></a><span data-ttu-id="06325-172">Mensual relativo</span><span class="sxs-lookup"><span data-stu-id="06325-172">Relative monthly</span></span>

<span data-ttu-id="06325-173">El patrón mensual relativo hace que un evento se repita el mismo día de la semana en la misma posición relativa en el mes, en función del número de meses entre cada repetición.</span><span class="sxs-lookup"><span data-stu-id="06325-173">The relative monthly pattern causes an event to repeat on the same day of the week in the same relative position in the month, based on the number of months between each occurrence.</span></span> <span data-ttu-id="06325-174">Por ejemplo, "cada segundo miércoles del mes".</span><span class="sxs-lookup"><span data-stu-id="06325-174">For example, "every second Wednesday of the month."</span></span>

#### <a name="relevant-properties"></a><span data-ttu-id="06325-175">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="06325-175">Relevant properties</span></span>

| <span data-ttu-id="06325-176">Propiedad</span><span class="sxs-lookup"><span data-stu-id="06325-176">Property</span></span> | <span data-ttu-id="06325-177">Relevancia</span><span class="sxs-lookup"><span data-stu-id="06325-177">Relevance</span></span> | <span data-ttu-id="06325-178">Descripción</span><span class="sxs-lookup"><span data-stu-id="06325-178">Description</span></span> |
|----------|-----------|-------------|
| <span data-ttu-id="06325-179">**daysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="06325-179">**daysOfWeek**</span></span> | <span data-ttu-id="06325-180">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-180">Required</span></span> | <span data-ttu-id="06325-181">Especifica en qué días de la semana puede producirse el evento.</span><span class="sxs-lookup"><span data-stu-id="06325-181">Specifies on which day(s) of the week the event can occur.</span></span> <span data-ttu-id="06325-182">Los eventos mensuales relativos sólo ocurren una vez al mes, por lo que si especifica más de un valor, el evento tendrá lugar en el primer día que se ajuste al patrón.</span><span class="sxs-lookup"><span data-stu-id="06325-182">Relative monthly events only occur once per month, so if more than one value is specified, the event falls on the first day that satisfies the pattern.</span></span> |
| <span data-ttu-id="06325-183">**index**</span><span class="sxs-lookup"><span data-stu-id="06325-183">**index**</span></span> | <span data-ttu-id="06325-184">Opcional</span><span class="sxs-lookup"><span data-stu-id="06325-184">Optional</span></span> | <span data-ttu-id="06325-185">Especifica en qué instancia de los días permitidos especificados en **daysOfsWeek** se produce el evento, contados a partir de la primera instancia del mes.</span><span class="sxs-lookup"><span data-stu-id="06325-185">Specifies on which instance of the allowed days specified in **daysOfsWeek** the event occurs, counted from the first instance in the month.</span></span> <span data-ttu-id="06325-186">Valores posibles: `first`, `second`, `third`, `fourth` y `last`.</span><span class="sxs-lookup"><span data-stu-id="06325-186">Possible values: `first`, `second`, `third`, `fourth`, and `last`.</span></span> <span data-ttu-id="06325-187">Valor predeterminado: `first`.</span><span class="sxs-lookup"><span data-stu-id="06325-187">Default value: `first`.</span></span> |
| <span data-ttu-id="06325-188">**interval**</span><span class="sxs-lookup"><span data-stu-id="06325-188">**interval**</span></span> | <span data-ttu-id="06325-189">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-189">Required</span></span> | <span data-ttu-id="06325-190">Especifica el número de meses entre cada repetición.</span><span class="sxs-lookup"><span data-stu-id="06325-190">Specifies the number of months between each occurrence.</span></span> |
| <span data-ttu-id="06325-191">**type**</span><span class="sxs-lookup"><span data-stu-id="06325-191">**type**</span></span> | <span data-ttu-id="06325-192">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-192">Required</span></span> | <span data-ttu-id="06325-193">Se debe establecer en `relativeMonthly`.</span><span class="sxs-lookup"><span data-stu-id="06325-193">Must be set to `relativeMonthly`.</span></span> |

#### <a name="examples"></a><span data-ttu-id="06325-194">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="06325-194">Examples</span></span>

- <span data-ttu-id="06325-195">Repetir este evento el segundo miércoles de cada mes</span><span class="sxs-lookup"><span data-stu-id="06325-195">Repeat this event on the second Wednesday of every month</span></span>

  ```json
    "pattern": {
      "type": "relativeMonthly",
      "interval": 1,
      "daysOfWeek": [ "Wednesday" ],
      "index": "second"
    }
  ```
- <span data-ttu-id="06325-196">Repetir este evento en el primer jueves o viernes de cada mes</span><span class="sxs-lookup"><span data-stu-id="06325-196">Repeat this event on the first Thursday or Friday of every month</span></span>

  ```json
    "pattern": {
      "type": "relativeMonthly",
      "interval": 1,
      "daysOfWeek": [ "Thursday", "Friday" ],
      "index": "first"
    }
  ```

### <a name="absolute-yearly"></a><span data-ttu-id="06325-197">Anual absoluto</span><span class="sxs-lookup"><span data-stu-id="06325-197">Absolute yearly</span></span>

<span data-ttu-id="06325-198">El patrón anual absoluto hace que un evento se repita en el mismo mes y día (por ejemplo, 15 de abril), basándose en el número de años entre cada repetición.</span><span class="sxs-lookup"><span data-stu-id="06325-198">The absolute yearly pattern causes an event to repeat on the same month and day (for example, April 15), based on the number of years between each occurrence.</span></span>

#### <a name="relevant-properties"></a><span data-ttu-id="06325-199">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="06325-199">Relevant properties</span></span>

| <span data-ttu-id="06325-200">Propiedad</span><span class="sxs-lookup"><span data-stu-id="06325-200">Property</span></span> | <span data-ttu-id="06325-201">Relevancia</span><span class="sxs-lookup"><span data-stu-id="06325-201">Relevance</span></span> | <span data-ttu-id="06325-202">Descripción</span><span class="sxs-lookup"><span data-stu-id="06325-202">Description</span></span> |
|----------|-----------|-------------|
| <span data-ttu-id="06325-203">**dayOfMonth**</span><span class="sxs-lookup"><span data-stu-id="06325-203">**dayOfMonth**</span></span> | <span data-ttu-id="06325-204">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-204">Required</span></span> | <span data-ttu-id="06325-205">Especifica el día del mes en que se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="06325-205">Specifies on which day of the month the event occurs.</span></span> |
| <span data-ttu-id="06325-206">**month**</span><span class="sxs-lookup"><span data-stu-id="06325-206">**month**</span></span> | <span data-ttu-id="06325-207">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-207">Required</span></span> | <span data-ttu-id="06325-208">Especifica en qué mes se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="06325-208">Specifies in which month the event occurs.</span></span> |
| <span data-ttu-id="06325-209">**interval**</span><span class="sxs-lookup"><span data-stu-id="06325-209">**interval**</span></span> | <span data-ttu-id="06325-210">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-210">Required</span></span> | <span data-ttu-id="06325-211">Especifica el número de años entre cada repetición.</span><span class="sxs-lookup"><span data-stu-id="06325-211">Specifies the number of years between each occurrence.</span></span> |
| <span data-ttu-id="06325-212">**type**</span><span class="sxs-lookup"><span data-stu-id="06325-212">**type**</span></span> | <span data-ttu-id="06325-213">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-213">Required</span></span> | <span data-ttu-id="06325-214">Se debe establecer en `absoluteYearly`.</span><span class="sxs-lookup"><span data-stu-id="06325-214">Must be set to `absoluteYearly`.</span></span> |

#### <a name="example"></a><span data-ttu-id="06325-215">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="06325-215">Example</span></span>

- <span data-ttu-id="06325-216">Repetir este evento el 15 de abril de cada año</span><span class="sxs-lookup"><span data-stu-id="06325-216">Repeat this event on April 15 every year</span></span>

  ```json
    "pattern": {
      "type": "absoluteYearly",
      "interval": 1,
      "dayOfMonth": 15,
      "month": 4
    }
  ```

### <a name="relative-yearly"></a><span data-ttu-id="06325-217">Anual relativo</span><span class="sxs-lookup"><span data-stu-id="06325-217">Relative yearly</span></span>

<span data-ttu-id="06325-218">El patrón anual relativo hace que un evento se repita el mismo día de la semana en la misma posición relativa de un mes concreto, en función del número de años entre cada repetición.</span><span class="sxs-lookup"><span data-stu-id="06325-218">The relative yearly pattern causes an event to repeat on the same day of the week in the same relative position in a specific month, based on the number of years between each occurrence.</span></span> <span data-ttu-id="06325-219">Por ejemplo, "cada último miércoles de noviembre".</span><span class="sxs-lookup"><span data-stu-id="06325-219">For example, "every last Wednesday of November."</span></span>

#### <a name="relevant-properties"></a><span data-ttu-id="06325-220">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="06325-220">Relevant properties</span></span>

| <span data-ttu-id="06325-221">Propiedad</span><span class="sxs-lookup"><span data-stu-id="06325-221">Property</span></span> | <span data-ttu-id="06325-222">Relevancia</span><span class="sxs-lookup"><span data-stu-id="06325-222">Relevance</span></span> | <span data-ttu-id="06325-223">Descripción</span><span class="sxs-lookup"><span data-stu-id="06325-223">Description</span></span> |
|----------|-----------|-------------|
| <span data-ttu-id="06325-224">**daysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="06325-224">**daysOfWeek**</span></span> | <span data-ttu-id="06325-225">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-225">Required</span></span> | <span data-ttu-id="06325-226">Especifica en qué días de la semana puede producirse el evento.</span><span class="sxs-lookup"><span data-stu-id="06325-226">Specifies on which day(s) of the week the event can occur.</span></span> <span data-ttu-id="06325-227">Los eventos anuales relativos sólo ocurren una vez al año, por lo que si especifica más de un valor, el evento tendrá lugar en el primer día que se ajuste al patrón.</span><span class="sxs-lookup"><span data-stu-id="06325-227">Relative yearly events only occur once per year, so if more than one value is specified, the event falls on the first day that satisfies the pattern.</span></span> |
| <span data-ttu-id="06325-228">**index**</span><span class="sxs-lookup"><span data-stu-id="06325-228">**index**</span></span> | <span data-ttu-id="06325-229">Opcional</span><span class="sxs-lookup"><span data-stu-id="06325-229">Optional</span></span> | <span data-ttu-id="06325-230">Especifica en qué instancia de los días permitidos especificados en **daysOfsWeek** se produce el evento, contados a partir de la primera instancia del mes.</span><span class="sxs-lookup"><span data-stu-id="06325-230">Specifies on which instance of the allowed days specified in **daysOfsWeek** the event occurs, counted from the first instance in the month.</span></span> <span data-ttu-id="06325-231">Valores posibles: `first`, `second`, `third`, `fourth` y `last`.</span><span class="sxs-lookup"><span data-stu-id="06325-231">Possible values: `first`, `second`, `third`, `fourth`, and `last`.</span></span> <span data-ttu-id="06325-232">Valor predeterminado: `first`.</span><span class="sxs-lookup"><span data-stu-id="06325-232">Default value: `first`.</span></span> |
| <span data-ttu-id="06325-233">**month**</span><span class="sxs-lookup"><span data-stu-id="06325-233">**month**</span></span> | <span data-ttu-id="06325-234">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-234">Required</span></span> | <span data-ttu-id="06325-235">Especifica en qué mes se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="06325-235">Specifies in which month the event occurs.</span></span> |
| <span data-ttu-id="06325-236">**interval**</span><span class="sxs-lookup"><span data-stu-id="06325-236">**interval**</span></span> | <span data-ttu-id="06325-237">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-237">Required</span></span> | <span data-ttu-id="06325-238">Especifica el número de años entre cada repetición.</span><span class="sxs-lookup"><span data-stu-id="06325-238">Specifies the number of years between each occurrence.</span></span> |
| <span data-ttu-id="06325-239">**type**</span><span class="sxs-lookup"><span data-stu-id="06325-239">**type**</span></span> | <span data-ttu-id="06325-240">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-240">Required</span></span> | <span data-ttu-id="06325-241">Se debe establecer en `relativeMonthly`.</span><span class="sxs-lookup"><span data-stu-id="06325-241">Must be set to `relativeMonthly`.</span></span> |

#### <a name="examples"></a><span data-ttu-id="06325-242">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="06325-242">Examples</span></span>

- <span data-ttu-id="06325-243">Repetir este evento el último miércoles de noviembre de cada año</span><span class="sxs-lookup"><span data-stu-id="06325-243">Repeat this event on the last Wednesday of November every year</span></span>

  ```json
    "pattern": {
      "type": "relativeYearly",
      "interval": 1,
      "daysOfWeek": [ "Wednesday" ],
      "index": "last",
      "month": 11
    }
  ```

## <a name="recurrence-ranges"></a><span data-ttu-id="06325-244">Intervalos de periodicidad</span><span class="sxs-lookup"><span data-stu-id="06325-244">Recurrence ranges</span></span>

<span data-ttu-id="06325-245">La segunda parte de una repetición es el rango.</span><span class="sxs-lookup"><span data-stu-id="06325-245">The second part of a recurrence is the range.</span></span> <span data-ttu-id="06325-246">Especifica cuánto tiempo se repite el patrón.</span><span class="sxs-lookup"><span data-stu-id="06325-246">This specifies how long the pattern repeats.</span></span> <span data-ttu-id="06325-247">Por ejemplo, un evento podría terminar después de 10 repeticiones, en una fecha específica, o podría no tener fin.</span><span class="sxs-lookup"><span data-stu-id="06325-247">For example, an event could end after 10 occurrences, by a specific date, or could have no end.</span></span> <span data-ttu-id="06325-248">Un intervalo se representa en la API por el [recurso recurrenceRange](../api-reference/v1.0/resources/recurrencepattern.md).</span><span class="sxs-lookup"><span data-stu-id="06325-248">A range is represented in the API by the [recurrenceRange resource](../api-reference/v1.0/resources/recurrencepattern.md).</span></span>

<span data-ttu-id="06325-249">Según el tipo de intervalo, ciertos campos de **recurrenceRange** son obligatorios o ignorados.</span><span class="sxs-lookup"><span data-stu-id="06325-249">Depending on the type of range, certain fields of **recurrenceRange** are required or ignored.</span></span>

> <span data-ttu-id="06325-250">**Nota**: Incluso si se omite un campo, también se valida.</span><span class="sxs-lookup"><span data-stu-id="06325-250">**Note**: Even if a field is ignored, it is still validated.</span></span> <span data-ttu-id="06325-251">Si un campo tiene una lista determinada de valores posibles, utilizar un valor fuera del conjunto permitido provocará un error, incluso si ese campo se omite.</span><span class="sxs-lookup"><span data-stu-id="06325-251">If a field has a set list of possible values, using a value outside the allowed set causes an error, even if that field is ignored.</span></span>

<span data-ttu-id="06325-252">Analicemos cada uno de los tipos de intervalo posibles.</span><span class="sxs-lookup"><span data-stu-id="06325-252">Let's take a look at each of the possible range types.</span></span>

### <a name="numbered-range"></a><span data-ttu-id="06325-253">Rango numerado</span><span class="sxs-lookup"><span data-stu-id="06325-253">Numbered range</span></span>

<span data-ttu-id="06325-254">El rango numerado hace que un evento se produzca un número fijo de veces (según el modelo) desde la fecha de inicio.</span><span class="sxs-lookup"><span data-stu-id="06325-254">The numbered range causes an event to occur a fixed number of times (based on the pattern) from a start date.</span></span>

#### <a name="relevant-properties"></a><span data-ttu-id="06325-255">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="06325-255">Relevant properties</span></span>

| <span data-ttu-id="06325-256">Propiedad</span><span class="sxs-lookup"><span data-stu-id="06325-256">Property</span></span> | <span data-ttu-id="06325-257">Relevancia</span><span class="sxs-lookup"><span data-stu-id="06325-257">Relevance</span></span> | <span data-ttu-id="06325-258">Descripción</span><span class="sxs-lookup"><span data-stu-id="06325-258">Description</span></span> |
|----------|-----------|-------------|
| <span data-ttu-id="06325-259">**numberOfOccurences**</span><span class="sxs-lookup"><span data-stu-id="06325-259">**numberOfOccurences**</span></span> | <span data-ttu-id="06325-260">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-260">Required</span></span> | <span data-ttu-id="06325-261">Especifica el número de repeticiones.</span><span class="sxs-lookup"><span data-stu-id="06325-261">Specifies the number of occurrences.</span></span> <span data-ttu-id="06325-262">Debe ser un número entero positivo.</span><span class="sxs-lookup"><span data-stu-id="06325-262">Must be a positive integer.</span></span> |
| <span data-ttu-id="06325-263">**recurrenceTimeZone**</span><span class="sxs-lookup"><span data-stu-id="06325-263">**recurrenceTimeZone**</span></span> | <span data-ttu-id="06325-264">Opcional</span><span class="sxs-lookup"><span data-stu-id="06325-264">Optional</span></span> | <span data-ttu-id="06325-265">Especifica la zona horaria de la propiedad **startDate**.</span><span class="sxs-lookup"><span data-stu-id="06325-265">Specifies the time zone for the **startDate** property.</span></span> <span data-ttu-id="06325-266">Si no se especifica, se usa la zona horaria del evento.</span><span class="sxs-lookup"><span data-stu-id="06325-266">If not specified, the time zone of the event is used.</span></span> |
| <span data-ttu-id="06325-267">**startDate**</span><span class="sxs-lookup"><span data-stu-id="06325-267">**startDate**</span></span> | <span data-ttu-id="06325-268">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-268">Required</span></span> | <span data-ttu-id="06325-269">Especifica la fecha para comenzar a aplicar el patrón.</span><span class="sxs-lookup"><span data-stu-id="06325-269">Specifies the date to start applying the pattern.</span></span> <span data-ttu-id="06325-270">El valor de **startDate** DEBE corresponderse con el valor de la fecha de la propiedad **start** en el [recurso de evento](../api-reference/v1.0/resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="06325-270">The value of **startDate** MUST correspond to the date value of the **start** property on the [event resource](../api-reference/v1.0/resources/event.md).</span></span> <span data-ttu-id="06325-271">Tenga en cuenta que no puede producirse la primera aparición de la reunión en esta fecha si no encaja en el patrón.</span><span class="sxs-lookup"><span data-stu-id="06325-271">Note that the first occurrence of the meeting may not occur on this date if it does not fit the pattern.</span></span> |
| <span data-ttu-id="06325-272">**type**</span><span class="sxs-lookup"><span data-stu-id="06325-272">**type**</span></span> | <span data-ttu-id="06325-273">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-273">Required</span></span> | <span data-ttu-id="06325-274">Se debe establecer en `numbered`.</span><span class="sxs-lookup"><span data-stu-id="06325-274">Must be set to `numbered`.</span></span> |

#### <a name="examples"></a><span data-ttu-id="06325-275">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="06325-275">Examples</span></span>

- <span data-ttu-id="06325-276">Repetir este evento 10 veces</span><span class="sxs-lookup"><span data-stu-id="06325-276">Repeat this event 10 times</span></span>

  ```json
    "range": {
      "type": "numbered",
      "startDate": "2017-04-02",
      "numberOfOccurrences": 10
    }
  ```

### <a name="end-date-range"></a><span data-ttu-id="06325-277">Intervalo de fecha de finalización</span><span class="sxs-lookup"><span data-stu-id="06325-277">End date range</span></span>

<span data-ttu-id="06325-278">El intervalo de fecha de finalización hace que un evento se repita todos los días que encajan en el patrón aplicable entre una fecha inicial y una fecha de finalización.</span><span class="sxs-lookup"><span data-stu-id="06325-278">The end date range causes an event to occur on all days that fit the applicable pattern between a start date and an end date.</span></span>

#### <a name="relevant-properties"></a><span data-ttu-id="06325-279">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="06325-279">Relevant properties</span></span>

| <span data-ttu-id="06325-280">Propiedad</span><span class="sxs-lookup"><span data-stu-id="06325-280">Property</span></span> | <span data-ttu-id="06325-281">Relevancia</span><span class="sxs-lookup"><span data-stu-id="06325-281">Relevance</span></span> | <span data-ttu-id="06325-282">Descripción</span><span class="sxs-lookup"><span data-stu-id="06325-282">Description</span></span> |
|----------|-----------|-------------|
| <span data-ttu-id="06325-283">**endDate**</span><span class="sxs-lookup"><span data-stu-id="06325-283">**endDate**</span></span> | <span data-ttu-id="06325-284">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-284">Required</span></span> | <span data-ttu-id="06325-285">Especifica la fecha para dejar de aplicar el patrón.</span><span class="sxs-lookup"><span data-stu-id="06325-285">Specifies the date to stop applying the pattern.</span></span> <span data-ttu-id="06325-286">Tenga en cuenta que no puede producirse la última aparición de la reunión en esta fecha si no encaja en el patrón.</span><span class="sxs-lookup"><span data-stu-id="06325-286">Note that the last occurrence of the meeting may not occur on this date if it does not fit the pattern.</span></span> |
| <span data-ttu-id="06325-287">**recurrenceTimeZone**</span><span class="sxs-lookup"><span data-stu-id="06325-287">**recurrenceTimeZone**</span></span> | <span data-ttu-id="06325-288">Opcional</span><span class="sxs-lookup"><span data-stu-id="06325-288">Optional</span></span> | <span data-ttu-id="06325-289">Especifica la zona horaria de las propiedades **startDate** y **endDate**.</span><span class="sxs-lookup"><span data-stu-id="06325-289">Specifies the time zone for the **startDate** and **endDate** properties.</span></span> <span data-ttu-id="06325-290">Si no se especifica, se usa la zona horaria del evento.</span><span class="sxs-lookup"><span data-stu-id="06325-290">If not specified, the time zone of the event is used.</span></span> |
| <span data-ttu-id="06325-291">**startDate**</span><span class="sxs-lookup"><span data-stu-id="06325-291">**startDate**</span></span> | <span data-ttu-id="06325-292">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-292">Required</span></span> | <span data-ttu-id="06325-293">Especifica la fecha para comenzar a aplicar el patrón.</span><span class="sxs-lookup"><span data-stu-id="06325-293">Specifies the date to start applying the pattern.</span></span> <span data-ttu-id="06325-294">El valor de **startDate** DEBE corresponderse con el valor de la fecha de la propiedad **start** en el [recurso de evento](../api-reference/v1.0/resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="06325-294">The value of **startDate** MUST correspond to the date value of the **start** property on the [event resource](../api-reference/v1.0/resources/event.md).</span></span> <span data-ttu-id="06325-295">Tenga en cuenta que no puede producirse la primera aparición de la reunión en esta fecha si no encaja en el patrón.</span><span class="sxs-lookup"><span data-stu-id="06325-295">Note that the first occurrence of the meeting may not occur on this date if it does not fit the pattern.</span></span> |
| <span data-ttu-id="06325-296">**type**</span><span class="sxs-lookup"><span data-stu-id="06325-296">**type**</span></span> | <span data-ttu-id="06325-297">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-297">Required</span></span> | <span data-ttu-id="06325-298">Se debe establecer en **endDate**.</span><span class="sxs-lookup"><span data-stu-id="06325-298">Must be set to **endDate**.</span></span> |

#### <a name="examples"></a><span data-ttu-id="06325-299">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="06325-299">Examples</span></span>

- <span data-ttu-id="06325-300">Repetir este evento desde el 1 de julio de 2017 hasta el 31 de julio de 2017</span><span class="sxs-lookup"><span data-stu-id="06325-300">Repeat this event from July 1, 2017, to July 31, 2017</span></span>

  ```json
    "range": {
      "type": "endDate",
      "startDate": "2017-07-01",
      "endDate": "2017-07-31"
    }
  ```

### <a name="no-end-range"></a><span data-ttu-id="06325-301">Sin fecha de finalización</span><span class="sxs-lookup"><span data-stu-id="06325-301">No end range</span></span>

<span data-ttu-id="06325-302">Sin fecha de finalización hace que un evento se repita todos los días que encajen en el patrón aplicable después de una fecha de inicio.</span><span class="sxs-lookup"><span data-stu-id="06325-302">The no end range causes an event to occur on all days that fit the applicable pattern after a start date.</span></span>

#### <a name="relevant-properties"></a><span data-ttu-id="06325-303">Propiedades relevantes</span><span class="sxs-lookup"><span data-stu-id="06325-303">Relevant properties</span></span>

| <span data-ttu-id="06325-304">Propiedad</span><span class="sxs-lookup"><span data-stu-id="06325-304">Property</span></span> | <span data-ttu-id="06325-305">Relevancia</span><span class="sxs-lookup"><span data-stu-id="06325-305">Relevance</span></span> | <span data-ttu-id="06325-306">Descripción</span><span class="sxs-lookup"><span data-stu-id="06325-306">Description</span></span> |
|----------|-----------|-------------|
| <span data-ttu-id="06325-307">**recurrenceTimeZone**</span><span class="sxs-lookup"><span data-stu-id="06325-307">**recurrenceTimeZone**</span></span> | <span data-ttu-id="06325-308">Opcional</span><span class="sxs-lookup"><span data-stu-id="06325-308">Optional</span></span> | <span data-ttu-id="06325-309">Especifica la zona horaria de la propiedad **startDate**.</span><span class="sxs-lookup"><span data-stu-id="06325-309">Specifies the time zone for the **startDate** property.</span></span> <span data-ttu-id="06325-310">Si no se especifica, se usa la zona horaria del evento.</span><span class="sxs-lookup"><span data-stu-id="06325-310">If not specified, the time zone of the event is used.</span></span> |
| <span data-ttu-id="06325-311">**startDate**</span><span class="sxs-lookup"><span data-stu-id="06325-311">**startDate**</span></span> | <span data-ttu-id="06325-312">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-312">Required</span></span> | <span data-ttu-id="06325-313">Especifica la fecha para comenzar a aplicar el patrón.</span><span class="sxs-lookup"><span data-stu-id="06325-313">Specifies the date to start applying the pattern.</span></span> <span data-ttu-id="06325-314">El valor de **startDate** DEBE corresponderse con el valor de la fecha de la propiedad **start** en el [recurso de evento](../api-reference/v1.0/resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="06325-314">The value of **startDate** MUST correspond to the date value of the **start** property on the [event resource](../api-reference/v1.0/resources/event.md).</span></span> <span data-ttu-id="06325-315">Tenga en cuenta que no puede producirse la primera aparición de la reunión en esta fecha si no encaja en el patrón.</span><span class="sxs-lookup"><span data-stu-id="06325-315">Note that the first occurrence of the meeting may not occur on this date if it does not fit the pattern.</span></span> |
| <span data-ttu-id="06325-316">**type**</span><span class="sxs-lookup"><span data-stu-id="06325-316">**type**</span></span> | <span data-ttu-id="06325-317">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06325-317">Required</span></span> | <span data-ttu-id="06325-318">Se debe establecer en `noEnd`.</span><span class="sxs-lookup"><span data-stu-id="06325-318">Must be set to `noEnd`.</span></span> |

#### <a name="examples"></a><span data-ttu-id="06325-319">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="06325-319">Examples</span></span>

- <span data-ttu-id="06325-320">Repetir este evento desde 15 de mayo de 2017 para siempre</span><span class="sxs-lookup"><span data-stu-id="06325-320">Repeat this event from May 15, 2017, forever</span></span>

  ```json
    "range": {
      "type": "noEnd",
      "startDate": "2017-05-15"
    }
  ```

## <a name="using-patterns-and-ranges-to-create-recurring-events"></a><span data-ttu-id="06325-321">Usar patrones y rangos para crear eventos periódicos</span><span class="sxs-lookup"><span data-stu-id="06325-321">Using patterns and ranges to create recurring events</span></span>

<span data-ttu-id="06325-322">Ahora que hemos visto los patrones y rangos por separado, analicemos cómo funcionan e interactúan con las propiedades **start** y **end** en el evento.</span><span class="sxs-lookup"><span data-stu-id="06325-322">Now that we've looked at patterns and ranges separately, let's look at how they work together and how they interact with the **start** and **end** properties on the event.</span></span>

### <a name="creating-a-recurrence-rule"></a><span data-ttu-id="06325-323">Crear una regla de periodicidad</span><span class="sxs-lookup"><span data-stu-id="06325-323">Creating a recurrence rule</span></span>

<span data-ttu-id="06325-324">Para crear una regla de periodicidad, debe especificar tanto un patrón como un rango.</span><span class="sxs-lookup"><span data-stu-id="06325-324">To create a recurrence rule, you must specify both a pattern and a range.</span></span> <span data-ttu-id="06325-325">Cualquier tipo de patrón puede funcionar con cualquier tipo de rango.</span><span class="sxs-lookup"><span data-stu-id="06325-325">Any pattern type can work with any range type.</span></span> <span data-ttu-id="06325-326">A continuación, se muestran algunos ejemplos.</span><span class="sxs-lookup"><span data-stu-id="06325-326">Here are a few examples.</span></span>

#### <a name="examples"></a><span data-ttu-id="06325-327">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="06325-327">Examples</span></span>

- <span data-ttu-id="06325-328">**Reunión de 13:00 a 13:30 todos los lunes a partir del 4 de septiembre de 2017 hasta el final del año**</span><span class="sxs-lookup"><span data-stu-id="06325-328">**Meet from 1:00 PM to 1:30 PM every Monday starting September 4, 2017, until the end of the year**</span></span>

  - <span data-ttu-id="06325-329">El requisito "cada lunes" se cumple fácilmente por el tipo de patrón de periodicidad `weekly`.</span><span class="sxs-lookup"><span data-stu-id="06325-329">The "every Monday" requirement is easily met by the `weekly` recurrence pattern type.</span></span>
  - <span data-ttu-id="06325-330">El requisito "hasta el final del año" indica un tipo de intervalo de repetición `endDate`.</span><span class="sxs-lookup"><span data-stu-id="06325-330">The "until the end of the year" requirement indicates an `endDate` recurrence range type.</span></span>

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

  <span data-ttu-id="06325-331">Dado que el 31 de diciembre de 2017 es domingo, la última aparición en esta serie será el lunes 25 de diciembre.</span><span class="sxs-lookup"><span data-stu-id="06325-331">Because December 31, 2017, is on a Sunday, the last occurrence in this series will be on Monday, December 25.</span></span>

- <span data-ttu-id="06325-332">**Reunión de 14:00 a 15:00 el primer jueves de meses alternos a partir del 29 de agosto de 2017**</span><span class="sxs-lookup"><span data-stu-id="06325-332">**Meet from 2:00 PM to 3:00 PM on the first Thursday of every other month starting August 29, 2017**</span></span>

  - <span data-ttu-id="06325-333">El requisito "primer jueves de meses alternos" se consigue estableciendo un patrón mensual relativo.</span><span class="sxs-lookup"><span data-stu-id="06325-333">The "first Thursday of every other month" requirement is achievable by using a relative monthly pattern.</span></span> <span data-ttu-id="06325-334">La parte "de meses alternos" indica que **interval** debe establecerse en `2`.</span><span class="sxs-lookup"><span data-stu-id="06325-334">The "every other month" portion indicates that the **interval** should be set to `2`.</span></span>
  - <span data-ttu-id="06325-335">Dado que no hay ningún requisito de fecha de finalización, puede usarse un tipo de rango `noEnd`.</span><span class="sxs-lookup"><span data-stu-id="06325-335">Because there is no requirement on an end date, a `noEnd` range type can be used.</span></span>

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

  <span data-ttu-id="06325-336">Dado que el valor de **startDate** comienza tras el primer jueves de agosto, la primera aparición de esta serie será en septiembre.</span><span class="sxs-lookup"><span data-stu-id="06325-336">Because the value of **startDate** is after the first Thursday in August, the first occurrence of this series will be in September.</span></span>

## <a name="next-steps"></a><span data-ttu-id="06325-337">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="06325-337">Next steps</span></span>
    
<span data-ttu-id="06325-338">Obtenga más información sobre la [integración con el Calendario de Outlook](outlook-calendar-concept-overview.md).</span><span class="sxs-lookup"><span data-stu-id="06325-338">Find out more about [integrating with Outlook calendar](outlook-calendar-concept-overview.md).</span></span>
