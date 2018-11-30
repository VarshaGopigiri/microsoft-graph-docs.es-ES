---
title: tipo de recurso mediaStream
description: El tipo de mediaStream.
ms.openlocfilehash: 28eb98a3ab1be67c60c6ebd35deb7618f1618be3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090726"
---
# <a name="mediastream-resource-type"></a>tipo de recurso mediaStream

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El tipo de mediaStream.

## <a name="properties"></a>Propiedades

| Propiedad    | Tipo    | Descripción                                                                                                   |
| :---------- | :------ | :------------------------------------------------------------------------------------------------------------ |
| dirección   | String  | La dirección. Los valores posibles son `inactive`, `sendOnly`, `receiveOnly`, `sendReceive`.                  |
| label       | String  | La etiqueta de secuencia de medios.                                                                                       |
| mediaType   | String  | El tipo de medios. Los valores posibles son `unknown`, `audio`, `video`, `videoBasedScreenSharing`, `data`.        |
| serverMuted | Booleano | Si se desactiva la multimedia por el servidor.                                                                          |
| sourceId    | String  | El identificador de origen.                                                                                                |

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
