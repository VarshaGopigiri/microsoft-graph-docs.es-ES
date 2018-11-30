---
title: Tipo de recurso physicalAddress
description: Representa la dirección postal de un recurso, como un contacto o un evento.
ms.openlocfilehash: 819240be3eb9a088fde43390fbb1d1d4af1fd30c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089743"
---
# <a name="physicaladdress-resource-type"></a>Tipo de recurso physicalAddress

Representa la dirección postal de un recurso, como un contacto o un evento.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|type|String|El tipo de dirección. Los valores posibles son: `unknown`, `home`, `business` y `other`.|
|postOfficeBox|String|El número de apartado de correos.|
|ciudad|String|Ciudad.|
|countryOrRegion|String|País o región. Se trata de un valor de cadena de formato libre, por ejemplo, "Estados Unidos".|
|postalCode|String|Código postal.|
|state|String|Estado.|
|street|String|Calle.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.physicalAddress"
}-->

```json
{
  "type": "string",
  "postOfficeBox": "string",
  "city": "string",
  "countryOrRegion": "string",
  "postalCode": "string",
  "state": "string",
  "street": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "physicalAddress resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
