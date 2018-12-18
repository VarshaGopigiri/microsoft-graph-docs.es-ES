---
title: Obtener los cambios incrementales en los mensajes de una carpeta
description: La consulta de delta permite consultar las adiciones, eliminaciones o actualizaciones a los mensajes de una carpeta, por medio de una serie de
author: piotrci
ms.openlocfilehash: 4325826ee3d94766fac5bb345d4311bd03b1fb89
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27346553"
---
# <a name="get-incremental-changes-to-messages-in-a-folder"></a><span data-ttu-id="b9da6-103">Obtener los cambios incrementales en los mensajes de una carpeta</span><span class="sxs-lookup"><span data-stu-id="b9da6-103">Get incremental changes to messages in a folder</span></span>

<span data-ttu-id="b9da6-p101">Consulta de delta permite consultar las adiciones, eliminaciones o actualizaciones a los mensajes de una carpeta, por medio de una serie de llamadas a función [delta](/graph/api/message-delta?view=graph-rest-1.0). Los datos de delta permiten mantener y sincronizar un almacén local de mensajes de un usuario, sin tener que capturar cada vez todo el conjunto de mensajes del usuario desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="b9da6-p101">Delta query lets you query for additions, deletions, or updates to messages in a folder, by way of a series of [delta](/graph/api/message-delta?view=graph-rest-1.0) function calls. Delta data enables you to maintain and synchronize a local store of a user's messages, without having to fetch the entire set of the user's messages from the server every time.</span></span>

