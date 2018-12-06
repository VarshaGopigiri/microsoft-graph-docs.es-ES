---
title: Buscar horas posibles para una reunión en el Calendario de Outlook
description: 'Buscar un horario y un lugar comunes para reunirse en un área profesional o académica a menudo conlleva sobrecargas. Las aplicaciones de Microsoft Graph pueden usar '
ms.openlocfilehash: 92390509f68d469cf9912e9e903a2576b8fa7506
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092953"
---
# <a name="find-possible-meeting-times-on-the-outlook-calendar"></a><span data-ttu-id="39023-104">Buscar horas posibles para una reunión en el Calendario de Outlook</span><span class="sxs-lookup"><span data-stu-id="39023-104">Find possible meeting times on the Outlook calendar</span></span>

<span data-ttu-id="39023-p102">Buscar un horario y un lugar comunes para reunirse en un área profesional o académica a menudo conlleva sobrecargas. Las aplicaciones de Microsoft Graph pueden utilizar [findMeetingTimes](/graph/api/user-findmeetingtimes?view=graph-rest-1.0) para identificar cualquier hora posible para una reunión que cumpla con los horarios, la ubicación y otras restricciones.</span><span class="sxs-lookup"><span data-stu-id="39023-p102">In a workplace or school, looking for a common time and place to meet often incurs overhead. Microsoft Graph applications can use [findMeetingTimes](/graph/api/user-findmeetingtimes?view=graph-rest-1.0) to identify any possible meeting times that satisfy time, location, and other constraints.</span></span>   

<span data-ttu-id="39023-p103">La acción **findMeetingTimes** permite especificar condiciones como el rango de fechas o el intervalo horario para una reunión, así como la duración, los asistentes opcionales y necesarios, y la naturaleza de la actividad (**activityDomain**). La acción tiene en cuenta la disponibilidad y la programación profesional habitual de los asistentes y organizadores, y sugiere los horarios que son adecuados para los participantes y el tipo de actividad. Por ejemplo, las sugerencias para una actividad de trabajo siempre se producen durante las horas de trabajo del organizador y los asistentes, y las sugerencias donde los asistentes necesarios están disponibles se ordenan en la parte de arriba de la lista de sugerencias.</span><span class="sxs-lookup"><span data-stu-id="39023-p103">The **findMeetingTimes** action lets you specify conditions such as the meeting date/time range, duration, optional or required attendees, and nature of the activity (**activityDomain**). The action takes into account the attendees' and organizer's normal work schedules and free/busy status, and suggests times that are appropriate for the participants and type of activity. For instance, suggestions for a work-related activity always occur during the work hours of the organizer and attendees, and suggestions where required attendees are available are ordered higher up in the suggested list.</span></span>

<span data-ttu-id="39023-p104">En Office 365, las horas de trabajo y las zonas horarias se pueden configurar en cada buzón. La acción **findMeetingTimes** controla las variaciones entre las zonas horarias del organizador y los asistentes. De manera predeterminada, **findMeetingTimes** devuelve sugerencias en UTC. Puede utilizar el siguiente encabezado de la solicitud para que **findMeetingTimes** devuelva sugerencias expresadas en una zona horaria específica.</span><span class="sxs-lookup"><span data-stu-id="39023-p104">In Office 365, work hours and time zones are configurable per mailbox. The **findMeetingTimes** action handles time zone variations among the organizer and attendees. By default, **findMeetingTimes** returns suggestions in UTC. You can use the following request header to have **findMeetingTimes** return suggestions expressed in a specific time zone.</span></span>
```
Prefer: outlook.timezone="{time-zone-string}}"
```

<span data-ttu-id="39023-114">Es posible especificar un porcentaje (**minimumAttendeePercentage**) para un cuórum y hacer que **findMeetingTimes** devuelva sugerencias solo si está disponible un número mínimo de asistentes, lo que es especialmente útil para reuniones de mayor tamaño.</span><span class="sxs-lookup"><span data-stu-id="39023-114">Especially useful for larger meetings, you can specify a percentage (**minimumAttendeePercentage**) for a quorum and have **findMeetingTimes** return suggestions only if that minimum attendee availability is met.</span></span>

<span data-ttu-id="39023-p105">Si **findMeetingTimes** no puede sugerir un horario de reunión, indica un motivo específico (**emptySuggestionsReason**), como que el organizador o un asistente necesario no están disponibles. Basándose en este valor, se pueden ajustar mejor los parámetros y llamar otra vez a **findMeetingTimes**.</span><span class="sxs-lookup"><span data-stu-id="39023-p105">If **findMeetingTimes** cannot suggest any meeting times, it indicates a specific reason (**emptySuggestionsReason**), such as the organizer or a required attendee not available. Based on this value, you can better adjust the parameters and call **findMeetingTimes** again.</span></span>

