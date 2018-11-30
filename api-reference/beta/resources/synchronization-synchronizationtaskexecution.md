---
title: tipo de recurso synchronizationTaskExecution
description: Resuma los resultados de la ejecución del trabajo de sincronización.
ms.openlocfilehash: 4aefba4bdf9ab850892344e6e34683e81d1a1afa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086913"
---
# <a name="synchronizationtaskexecution-resource-type"></a>tipo de recurso synchronizationTaskExecution

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Resuma los resultados de la ejecución del trabajo de sincronización.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|activityIdentifier           |String |Identificador de la ejecución del trabajo.|
|countEntitled                |Int64  |Recuento de procesado entradas que se han asignado a esta aplicación.|
|countEntitledForProvisioning |Int64  |Recuento de procesado entradas que se han asignado para el aprovisionamiento.|
|countEscrowed                |Int64  |Número de entradas que se han custodiadas (errores).|
|countEscrowedRaw             |Int64  |Recuento de las entradas que se han custodiadas, incluidos los depósitos de garantía generados por el sistema.|
|countExported                |Int64  |Recuento de movimientos exportados.|
|countExports                 |Int64  |Recuento de las entradas que se esperaban que se va a exportar.|
|countImported                |Int64  |Número de entradas importadas.|
|countImportedDeltas          |Int64  |Número de cambios de delta importados.|
|countImportedReferenceDeltas |Int64  |Recuento de cambios delta importados relativas a los cambios de referencia.|
|error                        |[synchronizationError](synchronization-synchronizationerror.md)|Si se ha encontrado un error, contiene un objeto **synchronizationError** con detalles.|
|estado                        |String |Resumir los resultados de esta ejecución de código. Los valores posibles son: `Succeeded`, `Failed` y `EntryLevelErrors`.|
|timeBegan                    |DateTimeOffset|Empezó a tiempo cuando se ejecuta este trabajo. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|timeEnded                    |DateTimeOffset|Finalizó el tiempo cuando se ejecuta este trabajo. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.synchronizationTaskExecution"
}-->

```json
{
  "activityIdentifier": "String",
  "countEntitled": 1024,
  "countEntitledForProvisioning": 1024,
  "countEscrowed": 1024,
  "countEscrowedRaw": 1024,
  "countExported": 1024,
  "countExports": 1024,
  "countImported": 1024,
  "countImportedDeltas": 1024,
  "countImportedReferenceDeltas": 1024,
  "error": {"@odata.type": "microsoft.graph.synchronizationError"},
  "state": "String",
  "timeBegan": "String (timestamp)",
  "timeEnded": "String (timestamp)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationTaskExecution resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->