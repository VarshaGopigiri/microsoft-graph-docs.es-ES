---
title: tipo de recurso synchronizationSchedule
description: Define la programación que se usa para ejecutar un synchronizationJob.
localization_priority: Normal
ms.openlocfilehash: b59c36a36d837c21c147033dff8de66b85c863a1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27877871"
---
# <a name="synchronizationschedule-resource-type"></a>tipo de recurso synchronizationSchedule

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Define la programación que se usa para ejecutar un [synchronizationJob](synchronization-synchronizationjob.md).

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|expiración|DateTimeOffset|Fecha y hora de caducidad de este trabajo. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|interval|Duración|El intervalo entre iteraciones de sincronización.|
|state|String| Los valores posibles son: `Active` y `Disabled`.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.synchronizationSchedule"
}-->

```json
{
  "expiration": "String (timestamp)",
  "interval": "String (duration)",
  "state": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationSchedule resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
