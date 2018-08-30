# <a name="get-freebusy-schedule-for-users-and-resources-preview"></a><span data-ttu-id="5f6c1-101">Obtener el programa sobre la disponibilidad de los usuarios y los recursos (vista previa)</span><span class="sxs-lookup"><span data-stu-id="5f6c1-101">Get free/busy schedule for users and resources (preview)</span></span>

<span data-ttu-id="5f6c1-102">En el entorno laboral o escolar, un escenario común es tratar de averiguar cuándo un usuario está disponible para una reunión, así como examinar la disponibilidad de un grupo, sala o equipo para un período de tiempo.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-102">In a work or school setting, a common scenario is to see when a user is free for meeting, or to browse the availability of a team, room, or equipment for a time period.</span></span>

<span data-ttu-id="5f6c1-103">La acción [getSchedule](../api-reference/beta/api/calendar_getschedule.md) permite obtener la información sobre la disponibilidad de una o más entidades (usuarios, listas de distribución o recursos) para un período de tiempo específico.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-103">The [getSchedule](../api-reference/beta/api/calendar_getschedule.md) action lets you get the availability information of one or more entities - users, distribution lists, or resources - for a specific period of time.</span></span> 

## <a name="example"></a><span data-ttu-id="5f6c1-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5f6c1-104">Example</span></span>

<span data-ttu-id="5f6c1-105">Un ejemplo sencillo es encontrar el programa de disponibilidad de un compañero, Alex, en un día específico, de 9 a. m. a 6 p. m., hora estándar del Pacífico:</span><span class="sxs-lookup"><span data-stu-id="5f6c1-105">A simple example is to find the free/busy schedule of a coworker, Alex, on a specific day, from 9am to 6pm, Pacitfic Standard Time:</span></span>

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

<span data-ttu-id="5f6c1-106">**getSchedule** devuelve dos elementos de programación que coinciden con los eventos existentes en el calendario predeterminado de Alex, y corresponden a las horas de inicio y fin de cada elemento y al estado de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-106">**getSchedule** returns two schedule items that match existing events in Alex' default calendar, showing the start and end times of each event and its free/busy status.</span></span> <span data-ttu-id="5f6c1-107">Se puede asumir que Alex está libre el tiempo restante en esa fecha o intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-107">You can assume Alex is free for the remaining time in that date/time range.</span></span>

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

<span data-ttu-id="5f6c1-108">Además del programa de disponibilidad y del horario laboral de Alex, **getSchedule** también devuelve la **availabilityView** que es una vista combinada de la disponibilidad de Alex para ese día.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-108">Apart from the free/busy schedule and working hours of Alex, **getSchedule** also returns **availabilityView**, which is a merged view of Alex' availability for that day.</span></span> <span data-ttu-id="5f6c1-109">La vista combinada es una cadena que consiste en intervalos de tiempo que cubren el día en cuestión, donde cada franja horaria indica la disponibilidad de Alex mediante la siguiente convención:</span><span class="sxs-lookup"><span data-stu-id="5f6c1-109">The merged view is a string that consists of time slots covering that day, with each time slot indicating Alex' availability using the following convention:</span></span> 

- <span data-ttu-id="5f6c1-110">`0`= libre</span><span class="sxs-lookup"><span data-stu-id="5f6c1-110">`0`= free</span></span>
- <span data-ttu-id="5f6c1-111">`1`= provisional</span><span class="sxs-lookup"><span data-stu-id="5f6c1-111">`1`= tentative</span></span>
- <span data-ttu-id="5f6c1-112">`2`= ocupado</span><span class="sxs-lookup"><span data-stu-id="5f6c1-112">`2`= busy</span></span>
- <span data-ttu-id="5f6c1-113">`3`= fuera de la oficina</span><span class="sxs-lookup"><span data-stu-id="5f6c1-113">`3`= out of office</span></span>
- <span data-ttu-id="5f6c1-114">`4`= trabajando en otro lugar.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-114">`4`= working elsewhere.</span></span> 

<span data-ttu-id="5f6c1-115">De forma predeterminada, la longitud de cada franja horaria es de 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-115">Specifies the length of each time slot in minutes. Default is 30 minutes.</span></span> <span data-ttu-id="5f6c1-116">Este ejemplo utiliza la propiedad **availabilityViewInternal** para personalizar la franja horaria y convertirla en intervalos de 15 minutos.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-116">This example uses the **availabilityViewInterval** property to customize the time slot to be 15 minutes.</span></span>

## <a name="how-is-getschedule-different-from-findmeetingtimes"></a><span data-ttu-id="5f6c1-117">¿En qué se diferencia getSchedule de findMeetingTimes?</span><span class="sxs-lookup"><span data-stu-id="5f6c1-117">How is getSchedule different from findMeetingTimes</span></span>

