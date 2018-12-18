---
title: Obtener la programación de disponibilidad de usuarios y recursos (versión preliminar)
description: En el trabajo o la escuela, es común querer ver cuándo un usuario está libre para una reunión o mirar la disponibilidad de un equipo, sala o equipamiento durante un período de tiempo.
author: angelgolfer-ms
ms.openlocfilehash: 2f201ed552200f7c8dd55b368a504b4eca1e3ba5
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27317762"
---
# <a name="get-freebusy-schedule-of-users-and-resources-preview"></a><span data-ttu-id="2a835-103">Obtener la programación de disponibilidad de usuarios y recursos (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="2a835-103">Get free/busy schedule of users and resources (preview)</span></span>

<span data-ttu-id="2a835-104">En el trabajo o la escuela, es común querer ver cuándo un usuario está libre para una reunión o mirar la disponibilidad de un equipo, sala o equipamiento durante un período de tiempo.</span><span class="sxs-lookup"><span data-stu-id="2a835-104">In a work or school setting, a common scenario is to see when a user is free for meeting, or to browse the availability of a team, room, or equipment for a time period.</span></span>

<span data-ttu-id="2a835-105">Con la acción [getSchedule](/graph/api/calendar-getschedule?view=graph-rest-beta) podrá obtener la información de disponibilidad de una o más entidades (usuarios, listas de distribución o recursos) durante un período de tiempo específico.</span><span class="sxs-lookup"><span data-stu-id="2a835-105">The [getSchedule](/graph/api/calendar-getschedule?view=graph-rest-beta) action lets you get the availability information of one or more entities - users, distribution lists, or resources - for a specific period of time.</span></span> 

## <a name="example"></a><span data-ttu-id="2a835-106">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2a835-106">Example</span></span>

<span data-ttu-id="2a835-107">Un ejemplo sencillo es buscar la programación de disponibilidad de un compañero de trabajo, Miguel, un día concreto, de 9:00 a 18:00 CET:</span><span class="sxs-lookup"><span data-stu-id="2a835-107">A simple example is to find the free/busy schedule of a coworker, Alex, on a specific day, from 9am to 6pm, Pacitfic Standard Time:</span></span>

<!-- {
  "blockType": "ignored",
  "name": "calendar_getSchedule_concept"
}-->
```http
POST https://graph.microsoft.com/beta/me/calendar/getschedule 
Prefer: outlook.timezone="Pacific Standard Time"
Content-Type: application/json

{        
    "Schedules": ["AlexW@contoso.OnMicrosoft.com"],
    "StartTime": {
        "dateTime": "2018-08-06T09:00:00",
        "timeZone": "Pacific Standard Time"
    },
    "EndTime": {
        "dateTime": "2018-08-06T18:00:00",
        "timeZone": "Pacific Standard Time"
    },
    "availabilityViewInterval": "15"
}
```

<span data-ttu-id="2a835-108">**getSchedule** devuelve dos elementos de programación que coinciden con los eventos existentes en el calendario predeterminado de Miguel, que muestra las horas de inicio y finalización de cada evento y el estado de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="2a835-108">**getSchedule** returns two schedule items that match existing events in Alex' default calendar, showing the start and end times of each event and its free/busy status.</span></span> <span data-ttu-id="2a835-109">Puede suponer que Miguel está disponible durante el tiempo restante en ese intervalo de fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="2a835-109">You can assume Alex is free for the remaining time in that date/time range.</span></span>

<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.scheduleInformation",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.scheduleInformation)",
    "value":[
        {
            "scheduleId":"AlexW@contoso.OnMicrosoft.com",
            "availabilityView":"111111002222222200000000000000000000",
            "scheduleItems":[
                {
                    "isPrivate":false,
                    "status":"Tentative",
                    "start":{
                        "dateTime":"2018-08-06T09:00:00.0000000",
                        "timeZone":"Pacific Standard Time"
                    },
                    "end":{
                        "dateTime":"2018-08-06T10:30:00.0000000",
                        "timeZone":"Pacific Standard Time"
                    }
                },
                {
                    "isPrivate":false,
                    "status":"Busy",
                    "start":{
                        "dateTime":"2018-08-06T11:00:00.0000000",
                        "timeZone":"Pacific Standard Time"
                    },
                    "end":{
                        "dateTime":"2018-08-06T13:00:00.0000000",
                        "timeZone":"Pacific Standard Time"
                    }
                }
            ],
            "workingHours":{
                "daysOfWeek":[
                    "monday",
                    "tuesday",
                    "wednesday",
                    "thursday",
                    "friday"
                ],
                "startTime":"08:00:00.0000000",
                "endTime":"17:00:00.0000000",
                "timeZone":{
                    "@odata.type":"#microsoft.graph.customTimeZone",
                    "bias":480,
                    "name":"Customized Time Zone",
                    "standardOffset":{
                        "time":"02:00:00.0000000",
                        "dayOccurrence":1,
                        "dayOfWeek":"sunday",
                        "month":11,
                        "year":0
                    },
                    "daylightOffset":{
                        "daylightBias":-60,
                        "time":"02:00:00.0000000",
                        "dayOccurrence":2,
                        "dayOfWeek":"sunday",
                        "month":3,
                        "year":0
                    }
                }
            }
        }
    ]
}

