---
title: tipo de recurso bookingCustomer
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: 1eef44dfe994238d654a21c5f26ec102dcf1881d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084198"
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
|displayName|String|El nombre del cliente.|
|emailAddress|String|La dirección SMTP del cliente.|
|id|String| El identificador del cliente. Solo lectura.|

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