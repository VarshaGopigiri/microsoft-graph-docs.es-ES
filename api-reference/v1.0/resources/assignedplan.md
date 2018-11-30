---
title: Tipo de recurso assignedPlan
description: La propiedad **assignedPlans** de la entidad user y la entidad organization es una colección de **provisionedPlan**.
ms.openlocfilehash: 306c485b31189e7693075735ceda0812d3259251
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029594"
---
# <a name="assignedplan-resource-type"></a>Tipo de recurso assignedPlan

La propiedad **assignedPlans** de la entidad [user](user.md) y la entidad [organization](organization.md) es una colección de **provisionedPlan**.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|assignedDateTime|DateTimeOffset|Fecha y hora en que se asignó el plan; por ejemplo: 2013-01-02T19:32:30Z. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|capabilityStatus|String|Por ejemplo, "Habilitado".|
|service|String|Nombre del servicio; por ejemplo, "Exchange".|
|servicePlanId|Guid|GUID que identifica el plan de servicio.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.assignedPlan"
}-->

```json
{
  "assignedDateTime": "String (timestamp)",
  "capabilityStatus": "string",
  "service": "string",
  "servicePlanId": "guid"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "assignedPlan resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
