---
title: Tipo de recurso NamedItem
description: Representa un nombre definido para un rango de celdas o un valor. Los nombres pueden ser objetos primitivos con nombre (como puede verse en el tipo siguiente), un objeto de rango o una referencia a un rango. Este objeto puede usarse para obtener un objeto de rango asociado a nombres.
localization_priority: Normal
ms.openlocfilehash: e413361cc42a0f8f65e23e12d36b49d2c7bcebb3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27883828"
---
# <a name="nameditem-resource-type"></a>Tipo de recurso NamedItem

Representa un nombre definido para un rango de celdas o un valor. Los nombres pueden ser objetos primitivos con nombre (como puede verse en el tipo siguiente), un objeto de rango o una referencia a un rango. Este objeto puede usarse para obtener un objeto de rango asociado a nombres.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Add](../api/nameditem-add.md)|[WorkbookNamedItem](nameditem.md)|Agrega un nuevo nombre a la colección del ámbito especificado.|
|[AddFormulaLocal](../api/nameditem-addformulalocal.md)|[WorkbookNamedItem](nameditem.md)|Agrega un nuevo nombre a la colección del ámbito especificado empleando la configuración regional del usuario para la fórmula.|
|[Get NamedItem](../api/nameditem-get.md) | [WorkbookNamedItem](nameditem.md) |Lee las propiedades y relaciones del objeto namedItem.|
|[Update](../api/nameditem-update.md) | [WorkbookNamedItem](nameditem.md)   |Actualiza el objeto NamedItem. |
|[Range](../api/nameditem-range.md)|[Range](range.md)|Devuelve el objeto de intervalo asociado al nombre. Produce una excepción si el tipo del elemento con nombre no es un intervalo.|
|[List](../api/nameditem-list.md) | Colección de [WorkbookNamedItem](nameditem.md) |Obtiene la colección de objetos namedItem. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|name|string|Nombre del objeto. Solo lectura.|
|comment|string|Representa el comentario asociado a este nombre.|
|scope|string|Indica si el nombre está en el ámbito del libro o de una hoja de cálculo específica. Solo lectura.|
|type|string|Indica qué tipo de referencia está asociado con el nombre. Los valores posibles son: `String`, `Integer`, `Double`, `Boolean`, `Range`. Solo lectura.|
|valor|Json|Representa la fórmula a la que debe hacer referencia el nombre, según su definición. Por ejemplo =Sheet14!$B$2:$H$12, =4.75, etc. Solo lectura.|
|visible|boolean|Especifica si el objeto está visible o no.|

## <a name="relationships"></a>Relaciones
| Relación     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|worksheet|[WorkbookWorksheet](worksheet.md)|Devuelve la hoja de cálculo que tiene como ámbito el elemento con nombre. Solo está disponible si el elemento tiene como ámbito la hoja de cálculo. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookNamedItem"
}-->

```json
{
  "name": "string",
  "comment": "string",
  "scope": "string",
  "type": "string",
  "value": {"@odata.type": "microsoft.graph.Json"},
  "visible": true
  
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "NamedItem resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
