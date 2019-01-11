---
title: tipo de recurso de llamada
description: El recurso **de llamadas** se crea cuando hay una llamada entrante de la aplicación o la aplicación crea una nueva llamada saliente a través de un `POST` en `app/calls`.
author: VinodRavichandran
localization_priority: Priority
ms.openlocfilehash: d2748b410352effb7119a569bdf48c86f2f7c2ad
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27810706"
---
# <a name="call-resource-type"></a>tipo de recurso de llamada

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **de llamadas** se crea cuando hay una llamada entrante de la aplicación o la aplicación crea una nueva llamada saliente a través de un `POST` en `app/calls`.

Pueden configurar las llamadas como un punto a punto o como una llamada entre varias partes. Para crear o unirse a una llamada entre varias partes, proporcionar el `chatInfo` y `meetingInfo`. Si no se proporcionan estos, se crea automáticamente una nueva reunión ad hoc. Para una llamada entrante, registre estos valores en un almacén altamente disponible, por lo que la aplicación para volver a unirse a la llamada en el caso de que la aplicación se bloquea.

Aunque la misma identidad no puede ser invitada varias veces, es posible para una aplicación para unirse a la misma de la reunión varias veces. Cada vez que las combinaciones de aplicación, una llamada distinta `id` sirve para la llamada a la reunión. Se recomienda que utilice identidades diferentes para unirse a la reunión en orden para los clientes que se muestren los participantes como diferentes.

## <a name="methods"></a>Métodos

| Método                                                            | Tipo de valor devuelto                                       | Descripción                                  |
|:------------------------------------------------------------------|:--------------------------------------------------|:---------------------------------------------|
| [Obtener la llamada](../api/call-get.md)                                    | [llamada](call.md)                                   | Leer las propiedades del objeto de **llamada** .      |
| [Delete](../api/call-delete.md)                                   |                                                   | Eliminar o Colgar un activo **de llamadas**.        |
| **Control de llamadas**                                                 |                                                   |                                              |
| [Respuesta](../api/call-answer.md)                                   |                                                   | Responder a una llamada entrante.                     |
| [Reject](../api/call-reject.md)                                   |                                                   | Rechazar una llamada entrante.                     |
| [Redirigir](../api/call-redirect.md)                               |                                                   | Redirigir una llamada entrante.                   |
| [Transfer](../api/call-transfer.md)                               |                                                   | Transferir una llamada                              |
| **Multi-party**                                                   |                                                   |                                              |
| [Participantes de la lista](../api/call-list-participants.md)             | colección de [participante](participant.md)          | Obtener una colección de objetos de participantes.         |
| [Invitar a participantes](../api/participant-invite.md)               | [commsOperation](commsoperation.md)               | Invitar a participantes a la llamada activa.      |
| [Desactivar todos los participantes](../api/participant-muteall.md)            | [commsOperation](commsoperation.md)               | Silenciar a todos los participantes de la llamada.           |
| [Configurar el Mezclador de Audio](../api/participant-configuremixer.md)     | [commsOperation](commsoperation.md)               | Configurar el audio en una conversación entre varias partes.  |
| [Crear audioRoutingGroup](../api/call-post-audioroutinggroups.md)| [audioRoutingGroup](audioroutinggroup.md)         | Crear un nuevo audioRoutingGroup por la publicación de la colección audioRoutingGroups. |
| [Lista audioRoutingGroups](../api/call-list-audioroutinggroups.md) | colección de [audioRoutingGroup](audioroutinggroup.md)|Obtener una colección de objetos audioRoutingGroup.  |
| **Respuesta interactiva de voz**                                    |                                                   |                                              |
| [PlayPrompt](../api/call-playprompt.md)                           | [playPromptOperation](playpromptoperation.md)     | Reproducir el símbolo del sistema en la llamada.                     |
| [Registro](../api/call-record.md)                                   | [recordOperation](recordoperation.md)             | Registro de la llamada.                             |
| [CancelMediaProcessing](../api/call-cancelmediaprocessing.md)     | [commsOperation](commsoperation.md)               | Cancelar el proceso de medios.                     |
| [SubscribeToTone](../api/call-subscribetotone.md)                 | [commsOperation](commsoperation.md)               | Suscribirse a tonos DTMF.                     |
| **Operaciones de participantes Self**                                   |                                                   |                                              |
| [Desactivación de audio](../api/call-mute.md)                                       | [commsOperation](commsoperation.md)               | Silenciar self en la llamada.                       |
| [Reactivar audio](../api/call-unmute.md)                                   | [commsOperation](commsoperation.md)               | Reactivar self en la llamada.                     |
| [UpdateMetadata](../api/call-updatemetadata.md)                   | [commsOperation](commsoperation.md)               | Actualizar los metadatos para sí mismo en la lista de participantes.          |
| [ChangeScreenSharingRole](../api/call-changescreensharingrole.md) |                                                   | Iniciar y detener el uso compartido de pantalla en la llamada                                             |

