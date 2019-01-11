---
title: tipo de recurso participantInfo
description: Contiene propiedades adicionales acerca de la identidad del participante
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: 94bbc587f26f8b5122571899eb235d9c1fc27e90
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27870668"
---
# <a name="participantinfo-resource-type"></a>tipo de recurso participantInfo

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Contiene propiedades adicionales acerca de la identidad del participante

## <a name="properties"></a>Propiedades

| Propiedad       | Tipo                          | Description  |
|:---------------|:------------------------------|:-------------|
| identity       | [identitySet](identityset.md) | El [identitySet](identityset.md) asociado a este participante. |
| languageId     | Cadena                        | La cadena de referencia cultural del idioma. |
| región         | Cadena                        | Región del participante. |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "languageId", "region"
  ],
  "@odata.type": "microsoft.graph.participantInfo"
}-->
```json
{
  "identity": { "@odata.type": "#microsoft.graph.identitySet" },
  "languageId": "String",
  "region": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "participantInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
