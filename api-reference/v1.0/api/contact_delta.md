# <a name="contact-delta"></a><span data-ttu-id="18b47-101">contacto: delta</span><span class="sxs-lookup"><span data-stu-id="18b47-101">contact: delta</span></span>

<span data-ttu-id="18b47-102">Obtiene un conjunto de contactos que se hayan agregado, eliminado o actualizado en una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="18b47-102">Get a set of contacts that have been added, deleted, or updated in a specified folder.</span></span>

<span data-ttu-id="18b47-p101">La llamada de una función **delta** para los contactos de una carpeta funciona de forma similar a una solicitud GET, salvo que, al aplicar correctamente [tokens de estado](../../../concepts/delta_query_overview.md) en al menos una de estas llamadas, puede realizar una consulta para obtener los cambios incrementales en los contactos de la carpeta. Esto permite mantener y sincronizar un almacén local de contactos de un usuario, sin tener que capturar cada vez todo el conjunto de contactos desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="18b47-p101">A **delta** function call for contacts in a folder is similar to a GET request, except that by appropriately applying [state tokens](../../../concepts/delta_query_overview.md) in one or more of these calls, you can query for incremental changes in the contacts in that folder. This allows you to maintain and synchronize a local store of a user's contacts without having to fetch the entire set of contacts from the server every time.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="18b47-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="18b47-105">Prerequisites</span></span>
<span data-ttu-id="18b47-106">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: _Contacts.Read_; _Contacts.ReadWrite_</span><span class="sxs-lookup"><span data-stu-id="18b47-106">One of the following **scopes** is required to execute this API: _Contacts.Read_; _Contacts.ReadWrite_</span></span>
## <a name="http-request"></a><span data-ttu-id="18b47-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="18b47-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/contactFolders/{id}/contacts/delta
GET /users/<id>/contactFolders/{id}/contacts/delta
```

### <a name="query-parameters"></a><span data-ttu-id="18b47-108">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="18b47-108">Query parameters</span></span>

<span data-ttu-id="18b47-p102">El seguimiento de cambios en los contactos conlleva al menos una llamada de una función **delta**. Si usa cualquier parámetro de consulta (distinto de `$deltatoken` y `$skiptoken`), debe especificarlo en la solicitud **delta** inicial. Microsoft Graph codifica automáticamente cualquier parámetro especificado en la parte del token de la URL `nextLink` o `deltaLink` proporcionada en la respuesta. Solo debe especificar una vez por adelantado los parámetros de consulta deseados. En solicitudes posteriores, basta con copiar y aplicar la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.</span><span class="sxs-lookup"><span data-stu-id="18b47-p102">Tracking changes in contacts incurs a round of one or more **delta** function calls. If you use any query parameter (other than `$deltatoken` and `$skiptoken`), you must specify it in the initial **delta** request. Microsoft Graph automatically encodes any specified parameters into the token portion of the `nextLink` or `deltaLink` URL provided in the response. You only need to specify any desired query parameters once upfront. In subsequent requests, simply copy and apply the `nextLink` or `deltaLink` URL from the previous response, as that URL already includes the encoded, desired parameters.</span></span>

| <span data-ttu-id="18b47-114">Parámetro de consulta</span><span class="sxs-lookup"><span data-stu-id="18b47-114">Query parameter</span></span>      | <span data-ttu-id="18b47-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="18b47-115">Type</span></span>   |<span data-ttu-id="18b47-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="18b47-116">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="18b47-117">$deltatoken</span><span class="sxs-lookup"><span data-stu-id="18b47-117">$deltatoken</span></span> | <span data-ttu-id="18b47-118">string</span><span class="sxs-lookup"><span data-stu-id="18b47-118">string</span></span> | <span data-ttu-id="18b47-p103">[Token de estado](../../../concepts/delta_query_overview.md) que se devuelve en la dirección URL de `deltaLink` de la llamada de función **delta** anterior para la misma colección de contactos. Indica el progreso de la ronda de seguimiento de cambios. Guarde y aplique toda la dirección URL `deltaLink`, incluido este token, en la primera solicitud de la siguiente ronda de seguimiento de cambios de la colección.</span><span class="sxs-lookup"><span data-stu-id="18b47-p103">A [state token](../../../concepts/delta_query_overview.md) returned in the `deltaLink` URL of the previous **delta** function call for the same contact collection, indicating the completion of that round of change tracking. Save and apply the entire `deltaLink` URL including this token in the first request of the next round of change tracking for that collection.</span></span>|
| <span data-ttu-id="18b47-121">$skiptoken</span><span class="sxs-lookup"><span data-stu-id="18b47-121">$skiptoken</span></span> | <span data-ttu-id="18b47-122">string</span><span class="sxs-lookup"><span data-stu-id="18b47-122">string</span></span> | <span data-ttu-id="18b47-123">[Token de estado](../../../concepts/delta_query_overview.md) que se devuelve en la dirección URL de `nextLink` de la llamada de función **delta**. Indica que debe realizarse el seguimiento de más cambios en la misma colección de contactos.</span><span class="sxs-lookup"><span data-stu-id="18b47-123">A [state token](../../../concepts/delta_query_overview.md) returned in the `nextLink` URL of the previous **delta** function call, indicating there are further changes to be tracked in the same contact collection.</span></span> |


#### <a name="odata-query-parameters"></a><span data-ttu-id="18b47-124">Parámetros de consulta de OData</span><span class="sxs-lookup"><span data-stu-id="18b47-124">OData query parameters</span></span>

- <span data-ttu-id="18b47-p104">Puede utilizar un parámetro de consulta `$select` como en cualquier solicitud GET para especificar solo las propiedades que necesita para un mejor rendimiento. Siempre se devuelve la propiedad _id_.</span><span class="sxs-lookup"><span data-stu-id="18b47-p104">You can use a `$select` query parameter as in any GET request to specify only the properties your need for best performance. The _id_ property is always returned.</span></span> 


## <a name="request-headers"></a><span data-ttu-id="18b47-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="18b47-127">Request headers</span></span>
| <span data-ttu-id="18b47-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="18b47-128">Name</span></span>       | <span data-ttu-id="18b47-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="18b47-129">Type</span></span> | <span data-ttu-id="18b47-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="18b47-130">Description</span></span> |
|:---------------|:----------|:----------|
| <span data-ttu-id="18b47-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="18b47-131">Authorization</span></span>  | <span data-ttu-id="18b47-132">string</span><span class="sxs-lookup"><span data-stu-id="18b47-132">string</span></span>  | <span data-ttu-id="18b47-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="18b47-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="18b47-135">Content-Type</span><span class="sxs-lookup"><span data-stu-id="18b47-135">Content-Type</span></span>  | <span data-ttu-id="18b47-136">string</span><span class="sxs-lookup"><span data-stu-id="18b47-136">string</span></span>  | <span data-ttu-id="18b47-p106">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="18b47-p106">application/json. Required.</span></span> |
| <span data-ttu-id="18b47-139">Prefer</span><span class="sxs-lookup"><span data-stu-id="18b47-139">Prefer</span></span> | <span data-ttu-id="18b47-140">string</span><span class="sxs-lookup"><span data-stu-id="18b47-140">string</span></span>  | <span data-ttu-id="18b47-p107">odata.maxpagesize={x}. Opcional.</span><span class="sxs-lookup"><span data-stu-id="18b47-p107">odata.maxpagesize={x}. Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="18b47-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="18b47-143">Response</span></span>

<span data-ttu-id="18b47-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `200, OK` y el objeto de colección [contacto](../resources/contact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="18b47-144">If successful, this method returns a `200, OK` response code and [contact](../resources/contact.md) collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="18b47-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="18b47-145">Example</span></span>
##### <a name="request"></a><span data-ttu-id="18b47-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="18b47-146">Request</span></span>
<span data-ttu-id="18b47-147">En el ejemplo siguiente se muestra cómo realizar una llamada de función **delta** única, usar un parámetro `$select` para obtener solo la propiedad **displayName** de cada contacto, y limitar el número máximo de contactos en el cuerpo de la respuesta a 2.</span><span class="sxs-lookup"><span data-stu-id="18b47-147">The following example shows how to make a single **delta** function call, use the `$select` parameter to get only each contact's **displayName** property, and limit the maximum number of contacts in the response body to 2.</span></span>

<span data-ttu-id="18b47-148">Para realizar un seguimiento de los contactos en las carpetas, debería realizar al menos una llamada de función **delta**, con unos tokens de estado adecuados, para obtener el conjunto de cambios incrementales desde la última consulta delta.</span><span class="sxs-lookup"><span data-stu-id="18b47-148">To track changes in the contacts in a folder, you would make one or more **delta** function calls, with appropriate state tokens, to get the set of incremental changes since the last delta query.</span></span> 

<span data-ttu-id="18b47-p108">Encontrará un ejemplo similar en el que se muestra cómo usar los tokens de estado para realizar un seguimiento de los cambios en los mensajes de una carpeta de correo: [Obtener los cambios incrementales en los mensajes de una carpeta](../../../concepts/delta_query_messages.md). Las diferencias principales entre realizar un seguimiento de los contactos y realizar un seguimiento de los mensajes en una carpeta están en las direcciones URL de consulta delta. Además, las respuestas de consulta devuelven colecciones **contact** en lugar de colecciones **message**.</span><span class="sxs-lookup"><span data-stu-id="18b47-p108">You can find a similar example that shows how to use the state tokens to track changes in the messages of a mail folder: [Get incremental changes to messages in a folder](../../../concepts/delta_query_messages.md). The main differences between tracking contacts and tracking messages in a folder are in the delta query request URLs, and the query responses returning **contact** rather than **message** collections.</span></span>
 
<!-- {
  "blockType": "request",
  "name": "contact_delta"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/contactFolders/{id}/contacts/delta?$select=displayName

Prefer: odata.maxpagesize=2
```

