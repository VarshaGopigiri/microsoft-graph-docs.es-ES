# <a name="outlook-calendar-api-overview"></a>Información general sobre la API de calendario de Outlook

El calendario de Outlook forma parte del centro de mensajería de Outlook en Office 365 que también le permite administrar correos electrónicos y contactos, buscar información sobre los usuarios de la organización, iniciar conversaciones en línea, compartir archivos y colaborar en grupos.

## <a name="why-integrate-with-outlook-calendar"></a>¿Por qué debería realizar la integración con el calendario de Outlook?

### <a name="reach-hundreds-of-millions-of-customers-and-build-rich-scenarios"></a>Llegar a cientos de millones de clientes y crear escenarios enriquecidos

Muchos millones de clientes usan el calendario de Outlook como parte de un concentrador integrado que permite comunicarse de forma eficaz y aumentar la productividad. Pueden programar reuniones, administrar los mensajes de correo electrónico, buscar información sobre los contactos y otros usuarios, e iniciar conversaciones o reuniones en línea en un solo lugar, ya sea en la web, en el móvil o en el escritorio. Microsoft Graph no solo conecta las aplicaciones con el calendario, el correo y los datos de contactos de estos clientes, también permite a las aplicaciones [integrarse con lo mejor de Microsoft 365](overview-major-services.md) y ser compatibles con una amplia variedad de escenarios que mejoran la productividad y la colaboración.

### <a name="automate-appointment-organization-and-calendaring"></a>Automatizar la organización de citas y los calendarios

A los clientes les gusta cómo Outlook les permite organizar su tiempo de trabajo, familiar y de actividades personales. La API de REST de Microsoft Graph mantiene la igualdad con la experiencias del cliente y permite a las aplicaciones crear, administrar y responder a eventos con esa misma naturalidad:

- En Outlook, los clientes pueden crear calendarios individuales para el trabajo, la familia y otros fines y organizarlos en grupos de calendarios. Pueden activar los calendarios gratuitos **Cumpleaños** y **Días festivos** para que les recuerden los cumpleaños de los contactos y los días festivos locales. Pueden agregar calendarios que se adapten a sus intereses, como los calendarios de equipos deportivos y programas de televisión. Los clientes pueden seleccionar y superponer calendarios, para así poder ver sus eventos en la misma vista. A través de la API de calendario, la aplicación puede organizar de forma similar [calendarios](../api-reference/v1.0/resources/calendar.md) en [grupos de calendarios](../api-reference/v1.0/resources/calendargroup.md) e interactuar con los calendarios interesantes como con cualquier otro **calendario** en el buzón del usuario. 

- Los clientes de Outlook pueden aplicar categorías a eventos, mensajes, contactos, tareas y entradas de grupo de forma coherente para mejorar la organización y detección. La API de calendario le permite acceder a [la lista principal de un usuario de categorías y definirla](../api-reference/v1.0/api/outlookuser_post_mastercategories.md), lo que abre las puertas a escenarios creativos adicionales. Por ejemplo, un club deportivo puede organizar un torneo y ofrecer una aplicación que diferencia correos electrónicos y eventos de cada deporte con su propia categoría de color. Para las últimas noticias como cambios imprevistos de calendario, la aplicación también puede establecer la propiedad **importance** de los eventos y mensajes de correo electrónico para avisar a los clientes.

- En una carpeta de calendario, puede [crear](../api-reference/v1.0/api/user_post_events.md) y [actualizar](../api-reference/v1.0/api/event_update.md) [eventos](../api-reference/v1.0/resources/event.md) de instancia única, o [programar y mantener eventos periódicos](outlook-schedule-recurring-events.md). Puede permitir que los clientes respondan a [convocatorias de reunión](../api-reference/v1.0/resources/eventmessage.md) y [pospongan](../api-reference/v1.0/api/event_snoozereminder.md) o [descarten](../api-reference/v1.0/api/event_dismissreminder.md) [avisos](../api-reference/v1.0/resources/reminder.md) con la propiedad de navegación **event** asociada.


### <a name="help-customers-stay-synchronized-and-navigate-their-day"></a>Ayudar a los clientes a mantenerse sincronizados y organizar sus días

