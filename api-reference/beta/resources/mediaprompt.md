---
title: tipo de recurso mediaPrompt
description: El tipo de mediaPrompt.
ms.openlocfilehash: 1a782d391110d35b07b551e44ebd3b931dbcadba
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089246"
---
# <a name="mediaprompt-resource-type"></a>tipo de recurso mediaPrompt

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El tipo de mediaPrompt.

## <a name="properties"></a>Propiedades

| Propiedad    | Tipo                      | Descripción                                                                     |
| :---------- | :------------------------ | :------------------------------------------------------------------------------ |
| bucle        | Int32                     | El recuento del bucle. el valor 0 indica que el bucle indefinido. El valor predeterminado es `1`. |
| mediaInfo   | [mediaInfo](mediainfo.md) | La información de medios                                                           |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.mediaPrompt"
}-->

```json
{
  "loop": 1024,
  "mediaInfo": { "@odata.type": "#microsoft.graph.mediaInfo" }
}
```

## <a name="example"></a>Ejemplo

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.mediaPrompt"
}-->
```json
{
  "mediaInfo": {
    "uri": "https://cdn.contoso.com/beep.wav",
    "resourceId": "1D6DE2D4-CD51-4309-8DAA-70768651088E"
  },
  "loop": 5
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mediaPrompt resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
