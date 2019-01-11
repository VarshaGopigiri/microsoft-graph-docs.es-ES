---
title: tipo de recurso targetResourceServicePrincipal
description: Indica la ServicePrincipalId para el recurso que resulta afectada la actividad de auditoría. Deriva el recurso targetResource.
localization_priority: Normal
ms.openlocfilehash: 37bd63851ca9169afb669c710ef4cb2c150ea615
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27839602"
---
# <a name="targetresourceserviceprincipal-resource-type"></a>tipo de recurso targetResourceServicePrincipal
Indica la ServicePrincipalId para el recurso que resulta afectada la actividad de auditoría. Deriva el recurso [targetResource](targetresource.md) .



## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
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
