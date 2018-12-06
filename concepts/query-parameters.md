---
title: Usar parámetros de consulta para personalizar respuestas
description: Microsoft Graph proporciona parámetros de consulta opcionales que puede usar para especificar y controlar la cantidad de datos devueltos en una respuesta. Se admiten los siguientes parámetros de consulta.
ms.openlocfilehash: e41a6e8d9cc42506985bd82f00bcdc4efaec8add
ms.sourcegitcommit: 2532b8dd7f2533d956e2600855b3daeabdd9b8ff
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/30/2018
ms.locfileid: "27092959"
---
# <a name="use-query-parameters-to-customize-responses"></a><span data-ttu-id="be32e-104">Usar parámetros de consulta para personalizar respuestas</span><span class="sxs-lookup"><span data-stu-id="be32e-104">Use query parameters to customize responses</span></span>

<span data-ttu-id="be32e-p102">Microsoft Graph proporciona parámetros de consulta opcionales que puede usar para especificar y controlar la cantidad de datos devueltos en una respuesta. Se admiten los siguientes parámetros de consulta.</span><span class="sxs-lookup"><span data-stu-id="be32e-p102">Microsoft Graph provides optional query parameters that you can use to specify and control the amount of data returned in a response. The following query parameters are supported.</span></span>

><span data-ttu-id="be32e-107">**Nota:** Haga clic en los ejemplos para probarlos en [Probador de Graph][graph-explorer].</span><span class="sxs-lookup"><span data-stu-id="be32e-107">**Note:** Click the examples to try them in [Graph Explorer][graph-explorer].</span></span>

