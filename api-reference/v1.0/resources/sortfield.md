---
title: Tipo de recurso SortField
description: Representa una condición en una operación de ordenación.
localization_priority: Normal
ms.openlocfilehash: 2c1b9a272fd024455d1297c5f59ca7684283e1a1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27825973"
---
# <a name="sortfield-resource-type"></a>Tipo de recurso SortField

Representa una condición en una operación de ordenación.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|ascending|boolean|Representa si la ordenación se realiza en orden ascendente.|
|color|string|Representa el color que es el destino de la condición si la ordenación se realiza según la fuente o el color de celda.|
|dataOption|string|Representa las opciones de ordenación adicionales para este campo. Los valores posibles son: `Normal`, `TextAsNumber`.|
|Key|int|Representa la columna (o fila, según la orientación de ordenación) en que se encuentra la condición. Se representa como un desplazamiento de la primera columna (o fila).|
|sortOn|string|Representa el tipo de ordenación de esta condición. Los valores posibles son: `Value`, `CellColor`, `FontColor`, `Icon`.|
|icono|[WorkbookIcon](icon.md)|Representa el icono que es el destino de la condición si la ordenación se realiza según el icono de la celda.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "@odata.type": "microsoft.graph.workbookSortField"
}-->

```json
{
  "ascending": true,
  "color": "string",
  "dataOption": "string",
  "key": 1024,
  "sortOn": "string",
  "icon": { "@odata.type": "microsoft.graph.workbookIcon" }
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "SortField resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
