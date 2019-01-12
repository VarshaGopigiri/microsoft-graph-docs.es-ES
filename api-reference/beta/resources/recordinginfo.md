---
title: tipo de recurso recordingInfo
description: Información de grabación de un participante.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 08ecaa450fb1c937666068bad656b40497092363
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27990141"
---
# <a name="recordinginfo-resource-type"></a>tipo de recurso recordingInfo

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Información de grabación de un participante.

## <a name="properties"></a>Propiedades

| Propiedad       | Tipo    | Descripción|
|:---------------|:--------|:----------|
| initiatedBy | [participantInfo](participantinfo.md) | El participante que inició la grabación. |
| status | Cadena | Los valores posibles son: `recordingCapable`, `notRecording` y `startedRecording`. |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.recordingInfo"
}-->
```json
{
  "initiatedBy": {"@odata.type": "#microsoft.graph.participantInfo"},
  "status": "recordingCapable | notRecording | startedRecording"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "recordingInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
