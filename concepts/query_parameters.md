# <a name="use-query-parameters-to-customize-responses"></a><span data-ttu-id="810a1-101">Usar parámetros de consulta para personalizar respuestas</span><span class="sxs-lookup"><span data-stu-id="810a1-101">Use query parameters to customize responses</span></span>

<span data-ttu-id="810a1-p101">Microsoft Graph proporciona parámetros de consulta opcionales que puede usar para especificar y controlar la cantidad de datos devueltos en una respuesta. Se admiten los siguientes parámetros de consulta.</span><span class="sxs-lookup"><span data-stu-id="810a1-p101">Microsoft Graph provides optional query parameters that you can use to specify and control the amount of data returned in a response. The following query parameters are supported.</span></span>

><span data-ttu-id="810a1-104">**Nota:** Haga clic en los ejemplos para probarlos en [Probador de Graph][graph-explorer].</span><span class="sxs-lookup"><span data-stu-id="810a1-104">**Note:** Click the examples to try them in [Graph Explorer][graph-explorer].</span></span>

| <span data-ttu-id="810a1-105">Nombre</span><span class="sxs-lookup"><span data-stu-id="810a1-105">Name</span></span>                     | <span data-ttu-id="810a1-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="810a1-106">Description</span></span> | <span data-ttu-id="810a1-107">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="810a1-107">Example</span></span>
|:-------------------------|:------------|:---------|
| [<span data-ttu-id="810a1-108">$count</span><span class="sxs-lookup"><span data-stu-id="810a1-108">$count</span></span>](#count-parameter)         | <span data-ttu-id="810a1-109">Recupera el número total de recursos coincidentes.</span><span class="sxs-lookup"><span data-stu-id="810a1-109">Retrieves the total count of matching resources.</span></span> | [`/me/messages?$top=2&$count=true`][count-example]
| [<span data-ttu-id="810a1-110">$expand</span><span class="sxs-lookup"><span data-stu-id="810a1-110">$expand</span></span>](#expand-parameter)       | <span data-ttu-id="810a1-111">Recupera los recursos relacionados.</span><span class="sxs-lookup"><span data-stu-id="810a1-111">Retrieves related resources.</span></span>|[`/groups?$expand=members`][expand-example]
| [<span data-ttu-id="810a1-112">$filter</span><span class="sxs-lookup"><span data-stu-id="810a1-112">$filter</span></span>](#filter-parameter)       | <span data-ttu-id="810a1-113">Filtra los resultados (filas).</span><span class="sxs-lookup"><span data-stu-id="810a1-113">Filters results (rows).</span></span>|[`/users?$filter=startswith(givenName,'J')`][filter-example]
| [<span data-ttu-id="810a1-114">$format</span><span class="sxs-lookup"><span data-stu-id="810a1-114">$format</span></span>](#format-parameter)       | <span data-ttu-id="810a1-115">Devuelve los resultados en el formato de medio especificado.</span><span class="sxs-lookup"><span data-stu-id="810a1-115">Returns the results in the specified media format.</span></span>|[`/users?$format=json`][format-example]
| [<span data-ttu-id="810a1-116">$orderby</span><span class="sxs-lookup"><span data-stu-id="810a1-116">$orderby</span></span>](#orderby-parameter)     | <span data-ttu-id="810a1-117">Ordena los resultados.</span><span class="sxs-lookup"><span data-stu-id="810a1-117">Orders results.</span></span>|[`/users?$orderby=displayName desc`][orderby-example]
| [<span data-ttu-id="810a1-118">$search</span><span class="sxs-lookup"><span data-stu-id="810a1-118">$search</span></span>](#search-parameter)       | <span data-ttu-id="810a1-p102">Devuelve los resultados en función de los criterios de búsqueda. Actualmente, se admite en las colecciones de **mensajes** y **usuarios**.</span><span class="sxs-lookup"><span data-stu-id="810a1-p102">Returns results based on search criteria. Currently supported on **messages** and **person** collections.</span></span>|[`/me/messages?$search=pizza`][search-example]
| [<span data-ttu-id="810a1-121">$select</span><span class="sxs-lookup"><span data-stu-id="810a1-121">$select</span></span>](#select-parameter)       | <span data-ttu-id="810a1-122">Filtra las propiedades (columnas).</span><span class="sxs-lookup"><span data-stu-id="810a1-122">Filters properties (columns).</span></span>|[`/users?$select=givenName,surname`][select-example]
| [<span data-ttu-id="810a1-123">$skip</span><span class="sxs-lookup"><span data-stu-id="810a1-123">$skip</span></span>](#skip-parameter)           | <span data-ttu-id="810a1-p103">Indexa en un conjunto de resultados. También se usa en algunas API para implementar la paginación y se puede usar junto a `$top` para paginar manualmente los resultados.</span><span class="sxs-lookup"><span data-stu-id="810a1-p103">Indexes into a result set. Also used by some APIs to implement paging and can be used together with `$top` to manually page results.</span></span> | [`/me/messages?$skip=11`][skip-example]
| [<span data-ttu-id="810a1-126">$skipToken</span><span class="sxs-lookup"><span data-stu-id="810a1-126">$skipToken</span></span>](#skiptoken-parameter) | <span data-ttu-id="810a1-p104">Recupera la siguiente página de resultados de conjuntos de resultados que abarcan varias páginas. (Algunas API usan `$skip` en su lugar).</span><span class="sxs-lookup"><span data-stu-id="810a1-p104">Retrieves the next page of results from result sets that span multiple pages. (Some APIs use `$skip` instead.)</span></span> | `/users?$skiptoken=X%274453707402000100000017...`|
| [<span data-ttu-id="810a1-129">$top</span><span class="sxs-lookup"><span data-stu-id="810a1-129">$top</span></span>](#top-parameter)             | <span data-ttu-id="810a1-130">Establece el tamaño de la página de resultados.</span><span class="sxs-lookup"><span data-stu-id="810a1-130">Sets the page size of results.</span></span> |[`/users?$top=2`][top-example]



<span data-ttu-id="810a1-131">Estos parámetros son compatibles con el [lenguaje de consulta de OData V4][odata-query].</span><span class="sxs-lookup"><span data-stu-id="810a1-131">These parameters are compatible with the [OData V4 query language][odata-query].</span></span> <span data-ttu-id="810a1-132">No todos los parámetros se admiten en todas las API de Microsoft Graph, y la compatibilidad puede variar considerablemente entre los puntos de conexión `v1.0` y `beta`.</span><span class="sxs-lookup"><span data-stu-id="810a1-132">Not all parameters are supported across all Microsoft Graph APIs, and support might differ significantly between the `v1.0` and `beta` endpoints.</span></span> 

> <span data-ttu-id="810a1-p106">**Nota:** En el punto de conexión `beta`, el prefijo `$` es opcional. Por ejemplo, en lugar de `$filter`, puede usar `filter`. Para obtener más detalles y ejemplos, vea [Compatibilidad con los parámetros de consulta sin el prefijo "$" en Microsoft Graph](http://dev.office.com/queryparametersinMicrosoftGraph).</span><span class="sxs-lookup"><span data-stu-id="810a1-p106">**Note:** On the `beta` endpoint, the `$` prefix is optional. For example, instead of `$filter`, you can use `filter`. For more details and examples, see [Supporting query parameters without $ prefixes in Microsoft Graph](http://dev.office.com/queryparametersinMicrosoftGraph).</span></span>

## <a name="encoding-query-parameters"></a><span data-ttu-id="810a1-136">Codificación de parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="810a1-136">Encoding query parameters</span></span>

<span data-ttu-id="810a1-137">Los valores de los parámetros de consulta deben ser codificados por porcentaje.</span><span class="sxs-lookup"><span data-stu-id="810a1-137">The values of query parameters should be percent-encoded.</span></span> <span data-ttu-id="810a1-138">Muchos clientes HTTP, exploradores y herramientas (como el [Probador de Graph][graph-explorer]) le servirán de ayuda.</span><span class="sxs-lookup"><span data-stu-id="810a1-138">Many HTTP clients, browsers, and tools (such as the [Graph Explorer][graph-explorer]) will help you with this.</span></span> <span data-ttu-id="810a1-139">Si una consulta produce un error, puede deberse a que los valores de los parámetros de consulta no se han codificado correctamente.</span><span class="sxs-lookup"><span data-stu-id="810a1-139">If a query is failing, one possible cause is failure to encode the query parameter values appropriately.</span></span>

<span data-ttu-id="810a1-140">Una dirección URL sin codificar tiene el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="810a1-140">An unencoded URL looks like this:</span></span>

```http
GET https://graph.microsoft.com/v1.0/users?$filter=startswith(givenName, 'J')
```

<span data-ttu-id="810a1-141">Una dirección URL codificada correctamente tiene el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="810a1-141">A properly encoded URL looks like this:</span></span>

```http
GET https://graph.microsoft.com/v1.0/users?$filter=startswith(givenName%2C+'J')
```

## <a name="count-parameter"></a><span data-ttu-id="810a1-142">parámetro de recuento</span><span class="sxs-lookup"><span data-stu-id="810a1-142">count parameter</span></span>

<span data-ttu-id="810a1-143">Use el parámetro de consulta `$count` para incluir un recuento del número total de elementos de una colección junto con la página de valores de datos que se devuelve desde Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="810a1-143">Use the `$count` query parameter to include a count of the total number of items in a collection alongside the page of data values returned from Microsoft Graph.</span></span> 

<span data-ttu-id="810a1-144">Por ejemplo, la siguiente solicitud devolverá tanto la colección de **contactos** del usuario actual como el número de elementos de la colección de **contactos** en la propiedad `@odata.count`.</span><span class="sxs-lookup"><span data-stu-id="810a1-144">For example, the following request will return both the **contact** collection of the current user, and the number of items in the **contact** collection in the `@odata.count` property.</span></span>

```http
GET  https://graph.microsoft.com/v1.0/me/contacts?$count=true
```

[<span data-ttu-id="810a1-145">Probar en el Probador de Graph</span><span class="sxs-lookup"><span data-stu-id="810a1-145">Try in Graph Explorer</span></span>](https://developer.microsoft.com/graph/graph-explorer?request=me/contacts?$count=true&method=GET&version=v1.0)


><span data-ttu-id="810a1-146">**Nota:** `$count` no se admite con colecciones de recursos que se derivan de [directoryObject](../api-reference/v1.0/resources/directoryobject.md), como las colecciones de [usuarios](../api-reference/v1.0/resources/user.md) o [grupos](../api-reference/v1.0/resources/group.md).</span><span class="sxs-lookup"><span data-stu-id="810a1-146">**Note:** `$count` is not supported for collections of resources that derive from [directoryObject](../api-reference/v1.0/resources/directoryobject.md) like collections of [users](../api-reference/v1.0/resources/user.md) or [groups](../api-reference/v1.0/resources/group.md).</span></span>

## <a name="expand-parameter"></a><span data-ttu-id="810a1-147">parámetro de expansión</span><span class="sxs-lookup"><span data-stu-id="810a1-147">expand parameter</span></span>

<span data-ttu-id="810a1-148">Muchos de los recursos de Microsoft Graph exponen ambas propiedades declaradas de los recursos, así como sus relaciones con otros recursos.</span><span class="sxs-lookup"><span data-stu-id="810a1-148">Many Microsoft Graph resources expose both declared properties of the resource as well as its relationships with other resources.</span></span> <span data-ttu-id="810a1-149">Estas relaciones también se denominan propiedades de referencia o propiedades de navegación, y pueden hacer referencia a un único recurso o a una colección de recursos.</span><span class="sxs-lookup"><span data-stu-id="810a1-149">These relationships are also called reference properties or navigation properties, and they can reference either a single resource or a collection of resources.</span></span> <span data-ttu-id="810a1-150">Por ejemplo, las carpetas de correo, el administrador y los informes directos de un usuario se exponen como relaciones.</span><span class="sxs-lookup"><span data-stu-id="810a1-150">For example, the mail folders, manager, and direct reports of a user are all exposed as relationships.</span></span> 

<span data-ttu-id="810a1-p109">Normalmente, se pueden consultar las propiedades de un recurso o una de sus relaciones en una sola solicitud, pero no ambas. Puede usar el parámetro de cadena de consulta `$expand` para incluir en los resultados de la consulta el recurso expandido o la colección a la que se hace referencia con una única relación (propiedad de navegación).</span><span class="sxs-lookup"><span data-stu-id="810a1-p109">Normally, you can query either the properties of a resource or one of its relationships in a single request, but not both. You can use the `$expand` query string parameter to include the expanded resource or collection referenced by a single relationship (navigation property) in your results.</span></span>

<span data-ttu-id="810a1-153">En el ejemplo siguiente se obtiene la información de la unidad raíz junto con los elementos secundarios de nivel superior de una unidad:</span><span class="sxs-lookup"><span data-stu-id="810a1-153">The following example gets root drive information along with the top-level child items in a drive:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/drive/root?$expand=children
```

[<span data-ttu-id="810a1-154">Probar en el Probador de Graph</span><span class="sxs-lookup"><span data-stu-id="810a1-154">Try in Graph Explorer</span></span>](https://developer.microsoft.com/graph/graph-explorer?request=me/drive/root?$expand=children&method=GET&version=v1.0)

<span data-ttu-id="810a1-p110">Con algunas colecciones de recursos, también se pueden especificar las propiedades que se van a devolver en los recursos expandidos si se agrega un parámetro `$select`. En el ejemplo siguiente se realiza la misma consulta que en el anterior, pero se usa una instrucción [`$select`](#select-parameter) para limitar las propiedades devueltas para los elementos secundarios expandidos a las propiedades **id** y **name**.</span><span class="sxs-lookup"><span data-stu-id="810a1-p110">With some resource collections, you can also specify the properties to be returned in the expanded resources by adding a `$select` parameter. The following example performs the same query as the previous example but uses a [`$select`](#select-parameter) statement to limit the properties returned for the expanded child items to the **id** and **name** properties.</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/drive/root?$expand=children($select=id,name)
```

<span data-ttu-id="810a1-157">[Probar en el Probador de Graph][expand-example]</span><span class="sxs-lookup"><span data-stu-id="810a1-157">[Try in Graph Explorer][expand-example]</span></span>

> <span data-ttu-id="810a1-p111">**Nota:** No todas las relaciones y recursos admiten el parámetro de consulta `$expand`. Por ejemplo, se pueden expandir las relaciones **directReports**, **manager** y **memberOf** de un usuario, pero no se pueden expandir sus relaciones **events**, **messages** o **photo**. No todos los recursos o relaciones admiten el uso de `$select` en elementos expandidos.</span><span class="sxs-lookup"><span data-stu-id="810a1-p111">**Note:** Not all relationships and resources support the `$expand` query parameter. For example, you can expand the **directReports**, **manager**, and **memberOf** relationships on a user, but you cannot expand its **events**, **messages**, or **photo** relationships. Not all resources or relationships support using `$select` on expanded items.</span></span> 
> 
> <span data-ttu-id="810a1-161">Con recursos de Azure AD que se derivan de [directoryObject](../api-reference/v1.0/resources/directoryobject.md), como [user](../api-reference/v1.0/resources/user.md) y [group](../api-reference/v1.0/resources/group.md), solo se admite `$expand` para `beta` y normalmente devuelve un máximo de 20 elementos para la relación expandida.</span><span class="sxs-lookup"><span data-stu-id="810a1-161">With Azure AD resources that derive from [directoryObject](../api-reference/v1.0/resources/directoryobject.md), like [user](../api-reference/v1.0/resources/user.md) and [group](../api-reference/v1.0/resources/group.md), `$expand` is only supported for `beta` and  typically returns a maximum of 20 items for the expanded relationship.</span></span>

## <a name="filter-parameter"></a><span data-ttu-id="810a1-162">parámetro de filtrado</span><span class="sxs-lookup"><span data-stu-id="810a1-162">filter parameter</span></span>

<span data-ttu-id="810a1-163">Use el parámetro de consulta `$filter` para recuperar solo un subconjunto de una colección.</span><span class="sxs-lookup"><span data-stu-id="810a1-163">Use the `$filter` query parameter to retrieve just a subset of a collection.</span></span> 

<span data-ttu-id="810a1-164">Por ejemplo, para buscar usuarios cuyos nombres para mostrar comiencen por la letra "J", use `startswith`.</span><span class="sxs-lookup"><span data-stu-id="810a1-164">For example, to find users whose display name starts with the letter 'J', use `startswith`.</span></span>

```http
GET https://graph.microsoft.com/v1.0/users?$filter=startswith(displayName,'J')
```

<span data-ttu-id="810a1-165">[Probar en el Probador de Graph][filter-example]</span><span class="sxs-lookup"><span data-stu-id="810a1-165">[Try in Graph Explorer][filter-example]</span></span>

<span data-ttu-id="810a1-166">La compatibilidad con los operadores `$filter` varía en función de la API de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="810a1-166">Support for `$filter` operators varies across Microsoft Graph APIs.</span></span> <span data-ttu-id="810a1-167">Generalmente, se admiten los siguientes operadores lógicos:</span><span class="sxs-lookup"><span data-stu-id="810a1-167">The following logical operators are generally supported:</span></span> 

- <span data-ttu-id="810a1-168">igual a (`eq`)</span><span class="sxs-lookup"><span data-stu-id="810a1-168">equals (`eq`)</span></span>
- <span data-ttu-id="810a1-169">no es igual a (`ne`)</span><span class="sxs-lookup"><span data-stu-id="810a1-169">not equals (`ne`)</span></span>
- <span data-ttu-id="810a1-170">mayor que (`gt`)</span><span class="sxs-lookup"><span data-stu-id="810a1-170">greater than (`gt`)</span></span>
- <span data-ttu-id="810a1-171">mayor o igual que (`ge`)</span><span class="sxs-lookup"><span data-stu-id="810a1-171">greater than or equals (`ge`)</span></span>
- <span data-ttu-id="810a1-172">menor que (`lt`), menor o igual que (`le`)</span><span class="sxs-lookup"><span data-stu-id="810a1-172">less than (`lt`), less than or equals (`le`)</span></span>
- <span data-ttu-id="810a1-173">y (`and`)</span><span class="sxs-lookup"><span data-stu-id="810a1-173">and (`and`)</span></span>
- <span data-ttu-id="810a1-174">o (`or`)</span><span class="sxs-lookup"><span data-stu-id="810a1-174">or (`or`)</span></span>
- <span data-ttu-id="810a1-175">no (`not`)</span><span class="sxs-lookup"><span data-stu-id="810a1-175">not (`not`)</span></span>
 
<span data-ttu-id="810a1-176">El operador de cadena `startswith` se suele admitir.</span><span class="sxs-lookup"><span data-stu-id="810a1-176">The `startswith` string operator is often supported.</span></span> <span data-ttu-id="810a1-177">El operador lambda `any` se admite con algunas API.</span><span class="sxs-lookup"><span data-stu-id="810a1-177">The `any` lambda operator is supported for some APIs.</span></span> <span data-ttu-id="810a1-178">Para obtener algunos ejemplos de uso, vea la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="810a1-178">For some  usage examples, see the following table.</span></span> <span data-ttu-id="810a1-179">Para obtener detalles adicionales sobre la sintaxis de `$filter`, vea el [protocolo OData][odata-filter].</span><span class="sxs-lookup"><span data-stu-id="810a1-179">For more details about `$filter` syntax, see the [OData protocol][odata-filter].</span></span>  

<span data-ttu-id="810a1-180">En la tabla siguiente se muestran algunos ejemplos de uso del parámetro de consulta `$filter`.</span><span class="sxs-lookup"><span data-stu-id="810a1-180">The following table shows some examples that use the `$filter` query parameter.</span></span>

> <span data-ttu-id="810a1-181">**Nota:** Haga clic en los ejemplos para probarlos en [Probador de Graph][graph-explorer].</span><span class="sxs-lookup"><span data-stu-id="810a1-181">**Note:** Click the examples to try them in [Graph Explorer][graph-explorer].</span></span>

| <span data-ttu-id="810a1-182">Descripción</span><span class="sxs-lookup"><span data-stu-id="810a1-182">Description</span></span> | <span data-ttu-id="810a1-183">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="810a1-183">Example</span></span>
|:------------|:--------|
| <span data-ttu-id="810a1-184">Buscar usuarios con el nombre Mary en varias propiedades.</span><span class="sxs-lookup"><span data-stu-id="810a1-184">Search for users with the name Mary across multiple properties.</span></span> | [`https://graph.microsoft.com/v1.0/users?$filter=startswith(displayName,'mary') or startswith(givenName,'mary') or startswith(surname,'mary') or startswith(mail,'mary') or startswith(userPrincipalName,'mary')`](https://developer.microsoft.com/graph/graph-explorer?request=users?$filter=startswith(displayName,'mary')+or+startswith(givenName,'mary')+or+startswith(surname,'mary')+or+startswith(mail,'mary')+or+startswith(userPrincipalName,'mary')&method=GET&version=v1.0) 
| <span data-ttu-id="810a1-185">Obtener todos los eventos del usuario que inició sesión que comiencen después del 1/7/2017.</span><span class="sxs-lookup"><span data-stu-id="810a1-185">Get all the signed-in user's events that start after 7/1/2017.</span></span> | [`https://graph.microsoft.com/v1.0/me/events?$filter=start/dateTime ge '2017-07-01T08:00'`](https://developer.microsoft.com/graph/graph-explorer?request=me/events?$filter=start/dateTime+ge+'2017-07-01T08:00'&method=GET&version=v1.0) 
| <span data-ttu-id="810a1-186">Obtener todos los correos electrónicos de una dirección específica recibidos por el usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="810a1-186">Get all emails from a specific address received by the signed-in user.</span></span> | [`https://graph.microsoft.com/v1.0/me/messages?$filter=from/emailAddress/address eq 'someuser@example.com'`](https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$filter=from/emailAddress/address+eq+'someuser@.com'&method=GET&version=v1.0) 
| <span data-ttu-id="810a1-187">Obtener todos los correos electrónicos recibidos en abril de 2017 por el usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="810a1-187">Get all emails received by the signed-in user in April 2017.</span></span> | [`https://graph.microsoft.com/v1.0/me/mailFolders/inbox/messages?$filter=ReceivedDateTime ge 2017-04-01 and receivedDateTime lt 2017-05-01`](https://developer.microsoft.com/graph/graph-explorer?request=me/mailFolders/inbox/messages?$filter=ReceivedDateTime+ge+2017-04-01+and+receivedDateTime+lt+2017-05-01&method=GET&version=v1.0) 
| <span data-ttu-id="810a1-188">Obtener todos los correos electrónicos no leídos en la Bandeja de entrada del usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="810a1-188">Get all unread mail in the signed-in user's Inbox.</span></span> | [`https://graph.microsoft.com/v1.0/me/mailFolders/inbox/messages?$filter=isRead eq false`](https://developer.microsoft.com/graph/graph-explorer?request=me/mailFolders/inbox/messages?$filter=isRead+eq+false&method=GET&version=v1.0) 
| <span data-ttu-id="810a1-189">Enumerar todos los grupos de Office 365 de una organización.</span><span class="sxs-lookup"><span data-stu-id="810a1-189">List all Office 365 groups in an organization.</span></span> | [`https://graph.microsoft.com/v1.0/groups?$filter=groupTypes/any(c:c+eq+'Unified')`](https://developer.microsoft.com/graph/graph-explorer?request=groups?$filter=groupTypes/any(c:c+eq+'Unified')&method=GET&version=v1.0) 

> <span data-ttu-id="810a1-p114">**Nota:** Los operadores `$filter` siguientes no se admiten para recursos de Azure AD: `ne`, `gt`, `ge`, `lt`, `le` y `not`. El operador de cadena `contains` actualmente no se admite en ningún recurso de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="810a1-p114">**Note:** The following `$filter` operators are not supported for Azure AD resources:  `ne`, `gt`, `ge`, `lt`, `le`, and `not`. The `contains` string operator is currently not supported on any Microsoft Graph resources.</span></span>

## <a name="format-parameter"></a><span data-ttu-id="810a1-192">parámetro de formato</span><span class="sxs-lookup"><span data-stu-id="810a1-192">format parameter</span></span>

<span data-ttu-id="810a1-193">Use el parámetro de consulta `$format` para especificar el formato de medio de los elementos devueltos desde Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="810a1-193">Use the `$format` query parameter to specify the media format of the items returned from Microsoft Graph.</span></span>

<span data-ttu-id="810a1-194">Por ejemplo, la solicitud siguiente devuelve los usuarios de la organización en formato JSON:</span><span class="sxs-lookup"><span data-stu-id="810a1-194">For example, the following request returns the users in the organization in the json format:</span></span>

```http
GET https://graph.microsoft.com/v1.0/users?$format=json
```

<span data-ttu-id="810a1-195">[Probar en el Probador de Graph][format-example]</span><span class="sxs-lookup"><span data-stu-id="810a1-195">[Try in Graph Explorer][format-example]</span></span>

> <span data-ttu-id="810a1-196">**Nota**: El parámetro de consulta `$format` admite varios formatos, como atom, xml y json, pero puede que no todos los formatos devuelvan resultados.</span><span class="sxs-lookup"><span data-stu-id="810a1-196">**Note:** The `$format` query parameter supports a number of formats (for example, atom, xml, and json) but results may not be returned in all formats.</span></span>

## <a name="orderby-parameter"></a><span data-ttu-id="810a1-197">parámetro orderby</span><span class="sxs-lookup"><span data-stu-id="810a1-197">orderby parameter</span></span>

<span data-ttu-id="810a1-198">Use el parámetro de consulta `$orderby` para especificar el criterio de ordenación de los elementos devueltos desde Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="810a1-198">Use the `$orderby` query parameter to specify the sort order of the items returned from Microsoft Graph.</span></span>

<span data-ttu-id="810a1-199">Por ejemplo, la solicitud siguiente devuelve los usuarios de la organización ordenados por su nombre para mostrar:</span><span class="sxs-lookup"><span data-stu-id="810a1-199">For example, the following request returns the users in the organization ordered by their display name:</span></span>

```http
GET https://graph.microsoft.com/v1.0/users?$orderby=displayName
```
<span data-ttu-id="810a1-200">[Probar en el Probador de Graph][orderby-example]</span><span class="sxs-lookup"><span data-stu-id="810a1-200">[Try in Graph Explorer][orderby-example]</span></span>

<span data-ttu-id="810a1-p115">También puede ordenar por entidades de tipo complejo. La solicitud siguiente obtiene los mensajes y los ordena por el campo **address** de la propiedad **from**, que es del tipo complejo **emailAddress**:</span><span class="sxs-lookup"><span data-stu-id="810a1-p115">You can also sort by complex type entities. The following request gets messages and sorts them by the **address** field of the **from** property, which is of the complex type **emailAddress**:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/messages?$orderby=from/emailAddress/address
```
[<span data-ttu-id="810a1-203">Probar en el Probador de Graph</span><span class="sxs-lookup"><span data-stu-id="810a1-203">Try in Graph Explorer</span></span>](https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$orderby=from/emailAddress/address&method=GET&version=v1.0)

<span data-ttu-id="810a1-204">Para ordenar los resultados en orden ascendente o descendente, anexe `asc` o `desc` al nombre del campo, separado por un espacio. Por ejemplo, `?$orderby=name%20desc`.</span><span class="sxs-lookup"><span data-stu-id="810a1-204">To sort the results in ascending or descending order, append either `asc` or `desc` to the field name, separated by a space; for example, `?$orderby=name%20desc`.</span></span>

<span data-ttu-id="810a1-205">Con algunas API se pueden ordenar los resultados por varias propiedades.</span><span class="sxs-lookup"><span data-stu-id="810a1-205">With some APIs, you can order results on multiple properties.</span></span> <span data-ttu-id="810a1-206">Por ejemplo, en la siguiente solicitud se ordenan los mensajes en la Bandeja de entrada del usuario; primero por el nombre de la persona que lo envió en orden descendente (de la Z a la A) y, después, por asunto en orden ascendente (el valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="810a1-206">For example, the following request orders the messages in the user's Inbox, first by the name of the person who sent it in descending order (Z to A), and then by subject in ascending order (default).</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/mailFolders/Inbox/messages?$orderby=from/emailAddress/name desc,subject
```

[<span data-ttu-id="810a1-207">Probar en el Probador de Graph</span><span class="sxs-lookup"><span data-stu-id="810a1-207">Try in Graph Explorer</span></span>](https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$orderby=from/emailAddress/name%20desc,subject&method=GET&version=v1.0)

<span data-ttu-id="810a1-208">Si especifica $filter, el servidor deducirá un criterio de ordenación para los resultados.</span><span class="sxs-lookup"><span data-stu-id="810a1-208">When you specify $filter the server will infer a sort order for the results.</span></span> <span data-ttu-id="810a1-209">Si usa tanto `$orderby` como `$filter`, porque el servidor siempre deduce un criterio de ordenación para los resultados de un `$filter`, las propiedades del `$filter` deben estar primero en `$orderby`, antes que cualquier otra propiedad y deben estar en el orden en el que aparecen en el parámetro `$filter`.</span><span class="sxs-lookup"><span data-stu-id="810a1-209">If you use both `$orderby` and `$filter`, because the server always infers a sort order for the results of a `$filter`, the properties in the `$filter` must be listed first in the `$orderby` before any other properties, and they must be listed in the order that they appear in the `$filter` parameter.</span></span> 

<span data-ttu-id="810a1-210">En el siguiente ejemplo, se muestra una consulta filtrada por las propiedades **subject** y **importance**, y después ordenada por las propiedades **subject**, **importance** y **receivedDateTime** en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="810a1-210">The following example shows a query filtered by the **subject** and **importance** properties, and then sorted by the **subject**, **importance**, and **receivedDateTime** properties in descending order.</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/messages?$filter=Subject eq 'welcome' and importance eq 'normal'&$orderby=subject,importance,receivedDateTime desc
```

[<span data-ttu-id="810a1-211">Probar en el Probador de Graph</span><span class="sxs-lookup"><span data-stu-id="810a1-211">Try in Graph Explorer</span></span>](https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$filter=subject%20eq%20%27welcome%27%20and%20importance%20eq%20%27normal%27%20&$orderby=subject,importance,receivedDateTime%20desc&method=GET&version=v1.0)

 > <span data-ttu-id="810a1-212">**Nota:** Con recursos de Azure AD que se derivan de [directoryObject](../api-reference/v1.0/resources/directoryobject.md), como [user](../api-reference/v1.0/resources/user.md) y [group](../api-reference/v1.0/resources/group.md), no se puede combinar `$orderby` con expresiones`$filter`.</span><span class="sxs-lookup"><span data-stu-id="810a1-212">**Note:** With Azure AD resources that derive from [directoryObject](../api-reference/v1.0/resources/directoryobject.md), like [user](../api-reference/v1.0/resources/user.md) and [group](../api-reference/v1.0/resources/group.md), you cannot combine `$orderby` with `$filter` expressions.</span></span> 

## <a name="search-parameter"></a><span data-ttu-id="810a1-213">parámetro de búsqueda</span><span class="sxs-lookup"><span data-stu-id="810a1-213">search parameter</span></span>

<span data-ttu-id="810a1-214">Use el parámetro de consulta `$search` para restringir los resultados de una solicitud para que coincidan con un criterio de búsqueda</span><span class="sxs-lookup"><span data-stu-id="810a1-214">Use the `$search` query parameter to restrict the results of a request to match a search criterion.</span></span>

> <span data-ttu-id="810a1-p118">**Nota:** Actualmente **solo** se pueden buscar las colecciones [message](../api-reference/v1.0/resources/message.md) y [person](../api-reference/v1.0/resources/person.md). Una solicitud `$search` devuelve hasta 250 resultados. No puede usar [`$filter`](#filter-parameter) o [`$orderby`](#orderby-parameter) en una solicitud de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="810a1-p118">**Note:** You can currently search **only** [message](../api-reference/v1.0/resources/message.md) and [person](../api-reference/v1.0/resources/person.md) collections. A `$search` request returns up to 250 results. You cannot use [`$filter`](#filter-parameter) or [`$orderby`](#orderby-parameter) in a search request.</span></span>

### <a name="using-search-on-message-collections"></a><span data-ttu-id="810a1-218">Uso de $search en colecciones de mensajes</span><span class="sxs-lookup"><span data-stu-id="810a1-218">Using $search on message collections</span></span>

<span data-ttu-id="810a1-219">Puede buscar mensajes con un valor en las propiedades de los mensajes específicos.</span><span class="sxs-lookup"><span data-stu-id="810a1-219">You can search messages based on a value in specific message properties.</span></span> <span data-ttu-id="810a1-220">Los resultados de la búsqueda se ordenan por la fecha y la hora en que se ha enviado el mensaje.</span><span class="sxs-lookup"><span data-stu-id="810a1-220">The results of a search on a message collection are sorted by the date and time that the message was sent.</span></span>

<span data-ttu-id="810a1-221">Si realiza una búsqueda en mensajes y especifica solo un valor sin las propiedades de mensaje específicas, la búsqueda se lleva a cabo con las propiedades de búsqueda predeterminadas de **from**, **subject** y **body**.</span><span class="sxs-lookup"><span data-stu-id="810a1-221">If you do a search on messages and specify only a value, the search is carried out on the default search properties of **from**, **subject**, and **body**.</span></span>

<span data-ttu-id="810a1-222">En el ejemplo siguiente, se devuelven todos los mensajes del buzón del usuario que ha iniciado sesión que contienen la palabra "pizza" en cualquiera de las tres propiedades de búsqueda predeterminadas:</span><span class="sxs-lookup"><span data-stu-id="810a1-222">The following example returns all messages in the signed-in user's Inbox that contains "pizza" in any of the three default search properties:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/messages?$search="pizza"
```

<span data-ttu-id="810a1-223">[Probar en el Probador de Graph][search-example]</span><span class="sxs-lookup"><span data-stu-id="810a1-223">[Try in Graph Explorer][search-example]</span></span>

<span data-ttu-id="810a1-224">Como alternativa, puede buscar mensajes especificando los nombres de propiedades de mensaje en la tabla siguiente, que se reconocen por la sintaxis de la consulta de palabras clave (KQL).</span><span class="sxs-lookup"><span data-stu-id="810a1-224">Alternatively, you can search messages by specifying message property names in the following table, that are recognized by the Keyword Query Language (KQL) syntax.</span></span> <span data-ttu-id="810a1-225">Estos nombres de propiedad corresponden a las propiedades que se definen en la entidad de **mensaje** de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="810a1-225">These property names correspond to properties defined in the **message** entity of Microsoft Graph.</span></span> <span data-ttu-id="810a1-226">Outlook y otras aplicaciones de Office 365, como SharePoint admiten la sintaxis KQL, proporciona la comodidad de un dominio de detección común para los almacenes de datos.</span><span class="sxs-lookup"><span data-stu-id="810a1-226">Outlook and other Office 365 applications such as SharePoint support KQL syntax, providing the convenience of a common discovery domain for their data stores.</span></span>


| <span data-ttu-id="810a1-227">Propiedades del correo electrónico que permiten búsquedas</span><span class="sxs-lookup"><span data-stu-id="810a1-227">Searchable email property</span></span>                | <span data-ttu-id="810a1-228">Descripción</span><span class="sxs-lookup"><span data-stu-id="810a1-228">Description</span></span> | <span data-ttu-id="810a1-229">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="810a1-229">Example</span></span> 
|:-------------------------|:------------|:---------|
| <span data-ttu-id="810a1-230">**attachment**</span><span class="sxs-lookup"><span data-stu-id="810a1-230">**attachment**</span></span>           | <span data-ttu-id="810a1-231">Los nombres de los archivos adjuntos a un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="810a1-231">The names of files attached to an email message.</span></span>|[`me/messages?$search="attachment:api-catalog.md"`][search-att-example]
| <span data-ttu-id="810a1-232">**bcc**</span><span class="sxs-lookup"><span data-stu-id="810a1-232">**bcc**</span></span>           | <span data-ttu-id="810a1-233">El campo **bcc** de un mensaje de correo electrónico, especificado como una dirección SMTP, alias o nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="810a1-233">The **bcc** field of an email message, specified as an SMTP address, display name, or alias.</span></span>|[`me/messages?$search="bcc:samanthab@contoso.com"&$select=subject,bccRecipients`][search-bcc-example]
| <span data-ttu-id="810a1-234">**body**</span><span class="sxs-lookup"><span data-stu-id="810a1-234">**body**</span></span>           | <span data-ttu-id="810a1-235">El cuerpo de un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="810a1-235">The body of an email message.</span></span>|[`me/messages?$search="body:excitement"`][search-body-example]
| <span data-ttu-id="810a1-236">**cc**</span><span class="sxs-lookup"><span data-stu-id="810a1-236">**cc**</span></span>           | <span data-ttu-id="810a1-237">El campo **cc** de un mensaje de correo electrónico, especificado como una dirección SMTP, alias o nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="810a1-237">The **cc** field of an email message, specified as an SMTP address, display name, or alias.</span></span>|[`me/messages?$search="cc:danas"&$select=subject,ccRecipients`][search-cc-example]
| <span data-ttu-id="810a1-238">**from**</span><span class="sxs-lookup"><span data-stu-id="810a1-238">**from**</span></span>           | <span data-ttu-id="810a1-239">El remitente de un mensaje de correo electrónico, especificado como una dirección SMTP, alias o nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="810a1-239">The sender of an email message, specified as an SMTP address, display name, or alias.</span></span>|[`me/messages?$search="from:randiw"&$select=subject,from`][search-from-example]
| <span data-ttu-id="810a1-240">**hasAttachment**</span><span class="sxs-lookup"><span data-stu-id="810a1-240">**HasAttachment**</span></span> | <span data-ttu-id="810a1-241">Verdadero si un mensaje contiene datos adjuntos que no son un archivo adjunto en línea, falso en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="810a1-241">True if an email message contains an attachment that is not an inline attachment, false otherwise.</span></span> |[`me/messages?$search="hasAttachments=true"`][search-from-example]
| <span data-ttu-id="810a1-242">**importance**</span><span class="sxs-lookup"><span data-stu-id="810a1-242">**importance**</span></span>           | <span data-ttu-id="810a1-243">La importancia de un mensaje de correo electrónico, que un remitente puede especificar al enviar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="810a1-243">The importance of an email message, which a sender can specify when sending a message.</span></span> <span data-ttu-id="810a1-244">Los valores posibles son`low`, `medium` o `high`.</span><span class="sxs-lookup"><span data-stu-id="810a1-244">The possible values are `low`, `medium`, or `high`.</span></span>|[`me/messages?$search="importance:high"&$select=subject,importance`][search-imp-example]
| <span data-ttu-id="810a1-245">**kind**</span><span class="sxs-lookup"><span data-stu-id="810a1-245">**Kind**</span></span>           | <span data-ttu-id="810a1-246">El tipo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="810a1-246">The type of message box.</span></span> <span data-ttu-id="810a1-247">Los valores posibles son `contacts`, `docs`, `email`, `faxes`, `im`, `journals`, `meetings`, `notes`, `posts`, `rssfeeds`, `tasks` o `voicemail`.</span><span class="sxs-lookup"><span data-stu-id="810a1-247">The possible values are `contacts`, `docs`, `email`, `faxes`, `im`, `journals`, `meetings`, `notes`, `posts`, `rssfeeds`, `tasks`, or `voicemail`.</span></span>|[`me/messages?$search="kind:voicemail"`][search-kind-example]
| <span data-ttu-id="810a1-248">**participants**</span><span class="sxs-lookup"><span data-stu-id="810a1-248">**participants**</span></span>           | <span data-ttu-id="810a1-249">Los campos **from**, **to**, **cc** y **bcc** de un mensaje de correo electrónico, especificados como una dirección SMTP, alias o nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="810a1-249">The **from**, **to**, **cc**, and **bcc** fields of an email message, specified as an SMTP address, display name, or alias.</span></span>|[`me/messages?$search="participants:danas"`][search-part-example]
| <span data-ttu-id="810a1-250">**received**</span><span class="sxs-lookup"><span data-stu-id="810a1-250">**received**</span></span>           | <span data-ttu-id="810a1-251">La fecha en la que un destinatario recibió un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="810a1-251">The date that an email message was received by a recipient.</span></span>|[`me/messages?$search="received:07/23/2018"&$select=subject,receivedDateTime`][search-rcvd-example]
| <span data-ttu-id="810a1-252">**recipients**</span><span class="sxs-lookup"><span data-stu-id="810a1-252">**recipients**</span></span>           | <span data-ttu-id="810a1-253">Los campos**to**, **cc** y **bcc** especificados como una dirección SMTP, alias o nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="810a1-253">The **to**, **cc**, and **bcc** fields of an email meesage, specified as an SMTP address, display name, or alias.</span></span>|[`me/messages?$search="recipients:randiq"&$select=subject,toRecipients,ccRecipients,bccRecipients`][search-rcpts-example]
| <span data-ttu-id="810a1-254">**sent**</span><span class="sxs-lookup"><span data-stu-id="810a1-254">**Sent**</span></span>           | <span data-ttu-id="810a1-255">La fecha en la que un remitente envió un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="810a1-255">The date that an email message was sent by the sender.</span></span>|[`me/messages?$search="sent:07/23/2018"&$select=subject,sentDateTime`][search-sent-example]
| <span data-ttu-id="810a1-256">**size**</span><span class="sxs-lookup"><span data-stu-id="810a1-256">**size**</span></span>           | <span data-ttu-id="810a1-257">El tamaño de un elemento, en bytes.</span><span class="sxs-lookup"><span data-stu-id="810a1-257">The size of an item in bytes.</span></span>|[`me/messages?$search="size:1..500000"`][search-size-example]
| <span data-ttu-id="810a1-258">**subject**</span><span class="sxs-lookup"><span data-stu-id="810a1-258">**subject**</span></span>           | <span data-ttu-id="810a1-259">El texto en la línea de asunto de un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="810a1-259">The text in the subject line of an email message.</span></span> <span data-ttu-id="810a1-260">.</span><span class="sxs-lookup"><span data-stu-id="810a1-260"></span></span>|[`me/messages?$search="subject:has"&$select=subject`][search-sbj-example]
| <span data-ttu-id="810a1-261">**to**</span><span class="sxs-lookup"><span data-stu-id="810a1-261">**to**</span></span>           | <span data-ttu-id="810a1-262">El campo **to** de un mensaje de correo electrónico, especificado como una dirección SMTP, alias o nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="810a1-262">The **to** field of an email message, specified as an SMTP address, display name, or alias.</span></span>|[`me/messages?$search="to:randiw"&$select=subject,toRecipients`][search-to-example]


<span data-ttu-id="810a1-263">Para obtener más información sobre las propiedades de correo electrónico que permiten búsquedas, la sintaxis KQL, los operadores compatibles y las sugerencias de búsqueda, vea los artículos siguientes:</span><span class="sxs-lookup"><span data-stu-id="810a1-263">For more information about KQL such as the syntax, supported operators, and tips on searching, see the following articles:</span></span>

- <span data-ttu-id="810a1-264">[Propiedades que permiten búsquedas en Exchange](https://docs.microsoft.com/es-ES/Exchange/policy-and-compliance/ediscovery/message-properties-and-search-operators#searchable-properties-in-exchange).</span><span class="sxs-lookup"><span data-stu-id="810a1-264">[Searchable properties in Exchange](https://docs.microsoft.com/es-ES/Exchange/policy-and-compliance/ediscovery/message-properties-and-search-operators#searchable-properties-in-exchange).</span></span>

- [<span data-ttu-id="810a1-265">Referencia de la sintaxis del lenguaje de consultas de palabras clave (KQL)</span><span class="sxs-lookup"><span data-stu-id="810a1-265">Keyword Query Language (KQL) syntax reference</span></span>](https://docs.microsoft.com/es-ES/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference)

- <span data-ttu-id="810a1-266">
  [Propiedades de mensajes y operadores de búsqueda para eDiscovery local en Exchange 2016](https://technet.microsoft.com/en-us/library/dn774955(v=exchg.160).aspx)</span><span class="sxs-lookup"><span data-stu-id="810a1-266">[Message properties and search operators for In-Place eDiscovery in Exchange 2016](https://technet.microsoft.com/en-us/library/dn774955(v=exchg.160).aspx)</span></span>

### <a name="using-search-on-person-collections"></a><span data-ttu-id="810a1-267">Uso de $search en colecciones de usuarios</span><span class="sxs-lookup"><span data-stu-id="810a1-267">Using $search on person collections</span></span>

<span data-ttu-id="810a1-p124">Puede usar la API de contactos de Microsoft Graph para recuperar los contactos más relevantes para un usuario. La relevancia viene determinada por las relaciones empresariales y los patrones de comunicación y colaboración del usuario. La API de contactos admite el parámetro de consulta `$search`.</span><span class="sxs-lookup"><span data-stu-id="810a1-p124">You can use the Microsoft Graph People API to retrieve the people who are most relevant to a user. Relevance is determined by the user’s communication and collaboration patterns and business relationships. The People API supports the `$search` query parameter.</span></span>

<span data-ttu-id="810a1-271">Las búsquedas de contactos se realizan en las propiedades **displayName** y **emailAddress** del recurso [person](../api-reference/v1.0/resources/person.md).</span><span class="sxs-lookup"><span data-stu-id="810a1-271">Searches on people occur on both the **displayName** and **emailAddress** properties of the [person](../api-reference/v1.0/resources/person.md) resource.</span></span>

<span data-ttu-id="810a1-272">La solicitud siguiente busca una persona llamada "Irene McGowen" en las propiedades **displayName** y **emailAddress** de todos los miembros de la colección **people** del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="810a1-272">The following request does a search for a person named "Irene McGowen" in the **displayName** and **emailAddress** properties in each person in the **people** collection of the signed-in user.</span></span> <span data-ttu-id="810a1-273">Dado que existe una persona llamada "Irene McGowan" relevante para el usuario que ha iniciado sesión, se devuelve la información de "Irene McGowan".</span><span class="sxs-lookup"><span data-stu-id="810a1-273">Because a person named "Irene McGowan" is relevant to the signed-in user, the information for "Irene McGowan" is returned.</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/people/?$search="Irene McGowen"
```

<span data-ttu-id="810a1-274">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="810a1-274">The following example shows the response.</span></span> 

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

<span data-ttu-id="810a1-275">Para más información sobre la API de contactos, vea [Obtener información sobre contactos relevantes](./people_example.md#search-people).</span><span class="sxs-lookup"><span data-stu-id="810a1-275">To learn more about the People API, see [Get information about relevant people](./people_example.md#search-people).</span></span>  

## <a name="select-parameter"></a><span data-ttu-id="810a1-276">parámetro de selección</span><span class="sxs-lookup"><span data-stu-id="810a1-276">select parameter</span></span>

<span data-ttu-id="810a1-277">Use el parámetro de consulta `$select` para devolver un conjunto de propiedades diferente al predeterminado para un recurso individual o una colección de recursos.</span><span class="sxs-lookup"><span data-stu-id="810a1-277">Use the `$select` query parameter to return a set of properties that are different than the default set for an individual resource or a collection of resources.</span></span> <span data-ttu-id="810a1-278">Con $select, puede especificar un subconjunto o un superconjunto de las propiedades predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="810a1-278">With $select, you can specify a subset or a superset of the default properties.</span></span>

<span data-ttu-id="810a1-279">Por ejemplo, al recuperar los mensajes del usuario que ha iniciado sesión, puede especificar que solo se devuelvan las propiedades **from** y **subject**:</span><span class="sxs-lookup"><span data-stu-id="810a1-279">For example, when retrieving the messages of the signed-in user, you can specify that only the **from** and **subject** properties be returned:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/messages?$select=from,subject
```

<span data-ttu-id="810a1-280">[Probar en el Probador de Graph][select-example]</span><span class="sxs-lookup"><span data-stu-id="810a1-280">[Try in Graph Explorer][select-example]</span></span>

> <span data-ttu-id="810a1-281">**Importante:** En general, se recomienda usar `$select` para limitar las propiedades devueltas por una consulta a las necesarias para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="810a1-281">**Important:** In general, we recommend that you use `$select` to limit the properties returned by a query to those needed by your app.</span></span> <span data-ttu-id="810a1-282">Esto es especialmente cierto para las consultas que potencialmente pueden devolver un conjunto de resultados grande.</span><span class="sxs-lookup"><span data-stu-id="810a1-282">This is especially true of queries that might potentially return a large result set.</span></span> <span data-ttu-id="810a1-283">Limitar las propiedades devueltas en cada fila reducirá la carga en la red y ayudará a mejorar el rendimiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="810a1-283">Limiting the properties returned in each row will reduce network load and help improve your app's performance.</span></span>
>
> <span data-ttu-id="810a1-p128">En `v1.0`, algunos recursos de Azure AD que se derivan de [directoryObject](../api-reference/v1.0/resources/directoryobject.md), como [user](../api-reference/v1.0/resources/user.md) y [group](../api-reference/v1.0/resources/group.md), devuelven un subconjunto predeterminado limitado de propiedades en las operaciones de lectura. Para estos recursos, debe usar `$select` para devolver propiedades fuera el conjunto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="810a1-p128">In `v1.0`, some Azure AD resources that derive from [directoryObject](../api-reference/v1.0/resources/directoryobject.md), like [user](../api-reference/v1.0/resources/user.md) and [group](../api-reference/v1.0/resources/group.md), return a limited, default subset of properties on reads. For these resources, you must use `$select` to return properties outside of the default set.</span></span>  

## <a name="skip-parameter"></a><span data-ttu-id="810a1-286">parámetros de omisión</span><span class="sxs-lookup"><span data-stu-id="810a1-286">skip parameter</span></span>

<span data-ttu-id="810a1-p129">Use el parámetro de consulta `$skip` para establecer el número de elementos que se omitirán al inicio de una colección. Por ejemplo, la solicitud siguiente devuelve eventos para el usuario ordenados por fecha de creación, empezando por el evento 21 de la colección:</span><span class="sxs-lookup"><span data-stu-id="810a1-p129">Use the `$skip` query parameter to set the number of items to skip at the start of a collection. For example, the following request returns events for the user sorted by date created, starting with the 21st event in the collection:</span></span>

```http
GET  https://graph.microsoft.com/v1.0/me/events?$orderby=createdDateTime&$skip=20
```
<span data-ttu-id="810a1-289">[Probar en el Probador de Graph][skip-example]</span><span class="sxs-lookup"><span data-stu-id="810a1-289">[Try in Graph Explorer][skip-example]</span></span>

> <span data-ttu-id="810a1-290">**Nota:** En algunas API de Microsoft Graph, como Correo y Calendario de Outlook (**message**, **event** y **calendar**), se usa `$skip` para implementar la paginación.</span><span class="sxs-lookup"><span data-stu-id="810a1-290">**Note:** Some Microsoft Graph APIs, like Outlook Mail and Calendars (**message**, **event**, and **calendar**), use `$skip` to implement paging.</span></span> <span data-ttu-id="810a1-291">Cuando los resultados de una consulta ocupen varias páginas, estas API devolverán una propiedad `@odata:nextLink` con una dirección URL que contendrá un parámetro `$skip`.</span><span class="sxs-lookup"><span data-stu-id="810a1-291">When results of a query span multiple pages, these APIs will return an `@odata:nextLink` property with a URL that contains a `$skip` parameter.</span></span> <span data-ttu-id="810a1-292">Puede usar esta dirección URL para devolver la siguiente página de resultados.</span><span class="sxs-lookup"><span data-stu-id="810a1-292">You can use this URL to return the next page of results.</span></span> <span data-ttu-id="810a1-293">Para obtener más información, vea [Paginación](./paging.md).</span><span class="sxs-lookup"><span data-stu-id="810a1-293">To learn more, see [Paging](./paging.md).</span></span>

## <a name="skiptoken-parameter"></a><span data-ttu-id="810a1-294">parámetro skipToken</span><span class="sxs-lookup"><span data-stu-id="810a1-294">skipToken parameter</span></span>

<span data-ttu-id="810a1-p131">Algunas consultas devuelven varias páginas de datos debido a la paginación del servidor o al uso del parámetro [`$top`](#top-parameter) para limitar el tamaño de página de la respuesta. Muchas API de Microsoft Graph usan el parámetro de consulta `skipToken` para hacer referencia a las páginas siguientes del resultado. El parámetro `$skiptoken` contiene un token opaco que hace referencia a la siguiente página de resultados y se devuelve en la dirección URL proporcionada en la propiedad `@odata.nextLink` en la respuesta. Para obtener más información, vea [Paginación](./paging.md).</span><span class="sxs-lookup"><span data-stu-id="810a1-p131">Some requests return multiple pages of data either due to server-side paging or due to the use of the [`$top`](#top-parameter) parameter to limit the page size of the response. Many Microsoft Graph APIs use the `skipToken` query parameter to reference subsequent pages of the result. The `$skiptoken` parameter contains an opaque token that references the next page of results and is returned in the URL provided in the `@odata.nextLink` property in the response. To learn more, see [Paging](./paging.md).</span></span>


## <a name="top-parameter"></a><span data-ttu-id="810a1-299">parámetro superior</span><span class="sxs-lookup"><span data-stu-id="810a1-299">top parameter</span></span>

<span data-ttu-id="810a1-300">Use el parámetro de consulta `$top` para especificar el tamaño de página del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="810a1-300">Use the `$top` query parameter to specify the page size of the result set.</span></span> 

<span data-ttu-id="810a1-301">Si quedan más elementos en el conjunto de resultados, el cuerpo de la respuesta contendrá un parámetro `@odata.nextLink`.</span><span class="sxs-lookup"><span data-stu-id="810a1-301">If more items remain in the result set, the response body will contain an `@odata.nextLink` parameter.</span></span> <span data-ttu-id="810a1-302">Este parámetro contiene una dirección URL que se puede usar para obtener la siguiente página de resultados.</span><span class="sxs-lookup"><span data-stu-id="810a1-302">This parameter contains a URL that you can use to get the next page of results.</span></span> <span data-ttu-id="810a1-303">Para obtener más información, vea [Paginación](./paging.md).</span><span class="sxs-lookup"><span data-stu-id="810a1-303">To learn more, see [Paging](./paging.md).</span></span> 

<span data-ttu-id="810a1-304">Por ejemplo, la solicitud siguiente devuelve los cinco primeros mensajes en el buzón del usuario:</span><span class="sxs-lookup"><span data-stu-id="810a1-304">For example, the following request returns the first five messages in the user's mailbox:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/messages?$top=5
```

<span data-ttu-id="810a1-305">[Probar en el Probador de Graph][top-example]</span><span class="sxs-lookup"><span data-stu-id="810a1-305">[Try in Graph Explorer][top-example]</span></span>


## <a name="error-handling-for-query-parameters"></a><span data-ttu-id="810a1-306">Control de errores para parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="810a1-306">Error handling for query parameters</span></span>

<span data-ttu-id="810a1-p133">Algunas solicitudes devolverán un mensaje de error si no se admite un parámetro de consulta especificado. Por ejemplo, no se puede usar `$expand` en la relación `user/photo`.</span><span class="sxs-lookup"><span data-stu-id="810a1-p133">Some requests will return an error message if a specified query parameter is not supported. For example, you cannot use `$expand` on the `user/photo` relationship.</span></span> 

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

<span data-ttu-id="810a1-309">Pero es importante tener en cuenta que los parámetros de consulta especificados en una solicitud pueden devolver un error silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="810a1-309">However, it is important to note that query parameters specified in a request might fail silently.</span></span> <span data-ttu-id="810a1-310">Esto puede suceder con parámetros de consulta no admitidos, así como con combinaciones no compatibles de parámetros de consulta.</span><span class="sxs-lookup"><span data-stu-id="810a1-310">This can be true for unsupported query parameters as well as for unsupported combinations of query parameters.</span></span> <span data-ttu-id="810a1-311">En estos casos, debe examinar los datos devueltos por la solicitud para determinar si los parámetros de consulta especificados tuvieron el efecto previsto.</span><span class="sxs-lookup"><span data-stu-id="810a1-311">In these cases, you should examine the data returned by the request to determine whether the query parameters you specified had the desired effect.</span></span> 

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

[search-att-example]: https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$search=%22attachment%3Aapi-catalog%2Emd%22&method=GET&version=v1.0
[search-bcc-example]: https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$search=%22bcc%3Asamanthab%40contoso%2Ecom%22%26$select=subject,bccRecipients&method=GET&version=v1.0
[search-body-example]: https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$search=%22body%3Aexcitement%22&method=GET&version=v1.0
[search-cc-example]: https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$search=%22cc%3Adanas%22%26$select=subject,ccRecipients&method=GET&version=v1.0
[search-from-example]: https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$search=%22from%3Arandiw%22%26$select=subject,from&method=GET&version=v1.0
[search-hasatt-example]: https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$search=%22hasAttachments=true%22&method=GET&version=v1.0
[search-imp-example]: https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$search=%22importance%3Ahigh%22%26$select=subject,importance&method=GET&version=v1.0
[search-kind-example]: https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$search=%22kind%3Avoicemail%22&method=GET&version=v1.0
[search-part-example]: https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$search=%22participants%3Adanas%22&method=GET&version=v1.0

[search-rcvd-example]: https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$search=%22received%3A07/23/2018%22%26$select=subject,receivedDateTime&method=GET&version=v1.0

[search-rcpts-example]: https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$search=%22recipients%3Arandiw%22%26$select=subject,toRecipients,ccRecipients,bccRecipients&method=GET&version=v1.0
[search-sent-example]: https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$search=%22sent%3A07/23/2018%22%26$select=subject,sentDateTime&method=GET&version=v1.0
[search-size-example]: https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$search=%22size%3A1%2E%2E500000%22&method=GET&version=v1.0

[search-sbj-example]: https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$search=%22subject%3Ahas%22%26$select=subject&method=GET&version=v1.
[search-to-example]: https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$search=%22to%3Arandiw%22%26$select=subject,toRecipients&method=GET&version=v1.0

