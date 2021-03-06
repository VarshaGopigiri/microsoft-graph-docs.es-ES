---
title: tipo de recurso expressionInputObject
description: 'Representa un objeto que se utilizará como datos de comprobación de la entrada cuando la [synchronizationSchema: parseExpression](../api/synchronization_synchronizationschema_parseexpression.md) acción realiza una evaluación de la expresión.'
localization_priority: Normal
ms.openlocfilehash: acf0fa5125d863224de6df76d46109b9888f8ddf
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27820114"
---
# <a name="expressioninputobject-resource-type"></a>tipo de recurso expressionInputObject

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa un objeto que se utilizará como datos de comprobación de la entrada cuando la [synchronizationSchema: parseExpression](../api/synchronization_synchronizationschema_parseexpression.md) acción realiza una evaluación de la expresión.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|definición|[objectDefinition](synchronization-objectdefinition.md)|Definición del objeto de prueba.|
|propiedades|colección de [stringKeyObjectValuePair](synchronization-stringkeyobjectvaluepair.md)|Valores de propiedad del objeto de prueba.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.expressionInputObject"
}-->

```json
{
  "definition": {"@odata.type": "microsoft.graph.objectDefinition"},
  "properties": [{"@odata.type": "microsoft.graph.stringKeyObjectValuePair"}]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "expressionInputObject resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
