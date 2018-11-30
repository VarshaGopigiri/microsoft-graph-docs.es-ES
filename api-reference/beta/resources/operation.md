---
title: tipo de recurso de la operación
description: El estado de una operación de larga duración.
ms.openlocfilehash: 71e6a1c47e1f3b18f1481700320779714d716bec
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085836"
---
# <a name="operation-resource-type"></a>tipo de recurso de la operación

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El estado de una operación de larga duración.

## <a name="methods"></a>Métodos

Ninguno

## <a name="properties"></a>Propiedades

| Propiedad           | Tipo            | Descripción                                                                     |
| :----------------- | :-------------- | :-------------------------------------------------------------------------------|
| createdDateTime    | DateTimeOffset  | La hora de inicio de la operación.                                                |
| id                 | String          | Id. de operación. Solo lectura. Servidor que se generó.                                  |
| lastActionDateTime | DateTimeOffset  | Hora de la última acción de la operación.                                   |
| status             | String          | Los valores posibles son: `notStarted`, `running`, `completed` y `failed`. Solo lectura. |

## <a name="relationships"></a>Relaciones

Ninguno

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.operation"
}-->
```json
{
  "createdDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "lastActionDateTime": "String (timestamp)",
  "status": "notStarted | running | completed | failed"
}
```

## <a name="example"></a>Ejemplo

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.operation"
}-->
```json
{
  "createdDateTime": "2018-09-06T15:58:41Z",
  "id": "ABB33D04-3A2C-4D78-996F-9EEEF55EF119",
  "lastActionDateTime": "2018-09-06T15:58:41Z",
  "status": "completed"
}
```

<!-- uuid: 13fa92b1-3b41-498b-aab1-f943464a124f
2018-03-30 10:29:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "operation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->