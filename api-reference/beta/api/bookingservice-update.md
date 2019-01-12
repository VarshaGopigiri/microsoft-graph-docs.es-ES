---
title: Actualizar bookingservice
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
author: angelgolfer-ms
ms.prod: bookings
ms.openlocfilehash: 6830ebc8fc101c4c9ce60f6157ed6bfdab82748c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27937043"
---
# <a name="update-bookingservice"></a>Actualizar bookingservice

 > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.
 
Actualizar las propiedades de un objeto [bookingService](../resources/bookingservice.md) en la [bookingbusiness](../resources/bookingbusiness.md)de especificado.

Los siguientes son algunos ejemplos que se pueden personalizar para un servicio:
- Precio
- Longitud típica de una cita
- Reminders
- Búfer para configurar antes o terminar después el servicio en cualquier momento
- Parámetros de [programación de directiva](../resources/bookingschedulingpolicy.md) como mínimo de notificación a Libreta o cancelar, y si los clientes pueden seleccionar los miembros del personal específico para una cita.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) |  Bookings.ReadWrite.All, Bookings.Manage.All   |
|Delegado (cuenta personal de Microsoft) | No admitida.   |
|Aplicación | No admitida.  |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
PATCH /bookingBusinesses/{id}/services/{id}
```
## <a name="optional-request-headers"></a>Encabezados de solicitud opcionales
| Nombre       | Descripción|
|:-----------|:-----------|
| Autorización  | Portador {código}|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|defaultDuration|Duración|La longitud predeterminada del servicio, representado en número de días, horas, minutos y segundos. Por ejemplo, P11D23H59M59.999999999999S. |
|defaultLocation|[location](../resources/location.md)|La ubicación física de forma predeterminada para el servicio.|
|defaultPrice|Doble|El precio monetarios predeterminado para el servicio.|
|defaultPriceType|string|Se carga el modo predeterminado en el servicio. Los valores posibles son: `undefined`, `fixedPrice`, `startingAt`, `hourly`, `free`, `priceVaries`, `callUs` y `notSet`.|
|defaultReminders|colección de [bookingReminder](../resources/bookingreminder.md)|Establece el valor predeterminado de avisos para una cita de este servicio. El valor de esta propiedad está disponible sólo cuando se lee este **bookingService** por su identificador.|
|descripción|String|Una descripción de texto para el servicio.|
|displayName|String|Un nombre de servicio.|
|emailAddress|String|Una dirección de correo electrónico|
|id|String| Solo lectura.|
|isHiddenFromCustomers|Booleano|True significa que este servicio no está disponible para los clientes de reserva.|
|notas|String|Obtener información adicional acerca de este servicio.|
|postBuffer|Duración|Finaliza el tiempo de búfer después de una cita para este servicio y antes de la siguiente cita del cliente se puede reservar.|
|Búfer|Duración|El tiempo para poder iniciar una cita para este servicio de búfer.|
|schedulingPolicy|[bookingSchedulingPolicy](../resources/bookingschedulingpolicy.md)|El conjunto de directivas que determinan cómo deben crearse y administrarse citas para este tipo de servicio.|
|staffMemberIds|Colección String|Representa los [miembros del personal](../resources/bookingstaffmember.md) que proporcionar este servicio. |

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No content`. No devuelve nada en el cuerpo de la respuesta.
## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
En el ejemplo siguiente se actualiza la duración del servicio especificado.
<!-- {
  "blockType": "request",
  "name": "update_bookingservice"
}-->
```http
PATCH https://graph.microsoft.com/beta/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/services/57da6774-a087-4d69-b0e6-6fb82c339976
Content-type: application/json

{
    "@odata.type":"#microsoft.graph.bookingService",
    "defaultDuration":"PT30M"
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
  "description": "Update bookingservice",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