<span data-ttu-id="5f6c1-118">La acción [findMeetingTimes](../api-reference/v1.0/api/user_findmeetingtimes.md) es similar a **getSchedule** en que ambas leen el estado de la disponibilidad y el horario laboral de un usuario y recursos específicos.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-118">The [findMeetingTimes](../api-reference/v1.0/api/user_findmeetingtimes.md) action is similar to **getSchedule** in that both read the free/busy status and working hours of specified users and resources.</span></span> <span data-ttu-id="5f6c1-119">Sin embargo, las dos acciones difieren significativamente.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-119">The two actions differ in a few major ways.</span></span>

### <a name="application"></a><span data-ttu-id="5f6c1-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5f6c1-120">Application</span></span>

<span data-ttu-id="5f6c1-121">**findMeetingTimes** aplica una lógica de negocios determinada para sugerir horas y ubicaciones para reuniones, tales como:</span><span class="sxs-lookup"><span data-stu-id="5f6c1-121">**findMeetingTimes** applies certain business logic to suggest meeting times and locations, such as:</span></span>

- <span data-ttu-id="5f6c1-122">La asistencia opcional u obligatoria de cada entidad</span><span class="sxs-lookup"><span data-stu-id="5f6c1-122">Optional or mandatory attendance of each entity</span></span>
- <span data-ttu-id="5f6c1-123">La naturaleza de la actividad solicitada para la hora del día</span><span class="sxs-lookup"><span data-stu-id="5f6c1-123">The nature of the requested activity for the time of the day</span></span>
- <span data-ttu-id="5f6c1-124">La asistencia mínima necesaria para que haya quórum en la reunión</span><span class="sxs-lookup"><span data-stu-id="5f6c1-124">The minimum attendance required for a quorum for a meeting</span></span>

<span data-ttu-id="5f6c1-125">Esta acción es adecuada para escenarios que dependen de la [optimización en la reserva de una cita](findmeetingtimes_example.md).</span><span class="sxs-lookup"><span data-stu-id="5f6c1-125">It is appropriate for scenarios that depend on [streamlining appointment booking](findmeetingtimes_example.md).</span></span>

<span data-ttu-id="5f6c1-126">**getSchedule** simplemente devuelve el estado de la disponibilidad de los eventos existentes en cada uno de los calendarios para un período de tiempo determinado y supone que el tiempo restante de este período es tiempo libre.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-126">**getSchedule** simply returns the free/busy status of existing events in each of the requested calendars for a given time period, and assumes the remaining time in that time period tp be free.</span></span> <span data-ttu-id="5f6c1-127">A continuación, puede aplicar más lógica de negocios para utilizar estos datos y completar su escenario.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-127">You would then apply further business logic to make use of this data to complete your scenario.</span></span>

### <a name="app-only-support"></a><span data-ttu-id="5f6c1-128">Compatibilidad solo con la aplicación</span><span class="sxs-lookup"><span data-stu-id="5f6c1-128">App-only support</span></span>

<span data-ttu-id="5f6c1-129">**findmeetingtimes** admite solo escenarios delegados que requieren que un usuario se haya conectado a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-129">**findmeetingtimes** supports only delegated scenarios which require a user to have signed in to the app.</span></span> <span data-ttu-id="5f6c1-130">La aplicación solo lee los eventos en los calendarios a los que pueden acceder los usuarios conectados.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-130">The app can read events in only the calendars that the signed-in user can access.</span></span> <span data-ttu-id="5f6c1-131">Esto puede incluir calendarios que otros usuarios hayan delegado o compartido con el usuario conectado.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-131">This can include calendars that other users have delegated or shared with the signed-in user.</span></span>

<span data-ttu-id="5f6c1-132">**getSchedule** admite tanto los escenarios delegados como exclusivamente de aplicación.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-132">**getSchedule** supports both delegated and app-only scenarios.</span></span> <span data-ttu-id="5f6c1-133">En este último, el administrador permite que la aplicación acceda a todos los calendarios sin un usuario conectado.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-133">In the latter, an administrator consents the app to access all calendars without a signed-in user.</span></span>


### <a name="version-support"></a><span data-ttu-id="5f6c1-134">Compatibilidad con versiones</span><span class="sxs-lookup"><span data-stu-id="5f6c1-134">Version support</span></span>

<span data-ttu-id="5f6c1-135">**findmeetingtimes** está generalmente disponible para todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-135">**findmeetingtimes** is generally available for all apps.</span></span> 

