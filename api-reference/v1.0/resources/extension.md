---
title: Tipo de recurso extension
description: Tipo abstracto para admitir el tipo abierto de OData v4 openTypeExtension.
ms.openlocfilehash: 1b3d735e0997ca128b539bff9a05c9c7c56799df
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028837"
---
# <a name="extension-resource-type"></a>Tipo de recurso extension

Tipo abstracto para admitir el tipo abierto de OData v4 [openTypeExtension](opentypeextension.md).

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "abstract": "true",
  "baseType": "microsoft.graph.entity",
  "blockType": "resource",
  "openType": true,
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.extension"
}-->

```json
{
  "id": "string (identifier)"
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|String| Solo lectura.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="methods"></a>Métodos

Consulte los métodos del tipo derivado [openTypeExtension](opentypeextension.md) para ver los métodos realmente compatibles.


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "extension resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->