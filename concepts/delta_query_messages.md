# <a name="get-incremental-changes-to-messages-in-a-folder"></a><span data-ttu-id="6f591-101">Obtener los cambios incrementales en los mensajes de una carpeta</span><span class="sxs-lookup"><span data-stu-id="6f591-101">Get incremental changes to messages in a folder</span></span> 

<span data-ttu-id="6f591-p101">Consulta de delta permite consultar las adiciones, eliminaciones o actualizaciones a los mensajes de una carpeta, por medio de una serie de llamadas a función [delta](../api-reference/v1.0/api/message_delta.md). Los datos de delta permiten mantener y sincronizar un almacén local de mensajes de un usuario, sin tener que capturar cada vez todo el conjunto de mensajes del usuario desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="6f591-p101">Delta query lets you query for additions, deletions, or updates to messages in a folder, by way of a series of [delta](../api-reference/v1.0/api/message_delta.md) function calls. Delta data enables you to maintain and synchronize a local store of a user's messages, without having to fetch the entire set of the user's messages from the server every time.</span></span>

<span data-ttu-id="6f591-p102">La consulta de delta admite la sincronización completa que recupera todos los mensajes de una carpeta (por ejemplo, la bandeja de entrada del usuario) y la sincronización incremental que recupera todos los mensajes que cambiaron en la carpeta desde la última sincronización. Normalmente, se debería realizar una sincronización completa inicial de todos los mensajes de una carpeta y, después, obtener los cambios incrementales en la carpeta de forma periódica.</span><span class="sxs-lookup"><span data-stu-id="6f591-p102">Delta query supports both full synchronization that retrieves all of the messages in a folder (for example, the user's Inbox), and incremental synchronization that retrieves all of the messages that have changed in that folder since the last synchronization. Typically, you would do an initial full synchronization of all the messages in a folder, and subsequently, get incremental changes to that folder periodically.</span></span> 

## <a name="track-message-changes-in-a-folder"></a><span data-ttu-id="6f591-106">Seguimiento de cambios de mensajes en una carpeta</span><span class="sxs-lookup"><span data-stu-id="6f591-106">Track message changes in a folder</span></span>

<span data-ttu-id="6f591-p103">La consulta de delta es una operación por carpeta. Para realizar el seguimiento de los cambios de los mensajes en una jerarquía de carpetas, debe realizar un seguimiento de cada carpeta de forma individual.</span><span class="sxs-lookup"><span data-stu-id="6f591-p103">Delta query is a per-folder operation. To track the changes of the messages in a folder hierarchy, you need to track each folder individually.</span></span> 

<span data-ttu-id="6f591-p104">El seguimiento de los cambios de mensajes en una carpeta de correo normalmente es una ronda de una o varias solicitudes GET con la función **delta**. La solicitud GET inicial es muy similar a la forma de [obtener mensajes](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/user_list_messages), salvo que se incluye la función **delta**:</span><span class="sxs-lookup"><span data-stu-id="6f591-p104">Tracking message changes in a mail folder typically is a round of one or more GET requests with the **delta** function. The initial GET request is very much like the way you [get messages](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/api/user_list_messages), except that you include the **delta** function:</span></span>

```
GET https://graph.microsoft.com/v1.0/me/mailFolders/{id}/messages/delta
```

<span data-ttu-id="6f591-111">Una solicitud GET con la función **delta** función devuelve:</span><span class="sxs-lookup"><span data-stu-id="6f591-111">A GET request with the **delta** function returns either:</span></span>

- <span data-ttu-id="6f591-112">Un `nextLink` (que contiene una dirección URL con una llamada de función **delta** y un _skipToken_), o</span><span class="sxs-lookup"><span data-stu-id="6f591-112">A `nextLink` (that contains a URL with a **delta** function call and a _skipToken_), or</span></span> 
- <span data-ttu-id="6f591-113">Un `deltaLink` (que contiene una dirección URL con una llamada de función **delta** y un _deltaToken_).</span><span class="sxs-lookup"><span data-stu-id="6f591-113">A `deltaLink` (that contains a URL with a **delta** function call and _deltaToken_).</span></span>

<span data-ttu-id="6f591-p105">Estos tokens son [tokens de estado](delta_query_overview.md#state-tokens) totalmente opacos para el cliente. Para continuar con una ronda de seguimiento de cambios, basta con copiar y aplicar la dirección URL devuelta desde la última solicitud GET a la siguiente llamada de función**delta** para la misma carpeta. Un `deltaLink` devuelto en una respuesta significa que la ronda actual de seguimiento de cambios está completa. Se puede guardar y usar la dirección URL `deltaLink` cuando se inicia la siguiente ronda.</span><span class="sxs-lookup"><span data-stu-id="6f591-p105">These tokens are [state tokens](delta_query_overview.md#state-tokens) that are completely opaque to the client. To proceed with a round of change tracking, simply copy and apply the URL returned from the last GET request to the next **delta** function call for the same folder. A `deltaLink` returned in a response signifies that the current round of change tracking is complete. You can save and use the `deltaLink` URL when you begin the next round.</span></span>

<span data-ttu-id="6f591-118">Vea el [ejemplo](#example-to-synchronize-messages-in-a-folder) siguiente para obtener información sobre cómo usar las direcciones URL `nextLink` y `deltaLink`.</span><span class="sxs-lookup"><span data-stu-id="6f591-118">See the [example](#example-to-synchronize-messages-in-a-folder) below to learn how to use the `nextLink` and `deltaLink` URLs.</span></span>

### <a name="use-query-parameters-in-a-delta-query-for-messages"></a><span data-ttu-id="6f591-119">Usar parámetros de consulta en una consulta de delta para los mensajes</span><span class="sxs-lookup"><span data-stu-id="6f591-119">Use query parameters in a delta query for messages</span></span>

- <span data-ttu-id="6f591-p106">Puede utilizar un parámetro de consulta `$select` como en cualquier solicitud GET para especificar solo las propiedades que necesita para un mejor rendimiento. Siempre se devuelve la propiedad _id_.</span><span class="sxs-lookup"><span data-stu-id="6f591-p106">You can use a `$select` query parameter as in any GET request to specify only the properties your need for best performance. The _id_ property is always returned.</span></span> 
- <span data-ttu-id="6f591-122">Compatibilidad con consultas de delta `$select`, `$top`, y `$expand` para los mensajes.</span><span class="sxs-lookup"><span data-stu-id="6f591-122">Delta query support `$select`, `$top`, and `$expand` for messages.</span></span> 
- <span data-ttu-id="6f591-123">Hay compatibilidad limitada para `$filter` y `$orderby`:</span><span class="sxs-lookup"><span data-stu-id="6f591-123">There is limited support for `$filter` and `$orderby`:</span></span>
  * <span data-ttu-id="6f591-124">Las únicas expresiones `$filter` admitidas son `$filter=receivedDateTime+ge+{value}` y `$filter=receivedDateTime+gt+{value}`.</span><span class="sxs-lookup"><span data-stu-id="6f591-124">The only supported `$filter` expresssions are `$filter=receivedDateTime+ge+{value}` or `$filter=receivedDateTime+gt+{value}`.</span></span>
  * <span data-ttu-id="6f591-p107">La única expresión `$orderby` admitida es `$orderby=receivedDateTime+desc`. Si no incluye una expresión `$orderby`, no se garantiza el orden de devolución.</span><span class="sxs-lookup"><span data-stu-id="6f591-p107">The only supported `$orderby` expression is `$orderby=receivedDateTime+desc`. If you do not include an `$orderby` expression, the return order is not guaranteed.</span></span> 
- <span data-ttu-id="6f591-127">No hay compatibilidad con `$search`.</span><span class="sxs-lookup"><span data-stu-id="6f591-127">There is no support for `$search`.</span></span>


### <a name="optional-request-header"></a><span data-ttu-id="6f591-128">Encabezado de solicitud opcional</span><span class="sxs-lookup"><span data-stu-id="6f591-128">Optional request header</span></span>

<span data-ttu-id="6f591-129">Cada solicitud GET de la consulta delta devuelve una colección de uno o más mensajes en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6f591-129">Each delta query GET request returns a collection of one or more messages in the response. You can optionally specify the request header, Prefer: odata.maxpagesize={x}, to set the maximum number of messages in a response.</span></span> <span data-ttu-id="6f591-130">Opcionalmente se puede especificar el encabezado de solicitud, `Prefer: odata.maxpagesize={x}`, para establecer el número máximo de mensajes en una respuesta.</span><span class="sxs-lookup"><span data-stu-id="6f591-130">Each delta query GET request returns a collection of one or more messages in the response. You can optionally specify the request header, `Prefer: odata.maxpagesize={x}`, to set the maximum number of messages in a response.</span></span>

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

6. When you eventually receive a _detlaToken (in an _@odata.deltaLink_ response header) in the response from a GET, stop. This 
round of change tracking is complete. 

7. Save the _deltaToken_. The next time you track changes for the same folder, make a GET request 
similar to step 1, except that now you can use this _deltaToken_ to get just the delta data (messages that have been added, deleted or updated) 
since the completion of the very first round.

-->

## <a name="example-to-synchronize-messages-in-a-folder"></a><span data-ttu-id="6f591-131">Ejemplo para sincronizar los mensajes de una carpeta</span><span class="sxs-lookup"><span data-stu-id="6f591-131">Example to synchronize messages in a folder</span></span>

<span data-ttu-id="6f591-132">En el ejemplo siguiente se muestra una serie de tres solicitudes para sincronizar una carpeta específica que contiene cinco mensajes:</span><span class="sxs-lookup"><span data-stu-id="6f591-132">The following example shows a series of 3 requests to synchronize a specific folder which contains 5 messages:</span></span>

- <span data-ttu-id="6f591-133">[Solicitud inicial de ejemplo](#sample-initial-request) y [respuesta](#sample-initial-response)</span><span class="sxs-lookup"><span data-stu-id="6f591-133">[Sample initial request](#sample-initial-request) and [response](#sample-initial-response)</span></span>
- <span data-ttu-id="6f591-134">[Segunda solicitud de ejemplo](#sample-second-request) y [respuesta](#sample-second-response)</span><span class="sxs-lookup"><span data-stu-id="6f591-134">[Sample second request](#sample-second-request) and [response](#sample-second-response)</span></span>
- <span data-ttu-id="6f591-135">[Tercera solicitud de ejemplo](#sample-third-request) y [respuesta final](#sample-third-and-final-response)</span><span class="sxs-lookup"><span data-stu-id="6f591-135">[Sample third request](#sample-third-request) and [final response](#sample-third-and-final-response)</span></span>

<span data-ttu-id="6f591-136">Vea también lo que hará la [siguiente ronda](#the-next-round).</span><span class="sxs-lookup"><span data-stu-id="6f591-136">See also what you'll do in the [next round](#the-next-round).</span></span>


### <a name="sample-initial-request"></a><span data-ttu-id="6f591-137">Solicitud inicial de ejemplo</span><span class="sxs-lookup"><span data-stu-id="6f591-137">Sample initial request</span></span>

<span data-ttu-id="6f591-p109">En este ejemplo, se sincroniza por primera vez la carpeta especificada, por lo que la solicitud de sincronización inicial no incluye ningún token de estado. Esa ronda devolverá todos los mensajes de esa carpeta.</span><span class="sxs-lookup"><span data-stu-id="6f591-p109">In this example, the specified folder is being synchronized for the first time, so the initial sync request does not include any state token. This round will return all the messages in that folder.</span></span>

<span data-ttu-id="6f591-140">La primera solicitud especifica lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6f591-140">The first request specifies the following:</span></span>

- <span data-ttu-id="6f591-141">Un parámetro `$select` que devuelva las propiedades **asunto** y **remitente** para cada mensaje en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6f591-141">A `$select` parameter to return the **Subject** and **Sender** properties for each message in the response.</span></span>
- <span data-ttu-id="6f591-142">El [encabezado de solicitud opcional](#optional-request-header), _odata.maxpagesize_, que devuelve dos mensajes a la vez.</span><span class="sxs-lookup"><span data-stu-id="6f591-142">The [optional request header](#optional-request-header), _odata.maxpagesize_, returning 2 messages at a time.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_messages_delta_1"
}-->
```
GET https://graph.microsoft.com/v1.0/me/mailfolders('AQMkADNkNAAAgEMAAAA')/messages/delta?$select=Subject,Sender HTTP/1.1
Prefer: odata.maxpagesize=2
```


### <a name="sample-initial-response"></a><span data-ttu-id="6f591-143">Respuesta inicial de ejemplo</span><span class="sxs-lookup"><span data-stu-id="6f591-143">Sample initial response</span></span>

<span data-ttu-id="6f591-p110">La respuesta incluye dos mensajes y un encabezado de respuesta `@odata.nextLink`. La dirección URL `nextLink` indica que la carpeta contiene más mensajes que recuperar.</span><span class="sxs-lookup"><span data-stu-id="6f591-p110">The response includes two messages and an `@odata.nextLink` response header. The `nextLink` URL indicates there are more messages in the folder to get.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message",
  "isCollection": true
} -->
```
{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#Collection(message)",
    "@odata.nextLink":"https://graph.microsoft.com/v1.0/me/mailfolders('AQMkADNkNAAAgEMAAAA')/messages/delta?$skiptoken=GwcBoTmPuoTQWfcsAbkYM",
    "value":[
        {
            "@odata.type":"#microsoft.graph.message",
            "@odata.etag":"W/\"CQAAABYAAAARn2vdzPFjSbaPPxzjlzOTAAASsKZz\"",
            "subject":"Holiday hours update",
            "sender":{
                "emailAddress":{
                    "name":"Dana Swope",
                    "address":"danas@contoso.onmicrosoft.com"
                }
            },
            "id":"AAMkADNkNAAASq35xAAA="
        },
        {
            "@odata.type":"#microsoft.graph.message",
            "@odata.etag":"W/\"CQAAABYAAAARn2vdzPFjSbaPPxzjlzOTAAAEfYB/\"",
            "subject":"Holiday promotion sale",
            "sender":{
                "emailAddress":{
                    "name":"Samantha Booth",
                    "address":"samanthab@contoso.onmicrosoft.com"
                }
            },
            "id":"AQMkADNkNAAAVRMKAAAAA=="
        }
    ]
}
```

### <a name="sample-second-request"></a><span data-ttu-id="6f591-146">Segunda solicitud de ejemplo</span><span class="sxs-lookup"><span data-stu-id="6f591-146">Sample second request</span></span>

<span data-ttu-id="6f591-p111">La segunda solicitud especifica la dirección URL `nextLink` devuelta de la respuesta anterior. Observe que ya no tiene que especificar el mismo parámetro `$select` como en la solicitud inicial, dado que el `skipToken` en la dirección URL `nextLink` lo codifica y lo incluye.</span><span class="sxs-lookup"><span data-stu-id="6f591-p111">The second request specifies the `nextLink` URL returned from the previous response. Notice that it no longer has to specify the same `$select` parameter as in the initial request, as the `skipToken` in the `nextLink` URL encodes and includes it.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_messages_delta_2"
}-->
```
GET https://graph.microsoft.com/v1.0/me/mailfolders('AQMkADNkNAAAgEMAAAA')/messages/delta?$skiptoken=GwcBoTmPuoTQWfcsAbkYM HTTP/1.1
Prefer: odata.maxpagesize=2
```

### <a name="sample-second-response"></a><span data-ttu-id="6f591-149">Segunda respuesta de ejemplo</span><span class="sxs-lookup"><span data-stu-id="6f591-149">Sample second response</span></span> 

<span data-ttu-id="6f591-150">La segunda respuesta devuelve los dos siguientes mensajes próximos en la carpeta y otro `nextLink`, para indicar que hay más mensajes para obtener desde la carpeta.</span><span class="sxs-lookup"><span data-stu-id="6f591-150">The second response returns the next 2 messages in the folder and another `nextLink`, indicating there are more messages to get from the folder.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message",
  "isCollection": true
} -->
```
{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#Collection(message)",
    "@odata.nextLink":"https://graph.microsoft.com/v1.0/me/mailfolders('AQMkADNkNAAAgEMAAAA')/messages/delta?$skiptoken=GwcBoTmPKILK4jLH7mAd1lLU",
    "value":[
        {
            "@odata.type":"#microsoft.graph.message",
            "@odata.etag":"W/\"CQAAABYAAAARn2vdzPFjSbaPPxzjlzOTAAAEfYB+\"",
            "subject":"New or modified user account information",
            "sender":{
                "emailAddress":{
                    "name":"Randi Welch",
                    "address":"randiw@contoso.onmicrosoft.com"
                }
            },
            "id":"AQMkADNkNAAAgWJAAAA"
        },
        {
            "@odata.type":"#microsoft.graph.message",
            "@odata.etag":"W/\"CQAAABYAAAARn2vdzPFjSbaPPxzjlzOTAAAEfYB9\"",
            "subject":"New or modified user account information",
            "sender":{
                "emailAddress":{
                    "name":"Randi Welch",
                    "address":"randiw@contoso.onmicrosoft.com"
                }
            },
            "id":"AQMkADNkNAAAgWHAAAA"
        }
    ]
}
```


### <a name="sample-third-request"></a><span data-ttu-id="6f591-151">Tercera solicitud de ejemplo</span><span class="sxs-lookup"><span data-stu-id="6f591-151">Sample third request</span></span>

<span data-ttu-id="6f591-152">La tercera solicitud continúa usando la última dirección URL `nextLink` devuelta desde la última solicitud de sincronización.</span><span class="sxs-lookup"><span data-stu-id="6f591-152">The third request continues to use the latest `nextLink` URL returned from the last sync request.</span></span> 

<!-- {
  "blockType": "request",
  "name": "get_messages_delta_3"
}-->
```
GET https://graph.microsoft.com/v1.0/me/mailfolders('AQMkADNkNAAAgEMAAAA')/messages/delta?$skiptoken=GwcBoTmPKILK4jLH7mAd1lLU HTTP/1.1
Prefer: odata.maxpagesize=2
```

### <a name="sample-third-and-final-response"></a><span data-ttu-id="6f591-153">Tercera y última respuesta de ejemplo</span><span class="sxs-lookup"><span data-stu-id="6f591-153">Sample third and final response</span></span>

<span data-ttu-id="6f591-p112">La tercera respuesta devuelve el único mensajes restante en la carpeta y una dirección URL `deltaLink` que indica que la sincronización se completó de momento para esta carpeta. Guarde y use la dirección URL `deltaLink` para [sincronizar la misma carpeta en la siguiente ronda](#the-next-round).</span><span class="sxs-lookup"><span data-stu-id="6f591-p112">The third response returns the only remaining message in the folder, and a `deltaLink` URL which indicates synchronization is complete for the time being for this folder. Save and use the `deltaLink` URL to [synchronize the same folder in the next round](#the-next-round).</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message",
  "isCollection": true
} -->
```
{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#Collection(message)",
    "@odata.deltaLink":"https://graph.microsoft.com/v1.0/me/mailfolders('AQMkADNkNAAAgEMAAAA')/messages/delta?$deltatoken=GwcBoTmPuoGNlgXgF1nyUNMXY",
    "value":[
        {
            "@odata.type":"#microsoft.graph.message",
            "@odata.etag":"W/\"CQAAABYAAAARn2vdzPFjSbaPPxzjlzOTAAAEfYB8\"",
            "subject":"You've joined the Customer Manager group",
            "sender":{
                "emailAddress":{
                    "name":"Customer Managers team",
                    "address":"customer_managers@contoso.onmicrosoft.com"
                }
            },
            "id":"AQMkADNkNAAAgWFAAAA"
        }
    ]
}
```


### <a name="the-next-round"></a><span data-ttu-id="6f591-156">La siguiente ronda</span><span class="sxs-lookup"><span data-stu-id="6f591-156">The next round</span></span>

<span data-ttu-id="6f591-p113">Con el `deltaLink` de la [última solicitud](#sample-third-request) de la última ronda, solo se podrán obtener aquellos mensajes que cambiaron (que se agregaron, eliminaron o actualizaron) en esa carpeta desde entonces. La primera solicitud de la ronda siguiente será similar a la mostrada a continuación, suponiendo que prefiere mantener el mismo tamaño de página máximo en la respuesta:</span><span class="sxs-lookup"><span data-stu-id="6f591-p113">Using the `deltaLink` from the [last request](#sample-third-request) in the last round, you will be able to get only those messages that have changed (by being added, deleted, or updated) in that folder since then. Your first request in the next round will look like the following, assuming you prefer to keep the same maximum page size in the response:</span></span>

<!-- {
  "blockType": "request",
  "name": "get_messages_delta_next"
}-->
```
GET https://graph.microsoft.com/v1.0/me/mailfolders('AQMkADNkNAAAgEMAAAA')/messages/delta?$deltatoken=GwcBoTmPuoGNlgXgF1nyUNMXY HTTP/1.1
Prefer: odata.maxpagesize=2
```



## <a name="see-also"></a><span data-ttu-id="6f591-159">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="6f591-159">See also</span></span>

- [<span data-ttu-id="6f591-160">Consulta delta de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="6f591-160">Microsoft Graph delta query</span></span>](../Concepts/delta_query_overview.md)
- [<span data-ttu-id="6f591-161">Obtener los cambios incrementales de los eventos en una vista de calendario</span><span class="sxs-lookup"><span data-stu-id="6f591-161">Get incremental changes to events in a calendar view</span></span>](../Concepts/delta_query_events.md)
- [<span data-ttu-id="6f591-162">Obtener los cambios incrementales en los grupos</span><span class="sxs-lookup"><span data-stu-id="6f591-162">Get incremental changes to groups</span></span>](../Concepts/delta_query_groups.md)
- [<span data-ttu-id="6f591-163">Obtener los cambios incrementales en los usuarios</span><span class="sxs-lookup"><span data-stu-id="6f591-163">Get incremental changes to users</span></span>](../Concepts/delta_query_users.md)
