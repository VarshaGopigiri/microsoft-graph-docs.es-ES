---
title: tipo de recurso signInLocation
description: Proporciona la ciudad, estado y país o región desde donde ha ocurrido en el inicio de sesión.
ms.openlocfilehash: a3d4f6ca5ec18e70960f45a3da1bb06d51ee1e65
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087242"
---
# <a name="signinlocation-resource-type"></a>tipo de recurso signInLocation
Proporciona la ciudad, estado y país o región desde donde ha ocurrido en el inicio de sesión.



## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|city|String|Proporciona la ciudad donde se originó en el inicio de sesión. Esto se calcula utilizando la información de latitud y longitud de la actividad de inicio de sesión.|
|countryOrRegion|String|Proporciona la información de código de país (código de 2 letras) donde se originó en el inicio de sesión.  Esto se calcula utilizando la información de latitud y longitud de la actividad de inicio de sesión.|
|coordenadas geográficas|[geoCoordinates](geocoordinates.md)|Proporciona la latitud, longitud y altitud donde se originó en el inicio de sesión.|
|estado|String|Proporciona el estado donde se originó en el inicio de sesión. Esto se calcula utilizando la información de latitud y longitud de la actividad de inicio de sesión.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.signInLocation"
}-->

```json
{
  "city": "String",
  "countryOrRegion": "String",
  "geoCoordinates": {"@odata.type": "microsoft.graph.geoCoordinates"},
  "state": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "signInLocation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->