##### <a name="response"></a><span data-ttu-id="18b47-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="18b47-151">Response</span></span>
<span data-ttu-id="18b47-152">Si la solicitud es correcta, la respuesta debería incluir un símbolo de estado, que puede ser un _skipToken_</span><span class="sxs-lookup"><span data-stu-id="18b47-152">If the request is successful, the response would include a state token, which is either a _skipToken_</span></span>  
<span data-ttu-id="18b47-p109">(en un encabezado de respuesta de _@odata.nextLink_) o un _deltaToken_ (en un encabezado de respuesta de _@odata.deltaLink_). Respectivamente, indican si debe continuar con la ronda, o bien si ha terminado de obtener todos los cambios de la ronda.</span><span class="sxs-lookup"><span data-stu-id="18b47-p109">(in an _@odata.nextLink_ response header) or a _deltaToken_ (in an _@odata.deltaLink_ response header). Respectively, they indicate whether you should continue with the round or you have completed getting all the changes for that round.</span></span>

<span data-ttu-id="18b47-155">La respuesta siguiente muestra un _skipToken_ en un encabezado de respuesta de _@odata.nextLink_.</span><span class="sxs-lookup"><span data-stu-id="18b47-155">The response below shows a _skipToken_ in an _@odata.nextLink_ response header.</span></span>

<span data-ttu-id="18b47-p110">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="18b47-p110">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contact",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 337

{
  "@odata.nextLink":"https://graph.microsoft.com/v1.0/me/contactfolders('{id}')/contacts/delta?$skiptoken={_skipToken_}",
  "value": [
    {
      "parentFolderId": "parentFolderId-value",
      "birthday": "2016-10-19T10:37:00Z",
      "fileAs": "fileAs-value",
      "displayName": "displayName-value",
      "givenName": "givenName-value",
      "initials": "initials-value"
    }
  ]
}
```

### <a name="see-also"></a><span data-ttu-id="18b47-158">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="18b47-158">See also</span></span>

- [<span data-ttu-id="18b47-159">Usar la consulta delta para realizar el seguimiento de los cambios en datos de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="18b47-159">Use delta query to track changes in Microsoft Graph data</span></span>](../../../concepts/delta_query_overview.md)
- [<span data-ttu-id="18b47-160">Obtener los cambios incrementales en los mensajes de una carpeta</span><span class="sxs-lookup"><span data-stu-id="18b47-160">Get incremental changes to messages in a folder</span></span>](../../../concepts/delta_query_messages.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "contact: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->