---
title: Obtener la programación de disponibilidad de usuarios y recursos (versión preliminar)
description: En el trabajo o la escuela, es común querer ver cuándo un usuario está libre para una reunión o mirar la disponibilidad de un equipo, sala o equipamiento durante un período de tiempo.
ms.openlocfilehash: 8a2dd9318bdd806c99d525ee41f46d78d1963b47
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092916"
---
# <a name="get-freebusy-schedule-of-users-and-resources-preview"></a>Obtener la programación de disponibilidad de usuarios y recursos (versión preliminar)

En el trabajo o la escuela, es común querer ver cuándo un usuario está libre para una reunión o mirar la disponibilidad de un equipo, sala o equipamiento durante un período de tiempo.

Con la acción [getSchedule](/graph/api/calendar-getschedule?view=graph-rest-beta) podrá obtener la información de disponibilidad de una o más entidades (usuarios, listas de distribución o recursos) durante un período de tiempo específico. 

## <a name="example"></a>Ejemplo

Un ejemplo sencillo es buscar la programación de disponibilidad de un compañero de trabajo, Miguel, un día concreto, de 9:00 a 18:00 CET:

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

**getSchedule** devuelve dos elementos de programación que coinciden con los eventos existentes en el calendario predeterminado de Miguel, que muestra las horas de inicio y finalización de cada evento y el estado de disponibilidad. Puede suponer que Miguel está disponible durante el tiempo restante en ese intervalo de fecha y hora.

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

Aparte de la programación de disponibilidad y las horas de trabajo de Miguel, **getSchedule** también devuelve **availabilityView**, que es una vista combinada de la disponibilidad de Miguel para ese día. La vista combinada es una cadena formada por franjas temporales relativas a ese día, donde cada intervalo de tiempo indica la disponibilidad de Miguel mediante la convención siguiente: 

- `0`= disponible
- `1`= provisional
- `2`= ocupado
- `3`= fuera de la oficina
- `4`= trabajando en otro sitio. 

De forma predeterminada, cada intervalo de tiempo es de 30 minutos. Este ejemplo usa la propiedad **availabilityViewInterval** para personalizar el intervalo de tiempo y que sea de 15 minutos.

## <a name="how-is-getschedule-different-from-findmeetingtimes"></a>Diferencias entre getSchedule y findMeetingTimes

La acción [findMeetingTimes](/graph/api/user-findmeetingtimes?view=graph-rest-1.0) se parece a **getSchedule** en que ambas leen el estado de disponibilidad y el horario de trabajo de los usuarios y recursos especificados. Las diferencias entre las dos acciones son más obvias.

### <a name="application"></a>Aplicación

**findMeetingTimes** usa determinadas lógicas empresariales para sugerir horas de reunión y ubicaciones, como por ejemplo:

- Asistencia obligatoria u opcional de cada entidad.
- La naturaleza de la actividad solicitada para la hora del día.
- La asistencia mínima necesaria para establecer el quorum de una reunión.

Es adecuado para los escenarios que dependen de [la optimización de la reserva de citas](findmeetingtimes-example.md).

**getSchedule** simplemente devuelve el estado de disponibilidad de los eventos existentes en cada uno de los calendarios solicitados durante un período de tiempo específico y asume que el tiempo restante está libre. Tendría que recurrir a más lógicas empresariales para hacer mejor uso de estos datos y completar el escenario.

### <a name="app-only-support"></a>Compatibilidad solo para la aplicación

**findmeetingtimes** solo admite escenarios delegados que requieren que un usuario haya iniciado sesión en la aplicación. La aplicación solo puede leer eventos en los calendarios a los que tenga acceso el usuario que haya iniciado sesión. Esto puede incluir los calendarios que otros usuarios hayan delegado o compartido con el usuario que ha iniciado sesión.

**getSchedule** admite tanto escenarios delegados como los que son solo para la aplicación. En los segundos, un administrador consiente que la aplicación tenga acceso a todos los calendarios sin que un usuario haya iniciado sesión.


### <a name="version-support"></a>Soporte de versión

**findmeetingtimes** suele estar disponible para todas las aplicaciones. 

**getSchedule** está disponible actualmente [en estado de vista previa](versioning-and-support.md#beta-version)y, por tanto, no es adecuado para su uso en aplicaciones de producción.


## <a name="permissions"></a>Permisos
El permiso con privilegios mínimo que necesita para obtener información de disponibilidad es Calendar.Read. Según el escenario de la aplicación, esto lo puede aprobar el administrador o el usuario que hayan iniciado sesión.
Aparte del estado de disponibilidad y las horas de trabajo de entidades solicitadas, **getSchedule** también puede devolver el asunto y la ubicación de un evento, siempre que

- el evento esté marcado con el nivel de confidencialidad bajo - `normal` o `personal` y se den una o más de las condiciones siguientes:

- la configuración del calendario del usuario solicitado permite que todos los usuarios de la organización vean títulos y ubicaciones;
- el calendario del usuario solicitado se comparte con el usuario que ha iniciado sesión;
- el usuario que ha iniciado sesión es un administrador en la misma organización que el usuario solicitado.

## <a name="time-zone-representation"></a>Representación de zona horaria
De forma predeterminada, las horas de inicio y finalización de los elementos devueltos de programación se representan en UTC. Puede usar un encabezado `Prefer` para especificar la zona horaria correspondiente a la aplicación. Por ejemplo: 
```
Prefer: outlook.timezone="Pacific Standard Time"
```

## <a name="limits-and-error-conditions"></a>Límites y condiciones de error
Tenga en cuenta los siguientes límites y condiciones de error:

- **getSchedule** admite la búsqueda de información de disponibilidad para un máximo de 20 entidades a la vez. Este límite se aplica el número de usuarios identificados de forma individual o como miembros de una lista de distribución, así como al número de recursos.
- El período de tiempo para buscar debe ser menos de 42 días.
- Si **getSchedule** no puede identificar un usuario o recurso específico, devuelve un elemento de programación única e indica el error. 

## <a name="see-also"></a>Vea también
- [Referencia de permisos](permissions-reference.md#calendars-permissions)
- [Buscar horas posibles para una reunión en el Calendario de Outlook](findmeetingtimes-example.md)
