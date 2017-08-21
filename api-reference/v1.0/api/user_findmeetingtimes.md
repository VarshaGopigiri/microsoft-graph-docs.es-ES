# <a name="user-findmeetingtimes"></a><span data-ttu-id="02755-101">user: findMeetingTimes</span><span class="sxs-lookup"><span data-stu-id="02755-101">user: findMeetingTimes</span></span>
<span data-ttu-id="02755-102">Busque sugerencias de hora de la reunión en función de la disponibilidad del organizador y los asistentes, y restricciones de hora o de ubicación especificadas como parámetros.</span><span class="sxs-lookup"><span data-stu-id="02755-102">Find meeting time suggestions based on organizer and attendee availability, and time or location constraints specified as parameters.</span></span>

<span data-ttu-id="02755-p101">Si **findMeetingTimes** no puede devolver sugerencias de reunión, la respuesta podría indicar un motivo en la propiedad **emptySuggestionsReason**. Basándose en este valor, se pueden ajustar mejor los parámetros y llamar otra vez a **findMeetingTimes**.</span><span class="sxs-lookup"><span data-stu-id="02755-p101">If **findMeetingTimes** cannot return any meeting suggestions, the response would indicate a reason in the **emptySuggestionsReason** property. Based on this value, you can better adjust the parameters and call **findMeetingTimes** again.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="02755-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="02755-105">Prerequisites</span></span>
<span data-ttu-id="02755-106">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Calendars.Read.Shared* o *Calendars.ReadWrite.Shared*</span><span class="sxs-lookup"><span data-stu-id="02755-106">One of the following **scopes** is required to execute this API: *Calendars.Read.Shared* or *Calendars.ReadWrite.Shared*</span></span>
## <a name="http-request"></a><span data-ttu-id="02755-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="02755-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/findMeetingTimes
POST /users/{id|userPrincipalName}/findMeetingTimes
```
## <a name="request-headers"></a><span data-ttu-id="02755-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="02755-108">Request headers</span></span>
| <span data-ttu-id="02755-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="02755-109">Name</span></span>       | <span data-ttu-id="02755-110">Valor</span><span class="sxs-lookup"><span data-stu-id="02755-110">Value</span></span>|
|:---------------|:----------|
| <span data-ttu-id="02755-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="02755-111">Authorization</span></span>  | <span data-ttu-id="02755-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="02755-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="02755-114">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="02755-114">Prefer: outlook.timezone</span></span> | <span data-ttu-id="02755-p103">Una cadena que representa una zona horaria concreta para la respuesta, por ejemplo, "Hora estándar del Pacífico". Opcional. Se utiliza la hora UTC si no se especifica este encabezado.</span><span class="sxs-lookup"><span data-stu-id="02755-p103">A string representing a specific time zone for the response, for example, "Pacific Standard Time". Optional. UTC is used if this header is not specified.</span></span>|


## <a name="request-body"></a><span data-ttu-id="02755-118">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="02755-118">Request body</span></span>
<span data-ttu-id="02755-p104">Todos los parámetros admitidos se enumeran a continuación. Dependiendo de su escenario, especifique un objeto JSON para cada uno de los parámetros necesarios en el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="02755-p104">All the supported parameters are listed below. Depending on your scenario, specify a JSON object for each of the necessary parameters in the request body.</span></span> 


| <span data-ttu-id="02755-121">Parámetro</span><span class="sxs-lookup"><span data-stu-id="02755-121">Parameter</span></span>    | <span data-ttu-id="02755-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="02755-122">Type</span></span>   |<span data-ttu-id="02755-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="02755-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="02755-124">attendees</span><span class="sxs-lookup"><span data-stu-id="02755-124">attendees</span></span>|<span data-ttu-id="02755-125">Colección [attendeeBase](../resources/attendeebase.md)</span><span class="sxs-lookup"><span data-stu-id="02755-125">[attendeeBase](../resources/attendeebase.md) collection</span></span>|<span data-ttu-id="02755-p105">Una colección de los asistentes o los recursos de la reunión. Puesto que findMeetingTimes supone que cualquier asistente que sea una persona siempre es necesario, especifique `required` para una persona y `resource` para un recurso en la propiedad **tipo** correspondiente. Una colección vacía hace que **findMeetingTimes** busque intervalos de tiempo libres solo para el organizador. Opcional.</span><span class="sxs-lookup"><span data-stu-id="02755-p105">A collection of attendees or resources for the meeting. Since findMeetingTimes assumes that any attendee who is a person is always required, specify `required` for a person and `resource` for a resource in the corresponding **type** property. An empty collection causes **findMeetingTimes** to look for free time slots for only the organizer. Optional.</span></span>|
|<span data-ttu-id="02755-130">isOrganizerOptional</span><span class="sxs-lookup"><span data-stu-id="02755-130">isOrganizerOptional</span></span>|<span data-ttu-id="02755-131">Edm.Boolean</span><span class="sxs-lookup"><span data-stu-id="02755-131">Edm.Boolean</span></span>|<span data-ttu-id="02755-p106">Especificar `True` si no es preciso que el organizador asista. El valor predeterminado es `false`. Opcional.</span><span class="sxs-lookup"><span data-stu-id="02755-p106">Specify `True` if the organizer doesn't necessarily have to attend. The default is `false`. Optional.</span></span>|
|<span data-ttu-id="02755-135">locationConstraint</span><span class="sxs-lookup"><span data-stu-id="02755-135">locationConstraint</span></span>|[<span data-ttu-id="02755-136">locationConstraint</span><span class="sxs-lookup"><span data-stu-id="02755-136">locationConstraint</span></span>](../resources/locationconstraint.md)|<span data-ttu-id="02755-p107">Los requisitos del organizador sobre la ubicación de la reunión, por ejemplo si se requiere una sugerencia para una ubicación de la reunión o si hay ubicaciones específicas en las que únicamente pueda tener lugar la reunión. Opcional.</span><span class="sxs-lookup"><span data-stu-id="02755-p107">The organizer's requirements about the meeting location, such as whether a suggestion for a meeting location is required, or there are specific locations only where the meeting can take place. Optional.</span></span>|
|<span data-ttu-id="02755-139">maxCandidates</span><span class="sxs-lookup"><span data-stu-id="02755-139">maxCandidates</span></span>|<span data-ttu-id="02755-140">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="02755-140">Edm.Int32</span></span>|<span data-ttu-id="02755-p108">El número máximo de sugerencias de hora de la reunión que se va a devolver. Opcional.</span><span class="sxs-lookup"><span data-stu-id="02755-p108">The maximum number of meeting time suggestions to be returned. Optional.</span></span>|
|<span data-ttu-id="02755-143">meetingDuration</span><span class="sxs-lookup"><span data-stu-id="02755-143">meetingDuration</span></span>|<span data-ttu-id="02755-144">Edm.Duration</span><span class="sxs-lookup"><span data-stu-id="02755-144">Edm.Duration</span></span>|<span data-ttu-id="02755-p109">La duración de la reunión en formato [ISO8601](http://www.iso.org/iso/iso8601). Por ejemplo, 1 hora se indica como "PT1H", donde "P" es el designador de duración, "T" es el designador de tiempo y "H" es el designador de hora. Use M para indicar los minutos de la duración; por ejemplo, 2 horas y 30 minutos sería "PT2H30M". Si no se especifica ninguna duración de la reunión, **findMeetingTimes** usa el valor predeterminado de 30 minutos. Opcional.</span><span class="sxs-lookup"><span data-stu-id="02755-p109">The length of the meeting, denoted in [ISO8601](http://www.iso.org/iso/iso8601) format. For example, 1 hour is denoted as 'PT1H', where 'P' is the duration designator, 'T' is the time designator, 'H' is the hour designator. If no meeting duration is specified, **findMeetingTimes** uses the default of 30 minutes. Optional.</span></span>|
|<span data-ttu-id="02755-150">minimumAttendeePercentage</span><span class="sxs-lookup"><span data-stu-id="02755-150">minimumAttendeePercentage</span></span>|<span data-ttu-id="02755-151">Edm.Double</span><span class="sxs-lookup"><span data-stu-id="02755-151">Edm.Double</span></span>| <span data-ttu-id="02755-p110">La [confianza](#the-confidence-of-a-meeting-suggestion) mínima necesaria para que se devuelva un intervalo de tiempo en la respuesta. Es un valor de porcentaje (%) comprendido entre 0 y 100. Opcional.</span><span class="sxs-lookup"><span data-stu-id="02755-p110">The minimum required [confidence](#the-confidence-of-a-meeting-suggestion) for a time slot to be returned in the response. It is a % value ranging from 0 to 100. Optional.</span></span>|
|<span data-ttu-id="02755-155">returnSuggestionReasons</span><span class="sxs-lookup"><span data-stu-id="02755-155">returnSuggestionReasons</span></span>|<span data-ttu-id="02755-156">Edm.Boolean</span><span class="sxs-lookup"><span data-stu-id="02755-156">Edm.Boolean</span></span>|<span data-ttu-id="02755-p111">Especifique `True` para devolver un motivo para cada sugerencia de la reunión en la propiedad **suggestionReason**. El valor predeterminado es `false` para no devolver esa propiedad. Opcional.</span><span class="sxs-lookup"><span data-stu-id="02755-p111">Specify `True` to return a reason for each meeting suggestion in the **suggestionReason** property. The default is `false` to not return that property. Optional.</span></span>|
|<span data-ttu-id="02755-160">timeConstraint</span><span class="sxs-lookup"><span data-stu-id="02755-160">timeConstraint</span></span>|[<span data-ttu-id="02755-161">timeConstraint</span><span class="sxs-lookup"><span data-stu-id="02755-161">timeConstraint</span></span>](../resources/timeconstraint.md)|<span data-ttu-id="02755-p112">Las restricciones de tiempo para una reunión, que pueden incluir la naturaleza de la reunión (propiedad **activityDomain**) y posibles periodos de tiempo de la reunión (propiedad **timeSlots**). **findMeetingTimes** asume **activityDomain** como `work` si no especifica este parámetro. Opcional.</span><span class="sxs-lookup"><span data-stu-id="02755-p112">Any time restrictions for a meeting, which can include the nature of the meeting (**activityDomain** property) and possible meeting time periods (**timeSlots** property). **findMeetingTimes** assumes **activityDomain** as `work` if you don't specify this parameter. Optional.</span></span>|

<span data-ttu-id="02755-165">En la tabla siguiente se describen las restricciones puede especificar en el parámetro **timeConstraint**.</span><span class="sxs-lookup"><span data-stu-id="02755-165">The following table describes the restrictions you can further specify in the **timeConstraint** parameter.</span></span>

|<span data-ttu-id="02755-166">**valor activityDomain en timeConstraint**</span><span class="sxs-lookup"><span data-stu-id="02755-166">**activityDomain value in timeConstraint**</span></span>|<span data-ttu-id="02755-167">**Sugerencias de hora de reunión**</span><span class="sxs-lookup"><span data-stu-id="02755-167">**Suggestions for meeting times**</span></span>|
|:-----|:-----|
|<span data-ttu-id="02755-168">trabajo</span><span class="sxs-lookup"><span data-stu-id="02755-168">work</span></span>| <span data-ttu-id="02755-p113">Las sugerencias se encuentran dentro de la jornada laboral del usuario, que está definida en su configuración de calendario y tanto el administrador como el propio usuario pueden personalizar. Las horas de trabajo por defecto son de lunes a viernes, de 8 a.m. a 5 p.m. en la zona horaria establecida para el buzón. Este es el valor predeterminado si no se especifica **activityDomain**.</span><span class="sxs-lookup"><span data-stu-id="02755-p113">Suggestions are within the user's work hours which are defined in the user’s calendar configuration and can be customized by the user or administrator. The default work hours are Monday to Friday, 8am to 5pm in the time zone set for the mailbox. This is the default value if no **activityDomain** is specified.</span></span> |
|<span data-ttu-id="02755-172">personal</span><span class="sxs-lookup"><span data-stu-id="02755-172">personal</span></span>| <span data-ttu-id="02755-p114">Las sugerencias se encuentran dentro de la jornada laboral del usuario y en sábado y domingo. El valor predeterminado es del lunes al domingo, de 8 a.m. a 5 p.m., en la configuración de zona horaria para el buzón.</span><span class="sxs-lookup"><span data-stu-id="02755-p114">Suggestions are within the user's work hours, and Saturday and Sunday. The default is Monday to Sunday, 8am to 5pm, in the time zone setting for the mailbox.</span></span>|
|<span data-ttu-id="02755-175">sin restricciones</span><span class="sxs-lookup"><span data-stu-id="02755-175">unrestricted</span></span> | <span data-ttu-id="02755-176">Las sugerencias pueden pertenecer a cualquier hora del día, todos los días de la semana.</span><span class="sxs-lookup"><span data-stu-id="02755-176">Suggestions can be from all hours of a day, all days of a week.</span></span>|
|<span data-ttu-id="02755-177">desconocido</span><span class="sxs-lookup"><span data-stu-id="02755-177">unknown</span></span> | <span data-ttu-id="02755-p115">No utilice este valor, pues quedará obsoleto en el futuro. Actualmente se comporta igual que `work`. Cambie cualquier código existente para usar `work`, `personal` o `unrestricted` según corresponda.</span><span class="sxs-lookup"><span data-stu-id="02755-p115">Do not use this value as it will be deprecated in the future. Currently behaves the same as `work`. Change any existing code to use `work`, `personal` or `unrestricted` as appropriate.</span></span>


<span data-ttu-id="02755-p116">Basándose en los parámetros especificados, **findMeetingTimes** comprueba el estado de disponibilidad en los calendarios principales del organizador y los asistentes. La acción calcula la mejor hora de la reunión posible y devuelve cualquier sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="02755-p116">Based on the specified parameters,**findMeetingTimes** checks the free/busy status in the primary calendars of the organizer and attendees. The action calculates the best possible meeting times, and returns any meeting suggestions.</span></span>

## <a name="response"></a><span data-ttu-id="02755-183">Respuesta</span><span class="sxs-lookup"><span data-stu-id="02755-183">Response</span></span>

<span data-ttu-id="02755-184">Si es correcto, este método devuelve un código de respuesta `200, OK` y un objeto [meetingTimeSuggestionsResult](../resources/meetingTimeSuggestionsResult.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="02755-184">If successful, this method returns `200, OK` response code and a [meetingTimeSuggestionsResult](../resources/meetingTimeSuggestionsResult.md) in the response body.</span></span> 

<span data-ttu-id="02755-p117">Un objeto **meetingTimeSuggestionsResult** incluye una colección de sugerencias de la reunión y una propiedad **emptySuggestionsReason**. Cada sugerencia se define como una [meetingTimeSuggestion](../resources/meetingTimeSuggestion.md), con los asistentes con un nivel de confianza medio del 50 % de asistir o un porcentaje concreto que especificó en el parámetro **minimumAttendeePercentage**.</span><span class="sxs-lookup"><span data-stu-id="02755-p117">A **meetingTimeSuggestionsResult** includes a collection of meeting suggestions and an **emptySuggestionsReason** property. Each suggestion is defined as a [meetingTimeSuggestion](../resources/meetingTimeSuggestion.md), with attendees having on the average a confidence level of 50% to attend, or a specific % that you have specified in the **minimumAttendeePercentage** parameter.</span></span> 

<span data-ttu-id="02755-187">De forma predeterminada, cada sugerencia de hora de la reunión se devuelve en formato UTC.</span><span class="sxs-lookup"><span data-stu-id="02755-187">By default, each meeting time suggestion is returned in UTC.</span></span> 

<span data-ttu-id="02755-p118">Si **findMeetingTimes** no puede devolver sugerencias de reunión, la respuesta podría indicar un motivo en la propiedad **emptySuggestionsReason**. Basándose en este valor, se pueden ajustar mejor los parámetros y llamar otra vez a **findMeetingTimes**.</span><span class="sxs-lookup"><span data-stu-id="02755-p118">If **findMeetingTimes** cannot return any meeting suggestions, the response would indicate a reason in the **emptySuggestionsReason** property. Based on this value, you can better adjust the parameters and call **findMeetingTimes** again.</span></span>

### <a name="the-confidence-of-a-meeting-suggestion"></a><span data-ttu-id="02755-190">La confianza de una sugerencia de la reunión</span><span class="sxs-lookup"><span data-stu-id="02755-190">The confidence of a meeting suggestion</span></span>

<span data-ttu-id="02755-191">La propiedad **confidence** de un objeto **meetingTimeSuggestion** oscila entre 0 % y 100 %, y representa la posibilidad de que todos los asistentes asistan a la reunión, tomando como base de su estado de disponibilidad individual:</span><span class="sxs-lookup"><span data-stu-id="02755-191">The **confidence** property of a **meetingTimeSuggestion** ranges from 0% to 100%, and represents the chance that all the attendees attend the meeting, based on each of their individual free/busy status:</span></span>

- <span data-ttu-id="02755-192">Para cada asistente, un estado libre para una periodo de tiempo de reunión especificado se corresponde al 100 % de posibilidades de asistencia, un estado desconocido al 49 % y un estado ocupado al 0 %.</span><span class="sxs-lookup"><span data-stu-id="02755-192">For each attendee, a free status for a specified meeting time period corresponds to 100% chance of attendance, unknown status 49%, and busy status 0%.</span></span>
- <span data-ttu-id="02755-193">La confianza de una sugerencia de hora de la reunión se calcula promediando la posibilidad de asistencia sobre todos los asistentes especificados para esa reunión.</span><span class="sxs-lookup"><span data-stu-id="02755-193">The confidence of a meeting time suggestion is computed by averaging the chance of attendance over all the attendees specified for that meeting.</span></span>
- <span data-ttu-id="02755-p119">Se puede usar el parámetro opcional **minimumAttendeePercentage** para **findMeetingTimes** para especificar que solo se devuelvan sugerencias de la hora de la reunión con al menos un nivel de confianza determinado. Por ejemplo, se puede especificar un valor **minimumAttendeePercentage** de 80 % si solo se quieren sugerencias que tengan una probabilidad del 80 % o más de que asistan todos los asistentes. Si no se especifica **minimumAttendeePercentage**, **findMeetingTimes** da por supuesto un valor de 50 %.</span><span class="sxs-lookup"><span data-stu-id="02755-p119">You can use the **minimumAttendeePercentage** optional parameter for **findMeetingTimes** to specify only meeting time suggestions of at least certain confidence level should be returned. For example, you can specify a **minimumAttendeePercentage** of 80% if you want only suggestions that have an 80% chance or more that all the attendees are attending. If you do not specify **minimumAttendeePercentage**, **findMeetingTimes** assumes a value of 50%.</span></span>
- <span data-ttu-id="02755-p120">Si hay varias sugerencias de hora de la reunión, la acción **findMeetingTimes** ordena primero las sugerencias por su valor de confianza calculado de alto a bajo. Si hay sugerencias con la misma confianza, entonces la acción las ordena cronológicamente.</span><span class="sxs-lookup"><span data-stu-id="02755-p120">If there are multiple meeting time suggestions, the **findMeetingTimes** action first orders the suggestions by their computed confidence value from high to low. If there are suggestions with the same confidence, the action then orders these suggestions chronologically.</span></span>

<span data-ttu-id="02755-199">Por ejemplo, si una sugerencia de hora de la reunión implica tres asistentes con el siguiente estado de disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="02755-199">As an example, if a meeting time suggestion involves 3 attendees with the following free/busy status:</span></span>

|<span data-ttu-id="02755-200">**Asistente**</span><span class="sxs-lookup"><span data-stu-id="02755-200">**Attendee**</span></span>|<span data-ttu-id="02755-201">**Estado de disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="02755-201">**Free/busy status**</span></span>|<span data-ttu-id="02755-202">**Posibilidades de asistencia (%)**</span><span class="sxs-lookup"><span data-stu-id="02755-202">**% Chance of attendance**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="02755-203">Dana</span><span class="sxs-lookup"><span data-stu-id="02755-203">Dana</span></span> | <span data-ttu-id="02755-204">Libre</span><span class="sxs-lookup"><span data-stu-id="02755-204">Free</span></span> | <span data-ttu-id="02755-205">100 %</span><span class="sxs-lookup"><span data-stu-id="02755-205">100%</span></span> |
|<span data-ttu-id="02755-206">Pelayo</span><span class="sxs-lookup"><span data-stu-id="02755-206">John</span></span> | <span data-ttu-id="02755-207">Desconocido</span><span class="sxs-lookup"><span data-stu-id="02755-207">Unknown</span></span> | <span data-ttu-id="02755-208">49 %</span><span class="sxs-lookup"><span data-stu-id="02755-208">49%</span></span> |
|<span data-ttu-id="02755-209">Fanny</span><span class="sxs-lookup"><span data-stu-id="02755-209">Fanny</span></span> | <span data-ttu-id="02755-210">Ocupado</span><span class="sxs-lookup"><span data-stu-id="02755-210">Busy</span></span> | <span data-ttu-id="02755-211">0 %</span><span class="sxs-lookup"><span data-stu-id="02755-211">0%</span></span> |

<span data-ttu-id="02755-212">Entonces la confianza de la sugerencia de hora de la reunión, que es la posibilidad media de asistencia, es (100 % + 49 % + 0 %)/3 = 49,66 %.</span><span class="sxs-lookup"><span data-stu-id="02755-212">Then the confidence of the meeting time suggestion, which is the average chance of attendance, is (100% + 49% + 0%)/3 = 49.66%.</span></span>

<span data-ttu-id="02755-213">Si especifica un valor **minimumAttendeePercentage** del 80 % en una operación **findMeetingTimes**, porque 49,66 %< 8 0%, la operación no sugerirá esta hora en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="02755-213">If you specify a **minimumAttendeePercentage** of 80% in a **findMeetingTimes** operation, because 49.66% < 80%, the operation will not suggest this time in the response.</span></span>

## <a name="example"></a><span data-ttu-id="02755-214">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="02755-214">Example</span></span>

<span data-ttu-id="02755-215">En el ejemplo siguiente se muestra cómo encontrar tiempo para reunirse en un lugar determinado y solicitar un motivo para cada sugerencia, especificando los siguientes parámetros en el cuerpo de la solicitud:</span><span class="sxs-lookup"><span data-stu-id="02755-215">The following example shows how to find time to meet at a pre-determined location, and request a reason for each suggestion, by specifying the following parameters in the request body:</span></span>

- <span data-ttu-id="02755-216">**attendees**</span><span class="sxs-lookup"><span data-stu-id="02755-216">**attendees**</span></span>
- <span data-ttu-id="02755-217">**locationConstraint**</span><span class="sxs-lookup"><span data-stu-id="02755-217">**locationConstraint**</span></span>
- <span data-ttu-id="02755-218">**timeConstraint**</span><span class="sxs-lookup"><span data-stu-id="02755-218">**timeConstraint**</span></span>
- <span data-ttu-id="02755-219">**meetingDuration**</span><span class="sxs-lookup"><span data-stu-id="02755-219">**meetingDuration**</span></span>
- <span data-ttu-id="02755-220">**returnSuggestionReasons**</span><span class="sxs-lookup"><span data-stu-id="02755-220">**returnSuggestionReasons**</span></span>
- <span data-ttu-id="02755-221">**minimumAttendeePercentage**</span><span class="sxs-lookup"><span data-stu-id="02755-221">**minimumAttendeePercentage**</span></span>

<span data-ttu-id="02755-222">Al establecer el parámetro **returnSuggestionReasons**, también se obtiene una explicación en la propiedad **suggestionReason** de cada sugerencia, si **findMeetingTimes** devuelve alguna sugerencia.</span><span class="sxs-lookup"><span data-stu-id="02755-222">By setting the **returnSuggestionReasons** parameter, you also get an explanation in the **suggestionReason** property for each suggestion, if **findMeetingTimes** returns any suggestion.</span></span>

<span data-ttu-id="02755-p121">Observe que la solicitud especifica la hora en la zona horaria PST y la respuesta devuelve las sugerencias de hora de la reunión en UTC, de forma predeterminada. Se puede usar el encabezado de solicitud `Prefer: outlook.timezone` para especificar también PST para los valores de hora de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="02755-p121">Notice that the request specifies time in the PST time zone, and the response returns meeting time suggestions in UTC, by default. You can use the `Prefer: outlook.timezone` request header to specify PST as well for the time values in the response.</span></span>

##### <a name="request"></a><span data-ttu-id="02755-225">Solicitud</span><span class="sxs-lookup"><span data-stu-id="02755-225">Request</span></span>
<span data-ttu-id="02755-226">Aquí está la solicitud de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="02755-226">Here is the example request.</span></span>
<!-- {
  "blockType": "request",
  "name": "user_findmeetingtimes"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/findMeetingTimes
Prefer: outlook.timezone="Pacific Standard Time"
Content-Type: application/json

{ 
  "attendees": [ 
    { 
      "type": "required",  
      "emailAddress": { 
        "name": "Fanny Downs",
        "address": "fannyd@contoso.onmicrosoft.com" 
      } 
    }
  ],  
  "locationConstraint": { 
    "isRequired": "false",  
    "suggestLocation": "false",  
    "locations": [ 
      { 
        "resolveAvailability": "false",
        "displayName": "Conf room Hood" 
      } 
    ] 
  },  
  "timeConstraint": {
    "activityDomain":"unrestricted", 
    "timeslots": [ 
      { 
        "start": { 
          "dateTime": "2017-04-17T09:00:00",  
          "timeZone": "Pacific Standard Time" 
        },  
        "end": { 
          "dateTime": "2017-04-19T17:00:00",  
          "timeZone": "Pacific Standard Time" 
        } 
      } 
    ] 
  },  
  "meetingDuration": "PT2H",
  "returnSuggestionReasons": "true",
  "minimumAttendeePercentage": "100"
}
```

