# <a name="microsoft-bookings-api-overview"></a>Información general sobre la API de Microsoft Bookings

Microsoft Bookings proporciona aplicaciones en línea y móviles que hacen que la programación de citas sea simple y eficiente para pequeñas empresas y sus clientes. Las empresas pequeñas que proporcionan sus servicios en forma de cita, como talleres, peluquerías y bufetes de abogados, pueden beneficiarse de tener sus reservas administradas, de forma que se libera tiempo para la tarea más importante: hacer crecer el negocio. Microsoft Bookings está disponible para negocios que tengan una suscripción de Office 365 Empresa Premium.

## <a name="why-integrate-with-microsoft-bookings-using-microsoft-graph"></a>¿Por qué debería realizar la integración con Microsoft Bookings mediante Microsoft Graph?

### <a name="streamline-appointment-booking"></a>Simplificar la reserva de citas
Un operador de una empresa nunca se perderá una reserva de cliente cuando no esté en el teléfono o la empresa esté cerrada. Los clientes pueden [ver los servicios disponibles](../api-reference/beta/api/bookingbusiness_list_services.md) y [reservar citas](../api-reference/beta/api/bookingbusiness_post_appointments.md) en cualquier momento directamente en la página de programación, en el sitio web de empresa o en Facebook. 

Los operadores de empresas pueden tomar reservas en cualquier lugar, en la web o una aplicación móvil, en persona o por teléfono. Pueden [reprogramar](../api-reference/beta//api/bookingappointment_update.md), [cancelar](../api-reference/beta/api/bookingappointment_cancel.md) o [volver a asignar](../api-reference/beta/api/bookingappointment_update.md) una reserva existente a otro miembro del personal disponible. 

### <a name="reduce-no-shows-and-increase-productivity-of-the-staff"></a>Reducir las incomparecencias y aumentar la productividad del personal
Los operadores de empresas pueden especificar [directivas de programación](../api-reference/beta/resources/bookingschedulingpolicy.md) que incluyan avisos mínimos de reservas y cancelaciones y los clientes pueden programar o reprogramar las citas por su cuenta. Las confirmaciones de citas automatizadas y los avisos reducen las incomparecencias y dejan que el personal use mejor sus horas de producción. 

### <a name="manage-customer-information-and-relationships-from-anywhere"></a>Administrar la información de los clientes y las relaciones desde cualquier lugar
Completar una cita automáticamente comprueba si el cliente ya está en la [lista clientes](../api-reference/beta/api/bookingbusiness_list_customers.md) y [agrega](../api-reference/beta/api/bookingbusiness_post_customers.md) el nombre del cliente y su dirección de correo electrónico a la lista, si es necesario. Esto facilita a los operadores de empresa mantenerse en contacto con sus clientes y enviar boletines periódicos u otros materiales promocionales.

### <a name="integrate-with-productivity-and-team-collaboration-services-in-microsoft-graph"></a>Integración con servicios de colaboración de equipo y productividad de Microsoft Graph
Usa el mismo extremo unificado de REST de Microsoft Graph, puede acceder a la API de Bookings y [realizar la integración con lo mejor de Microsoft 365](overview-major-services.md) para admitir escenarios más complejos. Por ejemplo, puede usar [Excel](excel-concept-overview.md#generate-reports-and-analyze-results) para analizar datos financieros de la empresa y realizar un seguimiento de ellos, generar informes profesionales o usar [SharePoint](sharepoint-concept-overview.md) o [Microsoft Teams](teams-concept-overview.md) para mejorar la colaboración en equipo.

## <a name="next-steps"></a>Siguientes pasos

Obtenga más información sobre:

- 
  [Microsoft Bookings](https://support.office.com/es-ES/article/Publish-your-business-calendar-online-with-Microsoft-Bookings-47403d64-a067-4754-9ae9-00157244c27d) y otras [aplicaciones empresariales de Office 365](https://support.office.com/en-us/article/manage-your-business-apps-in-the-business-center-47eca808-cf96-42ba-83e8-55daf18e49dc?ui=en-US&rs=en-US&ad=US).
- [Usar la API de Bookings](../api-reference/beta/resources/booking-api-overview.md) en Microsoft Graph.

