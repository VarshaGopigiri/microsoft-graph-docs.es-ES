# <a name="message-delta"></a><span data-ttu-id="e4384-101">mensaje: delta</span><span class="sxs-lookup"><span data-stu-id="e4384-101">message: delta</span></span>

<span data-ttu-id="e4384-102">Obtenga un conjunto de mensajes que se hayan agregado, eliminado o actualizado en una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="e4384-102">Get a set of messages that have been added, deleted, or updated in a specified folder.</span></span>

<span data-ttu-id="e4384-p101">La llamada de una función **delta** para los mensajes de una carteta funciona de forma similar a una solicitud GET, salvo que, al aplicar correctamente [tokens de estado](../../../concepts/delta_query_overview.md) en al menos una de estas llamadas, puede [realizar una consulta para obtener los cambios incrementales en los mensajes de la carpeta](../../../concepts/delta_query_messages.md). Esto permite mantener y sincronizar un almacén local de mensajes de un usuario, sin tener que capturar cada vez todo el conjunto de mensajes desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="e4384-p101">A **delta** function call for messages in a folder is similar to a GET request, except that by appropriately applying [state tokens](../../../concepts/delta_query_overview.md) in one or more of these calls, you can [query for incremental changes in the messages in that folder](../../../concepts/delta_query_messages.md). This allows you to maintain and synchronize a local store of a user's messages without having to fetch the entire set of messages from the server every time.</span></span>  

## <a name="permissions"></a><span data-ttu-id="e4384-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="e4384-105">Permissions</span></span>
<span data-ttu-id="e4384-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e4384-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e4384-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e4384-108">Permission type</span></span>      | <span data-ttu-id="e4384-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e4384-109">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="e4384-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e4384-110">Delegated (work or school account)</span></span> | <span data-ttu-id="e4384-111">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e4384-111">Mail.Read, Mail.ReadWrite</span></span>    | 
|<span data-ttu-id="e4384-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e4384-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e4384-113">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e4384-113">Mail.Read, Mail.ReadWrite</span></span>    | 
|<span data-ttu-id="e4384-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e4384-114">Application</span></span> | <span data-ttu-id="e4384-115">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e4384-115">Mail.Read, Mail.ReadWrite</span></span> | 

