---
title: Tipo de recurso RangeFill
description: Representa el fondo de un objeto de rango.
ms.openlocfilehash: 11806d95900c6e4ea1d4bf6ce4f4800bf5f6f66b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089980"
---
# <a name="rangefill-resource-type"></a>Tipo de recurso RangeFill

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa el fondo de un objeto de rango.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get RangeFill](../api/rangefill-get.md) | [RangeFill](rangefill.md) |Lee las propiedades y relaciones del objeto rangeFill.|
|[Update](../api/rangefill-update.md) | [RangeFill](rangefill.md)   |Actualiza el objeto RangeFill. |
|[Clear](../api/rangefill-clear.md)|None|Restablece el fondo del rango.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|color|string|Código de color HTML que representa el color de la línea de borde con el formato #RRGGBB (por ejemplo, "FFA500") o como un color HTML con nombre (por ejemplo, "naranja").|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.rangeFill"
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