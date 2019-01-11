---
title: tipo de recurso attributeMappingFunctionSchema
description: Describe una función que se puede usar en una asignación de atributos para transformar los valores durante la sincronización.
localization_priority: Normal
ms.openlocfilehash: 7273534d281d8ea5eaf3709b530776295cd9c767
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27822165"
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
|name                        |Cadena                    |Nombre del operador. |
|parámetros                  |colección de [attributeMappingParameterSchema](../resources/synchronization-attributemappingparameterschema.md)  |Colección de parámetros de la función.|

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