<span data-ttu-id="b9da6-p102">La consulta de delta admite la sincronización completa que recupera todos los mensajes de una carpeta (por ejemplo, la bandeja de entrada del usuario) y la sincronización incremental que recupera todos los mensajes que cambiaron en la carpeta desde la última sincronización. Normalmente, se debería realizar una sincronización completa inicial de todos los mensajes de una carpeta y, después, obtener los cambios incrementales en la carpeta de forma periódica.</span><span class="sxs-lookup"><span data-stu-id="b9da6-p102">Delta query supports both full synchronization that retrieves all of the messages in a folder (for example, the user's Inbox), and incremental synchronization that retrieves all of the messages that have changed in that folder since the last synchronization. Typically, you would do an initial full synchronization of all the messages in a folder, and subsequently, get incremental changes to that folder periodically.</span></span>

## <a name="track-message-changes-in-a-folder"></a><span data-ttu-id="b9da6-108">Seguimiento de cambios de mensajes en una carpeta</span><span class="sxs-lookup"><span data-stu-id="b9da6-108">Track message changes in a folder</span></span>

<span data-ttu-id="b9da6-p103">La consulta de delta es una operación por carpeta. Para realizar el seguimiento de los cambios de los mensajes en una jerarquía de carpetas, debe realizar un seguimiento de cada carpeta de forma individual.</span><span class="sxs-lookup"><span data-stu-id="b9da6-p103">Delta query is a per-folder operation. To track the changes of the messages in a folder hierarchy, you need to track each folder individually.</span></span>

<span data-ttu-id="b9da6-p104">El seguimiento de los cambios de mensajes en una carpeta de correo normalmente es una ronda de una o varias solicitudes GET con la función **delta**. La solicitud GET inicial es muy similar a la forma de [obtener mensajes](/graph/api/user-list-messages?view=graph-rest-1.0), salvo que se incluye la función **delta**:</span><span class="sxs-lookup"><span data-stu-id="b9da6-p104">Tracking message changes in a mail folder typically is a round of one or more GET requests with the **delta** function. The initial GET request is very much like the way you [get messages](/graph/api/user-list-messages?view=graph-rest-1.0), except that you include the **delta** function:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/mailFolders/{id}/messages/delta
```

<span data-ttu-id="b9da6-113">Una solicitud GET con la función **delta** función devuelve:</span><span class="sxs-lookup"><span data-stu-id="b9da6-113">A GET request with the **delta** function returns either:</span></span>

- <span data-ttu-id="b9da6-114">Un `nextLink` (que contiene una dirección URL con una llamada de función **delta** y un _skipToken_), o</span><span class="sxs-lookup"><span data-stu-id="b9da6-114">A `nextLink` (that contains a URL with a **delta** function call and a _skipToken_), or</span></span>
- <span data-ttu-id="b9da6-115">Un `deltaLink` (que contiene una dirección URL con una llamada de función **delta** y un _deltaToken_).</span><span class="sxs-lookup"><span data-stu-id="b9da6-115">A `deltaLink` (that contains a URL with a **delta** function call and _deltaToken_).</span></span>

<span data-ttu-id="b9da6-p105">Estos tokens son [tokens de estado](delta-query-overview.md#state-tokens) totalmente opacos para el cliente. Para continuar con una ronda de seguimiento de cambios, basta con copiar y aplicar la dirección URL devuelta desde la última solicitud GET a la siguiente llamada de función**delta** para la misma carpeta. Un `deltaLink` devuelto en una respuesta significa que la ronda actual de seguimiento de cambios está completa. Se puede guardar y usar la dirección URL `deltaLink` cuando se inicia la siguiente ronda.</span><span class="sxs-lookup"><span data-stu-id="b9da6-p105">These tokens are [state tokens](delta-query-overview.md#state-tokens) that are completely opaque to the client. To proceed with a round of change tracking, simply copy and apply the URL returned from the last GET request to the next **delta** function call for the same folder. A `deltaLink` returned in a response signifies that the current round of change tracking is complete. You can save and use the `deltaLink` URL when you begin the next round.</span></span>

<span data-ttu-id="b9da6-120">Vea el [ejemplo](#example-to-synchronize-messages-in-a-folder) siguiente para obtener información sobre cómo usar las direcciones URL `nextLink` y `deltaLink`.</span><span class="sxs-lookup"><span data-stu-id="b9da6-120">See the [example](#example-to-synchronize-messages-in-a-folder) below to learn how to use the `nextLink` and `deltaLink` URLs.</span></span>

### <a name="use-query-parameters-in-a-delta-query-for-messages"></a><span data-ttu-id="b9da6-121">Usar parámetros de consulta en una consulta de delta para los mensajes</span><span class="sxs-lookup"><span data-stu-id="b9da6-121">Use query parameters in a delta query for messages</span></span>

- <span data-ttu-id="b9da6-p106">Puede utilizar un parámetro de consulta `$select` como en cualquier solicitud GET para especificar solo las propiedades que necesita para un mejor rendimiento. Siempre se devuelve la propiedad `id`.</span><span class="sxs-lookup"><span data-stu-id="b9da6-p106">You can use a `$select` query parameter as in any GET request to specify only the properties your need for best performance. The `id` property is always returned.</span></span>
- <span data-ttu-id="b9da6-124">Compatibilidad con consultas de delta `$select`, `$top`, y `$expand` para los mensajes.</span><span class="sxs-lookup"><span data-stu-id="b9da6-124">Delta query support `$select`, `$top`, and `$expand` for messages.</span></span>
- <span data-ttu-id="b9da6-125">Hay compatibilidad limitada para `$filter` y `$orderby`:</span><span class="sxs-lookup"><span data-stu-id="b9da6-125">There is limited support for `$filter` and `$orderby`:</span></span>
  - <span data-ttu-id="b9da6-126">Las únicas expresiones `$filter` admitidas son `$filter=receivedDateTime+ge+{value}` y `$filter=receivedDateTime+gt+{value}`.</span><span class="sxs-lookup"><span data-stu-id="b9da6-126">The only supported `$filter` expressions are `$filter=receivedDateTime+ge+{value}` or `$filter=receivedDateTime+gt+{value}`.</span></span>
  - <span data-ttu-id="b9da6-p107">La única expresión `$orderby` admitida es `$orderby=receivedDateTime+desc`. Si no incluye una expresión `$orderby`, no se garantiza el orden de devolución.</span><span class="sxs-lookup"><span data-stu-id="b9da6-p107">The only supported `$orderby` expression is `$orderby=receivedDateTime+desc`. If you do not include an `$orderby` expression, the return order is not guaranteed.</span></span>
- <span data-ttu-id="b9da6-129">No hay compatibilidad con `$search`.</span><span class="sxs-lookup"><span data-stu-id="b9da6-129">There is no support for `$search`.</span></span>

### <a name="optional-request-header"></a><span data-ttu-id="b9da6-130">Encabezado de solicitud opcional</span><span class="sxs-lookup"><span data-stu-id="b9da6-130">Optional request header</span></span>

<span data-ttu-id="b9da6-131">Cada solicitud GET de la consulta delta devuelve una colección de uno o más mensajes en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b9da6-131">Each delta query GET request returns a collection of one or more messages in the response.</span></span> <span data-ttu-id="b9da6-132">Opcionalmente se puede especificar el encabezado de solicitud, `Prefer: odata.maxpagesize={x}`, para establecer el número máximo de mensajes en una respuesta.</span><span class="sxs-lookup"><span data-stu-id="b9da6-132">You can optionally specify the request header, `Prefer: odata.maxpagesize={x}`, to set the maximum number of messages in a response.</span></span>

<!--
### Iterative process

A typical round to track message changes goes like this:

1. Make the initial GET request with the mandatory _Prefer: odata.track-changes_ header. If this is your very first delta query
for messages in that folder, don't provide any state token. If the messages support tracking changes, following the iterative
process (steps 2-6) described below will return the entire set of messages in that folder.

2. Check if the first response returns the _Preference-Applied: odata.track-changes_ header,
which confirms your resource supports tracking changes. Stop if you don't receive the response header.

3. If you receive a _skipToken_ (in an _@odata.nextLink_ response header) in the response, you should continue to track the
   additional messages that have changed (added, deleted, or updated). Make a second GET request, using the URL returned
   in _@odata.nextLink_, which includes a _skipToken_.

4. The second request will return additional messages that have changed, and either a _skipToken_ if there are more changed messages,
  or a _deltaToken_ if all the changed messages have been returned.

5. If you receive a _skipToken_ from the last GET request, continue getting the changes by sending a next GET call, similar to step 3.

6. When you eventually receive a _deltaToken (in an _@odata.deltaLink_ response header) in the response from a GET, stop. This
round of change tracking is complete.

7. Save the _deltaToken_. The next time you track changes for the same folder, make a GET request
similar to step 1, except that now you can use this _deltaToken_ to get just the delta data (messages that have been added, deleted or updated)
since the completion of the very first round.

-->

## <a name="example-to-synchronize-messages-in-a-folder"></a><span data-ttu-id="b9da6-133">Ejemplo para sincronizar los mensajes de una carpeta</span><span class="sxs-lookup"><span data-stu-id="b9da6-133">Example to synchronize messages in a folder</span></span>

<span data-ttu-id="b9da6-134">En el siguiente ejemplo se muestran dos rondas de sincronización de una carpeta concreta que inicialmente contiene cinco mensajes.</span><span class="sxs-lookup"><span data-stu-id="b9da6-134">The following example shows 2 rounds of synchronization of a specific folder which initially contains 5 messages.</span></span>

<span data-ttu-id="b9da6-135">La primera ronda implica una serie de tres solicitudes para sincronizar los cinco mensajes de la carpeta:</span><span class="sxs-lookup"><span data-stu-id="b9da6-135">The first round involves a series of 3 requests to synchronize all 5 messages in the folder:</span></span>

- <span data-ttu-id="b9da6-136">[Solicitud inicial de ejemplo](#sample-initial-request) y [respuesta](#sample-initial-response)</span><span class="sxs-lookup"><span data-stu-id="b9da6-136">[Sample initial request](#sample-initial-request) and [response](#sample-initial-response)</span></span>
- <span data-ttu-id="b9da6-137">[Segunda solicitud de ejemplo](#sample-second-request) y [respuesta](#sample-second-response)</span><span class="sxs-lookup"><span data-stu-id="b9da6-137">[Sample second request](#sample-second-request) and [response](#sample-second-response)</span></span>
- <span data-ttu-id="b9da6-138">[Tercera solicitud de ejemplo](#sample-third-request) y [respuesta final](#sample-third-and-final-response)</span><span class="sxs-lookup"><span data-stu-id="b9da6-138">[Sample third request](#sample-third-request) and [final response](#sample-third-and-final-response)</span></span>

<span data-ttu-id="b9da6-139">Después de la primera ronda, uno de los mensajes se elimina y otro se marca como leído.</span><span class="sxs-lookup"><span data-stu-id="b9da6-139">After the first round, one of the messages is deleted, and another is marked as read.</span></span> <span data-ttu-id="b9da6-140">La [segunda ronda](#synchronize-messages-in-the-same-folder-in-the-next-round) de sincronización devuelve solo el delta (la eliminación y actualización) sin devolver los demás mensajes que se han mantenido iguales.</span><span class="sxs-lookup"><span data-stu-id="b9da6-140">The [second round](#synchronize-messages-in-the-same-folder-in-the-next-round) of synchronization returns only the delta (the deletion and update), without returning the other messages that have remained the same.</span></span>

### <a name="sample-initial-request"></a><span data-ttu-id="b9da6-141">Solicitud inicial de ejemplo</span><span class="sxs-lookup"><span data-stu-id="b9da6-141">Sample initial request</span></span>

<span data-ttu-id="b9da6-p110">En este ejemplo, se sincroniza por primera vez la carpeta especificada, por lo que la solicitud de sincronización inicial no incluye ningún token de estado. Esa ronda devolverá todos los mensajes de esa carpeta.</span><span class="sxs-lookup"><span data-stu-id="b9da6-p110">In this example, the specified folder is being synchronized for the first time, so the initial sync request does not include any state token. This round will return all the messages in that folder.</span></span>

<span data-ttu-id="b9da6-144">La primera solicitud especifica lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b9da6-144">The first request specifies the following:</span></span>

- <span data-ttu-id="b9da6-145">Un parámetro `$select` que devuelva las propiedades `subject`, `sender` y `isRead` de cada mensaje de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b9da6-145">A `$select` parameter to return the `subject`, `sender`, and `isRead` properties for each message in the response.</span></span>
- <span data-ttu-id="b9da6-146">El [encabezado de solicitud opcional](#optional-request-header), _odata.maxpagesize_, que devuelve dos mensajes a la vez.</span><span class="sxs-lookup"><span data-stu-id="b9da6-146">The [optional request header](#optional-request-header), _odata.maxpagesize_, returning 2 messages at a time.</span></span>

<!-- {
  "blockType": "ignored",
  "sampleKeys": ["AQMkADNkNAAAgEMAAAA"],
  "name": "get_messages_delta_1"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/mailfolders/AQMkADNkNAAAgEMAAAA/messages/delta?$select=subject,sender,isRead HTTP/1.1
Prefer: odata.maxpagesize=2
```

### <a name="sample-initial-response"></a><span data-ttu-id="b9da6-147">Respuesta inicial de ejemplo</span><span class="sxs-lookup"><span data-stu-id="b9da6-147">Sample initial response</span></span>

<span data-ttu-id="b9da6-p111">La respuesta incluye dos mensajes y un encabezado de respuesta `@odata.nextLink`. La dirección URL `nextLink` indica que la carpeta contiene más mensajes que recuperar.</span><span class="sxs-lookup"><span data-stu-id="b9da6-p111">The response includes two messages and an `@odata.nextLink` response header. The `nextLink` URL indicates there are more messages in the folder to get.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message",
  "isCollection": true
} -->

