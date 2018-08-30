# <a name="get-freebusy-schedule-for-users-and-resources-preview"></a>Obtener el programa sobre la disponibilidad de los usuarios y los recursos (vista previa)

En el entorno laboral o escolar, un escenario común es tratar de averiguar cuándo un usuario está disponible para una reunión, así como examinar la disponibilidad de un grupo, sala o equipo para un período de tiempo.

La acción [getSchedule](../api-reference/beta/api/calendar_getschedule.md) permite obtener la información sobre la disponibilidad de una o más entidades (usuarios, listas de distribución o recursos) para un período de tiempo específico. 

## <a name="example"></a>Ejemplo

Un ejemplo sencillo es encontrar el programa de disponibilidad de un compañero, Alex, en un día específico, de 9 a. m. a 6 p. m., hora estándar del Pacífico:

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

**getSchedule** devuelve dos elementos de programación que coinciden con los eventos existentes en el calendario predeterminado de Alex, y corresponden a las horas de inicio y fin de cada elemento y al estado de disponibilidad. Se puede asumir que Alex está libre el tiempo restante en esa fecha o intervalo de tiempo.

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

Además del programa de disponibilidad y del horario laboral de Alex, **getSchedule** también devuelve la **availabilityView** que es una vista combinada de la disponibilidad de Alex para ese día. La vista combinada es una cadena que consiste en intervalos de tiempo que cubren el día en cuestión, donde cada franja horaria indica la disponibilidad de Alex mediante la siguiente convención: 

- `0`= libre
- `1`= provisional
- `2`= ocupado
- `3`= fuera de la oficina
- `4`= trabajando en otro lugar. 

De forma predeterminada, la longitud de cada franja horaria es de 30 minutos. Este ejemplo utiliza la propiedad **availabilityViewInternal** para personalizar la franja horaria y convertirla en intervalos de 15 minutos.

## <a name="how-is-getschedule-different-from-findmeetingtimes"></a>¿En qué se diferencia getSchedule de findMeetingTimes?

La acción [findMeetingTimes](../api-reference/v1.0/api/user_findmeetingtimes.md) es similar a **getSchedule** en que ambas leen el estado de la disponibilidad y el horario laboral de un usuario y recursos específicos. Sin embargo, las dos acciones difieren significativamente.

### <a name="application"></a>Aplicación

**findMeetingTimes** aplica una lógica de negocios determinada para sugerir horas y ubicaciones para reuniones, tales como:

- La asistencia opcional u obligatoria de cada entidad
- La naturaleza de la actividad solicitada para la hora del día
- La asistencia mínima necesaria para que haya quórum en la reunión

Esta acción es adecuada para escenarios que dependen de la [optimización en la reserva de una cita](findmeetingtimes_example.md).

**getSchedule** simplemente devuelve el estado de la disponibilidad de los eventos existentes en cada uno de los calendarios para un período de tiempo determinado y supone que el tiempo restante de este período es tiempo libre. A continuación, puede aplicar más lógica de negocios para utilizar estos datos y completar su escenario.

### <a name="app-only-support"></a>Compatibilidad solo con la aplicación

**findmeetingtimes** admite solo escenarios delegados que requieren que un usuario se haya conectado a la aplicación. La aplicación solo lee los eventos en los calendarios a los que pueden acceder los usuarios conectados. Esto puede incluir calendarios que otros usuarios hayan delegado o compartido con el usuario conectado.

**getSchedule** admite tanto los escenarios delegados como exclusivamente de aplicación. En este último, el administrador permite que la aplicación acceda a todos los calendarios sin un usuario conectado.


### <a name="version-support"></a>Compatibilidad con versiones

**findmeetingtimes** está generalmente disponible para todas las aplicaciones. 

**getSchedule** está actualmente disponible [en estado de versión preliminar](versioning_and_support.md#beta-version) y su uso no es apropiado en aplicaciones de producción.


## <a name="permissions"></a>Permisos
El permiso con menos privilegios necesario para conseguir la información sobre la disponibilidad es Calendar.Read. Según el escenario de su aplicación, este puede ser concedido por el usuario conectado o el administrador.
Además del estado de disponibilidad y el horario laboral de las entidades solicitadas, **getSchedule** también puede devolver el asunto y la ubicación de un evento, siempre que:

- El evento esté marcado con el nivel de confidencialidad bajo - `normal` o `personal` Y se cumplan una o más de las siguientes condiciones:

- La configuración del calendario del usuario solicitado permita que todos los usuarios de la organización vean los títulos y las ubicaciones
- El calendario del usuario solicitado se comparta con el usuario conectado
- El usuario conectado sea un administrador de la misma organización que el usuario solicitado.

## <a name="time-zone-representation"></a>Representación de la zona horaria
De forma predeterminada, las horas de inicio y final de los elementos del programa devueltos se presentan en UTC. Puede utilizar un encabezado `Prefer` para especificar una zona horaria adecuada para su aplicación. Por ejemplo: 
```
Prefer: outlook.timezone="Pacific Standard Time"
```

## <a name="limits-and-error-conditions"></a>Límites y condiciones de error
Tenga en cuenta los siguientes límites y condiciones de error:

- **getSchedule** puede admitir la búsqueda de la información de disponibilidad de hasta 20 entidades a la vez. Este límite se aplica al número de usuarios identificados individualmente o de miembros de una lista de distribución, así como al número de recursos.
- El período de tiempo para hacer la búsqueda debe ser inferior a 42 días.
- Si **getSchedule** no puede identificar a un usuario o recurso específico, devuelve un único elemento de programa e indica el error. 

## <a name="see-also"></a>Vea también
- [Referencia de permisos](permissions_reference.md#calendars-permissions)
- [Buscar horas posibles para una reunión en el calendario de Outlook](findmeetingtimes_example.md)
