---
title: tipo de recurso appHostedMediaConfig
description: Pila de medios alojado por la aplicación.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 36f869be347e2d55ec90079c62c5b6ebef85f144
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27928587"
---
# <a name="apphostedmediaconfig-resource-type"></a>tipo de recurso appHostedMediaConfig

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Pila de medios alojado por la aplicación.

## <a name="properties"></a>Propiedades

| Propiedad                          | Tipo    | Descripción                                                     |
| :-------------------------------- | :------ | :---------------------------------------------------------------|
| BLOB                              | Cadena  | El blob de configuración de medios generado por el agente de medios inteligentes.    |
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
