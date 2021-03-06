---
title: tipo de recurso commsOperation
description: El estado de determinadas operaciones de larga duración.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 79fc6801e95854b2530f8a28c13f7180ed02203f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27957728"
---
# <a name="commsoperation-resource-type"></a>tipo de recurso commsOperation

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El estado de determinadas operaciones de larga duración.

## <a name="methods"></a>Métodos
Ninguno

## <a name="properties"></a>Propiedades

| Propiedad           | Tipo                        | Descripción                                                                     |
| :----------------- | :-------------------------- | :-------------------------------------------------------------------------------|
| clientContext      | Cadena                      | El contexto de cliente.                                                             |
| createdDateTime    | DateTimeOffset              | La hora de inicio de la operación.                                                |
| id                 | Cadena                      | Id. de operación. Solo lectura. Servidor que se generó.                                  |
| lastActionDateTime | DateTimeOffset              | Hora de la última acción de la operación.                                   |
| resultInfo         | [resultInfo](resultinfo.md) | La información del resultado. Solo lectura. Servidor que se generó.                            |
| status             | Cadena                      | Los valores posibles son: `notStarted`, `running`, `completed` y `failed`. Solo lectura. |

## <a name="relationships"></a>Relaciones
Ninguno

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.commsOperation"
}-->
```json
{
  "clientContext": "String",
  "createdDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "lastActionDateTime": "String (timestamp)",
  "resultInfo": { "@odata.type": "#microsoft.graph.resultInfo" },
  "status": "notStarted | running | completed | failed"
}
```

## <a name="example"></a>Ejemplo

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.commsOperation"
}-->
```json
{
  "clientContext": "ABB33D04-3A2C-4D78-996F-9EEEF55EF119",
  "createdDateTime": "2018-09-06T15:58:41Z",
  "id": "ABB33D04-3A2C-4D78-996F-9EEEF55EF119",
  "lastActionDateTime": "2018-09-06T15:58:41Z",
  "resultInfo": {
    "@odata.type": "#microsoft.graph.resultInfo",
    "code": "200"
  },
  "status": "completed"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "commsOperation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