><span data-ttu-id="39023-117">**Nota** La acción **findMeetingTimes** en este momento está disponible para buzones profesionales o educativos de Office 365, pero no para los personales, ni los buzones de correo de outlook.com.</span><span class="sxs-lookup"><span data-stu-id="39023-117">**Note** The **findMeetingTimes** action is currently available to Office 365 work or school mailboxes, but not personal, outlook.com mailboxes.</span></span>

## <a name="example"></a><span data-ttu-id="39023-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="39023-118">Example</span></span>

<span data-ttu-id="39023-p106">En el siguiente ejemplo, se muestra cómo utilizar **findMeetingTimes** para devolver las horas posibles para que dos usuarios se reúnan durante un par de horas, teniendo en cuenta la programación profesional y la disponibilidad de los usuarios, y que los asistentes estarán ausentes durante una parte del tiempo. Como solo hay dos usuarios para esta reunión, las sugerencias requieren la asistencia del 100 %. A continuación, se muestra la disponibilidad de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="39023-p106">The following example shows how to use **findMeetingTimes** to return possible times for 2 users to meet for a couple of hours, taking into account the users' free/busy and work schedules, and the attendee being away for part of the time. Because there are only 2 users for this meeting, suggestions require 100% attendance. The following shows the users' free/busy schedule.</span></span>

### <a name="organizers-calendar"></a><span data-ttu-id="39023-122">Calendario del organizador</span><span class="sxs-lookup"><span data-stu-id="39023-122">Organizer's calendar</span></span>

