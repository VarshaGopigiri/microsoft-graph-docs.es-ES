---
title: tipo de recurso physicalOfficeAddress
description: Representa la dirección de la empresa de un recurso, como un contacto o un evento.
localization_priority: Normal
ms.openlocfilehash: bd4274e29b2ef0f9e7e8318528d18103be19fabc
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27817790"
---
# <a name="physicalofficeaddress-resource-type"></a>tipo de recurso physicalOfficeAddress

Representa la dirección de la empresa de un recurso, como un contacto de la organización.

## <a name="properties"></a>Propiedades

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|city|String|Ciudad.|
|countryOrRegion|String|País o región. Se trata de un valor de cadena de formato libre, por ejemplo, "Estados Unidos".|
|officeLocation  | Cadena | Ubicación de la oficina como el número de generación de cubos y office para un contacto de la organización.  |
|postalCode|String|Código postal.|
|state|String|Estado.|
|street|String|Calle.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.physicalOfficeAddress"
}-->

```json
{
  "city": "string",
  "countryOrRegion": "string",
  "officeLocation": "string",
  "postalCode": "string",
  "state": "string",
  "street": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "physicalOfficeAddress resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
