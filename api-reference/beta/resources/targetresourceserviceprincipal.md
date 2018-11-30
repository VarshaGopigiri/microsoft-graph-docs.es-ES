---
title: tipo de recurso targetResourceServicePrincipal
description: Indica la ServicePrincipalId para el recurso que resulta afectada la actividad de auditoría. Deriva el recurso targetResource.
ms.openlocfilehash: 6d6e19997f4bfead771fc0230207df62dde6c6cf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089066"
---
# <a name="targetresourceserviceprincipal-resource-type"></a>tipo de recurso targetResourceServicePrincipal
Indica la ServicePrincipalId para el recurso que resulta afectada la actividad de auditoría. Deriva el recurso [targetResource](targetresource.md) .



## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|appId|cadena|Indica el identificador único de la aplicación. Hace referencia al identificador de la aplicación para una aplicación de específico.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.targetResourceServicePrincipal"
}-->

```json
{
  "appId": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "targetResourceServicePrincipal resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->