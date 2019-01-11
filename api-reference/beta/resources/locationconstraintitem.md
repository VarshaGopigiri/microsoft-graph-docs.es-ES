---
title: Tipo de recurso locationConstraintItem
description: Las condiciones establecidas por un cliente para la ubicación de una reunión.
localization_priority: Normal
ms.openlocfilehash: 4c44a97a3ed0d5bcf56204fab1527c7e4b58455d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27874086"
---
# <a name="locationconstraintitem-resource-type"></a>Tipo de recurso locationConstraintItem

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Las condiciones establecidas por un cliente para la ubicación de una reunión.

Derivado de [ubicación](location.md).

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
  
  ],
  "@odata.type": "microsoft.graph.locationConstraintItem"
}-->

```json
{
  "resolveAvailability": true,
  "address": {"@odata.type": "microsoft.graph.physicalAddress"},
  "coordinates": {"@odata.type": "microsoft.graph.outlookGeoCoordinates"},
  "displayName": "string",
  "locationEmailAddress": "string",
  "locationUri": "string"
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
| address | [physicalAddress](physicaladdress.md) |Dirección postal de la ubicación. |
| coordinates | [outlookGeoCoordinates](outlookgeocoordinates.md) | Coordenadas geográficas y elevación de la ubicación. |
| displayName  | String | Nombre asociado a la ubicación.                       |
| locationEmailAddress | Cadena | Dirección de correo electrónico opcional de la ubicación |
| locationUri | String | URI opcional que representa la ubicación. |
| resolveAvailability | Booleano | Si se establece en verdadero y el recurso especificado está ocupado [findMeetingTimes](../api/user-findmeetingtimes.md) buscará otro recurso que esté libre. Si se establece en falso y el recurso especificado está ocupado, **findMeetingTimes** devolverá el recurso mejor puntuado en la caché del usuario sin comprobar que esté libre o no. El valor predeterminado es "true". |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "locationConstraintItem resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
