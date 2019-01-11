---
title: tipo de recurso recordOperation
description: El tipo de recordOperation
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: be6a124fcd7175489679a8c2392218530d510e9e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27880020"
---
# <a name="recordoperation-resource-type"></a>tipo de recurso recordOperation

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El tipo de recordOperation

## <a name="properties"></a>Propiedades

| Propiedad                       | Tipo                        | Description                                                                                                                                       |
| :----------------------------- | :---------------------------| :-------------------------------------------------------------------------------------------------------------------------------------------------|
| clientContext                  | Cadena                      | El contexto de cliente.                                                                                                                               |
| completionReason               | Cadena                      | Los valores posibles son: `operationCanceled`, `stopToneDetected`, `maxRecordDurationReached`, `initialSilenceTimeout`, `maxSilenceTimeout`, `playPromptFailed`, `playBeepFailed`, `mediaReceiveTimeout`, `unspecifiedError` y `none`. |
| createdDateTime                | DateTimeOffset              | La hora de creación de la grabación.                                                                                                          |
| id                             | Cadena                      | Identificador de la operación de servidor. Es de sólo lectura. Servidor que se generó.                                                                                             |
| lastActionDateTime             | DateTimeOffset              | Hora de la última acción de la operación.                                                                                                     |
| recordResourceAccessToken      | Cadena                      | El token de acceso necesario para recuperar la grabación.                                                                                              |
| recordResourceLocation         | Cadena                      | La ubicación donde se encuentra la grabación.                                                                                                      |
| resultInfo                     | [resultInfo](resultinfo.md) | La información del resultado.  Solo lectura. Servidor que se generó.                                                                                             |
| status                         | Cadena                      | Los valores posibles son: `notStarted`, `running`, `completed` y `failed`. Solo lectura. Servidor que se generó.                                                 |

## <a name="relationships"></a>Relaciones
Ninguno

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.recordOperation"
}-->
```json
{
  "clientContext": "String",
  "completionReason": "operationCanceled | stopToneDetected | maxRecordDurationReached | initialSilenceTimeout | maxSilenceTimeout | playPromptFailed | playBeepFailed | mediaReceiveTimeout | unspecifiedError | none",
  "createdDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "lastActionDateTime": "String (timestamp)",
  "recordResourceAccessToken": "String",
  "recordResourceLocation": "String",
  "resultInfo": {"@odata.type": "#microsoft.graph.resultInfo"},
  "status": "notStarted | running | completed | failed"
}
```

## <a name="example"></a>Ejemplo

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.recordOperation",
  "truncated": true
}-->
```json
{
  "clientContext": "d45324c1-fcb5-430a-902c-f20af696537c",
  "id": "ABB33D04-3A2C-4D78-996F-9EEEF55EF119",
  "recordResourceAccessToken": "<access-token>",
  "recordResourceLocation": "https://resource.location/ABB33D04-3A2C-4D78-996F-9EEEF55EF119",
  "status": "completed"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "recordOperation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
