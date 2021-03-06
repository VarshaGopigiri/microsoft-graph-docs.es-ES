---
title: tipo de recurso attributeMappingSource
description: 'Define cómo debe ser un valor extrajo (o transforma) desde el objeto de origen. Por ejemplo, puede ser un valor simple tomado de un atributo determinado en el objeto de origen, o puede ser una expresión de cadena concatenación/extracción/sustitución en función de varios atributos de origen más compleja. '
localization_priority: Normal
ms.openlocfilehash: a7c1493f27f34230d4305fe95b2d2f03a5ad25e2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27825014"
---
# <a name="attributemappingsource-resource-type"></a>tipo de recurso attributeMappingSource

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Define cómo debe ser un valor extrajo (o transforma) desde el objeto de origen. Por ejemplo, puede ser un valor simple tomado de un atributo determinado en el objeto de origen, o puede ser una expresión de cadena concatenación/extracción/sustitución en función de varios atributos de origen más compleja. 

## <a name="properties"></a>Propiedades

| Propiedad              | Tipo                      | Description               |
|:----------------------|:--------------------------|:--------------------------|
|expresión             |Cadena                     |Representación de la expresión equivalente de este objeto **attributeMappingSource** .|
|name                   |Cadena                     |Parámetro nombre de origen de la asignación. Según el valor de la propiedad **type** , esto puede ser el nombre de la función, el nombre del atributo de origen, o un valor constante que se va a utilizar. |
|parámetros             |colección de [stringKeyAttributeMappingSourceValuePair](synchronization-stringkeyattributemappingsourcevaluepair.md) | Si este objeto representa una función, enumera los parámetros de la función. Parámetros constan de objetos de **attributeMappingSource** ellos mismos, lo que permite para expresiones complejas. Si no es del **tipo** `Function`, esta propiedad será null o vacío matriz. |
|type                   | Cadena                    |El tipo de este origen de asignación de atributo. Los valores posibles son: `Attribute`, `Constant` y `Function`. El valor predeterminado es `Attribute`.| 

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attributeMappingSource"
}-->

```json
{
  "expression": "String",
  "name": "String",
  "parameters": [{"@odata.type": "microsoft.graph.stringKeyAttributeMappingSourceValuePair"}],
  "type": "String"
}
```

## <a name="json-examples"></a>Ejemplos JSON

Asignación de atributo para el atributo simple

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attributeMappingSource"
}-->

```json
{
    "expression": "[mail]",
    "name": "mail",
    "type": "Attribute"
}
```

Expresión de extracción de 8 primeros caracteres del atributo de origen

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attributeMappingSource"
}-->

```json
 {
    "expression": "Mid([userPrincipalName], 1, 8)",
    "name": "Mid",
    "parameters": [
        {
            "key": "source",
            "value": {
                "expression": "[userPrincipalName]",
                "name": "userPrincipalName",
                "parameters": [],
                "type": "Attribute"
            }
        },
        {
            "key": "start",
            "value": {
                "expression": "\"1\"",
                "name": "1",
                "parameters": [],
                "type": "Constant"
            }
        },
        {
            "key": "length",
            "value": {
                "expression": "\"8\"",
                "name": "8",
                "parameters": [],
                "type": "Constant"
            }
        }
    ],
    "type": "Function"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attributeMappingSource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
