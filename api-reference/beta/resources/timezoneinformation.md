---
title: Tipo de recurso timeZoneInformation
description: Representa una zona horaria. El formato compatible es Windows, y la autoridad de números asignados de Internet (IANA) hora zona (también conocida como zona horaria de Olson)
ms.openlocfilehash: 5508f20812b8327a068364df7eb33c5072c3512e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086673"
---
# <a name="timezoneinformation-resource-type"></a>Tipo de recurso timeZoneInformation

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa una zona horaria. El formato admitido es Windows y, cuando se corrija el problema conocido actual, también se admitirá el formato de [zona horaria Internet Assigned Numbers Authority (IANA)](https://www.iana.org/time-zones) (también conocida como "zona horaria Olson").

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|alias|string|Identificador de la zona horaria.|
|displayName|string|Cadena de visualización que representa la zona horaria.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.timeZoneInformation"
}-->

```json
{
  "alias": "string",
  "displayName": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "timeZoneInformation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->