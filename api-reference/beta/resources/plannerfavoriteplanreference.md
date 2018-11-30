---
title: tipo de recurso plannerFavoritePlanReference
description: 'El recurso **plannerFavoritePlanReference** escriba representa una referencia a un plannerPlan que se ha marcado como un favorito por el usuario. '
ms.openlocfilehash: bd399572dfce54ee7e46da6af60eb661484519de
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085012"
---
# <a name="plannerfavoriteplanreference-resource-type"></a>tipo de recurso plannerFavoritePlanReference

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **plannerFavoritePlanReference** escriba representa una referencia a un [plannerPlan](plannerplan.md) que se ha marcado como un favorito por el usuario. Los clientes deben tener en cuenta que las entradas de **plannerFavoritePlanReference** pueden hacer referencia a **plannerPlans** que se eliminan, que ya no se puede obtener acceso el usuario, o que se han actualizado con un título diferente.

Se recomienda que los clientes notificar a los usuarios cuando hay discrepancias y mantener actualizadas las entradas.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|orderHint|String|Sugerencia que se usa para ordenar los elementos de este tipo en una vista de lista. El formato se define en [Using order hints in Planner](planner-order-hint-format.md) (Usar sugerencias de orden en Planner).|
|planTitle|String|Título del plan en el momento en que el usuario marca como favorito.|


## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerFavoritePlanReference"
}-->

```json
{
  "orderHint": "String",
  "planTitle": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerFavoritePlanReference resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
