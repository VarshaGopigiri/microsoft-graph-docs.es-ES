---
title: tipo de recurso bookingWorkHours
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
ms.openlocfilehash: 94920287cd7358c68686da2d0969c676e3c481ee
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888959"
---
# <a name="bookingworkhours-resource-type"></a>tipo de recurso bookingWorkHours

 > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.
 
Representa el conjunto de horas de trabajo en un solo día de la semana, para un [bookingBusiness](bookingbusiness.md) o [bookingStaffMember](bookingstaffmember.md).

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|día|Cadena| El día de la semana representado por esta instancia. Los valores posibles son: `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday` y `saturday`.|
|intervalos de tiempo|colección de [bookingWorkTimeSlot](bookingworktimeslot.md)|Una lista de horas de inicio y fin durante un día.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.bookingWorkHours"
}-->

```json
{
  "day": "String",
  "timeSlots": [{"@odata.type": "microsoft.graph.bookingWorkTimeSlot"}]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "bookingWorkHours resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
