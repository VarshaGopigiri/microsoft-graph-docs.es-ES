---
title: Obtener los cambios incrementales en los mensajes de una carpeta
description: La consulta de delta permite consultar las adiciones, eliminaciones o actualizaciones a los mensajes de una carpeta, por medio de una serie de
author: piotrci
localization_priority: Priority
ms.openlocfilehash: 0200c49c1a673a338af793649bb67f9628c2e8f2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27820912"
---
# <a name="get-incremental-changes-to-messages-in-a-folder"></a>Obtener los cambios incrementales en los mensajes de una carpeta

Consulta de delta permite consultar las adiciones, eliminaciones o actualizaciones a los mensajes de una carpeta, por medio de una serie de llamadas a función [delta](/graph/api/message-delta?view=graph-rest-1.0). Los datos de delta permiten mantener y sincronizar un almacén local de mensajes de un usuario, sin tener que capturar cada vez todo el conjunto de mensajes del usuario desde el servidor.

La consulta de delta admite la sincronización completa que recupera todos los mensajes de una carpeta (por ejemplo, la bandeja de entrada del usuario) y la sincronización incremental que recupera todos los mensajes que cambiaron en la carpeta desde la última sincronización. Normalmente, se debería realizar una sincronización completa inicial de todos los mensajes de una carpeta y, después, obtener los cambios incrementales en la carpeta de forma periódica.

## <a name="track-message-changes-in-a-folder"></a>Seguimiento de cambios de mensajes en una carpeta

La consulta de delta es una operación por carpeta. Para realizar el seguimiento de los cambios de los mensajes en una jerarquía de carpetas, debe realizar un seguimiento de cada carpeta de forma individual.

El seguimiento de los cambios de mensajes en una carpeta de correo normalmente es una ronda de una o varias solicitudes GET con la función **delta**. La solicitud GET inicial es muy similar a la forma de [obtener mensajes](/graph/api/user-list-messages?view=graph-rest-1.0), salvo que se incluye la función **delta**:

```http
GET https://graph.microsoft.com/v1.0/me/mailFolders/{id}/messages/delta
```

Una solicitud GET con la función **delta** función devuelve:

- Un `nextLink` (que contiene una dirección URL con una llamada de función **delta** y un _skipToken_), o
- Un `deltaLink` (que contiene una dirección URL con una llamada de función **delta** y un _deltaToken_).

