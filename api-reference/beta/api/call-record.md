---
title: 'llamar a: registro'
description: Registro de la llamada.
author: VinodRavichandran
ms.openlocfilehash: 5de56ca417f5a6d06e8116802eeba2dd3d39e399
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27303552"
---
# <a name="call-record"></a>llamar a: registro

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Registro de la llamada.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

| Tipo de permiso | Permisos (de menos a más privilegiados) |
| :-------------- | :------------------------------------------ |
| Delegado (cuenta profesional o educativa)     | No se admite        |
| Delegado (cuenta personal de Microsoft) | No se admite        |
| Aplicación     | Calls.AccessMedia.All                       |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /app/calls/{id}/record
POST /applications/{id}/calls/{id}/record
```

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre          | Descripción               |
|:--------------|:--------------------------|
| Authorization | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.

| Parámetro      | Type    |Descripción|
|:---------------|:--------|:----------|
|solicita|colección de [mediaprompt](../resources/mediaprompt.md) | Colección de indicaciones para reproducir (si hay alguno) antes de la grabación se iniciará. Los clientes pueden elegir especificar la acción "playPrompt" por separado o especificar como parte de "registro" - principalmente todos los registros están precedido por un símbolo del sistema |
|bargeInAllowed|Boolean| Permitir que los usuarios escriban opción antes de que finalice el símbolo del sistema.                                                                 |
|initialSilenceTimeoutInSeconds | Int32| Silencio inicial máximo permitido desde el momento en que se inicia la operación de registro antes de la operación de conmutación por error y tiempo de espera. Si se está reproduciendo un símbolo del sistema, este temporizador se inicia después de que finalice el símbolo del sistema. |
|maxSilenceTimeoutInSeconds|Int32| El tiempo de espera máximo silencio en segundos.|
|maxRecordDurationInSeconds|Int32| La duración de registro máximo en segundos.|
|playBeep|Boolean| Emite un pitido tras reproducir el símbolo del sistema.|
|streamWhileRecording|Boolean|Si se establece en true, una ubicación de recursos será proporcionado en cuanto se inicia la grabación. |
|stopTones|Colección String|Detener tonos especificados para finalizar la grabación.|
|clientContext|String|El contexto de cliente.|

## <a name="response"></a>Respuesta
Devuelve `202 Accepted` código de respuesta y un encabezado de ubicación con un uri para el [commsOperation](../resources/commsoperation.md) creado para esta solicitud.

## <a name="example"></a>Ejemplo
En el siguiente ejemplo se muestra cómo llamar a esta API.

##### <a name="request"></a>Solicitud
En el ejemplo siguiente se muestra la solicitud.

<!-- {
  "blockType": "request",
  "name": "call_record"
}-->
```http
POST https://graph.microsoft.com/beta/app/calls/{id}/record
Content-Type: application/json
Content-Length: 394

{
  "bargeInAllowed": true,
  "clientContext": "d45324c1-fcb5-430a-902c-f20af696537c",
  "prompts": [
    {
      "@odata.type": "#microsoft.graph.mediaPrompt",
      "mediaInfo": {
        "uri": "https://cdn.contoso.com/beep.wav",
        "resourceId": "1D6DE2D4-CD51-4309-8DAA-70768651088E"
      },
      "loop": 5
    }
  ],
  "maxRecordDurationInSeconds": 1800,
  "initialSilenceTimeoutInSeconds": 10,
  "maxSilenceTimeoutInSeconds": 2,
  "recordingFormat": "wav",
  "playBeep": true,
  "streamWhileRecording": true,
  "stopTones": [ "#", "11", "*" ]
}
```

##### <a name="response"></a>Respuesta

> **Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.recordOperation"
} -->
```http
HTTP/1.1 202 Accepted
Location: https://graph.microsoft.com/beta/app/calls/57dab8b1-894c-409a-b240-bd8beae78896/operations/0fe0623f-d628-42ed-b4bd-8ac290072cc5
```

##### <a name="notification---operation-completed"></a>Notificación: la operación se terminó

```http
POST https://bot.contoso.com/api/calls
Authorization: Bearer <TOKEN>
Content-Type: application/json
```

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.commsNotifications"
}-->
```json
{
  "value": [
    {
      "changeType": "deleted",
      "resource": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896/operations/0FE0623FD62842EDB4BD8AC290072CC5",
      "resourceData": {
        "@odata.type": "#microsoft.graph.recordOperation",
        "@odata.id": "/app/calls/57DAB8B1894C409AB240BD8BEAE78896/operations/0FE0623FD62842EDB4BD8AC290072CC5",
        "@odata.etag": "W/\"54451\"",
        "clientContext": "d45324c1-fcb5-430a-902c-f20af696537c",
        "status": "completed",
        "recordResourceLocation": "https://file.location/17e3b46c-f61d-4f4d-9635-c626ef18e6ad",
        "recordResourceAccessToken": "<access-token>",
        "completionReason": "stopToneDetected"
      }
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "call: record",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
