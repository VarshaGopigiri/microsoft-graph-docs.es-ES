# <a name="use-query-parameters-to-customize-responses"></a><span data-ttu-id="64b6c-101">Usar parámetros de consulta para personalizar respuestas</span><span class="sxs-lookup"><span data-stu-id="64b6c-101">Use query parameters to customize responses</span></span>

<span data-ttu-id="64b6c-p101">Microsoft Graph proporciona parámetros de consulta opcionales que puede usar para especificar y controlar la cantidad de datos devueltos en una respuesta. Se admiten los siguientes parámetros de consulta.</span><span class="sxs-lookup"><span data-stu-id="64b6c-p101">Microsoft Graph provides optional query parameters that you can use to specify and control the amount of data returned in a response. The following query parameters are supported.</span></span>

><span data-ttu-id="64b6c-104">**Nota:** Haga clic en los ejemplos para probarlos en [Probador de Graph][graph-explorer].</span><span class="sxs-lookup"><span data-stu-id="64b6c-104">**Note:** Click the examples to try them in [Graph Explorer][graph-explorer].</span></span>

| <span data-ttu-id="64b6c-105">Nombre</span><span class="sxs-lookup"><span data-stu-id="64b6c-105">Name</span></span>                     | <span data-ttu-id="64b6c-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="64b6c-106">Description</span></span> | <span data-ttu-id="64b6c-107">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="64b6c-107">Example</span></span>
|:-------------------------|:------------|:---------|
| [<span data-ttu-id="64b6c-108">$count</span><span class="sxs-lookup"><span data-stu-id="64b6c-108">$count</span></span>](#count-parameter)         | <span data-ttu-id="64b6c-109">Recupera el número total de recursos coincidentes.</span><span class="sxs-lookup"><span data-stu-id="64b6c-109">Retrieves the total count of matching resources.</span></span> | [`/me/messages?$top=2&$count=true`][count-example]
| [<span data-ttu-id="64b6c-110">$expand</span><span class="sxs-lookup"><span data-stu-id="64b6c-110">$expand</span></span>](#expand-parameter)       | <span data-ttu-id="64b6c-111">Recupera los recursos relacionados.</span><span class="sxs-lookup"><span data-stu-id="64b6c-111">Retrieves related resources.</span></span>|[`/groups?$expand=members`][expand-example]
| [<span data-ttu-id="64b6c-112">$filter</span><span class="sxs-lookup"><span data-stu-id="64b6c-112">$filter</span></span>](#filter-parameter)       | <span data-ttu-id="64b6c-113">Filtra los resultados (filas).</span><span class="sxs-lookup"><span data-stu-id="64b6c-113">Filters results (rows).</span></span>|[`/users?$filter=startswith(givenName,'J')`][filter-example]
| [<span data-ttu-id="64b6c-114">$format</span><span class="sxs-lookup"><span data-stu-id="64b6c-114">$format</span></span>](#format-parameter)       | <span data-ttu-id="64b6c-115">Devuelve los resultados en el formato de medio especificado.</span><span class="sxs-lookup"><span data-stu-id="64b6c-115">Returns the results in the specified media format.</span></span>|[`/users?$format=json`][format-example]
| [<span data-ttu-id="64b6c-116">$orderby</span><span class="sxs-lookup"><span data-stu-id="64b6c-116">$orderby</span></span>](#orderby-parameter)     | <span data-ttu-id="64b6c-117">Ordena los resultados.</span><span class="sxs-lookup"><span data-stu-id="64b6c-117">Orders results.</span></span>|[`/users?$orderby=displayName desc`][orderby-example]
| [<span data-ttu-id="64b6c-118">$search</span><span class="sxs-lookup"><span data-stu-id="64b6c-118">$search</span></span>](#search-parameter)       | <span data-ttu-id="64b6c-p102">Devuelve los resultados en función de los criterios de búsqueda. Actualmente, se admite en las colecciones de **mensajes** y **usuarios**.</span><span class="sxs-lookup"><span data-stu-id="64b6c-p102">Returns results based on search criteria. Currently supported on **messages** and **person** collections.</span></span>|[`/me/messages?$search=pizza`][search-example]
| [<span data-ttu-id="64b6c-121">$select</span><span class="sxs-lookup"><span data-stu-id="64b6c-121">$select</span></span>](#select-parameter)       | <span data-ttu-id="64b6c-122">Filtra las propiedades (columnas).</span><span class="sxs-lookup"><span data-stu-id="64b6c-122">Filters properties (columns).</span></span>|[`/users?$select=givenName,surname`][select-example]
| [<span data-ttu-id="64b6c-123">$skip</span><span class="sxs-lookup"><span data-stu-id="64b6c-123">$skip</span></span>](#skip-parameter)           | <span data-ttu-id="64b6c-p103">Indexa en un conjunto de resultados. También se usa en algunas API para implementar la paginación y se puede usar junto a `$top` para paginar manualmente los resultados.</span><span class="sxs-lookup"><span data-stu-id="64b6c-p103">Indexes into a result set. Also used by some APIs to implement paging and can be used together with `$top` to manually page results.</span></span> | [`/me/messages?$skip=11`][skip-example]
| [<span data-ttu-id="64b6c-126">$skipToken</span><span class="sxs-lookup"><span data-stu-id="64b6c-126">$skipToken</span></span>](#skiptoken-parameter) | <span data-ttu-id="64b6c-p104">Recupera la siguiente página de resultados de conjuntos de resultados que abarcan varias páginas. (Algunas API usan `$skip` en su lugar).</span><span class="sxs-lookup"><span data-stu-id="64b6c-p104">Retrieves the next page of results from result sets that span multiple pages. (Some APIs use `$skip` instead.)</span></span> | `/users?$skiptoken=X%274453707402000100000017...`|
| [<span data-ttu-id="64b6c-129">$top</span><span class="sxs-lookup"><span data-stu-id="64b6c-129">$top</span></span>](#top-parameter)             | <span data-ttu-id="64b6c-130">Establece el tamaño de la página de resultados.</span><span class="sxs-lookup"><span data-stu-id="64b6c-130">Sets the page size of results.</span></span> |[`/users?$top=2`][top-example]



<span data-ttu-id="64b6c-131">Estos parámetros son compatibles con el [lenguaje de consulta de OData V4][odata-query].</span><span class="sxs-lookup"><span data-stu-id="64b6c-131">These parameters are compatible with the [OData V4 query language][odata-query].</span></span> <span data-ttu-id="64b6c-132">No todos los parámetros se admiten en todas las API de Microsoft Graph, y la compatibilidad puede variar considerablemente entre los puntos de conexión `v1.0` y `beta`.</span><span class="sxs-lookup"><span data-stu-id="64b6c-132">Not all parameters are supported across all Microsoft Graph APIs, and support might differ significantly between the `v1.0` and `beta` endpoints.</span></span> 

> <span data-ttu-id="64b6c-p106">**Nota:** En el punto de conexión `beta`, el prefijo `$` es opcional. Por ejemplo, en lugar de `$filter`, puede usar `filter`. Para obtener más detalles y ejemplos, vea [Compatibilidad con los parámetros de consulta sin el prefijo "$" en Microsoft Graph](http://dev.office.com/queryparametersinMicrosoftGraph).</span><span class="sxs-lookup"><span data-stu-id="64b6c-p106">**Note:** On the `beta` endpoint, the `$` prefix is optional. For example, instead of `$filter`, you can use `filter`. For more details and examples, see [Supporting query parameters without $ prefixes in Microsoft Graph](http://dev.office.com/queryparametersinMicrosoftGraph).</span></span>

## <a name="encoding-query-parameters"></a><span data-ttu-id="64b6c-136">Codificación de parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="64b6c-136">Encoding query parameters</span></span>

<span data-ttu-id="64b6c-137">Los valores de los parámetros de consulta deben ser codificados por porcentaje.</span><span class="sxs-lookup"><span data-stu-id="64b6c-137">The values of query parameters should be percent-encoded.</span></span> <span data-ttu-id="64b6c-138">Muchos clientes HTTP, exploradores y herramientas (como el [Probador de Graph][graph-explorer]) le servirán de ayuda.</span><span class="sxs-lookup"><span data-stu-id="64b6c-138">Many HTTP clients, browsers, and tools (such as the [Graph Explorer][graph-explorer]) will help you with this.</span></span> <span data-ttu-id="64b6c-139">Si una consulta produce un error, puede deberse a que los valores de los parámetros de consulta no se han codificado correctamente.</span><span class="sxs-lookup"><span data-stu-id="64b6c-139">If a query is failing, one possible cause is failure to encode the query parameter values appropriately.</span></span>

<span data-ttu-id="64b6c-140">Una dirección URL sin codificar tiene el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="64b6c-140">An unencoded URL looks like this:</span></span>

```http
GET https://graph.microsoft.com/v1.0/users?$filter=startswith(givenName, 'J')
```

<span data-ttu-id="64b6c-141">Una dirección URL codificada correctamente tiene el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="64b6c-141">A properly encoded URL looks like this:</span></span>

```http
GET https://graph.microsoft.com/v1.0/users?$filter=startswith(givenName%2C+'J')
```

## <a name="count-parameter"></a><span data-ttu-id="64b6c-142">parámetro de recuento</span><span class="sxs-lookup"><span data-stu-id="64b6c-142">count parameter</span></span>

<span data-ttu-id="64b6c-143">Use el parámetro de consulta `$count` para incluir un recuento del número total de elementos de una colección junto con la página de valores de datos que se devuelve desde Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="64b6c-143">Use the `$count` query parameter to include a count of the total number of items in a collection alongside the page of data values returned from Microsoft Graph.</span></span> 

<span data-ttu-id="64b6c-144">Por ejemplo, la siguiente solicitud devolverá tanto la colección de **contactos** del usuario actual como el número de elementos de la colección de **contactos** en la propiedad `@odata.count`.</span><span class="sxs-lookup"><span data-stu-id="64b6c-144">For example, the following request will return both the **contact** collection of the current user, and the number of items in the **contact** collection in the `@odata.count` property.</span></span>

```http
GET  https://graph.microsoft.com/v1.0/me/contacts?$count=true
```

[<span data-ttu-id="64b6c-145">Probar en el Probador de Graph</span><span class="sxs-lookup"><span data-stu-id="64b6c-145">Try in Graph Explorer</span></span>](https://developer.microsoft.com/graph/graph-explorer?request=me/contacts?$count=true&method=GET&version=v1.0)


><span data-ttu-id="64b6c-146">**Nota:** `$count` no se admite con colecciones de recursos que se derivan de [directoryObject](../api-reference/v1.0/resources/directoryobject.md), como las colecciones de [usuarios](../api-reference/v1.0/resources/user.md) o [grupos](../api-reference/v1.0/resources/group.md).</span><span class="sxs-lookup"><span data-stu-id="64b6c-146">**Note:** `$count` is not supported for collections of resources that derive from [directoryObject](../api-reference/v1.0/resources/directoryobject.md) like collections of [users](../api-reference/v1.0/resources/user.md) or [groups](../api-reference/v1.0/resources/group.md).</span></span>

## <a name="expand-parameter"></a><span data-ttu-id="64b6c-147">parámetro de expansión</span><span class="sxs-lookup"><span data-stu-id="64b6c-147">expand parameter</span></span>

<span data-ttu-id="64b6c-148">Muchos de los recursos de Microsoft Graph exponen ambas propiedades declaradas de los recursos, así como sus relaciones con otros recursos.</span><span class="sxs-lookup"><span data-stu-id="64b6c-148">Many Microsoft Graph resources expose both declared properties of the resource as well as its relationships with other resources.</span></span> <span data-ttu-id="64b6c-149">Estas relaciones también se denominan propiedades de referencia o propiedades de navegación, y pueden hacer referencia a un único recurso o a una colección de recursos.</span><span class="sxs-lookup"><span data-stu-id="64b6c-149">These relationships are also called reference properties or navigation properties, and they can reference either a single resource or a collection of resources.</span></span> <span data-ttu-id="64b6c-150">Por ejemplo, las carpetas de correo, el administrador y los informes directos de un usuario se exponen como relaciones.</span><span class="sxs-lookup"><span data-stu-id="64b6c-150">For example, the mail folders, manager, and direct reports of a user are all exposed as relationships.</span></span> 

<span data-ttu-id="64b6c-p109">Normalmente, se pueden consultar las propiedades de un recurso o una de sus relaciones en una sola solicitud, pero no ambas. Puede usar el parámetro de cadena de consulta `$expand` para incluir en los resultados de la consulta el recurso expandido o la colección a la que se hace referencia con una única relación (propiedad de navegación).</span><span class="sxs-lookup"><span data-stu-id="64b6c-p109">Normally, you can query either the properties of a resource or one of its relationships in a single request, but not both. You can use the `$expand` query string parameter to include the expanded resource or collection referenced by a single relationship (navigation property) in your results.</span></span>

<span data-ttu-id="64b6c-153">En el ejemplo siguiente se obtiene la información de la unidad raíz junto con los elementos secundarios de nivel superior de una unidad:</span><span class="sxs-lookup"><span data-stu-id="64b6c-153">The following example gets root drive information along with the top-level child items in a drive:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/drive/root?$expand=children
```

[<span data-ttu-id="64b6c-154">Probar en el Probador de Graph</span><span class="sxs-lookup"><span data-stu-id="64b6c-154">Try in Graph Explorer</span></span>](https://developer.microsoft.com/graph/graph-explorer?request=me/drive/root?$expand=children&method=GET&version=v1.0)

<span data-ttu-id="64b6c-p110">Con algunas colecciones de recursos, también se pueden especificar las propiedades que se van a devolver en los recursos expandidos si se agrega un parámetro `$select`. En el ejemplo siguiente se realiza la misma consulta que en el anterior, pero se usa una instrucción [`$select`](#select-parameter) para limitar las propiedades devueltas para los elementos secundarios expandidos a las propiedades **id** y **name**.</span><span class="sxs-lookup"><span data-stu-id="64b6c-p110">With some resource collections, you can also specify the properties to be returned in the expanded resources by adding a `$select` parameter. The following example performs the same query as the previous example but uses a [`$select`](#select-parameter) statement to limit the properties returned for the expanded child items to the **id** and **name** properties.</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/drive/root?$expand=children($select=id,name)
```

<span data-ttu-id="64b6c-157">[Probar en el Probador de Graph][expand-example]</span><span class="sxs-lookup"><span data-stu-id="64b6c-157">[Try in Graph Explorer][expand-example]</span></span>

> <span data-ttu-id="64b6c-p111">**Nota:** No todas las relaciones y recursos admiten el parámetro de consulta `$expand`. Por ejemplo, se pueden expandir las relaciones **directReports**, **manager** y **memberOf** de un usuario, pero no se pueden expandir sus relaciones **events**, **messages** o **photo**. No todos los recursos o relaciones admiten el uso de `$select` en elementos expandidos.</span><span class="sxs-lookup"><span data-stu-id="64b6c-p111">**Note:** Not all relationships and resources support the `$expand` query parameter. For example, you can expand the **directReports**, **manager**, and **memberOf** relationships on a user, but you cannot expand its **events**, **messages**, or **photo** relationships. Not all resources or relationships support using `$select` on expanded items.</span></span> 
> 
> <span data-ttu-id="64b6c-161">Con recursos de Azure AD que se derivan de [directoryObject](../api-reference/v1.0/resources/directoryobject.md), como [user](../api-reference/v1.0/resources/user.md) y [group](../api-reference/v1.0/resources/group.md), solo se admite `$expand` para `beta` y normalmente devuelve un máximo de 20 elementos para la relación expandida.</span><span class="sxs-lookup"><span data-stu-id="64b6c-161">With Azure AD resources that derive from [directoryObject](../api-reference/v1.0/resources/directoryobject.md), like [user](../api-reference/v1.0/resources/user.md) and [group](../api-reference/v1.0/resources/group.md), `$expand` is only supported for `beta` and  typically returns a maximum of 20 items for the expanded relationship.</span></span>

## <a name="filter-parameter"></a><span data-ttu-id="64b6c-162">parámetro de filtrado</span><span class="sxs-lookup"><span data-stu-id="64b6c-162">filter parameter</span></span>

<span data-ttu-id="64b6c-163">Use el parámetro de consulta `$filter` para recuperar solo un subconjunto de una colección.</span><span class="sxs-lookup"><span data-stu-id="64b6c-163">Use the `$filter` query parameter to retrieve just a subset of a collection.</span></span> 

<span data-ttu-id="64b6c-164">Por ejemplo, para buscar usuarios cuyos nombres para mostrar comiencen por la letra "J", use `startswith`.</span><span class="sxs-lookup"><span data-stu-id="64b6c-164">For example, to find users whose display name starts with the letter 'J', use `startswith`.</span></span>

```http
GET https://graph.microsoft.com/v1.0/users?$filter=startswith(displayName,'J')
```

<span data-ttu-id="64b6c-165">[Probar en el Probador de Graph][filter-example]</span><span class="sxs-lookup"><span data-stu-id="64b6c-165">[Try in Graph Explorer][filter-example]</span></span>

<span data-ttu-id="64b6c-166">La compatibilidad con los operadores `$filter` varía en función de la API de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="64b6c-166">Support for `$filter` operators varies across Microsoft Graph APIs.</span></span> <span data-ttu-id="64b6c-167">Generalmente, se admiten los siguientes operadores lógicos:</span><span class="sxs-lookup"><span data-stu-id="64b6c-167">The following logical operators are generally supported:</span></span> 

- <span data-ttu-id="64b6c-168">igual a (`eq`)</span><span class="sxs-lookup"><span data-stu-id="64b6c-168">equals (`eq`)</span></span>
- <span data-ttu-id="64b6c-169">no es igual a (`ne`)</span><span class="sxs-lookup"><span data-stu-id="64b6c-169">not equals (`ne`)</span></span>
- <span data-ttu-id="64b6c-170">mayor que (`gt`)</span><span class="sxs-lookup"><span data-stu-id="64b6c-170">greater than (`gt`)</span></span>
- <span data-ttu-id="64b6c-171">mayor o igual que (`ge`)</span><span class="sxs-lookup"><span data-stu-id="64b6c-171">greater than or equals (`ge`)</span></span>
- <span data-ttu-id="64b6c-172">menor que (`lt`), menor o igual que (`le`)</span><span class="sxs-lookup"><span data-stu-id="64b6c-172">less than (`lt`), less than or equals (`le`)</span></span>
- <span data-ttu-id="64b6c-173">y (`and`)</span><span class="sxs-lookup"><span data-stu-id="64b6c-173">and (`and`)</span></span>
- <span data-ttu-id="64b6c-174">o (`or`)</span><span class="sxs-lookup"><span data-stu-id="64b6c-174">or (`or`)</span></span>
- <span data-ttu-id="64b6c-175">no (`not`)</span><span class="sxs-lookup"><span data-stu-id="64b6c-175">not (`not`)</span></span>
 
<span data-ttu-id="64b6c-176">El operador de cadena `startswith` se suele admitir.</span><span class="sxs-lookup"><span data-stu-id="64b6c-176">The `startswith` string operator is often supported.</span></span> <span data-ttu-id="64b6c-177">El operador lambda `any` se admite con algunas API.</span><span class="sxs-lookup"><span data-stu-id="64b6c-177">The `any` lambda operator is supported for some APIs.</span></span> <span data-ttu-id="64b6c-178">Para obtener algunos ejemplos de uso, vea la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="64b6c-178">For some  usage examples, see the following table.</span></span> <span data-ttu-id="64b6c-179">Para obtener detalles adicionales sobre la sintaxis de `$filter`, vea el [protocolo OData][odata-filter].</span><span class="sxs-lookup"><span data-stu-id="64b6c-179">For more details about `$filter` syntax, see the [OData protocol][odata-filter].</span></span>  

<span data-ttu-id="64b6c-180">En la tabla siguiente se muestran algunos ejemplos de uso del parámetro de consulta `$filter`.</span><span class="sxs-lookup"><span data-stu-id="64b6c-180">The following table shows some examples that use the `$filter` query parameter.</span></span>

> <span data-ttu-id="64b6c-181">**Nota:** Haga clic en los ejemplos para probarlos en [Probador de Graph][graph-explorer].</span><span class="sxs-lookup"><span data-stu-id="64b6c-181">**Note:** Click the examples to try them in [Graph Explorer][graph-explorer].</span></span>

| <span data-ttu-id="64b6c-182">Descripción</span><span class="sxs-lookup"><span data-stu-id="64b6c-182">Description</span></span> | <span data-ttu-id="64b6c-183">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="64b6c-183">Example</span></span>
|:------------|:--------|
| <span data-ttu-id="64b6c-184">Buscar usuarios con el nombre Mary en varias propiedades.</span><span class="sxs-lookup"><span data-stu-id="64b6c-184">Search for users with the name Mary across multiple properties.</span></span> | [`https://graph.microsoft.com/v1.0/users?$filter=startswith(displayName,'mary') or startswith(givenName,'mary') or startswith(surname,'mary') or startswith(mail,'mary') or startswith(userPrincipalName,'mary')`](https://developer.microsoft.com/graph/graph-explorer?request=users?$filter=startswith(displayName,'mary')+or+startswith(givenName,'mary')+or+startswith(surname,'mary')+or+startswith(mail,'mary')+or+startswith(userPrincipalName,'mary')&method=GET&version=v1.0) 
| <span data-ttu-id="64b6c-185">Obtener todos los eventos del usuario que inició sesión que comiencen después del 1/7/2017.</span><span class="sxs-lookup"><span data-stu-id="64b6c-185">Get all the signed-in user's events that start after 7/1/2017.</span></span> | [`https://graph.microsoft.com/v1.0/me/events?$filter=start/dateTime ge '2017-07-01T08:00'`](https://developer.microsoft.com/graph/graph-explorer?request=me/events?$filter=start/dateTime+ge+'2017-07-01T08:00'&method=GET&version=v1.0) 
| <span data-ttu-id="64b6c-186">Obtener todos los correos electrónicos de una dirección específica recibidos por el usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="64b6c-186">Get all emails from a specific address received by the signed-in user.</span></span> | [`https://graph.microsoft.com/v1.0/me/messages?$filter=from/emailAddress/address eq 'someuser@example.com'`](https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$filter=from/emailAddress/address+eq+'someuser@.com'&method=GET&version=v1.0) 
| <span data-ttu-id="64b6c-187">Obtener todos los correos electrónicos recibidos en abril de 2017 por el usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="64b6c-187">Get all emails received by the signed-in user in April 2017.</span></span> | [`https://graph.microsoft.com/v1.0/me/mailFolders/inbox/messages?$filter=ReceivedDateTime ge 2017-04-01 and receivedDateTime lt 2017-05-01`](https://developer.microsoft.com/graph/graph-explorer?request=me/mailFolders/inbox/messages?$filter=ReceivedDateTime+ge+2017-04-01+and+receivedDateTime+lt+2017-05-01&method=GET&version=v1.0) 
| <span data-ttu-id="64b6c-188">Obtener todos los correos electrónicos no leídos en la Bandeja de entrada del usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="64b6c-188">Get all unread mail in the signed-in user's Inbox.</span></span> | [`https://graph.microsoft.com/v1.0/me/mailFolders/inbox/messages?$filter=isRead eq false`](https://developer.microsoft.com/graph/graph-explorer?request=me/mailFolders/inbox/messages?$filter=isRead+eq+false&method=GET&version=v1.0) 
| <span data-ttu-id="64b6c-189">Enumerar todos los grupos de Office 365 de una organización.</span><span class="sxs-lookup"><span data-stu-id="64b6c-189">List all Office 365 groups in an organization.</span></span> | [`https://graph.microsoft.com/v1.0/groups?$filter=groupTypes/any(c:c+eq+'Unified')`](https://developer.microsoft.com/graph/graph-explorer?request=groups?$filter=groupTypes/any(c:c+eq+'Unified')&method=GET&version=v1.0) 

> <span data-ttu-id="64b6c-p114">**Nota:** Los operadores `$filter` siguientes no se admiten para recursos de Azure AD: `ne`, `gt`, `ge`, `lt`, `le` y `not`. El operador de cadena `contains` actualmente no se admite en ningún recurso de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="64b6c-p114">**Note:** The following `$filter` operators are not supported for Azure AD resources:  `ne`, `gt`, `ge`, `lt`, `le`, and `not`. The `contains` string operator is currently not supported on any Microsoft Graph resources.</span></span>

## <a name="format-parameter"></a><span data-ttu-id="64b6c-192">parámetro de formato</span><span class="sxs-lookup"><span data-stu-id="64b6c-192">format parameter</span></span>

<span data-ttu-id="64b6c-193">Use el parámetro de consulta `$format` para especificar el formato de medio de los elementos devueltos desde Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="64b6c-193">Use the `$format` query parameter to specify the media format of the items returned from Microsoft Graph.</span></span>

<span data-ttu-id="64b6c-194">Por ejemplo, la solicitud siguiente devuelve los usuarios de la organización en formato JSON:</span><span class="sxs-lookup"><span data-stu-id="64b6c-194">For example, the following request returns the users in the organization in the json format:</span></span>

```http
GET https://graph.microsoft.com/v1.0/users?$format=json
```

<span data-ttu-id="64b6c-195">[Probar en el Probador de Graph][format-example]</span><span class="sxs-lookup"><span data-stu-id="64b6c-195">[Try in Graph Explorer][format-example]</span></span>

> <span data-ttu-id="64b6c-196">**Nota**: El parámetro de consulta `$format` admite varios formatos, como atom, xml y json, pero puede que no todos los formatos devuelvan resultados.</span><span class="sxs-lookup"><span data-stu-id="64b6c-196">**Note:** The `$format` query parameter supports a number of formats (for example, atom, xml, and json) but results may not be returned in all formats.</span></span>

## <a name="orderby-parameter"></a><span data-ttu-id="64b6c-197">parámetro orderby</span><span class="sxs-lookup"><span data-stu-id="64b6c-197">orderby parameter</span></span>

<span data-ttu-id="64b6c-198">Use el parámetro de consulta `$orderby` para especificar el criterio de ordenación de los elementos devueltos desde Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="64b6c-198">Use the `$orderby` query parameter to specify the sort order of the items returned from Microsoft Graph.</span></span>

<span data-ttu-id="64b6c-199">Por ejemplo, la solicitud siguiente devuelve los usuarios de la organización ordenados por su nombre para mostrar:</span><span class="sxs-lookup"><span data-stu-id="64b6c-199">For example, the following request returns the users in the organization ordered by their display name:</span></span>

```http
GET https://graph.microsoft.com/v1.0/users?$orderby=displayName
```
<span data-ttu-id="64b6c-200">[Probar en el Probador de Graph][orderby-example]</span><span class="sxs-lookup"><span data-stu-id="64b6c-200">[Try in Graph Explorer][orderby-example]</span></span>

<span data-ttu-id="64b6c-p115">También puede ordenar por entidades de tipo complejo. La solicitud siguiente obtiene los mensajes y los ordena por el campo **address** de la propiedad **from**, que es del tipo complejo **emailAddress**:</span><span class="sxs-lookup"><span data-stu-id="64b6c-p115">You can also sort by complex type entities. The following request gets messages and sorts them by the **address** field of the **from** property, which is of the complex type **emailAddress**:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/messages?$orderby=from/emailAddress/address
```
[<span data-ttu-id="64b6c-203">Probar en el Probador de Graph</span><span class="sxs-lookup"><span data-stu-id="64b6c-203">Try in Graph Explorer</span></span>](https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$orderby=from/emailAddress/address&method=GET&version=v1.0)

<span data-ttu-id="64b6c-204">Para ordenar los resultados en orden ascendente o descendente, anexe `asc` o `desc` al nombre del campo, separado por un espacio. Por ejemplo, `?$orderby=name%20desc`.</span><span class="sxs-lookup"><span data-stu-id="64b6c-204">To sort the results in ascending or descending order, append either `asc` or `desc` to the field name, separated by a space; for example, `?$orderby=name%20desc`.</span></span>

<span data-ttu-id="64b6c-205">Con algunas API se pueden ordenar los resultados por varias propiedades.</span><span class="sxs-lookup"><span data-stu-id="64b6c-205">With some APIs, you can order results on multiple properties.</span></span> <span data-ttu-id="64b6c-206">Por ejemplo, en la siguiente solicitud se ordenan los mensajes en la Bandeja de entrada del usuario; primero por el nombre de la persona que lo envió en orden descendente (de la Z a la A) y, después, por asunto en orden ascendente (el valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="64b6c-206">For example, the following request orders the messages in the user's Inbox, first by the name of the person who sent it in descending order (Z to A), and then by subject in ascending order (default).</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/mailFolders/Inbox/messages?$orderby=from/emailAddress/name desc,subject
```

[<span data-ttu-id="64b6c-207">Probar en el Probador de Graph</span><span class="sxs-lookup"><span data-stu-id="64b6c-207">Try in Graph Explorer</span></span>](https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$orderby=from/emailAddress/name%20desc,subject&method=GET&version=v1.0)

<span data-ttu-id="64b6c-208">Si especifica $filter, el servidor deducirá un criterio de ordenación para los resultados.</span><span class="sxs-lookup"><span data-stu-id="64b6c-208">When you specify $filter the server will infer a sort order for the results.</span></span> <span data-ttu-id="64b6c-209">Si usa tanto `$orderby` como `$filter`, porque el servidor siempre deduce un criterio de ordenación para los resultados de un `$filter`, las propiedades del `$filter` deben estar primero en `$orderby`, antes que cualquier otra propiedad y deben estar en el orden en el que aparecen en el parámetro `$filter`.</span><span class="sxs-lookup"><span data-stu-id="64b6c-209">If you use both `$orderby` and `$filter`, because the server always infers a sort order for the results of a `$filter`, the properties in the `$filter` must be listed first in the `$orderby` before any other properties, and they must be listed in the order that they appear in the `$filter` parameter.</span></span> 

<span data-ttu-id="64b6c-210">En el siguiente ejemplo, se muestra una consulta filtrada por las propiedades **subject** y **importance**, y después ordenada por las propiedades **subject**, **importance** y **receivedDateTime** en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="64b6c-210">The following example shows a query filtered by the **subject** and **importance** properties, and then sorted by the **subject**, **importance**, and **receivedDateTime** properties in descending order.</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/messages?$filter=Subject eq 'welcome to exchange unified messaging' and importance eq 'normal'&$orderby=subject,importance,receivedDateTime desc
```

[<span data-ttu-id="64b6c-211">Probar en el Probador de Graph</span><span class="sxs-lookup"><span data-stu-id="64b6c-211">Try in Graph Explorer</span></span>](https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$filter=subject%20eq%20%27welcome to exchange unified messaging%27%20and%20importance%20eq%20%27normal%27%20&$orderby=subject,importance,receivedDateTime%20desc&method=GET&version=v1.0)

 > <span data-ttu-id="64b6c-212">**Nota:** Con recursos de Azure AD que se derivan de [directoryObject](../api-reference/v1.0/resources/directoryobject.md), como [user](../api-reference/v1.0/resources/user.md) y [group](../api-reference/v1.0/resources/group.md), no se puede combinar `$orderby` con expresiones`$filter`.</span><span class="sxs-lookup"><span data-stu-id="64b6c-212">**Note:** With Azure AD resources that derive from [directoryObject](../api-reference/v1.0/resources/directoryobject.md), like [user](../api-reference/v1.0/resources/user.md) and [group](../api-reference/v1.0/resources/group.md), you cannot combine `$orderby` with `$filter` expressions.</span></span> 

## <a name="search-parameter"></a><span data-ttu-id="64b6c-213">parámetro de búsqueda</span><span class="sxs-lookup"><span data-stu-id="64b6c-213">search parameter</span></span>

<span data-ttu-id="64b6c-214">Use el parámetro de consulta `$search` para restringir los resultados de una solicitud para que coincidan con un criterio de búsqueda</span><span class="sxs-lookup"><span data-stu-id="64b6c-214">Use the `$search` query parameter to restrict the results of a request to match a search criterion.</span></span>

> <span data-ttu-id="64b6c-p118">**Nota:** Actualmente **solo** se pueden buscar las colecciones [message](../api-reference/v1.0/resources/message.md) y [person](../api-reference/v1.0/resources/person.md). Una solicitud `$search` devuelve hasta 250 resultados. No puede usar [`$filter`](#filter-parameter) o [`$orderby`](#orderby-parameter) en una solicitud de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="64b6c-p118">**Note:** You can currently search **only** [message](../api-reference/v1.0/resources/message.md) and [person](../api-reference/v1.0/resources/person.md) collections. A `$search` request returns up to 250 results. You cannot use [`$filter`](#filter-parameter) or [`$orderby`](#orderby-parameter) in a search request.</span></span>

### <a name="using-search-on-message-collections"></a><span data-ttu-id="64b6c-218">Uso de $search en colecciones de mensajes</span><span class="sxs-lookup"><span data-stu-id="64b6c-218">Using $search on message collections</span></span>

<span data-ttu-id="64b6c-219">Las aplicaciones de Office 365, como Outlook y SharePoint, admiten la sintaxis del lenguaje de consulta de palabras clave (KQL) para realizar búsquedas.</span><span class="sxs-lookup"><span data-stu-id="64b6c-219">Office 365 applications, such as Outlook and SharePoint, support the Keyword Query Language (KQL) syntax to do searches.</span></span> <span data-ttu-id="64b6c-220">Esto proporciona la comodidad de un dominio de detección común para sus almacenes de datos.</span><span class="sxs-lookup"><span data-stu-id="64b6c-220">This provides the convenience of a common discovery domain for their data stores.</span></span> 

<span data-ttu-id="64b6c-221">Cuando busca en las colecciones de mensajes, los resultados se ordenan por la fecha y la hora en que se ha enviado el mensaje.</span><span class="sxs-lookup"><span data-stu-id="64b6c-221">When you search message collections, the results are sorted by the date and time that the message was sent.</span></span> 

<span data-ttu-id="64b6c-222">Puede especificar las siguientes propiedades en un **mensaje** en un criterio `$search`:</span><span class="sxs-lookup"><span data-stu-id="64b6c-222">You can specify the following properties on a **message** in a `$search` criterion:</span></span>

- <span data-ttu-id="64b6c-223">**attachments**</span><span class="sxs-lookup"><span data-stu-id="64b6c-223">**attachments**</span></span>
- <span data-ttu-id="64b6c-224">**bccRecipients**</span><span class="sxs-lookup"><span data-stu-id="64b6c-224">**bccRecipients**</span></span>
- <span data-ttu-id="64b6c-225">**body**</span><span class="sxs-lookup"><span data-stu-id="64b6c-225">**body**</span></span>
- <span data-ttu-id="64b6c-226">**category**</span><span class="sxs-lookup"><span data-stu-id="64b6c-226">**category**</span></span>
- <span data-ttu-id="64b6c-227">**ccRecipients**</span><span class="sxs-lookup"><span data-stu-id="64b6c-227">**ccRecipients**</span></span>
- <span data-ttu-id="64b6c-228">**content**</span><span class="sxs-lookup"><span data-stu-id="64b6c-228">**content**</span></span>
- <span data-ttu-id="64b6c-229">**from**</span><span class="sxs-lookup"><span data-stu-id="64b6c-229">**from**</span></span>
- <span data-ttu-id="64b6c-230">**hasAttachments**</span><span class="sxs-lookup"><span data-stu-id="64b6c-230">**hasAttachments**</span></span>
- <span data-ttu-id="64b6c-231">**participants**</span><span class="sxs-lookup"><span data-stu-id="64b6c-231">**participants**</span></span>
- <span data-ttu-id="64b6c-232">**receivedDateTime**</span><span class="sxs-lookup"><span data-stu-id="64b6c-232">**receivedDateTime**</span></span>
- <span data-ttu-id="64b6c-233">**sender**</span><span class="sxs-lookup"><span data-stu-id="64b6c-233">**sender**</span></span>
- <span data-ttu-id="64b6c-234">**subject**</span><span class="sxs-lookup"><span data-stu-id="64b6c-234">**subject**</span></span>
- <span data-ttu-id="64b6c-235">**toRecipients**</span><span class="sxs-lookup"><span data-stu-id="64b6c-235">**toRecipients**</span></span>

<span data-ttu-id="64b6c-236">Si realiza una búsqueda en mensajes y especifica un solo valor, la búsqueda se lleva a cabo con las propiedades de búsqueda predeterminadas de **from**, **subject** y **body**.</span><span class="sxs-lookup"><span data-stu-id="64b6c-236">If you do a search on messages and specify only a value, the search is carried out on the default search properties of **from**, **subject**, and **body**.</span></span>

<span data-ttu-id="64b6c-237">En el ejemplo siguiente, se devuelven todos los mensajes del buzón del usuario que ha iniciado sesión que contienen la palabra "pizza" en cualquiera de las tres propiedades de búsqueda predeterminadas:</span><span class="sxs-lookup"><span data-stu-id="64b6c-237">The following example returns all messages in the signed-in user's Inbox that contains "pizza" in any of the three default search properties:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/messages?$search="pizza"
```

<span data-ttu-id="64b6c-238">[Probar en el Probador de Graph][search-example]</span><span class="sxs-lookup"><span data-stu-id="64b6c-238">[Try in Graph Explorer][search-example]</span></span>

<span data-ttu-id="64b6c-239">En el ejemplo siguiente, se buscan todos los mensajes en el buzón del usuario que se enviaron desde una dirección de correo específica:</span><span class="sxs-lookup"><span data-stu-id="64b6c-239">The next example searches all messages in the user's Inbox that were sent from a specific email address:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/messages?$search="from:help@contoso.com"
```
<span data-ttu-id="64b6c-240">Para obtener más información sobre KQL, como la sintaxis, operadores compatibles y sugerencias de búsqueda, vea los artículos siguientes:</span><span class="sxs-lookup"><span data-stu-id="64b6c-240">For more information about KQL such as the syntax, supported operators, and tips on searching, see the following articles:</span></span>

- [<span data-ttu-id="64b6c-241">Referencia de la sintaxis del lenguaje de consultas de palabras clave (KQL)</span><span class="sxs-lookup"><span data-stu-id="64b6c-241">Keyword Query Language (KQL) syntax reference</span></span>](https://docs.microsoft.com/es-ES/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference)

- <span data-ttu-id="64b6c-242">
  [Propiedades de mensajes y operadores de búsqueda para eDiscovery local en Exchange 2016](https://technet.microsoft.com/en-us/library/dn774955(v=exchg.160).aspx)</span><span class="sxs-lookup"><span data-stu-id="64b6c-242">[Message properties and search operators for In-Place eDiscovery in Exchange 2016](https://technet.microsoft.com/en-us/library/dn774955(v=exchg.160).aspx)</span></span>

### <a name="using-search-on-person-collections"></a><span data-ttu-id="64b6c-243">Uso de $search en colecciones de usuarios</span><span class="sxs-lookup"><span data-stu-id="64b6c-243">Using $search on person collections</span></span>

<span data-ttu-id="64b6c-p120">Puede usar la API de contactos de Microsoft Graph para recuperar los contactos más relevantes para un usuario. La relevancia viene determinada por las relaciones empresariales y los patrones de comunicación y colaboración del usuario. La API de contactos admite el parámetro de consulta `$search`.</span><span class="sxs-lookup"><span data-stu-id="64b6c-p120">You can use the Microsoft Graph People API to retrieve the people who are most relevant to a user. Relevance is determined by the user’s communication and collaboration patterns and business relationships. The People API supports the `$search` query parameter.</span></span>

<span data-ttu-id="64b6c-247">Las búsquedas de contactos se realizan en las propiedades **displayName** y **emailAddress** del recurso [person](../api-reference/v1.0/resources/person.md).</span><span class="sxs-lookup"><span data-stu-id="64b6c-247">Searches on people occur on both the **displayName** and **emailAddress** properties of the [person](../api-reference/v1.0/resources/person.md) resource.</span></span>

<span data-ttu-id="64b6c-248">La solicitud siguiente busca una persona llamada "Irene McGowen" en las propiedades **displayName** y **emailAddress** de todos los miembros de la colección **people** del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="64b6c-248">The following request does a search for a person named "Irene McGowen" in the **displayName** and **emailAddress** properties in each person in the **people** collection of the signed-in user.</span></span> <span data-ttu-id="64b6c-249">Dado que existe una persona llamada "Irene McGowan" relevante para el usuario que ha iniciado sesión, se devuelve la información de "Irene McGowan".</span><span class="sxs-lookup"><span data-stu-id="64b6c-249">The following request does a search for a person named "Irene McGowen". Because a person named "Irene McGowan" is relevant to the signed-in user, the information for "Irene McGowan" is returned.</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/people/?$search="Irene McGowen"
```

<span data-ttu-id="64b6c-250">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="64b6c-250">The following example shows the response.</span></span> 

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
       {
           "id": "C0BD1BA1-A84E-4796-9C65-F8A0293741D1",
           "displayName": "Irene McGowan",
           "givenName": "Irene",
           "surname": "McGowan",
           "birthday": "",
           "personNotes": "",
           "isFavorite": false,
           "jobTitle": "Auditor",
           "companyName": null,
           "yomiCompany": "",
           "department": "Finance",
           "officeLocation": "12/1110",
           "profession": "",
           "userPrincipalName": "irenem@contoso.onmicrosoft.com",
           "imAddress": "sip:irenem@contoso.onmicrosoft.com",
           "scoredEmailAddresses": [
               {
                   "address": "irenem@contoso.onmicrosoft.com",
                   "relevanceScore": -16.446060612802224
               }
           ],
           "phones": [
               {
                   "type": "Business",
                   "number": "+1 412 555 0109"
               }
           ],
           "postalAddresses": [],
           "websites": [],
           "personType": {
               "class": "Person",
               "subclass": "OrganizationUser"
           }
       }
   ]
}
```

<span data-ttu-id="64b6c-251">Para más información sobre la API de contactos, vea [Obtener información sobre contactos relevantes](./people_example.md#search-people).</span><span class="sxs-lookup"><span data-stu-id="64b6c-251">To learn more about the People API, see [Get information about relevant people](./people_example.md#search-people).</span></span>  

## <a name="select-parameter"></a><span data-ttu-id="64b6c-252">parámetro de selección</span><span class="sxs-lookup"><span data-stu-id="64b6c-252">select parameter</span></span>

<span data-ttu-id="64b6c-253">Use el parámetro de consulta `$select` para devolver un conjunto de propiedades diferente al predeterminado para un recurso individual o una colección de recursos.</span><span class="sxs-lookup"><span data-stu-id="64b6c-253">Use the `$select` query parameter to return a set of properties that are different than the default set for an individual resource or a collection of resources.</span></span> <span data-ttu-id="64b6c-254">Con $select, puede especificar un subconjunto o un superconjunto de las propiedades predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="64b6c-254">With $select, you can specify a subset or a superset of the default properties.</span></span>

<span data-ttu-id="64b6c-255">Por ejemplo, al recuperar los mensajes del usuario que ha iniciado sesión, puede especificar que solo se devuelvan las propiedades **from** y **subject**:</span><span class="sxs-lookup"><span data-stu-id="64b6c-255">For example, when retrieving the messages of the signed-in user, you can specify that only the **from** and **subject** properties be returned:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/messages?$select=from,subject
```

<span data-ttu-id="64b6c-256">[Probar en el Probador de Graph][select-example]</span><span class="sxs-lookup"><span data-stu-id="64b6c-256">[Try in Graph Explorer][select-example]</span></span>

> <span data-ttu-id="64b6c-257">**Importante:** En general, se recomienda usar `$select` para limitar las propiedades devueltas por una consulta a las necesarias para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="64b6c-257">**Important:** In general, we recommend that you use `$select` to limit the properties returned by a query to those needed by your app.</span></span> <span data-ttu-id="64b6c-258">Esto es especialmente cierto para las consultas que potencialmente pueden devolver un conjunto de resultados grande.</span><span class="sxs-lookup"><span data-stu-id="64b6c-258">This is especially true of queries that might potentially return a large result set.</span></span> <span data-ttu-id="64b6c-259">Limitar las propiedades devueltas en cada fila reducirá la carga en la red y ayudará a mejorar el rendimiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="64b6c-259">Limiting the properties returned in each row will reduce network load and help improve your app's performance.</span></span>
>
> <span data-ttu-id="64b6c-p124">En `v1.0`, algunos recursos de Azure AD que se derivan de [directoryObject](../api-reference/v1.0/resources/directoryobject.md), como [user](../api-reference/v1.0/resources/user.md) y [group](../api-reference/v1.0/resources/group.md), devuelven un subconjunto predeterminado limitado de propiedades en las operaciones de lectura. Para estos recursos, debe usar `$select` para devolver propiedades fuera el conjunto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="64b6c-p124">In `v1.0`, some Azure AD resources that derive from [directoryObject](../api-reference/v1.0/resources/directoryobject.md), like [user](../api-reference/v1.0/resources/user.md) and [group](../api-reference/v1.0/resources/group.md), return a limited, default subset of properties on reads. For these resources, you must use `$select` to return properties outside of the default set.</span></span>  

## <a name="skip-parameter"></a><span data-ttu-id="64b6c-262">parámetros de omisión</span><span class="sxs-lookup"><span data-stu-id="64b6c-262">skip parameter</span></span>

<span data-ttu-id="64b6c-p125">Use el parámetro de consulta `$skip` para establecer el número de elementos que se omitirán al inicio de una colección. Por ejemplo, la solicitud siguiente devuelve eventos para el usuario ordenados por fecha de creación, empezando por el evento 21 de la colección:</span><span class="sxs-lookup"><span data-stu-id="64b6c-p125">Use the `$skip` query parameter to set the number of items to skip at the start of a collection. For example, the following request returns events for the user sorted by date created, starting with the 21st event in the collection:</span></span>

```http
GET  https://graph.microsoft.com/v1.0/me/events?$orderby=createdDateTime&$skip=20
```
<span data-ttu-id="64b6c-265">[Probar en el Probador de Graph][skip-example]</span><span class="sxs-lookup"><span data-stu-id="64b6c-265">[Try in Graph Explorer][skip-example]</span></span>

> <span data-ttu-id="64b6c-266">**Nota:** En algunas API de Microsoft Graph, como Correo y Calendario de Outlook (**message**, **event** y **calendar**), se usa `$skip` para implementar la paginación.</span><span class="sxs-lookup"><span data-stu-id="64b6c-266">**Note:** Some Microsoft Graph APIs, like Outlook Mail and Calendars (**message**, **event**, and **calendar**), use `$skip` to implement paging.</span></span> <span data-ttu-id="64b6c-267">Cuando los resultados de una consulta ocupen varias páginas, estas API devolverán una propiedad `@odata:nextLink` con una dirección URL que contendrá un parámetro `$skip`.</span><span class="sxs-lookup"><span data-stu-id="64b6c-267">When results of a query span multiple pages, these APIs will return an `@odata:nextLink` property with a URL that contains a `$skip` parameter.</span></span> <span data-ttu-id="64b6c-268">Puede usar esta dirección URL para devolver la siguiente página de resultados.</span><span class="sxs-lookup"><span data-stu-id="64b6c-268">You can use this URL to return the next page of results.</span></span> <span data-ttu-id="64b6c-269">Para obtener más información, vea [Paginación](./paging.md).</span><span class="sxs-lookup"><span data-stu-id="64b6c-269">To learn more, see [Paging](./paging.md).</span></span>

## <a name="skiptoken-parameter"></a><span data-ttu-id="64b6c-270">parámetro skipToken</span><span class="sxs-lookup"><span data-stu-id="64b6c-270">skipToken parameter</span></span>

<span data-ttu-id="64b6c-p127">Algunas consultas devuelven varias páginas de datos debido a la paginación del servidor o al uso del parámetro [`$top`](#top-parameter) para limitar el tamaño de página de la respuesta. Muchas API de Microsoft Graph usan el parámetro de consulta `skipToken` para hacer referencia a las páginas siguientes del resultado. El parámetro `$skiptoken` contiene un token opaco que hace referencia a la siguiente página de resultados y se devuelve en la dirección URL proporcionada en la propiedad `@odata.nextLink` en la respuesta. Para obtener más información, vea [Paginación](./paging.md).</span><span class="sxs-lookup"><span data-stu-id="64b6c-p127">Some requests return multiple pages of data either due to server-side paging or due to the use of the [`$top`](#top-parameter) parameter to limit the page size of the response. Many Microsoft Graph APIs use the `skipToken` query parameter to reference subsequent pages of the result. The `$skiptoken` parameter contains an opaque token that references the next page of results and is returned in the URL provided in the `@odata.nextLink` property in the response. To learn more, see [Paging](./paging.md).</span></span>


## <a name="top-parameter"></a><span data-ttu-id="64b6c-275">parámetro superior</span><span class="sxs-lookup"><span data-stu-id="64b6c-275">top parameter</span></span>

<span data-ttu-id="64b6c-276">Use el parámetro de consulta `$top` para especificar el tamaño de página del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="64b6c-276">Use the `$top` query parameter to specify the page size of the result set.</span></span> 

<span data-ttu-id="64b6c-277">Si quedan más elementos en el conjunto de resultados, el cuerpo de la respuesta contendrá un parámetro `@odata.nextLink`.</span><span class="sxs-lookup"><span data-stu-id="64b6c-277">If more items remain in the result set, the response body will contain an `@odata.nextLink` parameter.</span></span> <span data-ttu-id="64b6c-278">Este parámetro contiene una dirección URL que se puede usar para obtener la siguiente página de resultados.</span><span class="sxs-lookup"><span data-stu-id="64b6c-278">This parameter contains a URL that you can use to get the next page of results.</span></span> <span data-ttu-id="64b6c-279">Para obtener más información, vea [Paginación](./paging.md).</span><span class="sxs-lookup"><span data-stu-id="64b6c-279">To learn more, see [Paging](./paging.md).</span></span> 

<span data-ttu-id="64b6c-280">Por ejemplo, la solicitud siguiente devuelve los cinco primeros mensajes en el buzón del usuario:</span><span class="sxs-lookup"><span data-stu-id="64b6c-280">For example, the following request returns the first five messages in the user's mailbox:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/messages?$top=5
```

<span data-ttu-id="64b6c-281">[Probar en el Probador de Graph][top-example]</span><span class="sxs-lookup"><span data-stu-id="64b6c-281">[Try in Graph Explorer][top-example]</span></span>


## <a name="error-handling-for-query-parameters"></a><span data-ttu-id="64b6c-282">Control de errores para parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="64b6c-282">Error handling for query parameters</span></span>

<span data-ttu-id="64b6c-p129">Algunas solicitudes devolverán un mensaje de error si no se admite un parámetro de consulta especificado. Por ejemplo, no se puede usar `$expand` en la relación `user/photo`.</span><span class="sxs-lookup"><span data-stu-id="64b6c-p129">Some requests will return an error message if a specified query parameter is not supported. For example, you cannot use `$expand` on the `user/photo` relationship.</span></span> 

```http
https://graph.microsoft.com/beta/me?$expand=photo
```

```json
{
    "error":{
        "code":"ExpandNotSupported",
        "message":"Expand is not allowed for property 'Photo' according to the entity schema.",
        "innerError":{
            "request-id":"1653fefd-bc31-484b-bb10-8dc33cb853ec",
            "date":"2017-07-31T20:55:01"
        }
    }
}
```

<span data-ttu-id="64b6c-285">Pero es importante tener en cuenta que los parámetros de consulta especificados en una solicitud pueden devolver un error silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="64b6c-285">However, it is important to note that query parameters specified in a request might fail silently.</span></span> <span data-ttu-id="64b6c-286">Esto puede suceder con parámetros de consulta no admitidos, así como con combinaciones no compatibles de parámetros de consulta.</span><span class="sxs-lookup"><span data-stu-id="64b6c-286">This can be true for unsupported query parameters as well as for unsupported combinations of query parameters.</span></span> <span data-ttu-id="64b6c-287">En estos casos, debe examinar los datos devueltos por la solicitud para determinar si los parámetros de consulta especificados tuvieron el efecto previsto.</span><span class="sxs-lookup"><span data-stu-id="64b6c-287">In these cases, you should examine the data returned by the request to determine whether the query parameters you specified had the desired effect.</span></span> 

[graph-explorer]: https://developer.microsoft.com/graph/graph-explorer
[odata-filter]: http://docs.oasis-open.org/odata/odata/v4.0/errata03/os/complete/part2-url-conventions/odata-v4.0-errata03-os-part2-url-conventions-complete.html#_Toc453752358
[odata-query]: http://docs.oasis-open.org/odata/odata/v4.0/errata03/os/complete/part2-url-conventions/odata-v4.0-errata03-os-part2-url-conventions-complete.html#_Toc453752356
[count-example]: https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$top=2%26$count=true&method=GET&version=v1.0
[expand-example]: https://developer.microsoft.com/graph/graph-explorer?request=groups$expand=members&method=GET&version=v1.0
[filter-example]: https://developer.microsoft.com/graph/graph-explorer?request=users?$filter=startswith(givenName,'J')&method=GET&version=v1.0
[format-example]: https://developer.microsoft.com/graph/graph-explorer?request=users?$format=json&method=GET&version=v1.0
[orderby-example]: https://developer.microsoft.com/graph/graph-explorer?request=users?$orderby=displayName%20DESC&method=GET&version=v1.0
[search-example]: https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$search=pizza&method=GET&version=v1.0
[select-example]: https://developer.microsoft.com/graph/graph-explorer?request=users?$select=givenName,surname&method=GET&version=v1.0
[skip-example]: https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$skip=11&method=GET&version=v1.0
[top-example]: https://developer.microsoft.com/graph/graph-explorer?request=users?$top=2&method=GET&version=v1.0


