---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: ItemAnalytics
ms.openlocfilehash: b50df7d1fdf67cffd508c3b5891d07c599521c8a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085489"
---
# <a name="itemanalytics-resource-type"></a>tipo de recurso itemAnalytics

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **itemAnalytics** proporciona análisis acerca de las actividades que tuvieron lugar en un elemento. Actualmente, este recurso sólo está disponible en SharePoint y OneDrive para la empresa.

También puede usar la API [getActivitiesByInterval][] para recuperar análisis a través de un intervalo de tiempo personalizado o un intervalo.

>**Nota:** El recurso **itemAnalytics** aún no está disponible en todas las [implementaciones nacionales](/graph/deployments).

## <a name="json-representation"></a>Representación JSON

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@type": "microsoft.graph.itemAnalytics",
  "@type.aka": "oneDrive.analytics"
}-->

```json
{
  "allTime": {"@odata.type": "microsoft.graph.itemActivityStat"},
  "lastSevenDays": {"@odata.type": "microsoft.graph.itemActivityStat"}
}
```

## <a name="properties"></a>Propiedades

| Propiedad      | Tipo                 | Descripción
|:--------------|:---------------------|:--------------------------------------
| allTime       | [itemActivityStat][] | Análisis a través de la vida útil del elemento.
| lastSevenDays | [itemActivityStat][] | Análisis de los últimos siete días.

[itemActivityStat]: itemactivitystat.md


[getActivitiesByInterval]: ../api/itemactivity-getbyinterval.md

<!-- {
  "type": "#page.annotation",
  "description": "The ItemAnalytics object provides analytics about activities that took place on an item.",
  "keywords": "activities,activity,action,analytics",
  "section": "documentation",
  "tocPath": "Resources/ItemAnalytics"
} -->