<span data-ttu-id="39023-123">![Calendario profesional del organizador del 17 al 21 de abril que muestra las horas disponibles y ocupadas](./images/findmeetingtimes_organizer_free_busy.jpg "Calendario profesional del organizador del 17 al 21 de abril que muestra las horas disponibles y ocupadas")</span><span class="sxs-lookup"><span data-stu-id="39023-123">![The organizer's work calendar for April 17-21 showing free-busy times](./images/findmeetingtimes_organizer_free_busy.jpg "The organizer's work calendar for April 17-21 showing free-busy times")</span></span>

### <a name="attendees-calendar"></a><span data-ttu-id="39023-124">Calendario de los asistentes</span><span class="sxs-lookup"><span data-stu-id="39023-124">Attendee's calendar</span></span>

<span data-ttu-id="39023-125">![Calendario profesional del asistente del 17 al 21 de abril que muestra las horas disponibles y ocupadas](./images/findmeetingtimes_attendee_free_busy.jpg "Calendario profesional del asistente del 17 al 21 de abril que muestra las horas disponibles y ocupadas")</span><span class="sxs-lookup"><span data-stu-id="39023-125">![The attendee's work calendar for April 17-21 showing free-busy times](./images/findmeetingtimes_attendee_free_busy.jpg "The attendee's work calendar for April 17-21 showing free-busy times")</span></span>

<span data-ttu-id="39023-126">El ejemplo realiza dos llamadas a **findMeetingTimes**:</span><span class="sxs-lookup"><span data-stu-id="39023-126">The example makes 2 calls to **findMeetingTimes**:</span></span>

1. <span data-ttu-id="39023-p107">La primera llamada se busca dentro del intervalo de fechas del 18 al 20 de abril. Cuando el asistente se encuentra fuera de la oficina el 18 o 19 de abril y no hay ningún horario habitual disponible el 20 de abril, la primera llamada no devuelve ninguna sugerencia con el motivo (**emptySuggestionsReason**) de que los asistentes no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="39023-p107">The first call looks in the date range of April 18-20. As the attendee is out-of-office on April 18-19, and there is no commonly available time on April 20, the first call returns no suggestions with the reason (**emptySuggestionsReason**) that attendees are not available.</span></span>
2. <span data-ttu-id="39023-129">La segunda llamada busca la disponibilidad el 21 de abril y devuelve una sugerencia de las 14 a las 16 horas.</span><span class="sxs-lookup"><span data-stu-id="39023-129">The second call looks for availability on April 21 and returns a suggestion of 2-4pm.</span></span>

<span data-ttu-id="39023-p108">Las dos llamadas a **findMeetingTimes** incluyen los siguientes parámetros. Todos los [parámetros](/graph/api/user-findmeetingtimes?view=graph-rest-1.0#request-body) de **findMeetingTimes** son opcionales.</span><span class="sxs-lookup"><span data-stu-id="39023-p108">The two calls to **findMeetingTimes** include the following parameters. All [parameters](/graph/api/user-findmeetingtimes?view=graph-rest-1.0#request-body) for **findMeetingTimes** are optional.</span></span>

- <span data-ttu-id="39023-132">**asistentes**: uno de los asistentes, Naiara Padilla, se establece como `required` de la propiedad **type**</span><span class="sxs-lookup"><span data-stu-id="39023-132">**attendees**: one attendee, Samantha Booth, set as `required` for the **type** property</span></span>
- <span data-ttu-id="39023-133">**locationConstraint**: no se requiere ninguna sugerencia de ubicación</span><span class="sxs-lookup"><span data-stu-id="39023-133">**locationConstraint**: does not require any location suggestion</span></span>
- <span data-ttu-id="39023-134">**timeConstraint**: la primera llamada se busca en el rango de fechas o intervalo horario del 18 de abril a las 9 horas al 20 de abril a las 17 horas; después de que la primera llamada falla al sugerir horarios, la segunda llamada considera el 21 de abril de 9 a 17 horas</span><span class="sxs-lookup"><span data-stu-id="39023-134">**timeConstraint**: the first call looks in the date/time range of April 18, 9am to April 20, 5pm; after the first call fails to suggest any times, the second call looks at April 21, 9am to 5pm</span></span>
- <span data-ttu-id="39023-135">**meetingDuration**: dos horas</span><span class="sxs-lookup"><span data-stu-id="39023-135">**meetingDuration**: two hours</span></span>
- <span data-ttu-id="39023-136">**returnSuggestionReasons**: en este ejemplo se requiere un motivo para cada sugerencia</span><span class="sxs-lookup"><span data-stu-id="39023-136">**returnSuggestionReasons**: this example requires a reason for each suggestion</span></span>
- <span data-ttu-id="39023-137">**minimumAttendeePercentage**: 100 %, dado que el asistente debe poder asistir en cualquier horario sugerido</span><span class="sxs-lookup"><span data-stu-id="39023-137">**minimumAttendeePercentage**: 100%, as the attendee must be able to attend for any suggested time</span></span>

### <a name="first-request"></a><span data-ttu-id="39023-138">Primera solicitud</span><span class="sxs-lookup"><span data-stu-id="39023-138">First request</span></span>

<span data-ttu-id="39023-139">Busque un intervalo de tiempo libre de dos horas para ambos usuarios entre el 18 y el 20 de abril.</span><span class="sxs-lookup"><span data-stu-id="39023-139">Look for a 2-hour free time slot for both users over April 18-20.</span></span>

<!-- {
  "blockType": "ignored",
  "name": "findmeetingtimes_example_first"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/findMeetingTimes
Prefer: outlook.timezone="Pacific Standard Time"
Content-type: application/json

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
    "isRequired": false,  
    "suggestLocation": false,  
    "locations": [ 
      { 
        "resolveAvailability": false,
        "displayName": "Conf room Hood" 
      } 
    ] 
  },  
  "timeConstraint": {
    "activityDomain":"work", 
    "timeslots": [ 
      { 
        "start": { 
          "dateTime": "2017-04-18T09:00:00",  
          "timeZone": "Pacific Standard Time" 
        },  
        "end": { 
          "dateTime": "2017-04-20T17:00:00",  
          "timeZone": "Pacific Standard Time" 
        } 
      } 
    ] 
  },  
  "meetingDuration": "PT2H",
  "returnSuggestionReasons": true,
  "minimumAttendeePercentage": 100
}
```

### <a name="first-response"></a><span data-ttu-id="39023-140">Primera respuesta</span><span class="sxs-lookup"><span data-stu-id="39023-140">First response</span></span>
<span data-ttu-id="39023-141">No hay ningún intervalo de tiempo de dos horas en el horario laboral del 18 al 20 de abril en el que ambos usuarios estén disponibles.</span><span class="sxs-lookup"><span data-stu-id="39023-141">There is no 2-hour time slot during the work hours of April 18-20 when both users are available.</span></span>
<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.meetingTimeSuggestionsResult",
  "isCollection": false
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Preference-Applied: outlook.timezone="Pacific Standard Time"
Content-Length: 184

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#microsoft.graph.meetingTimeSuggestionsResult",
    "emptySuggestionsReason":"AttendeesUnavailable",
    "meetingTimeSuggestions":[

    ]
}
```

### <a name="second-request"></a><span data-ttu-id="39023-142">Segunda solicitud</span><span class="sxs-lookup"><span data-stu-id="39023-142">Second request</span></span>
<span data-ttu-id="39023-143">Busque un intervalo de tiempo de dos horas el 21 de abril.</span><span class="sxs-lookup"><span data-stu-id="39023-143">Look for a 2-hour time slot on April 21.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "findmeetingtimes_example_second"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/findMeetingTimes
Prefer: outlook.timezone="Pacific Standard Time"
Content-type: application/json

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
    "isRequired": false,  
    "suggestLocation": false,  
    "locations": [ 
      { 
        "resolveAvailability": false,
        "displayName": "Conf room Hood" 
      } 
    ] 
  },  
  "timeConstraint": {
    "activityDomain":"work", 
    "timeslots": [ 
      { 
        "start": { 
          "dateTime": "2017-04-21T09:00:00",  
          "timeZone": "Pacific Standard Time" 
        },  
        "end": { 
          "dateTime": "2017-04-21T17:00:00",  
          "timeZone": "Pacific Standard Time" 
        } 
      } 
    ] 
  },  
  "meetingDuration": "PT2H",
  "returnSuggestionReasons": true,
  "minimumAttendeePercentage": 100
}
```

### <a name="second-response"></a><span data-ttu-id="39023-144">Segunda respuesta</span><span class="sxs-lookup"><span data-stu-id="39023-144">Second response</span></span>
<span data-ttu-id="39023-145">La segunda solicitud **findMeetingTimes** sugiere el 21 de abril de las 14 a las 16 horas para que ambos usuarios se reúnan.</span><span class="sxs-lookup"><span data-stu-id="39023-145">The second **findMeetingTimes** request suggests April 21, 2-4pm for both users to meet.</span></span>
<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.meetingTimeSuggestionsResult",
  "isCollection": false
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Preference-Applied: outlook.timezone="Pacific Standard Time"
Content-Length: 714

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
                    "dateTime":"2017-04-21T14:00:00.0000000",
                    "timeZone":"Pacific Standard Time"
                },
                "end":{
                    "dateTime":"2017-04-21T16:00:00.0000000",
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



## <a name="next-steps"></a><span data-ttu-id="39023-146">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="39023-146">Next steps</span></span>

<span data-ttu-id="39023-p109">Hay ocasiones en las que no todos los asistentes pueden asistir a una reunión. Puede hacer que **findMeetingTimes** sugiera una hora si la _seguridad_ de asistencia alcanza un determinado porcentaje al especificar el parámetro opcional **minimumAttendeePercentage**. Obtenga más información acerca de la [seguridad de una sugerencia de reunión](/graph/api/user-findmeetingtimes?view=graph-rest-1.0#the-confidence-of-a-meeting-suggestion) y otros [parámetros](/graph/api/user-findmeetingtimes?view=graph-rest-1.0#request-body) y cómo aplicarlos según corresponda para las reuniones de mayor tamaño.</span><span class="sxs-lookup"><span data-stu-id="39023-p109">There are times when not all attendees can attend a meeting. You can have **findMeetingTimes** suggest a time if the _confidence_ for attendance reaches a certain percentage, by specifying the **minimumAttendeePercentage** optional parameter. Learn more about the [confidence of a meeting suggestion](/graph/api/user-findmeetingtimes?view=graph-rest-1.0#the-confidence-of-a-meeting-suggestion) and other [parameters](/graph/api/user-findmeetingtimes?view=graph-rest-1.0#request-body), and apply them as appropriate for meetings of larger sizes.</span></span>

<span data-ttu-id="39023-150">Después de obtener sugerencias para horas de reunión, le recomendamos que:</span><span class="sxs-lookup"><span data-stu-id="39023-150">After getting meeting time suggestions, you may want to:</span></span>

1. <span data-ttu-id="39023-151">[Cree un evento y lo envíe como una convocatoria de reunión](/graph/api/user-post-events?view=graph-rest-1.0).</span><span class="sxs-lookup"><span data-stu-id="39023-151">[Create an event and send it as a meeting request](/graph/api/user-post-events?view=graph-rest-1.0).</span></span>
2. <span data-ttu-id="39023-152">[Agregue datos adjuntos](/graph/api/event-post-attachments?view=graph-rest-1.0) al evento.</span><span class="sxs-lookup"><span data-stu-id="39023-152">[Add an attachment](/graph/api/event-post-attachments?view=graph-rest-1.0) to the event.</span></span>

<span data-ttu-id="39023-153">Obtenga más información sobre la [integración con el Calendario de Outlook](outlook-calendar-concept-overview.md).</span><span class="sxs-lookup"><span data-stu-id="39023-153">Find out more about [integrating with Outlook calendar](outlook-calendar-concept-overview.md).</span></span>
