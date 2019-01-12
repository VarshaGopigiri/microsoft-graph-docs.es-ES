---
title: Usar la API de reservas de Microsoft en Microsoft Graph
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Priority
author: angelgolfer-ms
ms.prod: bookings
ms.openlocfilehash: 494b13016c20124e1a81f996d332c97c15e46852
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27915735"
---
# <a name="use-the-microsoft-bookings-api-in-microsoft-graph"></a>Usar la API de reservas de Microsoft en Microsoft Graph

 > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.
 
Microsoft Bookings permite a los propietarios de pequeñas empresas administrar reservas de cliente y la información con el programa de instalación mínima. Propietario de una empresa puede crear una o varias empresas, con cada empresa que ofrece un conjunto de servicios. El propietario puede configurar los miembros del personal y especificar los servicios que lleva a cabo en cada miembro del personal. Un cliente puede reservar una cita para un servicio específico en que los negocios en una aplicación móvil o en línea. Las reservas se asegura de que la hora de la cita se mantiene actualizada para el negocio, los miembros del personal y clientes implicado.

Mediante programación, un [bookingBusiness](bookingbusiness.md) de la API de reservas implica los siguientes objetos:
 
- Uno o más objetos [bookingStaffMember](bookingstaffmember.md)
- Uno o más objetos [bookingService](bookingservice.md)
- Un conjunto de instancias de [bookingAppointment](bookingappointment.md)
- Un conjunto de objetos de [bookingCustomer](bookingcustomer.md)

## <a name="using-the-bookings-rest-api"></a>Uso de la API de REST de reservas

Eche un vistazo a través de los siguientes pasos antes de citas de cliente para una empresa de reserva por primera vez. Asegúrese de que proporcionan los [tokens de acceso](/graph/auth-overview) de adecuada para las operaciones correspondientes.

1. Asegúrese de que la empresa tiene una suscripción a [Office 365 Business Premium](https://products.office.com/en-us/business/office-365-business-premium) .
2. Crear un nuevo **bookingBusiness** mediante el envío de una operación de entrada para el conjunto de entidades. Como mínimo, debe especificar un nombre para el nuevo negocio que verán los clientes:<!-- { "blockType": "ignored" } -->
```http
POST https://graph.microsoft.com/beta/bookingBusinesses
Authorization: Bearer {access token}
Content-Type: application/json

{
    "displayName":"Contoso"
}
```
Utilice la propiedad **id** de la nueva **bookingBusiness** devuelto en la respuesta de entrada para continuar para [Personalizar](../api/bookingbusiness-update.md) la configuración del negocio y agregar los miembros del personal y servicios para la empresa.

3. Agregar a los miembros del personal individuales para el negocio:<!-- { "blockType": "ignored" } -->
```http
POST https://graph.microsoft.com/beta/bookingBusinesses/{id}/staffMembers
Authorization: Bearer {access token}
Content-Type: application/json

{
    "displayName":"Dana Swope",
    "emailAddress": "danas@contoso.com",
    "role": "externalGuest"
}
```
4. Definir cada servicio ofrecido por la empresa:<!-- { "blockType": "ignored" } -->
```http
POST https://graph.microsoft.com/beta/bookingBusinesses/{id}/services
Authorization: Bearer {access token}
Content-Type: application/json

{
    "displayName":"Bento"
}
```
5. Publicar la página de programación de la empresa, para permitir que a los clientes y los operadores de empresas iniciar citas de reserva:<!-- { "blockType": "ignored" } -->
```http
POST https://graph.microsoft.com/beta/bookingBusinesses/{id}/publish
Authorization: Bearer {access token}
```

En general, una lista de todas las empresas de reserva en el inquilino de Office 365:<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/beta/bookingBusinesses
Authorization: Bearer {access token}
```

## <a name="common-use-cases"></a>Casos de uso común 

En la siguiente tabla se enumera las operaciones comunes para una empresa de la API de reservas.

| Casos de uso        | Recursos de REST | Consulte también |
|:---------------|:--------|:----------|
| Crear, obtener, actualizar o eliminar una empresa | [bookingBusiness](bookingbusiness.md) | [Métodos de bookingBusiness](bookingbusiness.md#methods) |
| Actualización de la directiva de programación | [bookingSchedulingPolicy](bookingschedulingpolicy.md) | [Actualizar un bookingBusiness](../api/bookingbusiness-update.md) |
| Agregar, obtener, actualizar o eliminar a los miembros del personal | [bookingStaffMember](bookingstaffmember.md) | [Métodos de bookingStaffMember](bookingstaffmember.md#methods)  |
| Agregar, obtener, actualizar o eliminar los servicios | [bookingService](bookingservice.md) | [Métodos de bookingService](bookingservice.md#methods)  |
| Publicar o cancelar la publicación de la página de programación | [bookingBusiness](bookingbusiness.md) | [publicar](../api/bookingbusiness-publish.md) <br> [Cancelar la publicación](../api/bookingbusiness-unpublish.md) |
| Crear, obtener, actualizar, eliminar o cancelar una cita | [bookingAppointment](bookingappointment.md) | [Métodos de bookingAppointment](bookingappointment.md#methods)  |
| Obtener las citas en un intervalo de fechas | [bookingBusiness](bookingbusiness.md) | [Lista reservas calendarView](../api/bookingbusiness-list-calendarview.md) |
| Obtener moneda | [bookingCurrency](bookingcurrency.md) | [Métodos de bookingCurrency](bookingcurrency.md#methods) |


## <a name="see-also"></a>Vea también

- Pruebe la API en el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).
- Vea [cómo algunos de nuestros socios usan Microsoft Graph](https://developer.microsoft.com/graph/graph/examples#partners).
- Obtenga información sobre cómo elegir [los permisos](/graph/permissions-reference) en Microsoft Graph.