Estos tokens son [tokens de estado](delta-query-overview.md#state-tokens) totalmente opacos para el cliente. Para continuar con una ronda de seguimiento de cambios, basta con copiar y aplicar la dirección URL devuelta desde la última solicitud GET a la siguiente llamada de función**delta** para la misma carpeta. Un `deltaLink` devuelto en una respuesta significa que la ronda actual de seguimiento de cambios está completa. Se puede guardar y usar la dirección URL `deltaLink` cuando se inicia la siguiente ronda.

Vea el [ejemplo](#example-to-synchronize-messages-in-a-folder) siguiente para obtener información sobre cómo usar las direcciones URL `nextLink` y `deltaLink`.

### <a name="use-query-parameters-in-a-delta-query-for-messages"></a>Usar parámetros de consulta en una consulta de delta para los mensajes

- Puede utilizar un parámetro de consulta `$select` como en cualquier solicitud GET para especificar solo las propiedades que necesita para un mejor rendimiento. Siempre se devuelve la propiedad `id`.
- Compatibilidad con consultas de delta `$select`, `$top`, y `$expand` para los mensajes.
- Hay compatibilidad limitada para `$filter` y `$orderby`:
  - Las únicas expresiones `$filter` admitidas son `$filter=receivedDateTime+ge+{value}` y `$filter=receivedDateTime+gt+{value}`.
  - La única expresión `$orderby` admitida es `$orderby=receivedDateTime+desc`. Si no incluye una expresión `$orderby`, no se garantiza el orden de devolución.
- No hay compatibilidad con `$search`.

### <a name="optional-request-header"></a>Encabezado de solicitud opcional

Cada solicitud GET de la consulta delta devuelve una colección de uno o más mensajes en la respuesta. Opcionalmente se puede especificar el encabezado de solicitud, `Prefer: odata.maxpagesize={x}`, para establecer el número máximo de mensajes en una respuesta.

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

## <a name="example-to-synchronize-messages-in-a-folder"></a>Ejemplo para sincronizar los mensajes de una carpeta

En el siguiente ejemplo se muestran dos rondas de sincronización de una carpeta concreta que inicialmente contiene cinco mensajes.

La primera ronda implica una serie de tres solicitudes para sincronizar los cinco mensajes de la carpeta:

- [Solicitud inicial de ejemplo](#sample-initial-request) y [respuesta](#sample-initial-response)
- [Segunda solicitud de ejemplo](#sample-second-request) y [respuesta](#sample-second-response)
- [Tercera solicitud de ejemplo](#sample-third-request) y [respuesta final](#sample-third-and-final-response)

Después de la primera ronda, uno de los mensajes se elimina y otro se marca como leído. La [segunda ronda](#synchronize-messages-in-the-same-folder-in-the-next-round) de sincronización devuelve solo el delta (la eliminación y actualización) sin devolver los demás mensajes que se han mantenido iguales.

### <a name="sample-initial-request"></a>Solicitud inicial de ejemplo

En este ejemplo, se sincroniza por primera vez la carpeta especificada, por lo que la solicitud de sincronización inicial no incluye ningún token de estado. Esa ronda devolverá todos los mensajes de esa carpeta.

La primera solicitud especifica lo siguiente:

- Un parámetro `$select` que devuelva las propiedades `subject`, `sender` y `isRead` de cada mensaje de la respuesta.
- El [encabezado de solicitud opcional](#optional-request-header), _odata.maxpagesize_, que devuelve dos mensajes a la vez.

<!-- {
  "blockType": "ignored",
  "sampleKeys": ["AQMkADNkNAAAgEMAAAA"],
  "name": "get_messages_delta_1"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/mailfolders/AQMkADNkNAAAgEMAAAA/messages/delta?$select=subject,sender,isRead HTTP/1.1
Prefer: odata.maxpagesize=2
```

### <a name="sample-initial-response"></a>Respuesta inicial de ejemplo

La respuesta incluye dos mensajes y un encabezado de respuesta `@odata.nextLink`. La dirección URL `nextLink` indica que la carpeta contiene más mensajes que recuperar.

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

### <a name="sample-second-request"></a>Segunda solicitud de ejemplo

La segunda solicitud especifica la dirección URL `nextLink` devuelta de la respuesta anterior. Observe que ya no tiene que especificar el mismo parámetro `$select` como en la solicitud inicial, dado que el `skipToken` en la dirección URL `nextLink` lo codifica y lo incluye.

<!-- {
  "blockType": "ignored",
  "sampleKeys": ["AQMkADNkNAAAgEMAAAA"],
  "name": "get_messages_delta_2"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/mailfolders/AQMkADNkNAAAgEMAAAA/messages/delta?$skiptoken=GwcBoTmPuoTQWfcsAbkYM HTTP/1.1
Prefer: odata.maxpagesize=2
```

### <a name="sample-second-response"></a>Segunda respuesta de ejemplo

La segunda respuesta devuelve los dos siguientes mensajes próximos en la carpeta y otro `nextLink`, para indicar que hay más mensajes para obtener desde la carpeta.

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

### <a name="sample-third-request"></a>Tercera solicitud de ejemplo

La tercera solicitud continúa usando la última dirección URL `nextLink` devuelta desde la última solicitud de sincronización.

<!-- {
  "blockType": "ignored",
  "sampleKeys": ["AQMkADNkNAAAgEMAAAA"],
  "name": "get_messages_delta_3"
}-->
```
GET https://graph.microsoft.com/v1.0/me/mailFolders/AQMkADNkNAAAgEMAAAA/messages/delta?$skiptoken=GwcBoTmPKILK4jLH7mAd1lLU HTTP/1.1
Prefer: odata.maxpagesize=2
```

### <a name="sample-third-and-final-response"></a>Tercera y última respuesta de ejemplo

La tercera respuesta devuelve el único mensajes restante en la carpeta y una dirección URL `deltaLink` que indica que la sincronización se completó de momento para esta carpeta. Guarde y use la dirección URL `deltaLink` para [sincronizar la misma carpeta en la siguiente ronda](#synchronize-messages-in-the-same-folder-in-the-next-round).

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

### <a name="synchronize-messages-in-the-same-folder-in-the-next-round"></a>Sincronizar los mensajes de la misma carpeta en la siguiente ronda

Con el `deltaLink` de la [última solicitud](#sample-third-request) de la última ronda, solo se podrán obtener aquellos mensajes que cambiaron (que se agregaron, eliminaron o actualizaron) en esa carpeta desde entonces. La primera solicitud de la ronda siguiente será similar a la mostrada a continuación, suponiendo que prefiere mantener el mismo tamaño de página máximo en la respuesta:

<!-- {
  "blockType": "ignored",
  "sampleKeys": ["AQMkADNkNAAAgEMAAAA"],
  "name": "get_messages_delta_next"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/mailfolders/AQMkADNkNAAAgEMAAAA/messages/delta?$deltatoken=GwcBoTmPuoGNlgXgF1nyUNMXY HTTP/1.1
Prefer: odata.maxpagesize=2
```

La respuesta contiene un `deltaLink`. Esto indica que todos los cambios de la carpeta de correo remota están ahora sincronizados. Un mensaje se ha eliminado y el otro se ha cambiado.

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

## <a name="see-also"></a>Vea también

- [Consulta delta de Microsoft Graph](delta-query-overview.md)
- [Obtener los cambios incrementales de los eventos en una vista de calendario](delta-query-events.md)
- [Obtener los cambios incrementales en los grupos](delta-query-groups.md)
- [Obtener los cambios incrementales en los usuarios](delta-query-users.md)
