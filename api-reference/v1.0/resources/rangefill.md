---
title: Tipo de recurso RangeFill
description: Representa el fondo de un objeto de rango.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 75aa4bd91ad6f1038fdc42460c6a3c9ab928a09d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27911822"
---
# <a name="rangefill-resource-type"></a>Tipo de recurso RangeFill

Representa el fondo de un objeto de rango.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get RangeFill](../api/rangefill-get.md) | [WorkbookRangeFill](rangefill.md) |Lee las propiedades y relaciones del objeto rangeFill.|
|[Update](../api/rangefill-update.md) | [WorkbookRangeFill](rangefill.md)   |Actualiza el objeto RangeFill. |
|[Clear](../api/rangefill-clear.md)|None|Restablece el fondo del rango.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|color|string|Código de color HTML que representa el color de la línea de borde con el formato #RRGGBB (por ejemplo, "FFA500") o como un color HTML con nombre (por ejemplo, "naranja").|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookRangeFill"
}-->

```json
{
  "color": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "RangeFill resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
