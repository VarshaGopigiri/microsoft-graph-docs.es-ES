---
title: tipo de recurso plannerPlanContext
description: El recurso **plannerPlanContext** representa la relación de una plannerPlan para una experiencia de usuario fuera del organizador. Planes en el organizador pueden se exponen en otras experiencias, como Microsoft Teams, realizar un seguimiento de trabajo en el contexto de esa experiencia.
localization_priority: Normal
ms.openlocfilehash: fb86dc2e6fb16fe4e8c2a77d52b3a03f94a1d08a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27820982"
---
# <a name="plannerplancontext-resource-type"></a>tipo de recurso plannerPlanContext

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **plannerPlanContext** representa la relación de una [plannerPlan](plannerplan.md) para una experiencia de usuario fuera del organizador. Planes en el organizador pueden se exponen en otras experiencias, como Microsoft Teams, realizar un seguimiento de trabajo en el contexto de esa experiencia.
La experiencia de que la entrada de **plannerPlanContext** reresents se puede identificar en función de la propiedad **ownerAppId** :
 - 5e3ce6c0-2b1f-4285-8d4b-75ee78787346: la entrada de contexto pertenece a Microsoft Teams.
 - 00000003-0000-0ff1-CE00-000000000000: la entrada de contexto pertenece a SharePoint.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|associationType|Cadena|Admite valores NULL. Un tipo definido por la aplicación de la asociación entre el [plannerPlan](plannerplan.md) y la aplicación. La aplicación puede utilizar esta información para realizar un seguimiento de los distintos tipos de relaciones en el mismo [plannerPlan](plannerplan.md).|
|createdDateTime|DateTimeOffset|Solo lectura. La fecha y la hora cuando se creó el **plannerPlanContext** . El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|displayNameSegments|Colección String|Los segmentos del nombre de la experiencia del externo. Segmentos representan una estructura jerárquica que permite que otras aplicaciones mostrar la relación.|
|ownerAppId|Cadena|Solo lectura. Identificador de la aplicación que creó el **plannerPlanContext**.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerPlanContext"
}-->

```json
{
  "associationType": "Board",
  "createdDateTime": "2015-10-14T00:57:28.4698344Z",
  "displayNameSegments": [
    "Finance Team",
    "Budget Plans"
  ],
  "ownerAppId": "5e3ce6c0-2b1f-4285-8d4b-75ee78787346"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerPlanContext resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
