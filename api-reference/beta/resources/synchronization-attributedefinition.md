---
title: tipo de recurso attributeDefinition
description: Describe un atributo de un objeto.
ms.openlocfilehash: 2199f8dbe5c528cf3b1b73f007fdae3451833815
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090009"
---
# <a name="attributedefinition-resource-type"></a>tipo de recurso attributeDefinition

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Describe un atributo de un objeto.

## <a name="properties"></a>Propiedades

| Propiedad      | Tipo      | Descripción    |
|:--------------|:----------|:---------------|
|delimitador         |Booleano    | `true`Si el atributo debe utilizarse como el delimitador para el objeto. Atributos de anclaje deben tener un valor único que identifica un objeto y deben ser inmutables. El valor predeterminado es `false`. Uno y sólo uno, de los atributos del objeto deben designarse como el delimitador para admitir la sincronización. |
|caseExact      |Booleano    |`true`Si el valor de este atributo debe tratarse como entre mayúsculas y minúsculas. Esta configuración afecta a cómo el motor de sincronización detecta cambios para el atributo.|
|metadatos       |[metadataEntry](../resources/synchronization-metadataentry.md)    |Propiedades de extensión adicionales. A menos que se mencionan explícitamente, no se deben cambiar los valores de metadatos.|
|multivalor    |Booleano    |`true`Si un atributo puede tener varios valores. El valor predeterminado es `false`.|
|mutabilidad     |String     |Mutabilidad de un atributo. Los valores posibles son: `ReadWrite`, `ReadOnly`, `Immutable`, `WriteOnly`. El valor predeterminado es `ReadWrite`.|
|name           |String     |Nombre del atributo. Debe ser único dentro de la definición del objeto. No admite valores NULL.|
|necesario       |Booleano    |`true`Si se requiere el atributo. No se puede crear el objeto si falta alguno de los atributos necesarios. Si durante la sincronización, el atributo required no tiene ningún valor, se usará el valor predeterminado. Si no se ha establecido el valor predeterminado, sincronización registrará un error.|
|referencedObjects|[referencedObject](../resources/synchronization-referencedobject.md) |Para los atributos con `reference` escriba, objetos de listas que se hace referencia (por ejemplo, el `manager` mostrarían una lista de atributo `User` como el objeto que se hace referencia).|
|type           |String     |Tipo de valor de atributo. Valores posibles: `String`, `Integer`, `Reference`, `Binary`, `Boolean`. El valor predeterminado es `String`.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attributeDefinition"
}-->

```json
{
  "anchor": true,
  "caseExact": true,
  "defaultValue": "String",
  "metadata": [{"@odata.type": "microsoft.graph.metadataEntry"}],
  "multivalued": true,
  "mutability": "String",
  "name": "String",
  "referencedObjects": [{"@odata.type": "microsoft.graph.referencedObject"}],
  "required": true,
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attributeDefinition resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->