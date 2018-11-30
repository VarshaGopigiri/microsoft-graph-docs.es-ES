---
title: tipo de recurso de proceso
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: 2e60c9e008ccfddaa0bcc3e78c27cc17c65a3844
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086378"
---
# <a name="process-resource-type"></a>tipo de recurso de proceso

 > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Contiene información de estado acerca del proceso de relacionados con la alerta.

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo|Descripción|
|:---------------|:--------|:----------|
|accountName|String|Identificador (se ejecutó el proceso en el contexto de cuenta de usuario) de cuenta de usuario por ejemplo, AccountName, SID y así sucesivamente.|
|commandLine|String|La línea de comandos de invocación de proceso completo incluyendo todos los parámetros.|
|createdDateTime|DateTimeOffset|Hora a la que se inició el proceso. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|fileHash|[fileHash](filehash.md)|Tipo complejo que contiene los valores de hash de archivo (criptográficas y la ubicación).|
|integrityLevel|processIntegrityLevel|El nivel de la integridad del proceso. Los valores posibles son: `unknown`, `untrusted`, `low`, `medium`, `high`, `system`.|
|isElevated|Booleano|Es True si el proceso es un elevado.|
|name|String|El nombre de archivo de imagen del proceso.|
|parentProcessCreatedDateTime|DateTimeOffset|Fecha y hora en que se inició el proceso primario. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|parentProcessId|Int32|El proceso de identificador (PID) del proceso principal.|
|parentProcessName|String|El nombre del archivo de imagen del proceso principal.|
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