## <a name="http-request"></a><span data-ttu-id="e4384-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e4384-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/{id}/messages/delta
GET /users/<id>/mailFolders/{id}/messages/delta
```

### <a name="query-parameters"></a><span data-ttu-id="e4384-117">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="e4384-117">Query parameters</span></span>

<span data-ttu-id="e4384-p103">El seguimiento de cambios en los mensajes conlleva al menos una llamada de una función **delta**. Si usa cualquier parámetro de consulta (distinto de `$deltatoken` y `$skiptoken`), debe especificarlo en la solicitud **delta** inicial. Microsoft Graph codifica automáticamente cualquier parámetro especificado en la parte del token de la URL `nextLink` o `deltaLink` proporcionada en la respuesta. Solo debe especificar los parámetros de consulta deseados una vez por adelantado. En solicitudes posteriores, basta con copiar y aplicar la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.</span><span class="sxs-lookup"><span data-stu-id="e4384-p103">Tracking changes in messages incurs a round of one or more **delta** function calls. If you use any query parameter (other than `$deltatoken` and `$skiptoken`), you must specify it in the initial **delta** request. Microsoft Graph automatically encodes any specified parameters into the token portion of the `nextLink` or `deltaLink` URL provided in the response. You only need to specify any desired query parameters once upfront. In subsequent requests, simply copy and apply the `nextLink` or `deltaLink` URL from the previous response, as that URL already includes the encoded, desired parameters.</span></span>

| <span data-ttu-id="e4384-123">Parámetro de consulta</span><span class="sxs-lookup"><span data-stu-id="e4384-123">Query parameter</span></span>      | <span data-ttu-id="e4384-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4384-124">Type</span></span>   |<span data-ttu-id="e4384-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4384-125">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="e4384-126">$deltatoken</span><span class="sxs-lookup"><span data-stu-id="e4384-126">$deltatoken</span></span> | <span data-ttu-id="e4384-127">string</span><span class="sxs-lookup"><span data-stu-id="e4384-127">string</span></span> | <span data-ttu-id="e4384-p104">Un [token de estado](../../../concepts/delta_query_overview.md) que se devuelve en la URL de `deltaLink` de la llamada de función **delta** anterior para la misma colección de mensajes. Indica el progreso de la ronda de seguimiento de cambios. Guarde y aplique toda la dirección URL `deltaLink`, incluido este token, en la primera solicitud de la siguiente ronda de seguimiento de cambios de la colección.</span><span class="sxs-lookup"><span data-stu-id="e4384-p104">A [state token](../../../concepts/delta_query_overview.md) returned in the `deltaLink` URL of the previous **delta** function call for the same message collection, indicating the completion of that round of change tracking. Save and apply the entire `deltaLink` URL including this token in the first request of the next round of change tracking for that collection.</span></span>|
| <span data-ttu-id="e4384-130">$skiptoken</span><span class="sxs-lookup"><span data-stu-id="e4384-130">$skiptoken</span></span> | <span data-ttu-id="e4384-131">string</span><span class="sxs-lookup"><span data-stu-id="e4384-131">string</span></span> | <span data-ttu-id="e4384-132">Un [token de estado](../../../concepts/delta_query_overview.md) que se devuelve en la URL de `nextLink` de la llamada de función **delta**. Indica que debe realizarse el seguimiento de más cambios en la misma colección de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e4384-132">A [state token](../../../concepts/delta_query_overview.md) returned in the `nextLink` URL of the previous **delta** function call, indicating there are further changes to be tracked in the same message collection.</span></span> |


#### <a name="odata-query-parameters"></a><span data-ttu-id="e4384-133">Parámetros de consulta de OData</span><span class="sxs-lookup"><span data-stu-id="e4384-133">OData query parameters</span></span>

- <span data-ttu-id="e4384-p105">Puede utilizar un parámetro de consulta `$select` como en cualquier solicitud GET para especificar solo las propiedades que necesita para un mejor rendimiento. Siempre se devuelve la propiedad _id_.</span><span class="sxs-lookup"><span data-stu-id="e4384-p105">You can use a `$select` query parameter as in any GET request to specify only the properties your need for best performance. The _id_ property is always returned.</span></span> 
- <span data-ttu-id="e4384-136">Compatibilidad con consultas de delta `$select`, `$top`, y `$expand` para los mensajes.</span><span class="sxs-lookup"><span data-stu-id="e4384-136">Delta query support `$select`, `$top`, and `$expand` for messages.</span></span> 
- <span data-ttu-id="e4384-137">Hay compatibilidad limitada para `$filter` y `$orderby`:</span><span class="sxs-lookup"><span data-stu-id="e4384-137">There is limited support for `$filter` and `$orderby`:</span></span>
  * <span data-ttu-id="e4384-138">Las únicas expresiones `$filter` admitidas son `$filter=receivedDateTime+ge+{value}` y `$filter=receivedDateTime+gt+{value}`.</span><span class="sxs-lookup"><span data-stu-id="e4384-138">The only supported `$filter` expresssions are `$filter=receivedDateTime+ge+{value}` or `$filter=receivedDateTime+gt+{value}`.</span></span>
  * <span data-ttu-id="e4384-p106">La única expresión `$orderby` admitida es `$orderby=receivedDateTime+desc`. Si no incluye una expresión `$orderby`, no se garantiza el orden de devolución.</span><span class="sxs-lookup"><span data-stu-id="e4384-p106">The only supported `$orderby` expression is `$orderby=receivedDateTime+desc`. If you do not include an `$orderby` expression, the return order is not guaranteed.</span></span> 
- <span data-ttu-id="e4384-141">No hay compatibilidad con `$search`.</span><span class="sxs-lookup"><span data-stu-id="e4384-141">There is no support for `$search`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="e4384-142">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e4384-142">Request headers</span></span>
| <span data-ttu-id="e4384-143">Nombre</span><span class="sxs-lookup"><span data-stu-id="e4384-143">Name</span></span>       | <span data-ttu-id="e4384-144">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4384-144">Type</span></span> | <span data-ttu-id="e4384-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4384-145">Description</span></span> |
|:---------------|:----------|:----------|
| <span data-ttu-id="e4384-146">Authorization</span><span class="sxs-lookup"><span data-stu-id="e4384-146">Authorization</span></span>  | <span data-ttu-id="e4384-147">string</span><span class="sxs-lookup"><span data-stu-id="e4384-147">string</span></span>  | <span data-ttu-id="e4384-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e4384-p107">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="e4384-150">Content-Type</span><span class="sxs-lookup"><span data-stu-id="e4384-150">Content-Type</span></span>  | <span data-ttu-id="e4384-151">string</span><span class="sxs-lookup"><span data-stu-id="e4384-151">string</span></span>  | <span data-ttu-id="e4384-p108">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e4384-p108">application/json. Required.</span></span> |
| <span data-ttu-id="e4384-154">Prefer</span><span class="sxs-lookup"><span data-stu-id="e4384-154">Prefer</span></span> | <span data-ttu-id="e4384-155">string</span><span class="sxs-lookup"><span data-stu-id="e4384-155">string</span></span>  | <span data-ttu-id="e4384-p109">odata.maxpagesize={x}. Opcional.</span><span class="sxs-lookup"><span data-stu-id="e4384-p109">odata.maxpagesize={x}. Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="e4384-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e4384-158">Response</span></span>

<span data-ttu-id="e4384-159">Si se ejecuta correctamente, este método devuelve un código de respuesta `200, OK` y el objeto de colección [message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e4384-159">If successful, this method returns a `200, OK` response code and [message](../resources/message.md) collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e4384-160">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e4384-160">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e4384-161">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e4384-161">Request</span></span>
<span data-ttu-id="e4384-162">En el ejemplo siguiente se muestra cómo realizar una llamada de función **delta** única y limitar el número máximo de mensajes en el cuerpo de la respuesta a 2.</span><span class="sxs-lookup"><span data-stu-id="e4384-162">The following example shows how to make a single **delta** function call, and limit the maximum number of messages in the response body to 2.</span></span>

<span data-ttu-id="e4384-p110">Para realizar un seguimiento de los cambios de los mensajes de una carpeta, debería realizar al menos una llamada de función **delta** para obtener el conjunto de cambios incrementales desde la última consulta delta. Para obtener un ejemplo que muestre una ronda de llamadas de consulta delta, vea [Obtener los cambios incrementales en los mensajes de una carpeta](../../../concepts/delta_query_messages.md).</span><span class="sxs-lookup"><span data-stu-id="e4384-p110">To track changes in the messages in a folder, you would make one or more **delta** function calls to get the set of incremental changes since the last delta query. For an example that shows a round of delta query calls, see [Get incremental changes to messages in a folder](../../../concepts/delta_query_messages.md).</span></span>
 
<!-- {
  "blockType": "request",
  "name": "message_delta"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/mailFolders/{id}/messages/delta

Prefer: odata.maxpagesize=2
```

