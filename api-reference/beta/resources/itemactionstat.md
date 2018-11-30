---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: ItemActionStat
ms.openlocfilehash: f7e9351bc4a394005cffc712aa444c999a51b363
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089936"
---
# <a name="itemactionstat-resource-type"></a>tipo de recurso itemActionStat

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **itemActionStat** proporciona agregados detalles sobre una acción durante un período de tiempo.

## <a name="json-representation"></a>Representación JSON

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@type": "microsoft.graph.itemActionStat",
}-->

```json
{
  "actionCount": 123,
  "actorCount": 60
}
```

## <a name="properties"></a>Propiedades

| Propiedad    | Tipo  | Descripción
|:------------|:------|:-------------------------------------------------------
| CuentaAcción | Int32 | El número de veces que tuvo lugar la acción. Solo lectura.
| actorCount  | Int32 | El número de distintos actores que realizó la acción. Solo lectura.

<!-- {
  "type": "#page.annotation",
  "description": "The ItemActionStat object provides aggregate details about an action over a period of time.",
  "keywords": "activities,activity,action,analytics",
  "section": "documentation",
  "tocPath": "Resources/ItemActionStat"
} -->
