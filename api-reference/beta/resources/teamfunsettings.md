---
title: tipo de recurso teamFunSettings
description: Opciones para configurar el uso de Giphy, memes y pegatinas en el equipo.
localization_priority: Normal
ms.openlocfilehash: c53d3215e5f515361c66fe2d3d0ad10a5338e0c4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27852069"
---
# <a name="teamfunsettings-resource-type"></a>tipo de recurso teamFunSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Opciones para configurar el uso de Giphy, memes y pegatinas en el [equipo](team.md).

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
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
