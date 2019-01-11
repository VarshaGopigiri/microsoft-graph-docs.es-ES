---
title: tipo de recurso plannerRecentPlanReference
description: 'El recurso **plannerRecentPlanReference** escriba representa una referencia a un plannerPlan que recientemente se ha visto por un usuario. '
localization_priority: Normal
ms.openlocfilehash: 6ac17cd0a99d384cbc1f42e2e0d243c582204101
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805680"
---
# <a name="plannerrecentplanreference-resource-type"></a>tipo de recurso plannerRecentPlanReference

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **plannerRecentPlanReference** escriba representa una referencia a un [plannerPlan](plannerplan.md) que recientemente se ha visto por un usuario. El **plannerRecentPlanReferences** para un usuario se mantienen explícitamente por aplicaciones. Cualquier aplicación que implementa la característica de planes recientes debe registrar cuando el usuario vio por última vez un plan y actualización **plannerRecentPlanReference** entradas en consecuencia.
Aplicaciones deben tener en cuenta que las entradas de **plannerRecentPlanReference** pueden hacer referencia a **plannerPlans** que se eliminan, que ya no se puede obtener acceso el usuario, o que se han actualizado con un título diferente.
Se recomienda que aplicaciones notificar a los usuarios cuando hay discrepancias y mantener actualizadas las entradas.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|lastAccessedDateTime|DateTimeOffset|La fecha y la hora que el plan fue la última vez por el usuario. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|planTitle|Cadena|El título del plan en el momento de ve el usuario lo.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerRecentPlanReference"
}-->

```json
{
  "lastAccessedDateTime": "String (timestamp)",
  "planTitle": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerRecentPlanReference resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
