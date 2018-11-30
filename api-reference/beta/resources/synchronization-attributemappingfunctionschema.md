---
title: tipo de recurso attributeMappingFunctionSchema
description: Describe una función que se puede usar en una asignación de atributos para transformar los valores durante la sincronización.
ms.openlocfilehash: 9760669bb29700bfa79c1cd375857b4fd673879b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087044"
---
# <a name="attributemappingfunctionschema-resource-type"></a>tipo de recurso attributeMappingFunctionSchema

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Describe una función que se puede usar en una [asignación de atributos](synchronization-attributemapping.md) para transformar los valores durante la sincronización.

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[List](../api/synchronization-synchronizationschema-functions.md) | colección de [attributeMappingFunctionSchema](../resources/synchronization-attributemappingfunctionschema.md)|Funciones de la asignación de atributo de la lista compatible.|

## <a name="properties"></a>Propiedades

| Propiedad                   | Tipo                      | Descripción    |
|:---------------------------|:-------------------------|:---------------|
|name                        |String                    |Nombre del operador. |
|parameters                  |colección de [attributeMappingParameterSchema](../resources/synchronization-attributemappingparameterschema.md)  |Colección de parámetros de la función.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attributeMappingFunctionSchema"
}-->

```json
{
  "name": "String (identifier)",
  "parameters": [{"@odata.type": "microsoft.graph.attributeMappingParameterSchema"}]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attributeMappingFunctionSchema resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->