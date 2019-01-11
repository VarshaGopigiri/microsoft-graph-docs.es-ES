---
title: tipo de recurso onlineMeeting
description: Captura información acerca de la reunión, incluida la dirección URL de la combinación, la lista de los asistentes y la descripción.
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: b1a0b09c0e7c792b0a9662c08daecd212c027c89
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805162"
---
# <a name="onlinemeeting-resource-type"></a>tipo de recurso onlineMeeting

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Captura información acerca de la reunión, incluida la dirección URL de la combinación, la lista de los asistentes y la descripción.

## <a name="methods"></a>Métodos

| Método         | Tipo de valor devuelto | Descripción |
|:---------------|:--------|:----------|
| [Obtener onlineMeeting](../api/onlinemeeting-get.md) | [onlineMeeting](onlinemeeting.md) | Leer las propiedades y las relaciones del objeto onlineMeeting. |

## <a name="properties"></a>Propiedades

| Propiedad                  | Tipo                                                   | Description                                                                                                                |
| :------------------------ | :----------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------- |
| accessLevel               | Cadena                                                 | El nivel de acceso que controla la admisión a la reunión en línea. Los valores posibles son: `everyone`, `invited`, `locked`, `sameEnterprise` y `unknown`. |
| Audioconferencia         | [Audioconferencia](audioconferencing.md)              | Representa la información de acceso telefónica de un onlineMeeting. |
| canceledDateTime          | DateTime                                               | La hora cuando se canceló la reunión. |
| chatInfo                  | [chatInfo](chatinfo.md)                                | El chat asociado a esta reunión. |
| creationDateTime          | DateTime                                               | La hora de creación de la reunión. ReadOnly.
| endDateTime               | DateTime                                               | Hora de finalización de la reunión. |
| entryExitAnnouncement     | Booleano                                                | El estado de anuncios de asistencia para la reunión en línea. Cuando se habilitan los anuncios de asistencia, la reunión en línea anunciar los nombres de la combinación de participantswho la reunión a través de audio. |
| expirationDateTime        | DateTime                                               | La fecha de la hora Universal coordinada (UTC) y la hora después de la cual absoluta se puede eliminar la reunión en línea. El día y la hora deben estar comprendido entre un año antes y diez años después, la fecha y hora actuales en el servidor. |
| id                        | Cadena                                                 | El identificador asociado con la reunión en línea. Usar en una solicitud GET HTTP como el identificador. Solo lectura. Servidor que se generó. |
| isCancelled               | Booleano                                                | Si se ha cancelado la reunión. |
| joinUrl                   | Cadena                                                 | La dirección URL que se usa cuando se se unió a la reunión en línea desde la web. |
| meetingType               | Cadena                                                 | Los valores posibles son: `meetNow`, `scheduled`, `recurring`,`broadcast` |
| participants              | [meetingParticipants](meetingparticipants.md)          | Los participantes asociados a la reunión en línea.  Esto incluye el organizador y los asistentes. |
| startDateTime             | DateTime                                               | Hora de inicio de la reunión. |
| subject                   | Cadena                                                 | El asunto de la reunión en línea. |

## <a name="relationships"></a>Relaciones
Ninguno

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onlineMeeting"
}-->
```json
{
  "accessLevel": "everyone | invited | locked | sameEnterprise",
  "audioConferencing": {"@odata.type": "#microsoft.graph.audioConferencing"},
  "canceledDateTime": "String (timestamp)",
  "chatInfo": {"@odata.type": "#microsoft.graph.chatInfo"},
  "creationDateTime": "String (timestamp)",
  "endDateTime": "String (timestamp)",
  "entryExitAnnouncement": true,
  "expirationDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "isCancelled": false,
  "joinUrl": "String",
  "meetingType": "meetNow | scheduled | recurring | broadcast",
  "participants": {"@odata.type": "#microsoft.graph.meetingParticipants"},
  "startDateTime": "String (timestamp)",
  "subject": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onlineMeeting resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
