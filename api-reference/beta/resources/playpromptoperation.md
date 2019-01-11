---
title: tipo de recurso playPromptOperation
description: La operación de playPrompt para obtener el resultado de la acción playPrompt.
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: bc18b8f64dedd3fa4d758778bbee37c6bcfd46c6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27814381"
---
# <a name="playpromptoperation-resource-type"></a>tipo de recurso playPromptOperation

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

La operación de playPrompt para obtener el resultado de la acción playPrompt.

## <a name="properties"></a>Propiedades

| Propiedad            | Tipo                        | Description|
|:--------------------|:----------------------------|:-----------------------------------------------------------------------------------|
| clientContext       | Cadena                      | El contexto de cliente.                                                                |
| completionReason    | Cadena                      | Los valores posibles son: `unknown`, `completedSuccessfully` y `mediaOperationCanceled`. |
| createdDateTime     | DateTimeOffset              | La hora de inicio de la operación.                                                   |
| id                  | Cadena                      | Solo lectura.                                                                         |
| lastActionDateTime  | DateTimeOffset              | Hora de la última acción de la operación.                                      |
| resultInfo          | [resultInfo](resultInfo.md) | La información del resultado. Solo lectura. Servidor que se generó.                               |
| status              | Cadena                      | Los valores posibles son: `notStarted`, `running`, `completed` y `failed`.               |

## <a name="relationships"></a>Relaciones
Ninguno

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.playPromptOperation"
}-->
```json
{
  "clientContext": "String",
  "completionReason": "unknown | completedSuccessfully | mediaOperationCanceled",
  "createdDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "lastActionDateTime": "String (timestamp)",
  "resultInfo": {"@odata.type": "#microsoft.graph.resultInfo"},
  "status": "notStarted | running | completed | failed"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "playPromptOperation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