La API de calendario permite que los clientes organicen sus días y mejoren la productividad:

<!-- change link to notifications to the concept topic once it's created. In general, try staying in the conceptual level in these overview topics, if conceptual topics are available for the link destination. 
-->

- Puede mantener el almacenamiento local de la aplicación actualizado suscribiéndola a las [notificaciones de cambio](../api-reference/v1.0/resources/webhooks.md) y al [seguimiento de cambios en eventos](delta_query_events.md) en el calendario de un usuario.
- Puede mostrar la agenda del usuario con una [vista de aviso](../api-reference/v1.0/api/user_reminderview.md) ligera. 
- Puede dejar que el usuario [acepte](../api-reference/v1.0/api/event_accept.md) y realice una reunión en línea cómodamente a través de su propiedad **webLink**, que abre la reunión en Outlook en la web.
- Los usuarios también pueden [aceptar provisionalmente](../api-reference/v1.0/api/event_tentativelyaccept.md) o [rechazar](../api-reference/v1.0/api/event_decline.md) una reunión desde cualquier lugar.

### <a name="enhance-collaboration"></a>Mejorar la colaboración

- En Outlook, los clientes pueden compartir los calendarios con otros y conceder permisos para leer, escribir o eliminar contenido de los calendarios. También pueden delegar un calendario para permitir que otro cliente responda a convocatorias de reunión en su nombre. Mediante programación, aunque no puede iniciar una acción de compartir o delegar en nombre de un usuario, puede usar un conjunto de propiedades para comprobar el estado de uso compartido y habilitar escenarios para calendarios compartidos o delegados: **canEdit**, **canShare**, **canViewPrivateItems**, **isShared** y **isSharedWithMe**.
- La API del calendario le permite obtener elementos del calendario del usuario que ha iniciado sesión o de los usuarios que han compartido o delegado sus calendarios con el usuario que ha iniciado sesión. Por ejemplo, si Jorge ha compartido un calendario con Juan o si le ha delegado el acceso, en ese caso los [permisos delegados](permissions_reference.md#delegated-permissions-application-permissions-and-effective-permissions) de Juan le proporcionaría acceso de lectura al calendario compartido de Jorge, así como a su contenido.
- ** Los grupos de Office 365 facilitan a los miembros del grupo colaborar y acceder a las conversaciones del grupo y calendarios directamente en Outlook. Excepto unas pocas diferencias entre los calendarios de grupo y los calendarios de usuario, la API de calendario le permite interactuar con los calendarios de grupo como si fuesen calendarios de usuario. Consulte el recurso [calendar](../api-reference/v1.0/resources/calendar.md) para obtener más información.

** Indica características que se aplican específicamente a los calendarios de Outlook de cuentas profesionales o educativas.


### <a name="schedule-smart"></a>Programar de forma inteligente

Outlook y la API de calendario ofrecen varias ventajas inteligentes para programar eventos:

- A través de la configuración de la aplicación de calendario de Outlook, los clientes pueden habilitar que se agreguen eventos desde los correos electrónicos de forma automática, como reservas de vuelos, hoteles o restaurante, y facturas. Una vez que se han agregado, puede interactuar con estos eventos como si fuesen cualquier otro objeto [event](../api-reference/v1.0/resources/event.md) en el buzón del usuario y crear escenarios creativos en esta funcionalidad de Outlook.
- ** En Outlook, reservar una sala de reuniones es tan fácil como agregar un asistente al **evento**. La API de calendario representa una sala de reuniones como un objeto [emailAddress](../api-reference/v1.0/resources/emailaddress.md). Puede [obtener salas (vista previa)](../api-reference/beta/api/user_findrooms.md) y [obtener listas de salas (vista previa)](../api-reference/beta/api/user_findroomlists.md) que están disponibles en una cuenta empresarial. Para organizar una reunión en una sala específica, puede asignarla a la propiedad **location** del **event**.
- ** Puede [buscar la información de libre/ocupado para los usuarios y recursos (vista previa)](outlook-get-free-busy-schedule.md) para un período de tiempo específico. A continuación, puede usar estos datos para aplicarlos a los distintos escenarios, incluida la planificación de recursos y programación de eventos. 
- ** Si su escenario implica la programación de reuniones en un momento óptimo, puede considerar [utilizar findMeetingTimes para identificar posibles momentos o ubicaciones para reunirarse](findmeetingtimes_example.md). La función [findMeetingTimes](../api-reference/v1.0/api/user_findmeetingtimes.md) considera el estado de disponibilidad de los asistentes y las salas y horas preferidas y otras restricciones que indique. Si el primer intento no devuelve una hora de reunión común, compruebe la razón, ajuste los criterios y llame a **findMeetingTimes** de nuevo.


### <a name="teleconference-across-multiple-locations-and-time-zones"></a>Teleconferencia en varias ubicaciones y zonas horarias

Con la globalización, las reuniones de negocios de hoy en día suelen implicar a asistentes que participan desde diferentes ubicaciones y zonas horarias. Le mostramos cómo puede usar la API de calendario para administrar estas reuniones:

- Por ejemplo en Outlook, los clientes pueden organizar una reunión e incluir a asistentes que se unen desde una sala de conferencias en Seattle, una cafetería en París o una oficina doméstica en China. Mediante programación, la propiedad **locations** del evento, que es una colección de objetos [location](../api-reference/v1.0/resources/location.md), puede reflejar este nivel de detalles en **displayName** y **locationType** para cada **location**. Consulte un [ejemplo](../api-reference/v1.0/api/event_get.md#request-2).
- Outlook proporciona a los clientes la flexibilidad para organizar eventos y especificar una zona horaria para cada una de las horas de inicio y finalización de un evento. Para admitir esta flexibilidad, de forma predeterminada, la API de calendario devuelve las horas de **inicio** y **finalización** de un **evento** en UTC y proporciona las propiedades ** originalStartTimeZone** y **originalEndTimeZone** para indicar las zonas horarias utilizadas cuando se creó el evento. 
- Como alternativa, puede especificar el encabezado `Prefer: outlook.timezone="{time zone name}"` para que una operación de evento GET devuelva la hora de **inicio** y **finalización** en la zona horaria que especifique. El nombre de la zona horaria puede ser uno de los compatibles con Windows, así como los de esta [lista](../api-reference/v1.0/resources/datetimetimezone.md). Vea un [ejemplo](../api-reference/v1.0/api/event_get.md#request-1) del encabezado `Prefer` en uso.


### <a name="take-advantage-of-social-intelligence-and-other-developer-conveniences-in-microsoft-graph"></a>Aprovechar la inteligencia social y otras ventajas de desarrollador de Microsoft Graph

Use la [API de contactos](people_example.md) en Microsoft Graph para conectarse a [datos de contactos](../api-reference/v1.0/resources/person.md) que se basan en los patrones de comunicación y colaboración de un usuario y en las relaciones empresariales. Puede implementar controles como un selector de personas y sugerir a personas relevantes para el usuario al organizar reuniones en nombre del usuario.

Evite sobrecargas de almacenamiento y administración de datos en almacenes de datos de la aplicación externos. Con Microsoft Graph, puede almacenar los datos de la aplicación personalizada como [extensiones abiertas](extensibility_overview.md#open-extensions) en casos de recursos individuales. Si necesita que los datos tengan un tipo, o desea poder compartir el esquema con tipo, puede almacenar los datos de la aplicación personalizada en [extensiones de esquema](extensibility_overview.md#schema-extensions).


## <a name="next-steps"></a>Siguientes pasos

- Seleccione y pruebe consultas de ejemplo de calendario en [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Fevents&version=v1.0).
- Obtenga información sobre:
  - [Buscar horas posibles para una reunión en el Calendario de Outlook](findmeetingtimes_example.md)
  - [Programar citas repetidas como eventos periódicos en Outlook](outlook-schedule-recurring-events.md)
- Eche un vistazo a la referencia [de la API de calendario](../api-reference/v1.0/resources/calendar.md) de Outlook.

<!-- Replace the last item with the calendar API overview when it's published.
-->
