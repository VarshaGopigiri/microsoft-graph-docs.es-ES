---
title: tipo de recurso de proceso
description: Contiene información de estado acerca del proceso de relacionados con la alerta.
localization_priority: Normal
ms.openlocfilehash: 0b4207c1780dfd6327ceb67e837f793341e609ae
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27864424"
---
# <a name="process-resource-type"></a>tipo de recurso de proceso

Contiene información de estado acerca del proceso de relacionados con la alerta.

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo|Description|
|:---------------|:--------|:----------|
|accountName|Cadena|Identificador (se ejecutó el proceso en el contexto de cuenta de usuario) de cuenta de usuario por ejemplo, AccountName, SID y así sucesivamente.|
|commandLine|Cadena|La línea de comandos de invocación de proceso completo incluyendo todos los parámetros.|
|createdDateTime|DateTimeOffset|Hora a la que se inició el proceso. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|fileHash|[fileHash](filehash.md)|Tipo complejo que contiene los valores de hash de archivo (criptográficas y la ubicación).|
|integrityLevel|processIntegrityLevel|El nivel de la integridad del proceso. Los valores posibles son: `unknown`, `untrusted`, `low`, `medium`, `high`, `system`.|
|isElevated|Booleano|Es True si el proceso es un elevado.|
|name|Cadena|El nombre de archivo de imagen del proceso.|
|parentProcessCreatedDateTime|DateTimeOffset|Fecha y hora en que se inició el proceso primario. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|parentProcessId|Int32|El proceso de identificador (PID) del proceso principal.|
|parentProcessName|Cadena|El nombre del archivo de imagen del proceso principal.|
|ruta de acceso|String|Ruta de acceso completa, incluido el nombre de archivo.|
|processId|Int32|El proceso de identificador (PID) del proceso.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.process"
}-->

```json
{
  "accountName": "String",
  "commandLine": "String",
  "createdDateTime": "String (timestamp)",
  "fileHash": {"@odata.type": "microsoft.graph.fileHash"},
  "integrityLevel": "@odata.type: microsoft.graph.processIntegrityLevel",
  "isElevated": true,
  "name": "String",
  "parentProcessCreatedDateTime": "String (timestamp)",
  "parentProcessId": 1024,
  "parentProcessName": "String",
  "path": "String",
  "processId": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "process resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
