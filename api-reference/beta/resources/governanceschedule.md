---
title: tipo de recurso governanceSchedule
description: 'Representa la programación de un governanceRoleAssignmentRequest. Para una solicitud de asignación de rol, la programación controla cuándo se debe realizar la operación de asignación de rol, cuándo se debe detener la asignación de roles y la frecuencia con que realizar la operación de asignación de rol. '
ms.openlocfilehash: 6eff3977aa7806c975f968b8706f2e8c21e5d99e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088205"
---
# <a name="governanceschedule-resource-type"></a>tipo de recurso governanceSchedule

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa la programación de un [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md). Para una solicitud de asignación de rol, la programación controla cuándo se debe realizar la operación de asignación de rol, cuándo se debe detener la asignación de roles y la frecuencia con que realizar la operación de asignación de rol. 



## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|startDateTime|DateTimeOffset|La hora de inicio de la asignación de roles. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|endDateTime|DateTimeOffset|La hora de finalización de la asignación de roles. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. *Nota: si el valor es `null`, indica una asignación permanente.*|
|type|String|Tipo de programación de la asignación de roles. Sólo `Once` es compatible con este momento.
|duration|Duración|La duración de una asignación de roles. Está en formato de un objeto TimeSpan.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.governanceSchedule"
}-->

```json
{
  "duration": "String (timespan)",
  "startDateTime": "String (timestamp)",
  "endDateTime": "String (timestamp)",
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "governanceSchedule",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
