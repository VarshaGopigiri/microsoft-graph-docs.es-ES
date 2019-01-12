---
title: tipo de recurso bookingCurrency
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
author: angelgolfer-ms
ms.prod: bookings
ms.openlocfilehash: 7e2289bfa6c6aac62f12d7321d06caaafbc41f8c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27956006"
---
# <a name="bookingcurrency-resource-type"></a>tipo de recurso bookingCurrency

 > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.
 
Representa una moneda monetaria compatible con un [bookingBusiness](bookingbusiness.md).


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Lista bookingCurrencies](../api/bookingcurrency-list.md) | colección de [bookingCurrency](bookingcurrency.md) |Obtener una lista de objetos de **bookingCurrency** disponibles para una empresa de Microsoft Bookings.|
|[Obtener bookingCurrency](../api/bookingcurrency-get.md) | [bookingCurrency](bookingcurrency.md) |Obtener las propiedades de un objeto **bookingCurrency** .|


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|Cadena| Un código de moneda de 3 caracteres, basado en [ISO 4217](https://www.iso.org/iso-4217-currency-codes.html). Por ejemplo, el código de moneda para el dólar estadounidense es USD, y para el Dólar australiano es AUD. Solo lectura.|
|símbolo|Cadena| El símbolo de moneda. Por ejemplo, el símbolo de moneda para el dólar estadounidense y para el Dólar australiano es $.  |

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.bookingCurrency"
}-->

```json
{
  "id": "String (identifier)",
  "symbol": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "bookingCurrency resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
