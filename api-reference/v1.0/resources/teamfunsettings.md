---
title: tipo de recurso teamFunSettings
description: Opciones para configurar el uso de Giphy, memes y pegatinas en el equipo.
ms.openlocfilehash: ef816d027f015155cc09195c359523c83589725e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028990"
---
# <a name="teamfunsettings-resource-type"></a>tipo de recurso teamFunSettings



Opciones para configurar el uso de Giphy, memes y pegatinas en el [equipo](team.md).

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|allowGiphy|Booleano|Si establece en verdadero, permite el uso de Giphy.|
|giphyContentRating|Cadena (enumeración)|Clasificación de contenido de Giphy. Los valores posibles son: `moderate` y `strict`.|
|allowStickersAndMemes|Booleano|Si establece en true, permite a los usuarios para que incluya pegatinas y memes.|
|allowCustomMemes|Booleano|Si establece en true, permite a los usuarios para incluir memes personalizado.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamFunSettings"
}-->

```json
{
  "allowGiphy": true,
  "giphyContentRating": "strict",
  "allowStickersAndMemes": true,
  "allowCustomMemes": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "team's funSettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
