---
title: tipo de recurso plannerFavoritePlanReferenceCollection
description: " el valor es el objeto plannerFavoritePlanReference."
author: TarkanSevilmis
localization_priority: Normal
ms.openlocfilehash: 933589d455a683598576aa5c83df8bd19e6b553f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27828444"
---
# <a name="plannerfavoriteplanreferencecollection-resource-type"></a>tipo de recurso plannerFavoritePlanReferenceCollection

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **plannerFavoritePlanReferenceCollection** representa la colección de referencias a los planes que están marcadas como un favorito por un usuario. Este recurso es un tipo abierto y forma parte del objeto [plannerUser](planneruser.md) . El nombre de la propiedad en el par de valor de la propiedad es el identificador del plan correspondiente; el valor es el objeto [plannerFavoritePlanReference](plannerfavoriteplanreference.md) .


## <a name="properties"></a>Propiedades
Puede definir las propiedades de este tipo abierto. Los nombres de propiedad son `id` valores de recursos de [plannerPlan](plannerplan.md) y sus valores deben ser [plannerFavoritePlanReference](plannerfavoriteplanreference.md) objetos. Para quitar un elemento en la lista de favoritos, establezca el valor de la propiedad en `null`.


## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerFavoritePlanReferenceCollection"
}-->

```json
{
  "jd8S5gOaFk2S8aWCIAJz42QAAxtD": {
    "@odata.type": "microsoft.graph.plannerFavoritePlanReference",
    "orderHint": "8586866870001551087",
    "planTitle": "Customer reviews"
  },
  "uZWtCtli30CGoWLIWSat1mQAC0ai": {
    "@odata.type": "microsoft.graph.plannerFavoritePlanReference",
    "orderHint": "8586848705198093378",
    "planTitle": "Order Management (December 2017)"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerFavoritePlanReferenceCollection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
