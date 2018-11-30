---
title: tipo de recurso educationOrganization
description: Entidades abstractas que se utiliza para modelar la uniformidad entre los tipos de organización diferentes en el sector de educación.
ms.openlocfilehash: ed7a01072fe3adf00cb09082ad17954b9a921083
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029455"
---
# <a name="educationorganization-resource-type"></a>tipo de recurso educationOrganization

Entidades abstractas que se utiliza para modelar la uniformidad entre los tipos de organización diferentes en el sector de educación.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|description|String| Descripción de la organización.|
|displayName|String| Nombre para mostrar de organización.|
|externalSource|educationExternalSource| Origen donde se creó esta organización. Los valores posibles son: `sis`, `manual`, `unknownFutureValue`.|

## <a name="relationships"></a>Relaciones
Ninguna.


## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "abstract": true,
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationOrganization"
}-->

```json
{
  "description": "String",
  "displayName": "String",
  "externalSource": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationOrganization resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->