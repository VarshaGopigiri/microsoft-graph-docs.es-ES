---
title: tipo de recurso appHostedMediaConfig
description: Pila de medios alojado por la aplicación.
author: VinodRavichandran
ms.openlocfilehash: b96d6ff836ab36e5561c9ba3958123178e2fbde9
ms.sourcegitcommit: 0b3a57ac8b99871e56389f9be15e4f96e219f635
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2018
ms.locfileid: "27380131"
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
