---
title: tipo de recurso appHostedMediaConfig
description: Pila de medios alojado por la aplicación.
ms.openlocfilehash: 39080a8fdb5688ed9f1a5a8daba43266a0e7003e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084441"
---
# <a name="apphostedmediaconfig-resource-type"></a>tipo de recurso appHostedMediaConfig

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Pila de medios alojado por la aplicación.

## <a name="properties"></a>Propiedades

| Propiedad                          | Tipo    | Descripción                                                     |
| :-------------------------------- | :------ | :---------------------------------------------------------------|
| BLOB                              | String  | El blob de configuración de medios generado por el agente de medios inteligentes.    |
| removeFromDefaultAudioGroup       | Booleano | Quitar el grupo predeterminado de audio en audio                       |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.appHostedMediaConfig"
}-->
```json
{
  "blob": "String",
  "removeFromDefaultAudioGroup": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "appHostedMediaConfig resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
