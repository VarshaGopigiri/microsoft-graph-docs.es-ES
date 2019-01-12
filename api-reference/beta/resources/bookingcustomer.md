---
title: tipo de recurso bookingCustomer
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
author: angelgolfer-ms
ms.prod: bookings
ms.openlocfilehash: b213e4026ee33886c0e56db9790efff09fd8c522
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27925108"
---
# <a name="bookingcustomer-resource-type"></a>tipo de recurso bookingCustomer

 > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.
 
Representa a un cliente de un [bookingBsiness](bookingbusiness.md).


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Clientes de la lista](../api/bookingbusiness-list-customers.md) | colección de [bookingCustomer](bookingcustomer.md) | Obtener una lista de objetos de **bookingCustomer** . |
|[Crear bookingCustomer](../api/bookingbusiness-post-customers.md) | [bookingCustomer](bookingcustomer.md) | Crear un nuevo objeto **bookingCustomer** . |
|[Obtener bookingCustomer](../api/bookingcustomer-get.md) | [bookingCustomer](bookingcustomer.md) |Lea las propiedades y relaciones de un objeto **bookingCustomer** .|
|[Update](../api/bookingcustomer-update.md) | [bookingCustomer](bookingcustomer.md) |Actualizar un objeto **bookingCustomer** . |
|[Delete](../api/bookingcustomer-delete.md) | Ninguno |Eliminar un objeto **bookingCustomer** . |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|displayName|Cadena|El nombre del cliente.|
|emailAddress|Cadena|La dirección SMTP del cliente.|
|id|Cadena| El identificador del cliente. Solo lectura.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.bookingCustomer"
}-->

```json
{
  "displayName": "String",
  "emailAddress": "String",
  "id": "String (identifier)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "bookingCustomer resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
