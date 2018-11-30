---
title: tipo de recurso bookingAppointment
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: d7ae5aa0a8a228bc4453742147ca9c858e093a8a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083538"
---
# <a name="bookingappointment-resource-type"></a>tipo de recurso bookingAppointment

 > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.
 
Representa una cita de atención al cliente para una [bookingService](bookingservice.md), realizado por un conjunto de miembros del personal, proporcionado por una empresa de Microsoft Bookings.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Citas de lista](../api/bookingbusiness-list-appointments.md) |  colección de [bookingAppointment](bookingappointment.md) | Para obtener una lista de objetos de **bookingAppointment** en el especificado [bookingbusiness](../resources/bookingbusiness.md). |
|[Crear bookingAppointment](../api/bookingbusiness-post-appointments.md) |  [bookingAppointment](bookingappointment.md) | Crear un nuevo **bookingAppointment** para el [bookingbusiness](../resources/bookingbusiness.md)de especificado. |
|[Obtener bookingAppointment](../api/bookingappointment-get.md) | [bookingAppointment](bookingappointment.md) |Lea las propiedades y relaciones del objeto **bookingAppointment** .|
|[Update](../api/bookingappointment-update.md) | [bookingAppointment](bookingappointment.md)    |Actualizar un objeto **bookingAppointment** . |
|[Delete](../api/bookingappointment-delete.md) | Ninguno |Eliminar un objeto **bookingAppointment** . |
|[Cancelar](../api/bookingappointment-cancel.md)|Ninguno| Cancelar un objeto **bookingAppointment** .|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|customerEmailAddress|String|La dirección SMTP de la [bookingCustomer](bookingcustomer.md) que se reserva la cita.|
|customerId|String|El identificador de la [bookingCustomer](bookingcustomer.md) para esta cita. Si no se especifica ningún identificador cuando se crea una cita, a continuación, se crea un nuevo objeto **bookingCustomer** . Una vez establecida, se debe tener en cuenta el **customerId** inmutable.|
|customerLocation|[location](location.md)|Representa información de ubicación para el [bookingCustomer](bookingcustomer.md) que se reserva la cita.|
|customerName|String|El nombre del cliente.|
|customerNotes|String|Notas de cliente asociado a esta cita. Puede obtener el valor de sólo lectura cuando este **bookingAppointment** por su identificador. <br> Puede establecer esta propiedad sólo cuando se crea inicialmente una cita con un cliente nuevo. Después de ese momento, el valor se calcula a partir del cliente representado por **CustomerID (IdDeCliente)**.|
|customerPhone|String|Número de teléfono del cliente.|
|duration|Duración|La longitud de la cita, indicada en formato [ISO8601](https://www.iso.org/iso-8601-date-and-time-format.html) . |
|finalización|[dateTimeTimeZone](datetimetimezone.md)|La fecha, hora y zona horaria que finaliza la cita.|
|id|String| El identificador de la **bookingAppointment**. Solo lectura.|
|invoiceAmount|Doble|La cantidad facturada en la factura.|
|invoiceDate|[dateTimeTimeZone](datetimetimezone.md)|La fecha, hora y zona horaria de la factura para esta cita.|
|invoiceId|String|El identificador de la factura.|
|invoiceStatus|string| El estado de la factura. Los valores posibles son: `draft`, `reviewing`, `open`, `canceled`, `paid`, `corrective`.|
|invoiceUrl|String|La dirección URL de la factura en Microsoft Bookings.|
|optOutOfCustomerEmail|Booleano|True indica que el [bookingCustomer](bookingcustomer.md) para esta cita no desea recibir una confirmación para esta cita.|
|postBuffer|Duración|La cantidad de tiempo para reservar tras la finalización de una cita, para limpiar, como ejemplo. El valor se expresa en formato [ISO8601](https://www.iso.org/iso-8601-date-and-time-format.html) . |
|Búfer|Duración|La cantidad de tiempo para reservar antes de que comience la cita, para la preparación, como ejemplo. El valor se expresa en formato [ISO8601](https://www.iso.org/iso-8601-date-and-time-format.html) .|
|precio|Doble|El precio normal para una cita para la [bookingService](bookingservice.md)de especificado.|
|priceType|string| Configuración para proporcionar flexibilidad para la estructura de precios de servicios. Los valores posibles son: `undefined`, `fixedPrice`, `startingAt`, `hourly`, `free`, `priceVaries`, `callUs` y `notSet`.|
|avisos|colección de [bookingReminder](bookingreminder.md)|La colección de avisos de cliente enviados para esta cita. El valor de esta propiedad está disponible sólo cuando se lee este **bookingAppointment** por su identificador.|
|selfServiceAppointmentId|String|Un identificador de seguimiento adicional para la cita, si la cita se ha creado directamente por el cliente en la página programación, en lugar de hacerlo por un miembro del personal en el nombre del cliente.|
|serviceId|String|El identificador de la [bookingService](bookingservice.md) asociadas con esta cita.|
|serviceLocation|[location](location.md)|La ubicación donde se entrega el servicio.|
|serviceName|String|El nombre de la **bookingService** asociado a esta cita.<br>Esta propiedad es opcional cuando se crea una nueva cita. Si no se especifica, se calcula desde el servicio asociado con la cita por la propiedad **serviceId** .|
|serviceNotes|String|Notas de un [bookingStaffMember](bookingstaffmember.md). El valor de esta propiedad está disponible sólo cuando se lee este **bookingAppointment** por su identificador.|
|staffMemberIds|Colección String|El identificador de cada [bookingStaffMember](bookingstaffmember.md) que está programado en esta cita.|
|inicio|[dateTimeTimeZone](datetimetimezone.md)|La fecha, hora y zona horaria que comienza la cita.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.bookingAppointment"
}-->

```json
{
  "customerEmailAddress": "String",
  "customerId": "String",
  "customerLocation": {"@odata.type": "microsoft.graph.location"},
  "customerName": "String",
  "customerNotes": "String",
  "customerPhone": "String",
  "duration": "String (timestamp)",
  "end": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "id": "String (identifier)",
  "invoiceAmount": 1024,
  "invoiceDate": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "invoiceId": "String",
  "invoiceStatus": "string",
  "invoiceUrl": "String",
  "optOutOfCustomerEmail": true,
  "postBuffer": "String (timestamp)",
  "preBuffer": "String (timestamp)",
  "price": 1024,
  "priceType": "string",
  "reminders": [{"@odata.type": "microsoft.graph.bookingReminder"}],
  "selfServiceAppointmentId": "String",
  "serviceId": "String",
  "serviceLocation": {"@odata.type": "microsoft.graph.location"},
  "serviceName": "String",
  "serviceNotes": "String",
  "staffMemberIds": ["String"],
  "start": {"@odata.type": "microsoft.graph.dateTimeTimeZone"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "bookingAppointment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->