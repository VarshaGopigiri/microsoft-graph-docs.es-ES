---
title: tipo de recurso mentionsPreview
description: Representa información acerca de los objetos de mención en una instancia de recursos.
ms.openlocfilehash: cf6bed3cdfb2d3f541438da0c06fcf8f4873c17e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089766"
---
# <a name="mentionspreview-resource-type"></a>tipo de recurso mentionsPreview

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa información sobre los objetos [mencione](../resources/mention.md) en una instancia de recursos.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
| isMentioned | Booleano | Es True si el usuario ha iniciado sesión se menciona en la instancia de recurso primario. Solo lectura. Filtro de admite. |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.mentionsPreview"
}-->

```json
{
  "isMentioned": "Boolean"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mentionsPreview resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
