---
title: tipo de recurso mediaStream
description: El tipo de mediaStream.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: fd003bde0eca5fd21cb12c23d5c83699a6b79c8e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27916967"
---
# <a name="mediastream-resource-type"></a>tipo de recurso mediaStream

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El tipo de mediaStream.

## <a name="properties"></a>Propiedades

| Propiedad    | Tipo    | Descripción                                                                                                   |
| :---------- | :------ | :------------------------------------------------------------------------------------------------------------ |
| dirección   | Cadena  | La dirección. Los valores posibles son `inactive`, `sendOnly`, `receiveOnly`, `sendReceive`.                  |
| label       | Cadena  | La etiqueta de secuencia de medios.                                                                                       |
| mediaType   | Cadena  | El tipo de medios. Los valores posibles son `unknown`, `audio`, `video`, `videoBasedScreenSharing`, `data`.        |
| serverMuted | Booleano | Si se desactiva la multimedia por el servidor.                                                                          |
| sourceId    | Cadena  | El identificador de origen.                                                                                                |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "serverMuted"
  ],
  "@odata.type": "microsoft.graph.mediaStream"
}-->
```json
{
  "direction": "inactive | sendOnly | receiveOnly | sendReceive",
  "label": "String",
  "mediaType": "unknown | audio | video | videoBasedScreenSharing | data",
  "serverMuted": true,
  "sourceId": "String"
}
```

## <a name="example"></a>Ejemplo

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.mediaStream"
}-->
```json
{
  "direction": "sendReceive",
  "label": "main-audio",
  "mediaType": "audio",
  "serverMuted": false,
  "sourceId": "1024"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mediaStream resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
