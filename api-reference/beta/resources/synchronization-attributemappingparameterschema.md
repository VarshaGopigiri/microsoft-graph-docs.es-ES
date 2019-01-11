---
title: tipo de recurso attributeMappingParameterSchema
description: Describe un solo parámetro empleado en una attributeMappingFunctionSchema.
localization_priority: Normal
ms.openlocfilehash: 083f89ebc5a74e6fd58a33925b2bfa46801b7961
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27892172"
---
# <a name="attributemappingparameterschema-resource-type"></a>tipo de recurso attributeMappingParameterSchema

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Describe un solo parámetro empleado en una [attributeMappingFunctionSchema](../resources/synchronization-attributemappingfunctionschema.md).

## <a name="properties"></a>Propiedades

| Propiedad                   | Tipo                      | Description    |
|:---------------------------|:-------------------------|:---------------|
|allowMultipleOccurrences    |Booleano                   |El parámetro determinado se puede proporcionar varias veces (por ejemplo, cadenas de varias entradas en el `Concatenate(string,string,...)` (función)). |
|name                        |Cadena                    |Nombre del parámetro. |
|necesario                    |Booleano                   |`true`Si el parámetro es necesario; en caso contrario, `false`. |
|type                        |String                    |Valores posibles: `Boolean`, `Binary`, `Reference`, `Integer`, `String`. El valor predeterminado es `String`.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attributeMappingParameterSchema"
}-->

```json
{
  "allowMultipleOccurrences": "Boolean",
  "name": "String",
  "required": "Boolean",
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attributeMappingParameterSchema resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
