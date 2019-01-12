---
title: tipo de recurso bookingWorkHours
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
author: angelgolfer-ms
ms.prod: bookings
ms.openlocfilehash: af606cf8ea867c040c20db3b4082761b3de69052
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27958477"
---
# <a name="bookingworkhours-resource-type"></a>tipo de recurso bookingWorkHours

 > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.
 
Representa el conjunto de horas de trabajo en un solo día de la semana, para un [bookingBusiness](bookingbusiness.md) o [bookingStaffMember](bookingstaffmember.md).

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
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
