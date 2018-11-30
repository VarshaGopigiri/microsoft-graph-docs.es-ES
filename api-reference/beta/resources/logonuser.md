---
title: tipo de recurso de logonUser
description: Contiene información de estado sobre el usuario ha iniciado sesión en este host
ms.openlocfilehash: 80ff69453e99f5cd5103f85cd7d8c45696057f7c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090126"
---
# <a name="logonuser-resource-type"></a>tipo de recurso de logonUser

Contiene información de estado sobre el usuario ha iniciado sesión en este host

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo |Descripción|
|:---------------|:--------|:----------|
|accountDomain|String|Dominio de la cuenta de usuario que se usa para el inicio de sesión.|
|accountName|String|Nombre de cuenta de la cuenta de usuario que se usa para el inicio de sesión.|
|accountType|String|Tipo de cuenta de usuario, por definición de Windows. Los valores posibles son: `unknown`, `standard`, `power` y `administrator`.|
|firstSeenDateTime|DateTimeOffset|Fecha y hora en que se produjo el inicio de sesión más antigua por esta cuenta de usuario (período determinados por el proveedor). El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|lastSeenDateTime|DateTimeOffset|Fecha y hora en que se produjo el último inicio de sesión por esta cuenta de usuario. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|ID de registro|String|Identificador de inicio de sesión de usuario.|
|logonTypes|Colección String|Colección de los tipos de inicio de sesión para el usuario ha iniciado la sesión de observar cuando primero a último visto. Los valores posibles son: `unknown`, `interactive`, `remoteInteractive`, `network`, `batch`, `service`.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.logonUser"
}-->

```json
{
  "accountDomain": "String",
  "accountName": "String",
  "accountType": "String",
  "firstSeenDateTime": "String (timestamp)",
  "lastSeenDateTime": "String (timestamp)",
  "logonId": "String",
  "logonTypes": ["String"]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "logonUser resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->