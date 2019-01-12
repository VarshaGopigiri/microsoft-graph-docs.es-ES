---
title: tipo de recurso plannerPlanContextCollection
description: El recurso **plannerPlanContextCollection** representa la colección de contextos externos al que está vinculado un plan. Este recurso es un tipo abierto y forma parte del objeto plannerPlan. El valor en el par de valor de la propiedad es el objeto plannerPlanContext.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: 3281a7664561ac32c3908ca059209a1b89b4ea7d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27951813"
---
# <a name="plannerplancontextcollection-resource-type"></a>tipo de recurso plannerPlanContextCollection

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.


El recurso **plannerPlanContextCollection** representa la colección de contextos externos al que está vinculado un plan. Este recurso es un tipo abierto y forma parte del objeto [plannerPlan](plannerplan.md) . El valor en el par de valor de la propiedad es el objeto [plannerPlanContext](plannerplancontext.md) .


## <a name="properties"></a>Propiedades
Puede definir las propiedades de este tipo abierto. Los valores de propiedad deben ser distintivo identificador que representa el contexto externo como el nombre de la propiedad. Los valores de propiedad deben ser [plannerPlanContext](plannerplancontext.md) objetos. En función de los requisitos de OData, nombres de propiedad de tipos abiertos no pueden contener los siguientes caracteres: `.`, `:`, `%`, `@`. Estos caracteres que necesite se codifican mediante la codificación de dirección URL. Para quitar un elemento en la lista de favoritos, establezca el valor de la propiedad en `null`.

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerPlanContextCollection"
}-->

```json
{
  "48#19%3Ad128c63941b24733951ea7defd81e550%40thread%2Eskype19%3Ad128c63941b24733951ea7defd81e550%40thread%2Eskype": {
    "@odata.type": "#microsoft.graph.plannerPlanContext",
    "associationType": "Board",
    "createdDateTime": "2015-10-14T00:57:28.4698344Z",
    "displayNameSegments": [
        "Finance Team",
        "Budget Plans"
    ],
    "ownerAppId": "5e3ce6c0-2b1f-4285-8d4b-75ee78787346"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerPlanContextCollection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
