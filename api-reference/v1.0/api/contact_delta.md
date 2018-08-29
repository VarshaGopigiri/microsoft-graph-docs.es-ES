# <a name="contact-delta"></a><span data-ttu-id="96146-101">contacto: delta</span><span class="sxs-lookup"><span data-stu-id="96146-101">contact: delta</span></span>

<span data-ttu-id="96146-102">Obtiene un conjunto de contactos que se hayan agregado, eliminado o actualizado en una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="96146-102">Get a set of contacts that have been added, deleted, or updated in a specified folder.</span></span>

<span data-ttu-id="96146-p101">La llamada de una función **delta** para los contactos de una carpeta funciona de forma similar a una solicitud GET, salvo que, al aplicar correctamente [tokens de estado](../../../concepts/delta_query_overview.md) en al menos una de estas llamadas, puede realizar una consulta para obtener los cambios incrementales en los contactos de la carpeta. Esto permite mantener y sincronizar un almacén local de contactos de un usuario, sin tener que capturar cada vez todo el conjunto de contactos desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="96146-p101">A **delta** function call for contacts in a folder is similar to a GET request, except that by appropriately applying [state tokens](../../../concepts/delta_query_overview.md) in one or more of these calls, you can query for incremental changes in the contacts in that folder. This allows you to maintain and synchronize a local store of a user's contacts without having to fetch the entire set of contacts from the server every time.</span></span>  

