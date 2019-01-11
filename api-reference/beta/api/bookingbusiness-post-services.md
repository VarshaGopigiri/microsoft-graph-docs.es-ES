---
title: Crear bookingService
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
ms.openlocfilehash: 73e38c0abfeacb43d3ac7f4e28345ac56becb667
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27814297"
---
# <a name="create-bookingservice"></a>Crear bookingService

 > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.
 
Crear un nuevo [bookingService](../resources/bookingservice.md) para el [bookingbusiness](../resources/bookingbusiness.md)de especificado.
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
POST /bookingBusinesses/{id}/services

```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Descripción|
|:---------------|:----------|
| Autorización  | Portador {código}|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [bookingService](../resources/bookingservice.md) .


## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve `201, Created` objeto de código y [bookingService](../resources/bookingservice.md) de respuesta en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "create_bookingservice_from_bookingbusiness"
}-->
```http
POST https://graph.microsoft.com/beta/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/services
Content-type: application/json

{
    "@odata.type":"#microsoft.graph.bookingService",
    "defaultDuration":"PT1H30M",
    "defaultLocation":{
        "@odata.type":"#microsoft.graph.location",
        "address":{
            "@odata.type":"#microsoft.graph.physicalAddress",
            "city":"Buffalo",
            "countryOrRegion":"USA",
            "postalCode":"98052",
            "postOfficeBox":null,
            "state":"NY",
            "street":"4567 First Street",
            "type@odata.type":"#microsoft.graph.physicalAddressType",
            "type":null
        },
        "coordinates":null,
        "displayName":"Contoso Lunch Delivery",
        "locationEmailAddress":null,
        "locationType@odata.type":"#microsoft.graph.locationType",
        "locationType":null,
        "locationUri":null,
        "uniqueId":null,
        "uniqueIdType@odata.type":"#microsoft.graph.locationUniqueIdType",
        "uniqueIdType":null
    },
    "defaultPrice":10.0,
    "defaultPriceType@odata.type":"#microsoft.graph.bookingPriceType",
    "defaultPriceType":"fixedPrice",
    "defaultReminders@odata.type":"#Collection(microsoft.graph.bookingReminder)",
    "defaultReminders":[
        {
            "@odata.type":"#microsoft.graph.bookingReminder",
            "message":"Please be reminded that this service is tomorrow.",
            "offset":"P1D",
            "recipients@odata.type":"#microsoft.graph.bookingReminderRecipients",
            "recipients":"allAttendees"
        }
    ],
    "description":"Individual bento box lunch delivery",
    "displayName":"Bento",
    "isHiddenFromCustomers":false,
    "notes":"Home-cooked special",
    "postBuffer":"PT10M",
    "preBuffer":"PT5M",
    "schedulingPolicy":{
        "@odata.type":"#microsoft.graph.bookingSchedulingPolicy",
        "allowStaffSelection":true,
        "maximumAdvance":"P10D",
        "minimumLeadTime":"PT10H",
        "sendConfirmationsToOwner":true,
        "timeSlotInterval":"PT1H"
    },
    "staffMemberIds@odata.type":"#Collection(String)",
    "staffMemberIds":[
        "d90d1e8c-5cfe-48cf-a2d5-966267375b6a",
        "2f5f8794-0b29-45b5-b56a-2eb5ff7aa880"
    ]
}
```
En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [bookingService](../resources/bookingservice.md) .
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán desde una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.bookingService"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#bookingBusinesses('Contosolunchdelivery%40M365B489948.onmicrosoft.com')/services/$entity",
    "id": "57da6774-a087-4d69-b0e6-6fb82c339976",
    "displayName": "Bento",
    "defaultDuration": "PT1H30M",
    "defaultPrice": 10,
    "defaultPriceType": "fixedPrice",
    "description": "Individual bento box lunch delivery",
    "isHiddenFromCustomers": false,
    "notes": "Home-cooked special",
    "preBuffer": "PT5M",
    "postBuffer": "PT10M",
    "staffMemberIds": [],
    "defaultLocation": {
        "displayName": "Contoso Lunch Delivery",
        "locationEmailAddress": null,
        "locationUri": "",
        "locationType": null,
        "uniqueId": null,
        "uniqueIdType": null,
        "address": {
            "type": "home",
            "postOfficeBox": "",
            "street": "4567 First Street",
            "city": "Buffalo",
            "state": "NY",
            "countryOrRegion": "USA",
            "postalCode": "98052"
        },
        "coordinates": {
            "altitude": null,
            "latitude": null,
            "longitude": null,
            "accuracy": null,
            "altitudeAccuracy": null
        }
    },
    "defaultReminders": [
        {
            "offset": "P1D",
            "recipients": "allAttendees",
            "message": "Please be reminded that this service is tomorrow."
        }
    ],
    "schedulingPolicy": {
        "timeSlotInterval": "PT1H",
        "minimumLeadTime": "PT10H",
        "maximumAdvance": "P10D",
        "sendConfirmationsToOwner": true,
        "allowStaffSelection": true
    }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create bookingService",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