| <span data-ttu-id="be32e-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="be32e-108">Name</span></span>                     | <span data-ttu-id="be32e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="be32e-109">Description</span></span> | <span data-ttu-id="be32e-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="be32e-110">Example</span></span>
|:-------------------------|:------------|:---------|
| [<span data-ttu-id="be32e-111">$count</span><span class="sxs-lookup"><span data-stu-id="be32e-111">$count</span></span>](#count-parameter)         | <span data-ttu-id="be32e-112">Recupera el número total de recursos coincidentes.</span><span class="sxs-lookup"><span data-stu-id="be32e-112">Retrieves the total count of matching resources.</span></span> | [`/me/messages?$top=2&$count=true`][count-example]
| [<span data-ttu-id="be32e-113">$expand</span><span class="sxs-lookup"><span data-stu-id="be32e-113">$expand</span></span>](#expand-parameter)       | <span data-ttu-id="be32e-114">Recupera los recursos relacionados.</span><span class="sxs-lookup"><span data-stu-id="be32e-114">Retrieves related resources.</span></span>|[`/groups?$expand=members`][expand-example]
| [<span data-ttu-id="be32e-115">$filter</span><span class="sxs-lookup"><span data-stu-id="be32e-115">$filter</span></span>](#filter-parameter)       | <span data-ttu-id="be32e-116">Filtra los resultados (filas).</span><span class="sxs-lookup"><span data-stu-id="be32e-116">Filters results (rows).</span></span>|[`/users?$filter=startswith(givenName,'J')`][filter-example]
| [<span data-ttu-id="be32e-117">$format</span><span class="sxs-lookup"><span data-stu-id="be32e-117">$format</span></span>](#format-parameter)       | <span data-ttu-id="be32e-118">Devuelve los resultados en el formato de medio especificado.</span><span class="sxs-lookup"><span data-stu-id="be32e-118">Returns the results in the specified media format.</span></span>|[`/users?$format=json`][format-example]
| [<span data-ttu-id="be32e-119">$orderby</span><span class="sxs-lookup"><span data-stu-id="be32e-119">$orderby</span></span>](#orderby-parameter)     | <span data-ttu-id="be32e-120">Ordena los resultados.</span><span class="sxs-lookup"><span data-stu-id="be32e-120">Orders results.</span></span>|[`/users?$orderby=displayName desc`][orderby-example]
| [<span data-ttu-id="be32e-121">$search</span><span class="sxs-lookup"><span data-stu-id="be32e-121">$search</span></span>](#search-parameter)       | <span data-ttu-id="be32e-p103">Devuelve los resultados en función de los criterios de búsqueda. Actualmente, se admite en las colecciones de **mensajes** y **usuarios**.</span><span class="sxs-lookup"><span data-stu-id="be32e-p103">Returns results based on search criteria. Currently supported on **messages** and **person** collections.</span></span>|[`/me/messages?$search=pizza`][search-example]
| [<span data-ttu-id="be32e-124">$select</span><span class="sxs-lookup"><span data-stu-id="be32e-124">$select</span></span>](#select-parameter)       | <span data-ttu-id="be32e-125">Filtra las propiedades (columnas).</span><span class="sxs-lookup"><span data-stu-id="be32e-125">Filters properties (columns).</span></span>|[`/users?$select=givenName,surname`][select-example]
| [<span data-ttu-id="be32e-126">$skip</span><span class="sxs-lookup"><span data-stu-id="be32e-126">$skip</span></span>](#skip-parameter)           | <span data-ttu-id="be32e-p104">Indexa en un conjunto de resultados. También se usa en algunas API para implementar la paginación y se puede usar junto a `$top` para paginar manualmente los resultados.</span><span class="sxs-lookup"><span data-stu-id="be32e-p104">Indexes into a result set. Also used by some APIs to implement paging and can be used together with `$top` to manually page results.</span></span> | [`/me/messages?$skip=11`][skip-example]
| [<span data-ttu-id="be32e-129">$skipToken</span><span class="sxs-lookup"><span data-stu-id="be32e-129">$skipToken</span></span>](#skiptoken-parameter) | <span data-ttu-id="be32e-p105">Recupera la siguiente página de resultados de conjuntos de resultados que abarcan varias páginas. (Algunas API usan `$skip` en su lugar).</span><span class="sxs-lookup"><span data-stu-id="be32e-p105">Retrieves the next page of results from result sets that span multiple pages. (Some APIs use `$skip` instead.)</span></span> | `/users?$skiptoken=X%274453707402000100000017...`|
| [<span data-ttu-id="be32e-132">$top</span><span class="sxs-lookup"><span data-stu-id="be32e-132">$top</span></span>](#top-parameter)             | <span data-ttu-id="be32e-133">Establece el tamaño de la página de resultados.</span><span class="sxs-lookup"><span data-stu-id="be32e-133">Sets the page size of results.</span></span> |[`/users?$top=2`][top-example]



<span data-ttu-id="be32e-134">Estos parámetros son compatibles con el [lenguaje de consulta de OData V4][odata-query].</span><span class="sxs-lookup"><span data-stu-id="be32e-134">These parameters are compatible with the [OData V4 query language][odata-query].</span></span> <span data-ttu-id="be32e-135">No todos los parámetros se admiten en todas las API de Microsoft Graph, y la compatibilidad puede variar considerablemente entre los puntos de conexión `v1.0` y `beta`.</span><span class="sxs-lookup"><span data-stu-id="be32e-135">Not all parameters are supported across all Microsoft Graph APIs, and support might differ significantly between the `v1.0` and `beta` endpoints.</span></span> 

> <span data-ttu-id="be32e-136">**Nota:** En los puntos de conexión `beta` y `v1.0`, el prefijo `$` es opcional.</span><span class="sxs-lookup"><span data-stu-id="be32e-136">**Note:** On the `beta` and `v1.0` endpoint, the `$` prefix is optional.</span></span> <span data-ttu-id="be32e-137">Por ejemplo, en lugar de `$filter`, puede usar `filter`.</span><span class="sxs-lookup"><span data-stu-id="be32e-137">For example, instead of writing  `$filter`, you can write  `filter`.</span></span> 

## <a name="encoding-query-parameters"></a><span data-ttu-id="be32e-138">Codificación de parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="be32e-138">Encoding query parameters</span></span>

<span data-ttu-id="be32e-139">Los valores de los parámetros de consulta deben ser codificados por porcentaje.</span><span class="sxs-lookup"><span data-stu-id="be32e-139">The values of query parameters should be percent-encoded.</span></span> <span data-ttu-id="be32e-140">Muchos clientes HTTP, exploradores y herramientas (como el [Probador de Graph][graph-explorer]) le servirán de ayuda.</span><span class="sxs-lookup"><span data-stu-id="be32e-140">Many HTTP clients, browsers, and tools (such as the [Graph Explorer][graph-explorer]) will help you with this.</span></span> <span data-ttu-id="be32e-141">Si una consulta produce un error, puede deberse a que los valores de los parámetros de consulta no se han codificado correctamente.</span><span class="sxs-lookup"><span data-stu-id="be32e-141">If a query is failing, one possible cause is failure to encode the query parameter values appropriately.</span></span>

<span data-ttu-id="be32e-142">Una dirección URL sin codificar tiene el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="be32e-142">An unencoded URL looks like this:</span></span>

```http
GET https://graph.microsoft.com/v1.0/users?$filter=startswith(givenName, 'J')
```

<span data-ttu-id="be32e-143">Una dirección URL codificada correctamente tiene el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="be32e-143">A properly encoded URL looks like this:</span></span>

```http
GET https://graph.microsoft.com/v1.0/users?$filter=startswith(givenName%2C+'J')
```

## <a name="count-parameter"></a><span data-ttu-id="be32e-144">parámetro de recuento</span><span class="sxs-lookup"><span data-stu-id="be32e-144">count parameter</span></span>

<span data-ttu-id="be32e-145">Use el parámetro de consulta `$count` para incluir un recuento del número total de elementos de una colección junto con la página de valores de datos que se devuelve desde Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="be32e-145">Use the `$count` query parameter to include a count of the total number of items in a collection alongside the page of data values returned from Microsoft Graph.</span></span> 

<span data-ttu-id="be32e-146">Por ejemplo, la siguiente solicitud devolverá tanto la colección de **contactos** del usuario actual como el número de elementos de la colección de **contactos** en la propiedad `@odata.count`.</span><span class="sxs-lookup"><span data-stu-id="be32e-146">For example, the following request will return both the **contact** collection of the current user, and the number of items in the **contact** collection in the `@odata.count` property.</span></span>

```http
GET  https://graph.microsoft.com/v1.0/me/contacts?$count=true
```

[<span data-ttu-id="be32e-147">Probar en el Probador de Graph</span><span class="sxs-lookup"><span data-stu-id="be32e-147">Try in Graph Explorer</span></span>](https://developer.microsoft.com/graph/graph-explorer?request=me/contacts?$count=true&method=GET&version=v1.0)


><span data-ttu-id="be32e-148">**Nota:** `$count` no se admite con colecciones de recursos que se derivan de [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-1.0), como las colecciones de [usuarios](/graph/api/resources/user?view=graph-rest-1.0) o [grupos](/graph/api/resources/group?view=graph-rest-1.0).</span><span class="sxs-lookup"><span data-stu-id="be32e-148">**Note:** `$count` is not supported for collections of resources that derive from [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-1.0) like collections of [users](/graph/api/resources/user?view=graph-rest-1.0) or [groups](/graph/api/resources/group?view=graph-rest-1.0).</span></span>

## <a name="expand-parameter"></a><span data-ttu-id="be32e-149">parámetro de expansión</span><span class="sxs-lookup"><span data-stu-id="be32e-149">expand parameter</span></span>

<span data-ttu-id="be32e-150">Muchos de los recursos de Microsoft Graph exponen ambas propiedades declaradas de los recursos, así como sus relaciones con otros recursos.</span><span class="sxs-lookup"><span data-stu-id="be32e-150">Many Microsoft Graph resources expose both declared properties of the resource as well as its relationships with other resources.</span></span> <span data-ttu-id="be32e-151">Estas relaciones también se denominan propiedades de referencia o propiedades de navegación, y pueden hacer referencia a un único recurso o a una colección de recursos.</span><span class="sxs-lookup"><span data-stu-id="be32e-151">These relationships are also called reference properties or navigation properties, and they can reference either a single resource or a collection of resources.</span></span> <span data-ttu-id="be32e-152">Por ejemplo, las carpetas de correo, el administrador y los informes directos de un usuario se exponen como relaciones.</span><span class="sxs-lookup"><span data-stu-id="be32e-152">For example, the mail folders, manager, and direct reports of a user are all exposed as relationships.</span></span> 

<span data-ttu-id="be32e-p110">Normalmente, se pueden consultar las propiedades de un recurso o una de sus relaciones en una sola solicitud, pero no ambas. Puede usar el parámetro de cadena de consulta `$expand` para incluir en los resultados de la consulta el recurso expandido o la colección a la que se hace referencia con una única relación (propiedad de navegación).</span><span class="sxs-lookup"><span data-stu-id="be32e-p110">Normally, you can query either the properties of a resource or one of its relationships in a single request, but not both. You can use the `$expand` query string parameter to include the expanded resource or collection referenced by a single relationship (navigation property) in your results.</span></span>

<span data-ttu-id="be32e-155">En el ejemplo siguiente se obtiene la información de la unidad raíz junto con los elementos secundarios de nivel superior de una unidad:</span><span class="sxs-lookup"><span data-stu-id="be32e-155">The following example gets root drive information along with the top-level child items in a drive:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/drive/root?$expand=children
```

[<span data-ttu-id="be32e-156">Probar en el Probador de Graph</span><span class="sxs-lookup"><span data-stu-id="be32e-156">Try in Graph Explorer</span></span>](https://developer.microsoft.com/graph/graph-explorer?request=me/drive/root?$expand=children&method=GET&version=v1.0)

<span data-ttu-id="be32e-p111">Con algunas colecciones de recursos, también se pueden especificar las propiedades que se van a devolver en los recursos expandidos si se agrega un parámetro `$select`. En el ejemplo siguiente se realiza la misma consulta que en el anterior, pero se usa una instrucción [`$select`](#select-parameter) para limitar las propiedades devueltas para los elementos secundarios expandidos a las propiedades **id** y **name**.</span><span class="sxs-lookup"><span data-stu-id="be32e-p111">With some resource collections, you can also specify the properties to be returned in the expanded resources by adding a `$select` parameter. The following example performs the same query as the previous example but uses a [`$select`](#select-parameter) statement to limit the properties returned for the expanded child items to the **id** and **name** properties.</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/drive/root?$expand=children($select=id,name)
```

<span data-ttu-id="be32e-159">[Probar en el Probador de Graph][expand-example]</span><span class="sxs-lookup"><span data-stu-id="be32e-159">[Try in Graph Explorer][expand-example]</span></span>

> <span data-ttu-id="be32e-p112">**Nota:** No todas las relaciones y recursos admiten el parámetro de consulta `$expand`. Por ejemplo, se pueden expandir las relaciones **directReports**, **manager** y **memberOf** de un usuario, pero no se pueden expandir sus relaciones **events**, **messages** o **photo**. No todos los recursos o relaciones admiten el uso de `$select` en elementos expandidos.</span><span class="sxs-lookup"><span data-stu-id="be32e-p112">**Note:** Not all relationships and resources support the `$expand` query parameter. For example, you can expand the **directReports**, **manager**, and **memberOf** relationships on a user, but you cannot expand its **events**, **messages**, or **photo** relationships. Not all resources or relationships support using `$select` on expanded items.</span></span> 
> 
> <span data-ttu-id="be32e-163">Con recursos de Azure AD que se derivan de [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-1.0), como [user](/graph/api/resources/user?view=graph-rest-1.0) y [group](/graph/api/resources/group?view=graph-rest-1.0), solo se admite `$expand` para `beta` y normalmente devuelve un máximo de 20 elementos para la relación expandida.</span><span class="sxs-lookup"><span data-stu-id="be32e-163">With Azure AD resources that derive from [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-1.0), like [user](/graph/api/resources/user?view=graph-rest-1.0) and [group](/graph/api/resources/group?view=graph-rest-1.0), `$expand` is only supported for `beta` and  typically returns a maximum of 20 items for the expanded relationship.</span></span>

## <a name="filter-parameter"></a><span data-ttu-id="be32e-164">parámetro de filtrado</span><span class="sxs-lookup"><span data-stu-id="be32e-164">filter parameter</span></span>

<span data-ttu-id="be32e-165">Use el parámetro de consulta `$filter` para recuperar solo un subconjunto de una colección.</span><span class="sxs-lookup"><span data-stu-id="be32e-165">Use the `$filter` query parameter to retrieve just a subset of a collection.</span></span> 

<span data-ttu-id="be32e-166">Por ejemplo, para buscar usuarios cuyos nombres para mostrar comiencen por la letra "J", use `startswith`.</span><span class="sxs-lookup"><span data-stu-id="be32e-166">For example, to find users whose display name starts with the letter 'J', use `startswith`.</span></span>

```http
GET https://graph.microsoft.com/v1.0/users?$filter=startswith(displayName,'J')
```

<span data-ttu-id="be32e-167">[Probar en el Probador de Graph][filter-example]</span><span class="sxs-lookup"><span data-stu-id="be32e-167">[Try in Graph Explorer][filter-example]</span></span>

<span data-ttu-id="be32e-168">La compatibilidad con los operadores `$filter` varía en función de la API de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="be32e-168">Support for `$filter` operators varies across Microsoft Graph APIs.</span></span> <span data-ttu-id="be32e-169">Generalmente, se admiten los siguientes operadores lógicos:</span><span class="sxs-lookup"><span data-stu-id="be32e-169">The following logical operators are generally supported:</span></span> 

- <span data-ttu-id="be32e-170">igual a (`eq`)</span><span class="sxs-lookup"><span data-stu-id="be32e-170">equals (`eq`)</span></span>
- <span data-ttu-id="be32e-171">no es igual a (`ne`)</span><span class="sxs-lookup"><span data-stu-id="be32e-171">not equals (`ne`)</span></span>
- <span data-ttu-id="be32e-172">mayor que (`gt`)</span><span class="sxs-lookup"><span data-stu-id="be32e-172">greater than (`gt`)</span></span>
- <span data-ttu-id="be32e-173">mayor o igual que (`ge`)</span><span class="sxs-lookup"><span data-stu-id="be32e-173">greater than or equals (`ge`)</span></span>
- <span data-ttu-id="be32e-174">menor que (`lt`), menor o igual que (`le`)</span><span class="sxs-lookup"><span data-stu-id="be32e-174">less than (`lt`), less than or equals (`le`)</span></span>
- <span data-ttu-id="be32e-175">y (`and`)</span><span class="sxs-lookup"><span data-stu-id="be32e-175">and (`and`)</span></span>
- <span data-ttu-id="be32e-176">o (`or`)</span><span class="sxs-lookup"><span data-stu-id="be32e-176">or (`or`)</span></span>
- <span data-ttu-id="be32e-177">no (`not`)</span><span class="sxs-lookup"><span data-stu-id="be32e-177">not (`not`)</span></span>
 
<span data-ttu-id="be32e-178">El operador de cadena `startswith` se suele admitir.</span><span class="sxs-lookup"><span data-stu-id="be32e-178">The `startswith` string operator is often supported.</span></span> <span data-ttu-id="be32e-179">El operador lambda `any` se admite con algunas API.</span><span class="sxs-lookup"><span data-stu-id="be32e-179">The `any` lambda operator is supported for some APIs.</span></span> <span data-ttu-id="be32e-180">Para obtener algunos ejemplos de uso, vea la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="be32e-180">For some  usage examples, see the following table.</span></span> <span data-ttu-id="be32e-181">Para obtener detalles adicionales sobre la sintaxis de `$filter`, vea el [protocolo OData][odata-filter].</span><span class="sxs-lookup"><span data-stu-id="be32e-181">For more details about `$filter` syntax, see the [OData protocol][odata-filter].</span></span>  

<span data-ttu-id="be32e-182">En la tabla siguiente se muestran algunos ejemplos de uso del parámetro de consulta `$filter`.</span><span class="sxs-lookup"><span data-stu-id="be32e-182">The following table shows some examples that use the `$filter` query parameter.</span></span>

> <span data-ttu-id="be32e-183">**Nota:** Haga clic en los ejemplos para probarlos en [Probador de Graph][graph-explorer].</span><span class="sxs-lookup"><span data-stu-id="be32e-183">**Note:** Click the examples to try them in [Graph Explorer][graph-explorer].</span></span>

| <span data-ttu-id="be32e-184">Descripción</span><span class="sxs-lookup"><span data-stu-id="be32e-184">Description</span></span> | <span data-ttu-id="be32e-185">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="be32e-185">Example</span></span>
|:------------|:--------|
| <span data-ttu-id="be32e-186">Buscar usuarios con el nombre Mary en varias propiedades.</span><span class="sxs-lookup"><span data-stu-id="be32e-186">Search for users with the name Mary across multiple properties.</span></span> | [`https://graph.microsoft.com/v1.0/users?$filter=startswith(displayName,'mary') or startswith(givenName,'mary') or startswith(surname,'mary') or startswith(mail,'mary') or startswith(userPrincipalName,'mary')`](https://developer.microsoft.com/graph/graph-explorer?request=users?$filter=startswith(displayName,'mary')+or+startswith(givenName,'mary')+or+startswith(surname,'mary')+or+startswith(mail,'mary')+or+startswith(userPrincipalName,'mary')&method=GET&version=v1.0) 
| <span data-ttu-id="be32e-187">Obtener todos los eventos del usuario que inició sesión que comiencen después del 1/7/2017.</span><span class="sxs-lookup"><span data-stu-id="be32e-187">Get all the signed-in user's events that start after 7/1/2017.</span></span> | [`https://graph.microsoft.com/v1.0/me/events?$filter=start/dateTime ge '2017-07-01T08:00'`](https://developer.microsoft.com/graph/graph-explorer?request=me/events?$filter=start/dateTime+ge+'2017-07-01T08:00'&method=GET&version=v1.0) 
| <span data-ttu-id="be32e-188">Obtener todos los correos electrónicos de una dirección específica recibidos por el usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="be32e-188">Get all emails from a specific address received by the signed-in user.</span></span> | [`https://graph.microsoft.com/v1.0/me/messages?$filter=from/emailAddress/address eq 'someuser@example.com'`](https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$filter=from/emailAddress/address+eq+'someuser@.com'&method=GET&version=v1.0) 
| <span data-ttu-id="be32e-189">Obtener todos los correos electrónicos recibidos en abril de 2017 por el usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="be32e-189">Get all emails received by the signed-in user in April 2017.</span></span> | [`https://graph.microsoft.com/v1.0/me/mailFolders/inbox/messages?$filter=ReceivedDateTime ge 2017-04-01 and receivedDateTime lt 2017-05-01`](https://developer.microsoft.com/graph/graph-explorer?request=me/mailFolders/inbox/messages?$filter=ReceivedDateTime+ge+2017-04-01+and+receivedDateTime+lt+2017-05-01&method=GET&version=v1.0) 
| <span data-ttu-id="be32e-190">Obtener todos los correos electrónicos no leídos en la Bandeja de entrada del usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="be32e-190">Get all unread mail in the signed-in user's Inbox.</span></span> | [`https://graph.microsoft.com/v1.0/me/mailFolders/inbox/messages?$filter=isRead eq false`](https://developer.microsoft.com/graph/graph-explorer?request=me/mailFolders/inbox/messages?$filter=isRead+eq+false&method=GET&version=v1.0) 
| <span data-ttu-id="be32e-191">Enumerar todos los grupos de Office 365 de una organización.</span><span class="sxs-lookup"><span data-stu-id="be32e-191">List all Office 365 groups in an organization.</span></span> | [`https://graph.microsoft.com/v1.0/groups?$filter=groupTypes/any(c:c+eq+'Unified')`](https://developer.microsoft.com/graph/graph-explorer?request=groups?$filter=groupTypes/any(c:c+eq+'Unified')&method=GET&version=v1.0) 

> <span data-ttu-id="be32e-p115">**Nota:** Los operadores `$filter` siguientes no se admiten para recursos de Azure AD: `ne`, `gt`, `ge`, `lt`, `le` y `not`. El operador de cadena `contains` actualmente no se admite en ningún recurso de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="be32e-p115">**Note:** The following `$filter` operators are not supported for Azure AD resources:  `ne`, `gt`, `ge`, `lt`, `le`, and `not`. The `contains` string operator is currently not supported on any Microsoft Graph resources.</span></span>

## <a name="format-parameter"></a><span data-ttu-id="be32e-194">parámetro de formato</span><span class="sxs-lookup"><span data-stu-id="be32e-194">format parameter</span></span>

<span data-ttu-id="be32e-195">Use el parámetro de consulta `$format` para especificar el formato de medio de los elementos devueltos desde Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="be32e-195">Use the `$format` query parameter to specify the media format of the items returned from Microsoft Graph.</span></span>

<span data-ttu-id="be32e-196">Por ejemplo, la solicitud siguiente devuelve los usuarios de la organización en formato JSON:</span><span class="sxs-lookup"><span data-stu-id="be32e-196">For example, the following request returns the users in the organization in the json format:</span></span>

```http
GET https://graph.microsoft.com/v1.0/users?$format=json
```

<span data-ttu-id="be32e-197">[Probar en el Probador de Graph][format-example]</span><span class="sxs-lookup"><span data-stu-id="be32e-197">[Try in Graph Explorer][format-example]</span></span>

> <span data-ttu-id="be32e-198">**Nota**: El parámetro de consulta `$format` admite varios formatos, como atom, xml y json, pero puede que no todos los formatos devuelvan resultados.</span><span class="sxs-lookup"><span data-stu-id="be32e-198">**Note:** The `$format` query parameter supports a number of formats (for example, atom, xml, and json) but results may not be returned in all formats.</span></span>

## <a name="orderby-parameter"></a><span data-ttu-id="be32e-199">parámetro orderby</span><span class="sxs-lookup"><span data-stu-id="be32e-199">orderby parameter</span></span>

<span data-ttu-id="be32e-200">Use el parámetro de consulta `$orderby` para especificar el criterio de ordenación de los elementos devueltos desde Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="be32e-200">Use the `$orderby` query parameter to specify the sort order of the items returned from Microsoft Graph.</span></span>

<span data-ttu-id="be32e-201">Por ejemplo, la solicitud siguiente devuelve los usuarios de la organización ordenados por su nombre para mostrar:</span><span class="sxs-lookup"><span data-stu-id="be32e-201">For example, the following request returns the users in the organization ordered by their display name:</span></span>

```http
GET https://graph.microsoft.com/v1.0/users?$orderby=displayName
```
<span data-ttu-id="be32e-202">[Probar en el Probador de Graph][orderby-example]</span><span class="sxs-lookup"><span data-stu-id="be32e-202">[Try in Graph Explorer][orderby-example]</span></span>

<span data-ttu-id="be32e-p116">También puede ordenar por entidades de tipo complejo. La solicitud siguiente obtiene los mensajes y los ordena por el campo **address** de la propiedad **from**, que es del tipo complejo **emailAddress**:</span><span class="sxs-lookup"><span data-stu-id="be32e-p116">You can also sort by complex type entities. The following request gets messages and sorts them by the **address** field of the **from** property, which is of the complex type **emailAddress**:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/messages?$orderby=from/emailAddress/address
```
[<span data-ttu-id="be32e-205">Probar en el Probador de Graph</span><span class="sxs-lookup"><span data-stu-id="be32e-205">Try in Graph Explorer</span></span>](https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$orderby=from/emailAddress/address&method=GET&version=v1.0)

<span data-ttu-id="be32e-206">Para ordenar los resultados en orden ascendente o descendente, anexe `asc` o `desc` al nombre del campo, separado por un espacio. Por ejemplo, `?$orderby=name%20desc`.</span><span class="sxs-lookup"><span data-stu-id="be32e-206">To sort the results in ascending or descending order, append either `asc` or `desc` to the field name, separated by a space; for example, `?$orderby=name%20desc`.</span></span>

<span data-ttu-id="be32e-207">Con algunas API se pueden ordenar los resultados por varias propiedades.</span><span class="sxs-lookup"><span data-stu-id="be32e-207">With some APIs, you can order results on multiple properties.</span></span> <span data-ttu-id="be32e-208">Por ejemplo, en la siguiente solicitud se ordenan los mensajes en la Bandeja de entrada del usuario; primero por el nombre de la persona que lo envió en orden descendente (de la Z a la A) y, después, por asunto en orden ascendente (el valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="be32e-208">For example, the following request orders the messages in the user's Inbox, first by the name of the person who sent it in descending order (Z to A), and then by subject in ascending order (default).</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/mailFolders/Inbox/messages?$orderby=from/emailAddress/name desc,subject
```

[<span data-ttu-id="be32e-209">Probar en el Probador de Graph</span><span class="sxs-lookup"><span data-stu-id="be32e-209">Try in Graph Explorer</span></span>](https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$orderby=from/emailAddress/name%20desc,subject&method=GET&version=v1.0)

<span data-ttu-id="be32e-210">Si especifica $filter, el servidor deducirá un criterio de ordenación para los resultados.</span><span class="sxs-lookup"><span data-stu-id="be32e-210">When you specify $filter the server will infer a sort order for the results.</span></span> <span data-ttu-id="be32e-211">Si usa tanto `$orderby` como `$filter`, porque el servidor siempre deduce un criterio de ordenación para los resultados de un `$filter`, las propiedades del `$filter` deben estar primero en `$orderby`, antes que cualquier otra propiedad y deben estar en el orden en el que aparecen en el parámetro `$filter`.</span><span class="sxs-lookup"><span data-stu-id="be32e-211">If you use both `$orderby` and `$filter`, because the server always infers a sort order for the results of a `$filter`, the properties in the `$filter` must be listed first in the `$orderby` before any other properties, and they must be listed in the order that they appear in the `$filter` parameter.</span></span> 

<span data-ttu-id="be32e-212">En el siguiente ejemplo, se muestra una consulta filtrada por las propiedades **subject** y **importance**, y después ordenada por las propiedades **subject**, **importance** y **receivedDateTime** en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="be32e-212">The following example shows a query filtered by the **subject** and **importance** properties, and then sorted by the **subject**, **importance**, and **receivedDateTime** properties in descending order.</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/messages?$filter=Subject eq 'welcome' and importance eq 'normal'&$orderby=subject,importance,receivedDateTime desc
```

[<span data-ttu-id="be32e-213">Probar en el Probador de Graph</span><span class="sxs-lookup"><span data-stu-id="be32e-213">Try in Graph Explorer</span></span>](https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$filter=subject%20eq%20%27welcome%27%20and%20importance%20eq%20%27normal%27%20&$orderby=subject,importance,receivedDateTime%20desc&method=GET&version=v1.0)

 > <span data-ttu-id="be32e-214">**Nota:** Con recursos de Azure AD que se derivan de [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-1.0), como [user](/graph/api/resources/user?view=graph-rest-1.0) y [group](/graph/api/resources/group?view=graph-rest-1.0), no se puede combinar `$orderby` con expresiones`$filter`.</span><span class="sxs-lookup"><span data-stu-id="be32e-214">**Note:** With Azure AD resources that derive from [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-1.0), like [user](/graph/api/resources/user?view=graph-rest-1.0) and [group](/graph/api/resources/group?view=graph-rest-1.0), you cannot combine `$orderby` with `$filter` expressions.</span></span> 

## <a name="search-parameter"></a><span data-ttu-id="be32e-215">parámetro de búsqueda</span><span class="sxs-lookup"><span data-stu-id="be32e-215">search parameter</span></span>

<span data-ttu-id="be32e-216">Use el parámetro de consulta `$search` para restringir los resultados de una solicitud para que coincidan con un criterio de búsqueda</span><span class="sxs-lookup"><span data-stu-id="be32e-216">Use the `$search` query parameter to restrict the results of a request to match a search criterion.</span></span>

> <span data-ttu-id="be32e-p119">**Nota:** Actualmente **solo** se pueden buscar las colecciones [message](/graph/api/resources/message?view=graph-rest-1.0) y [person](/graph/api/resources/person?view=graph-rest-1.0). Una solicitud `$search` devuelve hasta 250 resultados. No puede usar [`$filter`](#filter-parameter) o [`$orderby`](#orderby-parameter) en una solicitud de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="be32e-p119">**Note:** You can currently search **only** [message](/graph/api/resources/message?view=graph-rest-1.0) and [person](/graph/api/resources/person?view=graph-rest-1.0) collections. A `$search` request returns up to 250 results. You cannot use [`$filter`](#filter-parameter) or [`$orderby`](#orderby-parameter) in a search request.</span></span>

### <a name="using-search-on-message-collections"></a><span data-ttu-id="be32e-220">Uso de $search en colecciones de mensajes</span><span class="sxs-lookup"><span data-stu-id="be32e-220">Using $search on message collections</span></span>

<span data-ttu-id="be32e-221">Puede buscar mensajes con un valor en las propiedades de los mensajes específicos.</span><span class="sxs-lookup"><span data-stu-id="be32e-221">You can search messages based on a value in specific message properties.</span></span> <span data-ttu-id="be32e-222">Los resultados de la búsqueda se ordenan por la fecha y la hora en que se ha enviado el mensaje.</span><span class="sxs-lookup"><span data-stu-id="be32e-222">The results of the search are sorted by the date and time that the message was sent.</span></span>

<span data-ttu-id="be32e-223">Si realiza una búsqueda en mensajes y especifica solo un valor sin las propiedades de mensaje específicas, la búsqueda se lleva a cabo con las propiedades de búsqueda predeterminadas de **from**, **subject** y **body**.</span><span class="sxs-lookup"><span data-stu-id="be32e-223">If you do a search on messages and specify only a value without specific message properties, the search is carried out on the default search properties of **from**, **subject**, and **body**.</span></span>

<span data-ttu-id="be32e-224">En el ejemplo siguiente, se devuelven todos los mensajes del buzón del usuario que ha iniciado sesión que contienen la palabra "pizza" en cualquiera de las tres propiedades de búsqueda predeterminadas:</span><span class="sxs-lookup"><span data-stu-id="be32e-224">The following example returns all messages in the signed-in user's Inbox that contains "pizza" in any of the three default search properties:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/messages?$search="pizza"
```

<span data-ttu-id="be32e-225">[Probar en el Probador de Graph][search-example]</span><span class="sxs-lookup"><span data-stu-id="be32e-225">[Try in Graph Explorer][search-example]</span></span>

<span data-ttu-id="be32e-226">Como alternativa, puede buscar mensajes especificando los nombres de propiedades de mensaje en la tabla siguiente, que se reconocen por la sintaxis de la consulta de palabras clave (KQL).</span><span class="sxs-lookup"><span data-stu-id="be32e-226">Alternatively, you can search messages by specifying message property names in the following table, that are recognized by the Keyword Query Language (KQL) syntax.</span></span> <span data-ttu-id="be32e-227">Estos nombres de propiedad corresponden a las propiedades que se definen en la entidad de **mensaje** de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="be32e-227">These property names correspond to properties defined in the **message** entity of Microsoft Graph.</span></span> <span data-ttu-id="be32e-228">Outlook y otras aplicaciones de Office 365, como SharePoint admiten la sintaxis KQL, proporciona la comodidad de un dominio de detección común para los almacenes de datos.</span><span class="sxs-lookup"><span data-stu-id="be32e-228">Outlook and other Office 365 applications such as SharePoint support KQL syntax, providing the convenience of a common discovery domain for their data stores.</span></span>


| <span data-ttu-id="be32e-229">Propiedades del correo electrónico que permiten búsquedas</span><span class="sxs-lookup"><span data-stu-id="be32e-229">Searchable email property</span></span>                | <span data-ttu-id="be32e-230">Descripción</span><span class="sxs-lookup"><span data-stu-id="be32e-230">Description</span></span> | <span data-ttu-id="be32e-231">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="be32e-231">Example</span></span> 
|:-------------------------|:------------|:---------|
| <span data-ttu-id="be32e-232">**attachment**</span><span class="sxs-lookup"><span data-stu-id="be32e-232">**attachment**</span></span>           | <span data-ttu-id="be32e-233">Los nombres de los archivos adjuntos a un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="be32e-233">The names of files attached to an email message.</span></span>|[`me/messages?$search="attachment:api-catalog.md"`][search-att-example]
| <span data-ttu-id="be32e-234">**bcc**</span><span class="sxs-lookup"><span data-stu-id="be32e-234">**bcc**</span></span>           | <span data-ttu-id="be32e-235">El campo **bcc** de un mensaje de correo electrónico, especificado como una dirección SMTP, alias o nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="be32e-235">The **bcc** field of an email message, specified as an SMTP address, display name, or alias.</span></span>|[`me/messages?$search="bcc:samanthab@contoso.com"&$select=subject,bccRecipients`][search-bcc-example]
| <span data-ttu-id="be32e-236">**body**</span><span class="sxs-lookup"><span data-stu-id="be32e-236">**body**</span></span>           | <span data-ttu-id="be32e-237">El cuerpo de un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="be32e-237">The body of an email message.</span></span>|[`me/messages?$search="body:excitement"`][search-body-example]
| <span data-ttu-id="be32e-238">**cc**</span><span class="sxs-lookup"><span data-stu-id="be32e-238">**cc**</span></span>           | <span data-ttu-id="be32e-239">El campo **cc** de un mensaje de correo electrónico, especificado como una dirección SMTP, alias o nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="be32e-239">The **cc** field of an email message, specified as an SMTP address, display name, or alias.</span></span>|[`me/messages?$search="cc:danas"&$select=subject,ccRecipients`][search-cc-example]
| <span data-ttu-id="be32e-240">**from**</span><span class="sxs-lookup"><span data-stu-id="be32e-240">**from**</span></span>           | <span data-ttu-id="be32e-241">El remitente de un mensaje de correo electrónico, especificado como una dirección SMTP, alias o nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="be32e-241">The sender of an email message, specified as an SMTP address, display name, or alias.</span></span>|[`me/messages?$search="from:randiw"&$select=subject,from`][search-from-example]
| <span data-ttu-id="be32e-242">**hasAttachment**</span><span class="sxs-lookup"><span data-stu-id="be32e-242">**hasAttachment**</span></span> | <span data-ttu-id="be32e-243">Verdadero si un mensaje contiene datos adjuntos que no son un archivo adjunto en línea, falso en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="be32e-243">True if an email message contains an attachment that is not an inline attachment, false otherwise.</span></span> |[`me/messages?$search="hasAttachments=true"`][search-from-example]
| <span data-ttu-id="be32e-244">**importance**</span><span class="sxs-lookup"><span data-stu-id="be32e-244">**importance**</span></span>           | <span data-ttu-id="be32e-245">La importancia de un mensaje de correo electrónico, que un remitente puede especificar al enviar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="be32e-245">The importance of an email message, which a sender can specify when sending a message.</span></span> <span data-ttu-id="be32e-246">Los valores posibles son`low`, `medium` o `high`.</span><span class="sxs-lookup"><span data-stu-id="be32e-246">The possible values are `low`, `medium`, or `high`.</span></span>|[`me/messages?$search="importance:high"&$select=subject,importance`][search-imp-example]
| <span data-ttu-id="be32e-247">**kind**</span><span class="sxs-lookup"><span data-stu-id="be32e-247">**kind**</span></span>           | <span data-ttu-id="be32e-248">El tipo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="be32e-248">The type of message.</span></span> <span data-ttu-id="be32e-249">Los valores posibles son `contacts`, `docs`, `email`, `faxes`, `im`, `journals`, `meetings`, `notes`, `posts`, `rssfeeds`, `tasks` o `voicemail`.</span><span class="sxs-lookup"><span data-stu-id="be32e-249">The possible values are `contacts`, `docs`, `email`, `faxes`, `im`, `journals`, `meetings`, `notes`, `posts`, `rssfeeds`, `tasks`, or `voicemail`.</span></span>|[`me/messages?$search="kind:voicemail"`][search-kind-example]
| <span data-ttu-id="be32e-250">**participants**</span><span class="sxs-lookup"><span data-stu-id="be32e-250">**participants**</span></span>           | <span data-ttu-id="be32e-251">Los campos **from**, **to**, **cc** y **bcc** de un mensaje de correo electrónico, especificados como una dirección SMTP, alias o nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="be32e-251">The **from**, **to**, **cc**, and **bcc** fields of an email message, specified as an SMTP address, display name, or alias.</span></span>|[`me/messages?$search="participants:danas"`][search-part-example]
| <span data-ttu-id="be32e-252">**received**</span><span class="sxs-lookup"><span data-stu-id="be32e-252">**received**</span></span>           | <span data-ttu-id="be32e-253">La fecha en la que un destinatario recibió un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="be32e-253">The date that an email message was received by a recipient.</span></span>|[`me/messages?$search="received:07/23/2018"&$select=subject,receivedDateTime`][search-rcvd-example]
| <span data-ttu-id="be32e-254">**recipients**</span><span class="sxs-lookup"><span data-stu-id="be32e-254">**recipients**</span></span>           | <span data-ttu-id="be32e-255">Los campos**to**, **cc** y **bcc** especificados como una dirección SMTP, alias o nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="be32e-255">The **to**, **cc**, and **bcc** fields of an email meesage, specified as an SMTP address, display name, or alias.</span></span>|[`me/messages?$search="recipients:randiq"&$select=subject,toRecipients,ccRecipients,bccRecipients`][search-rcpts-example]
| <span data-ttu-id="be32e-256">**sent**</span><span class="sxs-lookup"><span data-stu-id="be32e-256">**sent**</span></span>           | <span data-ttu-id="be32e-257">La fecha en la que un remitente envió un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="be32e-257">The date that an email message was sent by the sender.</span></span>|[`me/messages?$search="sent:07/23/2018"&$select=subject,sentDateTime`][search-sent-example]
| <span data-ttu-id="be32e-258">**size**</span><span class="sxs-lookup"><span data-stu-id="be32e-258">**size**</span></span>           | <span data-ttu-id="be32e-259">El tamaño de un elemento, en bytes.</span><span class="sxs-lookup"><span data-stu-id="be32e-259">The size of an item in bytes.</span></span>|[`me/messages?$search="size:1..500000"`][search-size-example]
| <span data-ttu-id="be32e-260">**subject**</span><span class="sxs-lookup"><span data-stu-id="be32e-260">**subject**</span></span>           | <span data-ttu-id="be32e-261">El texto en la línea de asunto de un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="be32e-261">The text in the subject line of an email message.</span></span> <span data-ttu-id="be32e-262">.</span><span class="sxs-lookup"><span data-stu-id="be32e-262"></span></span>|[`me/messages?$search="subject:has"&$select=subject`][search-sbj-example]
| <span data-ttu-id="be32e-263">**to**</span><span class="sxs-lookup"><span data-stu-id="be32e-263">**to**</span></span>           | <span data-ttu-id="be32e-264">El campo **to** de un mensaje de correo electrónico, especificado como una dirección SMTP, alias o nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="be32e-264">The **to** field of an email message, specified as an SMTP address, display name, or alias.</span></span>|[`me/messages?$search="to:randiw"&$select=subject,toRecipients`][search-to-example]


<span data-ttu-id="be32e-265">Para obtener más información sobre las propiedades de correo electrónico que permiten búsquedas, la sintaxis KQL, los operadores compatibles y las sugerencias de búsqueda, vea los artículos siguientes:</span><span class="sxs-lookup"><span data-stu-id="be32e-265">For more information about searchable email properties, KQL syntax, supported operators, and tips on searching, see the following articles:</span></span>

- <span data-ttu-id="be32e-266">[Propiedades que permiten búsquedas en Exchange](https://docs.microsoft.com/es-ES/Exchange/policy-and-compliance/ediscovery/message-properties-and-search-operators#searchable-properties-in-exchange).</span><span class="sxs-lookup"><span data-stu-id="be32e-266">[Searchable properties in Exchange](https://docs.microsoft.com/es-ES/Exchange/policy-and-compliance/ediscovery/message-properties-and-search-operators#searchable-properties-in-exchange).</span></span>

- [<span data-ttu-id="be32e-267">Referencia de la sintaxis del lenguaje de consultas de palabras clave (KQL)</span><span class="sxs-lookup"><span data-stu-id="be32e-267">Keyword Query Language (KQL) syntax reference</span></span>](https://docs.microsoft.com/es-ES/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference)

- <span data-ttu-id="be32e-268">
  [Propiedades de mensajes y operadores de búsqueda para eDiscovery local en Exchange 2016](https://technet.microsoft.com/en-us/library/dn774955(v=exchg.160).aspx)</span><span class="sxs-lookup"><span data-stu-id="be32e-268">[Message properties and search operators for In-Place eDiscovery in Exchange 2016](https://technet.microsoft.com/en-us/library/dn774955(v=exchg.160).aspx)</span></span>

### <a name="using-search-on-person-collections"></a><span data-ttu-id="be32e-269">Uso de $search en colecciones de usuarios</span><span class="sxs-lookup"><span data-stu-id="be32e-269">Using $search on person collections</span></span>

<span data-ttu-id="be32e-p125">Puede usar la API de contactos de Microsoft Graph para recuperar los contactos más relevantes para un usuario. La relevancia viene determinada por las relaciones empresariales y los patrones de comunicación y colaboración del usuario. La API de contactos admite el parámetro de consulta `$search`.</span><span class="sxs-lookup"><span data-stu-id="be32e-p125">You can use the Microsoft Graph People API to retrieve the people who are most relevant to a user. Relevance is determined by the user’s communication and collaboration patterns and business relationships. The People API supports the `$search` query parameter.</span></span>

<span data-ttu-id="be32e-273">Las búsquedas de contactos se realizan en las propiedades **displayName** y **emailAddress** del recurso [person](/graph/api/resources/person?view=graph-rest-1.0).</span><span class="sxs-lookup"><span data-stu-id="be32e-273">Searches on people occur on both the **displayName** and **emailAddress** properties of the [person](/graph/api/resources/person?view=graph-rest-1.0) resource.</span></span>

<span data-ttu-id="be32e-274">La solicitud siguiente busca una persona llamada "Irene McGowen" en las propiedades **displayName** y **emailAddress** de todos los miembros de la colección **people** del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="be32e-274">The following request does a search for a person named "Irene McGowen" in the **displayName** and **emailAddress** properties in each person in the **people** collection of the signed-in user.</span></span> <span data-ttu-id="be32e-275">Dado que existe una persona llamada "Irene McGowan" relevante para el usuario que ha iniciado sesión, se devuelve la información de "Irene McGowan".</span><span class="sxs-lookup"><span data-stu-id="be32e-275">Because a person named "Irene McGowan" is relevant to the signed-in user, the information for "Irene McGowan" is returned.</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/people/?$search="Irene McGowen"
```

<span data-ttu-id="be32e-276">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="be32e-276">The following example shows the response.</span></span> 

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

<span data-ttu-id="be32e-277">Para más información sobre la API de contactos, vea [Obtener información sobre contactos relevantes](./people-example.md#search-people).</span><span class="sxs-lookup"><span data-stu-id="be32e-277">To learn more about the People API, see [Get information about relevant people](./people-example.md#search-people).</span></span>  

## <a name="select-parameter"></a><span data-ttu-id="be32e-278">parámetro de selección</span><span class="sxs-lookup"><span data-stu-id="be32e-278">select parameter</span></span>

<span data-ttu-id="be32e-279">Use el parámetro de consulta `$select` para devolver un conjunto de propiedades diferente al predeterminado para un recurso individual o una colección de recursos.</span><span class="sxs-lookup"><span data-stu-id="be32e-279">Use the `$select` query parameter to return a set of properties that are different than the default set for an individual resource or a collection of resources.</span></span> <span data-ttu-id="be32e-280">Con $select, puede especificar un subconjunto o un superconjunto de las propiedades predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="be32e-280">With $select, you can specify a subset or a superset of the default properties.</span></span>

<span data-ttu-id="be32e-281">Por ejemplo, al recuperar los mensajes del usuario que ha iniciado sesión, puede especificar que solo se devuelvan las propiedades **from** y **subject**:</span><span class="sxs-lookup"><span data-stu-id="be32e-281">For example, when retrieving the messages of the signed-in user, you can specify that only the **from** and **subject** properties be returned:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/messages?$select=from,subject
```

<span data-ttu-id="be32e-282">[Probar en el Probador de Graph][select-example]</span><span class="sxs-lookup"><span data-stu-id="be32e-282">[Try in Graph Explorer][select-example]</span></span>

> <span data-ttu-id="be32e-283">**Importante:** En general, se recomienda usar `$select` para limitar las propiedades devueltas por una consulta a las necesarias para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="be32e-283">**Important:** In general, we recommend that you use `$select` to limit the properties returned by a query to those needed by your app.</span></span> <span data-ttu-id="be32e-284">Esto es especialmente cierto para las consultas que potencialmente pueden devolver un conjunto de resultados grande.</span><span class="sxs-lookup"><span data-stu-id="be32e-284">This is especially true of queries that might potentially return a large result set.</span></span> <span data-ttu-id="be32e-285">Limitar las propiedades devueltas en cada fila reducirá la carga en la red y ayudará a mejorar el rendimiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="be32e-285">Limiting the properties returned in each row will reduce network load and help improve your app's performance.</span></span>
>
> <span data-ttu-id="be32e-p129">En `v1.0`, algunos recursos de Azure AD que se derivan de [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-1.0), como [user](/graph/api/resources/user?view=graph-rest-1.0) y [group](/graph/api/resources/group?view=graph-rest-1.0), devuelven un subconjunto predeterminado limitado de propiedades en las operaciones de lectura. Para estos recursos, debe usar `$select` para devolver propiedades fuera el conjunto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="be32e-p129">In `v1.0`, some Azure AD resources that derive from [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-1.0), like [user](/graph/api/resources/user?view=graph-rest-1.0) and [group](/graph/api/resources/group?view=graph-rest-1.0), return a limited, default subset of properties on reads. For these resources, you must use `$select` to return properties outside of the default set.</span></span>  

## <a name="skip-parameter"></a><span data-ttu-id="be32e-288">parámetros de omisión</span><span class="sxs-lookup"><span data-stu-id="be32e-288">skip parameter</span></span>

<span data-ttu-id="be32e-p130">Use el parámetro de consulta `$skip` para establecer el número de elementos que se omitirán al inicio de una colección. Por ejemplo, la solicitud siguiente devuelve eventos para el usuario ordenados por fecha de creación, empezando por el evento 21 de la colección:</span><span class="sxs-lookup"><span data-stu-id="be32e-p130">Use the `$skip` query parameter to set the number of items to skip at the start of a collection. For example, the following request returns events for the user sorted by date created, starting with the 21st event in the collection:</span></span>

```http
GET  https://graph.microsoft.com/v1.0/me/events?$orderby=createdDateTime&$skip=20
```
<span data-ttu-id="be32e-291">[Probar en el Probador de Graph][skip-example]</span><span class="sxs-lookup"><span data-stu-id="be32e-291">[Try in Graph Explorer][skip-example]</span></span>

> <span data-ttu-id="be32e-292">**Nota:** En algunas API de Microsoft Graph, como Correo y Calendario de Outlook (**message**, **event** y **calendar**), se usa `$skip` para implementar la paginación.</span><span class="sxs-lookup"><span data-stu-id="be32e-292">**Note:** Some Microsoft Graph APIs, like Outlook Mail and Calendars (**message**, **event**, and **calendar**), use `$skip` to implement paging.</span></span> <span data-ttu-id="be32e-293">Cuando los resultados de una consulta ocupen varias páginas, estas API devolverán una propiedad `@odata:nextLink` con una dirección URL que contendrá un parámetro `$skip`.</span><span class="sxs-lookup"><span data-stu-id="be32e-293">When results of a query span multiple pages, these APIs will return an `@odata:nextLink` property with a URL that contains a `$skip` parameter.</span></span> <span data-ttu-id="be32e-294">Puede usar esta dirección URL para devolver la siguiente página de resultados.</span><span class="sxs-lookup"><span data-stu-id="be32e-294">You can use this URL to return the next page of results.</span></span> <span data-ttu-id="be32e-295">Para obtener más información, vea [Paginación](./paging.md).</span><span class="sxs-lookup"><span data-stu-id="be32e-295">To learn more, see [Paging](./paging.md).</span></span>

## <a name="skiptoken-parameter"></a><span data-ttu-id="be32e-296">parámetro skipToken</span><span class="sxs-lookup"><span data-stu-id="be32e-296">skipToken parameter</span></span>

<span data-ttu-id="be32e-p132">Algunas consultas devuelven varias páginas de datos debido a la paginación del servidor o al uso del parámetro [`$top`](#top-parameter) para limitar el tamaño de página de la respuesta. Muchas API de Microsoft Graph usan el parámetro de consulta `skipToken` para hacer referencia a las páginas siguientes del resultado. El parámetro `$skiptoken` contiene un token opaco que hace referencia a la siguiente página de resultados y se devuelve en la dirección URL proporcionada en la propiedad `@odata.nextLink` en la respuesta. Para obtener más información, vea [Paginación](./paging.md).</span><span class="sxs-lookup"><span data-stu-id="be32e-p132">Some requests return multiple pages of data either due to server-side paging or due to the use of the [`$top`](#top-parameter) parameter to limit the page size of the response. Many Microsoft Graph APIs use the `skipToken` query parameter to reference subsequent pages of the result. The `$skiptoken` parameter contains an opaque token that references the next page of results and is returned in the URL provided in the `@odata.nextLink` property in the response. To learn more, see [Paging](./paging.md).</span></span>


## <a name="top-parameter"></a><span data-ttu-id="be32e-301">parámetro superior</span><span class="sxs-lookup"><span data-stu-id="be32e-301">top parameter</span></span>

<span data-ttu-id="be32e-302">Use el parámetro de consulta `$top` para especificar el tamaño de página del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="be32e-302">Use the `$top` query parameter to specify the page size of the result set.</span></span> 

<span data-ttu-id="be32e-303">Si quedan más elementos en el conjunto de resultados, el cuerpo de la respuesta contendrá un parámetro `@odata.nextLink`.</span><span class="sxs-lookup"><span data-stu-id="be32e-303">If more items remain in the result set, the response body will contain an `@odata.nextLink` parameter.</span></span> <span data-ttu-id="be32e-304">Este parámetro contiene una dirección URL que se puede usar para obtener la siguiente página de resultados.</span><span class="sxs-lookup"><span data-stu-id="be32e-304">This parameter contains a URL that you can use to get the next page of results.</span></span> <span data-ttu-id="be32e-305">Para obtener más información, vea [Paginación](./paging.md).</span><span class="sxs-lookup"><span data-stu-id="be32e-305">To learn more, see [Paging](./paging.md).</span></span> 

<span data-ttu-id="be32e-306">Por ejemplo, la solicitud siguiente devuelve los cinco primeros mensajes en el buzón del usuario:</span><span class="sxs-lookup"><span data-stu-id="be32e-306">For example, the following request returns the first five messages in the user's mailbox:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/messages?$top=5
```

<span data-ttu-id="be32e-307">[Probar en el Probador de Graph][top-example]</span><span class="sxs-lookup"><span data-stu-id="be32e-307">[Try in Graph Explorer][top-example]</span></span>


## <a name="error-handling-for-query-parameters"></a><span data-ttu-id="be32e-308">Control de errores para parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="be32e-308">Error handling for query parameters</span></span>

<span data-ttu-id="be32e-p134">Algunas solicitudes devolverán un mensaje de error si no se admite un parámetro de consulta especificado. Por ejemplo, no se puede usar `$expand` en la relación `user/photo`.</span><span class="sxs-lookup"><span data-stu-id="be32e-p134">Some requests will return an error message if a specified query parameter is not supported. For example, you cannot use `$expand` on the `user/photo` relationship.</span></span> 

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

<span data-ttu-id="be32e-311">Pero es importante tener en cuenta que los parámetros de consulta especificados en una solicitud pueden devolver un error silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="be32e-311">However, it is important to note that query parameters specified in a request might fail silently.</span></span> <span data-ttu-id="be32e-312">Esto puede suceder con parámetros de consulta no admitidos, así como con combinaciones no compatibles de parámetros de consulta.</span><span class="sxs-lookup"><span data-stu-id="be32e-312">This can be true for unsupported query parameters as well as for unsupported combinations of query parameters.</span></span> <span data-ttu-id="be32e-313">En estos casos, debe examinar los datos devueltos por la solicitud para determinar si los parámetros de consulta especificados tuvieron el efecto previsto.</span><span class="sxs-lookup"><span data-stu-id="be32e-313">In these cases, you should examine the data returned by the request to determine whether the query parameters you specified had the desired effect.</span></span> 

[graph-explorer]: https://developer.microsoft.com/graph/graph-explorer
[odata-filter]: https://docs.oasis-open.org/odata/odata/v4.0/errata03/os/complete/part2-url-conventions/odata-v4.0-errata03-os-part2-url-conventions-complete.html#_Toc453752358
[odata-query]: https://docs.oasis-open.org/odata/odata/v4.0/errata03/os/complete/part2-url-conventions/odata-v4.0-errata03-os-part2-url-conventions-complete.html#_Toc453752356
[count-example]: https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$top=2%26$count=true&method=GET&version=v1.0
[expand-example]: https://developer.microsoft.com/graph/graph-explorer?request=groups?$expand=members&method=GET&version=v1.0
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

