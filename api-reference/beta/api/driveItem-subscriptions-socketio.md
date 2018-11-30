---
title: Obtener el extremo de websocket
description: No se admite el uso de estas API en aplicaciones de producción.
ms.openlocfilehash: c84bc3bdd3096a745cf21f282273694e63ab3afb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084581"
---
# <a name="get-websocket-endpoint"></a><span data-ttu-id="2d344-103">Obtener el extremo de websocket</span><span class="sxs-lookup"><span data-stu-id="2d344-103">Get websocket endpoint</span></span>

> <span data-ttu-id="2d344-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2d344-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span>
<span data-ttu-id="2d344-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2d344-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2d344-106">Le permite recibir notificaciones de cambio de casi en tiempo real para una [unidad][] mediante [socket.io][].</span><span class="sxs-lookup"><span data-stu-id="2d344-106">Allows you to receive near-real-time change notifications for a [drive][] using [socket.io][].</span></span>
<span data-ttu-id="2d344-107">Socket.IO es una biblioteca de notificaciones populares para JavaScript que utiliza WebSockets.</span><span class="sxs-lookup"><span data-stu-id="2d344-107">Socket.io is a popular notifications library for JavaScript that utilizes WebSockets.</span></span> <span data-ttu-id="2d344-108">Para obtener más información, vea [socket.io](https://socket.io).</span><span class="sxs-lookup"><span data-stu-id="2d344-108">To learn more, see [socket.io](https://socket.io).</span></span>

[unidad]: ../resources/drive.md
[drive]: ../resources/drive.md
[Socket.IO]: https://socket.io/
[socket.io]: https://socket.io/

## <a name="permissions"></a><span data-ttu-id="2d344-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="2d344-111">Permissions</span></span>

<span data-ttu-id="2d344-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2d344-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="2d344-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2d344-114">Permission type</span></span>                        | <span data-ttu-id="2d344-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2d344-115">Permissions (from least to most privileged)</span></span>
|:---------------------------------------|:-------------------------------------------
| <span data-ttu-id="2d344-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2d344-116">Delegated (work or school account)</span></span>     | <span data-ttu-id="2d344-117">Files.Read, Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2d344-117">Files.Read, Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>
| <span data-ttu-id="2d344-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2d344-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2d344-119">Files.Read, Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2d344-119">Files.Read, Files.ReadWrite, Files.ReadWrite.All</span></span>
| <span data-ttu-id="2d344-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2d344-120">Application</span></span>                            | <span data-ttu-id="2d344-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2d344-121">Not supported.</span></span>

## <a name="http-request"></a><span data-ttu-id="2d344-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2d344-122">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /me/drive/root/subscriptions/socketIo
GET /drives/{driveId}/root/subscriptions/socketIo
GET /groups/{groupId}/drive/root/subscriptions/socketIo
GET /sites/{siteId}/lists/{listId}/drive/root/subscriptions/socketIo
```

## <a name="example"></a><span data-ttu-id="2d344-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2d344-123">Example</span></span>

### <a name="request"></a><span data-ttu-id="2d344-124">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2d344-124">Request</span></span>

<!-- { "blockType": "request", "name": "drive_root_subscriptions_socketIo" } -->
```http
GET /me/drive/root/subscriptions/socketIo
```

### <a name="response"></a><span data-ttu-id="2d344-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2d344-125">Response</span></span>

<span data-ttu-id="2d344-126">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto de [suscripción](../resources/subscription.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2d344-126">If successful, this method returns a `200 OK` response code and a [subscription](../resources/subscription.md) object in the response body.</span></span>

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

<span data-ttu-id="2d344-127">El `notificationUrl` devuelta es una dirección URL de extremo de socket.io.</span><span class="sxs-lookup"><span data-stu-id="2d344-127">The `notificationUrl` returned is a socket.io endpoint URL.</span></span>
<span data-ttu-id="2d344-128">Para usarlo con un cliente de socket.io, dividir la cadena en el `/callback?` token.</span><span class="sxs-lookup"><span data-stu-id="2d344-128">To use it with a socket.io client, split the string on the `/callback?` token.</span></span>
<span data-ttu-id="2d344-129">La parte de la cadena antes de `/callback?` es la dirección URL de extremo de socket.io y la parte de la cadena después es una cadena de consulta opaco que se debe dar a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="2d344-129">The part of the string before `/callback?` is the socket.io endpoint URL and the part of the string after is an opaque query string that must be given to the libary.</span></span>

<span data-ttu-id="2d344-130">En el ejemplo siguiente se muestra cómo usar la `notificationUrl` con socket.io en JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2d344-130">The following example shows how to use the `notificationUrl` with socket.io in JavaScript.</span></span>

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