## <a name="permissions"></a><span data-ttu-id="96146-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="96146-105">Permissions</span></span>
<span data-ttu-id="96146-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="96146-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="96146-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="96146-108">Permission type</span></span>      | <span data-ttu-id="96146-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="96146-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="96146-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="96146-110">Delegated (work or school account)</span></span> | <span data-ttu-id="96146-111">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="96146-111">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="96146-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="96146-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="96146-113">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="96146-113">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="96146-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="96146-114">Application</span></span> | <span data-ttu-id="96146-115">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="96146-115">Contacts.Read, Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="96146-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="96146-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/contactFolders/{id}/contacts/delta
GET /users/{id}/contactFolders/{id}/contacts/delta
```

### <a name="query-parameters"></a><span data-ttu-id="96146-117">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="96146-117">Query parameters</span></span>

<span data-ttu-id="96146-p103">El seguimiento de cambios en los contactos conlleva al menos una llamada de una función **delta**. Si usa cualquier parámetro de consulta (distinto de `$deltatoken` y `$skiptoken`), debe especificarlo en la solicitud **delta** inicial. Microsoft Graph codifica automáticamente cualquier parámetro especificado en la parte del token de la URL `nextLink` o `deltaLink` proporcionada en la respuesta. Solo debe especificar una vez por adelantado los parámetros de consulta deseados. En solicitudes posteriores, basta con copiar y aplicar la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.</span><span class="sxs-lookup"><span data-stu-id="96146-p103">Tracking changes in contacts incurs a round of one or more **delta** function calls. If you use any query parameter (other than `$deltatoken` and `$skiptoken`), you must specify it in the initial **delta** request. Microsoft Graph automatically encodes any specified parameters into the token portion of the `nextLink` or `deltaLink` URL provided in the response. You only need to specify any desired query parameters once upfront. In subsequent requests, simply copy and apply the `nextLink` or `deltaLink` URL from the previous response, as that URL already includes the encoded, desired parameters.</span></span>

| <span data-ttu-id="96146-123">Parámetro de consulta</span><span class="sxs-lookup"><span data-stu-id="96146-123">Query parameter</span></span>      | <span data-ttu-id="96146-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="96146-124">Type</span></span>   |<span data-ttu-id="96146-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="96146-125">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="96146-126">$deltatoken</span><span class="sxs-lookup"><span data-stu-id="96146-126">$deltatoken</span></span> | <span data-ttu-id="96146-127">string</span><span class="sxs-lookup"><span data-stu-id="96146-127">string</span></span> | <span data-ttu-id="96146-p104">[Token de estado](../../../concepts/delta_query_overview.md) que se devuelve en la dirección URL de `deltaLink` de la llamada de función **delta** anterior para la misma colección de contactos. Indica el progreso de la ronda de seguimiento de cambios. Guarde y aplique toda la dirección URL `deltaLink`, incluido este token, en la primera solicitud de la siguiente ronda de seguimiento de cambios de la colección.</span><span class="sxs-lookup"><span data-stu-id="96146-p104">A [state token](../../../concepts/delta_query_overview.md) returned in the `deltaLink` URL of the previous **delta** function call for the same contact collection, indicating the completion of that round of change tracking. Save and apply the entire `deltaLink` URL including this token in the first request of the next round of change tracking for that collection.</span></span>|
| <span data-ttu-id="96146-130">$skiptoken</span><span class="sxs-lookup"><span data-stu-id="96146-130">$skiptoken</span></span> | <span data-ttu-id="96146-131">string</span><span class="sxs-lookup"><span data-stu-id="96146-131">string</span></span> | <span data-ttu-id="96146-132">[Token de estado](../../../concepts/delta_query_overview.md) que se devuelve en la dirección URL de `nextLink` de la llamada de función **delta**. Indica que debe realizarse el seguimiento de más cambios en la misma colección de contactos.</span><span class="sxs-lookup"><span data-stu-id="96146-132">A [state token](../../../concepts/delta_query_overview.md) returned in the `nextLink` URL of the previous **delta** function call, indicating there are further changes to be tracked in the same contact collection.</span></span> |

#### <a name="odata-query-parameters"></a><span data-ttu-id="96146-133">Parámetros de consulta de OData</span><span class="sxs-lookup"><span data-stu-id="96146-133">OData query parameters</span></span>

- <span data-ttu-id="96146-p105">Puede utilizar un parámetro de consulta `$select` como en cualquier solicitud GET para especificar solo las propiedades que necesita para un mejor rendimiento. Siempre se devuelve la propiedad _id_.</span><span class="sxs-lookup"><span data-stu-id="96146-p105">You can use a `$select` query parameter as in any GET request to specify only the properties your need for best performance. The _id_ property is always returned.</span></span> 


## <a name="request-headers"></a><span data-ttu-id="96146-136">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="96146-136">Request headers</span></span>
| <span data-ttu-id="96146-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="96146-137">Name</span></span>       | <span data-ttu-id="96146-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="96146-138">Type</span></span> | <span data-ttu-id="96146-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="96146-139">Description</span></span> |
|:---------------|:----------|:----------|
| <span data-ttu-id="96146-140">Authorization</span><span class="sxs-lookup"><span data-stu-id="96146-140">Authorization</span></span>  | <span data-ttu-id="96146-141">cadena</span><span class="sxs-lookup"><span data-stu-id="96146-141">string</span></span>  | <span data-ttu-id="96146-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="96146-p106">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="96146-144">Content-Type</span><span class="sxs-lookup"><span data-stu-id="96146-144">Content-Type</span></span>  | <span data-ttu-id="96146-145">string</span><span class="sxs-lookup"><span data-stu-id="96146-145">string</span></span>  | <span data-ttu-id="96146-p107">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="96146-p107">application/json. Required.</span></span> |
| <span data-ttu-id="96146-148">Prefer</span><span class="sxs-lookup"><span data-stu-id="96146-148">Prefer</span></span> | <span data-ttu-id="96146-149">string</span><span class="sxs-lookup"><span data-stu-id="96146-149">string</span></span>  | <span data-ttu-id="96146-p108">odata.maxpagesize={x}. Opcional.</span><span class="sxs-lookup"><span data-stu-id="96146-p108">odata.maxpagesize={x}. Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="96146-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="96146-152">Response</span></span>

<span data-ttu-id="96146-153">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto de colección [contacto](../resources/contact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="96146-153">If successful, this method returns a `200 OK` response code and [contact](../resources/contact.md) collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="96146-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="96146-154">Example</span></span>
##### <a name="request"></a><span data-ttu-id="96146-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="96146-155">Request</span></span>
<span data-ttu-id="96146-156">En el ejemplo siguiente se muestra cómo realizar una llamada de función **delta** única, usar un parámetro `$select` para obtener solo la propiedad **displayName** de cada contacto, y limitar el número máximo de contactos en el cuerpo de la respuesta a 2.</span><span class="sxs-lookup"><span data-stu-id="96146-156">The following example shows how to make a single **delta** function call, use the `$select` parameter to get only each contact's **displayName** property, and limit the maximum number of contacts in the response body to 2.</span></span>

<span data-ttu-id="96146-157">Para realizar un seguimiento de los contactos en las carpetas, debería realizar al menos una llamada de función **delta**, con unos tokens de estado adecuados, para obtener el conjunto de cambios incrementales desde la última consulta delta.</span><span class="sxs-lookup"><span data-stu-id="96146-157">To track changes in the contacts in a folder, you would make one or more **delta** function calls, with appropriate state tokens, to get the set of incremental changes since the last delta query.</span></span> 

<span data-ttu-id="96146-p109">Encontrará un ejemplo similar en el que se muestra cómo usar los tokens de estado para realizar un seguimiento de los cambios en los mensajes de una carpeta de correo: [Obtener los cambios incrementales en los mensajes de una carpeta](../../../concepts/delta_query_messages.md). Las diferencias principales entre realizar un seguimiento de los contactos y realizar un seguimiento de los mensajes en una carpeta están en las direcciones URL de consulta delta. Además, las respuestas de consulta devuelven colecciones **contact** en lugar de colecciones **message**.</span><span class="sxs-lookup"><span data-stu-id="96146-p109">You can find a similar example that shows how to use the state tokens to track changes in the messages of a mail folder: [Get incremental changes to messages in a folder](../../../concepts/delta_query_messages.md). The main differences between tracking contacts and tracking messages in a folder are in the delta query request URLs, and the query responses returning **contact** rather than **message** collections.</span></span>
 
<!-- {
  "blockType": "request",
  "name": "contact_delta"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/contactFolders/{id}/contacts/delta?$select=displayName
Prefer: odata.maxpagesize=2
```

