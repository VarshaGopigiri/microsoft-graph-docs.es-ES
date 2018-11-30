---
title: Tipo de recurso timeZoneBase
description: Representación básica de una zona horaria.
ms.openlocfilehash: 00e09b064a083aa72316838c213f9c84e1139a19
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089812"
---
# <a name="timezonebase-resource-type"></a>Tipo de recurso timeZoneBase

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representación básica de una zona horaria.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
| name | string | Nombre de una zona horaria. Puede ser un nombre de zona de hora estándar como "hora estándar de Hawái-Aleutianas" o "zona horaria personalizada" para una zona horaria personalizada. |


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.timeZoneBase"
}-->

```json
{
  "name": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "timeZoneBase resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->