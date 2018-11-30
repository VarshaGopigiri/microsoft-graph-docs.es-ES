---
title: Actualizar bookingappointment
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: fd63d11bf7a33751b6a271c57d0f871b5e6d474f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085676"
---
# <a name="update-bookingappointment"></a>Actualizar bookingappointment

 > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.
 
Actualizar las propiedades de un objeto [bookingAppointment](../resources/bookingappointment.md) en la [bookingbusiness](../resources/bookingbusiness.md)de especificado.
## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) |  BookingsAppointment.ReadWrite.All, Bookings.ReadWrite.All, Bookings.Manage.All   |
|Delegado (cuenta personal de Microsoft) | No admitida.   |
|Aplicación | No admitida.  |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
PATCH /bookingBusinesses/{id}/appointments/{id}
```
## <a name="optional-request-headers"></a>Encabezados de solicitud opcionales
| Nombre       | Descripción|
|:-----------|:-----------|
| Autorización  | Portador {código}|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|customerEmailAddress|String|La dirección SMTP de la [bookingCustomer](../resources/bookingcustomer.md) que se reserva la cita.|
|customerId|String|El identificador de la [bookingCustomer](../resources/bookingcustomer.md) para esta cita. Si no se especifica ningún identificador cuando se crea una cita, a continuación, se crea un nuevo objeto **bookingCustomer** . Una vez establecida, se debe tener en cuenta el **customerId** inmutable.|
|customerLocation|[location](../resources/location.md)|Representa información de ubicación para el [bookingCustomer](../resources/bookingcustomer.md) que se reserva la cita.|
|customerName|String|El nombre del cliente.|
|customerNotes|String|Notas de cliente asociado a esta cita. Puede obtener el valor de sólo lectura cuando este **bookingAppointment** por su identificador. <br> Puede establecer esta propiedad sólo cuando se crea inicialmente una cita con un cliente nuevo. Después de ese momento, el valor se calcula a partir del cliente representado por **CustomerID (IdDeCliente)**.|
|customerPhone|String|Número de teléfono del cliente.|
|duration|Duración|La longitud de la cita, indicada en formato [ISO8601](https://www.iso.org/iso-8601-date-and-time-format.html) . |
|finalización|[dateTimeTimeZone](../resources/datetimetimezone.md)|La fecha, hora y zona horaria que finaliza la cita.|
|invoiceAmount|Doble|La cantidad facturada en la factura.|
|invoiceDate|[dateTimeTimeZone](../resources/datetimetimezone.md)|La fecha, hora y zona horaria de la factura para esta cita.|
|invoiceId|String|El identificador de la factura.|
|invoiceStatus|string| El estado de la factura. Los valores posibles son: `draft`, `reviewing`, `open`, `canceled`, `paid`, `corrective`.|
|invoiceUrl|String|La dirección URL de la factura en Microsoft Bookings.|
|optOutOfCustomerEmail|Booleano|True indica que el [bookingCustomer](../resources/bookingcustomer.md) para esta cita no desea recibir una confirmación para esta cita.|
|postBuffer|Duración|La cantidad de tiempo para reservar tras la finalización de una cita, para limpiar, como ejemplo. El valor se expresa en formato [ISO8601](https://www.iso.org/iso-8601-date-and-time-format.html) . |
|Búfer|Duración|La cantidad de tiempo para reservar antes de que comience la cita, para la preparación, como ejemplo. El valor se expresa en formato [ISO8601](https://www.iso.org/iso-8601-date-and-time-format.html) .|
|precio|Doble|El precio normal para una cita para la [bookingService](../resources/bookingservice.md)de especificado.|
|priceType|string| Configuración para proporcionar flexibilidad para la estructura de precios de servicios. Los valores posibles son: `undefined`, `fixedPrice`, `startingAt`, `hourly`, `free`, `priceVaries`, `callUs` y `notSet`.|
|avisos|colección de [bookingReminder](../resources/bookingreminder.md)|La colección de avisos de cliente enviados para esta cita. El valor de esta propiedad está disponible sólo cuando se lee este **bookingAppointment** por su identificador.|
|selfServiceAppointmentId|String|Un identificador de seguimiento adicional para la cita, si la cita se ha creado directamente por el cliente en la página programación, en lugar de hacerlo por un miembro del personal en el nombre del cliente.|
|serviceId|String|El identificador de la [bookingService](../resources/bookingservice.md) asociadas con esta cita.|
|serviceLocation|[location](../resources/location.md)|La ubicación donde se entrega el servicio.|
|serviceName|String|El nombre de la **bookingService** asociado a esta cita.<br>Esta propiedad es opcional cuando se crea una nueva cita. Si no se especifica, se calcula desde el servicio asociado con la cita por la propiedad **serviceId** .|
|serviceNotes|String|Notas de un [bookingStaffMember](../resources/bookingstaffmember.md). El valor de esta propiedad está disponible sólo cuando se lee este **bookingAppointment** por su identificador.|
|staffMemberIds|Colección String|El identificador de cada [bookingStaffMember](../resources/bookingstaffmember.md) que está programado en esta cita.|
|inicio|[dateTimeTimeZone](../resources/datetimetimezone.md)|La fecha, hora y zona horaria que comienza la cita.|


## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.
## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
En el ejemplo siguiente se cambia la fecha de servicio por un día y actualiza la fecha de la factura.
<!-- {
  "blockType": "request",
  "name": "update_bookingappointment"
}-->
```http
PATCH https://graph.microsoft.com/beta/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/appointments/AAMkADKnAAA=
Content-type: application/json

{
    "@odata.type":"#microsoft.graph.bookingAppointment",
    "end":{
        "@odata.type":"#microsoft.graph.dateTimeTimeZone",
        "dateTime":"2018-05-06T12:30:00.0000000+00:00",
        "timeZone":"UTC"
    },
    "invoiceDate":{
        "@odata.type":"#microsoft.graph.dateTimeTimeZone",
        "dateTime":"2018-05-06T12:30:00.0000000+00:00",
        "timeZone":"UTC"
    },
    "start":{
        "@odata.type":"#microsoft.graph.dateTimeTimeZone",
        "dateTime":"2018-05-06T12:00:00.0000000+00:00",
        "timeZone":"UTC"
    }
}
```
##### <a name="response"></a>Respuesta
Este es un ejemplo de la respuesta.
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update bookingappointment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->