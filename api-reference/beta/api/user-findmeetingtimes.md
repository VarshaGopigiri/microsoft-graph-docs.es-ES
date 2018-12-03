---
title: 'user: findMeetingTimes'
description: Sugerir horas de reunión y las ubicaciones en función de la disponibilidad del organizador y el asistente y hora o la ubicación de las restricciones especificadas como parámetros.
ms.openlocfilehash: 8768059b6c15f96c0798fc3c4542410515e32555
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088313"
---
# <a name="user-findmeetingtimes"></a><span data-ttu-id="e5e1a-103">user: findMeetingTimes</span><span class="sxs-lookup"><span data-stu-id="e5e1a-103">user: findMeetingTimes</span></span>

> <span data-ttu-id="e5e1a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e5e1a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e5e1a-106">Sugerir horas de reunión y las ubicaciones en función de la disponibilidad del organizador y el asistente y hora o la ubicación de las restricciones especificadas como parámetros.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-106">Suggest meeting times and locations based on organizer and attendee availability, and time or location constraints specified as parameters.</span></span>

<span data-ttu-id="e5e1a-p102">Si **findMeetingTimes** no puede devolver sugerencias de reunión, la respuesta podría indicar un motivo en la propiedad **emptySuggestionsReason**. Basándose en este valor, se pueden ajustar mejor los parámetros y llamar otra vez a **findMeetingTimes**.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-p102">If **findMeetingTimes** cannot return any meeting suggestions, the response would indicate a reason in the **emptySuggestionsReason** property. Based on this value, you can better adjust the parameters and call **findMeetingTimes** again.</span></span>