##### <a name="response"></a><span data-ttu-id="e4384-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e4384-165">Response</span></span>
<span data-ttu-id="e4384-166">Si la solicitud es correcta, la respuesta debería incluir un símbolo de estado, que puede ser un _skipToken_</span><span class="sxs-lookup"><span data-stu-id="e4384-166">If the request is successful, the response would include a state token, which is either a _skipToken_</span></span>  
<span data-ttu-id="e4384-p111">(en un encabezado de respuesta de _@odata.nextLink_) o un _deltaToken_ (en un encabezado de respuesta de _@odata.deltaLink_). Respectivamente, indican si debe continuar con la ronda, o bien si ha terminado de obtener todos los cambios de la ronda.</span><span class="sxs-lookup"><span data-stu-id="e4384-p111">(in an _@odata.nextLink_ response header) or a _deltaToken_ (in an _@odata.deltaLink_ response header). Respectively, they indicate whether you should continue with the round or you have completed getting all the changes for that round.</span></span>

<span data-ttu-id="e4384-169">La respuesta siguiente muestra un _skipToken_ en un encabezado de respuesta de _@odata.nextLink_.</span><span class="sxs-lookup"><span data-stu-id="e4384-169">The response below shows a _skipToken_ in an _@odata.nextLink_ response header.</span></span>

<span data-ttu-id="e4384-p112">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e4384-p112">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 337

{
  "@odata.nextLink":"https://graph.microsoft.com/v1.0/me/mailfolders('{id}')/messages/delta?$skiptoken={_skipToken_}",
  "value": [
    {
      "receivedDateTime": "datetime-value",
      "sentDateTime": "datetime-value",
      "hasAttachments": true,
      "internetMessageId": "internetMessageId-value",
      "subject": "subject-value",
      "body": {
        "contentType": "contentType-value",
        "content": "content-value"
      }
    }
  ]
}
```

### <a name="see-also"></a><span data-ttu-id="e4384-172">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="e4384-172">See also</span></span>

- [<span data-ttu-id="e4384-173">Usar la consulta delta para realizar el seguimiento de los cambios en datos de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="e4384-173">Use delta query to track changes in Microsoft Graph data</span></span>](../../../concepts/delta_query_overview.md)
- [<span data-ttu-id="e4384-174">Obtener los cambios incrementales en los mensajes de una carpeta</span><span class="sxs-lookup"><span data-stu-id="e4384-174">Get incremental changes to messages in a folder</span></span>](../../../concepts/delta_query_messages.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->