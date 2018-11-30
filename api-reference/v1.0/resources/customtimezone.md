---
title: Tipo de recurso customTimeZone
description: Representa una zona horaria en la que la transición del horario de verano a la hora estándar, o viceversa, no es estándar.
ms.openlocfilehash: 36d497e3e6ad52ca5a59f4bc322410ee271e73bf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029920"
---
# <a name="customtimezone-resource-type"></a>Tipo de recurso customTimeZone

Representa una zona horaria en la que la transición del horario de verano a la hora estándar, o viceversa, no es estándar.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
| bias | Edm.Int32 | Diferencia horaria de la zona horaria con respecto a la hora universal coordinada (UTC). Este valor está en minutos.Las zonas horarias que son anteriores a UTC tienen una diferencia positiva; las zonas horarias que son posteriores a UTC tienen una diferencia negativa.|
| daylightOffset | [daylightTimeZoneOffset](daylighttimezoneoffset.md) | Especifica cuándo la zona horaria cambia de la hora estándar al horario de verano. |
| name | string | Nombre de la zona horaria personalizada. |
| standardOffset | [standardTimeZoneOffset](standardtimezoneoffset.md) | Especifica cuándo la zona horaria cambia del horario de verano a la hora estándar. |


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "baseType": "microsoft.graph.timeZoneBase",
  "@odata.type": "microsoft.graph.customTimeZone"
}-->

```json
{
  "bias": "Int32",
  "daylightOffset": {"@odata.type": "microsoft.graph.daylightTimeZoneOffset"},
  "name": "string",
  "standardOffset": {"@odata.type": "microsoft.graph.standardTimeZoneOffset"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "customTimeZone resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->