##### <a name="response"></a><span data-ttu-id="96146-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="96146-160">Response</span></span>
<span data-ttu-id="96146-161">Si la solicitud es correcta, la respuesta debería incluir un símbolo de estado, que puede ser un _skipToken_</span><span class="sxs-lookup"><span data-stu-id="96146-161">If the request is successful, the response would include a state token, which is either a _skipToken_</span></span>  
<span data-ttu-id="96146-p110">(en un encabezado de respuesta de _@odata.nextLink_) o un _deltaToken_ (en un encabezado de respuesta de _@odata.deltaLink_). Respectivamente, indican si debe continuar con la ronda, o bien si ha terminado de obtener todos los cambios de la ronda.</span><span class="sxs-lookup"><span data-stu-id="96146-p110">(in an _@odata.nextLink_ response header) or a _deltaToken_ (in an _@odata.deltaLink_ response header). Respectively, they indicate whether you should continue with the round or you have completed getting all the changes for that round.</span></span>

<span data-ttu-id="96146-164">La respuesta siguiente muestra un _skipToken_ en un encabezado de respuesta de _@odata.nextLink_.</span><span class="sxs-lookup"><span data-stu-id="96146-164">The response below shows a _skipToken_ in an _@odata.nextLink_ response header.</span></span>

<span data-ttu-id="96146-p111">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="96146-p111">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

### <a name="see-also"></a><span data-ttu-id="96146-167">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="96146-167">See also</span></span>

- [<span data-ttu-id="96146-168">Usar la consulta delta para realizar el seguimiento de los cambios en datos de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="96146-168">Use delta query to track changes in Microsoft Graph data</span></span>](../../../concepts/delta_query_overview.md)
- [<span data-ttu-id="96146-169">Obtener los cambios incrementales en los mensajes de una carpeta</span><span class="sxs-lookup"><span data-stu-id="96146-169">Get incremental changes to messages in a folder</span></span>](../../../concepts/delta_query_messages.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "contact: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->