<span data-ttu-id="5f6c1-136">**getSchedule** está actualmente disponible [en estado de versión preliminar](versioning_and_support.md#beta-version) y su uso no es apropiado en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-136">**getSchedule** is currently available [in preview status](versioning_and_support.md#beta-version), and therefore is not appropriate for use in production apps.</span></span>


## <a name="permissions"></a><span data-ttu-id="5f6c1-137">Permisos</span><span class="sxs-lookup"><span data-stu-id="5f6c1-137">Permissions</span></span>
<span data-ttu-id="5f6c1-138">El permiso con menos privilegios necesario para conseguir la información sobre la disponibilidad es Calendar.Read.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-138">The least privileged permission you need to get free/busy information is Calendar.Read.</span></span> <span data-ttu-id="5f6c1-139">Según el escenario de su aplicación, este puede ser concedido por el usuario conectado o el administrador.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-139">Depending on your app scenario, this can be consented by the signed-in user or administrator.</span></span>
<span data-ttu-id="5f6c1-140">Además del estado de disponibilidad y el horario laboral de las entidades solicitadas, **getSchedule** también puede devolver el asunto y la ubicación de un evento, siempre que:</span><span class="sxs-lookup"><span data-stu-id="5f6c1-140">Other than the free/busy status and working hours of requested entities, **getSchedule** can also return the subject and location of an event, provided that:</span></span>

- <span data-ttu-id="5f6c1-141">El evento esté marcado con el nivel de confidencialidad bajo - `normal` o `personal` Y se cumplan una o más de las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="5f6c1-141">If the event is marked with low sensitivity level - `normal` or `personal` AND one or more of the following conditions applies:</span></span>

- <span data-ttu-id="5f6c1-142">La configuración del calendario del usuario solicitado permita que todos los usuarios de la organización vean los títulos y las ubicaciones</span><span class="sxs-lookup"><span data-stu-id="5f6c1-142">The requested user’s calendar settings allow all the users in the organization to view titles and locations</span></span>
- <span data-ttu-id="5f6c1-143">El calendario del usuario solicitado se comparta con el usuario conectado</span><span class="sxs-lookup"><span data-stu-id="5f6c1-143">The requested user’s calendar is shared with the signed-in user</span></span>
- <span data-ttu-id="5f6c1-144">El usuario conectado sea un administrador de la misma organización que el usuario solicitado.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-144">The signed-in user is an administrator of the same organization as the requested user.</span></span>

## <a name="time-zone-representation"></a><span data-ttu-id="5f6c1-145">Representación de la zona horaria</span><span class="sxs-lookup"><span data-stu-id="5f6c1-145">Time zone representation</span></span>
<span data-ttu-id="5f6c1-146">De forma predeterminada, las horas de inicio y final de los elementos del programa devueltos se presentan en UTC.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-146">By default, the start and end times of the returned schedule items are represented in UTC.</span></span> <span data-ttu-id="5f6c1-147">Puede utilizar un encabezado `Prefer` para especificar una zona horaria adecuada para su aplicación.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-147">You can use a `Prefer` header to specify a time zone appropriate for your app.</span></span> <span data-ttu-id="5f6c1-148">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="5f6c1-148">As an example:</span></span> 
```
Prefer: outlook.timezone="Pacific Standard Time"
```

## <a name="limits-and-error-conditions"></a><span data-ttu-id="5f6c1-149">Límites y condiciones de error</span><span class="sxs-lookup"><span data-stu-id="5f6c1-149">Limits and error conditions</span></span>
<span data-ttu-id="5f6c1-150">Tenga en cuenta los siguientes límites y condiciones de error:</span><span class="sxs-lookup"><span data-stu-id="5f6c1-150">Be aware of the following limits and error condition:</span></span>

- <span data-ttu-id="5f6c1-151">**getSchedule** puede admitir la búsqueda de la información de disponibilidad de hasta 20 entidades a la vez.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-151">**getSchedule** can support looking up free/busy information for up to 20 entities at once.</span></span> <span data-ttu-id="5f6c1-152">Este límite se aplica al número de usuarios identificados individualmente o de miembros de una lista de distribución, así como al número de recursos.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-152">This limit applies to the number of users identified individually or as members of a distribution list, and to the number of resources as well.</span></span>
- <span data-ttu-id="5f6c1-153">El período de tiempo para hacer la búsqueda debe ser inferior a 42 días.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-153">The time period to look up must be less than 42 days.</span></span>
- <span data-ttu-id="5f6c1-154">Si **getSchedule** no puede identificar a un usuario o recurso específico, devuelve un único elemento de programa e indica el error.</span><span class="sxs-lookup"><span data-stu-id="5f6c1-154">If **getSchedule** cannot identify a specified user or resource, it returns a single schedule item and indicates the error.</span></span> 

## <a name="see-also"></a><span data-ttu-id="5f6c1-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f6c1-155">See also</span></span>
- [<span data-ttu-id="5f6c1-156">Referencia de permisos</span><span class="sxs-lookup"><span data-stu-id="5f6c1-156">Permissions reference</span></span>](permissions_reference.md#calendars-permissions)
- [<span data-ttu-id="5f6c1-157">Buscar horas posibles para una reunión en el calendario de Outlook</span><span class="sxs-lookup"><span data-stu-id="5f6c1-157">Find possible meeting times on the Outlook calendar</span></span>](findmeetingtimes_example.md)