```json
{
  "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Collection(message)",
  "@odata.nextLink": "https://graph.microsoft.com/v1.0/me/mailfolders('AQMkADNkNAAAgEMAAAA')/messages/delta?$skiptoken=GwcBoTmPuoTQWfcsAbkYM",
  "value": [
    {
      "@odata.type": "#microsoft.graph.message",
      "@odata.etag": "W/\"CQAAABYAAAARn2vdzPFjSbaPPxzjlzOTAAASsKZz\"",
      "subject": "Holiday hours update",
      "isRead": "false",
      "sender": {
        "emailAddress": {
          "name": "Dana Swope",
          "address": "danas@contoso.onmicrosoft.com"
        }
      },
      "id": "AAMkADNkNAAASq35xAAA="
    },
    {
      "@odata.type": "#microsoft.graph.message",
      "@odata.etag": "W/\"CQAAABYAAAARn2vdzPFjSbaPPxzjlzOTAAAEfYB/\"",
      "subject": "Holiday promotion sale",
      "isRead": "true",
      "sender": {
        "emailAddress": {
          "name": "Samantha Booth",
          "address": "samanthab@contoso.onmicrosoft.com"
        }
      },
      "id": "AQMkADNkNAAAVRMKAAAAA=="
    }
  ]
}
```

