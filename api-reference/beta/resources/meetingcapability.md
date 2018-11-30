---
title: tipo de recurso meetingCapability
description: Contiene las funciones de una reunión
ms.openlocfilehash: 438193d08ab5542f07d4cbf61704520d81433e50
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086418"
---
# <a name="meetingcapability-resource-type"></a>tipo de recurso meetingCapability

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Contiene las funciones de una reunión

## <a name="properties"></a>Propiedades

| Propiedad       | Tipo    | Descripción|
|:---------------|:--------|:----------|
| allowAnonymousUsersToDialOut | Booleano | Indica si se permiten hacer llamadas de los usuarios anónimos en una reunión. |
| autoAdmittedUsers | String | Los valores posibles son: `everyoneInCompany` y `everyone`. |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.meetingCapability"
}-->
```json
{
  "allowAnonymousUsersToDialOut": true,
  "autoAdmittedUsers": "everyoneInCompany | everyone"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "meetingCapability resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
