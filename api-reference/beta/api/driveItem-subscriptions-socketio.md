---
title: Obtener el extremo de websocket
description: No se admite el uso de estas API en aplicaciones de producción.
localization_priority: Normal
ms.openlocfilehash: a981a4d02d2e40fec0cb2bca397c7b7794d36867
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27859797"
---
# <a name="get-websocket-endpoint"></a>Obtener el extremo de websocket

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.
No se admite el uso de estas API en aplicaciones de producción.

Le permite recibir notificaciones de cambio de casi en tiempo real para una [unidad][] mediante [socket.io][].
Socket.IO es una biblioteca de notificaciones populares para JavaScript que utiliza WebSockets. Para obtener más información, vea [socket.io](https://socket.io).

[unidad]: ../resources/drive.md
[Socket.IO]: https://socket.io/

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

| Tipo de permiso                        | Permisos (de menos a más privilegiados)
|:---------------------------------------|:-------------------------------------------
| Delegado (cuenta profesional o educativa)     | Files.Read, Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All
| Delegado (cuenta personal de Microsoft) | Files.Read, Files.ReadWrite, Files.ReadWrite.All
| Aplicación                            | No admitida.

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
GET /me/drive/root/subscriptions/socketIo
GET /drives/{driveId}/root/subscriptions/socketIo
GET /groups/{groupId}/drive/root/subscriptions/socketIo
GET /sites/{siteId}/lists/{listId}/drive/root/subscriptions/socketIo
```

## <a name="example"></a>Ejemplo

### <a name="request"></a>Solicitud

<!-- { "blockType": "request", "name": "drive_root_subscriptions_socketIo" } -->
```http
GET /me/drive/root/subscriptions/socketIo
```

### <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto de [suscripción](../resources/subscription.md) en el cuerpo de la respuesta.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.subscription"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "id": "opaqueId-fj3hd7yf283jfk193726nvc2w3i2diemdu8",
  "notificationUrl": "https://f3hb0mpua.svc.ms/zbaehwg/callback?snthgk=1ff3-2345672zz831837523"
}
```

El `notificationUrl` devuelta es una dirección URL de extremo de socket.io.
Para usarlo con un cliente de socket.io, dividir la cadena en el `/callback?` token.
La parte de la cadena antes de `/callback?` es la dirección URL de extremo de socket.io y la parte de la cadena después es una cadena de consulta opaco que se debe dar a la biblioteca.

En el ejemplo siguiente se muestra cómo usar la `notificationUrl` con socket.io en JavaScript.

```javascript
// this is the notificationUrl returned from this API
var notificationUrl = "https://f3hb0mpua.svc.ms/zbaehwg/callback?snthgk=1ff3-2345672zz831837523";

// after the split, split[0] will be everything leading up to '/callback?' and split[1] will be everything after.
var split = notificationUrl.split("/callback?");

// 'io' comes from the socket.io client library
var socket = io(split[0], { query: split[1] });

// these examples log to the console.
// your app would provide its own callbacks
socket.on("connect", ()=>console.log("Connected!"));
socket.on("notification", (data)=>console.log("Notification!", data));
```

<!-- {
  "type": "#page.annotation"
}-->