## <a name="permissions"></a><span data-ttu-id="e5e1a-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="e5e1a-109">Permissions</span></span>
<span data-ttu-id="e5e1a-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e5e1a-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e5e1a-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e5e1a-112">Permission type</span></span>      | <span data-ttu-id="e5e1a-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e5e1a-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e5e1a-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e5e1a-114">Delegated (work or school account)</span></span> | <span data-ttu-id="e5e1a-115">Calendars.Read.Shared, Calendars.ReadWrite.Shared</span><span class="sxs-lookup"><span data-stu-id="e5e1a-115">Calendars.Read.Shared, Calendars.ReadWrite.Shared</span></span>    |
|<span data-ttu-id="e5e1a-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e5e1a-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e5e1a-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-117">Not supported.</span></span>    |
|<span data-ttu-id="e5e1a-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e5e1a-118">Application</span></span> | <span data-ttu-id="e5e1a-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="e5e1a-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e5e1a-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/findMeetingTimes
POST /users/{id|userPrincipalName}/findMeetingTimes
```
## <a name="request-headers"></a><span data-ttu-id="e5e1a-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e5e1a-121">Request headers</span></span>
| <span data-ttu-id="e5e1a-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="e5e1a-122">Name</span></span>       | <span data-ttu-id="e5e1a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e5e1a-123">Value</span></span>|
|:---------------|:----------|
| <span data-ttu-id="e5e1a-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="e5e1a-124">Authorization</span></span>  | <span data-ttu-id="e5e1a-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="e5e1a-127">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="e5e1a-127">Prefer: outlook.timezone</span></span> | <span data-ttu-id="e5e1a-p105">Una cadena que representa una zona horaria concreta para la respuesta, por ejemplo, "Hora estándar del Pacífico". Opcional. Se utiliza la hora UTC si no se especifica este encabezado.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-p105">A string representing a specific time zone for the response, for example, "Pacific Standard Time". Optional. UTC is used if this header is not specified.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e5e1a-131">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="e5e1a-131">Request body</span></span>
<span data-ttu-id="e5e1a-p106">Todos los parámetros admitidos se enumeran a continuación. Dependiendo de su escenario, especifique un objeto JSON para cada uno de los parámetros necesarios en el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-p106">All the supported parameters are listed below. Depending on your scenario, specify a JSON object for each of the necessary parameters in the request body.</span></span> 


| <span data-ttu-id="e5e1a-134">Parámetro</span><span class="sxs-lookup"><span data-stu-id="e5e1a-134">Parameter</span></span>    | <span data-ttu-id="e5e1a-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="e5e1a-135">Type</span></span>   |<span data-ttu-id="e5e1a-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5e1a-136">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e5e1a-137">attendees</span><span class="sxs-lookup"><span data-stu-id="e5e1a-137">attendees</span></span>|<span data-ttu-id="e5e1a-138">Colección [attendeeBase](../resources/attendeebase.md)</span><span class="sxs-lookup"><span data-stu-id="e5e1a-138">[attendeeBase](../resources/attendeebase.md) collection</span></span>|<span data-ttu-id="e5e1a-p107">Una colección de los asistentes o los recursos de la reunión. Puesto que findMeetingTimes supone que cualquier asistente que sea una persona siempre es necesario, especifique `required` para una persona y `resource` para un recurso en la propiedad **tipo** correspondiente. Una colección vacía hace que **findMeetingTimes** busque intervalos de tiempo libres solo para el organizador. Opcional.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-p107">A collection of attendees or resources for the meeting. Since findMeetingTimes assumes that any attendee who is a person is always required, specify `required` for a person and `resource` for a resource in the corresponding **type** property. An empty collection causes **findMeetingTimes** to look for free time slots for only the organizer. Optional.</span></span>|
|<span data-ttu-id="e5e1a-143">isOrganizerOptional</span><span class="sxs-lookup"><span data-stu-id="e5e1a-143">isOrganizerOptional</span></span>|<span data-ttu-id="e5e1a-144">Edm.Boolean</span><span class="sxs-lookup"><span data-stu-id="e5e1a-144">Edm.Boolean</span></span>|<span data-ttu-id="e5e1a-p108">Especificar `True` si no es preciso que el organizador asista. El valor predeterminado es `false`. Opcional.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-p108">Specify `True` if the organizer doesn't necessarily have to attend. The default is `false`. Optional.</span></span>|
|<span data-ttu-id="e5e1a-148">locationConstraint</span><span class="sxs-lookup"><span data-stu-id="e5e1a-148">locationConstraint</span></span>|[<span data-ttu-id="e5e1a-149">locationConstraint</span><span class="sxs-lookup"><span data-stu-id="e5e1a-149">locationConstraint</span></span>](../resources/locationconstraint.md)|<span data-ttu-id="e5e1a-p109">Los requisitos del organizador sobre la ubicación de la reunión, por ejemplo si se requiere una sugerencia para una ubicación de la reunión o si hay ubicaciones específicas en las que únicamente pueda tener lugar la reunión. Opcional.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-p109">The organizer's requirements about the meeting location, such as whether a suggestion for a meeting location is required, or there are specific locations only where the meeting can take place. Optional.</span></span>|
|<span data-ttu-id="e5e1a-152">maxCandidates</span><span class="sxs-lookup"><span data-stu-id="e5e1a-152">maxCandidates</span></span>|<span data-ttu-id="e5e1a-153">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="e5e1a-153">Edm.Int32</span></span>|<span data-ttu-id="e5e1a-p110">El número máximo de sugerencias de hora de la reunión que se va a devolver. Opcional.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-p110">The maximum number of meeting time suggestions to be returned. Optional.</span></span>|
|<span data-ttu-id="e5e1a-156">meetingDuration</span><span class="sxs-lookup"><span data-stu-id="e5e1a-156">meetingDuration</span></span>|<span data-ttu-id="e5e1a-157">Edm.Duration</span><span class="sxs-lookup"><span data-stu-id="e5e1a-157">Edm.Duration</span></span>|<span data-ttu-id="e5e1a-p111">La duración de la reunión en formato [ISO8601](https://www.iso.org/iso/iso8601). Por ejemplo, 1 hora se indica como "PT1H", donde "P" es el designador de duración, "T" es el designador de tiempo y "H" es el designador de hora. Use M para indicar los minutos de la duración; por ejemplo, 2 horas y 30 minutos sería "PT2H30M". Si no se especifica ninguna duración de la reunión, **findMeetingTimes** usa el valor predeterminado de 30 minutos. Opcional.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-p111">The length of the meeting, denoted in [ISO8601](https://www.iso.org/iso/iso8601) format. For example, 1 hour is denoted as 'PT1H', where 'P' is the duration designator, 'T' is the time designator, and 'H' is the hour designator. Use M to indicate minutes for the duration; for example, 2 hours and 30 minutes would be 'PT2H30M'. If no meeting duration is specified, **findMeetingTimes** uses the default of 30 minutes. Optional.</span></span>|
|<span data-ttu-id="e5e1a-163">minimumAttendeePercentage</span><span class="sxs-lookup"><span data-stu-id="e5e1a-163">minimumAttendeePercentage</span></span>|<span data-ttu-id="e5e1a-164">Edm.Double</span><span class="sxs-lookup"><span data-stu-id="e5e1a-164">Edm.Double</span></span>| <span data-ttu-id="e5e1a-p112">La [confianza](#the-confidence-of-a-meeting-suggestion) mínima necesaria para que se devuelva un intervalo de tiempo en la respuesta. Es un valor de porcentaje (%) comprendido entre 0 y 100. Opcional.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-p112">The minimum required [confidence](#the-confidence-of-a-meeting-suggestion) for a time slot to be returned in the response. It is a % value ranging from 0 to 100. Optional.</span></span>|
|<span data-ttu-id="e5e1a-168">returnSuggestionReasons</span><span class="sxs-lookup"><span data-stu-id="e5e1a-168">returnSuggestionReasons</span></span>|<span data-ttu-id="e5e1a-169">Edm.Boolean</span><span class="sxs-lookup"><span data-stu-id="e5e1a-169">Edm.Boolean</span></span>|<span data-ttu-id="e5e1a-p113">Especifique `True` para devolver un motivo para cada sugerencia de la reunión en la propiedad **suggestionReason**. El valor predeterminado es `false` para no devolver esa propiedad. Opcional.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-p113">Specify `True` to return a reason for each meeting suggestion in the **suggestionReason** property. The default is `false` to not return that property. Optional.</span></span>|
|<span data-ttu-id="e5e1a-173">timeConstraint</span><span class="sxs-lookup"><span data-stu-id="e5e1a-173">timeConstraint</span></span>|[<span data-ttu-id="e5e1a-174">timeConstraint</span><span class="sxs-lookup"><span data-stu-id="e5e1a-174">timeConstraint</span></span>](../resources/timeconstraint.md)|<span data-ttu-id="e5e1a-p114">Las restricciones de tiempo para una reunión, que pueden incluir la naturaleza de la reunión (propiedad **activityDomain**) y posibles periodos de tiempo de la reunión (propiedad **timeSlots**). **findMeetingTimes** asume **activityDomain** como `work` si no especifica este parámetro. Opcional.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-p114">Any time restrictions for a meeting, which can include the nature of the meeting (**activityDomain** property) and possible meeting time periods (**timeSlots** property). **findMeetingTimes** assumes **activityDomain** as `work` if you don't specify this parameter. Optional.</span></span>|

<span data-ttu-id="e5e1a-178">En la tabla siguiente se describen las restricciones puede especificar en el parámetro **timeConstraint**.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-178">The following table describes the restrictions you can further specify in the **timeConstraint** parameter.</span></span>

|<span data-ttu-id="e5e1a-179">valor activityDomain en timeConstraint</span><span class="sxs-lookup"><span data-stu-id="e5e1a-179">activityDomain value in timeConstraint</span></span>|<span data-ttu-id="e5e1a-180">Sugerencias de hora de reunión</span><span class="sxs-lookup"><span data-stu-id="e5e1a-180">Suggestions for meeting times</span></span>|
|:-----|:-----|
|<span data-ttu-id="e5e1a-181">trabajo</span><span class="sxs-lookup"><span data-stu-id="e5e1a-181">work</span></span>| <span data-ttu-id="e5e1a-p115">Las sugerencias se encuentran dentro de la jornada laboral del usuario, que está definida en su configuración de calendario y tanto el administrador como el propio usuario pueden personalizar. Las horas de trabajo por defecto son de lunes a viernes, de 8 a.m. a 5 p.m. en la zona horaria establecida para el buzón. Este es el valor predeterminado si no se especifica **activityDomain**.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-p115">Suggestions are within the user's work hours which are defined in the user’s calendar configuration and can be customized by the user or administrator. The default work hours are Monday to Friday, 8am to 5pm in the time zone set for the mailbox. This is the default value if no **activityDomain** is specified.</span></span> |
|<span data-ttu-id="e5e1a-185">personal</span><span class="sxs-lookup"><span data-stu-id="e5e1a-185">personal</span></span>| <span data-ttu-id="e5e1a-p116">Las sugerencias se encuentran dentro de la jornada laboral del usuario y en sábado y domingo. El valor predeterminado es del lunes al domingo, de 8 a.m. a 5 p.m., en la configuración de zona horaria para el buzón.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-p116">Suggestions are within the user's work hours, and Saturday and Sunday. The default is Monday to Sunday, 8am to 5pm, in the time zone setting for the mailbox.</span></span>|
|<span data-ttu-id="e5e1a-188">sin restricciones</span><span class="sxs-lookup"><span data-stu-id="e5e1a-188">unrestricted</span></span> | <span data-ttu-id="e5e1a-189">Las sugerencias pueden pertenecer a cualquier hora del día, todos los días de la semana.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-189">Suggestions can be from all hours of a day, all days of a week.</span></span>|
|<span data-ttu-id="e5e1a-190">desconocido</span><span class="sxs-lookup"><span data-stu-id="e5e1a-190">unknown</span></span> | <span data-ttu-id="e5e1a-p117">No utilice este valor, pues quedará obsoleto en el futuro. Actualmente se comporta igual que `work`. Cambie cualquier código existente para usar `work`, `personal` o `unrestricted` según corresponda.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-p117">Do not use this value as it will be deprecated in the future. Currently behaves the same as `work`. Change any existing code to use `work`, `personal` or `unrestricted` as appropriate.</span></span>


<span data-ttu-id="e5e1a-p118">Basándose en los parámetros especificados, **findMeetingTimes** comprueba el estado de disponibilidad en los calendarios principales del organizador y los asistentes. La acción calcula la mejor hora de la reunión posible y devuelve cualquier sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-p118">Based on the specified parameters,**findMeetingTimes** checks the free/busy status in the primary calendars of the organizer and attendees. The action calculates the best possible meeting times, and returns any meeting suggestions.</span></span>

## <a name="response"></a><span data-ttu-id="e5e1a-196">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e5e1a-196">Response</span></span>

<span data-ttu-id="e5e1a-197">Si es correcto, este método devuelve un código de respuesta `200 OK` y un objeto [meetingTimeSuggestionsResult](../resources/meetingtimesuggestionsresult.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-197">If successful, this method returns `200 OK` response code and a [meetingTimeSuggestionsResult](../resources/meetingtimesuggestionsresult.md) in the response body.</span></span> 

<span data-ttu-id="e5e1a-p119">Un objeto **meetingTimeSuggestionsResult** incluye una colección de sugerencias de la reunión y una propiedad **emptySuggestionsReason**. Cada sugerencia se define como una [meetingTimeSuggestion](../resources/meetingtimesuggestion.md), con los asistentes con un nivel de confianza medio del 50 % de asistir o un porcentaje concreto que especificó en el parámetro **minimumAttendeePercentage**.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-p119">A **meetingTimeSuggestionsResult** includes a collection of meeting suggestions and an **emptySuggestionsReason** property. Each suggestion is defined as a [meetingTimeSuggestion](../resources/meetingtimesuggestion.md), with attendees having on the average a confidence level of 50% to attend, or a specific % that you have specified in the **minimumAttendeePercentage** parameter.</span></span> 

<span data-ttu-id="e5e1a-200">De forma predeterminada, cada sugerencia de hora de la reunión se devuelve en formato UTC.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-200">By default, each meeting time suggestion is returned in UTC.</span></span> 

<span data-ttu-id="e5e1a-p120">Si **findMeetingTimes** no puede devolver sugerencias de reunión, la respuesta podría indicar un motivo en la propiedad **emptySuggestionsReason**. Basándose en este valor, se pueden ajustar mejor los parámetros y llamar otra vez a **findMeetingTimes**.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-p120">If **findMeetingTimes** cannot return any meeting suggestions, the response would indicate a reason in the **emptySuggestionsReason** property. Based on this value, you can better adjust the parameters and call **findMeetingTimes** again.</span></span>

### <a name="the-confidence-of-a-meeting-suggestion"></a><span data-ttu-id="e5e1a-203">La confianza de una sugerencia de la reunión</span><span class="sxs-lookup"><span data-stu-id="e5e1a-203">The confidence of a meeting suggestion</span></span>

<span data-ttu-id="e5e1a-204">La propiedad **confidence** de un objeto **meetingTimeSuggestion** oscila entre 0 % y 100 %, y representa la posibilidad de que todos los asistentes asistan a la reunión, tomando como base de su estado de disponibilidad individual:</span><span class="sxs-lookup"><span data-stu-id="e5e1a-204">The **confidence** property of a **meetingTimeSuggestion** ranges from 0% to 100%, and represents the chance that all the attendees attend the meeting, based on each of their individual free/busy status:</span></span>

- <span data-ttu-id="e5e1a-205">Para cada asistente, un estado libre para una periodo de tiempo de reunión especificado se corresponde al 100 % de posibilidades de asistencia, un estado desconocido al 49 % y un estado ocupado al 0 %.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-205">For each attendee, a free status for a specified meeting time period corresponds to 100% chance of attendance, unknown status 49%, and busy status 0%.</span></span>
- <span data-ttu-id="e5e1a-206">La confianza de una sugerencia de hora de la reunión se calcula promediando la posibilidad de asistencia sobre todos los asistentes especificados para esa reunión.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-206">The confidence of a meeting time suggestion is computed by averaging the chance of attendance over all the attendees specified for that meeting.</span></span>
- <span data-ttu-id="e5e1a-p121">Si hay varias sugerencias de hora de la reunión, la acción **findMeetingTimes** ordena primero las sugerencias por su valor de confianza calculado de alto a bajo. Si hay sugerencias con la misma confianza, entonces la acción las ordena cronológicamente.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-p121">If there are multiple meeting time suggestions, the **findMeetingTimes** action first orders the suggestions by their computed confidence value from high to low. If there are suggestions with the same confidence, the action then orders these suggestions chronologically.</span></span>
- <span data-ttu-id="e5e1a-p122">Se puede usar el parámetro opcional **minimumAttendeePercentage** para **findMeetingTimes** para especificar que solo se devuelvan sugerencias de la hora de la reunión con al menos un nivel de confianza determinado. Por ejemplo, se puede especificar un valor **minimumAttendeePercentage** de 80 % si solo se quieren sugerencias que tengan una probabilidad del 80 % o más de que asistan todos los asistentes. Si no se especifica **minimumAttendeePercentage**, **findMeetingTimes** da por supuesto un valor de 50 %.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-p122">You can use the **minimumAttendeePercentage** optional parameter for **findMeetingTimes** to specify only meeting time suggestions of at least certain confidence level should be returned. For example, you can specify a **minimumAttendeePercentage** of 80% if you want only suggestions that have an 80% chance or more that all the attendees are attending. If you do not specify **minimumAttendeePercentage**, **findMeetingTimes** assumes a value of 50%.</span></span>

<span data-ttu-id="e5e1a-212">Por ejemplo, si una sugerencia de hora de la reunión implica tres asistentes con el siguiente estado de disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="e5e1a-212">As an example, if a meeting time suggestion involves 3 attendees with the following free/busy status:</span></span>

|<span data-ttu-id="e5e1a-213">**Asistente**</span><span class="sxs-lookup"><span data-stu-id="e5e1a-213">**Attendee**</span></span>|<span data-ttu-id="e5e1a-214">**Estado de disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="e5e1a-214">**Free/busy status**</span></span>|<span data-ttu-id="e5e1a-215">**Posibilidades de asistencia (%)**</span><span class="sxs-lookup"><span data-stu-id="e5e1a-215">**% Chance of attendance**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e5e1a-216">Dana</span><span class="sxs-lookup"><span data-stu-id="e5e1a-216">Dana</span></span> | <span data-ttu-id="e5e1a-217">Libre</span><span class="sxs-lookup"><span data-stu-id="e5e1a-217">Free</span></span> | <span data-ttu-id="e5e1a-218">100 %</span><span class="sxs-lookup"><span data-stu-id="e5e1a-218">100%</span></span> |
|<span data-ttu-id="e5e1a-219">Pelayo</span><span class="sxs-lookup"><span data-stu-id="e5e1a-219">John</span></span> | <span data-ttu-id="e5e1a-220">Desconocido</span><span class="sxs-lookup"><span data-stu-id="e5e1a-220">Unknown</span></span> | <span data-ttu-id="e5e1a-221">49 %</span><span class="sxs-lookup"><span data-stu-id="e5e1a-221">49%</span></span> |
|<span data-ttu-id="e5e1a-222">Naiara</span><span class="sxs-lookup"><span data-stu-id="e5e1a-222">Samantha</span></span> | <span data-ttu-id="e5e1a-223">Ocupado</span><span class="sxs-lookup"><span data-stu-id="e5e1a-223">Busy</span></span> | <span data-ttu-id="e5e1a-224">0 %</span><span class="sxs-lookup"><span data-stu-id="e5e1a-224">0%</span></span> |

<span data-ttu-id="e5e1a-225">Entonces la confianza de la sugerencia de hora de la reunión, que es la posibilidad media de asistencia, es (100 % + 49 % + 0 %)/3 = 49,66 %.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-225">Then the confidence of the meeting time suggestion, which is the average chance of attendance, is (100% + 49% + 0%)/3 = 49.66%.</span></span>

<span data-ttu-id="e5e1a-226">Si especifica un valor **minimumAttendeePercentage** del 80 % en una operación **findMeetingTimes**, porque 49,66 %< 8 0%, la operación no sugerirá esta hora en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-226">If you specify a **minimumAttendeePercentage** of 80% in a **findMeetingTimes** operation, because 49.66% < 80%, the operation will not suggest this time in the response.</span></span>

## <a name="example"></a><span data-ttu-id="e5e1a-227">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e5e1a-227">Example</span></span>

<span data-ttu-id="e5e1a-228">En el ejemplo siguiente se muestra cómo encontrar tiempo para reunirse en un lugar determinado y solicitar un motivo para cada sugerencia, especificando los siguientes parámetros en el cuerpo de la solicitud:</span><span class="sxs-lookup"><span data-stu-id="e5e1a-228">The following example shows how to find time to meet at a pre-determined location, and request a reason for each suggestion, by specifying the following parameters in the request body:</span></span>

- <span data-ttu-id="e5e1a-229">**attendees**</span><span class="sxs-lookup"><span data-stu-id="e5e1a-229">**attendees**</span></span>
- <span data-ttu-id="e5e1a-230">**locationConstraint**</span><span class="sxs-lookup"><span data-stu-id="e5e1a-230">**locationConstraint**</span></span>
- <span data-ttu-id="e5e1a-231">**timeConstraint**</span><span class="sxs-lookup"><span data-stu-id="e5e1a-231">**timeConstraint**</span></span>
- <span data-ttu-id="e5e1a-232">**meetingDuration**</span><span class="sxs-lookup"><span data-stu-id="e5e1a-232">**meetingDuration**</span></span>
- <span data-ttu-id="e5e1a-233">**returnSuggestionReasons**</span><span class="sxs-lookup"><span data-stu-id="e5e1a-233">**returnSuggestionReasons**</span></span>
- <span data-ttu-id="e5e1a-234">**minimumAttendeePercentage**</span><span class="sxs-lookup"><span data-stu-id="e5e1a-234">**minimumAttendeePercentage**</span></span>

<span data-ttu-id="e5e1a-235">Al establecer el parámetro **returnSuggestionReasons**, también se obtiene una explicación en la propiedad **suggestionReason** de cada sugerencia, si **findMeetingTimes** devuelve alguna sugerencia.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-235">By setting the **returnSuggestionReasons** parameter, you also get an explanation in the **suggestionReason** property for each suggestion, if **findMeetingTimes** returns any suggestion.</span></span>

<span data-ttu-id="e5e1a-p123">Observe que la solicitud especifica la hora en la zona horaria PST y la respuesta devuelve las sugerencias de hora de la reunión en UTC, de forma predeterminada. Se puede usar el encabezado de solicitud `Prefer: outlook.timezone` para especificar también PST para los valores de hora de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-p123">Notice that the request specifies time in the PST time zone, and the response returns meeting time suggestions in UTC, by default. You can use the `Prefer: outlook.timezone` request header to specify PST as well for the time values in the response.</span></span>

##### <a name="request"></a><span data-ttu-id="e5e1a-238">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e5e1a-238">Request</span></span>
<span data-ttu-id="e5e1a-239">Aquí está la solicitud de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-239">Here is the example request.</span></span>
<!-- {
  "blockType": "request",
  "name": "user_findmeetingtimes"
}-->
```http
POST https://graph.microsoft.com/beta/me/findMeetingTimes
Prefer: outlook.timezone="Pacific Standard Time"
Content-Type: application/json

{ 
  "attendees": [ 
    { 
      "type": "required",  
      "emailAddress": { 
        "name": "Samantha Booth",
        "address": "samanthab@contoso.onmicrosoft.com" 
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

##### <a name="response"></a><span data-ttu-id="e5e1a-240">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e5e1a-240">Response</span></span>
<span data-ttu-id="e5e1a-p124">Esta es una solicitud de ejemplo. Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e5e1a-p124">Here is an example response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#microsoft.graph.meetingTimeSuggestionsResult",
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
                            "address":"samanthab@contoso.onmicrosoft.com"
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
                            "address":"samanthab@contoso.onmicrosoft.com"
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
  "suppressions": [
      "Warning: /api-reference/beta/api/user_findmeetingtimes.md:
      Failed to parse any rows out of table with headers: |activityDomain value|Suggestions for meeting times|"
  ],
  "tocPath": ""
}-->