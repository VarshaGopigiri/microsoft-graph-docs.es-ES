---
title: Tipo de recurso RangeFill
description: Representa el fondo de un objeto de rango.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 4043122f4c35c3e7f1c6f9d3919687833d35b9b3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27974346"
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
