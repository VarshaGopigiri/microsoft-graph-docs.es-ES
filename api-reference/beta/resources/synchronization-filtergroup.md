---
title: tipo de recurso filterGroup
description: Define un conjunto de cláusulas que debe cumplir un objeto que deben considerarse en ámbito. Se considera como un objeto en el ámbito del grupo (el grupo se evalúa a `true`) sólo si todas las cláusulas del grupo se evalúan a `true`.
ms.openlocfilehash: d49f7a4364f1d8ce3e1c4daba3bb331cf9a9c001
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089281"
---
# <a name="filtergroup-resource-type"></a>tipo de recurso filterGroup

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Define un conjunto de cláusulas que debe cumplir un objeto que deben considerarse en ámbito. Se considera como un objeto en el ámbito del grupo (el grupo se evalúa a `true`) sólo si todas las cláusulas del grupo se evalúan a `true`.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|cláusulas|colección [filterClause](synchronization-filterclause.md)|Filtrar cláusulas (condiciones) de este grupo. Deben cumplirse todas las cláusulas de un grupo en orden para el grupo de filtro evaluar a `true`.|
|name|String|Nombre legible del grupo de filtro.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.filterGroup"
}-->

```json
{
  "clauses": [{"@odata.type": "microsoft.graph.filterClause"}],
  "name": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "filterGroup resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->