---
title: tipo de recurso synchronizationStatus
description: Representa el estado actual de la synchronizationJob.
localization_priority: Normal
ms.openlocfilehash: 01f30338d7f6d4388554df08bf91655136c24a12
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27817034"
---
# <a name="synchronizationstatus-resource-type"></a>tipo de recurso synchronizationStatus

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa el estado actual de la [synchronizationJob](synchronization-synchronizationjob.md).

## <a name="properties"></a>Propiedades

| Propiedad                              | Tipo      | Descripción    |
|:--------------------------------------|:----------|:---------------|
|código|Cadena|Código de estado de alto nivel del trabajo de sincronización. Los valores posibles son: `NotConfigured`, `NotRun`, `Active`, `Paused` y `Quarantine`.|
|countSuccessiveCompleteFailures|Int64|Número de consecutivos veces este error del trabajo.|
|escrowsPruned|Booleano|`true`Si se han eliminado depósitos de garantía del trabajo (errores de nivel de objeto) durante la sincronización inicial. Si durante la sincronización inicial, alcanza el umbral de errores que normalmente se debería colocar el trabajo en cuarentena, se pueden eliminar depósitos de garantía. En lugar de entrar en cuarentena, el proceso de sincronización borra los errores del trabajo y continúa hasta que se complete la sincronización inicial. Cuando se complete la sincronización inicial, el trabajo pausar y espere a que el cliente limpiar los errores.|
|lastExecution|[synchronizationTaskExecution](synchronization-synchronizationtaskexecution.md)|Detalles de la última ejecución del trabajo.|
|lastSuccessfulExecution|[synchronizationTaskExecution](synchronization-synchronizationtaskexecution.md)|Detalles de la última ejecución de este trabajo, que no tiene errores.|
|lastSuccessfulExecutionWithExports|[synchronizationTaskExecution](synchronization-synchronizationtaskexecution.md)|Detalles de la última ejecución del trabajo, que los objetos exportados en el directorio de destino.|
|progreso|colección de [synchronizationProgress](synchronization-synchronizationprogress.md)|Detalles del progreso de una tarea hasta su finalización.|
|cuarentena|[synchronizationQuarantine](synchronization-quarantine.md)|Si el trabajo está en cuarentena, detalles de cuarentena.|
|steadyStateFirstAchievedTime|DateTimeOffset|El tiempo cuando se ha conseguido en primer lugar estado estable (no hay más cambios en el proceso). El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|steadyStateLastAchievedTime|DateTimeOffset|El tiempo cuando se ha conseguido por última vez el estado estable (no hay más cambios en el proceso). El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|synchronizedEntryCountByType|colección de [stringKeyLongValuePair](synchronization-stringkeylongvaluepair.md)|Recuento de los objetos sincronizados, enumeradas por tipo de objeto.|
|troubleshootingUrl|Cadena|En el caso de un error, la dirección URL con los pasos de solución de problemas para el problema.|

### <a name="synchronization-status-code-details"></a>Detalles del código de estado de sincronización

| Valor                              | Description    |
|:-----------------------------------|:---------------|
|No configurado                       |Trabajo no configuró y nunca se ejecuta. No hay autorización le ha proporcionado. |
|NotRun                              |Trabajo se ha configurado y, posiblemente, se ha iniciado, pero no ha completado su primera ejecución.|
|Activo                              |Trabajo periódicamente se está ejecutando.|
|En pausa                              |Trabajo se pausó (normalmente por un administrador) y actualmente no se está ejecutando, pero se conserva el estado del trabajo.|
|Cuarentena                          |El trabajo está en cuarentena. Esto puede suceder cuando hay un gran volumen de errores o errores críticos, como las credenciales revocado o ha caducado. Mientras está en cuarentena, el proceso de sincronización se intentará ejecutar el trabajo con frecuencia reducida.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.synchronizationStatus"
}-->

```json
{
  "code": "String",
  "countSuccessiveCompleteFailures": 1024,
  "escrowsPruned": true,
  "lastExecution": {"@odata.type": "microsoft.graph.synchronizationTaskExecution"},
  "lastSuccessfulExecution": {"@odata.type": "microsoft.graph.synchronizationTaskExecution"},
  "lastSuccessfulExecutionWithExports": {"@odata.type": "microsoft.graph.synchronizationTaskExecution"},
  "progress": [{"@odata.type": "microsoft.graph.synchronizationProgress"}],
  "quarantine": {"@odata.type": "microsoft.graph.synchronizationQuarantine"},
  "steadyStateFirstAchievedTime": "String (timestamp)",
  "steadyStateLastAchievedTime": "String (timestamp)",
  "synchronizedEntryCountByType": [{"@odata.type": "microsoft.graph.stringKeyLongValuePair"}],
  "troubleshootingUrl": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationStatus resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