### <a name="sample-second-request"></a><span data-ttu-id="b9da6-150">Segunda solicitud de ejemplo</span><span class="sxs-lookup"><span data-stu-id="b9da6-150">Sample second request</span></span>

<span data-ttu-id="b9da6-p112">La segunda solicitud especifica la dirección URL `nextLink` devuelta de la respuesta anterior. Observe que ya no tiene que especificar el mismo parámetro `$select` como en la solicitud inicial, dado que el `skipToken` en la dirección URL `nextLink` lo codifica y lo incluye.</span><span class="sxs-lookup"><span data-stu-id="b9da6-p112">The second request specifies the `nextLink` URL returned from the previous response. Notice that it no longer has to specify the same `$select` parameter as in the initial request, as the `skipToken` in the `nextLink` URL encodes and includes it.</span></span>

<!-- {
  "blockType": "ignored",
  "sampleKeys": ["AQMkADNkNAAAgEMAAAA"],
  "name": "get_messages_delta_2"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/mailfolders/AQMkADNkNAAAgEMAAAA/messages/delta?$skiptoken=GwcBoTmPuoTQWfcsAbkYM HTTP/1.1
Prefer: odata.maxpagesize=2
```

### <a name="sample-second-response"></a><span data-ttu-id="b9da6-153">Segunda respuesta de ejemplo</span><span class="sxs-lookup"><span data-stu-id="b9da6-153">Sample second response</span></span>

<span data-ttu-id="b9da6-154">La segunda respuesta devuelve los dos siguientes mensajes próximos en la carpeta y otro `nextLink`, para indicar que hay más mensajes para obtener desde la carpeta.</span><span class="sxs-lookup"><span data-stu-id="b9da6-154">The second response returns the next 2 messages in the folder and another `nextLink`, indicating there are more messages to get from the folder.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message",
  "isCollection": true
} -->

```json
{
  "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Collection(message)",
  "@odata.nextLink": "https://graph.microsoft.com/v1.0/me/mailfolders('AQMkADNkNAAAgEMAAAA')/messages/delta?$skiptoken=GwcBoTmPKILK4jLH7mAd1lLU",
  "value": [
    {
      "@odata.type": "#microsoft.graph.message",
      "@odata.etag": "W/\"CQAAABYAAAARn2vdzPFjSbaPPxzjlqfdAAAEfYB+\"",
      "subject": "Microsoft Virtual Academy at Contoso",
      "isRead": true,
      "sender": {
        "emailAddress": {
          "name": "Elliot Hyde",
          "address": "elliot-hyde@tailspintoys.com"
        }
      },
      "id": "AQMkADNkNAAAgWkAAAA"
    },
    {
      "@odata.type": "#microsoft.graph.message",
      "@odata.etag": "W/\"CQAAABYAAAARn2vdzPFjSbaPPxzjlzOTAAAEfYB+\"",
      "subject": "New or modified user account information",
      "isRead": true,
      "sender": {
        "emailAddress": {
          "name": "Randi Welch",
          "address": "randiw@contoso.onmicrosoft.com"
        }
      },
      "id": "AQMkADNkNAAAgWJAAAA"
    }
  ]
}
```

### <a name="sample-third-request"></a><span data-ttu-id="b9da6-155">Tercera solicitud de ejemplo</span><span class="sxs-lookup"><span data-stu-id="b9da6-155">Sample third request</span></span>

<span data-ttu-id="b9da6-156">La tercera solicitud continúa usando la última dirección URL `nextLink` devuelta desde la última solicitud de sincronización.</span><span class="sxs-lookup"><span data-stu-id="b9da6-156">The third request continues to use the latest `nextLink` URL returned from the last sync request.</span></span>

<!-- {
  "blockType": "ignored",
  "sampleKeys": ["AQMkADNkNAAAgEMAAAA"],
  "name": "get_messages_delta_3"
}-->
```
GET https://graph.microsoft.com/v1.0/me/mailFolders/AQMkADNkNAAAgEMAAAA/messages/delta?$skiptoken=GwcBoTmPKILK4jLH7mAd1lLU HTTP/1.1
Prefer: odata.maxpagesize=2
```

### <a name="sample-third-and-final-response"></a><span data-ttu-id="b9da6-157">Tercera y última respuesta de ejemplo</span><span class="sxs-lookup"><span data-stu-id="b9da6-157">Sample third and final response</span></span>

<span data-ttu-id="b9da6-p113">La tercera respuesta devuelve el único mensajes restante en la carpeta y una dirección URL `deltaLink` que indica que la sincronización se completó de momento para esta carpeta. Guarde y use la dirección URL `deltaLink` para [sincronizar la misma carpeta en la siguiente ronda](#synchronize-messages-in-the-same-folder-in-the-next-round).</span><span class="sxs-lookup"><span data-stu-id="b9da6-p113">The third response returns the only remaining message in the folder, and a `deltaLink` URL which indicates synchronization is complete for the time being for this folder. Save and use the `deltaLink` URL to [synchronize the same folder in the next round](#synchronize-messages-in-the-same-folder-in-the-next-round).</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message",
  "isCollection": true
} -->

```json
{
  "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Collection(message)",
  "@odata.deltaLink": "https://graph.microsoft.com/v1.0/me/mailfolders('AQMkADNkNAAAgEMAAAA')/messages/delta?$deltatoken=GwcBoTmPuoGNlgXgF1nyUNMXY",
  "value": [
    {
      "@odata.type": "#microsoft.graph.message",
      "@odata.etag": "W/\"CQAAABYAAAARn2vdzFPjSbaPPxzjlzOTAAAEfYB+\"",
      "subject": "Fabric CDN now available",
      "isRead": true,
      "sender": {
        "emailAddress": {
          "name": "Jodie Sharp",
          "address": "Jodie.Sharp@contoso.com"
        }
      },
      "id": "AAMkADk0MGFkODE3LWEAAA="
    }
  ]
}
```

### <a name="synchronize-messages-in-the-same-folder-in-the-next-round"></a><span data-ttu-id="b9da6-160">Sincronizar los mensajes de la misma carpeta en la siguiente ronda</span><span class="sxs-lookup"><span data-stu-id="b9da6-160">Synchronize messages in the same folder in the next round</span></span>

<span data-ttu-id="b9da6-p114">Con el `deltaLink` de la [última solicitud](#sample-third-request) de la última ronda, solo se podrán obtener aquellos mensajes que cambiaron (que se agregaron, eliminaron o actualizaron) en esa carpeta desde entonces. La primera solicitud de la ronda siguiente será similar a la mostrada a continuación, suponiendo que prefiere mantener el mismo tamaño de página máximo en la respuesta:</span><span class="sxs-lookup"><span data-stu-id="b9da6-p114">Using the `deltaLink` from the [last request](#sample-third-request) in the last round, you will be able to get only those messages that have changed (by being added, deleted, or updated) in that folder since then. Your first request in the next round will look like the following, assuming you prefer to keep the same maximum page size in the response:</span></span>

<!-- {
  "blockType": "ignored",
  "sampleKeys": ["AQMkADNkNAAAgEMAAAA"],
  "name": "get_messages_delta_next"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/mailfolders/AQMkADNkNAAAgEMAAAA/messages/delta?$deltatoken=GwcBoTmPuoGNlgXgF1nyUNMXY HTTP/1.1
Prefer: odata.maxpagesize=2
```

<span data-ttu-id="b9da6-163">La respuesta contiene un `deltaLink`.</span><span class="sxs-lookup"><span data-stu-id="b9da6-163">The response contains a `deltaLink`.</span></span> <span data-ttu-id="b9da6-164">Esto indica que todos los cambios de la carpeta de correo remota están ahora sincronizados.</span><span class="sxs-lookup"><span data-stu-id="b9da6-164">This indicates that all changes in the remote mail folder are now synchronized.</span></span> <span data-ttu-id="b9da6-165">Un mensaje se ha eliminado y el otro se ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="b9da6-165">One message was deleted and the other message was changed.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message",
  "isCollection": true
} -->

