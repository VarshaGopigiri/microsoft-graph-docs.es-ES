---
title: Tipo de recurso RangeBorder
description: Representa el borde de un objeto.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 8404a45ea7c56bbbb318994daa55229706d700a2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27960241"
---
# <a name="rangeborder-resource-type"></a>Tipo de recurso RangeBorder

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa el borde de un objeto.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get RangeBorder](../api/rangeborder-get.md) | [RangeBorder](rangeborder.md) |Lee las propiedades y relaciones del objeto rangeBorder.|
|[Update](../api/rangeborder-update.md) | [RangeBorder](rangeborder.md) |Actualiza el objeto RangeBorder. |
|[List](../api/rangeborder-list.md) | Colección [RangeBorder](rangeborder.md) |Obtiene la colección de objetos rangeBorder. |
|[Itemat](../api/rangebordercollection-itemat.md)|[RangeBorder](rangeborder.md)|Obtiene un objeto de borde mediante su índice.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|color|string|Código de color HTML que representa el color de la línea de borde con el formato #RRGGBB (por ejemplo, "FFA500") o como un color HTML con nombre (por ejemplo, "naranja").|
|id|string|Representa el identificador de borde. Valores posibles: `EdgeTop`, `EdgeBottom`, `EdgeLeft`, `EdgeRight`, `InsideVertical`, `InsideHorizontal`, `DiagonalDown`, `DiagonalUp`. Solo lectura.|
|sideIndex|string|Valor constante que indica el lado específico del borde. Valores posibles: `EdgeTop`, `EdgeBottom`, `EdgeLeft`, `EdgeRight`, `InsideVertical`, `InsideHorizontal`, `DiagonalDown`, `DiagonalUp`. Solo lectura.|
|style|string|Una de las constantes de estilo de línea que especifica el estilo de línea del borde. Valores posibles: `None`, `Continuous`, `Dash`, `DashDot`, `DashDotDot`, `Dot`, `Double`, `SlantDashDot`.|
|weight|string|Especifica el grosor del borde alrededor de un rango. Valores posibles: `Hairline`, `Thin`, `Medium`, `Thick`.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.rangeBorder"
}-->

```json
{
  "color": "string",
  "id": "string",
  "sideIndex": "string",
  "style": "string",
  "weight": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "RangeBorder resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
