---
title: tipo de recurso meetingCapability
description: Contiene las funciones de una reunión
author: VinodRavichandran
ms.openlocfilehash: 1a6f172922c0efbc9ad93e32141e364e2d0fc711
ms.sourcegitcommit: 0b3a57ac8b99871e56389f9be15e4f96e219f635
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2018
ms.locfileid: "27380250"
---
# <a name="meetingcapability-resource-type"></a>tipo de recurso meetingCapability

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Contiene las funciones de una reunión

## <a name="properties"></a>Propiedades

| Propiedad                          | Tipo    | Descripción                                                        |
|:----------------------------------|:--------|:-------------------------------------------------------------------|
| allowAnonymousUsersToDialOut      | Booleano | Indica si se permiten hacer llamadas de los usuarios anónimos en una reunión. |
| allowAnonymousUsersToStartMeeting | Booleano | Indica si se permiten a los usuarios anónimos para iniciar una reunión.  |
| autoAdmittedUsers                 | String  | Los valores posibles son: `everyoneInCompany` y `everyone`.              |

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
  "allowAnonymousUsersToStartMeeting": true,
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
