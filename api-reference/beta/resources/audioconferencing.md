---
title: tipo de recurso de audioconferencia
description: Representa la información de acceso telefónica de un onlineMeeting.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: cd65b094a17ad3fa470471c3ed6dd3908367e578
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27977510"
---
# <a name="audioconferencing-resource-type"></a>tipo de recurso de audioconferencia

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa la información de acceso telefónica de un [onlineMeeting](onlinemeeting.md).

## <a name="properties"></a>Propiedades

| Propiedad            | Tipo    | Descripción                                                                    |
|:--------------------|:--------|:-------------------------------------------------------------------------------|
| dialinUrl           | Cadena  | Una dirección URL a la página web accesibles de forma externa que contiene la información de marcado. |
| leaderPasscode      | Cadena  | La contraseña de coordinador necesaria para conectarse al proveedor de conferencia de Audio.      |
| participantPasscode | Cadena  | La contraseña de participantes necesaria para conectarse al proveedor de conferencia de Audio. |
| tollFreeNumber      | Cadena  | El número gratuito para conectarse al proveedor de conferencia de Audio.              |
| tollNumber          | Cadena  | El número de teléfono de pago para conectarse al proveedor de conferencia de Audio.                   |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.audioConferencing"
}-->
```json
{
  "dialinUrl": "String",
  "leaderPasscode": "String",
  "participantPasscode": "String",
  "tollFreeNumber": "String",
  "tollNumber": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "audioConferencing resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
