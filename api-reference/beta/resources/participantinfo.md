---
title: tipo de recurso participantInfo
description: Contiene propiedades adicionales acerca de la identidad del participante
author: VinodRavichandran
ms.openlocfilehash: 335626d1c34e2c54a86b0494e931c2da3fe283e7
ms.sourcegitcommit: 0b3a57ac8b99871e56389f9be15e4f96e219f635
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2018
ms.locfileid: "27380495"
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