---
title: Información general sobre la API de Microsoft Bookings
description: 'Microsoft Bookings proporciona aplicaciones en línea y móviles que hacen que la programación de citas sea simple y eficiente para pequeñas empresas y sus clientes. Las empresas pequeñas que proporcionan sus servicios en forma de cita, como talleres, peluquerías y bufetes de abogados, pueden beneficiarse de tener sus reservas administradas, de forma que se libera tiempo para la tarea más importante: hacer crecer el negocio. Microsoft Bookings está disponible para negocios que tengan una suscripción de Office 365 Empresa Premium.'
ms.openlocfilehash: 334b26b5f02e7060b0fddfe8264e138e9d3a2bdc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092898"
---
# <a name="microsoft-bookings-api-overview-preview"></a>Información general sobre la API de Microsoft Bookings

Microsoft Bookings proporciona aplicaciones en línea y móviles que hacen que la programación de citas sea simple y eficiente para pequeñas empresas y sus clientes. Las empresas pequeñas que proporcionan sus servicios en forma de cita, como talleres, peluquerías y bufetes de abogados, pueden beneficiarse de tener sus reservas administradas, de forma que se libera tiempo para la tarea más importante: hacer crecer el negocio. Microsoft Bookings está disponible para negocios que tengan una suscripción de Office 365 Empresa Premium.

## <a name="why-integrate-with-microsoft-bookings-using-microsoft-graph"></a>¿Por qué debería realizar la integración con Microsoft Bookings mediante Microsoft Graph?

### <a name="streamline-appointment-booking"></a>Simplificar la reserva de citas
Un operador de una empresa nunca se perderá una reserva de cliente cuando no esté en el teléfono o la empresa esté cerrada. Los clientes pueden [ver los servicios disponibles](/graph/api/bookingbusiness-list-services?view=graph-rest-beta) y [reservar citas](/graph/api/bookingbusiness-post-appointments?view=graph-rest-beta) en cualquier momento directamente en la página de programación, en el sitio web de empresa o en Facebook. 

Los operadores de empresas pueden tomar reservas en cualquier lugar, en la web o una aplicación móvil, en persona o por teléfono. Pueden [reprogramar](/graph/api/bookingappointment-update?view=graph-rest-beta), [cancelar](/graph/api/bookingappointment-cancel?view=graph-rest-beta) o [volver a asignar](/graph/api/bookingappointment-update?view=graph-rest-beta) una reserva existente a otro miembro del personal disponible. 

### <a name="reduce-no-shows-and-increase-productivity-of-the-staff"></a>Reducir las incomparecencias y aumentar la productividad del personal
Los operadores de empresas pueden especificar [directivas de programación](/graph/api/resources/bookingschedulingpolicy?view=graph-rest-beta) que incluyan avisos mínimos de reservas y cancelaciones y los clientes pueden programar o reprogramar las citas por su cuenta. Las confirmaciones de citas automatizadas y los avisos reducen las incomparecencias y dejan que el personal use mejor sus horas de producción. 

### <a name="manage-customer-information-and-relationships-from-anywhere"></a>Administrar la información de los clientes y las relaciones desde cualquier lugar
Completar una cita automáticamente comprueba si el cliente ya está en la [lista clientes](/graph/api/bookingbusiness-list-customers?view=graph-rest-beta) y [agrega](/graph/api/bookingbusiness-post-customers?view=graph-rest-beta) el nombre del cliente y su dirección de correo electrónico a la lista, si es necesario. Esto facilita a los operadores de empresa mantenerse en contacto con sus clientes y enviar boletines periódicos u otros materiales promocionales.

### <a name="integrate-with-productivity-and-team-collaboration-services-in-microsoft-graph"></a>Integración con servicios de colaboración de equipo y productividad de Microsoft Graph
Usa el mismo extremo unificado de REST de Microsoft Graph, puede acceder a la API de Bookings y [realizar la integración con lo mejor de Microsoft 365](overview-major-services.md) para admitir escenarios más complejos. Por ejemplo, puede usar [Excel](excel-concept-overview.md#generate-reports-and-analyze-results) para analizar datos financieros de la empresa y realizar un seguimiento de ellos, generar informes profesionales o usar [SharePoint](sharepoint-concept-overview.md) o [Microsoft Teams](teams-concept-overview.md) para mejorar la colaboración en equipo.

## <a name="api-reference"></a>Referencia de la API
¿Busca la referencia de la API para este servicio?

Vea la [API de Microsoft Bookings en Microsoft Graph beta](/graph/api/resources/booking-api-overview?view=graph-rest-beta).


## <a name="next-steps"></a>Pasos siguientes

Obtenga más información sobre:

- 
  [Microsoft Bookings](https://support.office.com/es-ES/article/Publish-your-business-calendar-online-with-Microsoft-Bookings-47403d64-a067-4754-9ae9-00157244c27d) y otras [aplicaciones empresariales de Office 365](https://support.office.com/es-ES/article/manage-your-business-apps-in-the-business-center-47eca808-cf96-42ba-83e8-55daf18e49dc?ui=en-US&rs=en-US&ad=US).
- [Usar la API de Bookings](/graph/api/resources/booking-api-overview?view=graph-rest-beta) en Microsoft Graph.