## <a name="properties"></a>Propiedades

| Propiedad            | Tipo                                                                                                   | Description                                                                                                                                                                                         |
| :------------------ | :------------------------------------------------------------------------------------------------------| :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| activeModalities    | Colección de cadenas                                                                                      | La lista de modalidades activos. Los valores posibles son: `unknown`, `audio`, `video`, `videoBasedScreenSharing` y `data`. Solo lectura. Servidor que se generó.                                                    |
| answeredBy          | [participantInfo](participantinfo.md)                                                                  | El participante que ha atendido la llamada. Solo lectura. Servidor que se generó.                                                                                                                                |
| callRoutes          | colección de [callRoute](callroute.md)                                                                   | La información de enrutamiento en cómo se redestinar la llamada. Solo lectura. Servidor que se generó.                                                                                                                |
| callbackUri         | Cadena                                                                                                 | El identificador de suscripción o de devolución de llamada en la que se entregarán las devoluciones de llamada.                                                                                                                               |
| chatInfo            | [chatInfo](chatinfo.md)                                                                                | La información de chat.                                                                                                                                                                               |
| dirección           | Cadena                                                                                                 | La dirección de la llamada. Los valores posibles son `incoming` o `outgoing`. Solo lectura. Servidor que se generó.                                                                                            |
| id                  | Cadena                                                                                                 | Solo lectura. Servidor que se generó.                                                                                                                                                                        |
| mediaConfig         | [appHostedMediaConfig](apphostedmediaconfig.md) o [serviceHostedMediaConfig](servicehostedmediaconfig.md) | La configuración de medios.                                                                                                                                                                        |
| meetingCapability   | [meetingCapability](meetingcapability.md)                                                              | Contiene las funciones de una reunión.                                                                                                                                                             |
| meetingInfo         | [organizerMeetingInfo](organizermeetinginfo.md) o [tokenMeetingInfo](tokenmeetinginfo.md)             | La información de la reunión.                                                                                                                                                                            |
| myParticipantId     | Cadena                                                                                                 | Solo lectura. Servidor que se generó.                                                                                                                                                                        |
| requestedModalities | Colección String                                                                                      | La lista de modalidades solicitados. | Los valores posibles son: `unknown`, `audio`, `video`, `videoBasedScreenSharing` y `data`.                                                                            |
| resultInfo          | [resultInfo](resultinfo.md)                                                                            | La información del resultado. Por ejemplo puede contener motivo terminación. Solo lectura. Servidor que se generó.                                                                                                       |
| ringingTimeoutInSeconds | Int32                                                                                              | Tiempo de espera de llamadas para las llamadas salientes de punto a punto                                                                                                                                                     |
| routingPolicies     | Colección String                                                                                      | Los valores posibles son: `none`, `noMissedCall`, `disableForwardingExceptPhone` y `disableForwarding`.                                                                                                   |
| source              | [participantInfo](participantinfo.md)                                                                  | El autor de la llamada.                                                                                                                                                                         |
| state               | Cadena                                                                                                 | El estado de la llamada. Los valores posibles son: `incoming`, `establishing`, `ringing`, `established`, `hold`, `transferring`, `transferAccepted`, `redirecting`, `terminating` y `terminated`. Solo lectura. Servidor que se generó.                         |
| subject             | Cadena                                                                                                 | El asunto de la conversación.                                                                                                                                                                    |
| objetivos             | colección de [participantInfo](participantinfo.md)                                                       | Los destinos de la llamada.                                                                                                                                                                            |
| tenantId            | Cadena                                                                                                 | tenantId en Azure Active Directory.                                                                                                                                                                 |
| terminationReason   | Cadena                                                                                                 | Solo lectura. Servidor que se generó.                                                                                                                                                                        |
| toneInfo            | [toneInfo](toneinfo.md)                                                                                | Solo lectura. Servidor que se generó.                                                                                                                                                                        |

