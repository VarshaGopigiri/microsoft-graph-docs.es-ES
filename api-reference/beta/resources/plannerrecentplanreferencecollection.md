---
title: tipo de recurso plannerRecentPlanReferenceCollection
description: El recurso **plannerRecentPlanReferenceCollection** representa la colección de referencias a los planes que se han visto recientemente por un usuario. Este recurso es un tipo abierto y forma parte del objeto plannerUser. El nombre de la propiedad es el identificador del plan correspondiente. El valor en el par de valor de la propiedad es el objeto plannerRecentPlanReference.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: 84eaedb2f37aefae32b5efac1e5a4a5dfb38e0d2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27980765"
---
# <a name="plannerrecentplanreferencecollection-resource-type"></a>tipo de recurso plannerRecentPlanReferenceCollection

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **plannerRecentPlanReferenceCollection** representa la colección de referencias a los planes que se han visto recientemente por un usuario. Este recurso es un tipo abierto y forma parte del objeto [plannerUser](planneruser.md) . El nombre de la propiedad es el identificador del plan correspondiente. El valor en el par de valor de la propiedad es el objeto [plannerRecentPlanReference](plannerrecentplanreference.md) .
Adición de referencias nuevo a esta colección se quitan automáticamente las entradas más antiguas cuando el tamaño de la colección supera un valor máximo predeterminado.


## <a name="properties"></a>Propiedades
Puede definir las propiedades de este tipo abierto. Los nombres de propiedad son `id` valores de recursos de [plannerPlan](plannerplan.md) y sus valores deben ser [plannerRecentPlanReference](plannerrecentplanreference.md) objetos. Para quitar un elemento en la lista de favoritos, establezca el valor de la propiedad en `null`.


## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerRecentPlanReferenceCollection"
}-->

```json
{
  "7oTB5aMIAE2rVo-1N-L7RmQAGX2q": {
    "@odata.type": "microsoft.graph.plannerRecentPlanReference",
    "lastAccessedDateTime": "2017-12-02T22:49:46.155Z",
    "planTitle": "Purchase Workflow"
  },
  "iKNMHkk3vEWpSF7F7iZWIGQAAMMw": {
    "@odata.type": "microsoft.graph.plannerRecentPlanReference",
    "lastAccessedDateTime": "2017-12-03T21:59:28.975Z",
    "planTitle": "New Year's Office Party"
  }
}
```



<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerRecentPlanReferenceCollection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
