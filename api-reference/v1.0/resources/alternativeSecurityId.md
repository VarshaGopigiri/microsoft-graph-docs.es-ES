---
title: Tipo de recurso alternativeSecurityId
description: Solo para uso interno.
ms.openlocfilehash: 9d941469da133d9a3e7149dfca55c813f60b3ce8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028615"
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
