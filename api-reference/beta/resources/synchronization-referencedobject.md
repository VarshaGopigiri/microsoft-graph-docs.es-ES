---
title: tipo de recurso referencedObject
description: Describe una referencia a otro objeto definido en la misma definición de Active directory.
ms.openlocfilehash: 63645048fd8ba6ad949da43baa261b2842ea4016
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090373"
---
# <a name="referencedobject-resource-type"></a>tipo de recurso referencedObject

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Describe una referencia a otro objeto definido en la misma [definición de Active directory](synchronization-directorydefinition.md).

## <a name="properties"></a>Propiedades

| Propiedad                   | Tipo                      | Descripción    |
|:---------------------------|:--------------------------|:---------------|
|referencedObjectName        |String                     |Nombre del objeto que se hace referencia. Debe coincidir con uno de los objetos en la [definición de Active directory](synchronization-directorydefinition.md).|
|referencedProperty          |String                     |**Actualmente no se admite**. Nombre de la propiedad en el objeto de referencia, el valor para el que se usa como referencia.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.referencedObject"
}-->

```json
{
  "referencedObjectName": "String",
  "referencedProperty": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "referencedObject resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
            