```json
{
  "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Collection(message)",
  "@odata.deltaLink": "https://graph.microsoft.com/v1.0/me/mailfolders('AQMkADNkNAAAgEMAAAA')/messages/delta?$deltatoken=GwcBoTmPuoGNlgXgF1nyUNMXY",
  "value": [
    {
      "@odata.type": "#microsoft.graph.message",
      "id": "AAMkADk0MGFkODE3LWE4MmYtNDRhOS0Dh_6qB-pB2Sa2pUum19a6YAAKnLuxoAAA=",
      "@removed": {
        "reason": "deleted"
      }
    },
    {
      "@odata.type": "#microsoft.graph.message",
      "@odata.etag": "W/\"CQAAABYAAAARn2vdzPFjSbaPPxzjlzOTAAASsKZz\"",
      "subject": "Holiday hours update",
      "isRead": "true",
      "sender": {
        "emailAddress": {
          "name": "Dana Swope",
          "address": "danas@contoso.onmicrosoft.com"
        }
      },
      "id": "AAMkADNkNAAASq35xAAA="
    }
  ]
}
```

## <a name="see-also"></a><span data-ttu-id="b9da6-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9da6-166">See also</span></span>

- [<span data-ttu-id="b9da6-167">Consulta delta de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="b9da6-167">Microsoft Graph delta query</span></span>](delta-query-overview.md)
- [<span data-ttu-id="b9da6-168">Obtener los cambios incrementales de los eventos en una vista de calendario</span><span class="sxs-lookup"><span data-stu-id="b9da6-168">Get incremental changes to events in a calendar view</span></span>](delta-query-events.md)
- [<span data-ttu-id="b9da6-169">Obtener los cambios incrementales en los grupos</span><span class="sxs-lookup"><span data-stu-id="b9da6-169">Get incremental changes to groups</span></span>](delta-query-groups.md)
- [<span data-ttu-id="b9da6-170">Obtener los cambios incrementales en los usuarios</span><span class="sxs-lookup"><span data-stu-id="b9da6-170">Get incremental changes to users</span></span>](delta-query-users.md)
