---
title: tipo de recurso synchronizationQuarantine
description: Proporciona información sobre el estado de la cuarentena de un synchronizationJob.
localization_priority: Normal
ms.openlocfilehash: fba0077d48e69ed4c2c190d0b50a6fcfc1749626
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27849731"
---
# <a name="synchronizationquarantine-resource-type"></a>tipo de recurso synchronizationQuarantine

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Proporciona información sobre el estado de la cuarentena de un [synchronizationJob](synchronization-synchronizationjob.md).

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|currentBegan|DateTimeOffset|Fecha y hora cuando la cuarentena por última vez evalúan e imponen. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|nextAttempt|DateTimeOffset|Fecha y hora en la que se realizó el siguiente intento para volver a evaluar la cuarentena. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|motivo|Cadena|Un código que indica la razón por la que se impone la cuarentena. Los valores posibles son: `EncounteredBaseEscrowThreshold`, `EncounteredTotalEscrowThreshold`, `EncounteredEscrowProportionThreshold`, `EncounteredQuarantineException` y `Unknown`.|
|seriesBegan|DateTimeOffset|Fecha y hora cuando la cuarentena en primer lugar se impone en esta serie (una serie se inicia cuando una cuarentena se impone en primer lugar y se restablece tan pronto como se eleva la cuarentena). El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|seriesCount|Int64|Número de veces en esta serie de la cuarentena se vuelve a evaluar y en vigor izquierda (una serie se inicia cuando se impone en primer lugar la cuarentena y se restablece tan pronto como se eleva cuarentena).|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.synchronizationQuarantine"
}-->

```json
{
  "currentBegan": "String (timestamp)",
  "nextAttempt": "String (timestamp)",
  "reason": "String",
  "seriesBegan": "String (timestamp)",
  "seriesCount": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationQuarantine resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