```

<span data-ttu-id="2a835-110">Aparte de la programación de disponibilidad y las horas de trabajo de Miguel, **getSchedule** también devuelve **availabilityView**, que es una vista combinada de la disponibilidad de Miguel para ese día.</span><span class="sxs-lookup"><span data-stu-id="2a835-110">Apart from the free/busy schedule and working hours of Alex, **getSchedule** also returns **availabilityView**, which is a merged view of Alex' availability for that day.</span></span> <span data-ttu-id="2a835-111">La vista combinada es una cadena formada por franjas temporales relativas a ese día, donde cada intervalo de tiempo indica la disponibilidad de Miguel mediante la convención siguiente:</span><span class="sxs-lookup"><span data-stu-id="2a835-111">The merged view is a string that consists of time slots covering that day, with each time slot indicating Alex' availability using the following convention:</span></span> 

- <span data-ttu-id="2a835-112">`0`= disponible</span><span class="sxs-lookup"><span data-stu-id="2a835-112">`0`= free</span></span>
- <span data-ttu-id="2a835-113">`1`= provisional</span><span class="sxs-lookup"><span data-stu-id="2a835-113">`1`= tentative</span></span>
- <span data-ttu-id="2a835-114">`2`= ocupado</span><span class="sxs-lookup"><span data-stu-id="2a835-114">`2`= busy</span></span>
- <span data-ttu-id="2a835-115">`3`= fuera de la oficina</span><span class="sxs-lookup"><span data-stu-id="2a835-115">`3`= out of office</span></span>
- <span data-ttu-id="2a835-116">`4`= trabajando en otro sitio.</span><span class="sxs-lookup"><span data-stu-id="2a835-116">`4`= working elsewhere.</span></span> 

<span data-ttu-id="2a835-117">De forma predeterminada, cada intervalo de tiempo es de 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="2a835-117">By default, the length of each time slot is 30 minutes.</span></span> <span data-ttu-id="2a835-118">Este ejemplo usa la propiedad **availabilityViewInterval** para personalizar el intervalo de tiempo y que sea de 15 minutos.</span><span class="sxs-lookup"><span data-stu-id="2a835-118">This example uses the **availabilityViewInterval** property to customize the time slot to be 15 minutes.</span></span>

## <a name="how-is-getschedule-different-from-findmeetingtimes"></a><span data-ttu-id="2a835-119">Diferencias entre getSchedule y findMeetingTimes</span><span class="sxs-lookup"><span data-stu-id="2a835-119">How is getSchedule different from findMeetingTimes</span></span>

<span data-ttu-id="2a835-120">La acción [findMeetingTimes](/graph/api/user-findmeetingtimes?view=graph-rest-1.0) se parece a **getSchedule** en que ambas leen el estado de disponibilidad y el horario de trabajo de los usuarios y recursos especificados.</span><span class="sxs-lookup"><span data-stu-id="2a835-120">The [findMeetingTimes](/graph/api/user-findmeetingtimes?view=graph-rest-1.0) action is similar to **getSchedule** in that both read the free/busy status and working hours of specified users and resources.</span></span> <span data-ttu-id="2a835-121">Las diferencias entre las dos acciones son más obvias.</span><span class="sxs-lookup"><span data-stu-id="2a835-121">The two actions differ in a few major ways.</span></span>

### <a name="application"></a><span data-ttu-id="2a835-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2a835-122">Application</span></span>

<span data-ttu-id="2a835-123">**findMeetingTimes** usa determinadas lógicas empresariales para sugerir horas de reunión y ubicaciones, como por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2a835-123">**findMeetingTimes** applies certain business logic to suggest meeting times and locations, such as:</span></span>

- <span data-ttu-id="2a835-124">Asistencia obligatoria u opcional de cada entidad.</span><span class="sxs-lookup"><span data-stu-id="2a835-124">Optional or mandatory attendance of each entity</span></span>
- <span data-ttu-id="2a835-125">La naturaleza de la actividad solicitada para la hora del día.</span><span class="sxs-lookup"><span data-stu-id="2a835-125">The nature of the requested activity for the time of the day</span></span>
- <span data-ttu-id="2a835-126">La asistencia mínima necesaria para establecer el quorum de una reunión.</span><span class="sxs-lookup"><span data-stu-id="2a835-126">The minimum attendance required for a quorum for a meeting</span></span>

<span data-ttu-id="2a835-127">Es adecuado para los escenarios que dependen de [la optimización de la reserva de citas](findmeetingtimes-example.md).</span><span class="sxs-lookup"><span data-stu-id="2a835-127">It is appropriate for scenarios that depend on [streamlining appointment booking](findmeetingtimes-example.md).</span></span>

<span data-ttu-id="2a835-128">**getSchedule** simplemente devuelve el estado de disponibilidad de los eventos existentes en cada uno de los calendarios solicitados durante un período de tiempo específico y asume que el tiempo restante está libre.</span><span class="sxs-lookup"><span data-stu-id="2a835-128">**getSchedule** simply returns the free/busy status of existing events in each of the requested calendars for a given time period, and assumes the remaining time in that time period tp be free.</span></span> <span data-ttu-id="2a835-129">Tendría que recurrir a más lógicas empresariales para hacer mejor uso de estos datos y completar el escenario.</span><span class="sxs-lookup"><span data-stu-id="2a835-129">You would then apply further business logic to make use of this data to complete your scenario.</span></span>

### <a name="app-only-support"></a><span data-ttu-id="2a835-130">Compatibilidad solo para la aplicación</span><span class="sxs-lookup"><span data-stu-id="2a835-130">App-only support</span></span>

<span data-ttu-id="2a835-131">**findmeetingtimes** solo admite escenarios delegados que requieren que un usuario haya iniciado sesión en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2a835-131">**findmeetingtimes** supports only delegated scenarios which require a user to have signed in to the app.</span></span> <span data-ttu-id="2a835-132">La aplicación solo puede leer eventos en los calendarios a los que tenga acceso el usuario que haya iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="2a835-132">The app can read events in only the calendars that the signed-in user can access.</span></span> <span data-ttu-id="2a835-133">Esto puede incluir los calendarios que otros usuarios hayan delegado o compartido con el usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="2a835-133">This can include calendars that other users have delegated or shared with the signed-in user.</span></span>

<span data-ttu-id="2a835-134">**getSchedule** admite tanto escenarios delegados como los que son solo para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2a835-134">**getSchedule** supports both delegated and app-only scenarios.</span></span> <span data-ttu-id="2a835-135">En los segundos, un administrador consiente que la aplicación tenga acceso a todos los calendarios sin que un usuario haya iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="2a835-135">In the latter, an administrator consents the app to access all calendars without a signed-in user.</span></span>


### <a name="version-support"></a><span data-ttu-id="2a835-136">Soporte de versión</span><span class="sxs-lookup"><span data-stu-id="2a835-136">Version support</span></span>

<span data-ttu-id="2a835-137">**findmeetingtimes** suele estar disponible para todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="2a835-137">**findmeetingtimes** is generally available for all apps.</span></span> 

<span data-ttu-id="2a835-138">**getSchedule** está disponible actualmente [en estado de vista previa](versioning-and-support.md#beta-version)y, por tanto, no es adecuado para su uso en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2a835-138">**getSchedule** is currently available [in preview status](versioning-and-support.md#beta-version), and therefore is not appropriate for use in production apps.</span></span>


## <a name="permissions"></a><span data-ttu-id="2a835-139">Permisos</span><span class="sxs-lookup"><span data-stu-id="2a835-139">Permissions</span></span>
<span data-ttu-id="2a835-140">El permiso con privilegios mínimo que necesita para obtener información de disponibilidad es Calendar.Read.</span><span class="sxs-lookup"><span data-stu-id="2a835-140">The least privileged permission you need to get free/busy information is Calendar.Read.</span></span> <span data-ttu-id="2a835-141">Según el escenario de la aplicación, esto lo puede aprobar el administrador o el usuario que hayan iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="2a835-141">Depending on your app scenario, this can be consented by the signed-in user or administrator.</span></span>
<span data-ttu-id="2a835-142">Aparte del estado de disponibilidad y las horas de trabajo de entidades solicitadas, **getSchedule** también puede devolver el asunto y la ubicación de un evento, siempre que</span><span class="sxs-lookup"><span data-stu-id="2a835-142">Other than the free/busy status and working hours of requested entities, **getSchedule** can also return the subject and location of an event, provided that:</span></span>

- <span data-ttu-id="2a835-143">el evento esté marcado con el nivel de confidencialidad bajo - `normal` o `personal` y se den una o más de las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="2a835-143">If the event is marked with low sensitivity level - `normal` or `personal` AND one or more of the following conditions applies:</span></span>

- <span data-ttu-id="2a835-144">la configuración del calendario del usuario solicitado permite que todos los usuarios de la organización vean títulos y ubicaciones;</span><span class="sxs-lookup"><span data-stu-id="2a835-144">The requested user’s calendar settings allow all the users in the organization to view titles and locations</span></span>
- <span data-ttu-id="2a835-145">el calendario del usuario solicitado se comparte con el usuario que ha iniciado sesión;</span><span class="sxs-lookup"><span data-stu-id="2a835-145">The requested user’s calendar is shared with the signed-in user</span></span>
- <span data-ttu-id="2a835-146">el usuario que ha iniciado sesión es un administrador en la misma organización que el usuario solicitado.</span><span class="sxs-lookup"><span data-stu-id="2a835-146">The signed-in user is an administrator of the same organization as the requested user.</span></span>

## <a name="time-zone-representation"></a><span data-ttu-id="2a835-147">Representación de zona horaria</span><span class="sxs-lookup"><span data-stu-id="2a835-147">Time zone representation</span></span>
<span data-ttu-id="2a835-148">De forma predeterminada, las horas de inicio y finalización de los elementos devueltos de programación se representan en UTC.</span><span class="sxs-lookup"><span data-stu-id="2a835-148">By default, the start and end times of the returned schedule items are represented in UTC.</span></span> <span data-ttu-id="2a835-149">Puede usar un encabezado `Prefer` para especificar la zona horaria correspondiente a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2a835-149">You can use a `Prefer` header to specify a time zone appropriate for your app.</span></span> <span data-ttu-id="2a835-150">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2a835-150">As an example:</span></span> 
```
Prefer: outlook.timezone="Pacific Standard Time"
```

## <a name="limits-and-error-conditions"></a><span data-ttu-id="2a835-151">Límites y condiciones de error</span><span class="sxs-lookup"><span data-stu-id="2a835-151">Limits and error conditions</span></span>
<span data-ttu-id="2a835-152">Tenga en cuenta los siguientes límites y condiciones de error:</span><span class="sxs-lookup"><span data-stu-id="2a835-152">Be aware of the following limits and error condition:</span></span>

- <span data-ttu-id="2a835-153">**getSchedule** admite la búsqueda de información de disponibilidad para un máximo de 20 entidades a la vez.</span><span class="sxs-lookup"><span data-stu-id="2a835-153">**getSchedule** can support looking up free/busy information for up to 20 entities at once.</span></span> <span data-ttu-id="2a835-154">Este límite se aplica el número de usuarios identificados de forma individual o como miembros de una lista de distribución, así como al número de recursos.</span><span class="sxs-lookup"><span data-stu-id="2a835-154">This limit applies to the number of users identified individually or as members of a distribution list, and to the number of resources as well.</span></span>
- <span data-ttu-id="2a835-155">El período de tiempo para buscar debe ser menos de 42 días.</span><span class="sxs-lookup"><span data-stu-id="2a835-155">The time period to look up must be less than 42 days.</span></span>
- <span data-ttu-id="2a835-156">Si **getSchedule** no puede identificar un usuario o recurso específico, devuelve un elemento de programación única e indica el error.</span><span class="sxs-lookup"><span data-stu-id="2a835-156">If **getSchedule** cannot identify a specified user or resource, it returns a single schedule item and indicates the error.</span></span> 

## <a name="see-also"></a><span data-ttu-id="2a835-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a835-157">See also</span></span>
- [<span data-ttu-id="2a835-158">Referencia de permisos</span><span class="sxs-lookup"><span data-stu-id="2a835-158">Permissions reference</span></span>](permissions-reference.md#calendars-permissions)
- [<span data-ttu-id="2a835-159">Buscar horas posibles para una reunión en el Calendario de Outlook</span><span class="sxs-lookup"><span data-stu-id="2a835-159">Find possible meeting times on the Outlook calendar</span></span>](findmeetingtimes-example.md)
