---
title: tipo de recurso modifiedProperty
description: Indica todas las propiedades modificadas con valor anterior y el nuevo valor para cualquier recurso en Azure AD que se ha cambiado
ms.openlocfilehash: c504969ee12798969aa39490e79cb5b60bdb5435
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085771"
---
# <a name="modifiedproperty-resource-type"></a>tipo de recurso modifiedProperty
Indica todas las propiedades modificadas con valor anterior y el nuevo valor para cualquier recurso en Azure AD que se ha cambiado



## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|displayName|String|Indica el nombre de propiedad del atributo de destino que se ha modificado.|
|newValue|cadena|Indica el valor actualizado de la propiedad.|
|oldValue|cadena|Indica el valor anterior (antes de la actualización) para la propiedad.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.modifiedProperty"
}-->

```json
{
  "displayName": "String",
  "newValue": "String",
  "oldValue": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "modifiedProperty resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->