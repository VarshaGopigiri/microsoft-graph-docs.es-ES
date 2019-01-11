---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: ItemActivityStat
localization_priority: Normal
ms.openlocfilehash: d0917d0100d33abee1095e2a7d06a4732d382937
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27854253"
---
# <a name="itemactivitystat-resource-type"></a>tipo de recurso itemActivityStat

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **itemActivityStat** proporciona información acerca de las actividades que tuvieron lugar dentro de un intervalo de tiempo.

## <a name="json-representation"></a>Representación JSON

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "baseType": "microsoft.graph.entity",
  "@type": "microsoft.graph.itemActivityStat",
}-->

```json
{
  "activities": [{"@odata.type": "microsoft.graph.itemActivity"}],
  "incompleteData": {"@odata.type": "microsoft.graph.incompleteData"},
  "isTrending": true,
  "startDateTime": "String (timestamp)",
  "endDateTime": "String (timestamp)",
  "create": {"@odata.type": "microsoft.graph.itemActionStat"},
  "delete": {"@odata.type": "microsoft.graph.itemActionStat"},
  "edit": {"@odata.type": "microsoft.graph.itemActionStat"},
  "move": {"@odata.type": "microsoft.graph.itemActionStat"},
  "access": {"@odata.type": "microsoft.graph.itemActionStat"}
}
```

## <a name="properties"></a>Propiedades

| Propiedad         | Tipo                    | Description
|:-----------------|:------------------------|:----------------------------------------
| incompleteData   | [incompleteData][]      | Indica que las estadísticas de este intervalo están basadas en datos incompletos. Solo lectura.
| isTrending       | Booleano                 | Indica si el elemento es "tendencias". Solo lectura.
| startDateTime    | DateTimeOffset          | Cuando se inicia el intervalo. Solo lectura.
| endDateTime      | DateTimeOffset          | Cuando finaliza el intervalo. Solo lectura.
| create           | [itemActionStat][]      | Estadísticas sobre las acciones de **crear** en este intervalo. Solo lectura.
| edit             | [itemActionStat][]      | Estadísticas sobre las acciones de **Edición** en este intervalo. Solo lectura.
| delete           | [itemActionStat][]      | Estadísticas sobre las acciones de **eliminación** en este intervalo. Solo lectura.
| move             | [itemActionStat][]      | Estadísticas sobre las acciones de **mover** en este intervalo. Solo lectura.
| Access           | [itemActionStat][]      | Estadísticas sobre las acciones de **acceso** en este intervalo. Solo lectura.

[itemActionStat]: itemactionstat.md
[incompleteData]: incompletedata.md

## <a name="relationships"></a>Relaciones

| Nombre de la relación | Tipo                        | Descripción
|:------------------|:----------------------------|:---------------------------
| activities        | Colección [itemActivity][] | Expone la **itemActivities** representado en este recurso **itemActivityStat** .

[itemActivity]: itemactivity.md

## <a name="remarks"></a>Observaciones

<!-- {
  "type": "#page.annotation",
  "description": "The ItemActivityStat object provides information about activities that took place on an item.",
  "keywords": "activities,activity,action,analytics",
  "section": "documentation",
  "tocPath": "Resources/ItemActivityStat"
} -->