##### <a name="response"></a><span data-ttu-id="02755-227">Respuesta</span><span class="sxs-lookup"><span data-stu-id="02755-227">Response</span></span>
<span data-ttu-id="02755-p122">Esta es una solicitud de ejemplo. Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="02755-p122">Here is an example response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.meetingTimeSuggestionsResult",
  "isCollection": false
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Preference-Applied: outlook.timezone="Pacific Standard Time"
Content-Length: 976

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#microsoft.graph.meetingTimeSuggestionsResult",
    "emptySuggestionsReason":"",
    "meetingTimeSuggestions":[
        {
            "confidence":100.0,
            "organizerAvailability":"free",
            "suggestionReason":"Suggested because it is one of the nearest times when all attendees are available.",
            "meetingTimeSlot":{
                "start":{
                    "dateTime":"2017-04-17T18:00:00.0000000",
                    "timeZone":"Pacific Standard Time"
                },
                "end":{
                    "dateTime":"2017-04-17T20:00:00.0000000",
                    "timeZone":"Pacific Standard Time"
                }
            },
            "attendeeAvailability":[
                {
                    "availability":"free",
                    "attendee":{
                        "type":"required",
                        "emailAddress":{
                            "address":"fannyd@contoso.onmicrosoft.com"
                        }
                    }
                }
            ],
            "locations":[
                {
                    "displayName":"Conf room Hood"
                }
            ]
        },
        {
            "confidence":100.0,
            "organizerAvailability":"free",
            "suggestionReason":"Suggested because it is one of the nearest times when all attendees are available.",
            "meetingTimeSlot":{
                "start":{
                    "dateTime":"2017-04-17T20:00:00.0000000",
                    "timeZone":"Pacific Standard Time"
                },
                "end":{
                    "dateTime":"2017-04-17T22:00:00.0000000",
                    "timeZone":"Pacific Standard Time"
                }
            },
            "attendeeAvailability":[
                {
                    "availability":"free",
                    "attendee":{
                        "type":"required",
                        "emailAddress":{
                            "address":"fannyd@contoso.onmicrosoft.com"
                        }
                    }
                }
            ],
            "locations":[
                {
                    "displayName":"Conf room Hood"
                }
            ]
        }
   ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: findMeetingTimes",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
