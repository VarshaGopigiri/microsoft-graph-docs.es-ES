---
title: Tipo de recurso alternativeSecurityId
description: Solo para uso interno.
localization_priority: Normal
ms.openlocfilehash: 23ef74085a4a3cc383f0854e9139c9a0b63e3d40
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27853805"
---
# <a name="alternativesecurityid-resource-type"></a>Tipo de recurso alternativeSecurityId

Solo para uso interno.

## <a name="json-representation"></a>Representación JSON

<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.alternativeSecurityId"
}-->

```json
{
  "type": 12345,
  "identityProvider": "string",
  "key": {"@odata.type": "Edm.Binary"}
}
```

## <a name="properties"></a>Propiedades
| Propiedad         | Tipo       | Descripción
|:-----------------|:-----------|:---------------------
| type             | Int32      | Sólo para uso interno
| identityProvider | string     | Sólo para uso interno
| Key              | Edm.Binary | Sólo para uso interno
