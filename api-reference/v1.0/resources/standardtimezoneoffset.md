---
title: Tipo de recurso standardTimeZoneOffset
description: Especifica cuándo una zona horaria cambia del horario de verano a la hora estándar.
localization_priority: Normal
ms.openlocfilehash: 5e224865f201041b72fb943bc3a76e8a67f7975a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27875848"
---
# <a name="standardtimezoneoffset-resource-type"></a>Tipo de recurso standardTimeZoneOffset

Especifica cuándo una zona horaria cambia del horario de verano a la hora estándar.

Por ejemplo, si se especifica una zona horaria con las propiedades siguientes:

- **dayOccurrence** es 3.
- **dayOfWeek** es "Domingo".
- **month** es 10.
- **time** es 02:00:00 y **year** es 0. Eso significa que la transición del horario de verano al estándar se produce todos los años a las 2:00 del tercer domingo de octubre.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
| dayOccurrence | Edm.Int32 | Representa la enésima repetición del día de la semana en el que se produce la transición del horario de verano a la hora estándar. |
| dayOfWeek | dayOfWeek | Representa el día de la semana en el que se produce la transición del horario de verano a la hora estándar. |
| month | Edm.Int32 | Representa el mes del año en el que se produce la transición del horario de verano a la hora estándar. |
| time | Edm.TimeOfDay | Representa la hora del día en la que se produce la transición del horario de verano a la hora estándar. |
| year | Edm.Int32 | Representa la frecuencia en términos de años con que se produce el cambio del horario de verano a la hora estándar. Por ejemplo, un valor 0 significa todos los años.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.standardTimeZoneOffset"
}-->

```json
{
  "dayOccurrence": "Int32",
  "dayOfWeek": "string",
  "month": "Int32",
  "time": "TimeOfDay",
  "year": "Int32"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "standardTimeZoneOffset resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
