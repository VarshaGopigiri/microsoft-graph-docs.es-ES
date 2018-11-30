---
title: tipo de recurso participantInfo
description: Contiene propiedades adicionales acerca de la identidad del participante
ms.openlocfilehash: c6f429e353d80ea53c5f5c00ca084ae7a8a4a7c1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083225"
---
# <a name="participantinfo-resource-type"></a>tipo de recurso participantInfo

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Contiene propiedades adicionales acerca de la identidad del participante

## <a name="properties"></a>Propiedades

| Propiedad       | Tipo                          | Descripción  |
|:---------------|:------------------------------|:-------------|
| identity       | [identitySet](identityset.md) | El [identitySet](identityset.md) asociado a este participante. |
| languageId     | String                        | La cadena de referencia cultural del idioma. |
| región         | String                        | Región del participante. |

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