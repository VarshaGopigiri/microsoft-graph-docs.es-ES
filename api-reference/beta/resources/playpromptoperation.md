---
title: tipo de recurso playPromptOperation
description: La operación de playPrompt para obtener el resultado de la acción playPrompt.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: d451418482d1adf1a4b7e16dc8a6eb8ca7febdb7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27937820"
---
# <a name="playpromptoperation-resource-type"></a>tipo de recurso playPromptOperation

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

La operación de playPrompt para obtener el resultado de la acción playPrompt.

## <a name="properties"></a>Propiedades

| Propiedad            | Tipo                        | Descripción|
|:--------------------|:----------------------------|:-----------------------------------------------------------------------------------|
| clientContext       | String                      | El contexto de cliente.                                                                |
| completionReason    | String                      | Los valores posibles son: `unknown`, `completedSuccessfully` y `mediaOperationCanceled`. |
| createdDateTime     | DateTimeOffset              | La hora de inicio de la operación.                                                   |
| id                  | String                      | Solo lectura.                                                                         |
| lastActionDateTime  | DateTimeOffset              | Hora de la última acción de la operación.                                      |
| resultInfo          | [resultInfo](resultInfo.md) | La información del resultado. Solo lectura. Servidor que se generó.                               |
| status              | String                      | Los valores posibles son: `notStarted`, `running`, `completed` y `failed`.               |

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