> Nota: Las propiedades marcan como `Server generated` se pasan por alto al procesar `POST` en `app/calls`.

## <a name="relationships"></a>Relaciones

| Relación        | Tipo                                                 | Description                                                         |
|:--------------------|:-----------------------------------------------------|:--------------------------------------------------------------------|
| audioRoutingGroups  | colección de [audioRoutingGroup](audioroutinggroup.md) | Solo lectura. Admite valores NULL.                                                |
| operaciones          | colección de [commsOperation](commsoperation.md)       | Solo lectura. Admite valores NULL.                                                |
| participants        | colección de [participante](participant.md)             | Solo lectura. Admite valores NULL.                                                |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "activeModalities",
    "answeredBy",
    "callRoutes",
    "chatInfo",
    "direction",
    "id",
    "meetingCapability",
    "meetingInfo",
    "myParticipantId",
    "resultInfo",
    "ringingTimeoutInSeconds",
    "routingPolicies",
    "state",
    "targets",
    "tenantId",
    "terminationReason",
    "toneInfo"
  ],
  "@odata.type": "microsoft.graph.call"
}-->
```json
{
  "activeModalities": ["unknown | audio | video | videoBasedScreenSharing | data"],
  "answeredBy": {"@odata.type": "#microsoft.graph.participantInfo"},
  "callRoutes": [{"@odata.type": "#microsoft.graph.callRoute"}],
  "callbackUri": "String",
  "chatInfo": {"@odata.type": "#microsoft.graph.chatInfo"},
  "direction": "incoming | outgoing",
  "id": "String (identifier)",
  "mediaConfig": {"@odata.type": "#microsoft.graph.mediaConfig"},
  "meetingCapability": {"@odata.type": "#microsoft.graph.meetingCapability"},
  "meetingInfo": {"@odata.type": "#microsoft.graph.meetingInfo"},
  "myParticipantId": "String",
  "requestedModalities": ["unknown | audio | video | videoBasedScreenSharing | data"],
  "resultInfo": {"@odata.type": "#microsoft.graph.resultInfo"},
  "ringingTimeoutInSeconds": 1024,
  "routingPolicies": ["none | noMissedCall | disableForwardingExceptPhone | disableForwarding"],
  "source": {"@odata.type": "#microsoft.graph.participantInfo"},
  "state": "incoming | establishing | ringing | established | hold | transferring | transferAccepted | redirecting | terminating | terminated",
  "subject": "String",
  "targets": [{"@odata.type": "#microsoft.graph.participantInfo"}],
  "tenantId": "String",
  "terminationReason": "String",
  "toneInfo": {"@odata.type": "#microsoft.graph.toneInfo"}
}
```

> **Nota:** Se encuentra la dirección URL de la combinación de una reunión programada con Microsoft Teams. Aquí es cómo extraer los datos de la dirección URL y relleno `chatInfo` y `meetingInfo`.

```http
https://teams.microsoft.com/l/meetup-join/19%3ameeting_NTg0NmQ3NTctZDVkZC00YzRhLThmNmEtOGQ3M2E0ODdmZDZk%40thread.v2/0?context=%7b%22Tid%22%3a%2272f988bf-86f1-41af-91ab-2d7cd011db47%22%2c%22Oid%22%3a%224b444206-207c-42f8-92a6-e332b41c88a2%22%7d
decodes to:
https://teams.microsoft.com/l/meetup-join/19:meeting_NTg0NmQ3NTctZDVkZC00YzRhLThmNmEtOGQ3M2E0ODdmZDZk@thread.v2/0?context={"Tid":"72f988bf-86f1-41af-91ab-2d7cd011db47","Oid":"4b444206-207c-42f8-92a6-e332b41c88a2"}
```

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.call",
  truncated: true
}-->
```json
{
  "chatInfo": {
    "threadId": "19:meeting_NTg0NmQ3NTctZDVkZC00YzRhLThmNmEtOGQ3M2E0ODdmZDZk@thread.v2",
    "messageId": "0",
    "replyChainMessageId": "0"
  },
  "meetingInfo": {
    "@odata.type": "#microsoft.graph.organizerMeetingInfo",
    "organizer": {
      "user": {
        "tenantId": "72f988bf-86f1-41af-91ab-2d7cd011db47",
        "id": "4b444206-207c-42f8-92a6-e332b41c88a2"
      }
    }
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "call resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
