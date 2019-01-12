---
title: tipo de recurso de participantes
description: El tipo de participantes.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: d6a4474525086fb1e8aefe00ad37acaf6511e9f9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27938336"
---
# <a name="participant-resource-type"></a>tipo de recurso de participantes

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El tipo de participantes.

## <a name="methods"></a>Métodos

| Método                                                          | Tipo de valor devuelto                              | Descripción                                       |
|:----------------------------------------------------------------|:-----------------------------------------|:--------------------------------------------------|
| [Obtener participante](../api/participant-get.md)                    | [participante](participant.md)            | Leer las propiedades del objeto **participante** .    |
| [ConfigureMixer](../api/participant-configuremixer.md)          | [commsOperation](commsoperation.md)      | Configure el Mezclador de audio participante.            |
| [Invitar](../api/participant-invite.md)                          | [commsOperation](commsoperation.md)      | Invitar a un participante a la llamada.                 |
| [Desactivar el participante](../api/participant-mute.md)                  | [commsOperation](commsoperation.md)      | Desactivar a un participante en una llamada.                     |
| [Desactivar todos los participantes](../api/participant-muteall.md)          | [commsOperation](commsoperation.md)      | Silenciar a todos los participantes en la reunión.         |

## <a name="properties"></a>Propiedades

| Propiedad             | Tipo                                     | Descripción                                                  |
| :------------------- | :--------------------------------------- | :------------------------------------------------------------|
| id                   | Cadena                                   | El identificador de participante.                                          |
| Info                 | [participantInfo](participantinfo.md)    | El participante del participante.                          |
| isInLobby            | boolean                                  | True si el participante se encuentra en la sala de espera                          |
| isMuted              | boolean                                  | True si se ha desactivado el participante (cliente o servidor ha desactivado)    |
| mediaStreams         | colección de [mediaStream](mediastream.md) | La lista de flujos de medios.                                   |
| metadatos             | Cadena                                   | Un blob de datos proporcionados por el participante en la lista de participantes     |
| recordingInfo        | [recordingInfo](recordinginfo.md)        | Información sobre si el participante tiene capacidad de grabación. |

## <a name="relationships"></a>Relaciones
Ninguno

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.participant"
}-->
```json
{
  "id": "String (identifier)",
  "info": {"@odata.type": "#microsoft.graph.participantInfo"},
  "isInLobby": true,
  "isMuted": true,
  "mediaStreams": [ { "@odata.type": "#microsoft.graph.mediaStream" } ],
  "metadata": "String",
  "recordingInfo": { "@odata.type": "#microsoft.graph.recordingInfo" }
}
```

## <a name="example"></a>Ejemplo

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.participant"
}-->
```json
{
  "id": "ABB33D04-3A2C-4D78-996F-9EEEF55EF119",
  "info": {
    "identity": {
      "user": {
        "id": "550fae72-d251-43ec-868c-373732c2704f",
        "tenantId": "72f988bf-86f1-41af-91ab-2d7cd011db47",
        "displayName": "Heidi Steen"
      }
    },
    "languageId": "en-US",
    "region": "westus"
  },
  "isInLobby": false,
  "isMuted": false,
  "mediaStreams": [
    {
      "sourceId": "1",
      "direction": "sendReceive",
      "label": "main-audio",
      "mediaType": "audio",
      "serverMuted": false
    }
  ],
  "metadata": "metadata-value",
  "recordingInfo": {
    "status": "recordingCapable"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "participant resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
