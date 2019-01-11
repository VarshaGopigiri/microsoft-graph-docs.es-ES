---
title: Tipo de recurso extension
description: Tipo abstracto para admitir el tipo abierto de OData v4 openTypeExtension.
localization_priority: Normal
ms.openlocfilehash: 2633c8a28c1be1a670a80834ce869b5156fc1de9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27834674"
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
|id|Cadena| Solo lectura.|

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
