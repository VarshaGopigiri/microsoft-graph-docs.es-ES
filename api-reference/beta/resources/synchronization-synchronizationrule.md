---
title: tipo de recurso synchronizationRule
description: Define cómo se debe realizar la sincronización para el motor de sincronización, incluidos los objetos que desea sincronizar y en qué dirección, cómo los objetos desde el directorio de origen deben coincidir con los objetos en el directorio de destino y cómo los atributos debe transformarse cuando se está sincronizando desde el origen al directorio de destino.
ms.openlocfilehash: c860228637a6cc3ad9137851408379bd7f779c75
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085080"
---
# <a name="synchronizationrule-resource-type"></a>tipo de recurso synchronizationRule

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Define cómo se debe realizar la sincronización para el motor de sincronización, incluidos los objetos que desea sincronizar y en qué dirección, cómo los objetos desde el directorio de origen deben coincidir con los objetos en el directorio de destino y cómo los atributos debe transformarse cuando se está sincronizando desde el origen al directorio de destino.

>**Nota:** Reglas de sincronización definición sincronización en una dirección - desde el directorio de origen al directorio de destino. Los directorios de origen y de destino se definen como parte de las propiedades de la regla.

Reglas de sincronización se actualizan como parte del [esquema de sincronización](synchronization-synchronizationschema.md).

## <a name="properties"></a>Propiedades

| Propiedad      | Tipo      | Descripción    |
|:--------------|:----------|:---------------|
|editable       |Booleano    |`true`Si la regla de sincronización se puede personalizar; `false` si esta regla es de sólo lectura y no se debe cambiar.|
|id             |String     |Identificador de regla de sincronización. Debe ser uno de los identificadores reconocidos por el motor de sincronización. Admite la regla de identificadores pueden encontrarse en la plantilla de sincronización devuelta por la API.|
|metadatos       |colección de [stringKeyStringValuePair](synchronization-stringkeystringvaluepair.md) |Propiedades de extensión adicionales. A menos que así lo indique explícitamente el equipo de soporte técnico, no se deben cambiar los valores de metadatos.|
|name           |String     |Nombre legible de la regla de sincronización. No admite valores NULL.|
|objectMappings |colección de [objectMapping](synchronization-objectmapping.md)    |Colección de asignaciones de objeto admitidos por la regla. Indica al motor de sincronización los objetos que se deben sincronizar.|
|prioridad       |Entero    |Prioridad con respecto a las demás reglas en la [synchronizationSchema](synchronization-synchronizationschema.md). En primer lugar se procesarán las reglas con el número de prioridad más baja.|
|sourceDirectoryName       |String    |Nombre del directorio de origen. Debe coincidir con una de las definiciones de Active directory en [synchronizationSchema](synchronization-synchronizationschema.md).|
|targetDirectoryName       |String    |Nombre del directorio de destino. Debe coincidir con una de las definiciones de Active directory en [synchronizationSchema](synchronization-synchronizationschema.md).|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.synchronizationRule"
}-->

```json
{
  "editable": true,
  "id": "String",
  "metadata": [{"@odata.type": "microsoft.graph.stringKeyStringValuePair"}],
  "name": "String",
  "objectMappings": [{"@odata.type": "microsoft.graph.objectMapping"}],
  "priority": 1024,
  "sourceDirectoryName": "String",
  "targetDirectoryName": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationRule resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->