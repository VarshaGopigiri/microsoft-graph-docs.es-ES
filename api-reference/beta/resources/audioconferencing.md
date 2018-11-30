---
title: tipo de recurso de audioconferencia
description: Representa la información de acceso telefónica de un onlineMeeting.
ms.openlocfilehash: dd23c6ade282e081482a8c079491644c663b4054
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085470"
---
# <a name="audioconferencing-resource-type"></a>tipo de recurso de audioconferencia

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa la información de acceso telefónica de un [onlineMeeting](onlinemeeting.md).

## <a name="properties"></a>Propiedades

| Propiedad            | Tipo    | Descripción                                                                    |
|:--------------------|:--------|:-------------------------------------------------------------------------------|
| dialinUrl           | String  | Una dirección URL a la página web accesibles de forma externa que contiene la información de marcado. |
| leaderPasscode      | String  | La contraseña de coordinador necesaria para conectarse al proveedor de conferencia de Audio.      |
| participantPasscode | String  | La contraseña de participantes necesaria para conectarse al proveedor de conferencia de Audio. |
| tollFreeNumber      | String  | El número gratuito para conectarse al proveedor de conferencia de Audio.              |
| tollNumber          | String  | El número de teléfono de pago para conectarse al proveedor de conferencia de Audio.                   |

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
