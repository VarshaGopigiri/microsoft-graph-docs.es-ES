---
title: Tipo de recurso SortField
description: Representa una condición en una operación de ordenación.
ms.openlocfilehash: bb5915e9d9637912b97c0425819acd15a6ed40ca
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088903"
---
# <a name="sortfield-resource-type"></a>Tipo de recurso SortField

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa una condición en una operación de ordenación.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|ascending|boolean|Representa si la ordenación se realiza en orden ascendente.|
|color|string|Representa el color que es el destino de la condición si la ordenación se realiza según la fuente o el color de celda.|
|dataOption|string|Representa opciones de ordenación adicionales para este campo. Valores posibles: `Normal`, `TextAsNumber`.|
|Key|int|Representa la columna (o fila, según la orientación de ordenación) en que se encuentra la condición. Se representa como un desplazamiento de la primera columna (o fila).|
|sortOn|string|Representa el tipo de ordenación de esta condición. Valores posibles: `Value`, `CellColor`, `FontColor`, `Icon`.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|icono|[Icon](icon.md)|Representa el icono que es el destino de la condición si la ordenación se realiza según el icono de la celda.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.sortField"
}-->

```json
{
  "ascending": true,
  "color": "string",
  "dataOption": "string",
  "key": 1024,
  "sortOn": "string"
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