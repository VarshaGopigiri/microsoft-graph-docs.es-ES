---
title: Tipo de recurso itemBody
description: Representa las propiedades del cuerpo de un elemento, como un mensaje, un evento o una publicación de grupo.
ms.openlocfilehash: ebcc2797052ac3a5a73547332e37c5e9c1bd3a41
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031246"
---
# <a name="itembody-resource-type"></a>Tipo de recurso itemBody

Representa las propiedades del cuerpo de un elemento, como un mensaje, un evento o una publicación de grupo.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|content|String|Contenido del elemento.|
|contentType|bodyType|Tipo de contenido. Valores posibles: `Text` y `HTML`.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.itemBody"
}-->

```json
{
  "content": "string",
  "contentType": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "itemBody resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
