---
title: tipo de recurso bookingService
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
ms.openlocfilehash: 63eae84249501426c43ad73326cbf005009753be
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27815445"
---
# <a name="bookingservice-resource-type"></a>tipo de recurso bookingService

 > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.
 
Representa información sobre un determinado servicio proporcionado por un [bookingBusiness](bookingbusiness.md), como el nombre de servicio, precio y el personal que normalmente proporciona dicho servicio.

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Servicios de la lista](../api/bookingbusiness-list-services.md) | colección de [bookingService](bookingservice.md) | Para obtener una lista de objetos de **bookingService** en el especificado [bookingbusiness](../resources/bookingbusiness.md).|
|[Crear bookingService](../api/bookingbusiness-post-services.md) | [bookingService](bookingservice.md) | Crear un **bookingService** para el [bookingbusiness](../resources/bookingbusiness.md)de especificado. |
|[Obtener bookingService](../api/bookingservice-get.md) | [bookingService](bookingservice.md) |Obtener las propiedades y relaciones de un objeto **bookingService** en la [bookingbusiness](../resources/bookingbusiness.md)de especificado.|
|[Update](../api/bookingservice-update.md) | [bookingService](bookingservice.md)    |Actualizar un objeto **bookingService** en la [bookingbusiness](../resources/bookingbusiness.md)de especificado. |
|[Delete](../api/bookingservice-delete.md) | Ninguno |Eliminar un objeto **bookingService** en la [bookingbusiness](../resources/bookingbusiness.md)de especificado. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|defaultDuration|Duración|La longitud predeterminada del servicio, representado en número de días, horas, minutos y segundos. Por ejemplo, P11D23H59M59.999999999999S. |
|defaultLocation|[location](location.md)|La ubicación física de forma predeterminada para el servicio.|
|defaultPrice|Doble|El precio monetarios predeterminado para el servicio.|
|defaultPriceType|string|Se carga el modo predeterminado en el servicio. Los valores posibles son: `undefined`, `fixedPrice`, `startingAt`, `hourly`, `free`, `priceVaries`, `callUs` y `notSet`.|
|defaultReminders|colección de [bookingReminder](bookingreminder.md)|Establece el valor predeterminado de avisos para una cita de este servicio. El valor de esta propiedad está disponible sólo cuando se lee este **bookingService** por su identificador.|
|descripción|Cadena|Una descripción de texto para el servicio.|
|displayName|Cadena|Un nombre de servicio.|
|emailAddress|Cadena|Una dirección de correo electrónico|
|id|Cadena|El identificador de ese servicio, en un formato GUID. Solo lectura.|
|isHiddenFromCustomers|Booleano|True significa que este servicio no está disponible para los clientes de reserva.|
|notas|Cadena|Obtener información adicional acerca de este servicio.|
|postBuffer|Duración|Finaliza el tiempo de búfer después de una cita para este servicio y antes de la siguiente cita del cliente se puede reservar.|
|Búfer|Duración|El tiempo para poder iniciar una cita para este servicio de búfer.|
|schedulingPolicy|[bookingSchedulingPolicy](bookingschedulingpolicy.md)|El conjunto de directivas que determinan cómo deben crearse y administrarse citas para este tipo de servicio.|
|staffMemberIds|Colección String|Representa los [miembros del personal](bookingstaffmember.md) que proporcionar este servicio. |

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.bookingService"
}-->

```json
{
  "defaultDuration": "String (timestamp)",
  "defaultLocation": {"@odata.type": "microsoft.graph.location"},
  "defaultPrice": 1024,
  "defaultPriceType": "string",
  "defaultReminders": [{"@odata.type": "microsoft.graph.bookingReminder"}],
  "description": "String",
  "displayName": "String",
  "emailAddress": "String",
  "id": "String (identifier)",
  "isHiddenFromCustomers": true,
  "notes": "String",
  "postBuffer": "String (timestamp)",
  "preBuffer": "String (timestamp)",
  "schedulingPolicy": {"@odata.type": "microsoft.graph.bookingSchedulingPolicy"},
  "staffMemberIds": ["String"]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "bookingService resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
