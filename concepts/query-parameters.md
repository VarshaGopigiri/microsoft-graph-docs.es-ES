---
title: Usar parámetros de consulta para personalizar respuestas
description: Microsoft Graph proporciona parámetros de consulta opcionales que puede usar para especificar y controlar la cantidad de datos devueltos en una respuesta. Se admiten los siguientes parámetros de consulta.
author: piotrci
ms.openlocfilehash: 6cdc4ce0f502e941e24a6197e7ba4b65cac13b20
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27311840"
---
# <a name="use-query-parameters-to-customize-responses"></a><span data-ttu-id="e67e9-104">Usar parámetros de consulta para personalizar respuestas</span><span class="sxs-lookup"><span data-stu-id="e67e9-104">Use query parameters to customize responses</span></span>

<span data-ttu-id="e67e9-105">Microsoft Graph admite parámetros de consulta opcionales que puede usar para especificar y controlar la cantidad de datos devueltos en una respuesta.</span><span class="sxs-lookup"><span data-stu-id="e67e9-105">Microsoft Graph supports optional query parameters that you can use to specify and control the amount of data returned in a response.</span></span> <span data-ttu-id="e67e9-106">La compatibilidad con los parámetros de consulta exactos varía de una operación API a otra y, en función de la API, puede diferir entre los puntos de conexión de las versiones 1.0 y beta.</span><span class="sxs-lookup"><span data-stu-id="e67e9-106">The support for the exact query parameters varies from one API operation to another, and depending on the API, can differ between the v1.0 and beta endpoints.</span></span> 

> <span data-ttu-id="e67e9-107">**Nota:** en los puntos de conexión de las versiones 1.0 y beta, el prefijo `$` es opcional.</span><span class="sxs-lookup"><span data-stu-id="e67e9-107">**Note:** On the v1.0 and beta endpoints, the `$` prefix is optional.</span></span> <span data-ttu-id="e67e9-108">Por ejemplo, en lugar de `$filter`, puede usar `filter`.</span><span class="sxs-lookup"><span data-stu-id="e67e9-108">For example, instead of `$filter`, you can use `filter`.</span></span>

<span data-ttu-id="e67e9-109">Los parámetros de consulta pueden ser opciones de consulta de sistema de OData u otros parámetros de consulta.</span><span class="sxs-lookup"><span data-stu-id="e67e9-109">Query parameters can be OData system query options or other query parameters.</span></span> 

## <a name="odata-system-query-options"></a><span data-ttu-id="e67e9-110">Opciones de consulta de sistema de OData</span><span class="sxs-lookup"><span data-stu-id="e67e9-110">OData system query options</span></span>
<span data-ttu-id="e67e9-111">Una operación de API de Microsoft Graph podría admitir una o varias de las siguientes opciones de consulta de sistema de OData.</span><span class="sxs-lookup"><span data-stu-id="e67e9-111">A Microsoft Graph API operation might support one or more of the following OData system query options.</span></span> <span data-ttu-id="e67e9-112">Estas opciones de consulta son compatibles con el [lenguaje de consulta de OData V4][odata-query].</span><span class="sxs-lookup"><span data-stu-id="e67e9-112">These query options are compatible with the [OData V4 query language][odata-query].</span></span>

><span data-ttu-id="e67e9-113">**Nota:** haga clic en los ejemplos para probarlos en el [Probador de Graph][graph-explorer].</span><span class="sxs-lookup"><span data-stu-id="e67e9-113">**Note:** Click the examples to try them in [Graph Explorer][graph-explorer].</span></span>

| <span data-ttu-id="e67e9-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="e67e9-114">Name</span></span>                     | <span data-ttu-id="e67e9-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="e67e9-115">Description</span></span> | <span data-ttu-id="e67e9-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e67e9-116">Example</span></span>
|:-------------------------|:------------|:---------|
| [<span data-ttu-id="e67e9-117">$count</span><span class="sxs-lookup"><span data-stu-id="e67e9-117">$count</span></span>](#count-parameter)         | <span data-ttu-id="e67e9-118">Recupera el número total de recursos coincidentes.</span><span class="sxs-lookup"><span data-stu-id="e67e9-118">Retrieves the total count of matching resources.</span></span> | [`/me/messages?$top=2&$count=true`][count-example]
| [<span data-ttu-id="e67e9-119">$expand</span><span class="sxs-lookup"><span data-stu-id="e67e9-119">$expand</span></span>](#expand-parameter)       | <span data-ttu-id="e67e9-120">Recupera los recursos relacionados.</span><span class="sxs-lookup"><span data-stu-id="e67e9-120">Retrieves related resources.</span></span>|[`/groups?$expand=members`][expand-example]
| [<span data-ttu-id="e67e9-121">$filter</span><span class="sxs-lookup"><span data-stu-id="e67e9-121">$filter</span></span>](#filter-parameter)       | <span data-ttu-id="e67e9-122">Filtra los resultados (filas).</span><span class="sxs-lookup"><span data-stu-id="e67e9-122">Filters results (rows).</span></span>|[`/users?$filter=startswith(givenName,'J')`][filter-example]
| [<span data-ttu-id="e67e9-123">$format</span><span class="sxs-lookup"><span data-stu-id="e67e9-123">$format</span></span>](#format-parameter)       | <span data-ttu-id="e67e9-124">Devuelve los resultados en el formato de medio especificado.</span><span class="sxs-lookup"><span data-stu-id="e67e9-124">Returns the results in the specified media format.</span></span>|[`/users?$format=json`][format-example]
| [<span data-ttu-id="e67e9-125">$orderby</span><span class="sxs-lookup"><span data-stu-id="e67e9-125">$orderby</span></span>](#orderby-parameter)     | <span data-ttu-id="e67e9-126">Ordena los resultados.</span><span class="sxs-lookup"><span data-stu-id="e67e9-126">Orders results.</span></span>|[`/users?$orderby=displayName desc`][orderby-example]
| [<span data-ttu-id="e67e9-127">$search</span><span class="sxs-lookup"><span data-stu-id="e67e9-127">$search</span></span>](#search-parameter)       | <span data-ttu-id="e67e9-p105">Devuelve los resultados en función de los criterios de búsqueda. Actualmente, se admite en las colecciones de **mensajes** y **usuarios**.</span><span class="sxs-lookup"><span data-stu-id="e67e9-p105">Returns results based on search criteria. Currently supported on **messages** and **person** collections.</span></span>|[`/me/messages?$search=pizza`][search-example]
| [<span data-ttu-id="e67e9-130">$select</span><span class="sxs-lookup"><span data-stu-id="e67e9-130">$select</span></span>](#select-parameter)       | <span data-ttu-id="e67e9-131">Filtra las propiedades (columnas).</span><span class="sxs-lookup"><span data-stu-id="e67e9-131">Filters properties (columns).</span></span>|[`/users?$select=givenName,surname`][select-example]
| [<span data-ttu-id="e67e9-132">$skip</span><span class="sxs-lookup"><span data-stu-id="e67e9-132">$skip</span></span>](#skip-parameter)           | <span data-ttu-id="e67e9-p106">Indexa en un conjunto de resultados. También se usa en algunas API para implementar la paginación y se puede usar junto a `$top` para paginar manualmente los resultados.</span><span class="sxs-lookup"><span data-stu-id="e67e9-p106">Indexes into a result set. Also used by some APIs to implement paging and can be used together with `$top` to manually page results.</span></span> | [`/me/messages?$skip=11`][skip-example]
| [<span data-ttu-id="e67e9-135">$top</span><span class="sxs-lookup"><span data-stu-id="e67e9-135">$top</span></span>](#top-parameter)             | <span data-ttu-id="e67e9-136">Establece el tamaño de la página de resultados.</span><span class="sxs-lookup"><span data-stu-id="e67e9-136">Sets the page size of results.</span></span> |[`/users?$top=2`][top-example]


## <a name="other-query-parameters"></a><span data-ttu-id="e67e9-137">Otros parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="e67e9-137">Other query parameters</span></span>

| <span data-ttu-id="e67e9-138">Nombre</span><span class="sxs-lookup"><span data-stu-id="e67e9-138">Name</span></span>                     | <span data-ttu-id="e67e9-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="e67e9-139">Description</span></span> | <span data-ttu-id="e67e9-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e67e9-140">Example</span></span>
|:-------------------------|:------------|:---------|
| [<span data-ttu-id="e67e9-141">$skipToken</span><span class="sxs-lookup"><span data-stu-id="e67e9-141">$skipToken</span></span>](#skiptoken-parameter) | <span data-ttu-id="e67e9-p107">Recupera la siguiente página de resultados de conjuntos de resultados que abarcan varias páginas. (Algunas API usan `$skip` en su lugar).</span><span class="sxs-lookup"><span data-stu-id="e67e9-p107">Retrieves the next page of results from result sets that span multiple pages. (Some APIs use `$skip` instead.)</span></span> | `/users?$skiptoken=X%274453707402000100000017...`|

## <a name="encoding-query-parameters"></a><span data-ttu-id="e67e9-144">Codificación de parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="e67e9-144">Encoding query parameters</span></span>

<span data-ttu-id="e67e9-145">Los valores de los parámetros de consulta deben ser codificados por porcentaje.</span><span class="sxs-lookup"><span data-stu-id="e67e9-145">The values of query parameters should be percent-encoded.</span></span> <span data-ttu-id="e67e9-146">Muchos clientes HTTP, exploradores y herramientas (como el [Probador de Graph][graph-explorer]) le servirán de ayuda.</span><span class="sxs-lookup"><span data-stu-id="e67e9-146">Many HTTP clients, browsers, and tools (such as the [Graph Explorer][graph-explorer]) will help you with this.</span></span> <span data-ttu-id="e67e9-147">Si una consulta produce un error, puede deberse a que los valores de los parámetros de consulta no se han codificado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e67e9-147">If a query is failing, one possible cause is failure to encode the query parameter values appropriately.</span></span>

<span data-ttu-id="e67e9-148">Una dirección URL sin codificar tiene el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="e67e9-148">An unencoded URL looks like this:</span></span>

```http
GET https://graph.microsoft.com/v1.0/users?$filter=startswith(givenName, 'J')
```

<span data-ttu-id="e67e9-149">Una dirección URL codificada correctamente tiene el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="e67e9-149">A properly encoded URL looks like this:</span></span>

```http
GET https://graph.microsoft.com/v1.0/users?$filter=startswith(givenName%2C+'J')
```

## <a name="count-parameter"></a><span data-ttu-id="e67e9-150">parámetro de recuento</span><span class="sxs-lookup"><span data-stu-id="e67e9-150">count parameter</span></span>

<span data-ttu-id="e67e9-151">Use el parámetro de consulta `$count` para incluir un recuento del número total de elementos de una colección junto con la página de valores de datos que se devuelve desde Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="e67e9-151">Use the `$count` query parameter to include a count of the total number of items in a collection alongside the page of data values returned from Microsoft Graph.</span></span> 

<span data-ttu-id="e67e9-152">Por ejemplo, la siguiente solicitud devolverá tanto la colección de **contactos** del usuario actual como el número de elementos de la colección de **contactos** en la propiedad `@odata.count`.</span><span class="sxs-lookup"><span data-stu-id="e67e9-152">For example, the following request will return both the **contact** collection of the current user, and the number of items in the **contact** collection in the `@odata.count` property.</span></span>

```http
GET  https://graph.microsoft.com/v1.0/me/contacts?$count=true
```

<span data-ttu-id="e67e9-153">
  [Probar en el Probador de Graph](https://developer.microsoft.com/graph/graph-explorer?request=me/contacts?$count=true&method=GET&version=v1.0)</span><span class="sxs-lookup"><span data-stu-id="e67e9-153">[Try in Graph Explorer](https://developer.microsoft.com/graph/graph-explorer?request=me/contacts?$count=true&method=GET&version=v1.0)</span></span>


><span data-ttu-id="e67e9-154">**Nota:** `$count` no se admite con colecciones de recursos que se derivan de [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-1.0), como las colecciones de [usuarios](/graph/api/resources/user?view=graph-rest-1.0) o [grupos](/graph/api/resources/group?view=graph-rest-1.0).</span><span class="sxs-lookup"><span data-stu-id="e67e9-154">**Note:** `$count` is not supported for collections of resources that derive from [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-1.0) like collections of [users](/graph/api/resources/user?view=graph-rest-1.0) or [groups](/graph/api/resources/group?view=graph-rest-1.0).</span></span>

## <a name="expand-parameter"></a><span data-ttu-id="e67e9-155">parámetro de expansión</span><span class="sxs-lookup"><span data-stu-id="e67e9-155">expand parameter</span></span>

<span data-ttu-id="e67e9-156">Muchos de los recursos de Microsoft Graph exponen ambas propiedades declaradas de los recursos, así como sus relaciones con otros recursos.</span><span class="sxs-lookup"><span data-stu-id="e67e9-156">Many Microsoft Graph resources expose both declared properties of the resource as well as its relationships with other resources.</span></span> <span data-ttu-id="e67e9-157">Estas relaciones también se denominan propiedades de referencia o propiedades de navegación, y pueden hacer referencia a un único recurso o a una colección de recursos.</span><span class="sxs-lookup"><span data-stu-id="e67e9-157">These relationships are also called reference properties or navigation properties, and they can reference either a single resource or a collection of resources.</span></span> <span data-ttu-id="e67e9-158">Por ejemplo, las carpetas de correo, el administrador y los informes directos de un usuario se exponen como relaciones.</span><span class="sxs-lookup"><span data-stu-id="e67e9-158">For example, the mail folders, manager, and direct reports of a user are all exposed as relationships.</span></span> 

<span data-ttu-id="e67e9-p110">Normalmente, se pueden consultar las propiedades de un recurso o una de sus relaciones en una sola solicitud, pero no ambas. Puede usar el parámetro de cadena de consulta `$expand` para incluir en los resultados de la consulta el recurso expandido o la colección a la que se hace referencia con una única relación (propiedad de navegación).</span><span class="sxs-lookup"><span data-stu-id="e67e9-p110">Normally, you can query either the properties of a resource or one of its relationships in a single request, but not both. You can use the `$expand` query string parameter to include the expanded resource or collection referenced by a single relationship (navigation property) in your results.</span></span>

<span data-ttu-id="e67e9-161">En el ejemplo siguiente se obtiene la información de la unidad raíz junto con los elementos secundarios de nivel superior de una unidad:</span><span class="sxs-lookup"><span data-stu-id="e67e9-161">The following example gets root drive information along with the top-level child items in a drive:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/drive/root?$expand=children
```

<span data-ttu-id="e67e9-162">
  [Probar en el Probador de Graph](https://developer.microsoft.com/graph/graph-explorer?request=me/drive/root?$expand=children&method=GET&version=v1.0)</span><span class="sxs-lookup"><span data-stu-id="e67e9-162">[Try in Graph Explorer](https://developer.microsoft.com/graph/graph-explorer?request=me/drive/root?$expand=children&method=GET&version=v1.0)</span></span>

<span data-ttu-id="e67e9-p111">Con algunas colecciones de recursos, también se pueden especificar las propiedades que se van a devolver en los recursos expandidos si se agrega un parámetro `$select`. En el ejemplo siguiente se realiza la misma consulta que en el anterior, pero se usa una instrucción [`$select`](#select-parameter) para limitar las propiedades devueltas para los elementos secundarios expandidos a las propiedades **id** y **name**.</span><span class="sxs-lookup"><span data-stu-id="e67e9-p111">With some resource collections, you can also specify the properties to be returned in the expanded resources by adding a `$select` parameter. The following example performs the same query as the previous example but uses a [`$select`](#select-parameter) statement to limit the properties returned for the expanded child items to the **id** and **name** properties.</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/drive/root?$expand=children($select=id,name)
```

<span data-ttu-id="e67e9-165">[Probar en el Probador de Graph][expand-example]</span><span class="sxs-lookup"><span data-stu-id="e67e9-165">[Try in Graph Explorer][expand-example]</span></span>

> <span data-ttu-id="e67e9-p112">**Nota:** No todas las relaciones y recursos admiten el parámetro de consulta `$expand`. Por ejemplo, se pueden expandir las relaciones **directReports**, **manager** y **memberOf** de un usuario, pero no se pueden expandir sus relaciones **events**, **messages** o **photo**. No todos los recursos o relaciones admiten el uso de `$select` en elementos expandidos.</span><span class="sxs-lookup"><span data-stu-id="e67e9-p112">**Note:** Not all relationships and resources support the `$expand` query parameter. For example, you can expand the **directReports**, **manager**, and **memberOf** relationships on a user, but you cannot expand its **events**, **messages**, or **photo** relationships. Not all resources or relationships support using `$select` on expanded items.</span></span> 
> 
> <span data-ttu-id="e67e9-169">Con recursos de Azure AD que se derivan de [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-1.0), como [user](/graph/api/resources/user?view=graph-rest-1.0) y [group](/graph/api/resources/group?view=graph-rest-1.0), solo se admite `$expand` para `beta` y normalmente devuelve un máximo de 20 elementos para la relación expandida.</span><span class="sxs-lookup"><span data-stu-id="e67e9-169">With Azure AD resources that derive from [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-1.0), like [user](/graph/api/resources/user?view=graph-rest-1.0) and [group](/graph/api/resources/group?view=graph-rest-1.0), `$expand` is only supported for `beta` and  typically returns a maximum of 20 items for the expanded relationship.</span></span>

## <a name="filter-parameter"></a><span data-ttu-id="e67e9-170">parámetro de filtrado</span><span class="sxs-lookup"><span data-stu-id="e67e9-170">filter parameter</span></span>

<span data-ttu-id="e67e9-171">Use el parámetro de consulta `$filter` para recuperar solo un subconjunto de una colección.</span><span class="sxs-lookup"><span data-stu-id="e67e9-171">Use the `$filter` query parameter to retrieve just a subset of a collection.</span></span> 

<span data-ttu-id="e67e9-172">Por ejemplo, para buscar usuarios cuyos nombres para mostrar comiencen por la letra "J", use `startswith`.</span><span class="sxs-lookup"><span data-stu-id="e67e9-172">For example, to find users whose display name starts with the letter 'J', use `startswith`.</span></span>

```http
GET https://graph.microsoft.com/v1.0/users?$filter=startswith(displayName,'J')
```

<span data-ttu-id="e67e9-173">[Probar en el Probador de Graph][filter-example]</span><span class="sxs-lookup"><span data-stu-id="e67e9-173">[Try in Graph Explorer][filter-example]</span></span>

<span data-ttu-id="e67e9-174">La compatibilidad con los operadores `$filter` varía en función de la API de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="e67e9-174">Support for `$filter` operators varies across Microsoft Graph APIs.</span></span> <span data-ttu-id="e67e9-175">Generalmente, se admiten los siguientes operadores lógicos:</span><span class="sxs-lookup"><span data-stu-id="e67e9-175">The following logical operators are generally supported:</span></span> 

- <span data-ttu-id="e67e9-176">igual a (`eq`)</span><span class="sxs-lookup"><span data-stu-id="e67e9-176">equals (`eq`)</span></span>
- <span data-ttu-id="e67e9-177">no es igual a (`ne`)</span><span class="sxs-lookup"><span data-stu-id="e67e9-177">not equals (`ne`)</span></span>
- <span data-ttu-id="e67e9-178">mayor que (`gt`)</span><span class="sxs-lookup"><span data-stu-id="e67e9-178">greater than (`gt`)</span></span>
- <span data-ttu-id="e67e9-179">mayor o igual que (`ge`)</span><span class="sxs-lookup"><span data-stu-id="e67e9-179">greater than or equals (`ge`)</span></span>
- <span data-ttu-id="e67e9-180">menor que (`lt`), menor o igual que (`le`)</span><span class="sxs-lookup"><span data-stu-id="e67e9-180">less than (`lt`), less than or equals (`le`)</span></span>
- <span data-ttu-id="e67e9-181">y (`and`)</span><span class="sxs-lookup"><span data-stu-id="e67e9-181">and (`and`)</span></span>
- <span data-ttu-id="e67e9-182">o (`or`)</span><span class="sxs-lookup"><span data-stu-id="e67e9-182">or (`or`)</span></span>
- <span data-ttu-id="e67e9-183">no (`not`)</span><span class="sxs-lookup"><span data-stu-id="e67e9-183">not (`not`)</span></span>
 
<span data-ttu-id="e67e9-184">El operador de cadena `startswith` se suele admitir.</span><span class="sxs-lookup"><span data-stu-id="e67e9-184">The `startswith` string operator is often supported.</span></span> <span data-ttu-id="e67e9-185">El operador lambda `any` se admite con algunas API.</span><span class="sxs-lookup"><span data-stu-id="e67e9-185">The `any` lambda operator is supported for some APIs.</span></span> <span data-ttu-id="e67e9-186">Para obtener algunos ejemplos de uso, vea la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e67e9-186">For some  usage examples, see the following table.</span></span> <span data-ttu-id="e67e9-187">Para obtener detalles adicionales sobre la sintaxis de `$filter`, vea el [protocolo OData][odata-filter].</span><span class="sxs-lookup"><span data-stu-id="e67e9-187">For more details about `$filter` syntax, see the [OData protocol][odata-filter].</span></span>  

<span data-ttu-id="e67e9-188">En la tabla siguiente se muestran algunos ejemplos de uso del parámetro de consulta `$filter`.</span><span class="sxs-lookup"><span data-stu-id="e67e9-188">The following table shows some examples that use the `$filter` query parameter.</span></span>

> <span data-ttu-id="e67e9-189">**Nota:** Haga clic en los ejemplos para probarlos en [Probador de Graph][graph-explorer].</span><span class="sxs-lookup"><span data-stu-id="e67e9-189">**Note:** Click the examples to try them in [Graph Explorer][graph-explorer].</span></span>

| <span data-ttu-id="e67e9-190">Descripción</span><span class="sxs-lookup"><span data-stu-id="e67e9-190">Description</span></span> | <span data-ttu-id="e67e9-191">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e67e9-191">Example</span></span>
|:------------|:--------|
| <span data-ttu-id="e67e9-192">Buscar usuarios con el nombre Mary en varias propiedades.</span><span class="sxs-lookup"><span data-stu-id="e67e9-192">Search for users with the name Mary across multiple properties.</span></span> | [`https://graph.microsoft.com/v1.0/users?$filter=startswith(displayName,'mary') or startswith(givenName,'mary') or startswith(surname,'mary') or startswith(mail,'mary') or startswith(userPrincipalName,'mary')`](https://developer.microsoft.com/graph/graph-explorer?request=users?$filter=startswith(displayName,'mary')+or+startswith(givenName,'mary')+or+startswith(surname,'mary')+or+startswith(mail,'mary')+or+startswith(userPrincipalName,'mary')&method=GET&version=v1.0) 
| <span data-ttu-id="e67e9-193">Obtener todos los eventos del usuario que inició sesión que comiencen después del 1/7/2017.</span><span class="sxs-lookup"><span data-stu-id="e67e9-193">Get all the signed-in user's events that start after 7/1/2017.</span></span> | [`https://graph.microsoft.com/v1.0/me/events?$filter=start/dateTime ge '2017-07-01T08:00'`](https://developer.microsoft.com/graph/graph-explorer?request=me/events?$filter=start/dateTime+ge+'2017-07-01T08:00'&method=GET&version=v1.0) 
| <span data-ttu-id="e67e9-194">Obtener todos los correos electrónicos de una dirección específica recibidos por el usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="e67e9-194">Get all emails from a specific address received by the signed-in user.</span></span> | [`https://graph.microsoft.com/v1.0/me/messages?$filter=from/emailAddress/address eq 'someuser@example.com'`](https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$filter=from/emailAddress/address+eq+'someuser@.com'&method=GET&version=v1.0) 
| <span data-ttu-id="e67e9-195">Obtener todos los correos electrónicos recibidos en abril de 2017 por el usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="e67e9-195">Get all emails received by the signed-in user in April 2017.</span></span> | [`https://graph.microsoft.com/v1.0/me/mailFolders/inbox/messages?$filter=ReceivedDateTime ge 2017-04-01 and receivedDateTime lt 2017-05-01`](https://developer.microsoft.com/graph/graph-explorer?request=me/mailFolders/inbox/messages?$filter=ReceivedDateTime+ge+2017-04-01+and+receivedDateTime+lt+2017-05-01&method=GET&version=v1.0) 
| <span data-ttu-id="e67e9-196">Obtener todos los correos electrónicos no leídos en la Bandeja de entrada del usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="e67e9-196">Get all unread mail in the signed-in user's Inbox.</span></span> | [`https://graph.microsoft.com/v1.0/me/mailFolders/inbox/messages?$filter=isRead eq false`](https://developer.microsoft.com/graph/graph-explorer?request=me/mailFolders/inbox/messages?$filter=isRead+eq+false&method=GET&version=v1.0) 
| <span data-ttu-id="e67e9-197">Enumerar todos los grupos de Office 365 de una organización.</span><span class="sxs-lookup"><span data-stu-id="e67e9-197">List all Office 365 groups in an organization.</span></span> | [`https://graph.microsoft.com/v1.0/groups?$filter=groupTypes/any(c:c+eq+'Unified')`](https://developer.microsoft.com/graph/graph-explorer?request=groups?$filter=groupTypes/any(c:c+eq+'Unified')&method=GET&version=v1.0) 

> <span data-ttu-id="e67e9-p115">**Nota:** Los operadores `$filter` siguientes no se admiten para recursos de Azure AD: `ne`, `gt`, `ge`, `lt`, `le` y `not`. El operador de cadena `contains` actualmente no se admite en ningún recurso de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="e67e9-p115">**Note:** The following `$filter` operators are not supported for Azure AD resources:  `ne`, `gt`, `ge`, `lt`, `le`, and `not`. The `contains` string operator is currently not supported on any Microsoft Graph resources.</span></span>

## <a name="format-parameter"></a><span data-ttu-id="e67e9-200">parámetro de formato</span><span class="sxs-lookup"><span data-stu-id="e67e9-200">format parameter</span></span>

<span data-ttu-id="e67e9-201">Use el parámetro de consulta `$format` para especificar el formato de medio de los elementos devueltos desde Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="e67e9-201">Use the `$format` query parameter to specify the media format of the items returned from Microsoft Graph.</span></span>

<span data-ttu-id="e67e9-202">Por ejemplo, la solicitud siguiente devuelve los usuarios de la organización en formato JSON:</span><span class="sxs-lookup"><span data-stu-id="e67e9-202">For example, the following request returns the users in the organization in the json format:</span></span>

```http
GET https://graph.microsoft.com/v1.0/users?$format=json
```

<span data-ttu-id="e67e9-203">[Probar en el Probador de Graph][format-example]</span><span class="sxs-lookup"><span data-stu-id="e67e9-203">[Try in Graph Explorer][format-example]</span></span>

> <span data-ttu-id="e67e9-204">**Nota**: El parámetro de consulta `$format` admite varios formatos, como atom, xml y json, pero puede que no todos los formatos devuelvan resultados.</span><span class="sxs-lookup"><span data-stu-id="e67e9-204">**Note:** The `$format` query parameter supports a number of formats (for example, atom, xml, and json) but results may not be returned in all formats.</span></span>

## <a name="orderby-parameter"></a><span data-ttu-id="e67e9-205">parámetro orderby</span><span class="sxs-lookup"><span data-stu-id="e67e9-205">orderby parameter</span></span>

<span data-ttu-id="e67e9-206">Use el parámetro de consulta `$orderby` para especificar el criterio de ordenación de los elementos devueltos desde Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="e67e9-206">Use the `$orderby` query parameter to specify the sort order of the items returned from Microsoft Graph.</span></span>

<span data-ttu-id="e67e9-207">Por ejemplo, la solicitud siguiente devuelve los usuarios de la organización ordenados por su nombre para mostrar:</span><span class="sxs-lookup"><span data-stu-id="e67e9-207">For example, the following request returns the users in the organization ordered by their display name:</span></span>

```http
GET https://graph.microsoft.com/v1.0/users?$orderby=displayName
```
<span data-ttu-id="e67e9-208">[Probar en el Probador de Graph][orderby-example]</span><span class="sxs-lookup"><span data-stu-id="e67e9-208">[Try in Graph Explorer][orderby-example]</span></span>

<span data-ttu-id="e67e9-p116">También puede ordenar por entidades de tipo complejo. La solicitud siguiente obtiene los mensajes y los ordena por el campo **address** de la propiedad **from**, que es del tipo complejo **emailAddress**:</span><span class="sxs-lookup"><span data-stu-id="e67e9-p116">You can also sort by complex type entities. The following request gets messages and sorts them by the **address** field of the **from** property, which is of the complex type **emailAddress**:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/messages?$orderby=from/emailAddress/address
```
<span data-ttu-id="e67e9-211">
  [Probar en el Probador de Graph](https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$orderby=from/emailAddress/address&method=GET&version=v1.0)</span><span class="sxs-lookup"><span data-stu-id="e67e9-211">[Try in Graph Explorer](https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$orderby=from/emailAddress/address&method=GET&version=v1.0)</span></span>

<span data-ttu-id="e67e9-212">Para ordenar los resultados en orden ascendente o descendente, anexe `asc` o `desc` al nombre del campo, separado por un espacio. Por ejemplo, `?$orderby=name%20desc`.</span><span class="sxs-lookup"><span data-stu-id="e67e9-212">To sort the results in ascending or descending order, append either `asc` or `desc` to the field name, separated by a space; for example, `?$orderby=name%20desc`.</span></span>

<span data-ttu-id="e67e9-213">Con algunas API se pueden ordenar los resultados por varias propiedades.</span><span class="sxs-lookup"><span data-stu-id="e67e9-213">With some APIs, you can order results on multiple properties.</span></span> <span data-ttu-id="e67e9-214">Por ejemplo, en la siguiente solicitud se ordenan los mensajes en la Bandeja de entrada del usuario; primero por el nombre de la persona que lo envió en orden descendente (de la Z a la A) y, después, por asunto en orden ascendente (el valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="e67e9-214">For example, the following request orders the messages in the user's Inbox, first by the name of the person who sent it in descending order (Z to A), and then by subject in ascending order (default).</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/mailFolders/Inbox/messages?$orderby=from/emailAddress/name desc,subject
```

<span data-ttu-id="e67e9-215">
  [Probar en el Probador de Graph](https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$orderby=from/emailAddress/name%20desc,subject&method=GET&version=v1.0)</span><span class="sxs-lookup"><span data-stu-id="e67e9-215">[Try in Graph Explorer](https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$orderby=from/emailAddress/name%20desc,subject&method=GET&version=v1.0)</span></span>

<span data-ttu-id="e67e9-216">Si especifica $filter, el servidor deducirá un criterio de ordenación para los resultados.</span><span class="sxs-lookup"><span data-stu-id="e67e9-216">When you specify $filter the server will infer a sort order for the results.</span></span> <span data-ttu-id="e67e9-217">Si usa tanto `$orderby` como `$filter`, porque el servidor siempre deduce un criterio de ordenación para los resultados de un `$filter`, las propiedades del `$filter` deben estar primero en `$orderby`, antes que cualquier otra propiedad y deben estar en el orden en el que aparecen en el parámetro `$filter`.</span><span class="sxs-lookup"><span data-stu-id="e67e9-217">If you use both `$orderby` and `$filter`, because the server always infers a sort order for the results of a `$filter`, the properties in the `$filter` must be listed first in the `$orderby` before any other properties, and they must be listed in the order that they appear in the `$filter` parameter.</span></span> 

<span data-ttu-id="e67e9-218">En el siguiente ejemplo, se muestra una consulta filtrada por las propiedades **subject** y **importance**, y después ordenada por las propiedades **subject**, **importance** y **receivedDateTime** en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="e67e9-218">The following example shows a query filtered by the **subject** and **importance** properties, and then sorted by the **subject**, **importance**, and **receivedDateTime** properties in descending order.</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/messages?$filter=Subject eq 'welcome' and importance eq 'normal'&$orderby=subject,importance,receivedDateTime desc
```

<span data-ttu-id="e67e9-219">
  [Probar en el Probador de Graph](https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$filter=subject%20eq%20%27welcome%27%20and%20importance%20eq%20%27normal%27%20&$orderby=subject,importance,receivedDateTime%20desc&method=GET&version=v1.0)</span><span class="sxs-lookup"><span data-stu-id="e67e9-219">[Try in Graph Explorer](https://developer.microsoft.com/graph/graph-explorer?request=me/messages?$filter=subject%20eq%20%27welcome%27%20and%20importance%20eq%20%27normal%27%20&$orderby=subject,importance,receivedDateTime%20desc&method=GET&version=v1.0)</span></span>

 > <span data-ttu-id="e67e9-220">**Nota:** Con recursos de Azure AD que se derivan de [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-1.0), como [user](/graph/api/resources/user?view=graph-rest-1.0) y [group](/graph/api/resources/group?view=graph-rest-1.0), no se puede combinar `$orderby` con expresiones`$filter`.</span><span class="sxs-lookup"><span data-stu-id="e67e9-220">**Note:** With Azure AD resources that derive from [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-1.0), like [user](/graph/api/resources/user?view=graph-rest-1.0) and [group](/graph/api/resources/group?view=graph-rest-1.0), you cannot combine `$orderby` with `$filter` expressions.</span></span> 

## <a name="search-parameter"></a><span data-ttu-id="e67e9-221">parámetro de búsqueda</span><span class="sxs-lookup"><span data-stu-id="e67e9-221">search parameter</span></span>

<span data-ttu-id="e67e9-222">Use el parámetro de consulta `$search` para restringir los resultados de una solicitud para que coincidan con un criterio de búsqueda</span><span class="sxs-lookup"><span data-stu-id="e67e9-222">Use the `$search` query parameter to restrict the results of a request to match a search criterion.</span></span>

> <span data-ttu-id="e67e9-p119">**Nota:** Actualmente **solo** se pueden buscar las colecciones [message](/graph/api/resources/message?view=graph-rest-1.0) y [person](/graph/api/resources/person?view=graph-rest-1.0). Una solicitud `$search` devuelve hasta 250 resultados. No puede usar [`$filter`](#filter-parameter) o [`$orderby`](#orderby-parameter) en una solicitud de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e67e9-p119">**Note:** You can currently search **only** [message](/graph/api/resources/message?view=graph-rest-1.0) and [person](/graph/api/resources/person?view=graph-rest-1.0) collections. A `$search` request returns up to 250 results. You cannot use [`$filter`](#filter-parameter) or [`$orderby`](#orderby-parameter) in a search request.</span></span>

### <a name="using-search-on-message-collections"></a><span data-ttu-id="e67e9-226">Uso de $search en colecciones de mensajes</span><span class="sxs-lookup"><span data-stu-id="e67e9-226">Using $search on message collections</span></span>

<span data-ttu-id="e67e9-227">Puede buscar mensajes con un valor en las propiedades de los mensajes específicos.</span><span class="sxs-lookup"><span data-stu-id="e67e9-227">You can search messages based on a value in specific message properties.</span></span> <span data-ttu-id="e67e9-228">Los resultados de la búsqueda se ordenan por la fecha y la hora en que se ha enviado el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e67e9-228">The results of the search are sorted by the date and time that the message was sent.</span></span>

<span data-ttu-id="e67e9-229">Si realiza una búsqueda en mensajes y especifica solo un valor sin las propiedades de mensaje específicas, la búsqueda se lleva a cabo con las propiedades de búsqueda predeterminadas de **from**, **subject** y **body**.</span><span class="sxs-lookup"><span data-stu-id="e67e9-229">If you do a search on messages and specify only a value without specific message properties, the search is carried out on the default search properties of **from**, **subject**, and **body**.</span></span>

<span data-ttu-id="e67e9-230">En el ejemplo siguiente, se devuelven todos los mensajes del buzón del usuario que ha iniciado sesión que contienen la palabra "pizza" en cualquiera de las tres propiedades de búsqueda predeterminadas:</span><span class="sxs-lookup"><span data-stu-id="e67e9-230">The following example returns all messages in the signed-in user's Inbox that contains "pizza" in any of the three default search properties:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/messages?$search="pizza"
```

<span data-ttu-id="e67e9-231">[Probar en el Probador de Graph][search-example]</span><span class="sxs-lookup"><span data-stu-id="e67e9-231">[Try in Graph Explorer][search-example]</span></span>

<span data-ttu-id="e67e9-232">Como alternativa, puede buscar mensajes especificando los nombres de propiedades de mensaje en la tabla siguiente, que se reconocen por la sintaxis de la consulta de palabras clave (KQL).</span><span class="sxs-lookup"><span data-stu-id="e67e9-232">Alternatively, you can search messages by specifying message property names in the following table, that are recognized by the Keyword Query Language (KQL) syntax.</span></span> <span data-ttu-id="e67e9-233">Estos nombres de propiedad corresponden a las propiedades que se definen en la entidad de **mensaje** de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="e67e9-233">These property names correspond to properties defined in the **message** entity of Microsoft Graph.</span></span> <span data-ttu-id="e67e9-234">Outlook y otras aplicaciones de Office 365, como SharePoint admiten la sintaxis KQL, proporciona la comodidad de un dominio de detección común para los almacenes de datos.</span><span class="sxs-lookup"><span data-stu-id="e67e9-234">Outlook and other Office 365 applications such as SharePoint support KQL syntax, providing the convenience of a common discovery domain for their data stores.</span></span>


| <span data-ttu-id="e67e9-235">Propiedades del correo electrónico que permiten búsquedas</span><span class="sxs-lookup"><span data-stu-id="e67e9-235">Searchable email property</span></span>                | <span data-ttu-id="e67e9-236">Descripción</span><span class="sxs-lookup"><span data-stu-id="e67e9-236">Description</span></span> | <span data-ttu-id="e67e9-237">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e67e9-237">Example</span></span> 
|:-------------------------|:------------|:---------|
| <span data-ttu-id="e67e9-238">**attachment**</span><span class="sxs-lookup"><span data-stu-id="e67e9-238">**attachment**</span></span>           | <span data-ttu-id="e67e9-239">Los nombres de los archivos adjuntos a un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e67e9-239">The names of files attached to an email message.</span></span>|[`me/messages?$search="attachment:api-catalog.md"`][search-att-example]
| <span data-ttu-id="e67e9-240">**bcc**</span><span class="sxs-lookup"><span data-stu-id="e67e9-240">**bcc**</span></span>           | <span data-ttu-id="e67e9-241">El campo **bcc** de un mensaje de correo electrónico, especificado como una dirección SMTP, alias o nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="e67e9-241">The **bcc** field of an email message, specified as an SMTP address, display name, or alias.</span></span>|[`me/messages?$search="bcc:samanthab@contoso.com"&$select=subject,bccRecipients`][search-bcc-example]
| <span data-ttu-id="e67e9-242">**body**</span><span class="sxs-lookup"><span data-stu-id="e67e9-242">**body**</span></span>           | <span data-ttu-id="e67e9-243">El cuerpo de un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e67e9-243">The body of an email message.</span></span>|[`me/messages?$search="body:excitement"`][search-body-example]
| <span data-ttu-id="e67e9-244">**cc**</span><span class="sxs-lookup"><span data-stu-id="e67e9-244">**cc**</span></span>           | <span data-ttu-id="e67e9-245">El campo **cc** de un mensaje de correo electrónico, especificado como una dirección SMTP, alias o nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="e67e9-245">The **cc** field of an email message, specified as an SMTP address, display name, or alias.</span></span>|[`me/messages?$search="cc:danas"&$select=subject,ccRecipients`][search-cc-example]
| <span data-ttu-id="e67e9-246">**from**</span><span class="sxs-lookup"><span data-stu-id="e67e9-246">**from**</span></span>           | <span data-ttu-id="e67e9-247">El remitente de un mensaje de correo electrónico, especificado como una dirección SMTP, alias o nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="e67e9-247">The sender of an email message, specified as an SMTP address, display name, or alias.</span></span>|[`me/messages?$search="from:randiw"&$select=subject,from`][search-from-example]
| <span data-ttu-id="e67e9-248">**hasAttachment**</span><span class="sxs-lookup"><span data-stu-id="e67e9-248">**hasAttachment**</span></span> | <span data-ttu-id="e67e9-249">Verdadero si un mensaje contiene datos adjuntos que no son un archivo adjunto en línea, falso en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e67e9-249">True if an email message contains an attachment that is not an inline attachment, false otherwise.</span></span> |[`me/messages?$search="hasAttachments=true"`][search-from-example]
| <span data-ttu-id="e67e9-250">**importance**</span><span class="sxs-lookup"><span data-stu-id="e67e9-250">**importance**</span></span>           | <span data-ttu-id="e67e9-251">La importancia de un mensaje de correo electrónico, que un remitente puede especificar al enviar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="e67e9-251">The importance of an email message, which a sender can specify when sending a message.</span></span> <span data-ttu-id="e67e9-252">Los valores posibles son`low`, `medium` o `high`.</span><span class="sxs-lookup"><span data-stu-id="e67e9-252">The possible values are `low`, `medium`, or `high`.</span></span>|[`me/messages?$search="importance:high"&$select=subject,importance`][search-imp-example]
| <span data-ttu-id="e67e9-253">**kind**</span><span class="sxs-lookup"><span data-stu-id="e67e9-253">**kind**</span></span>           | <span data-ttu-id="e67e9-254">El tipo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="e67e9-254">The type of message.</span></span> <span data-ttu-id="e67e9-255">Los valores posibles son `contacts`, `docs`, `email`, `faxes`, `im`, `journals`, `meetings`, `notes`, `posts`, `rssfeeds`, `tasks` o `voicemail`.</span><span class="sxs-lookup"><span data-stu-id="e67e9-255">The possible values are `contacts`, `docs`, `email`, `faxes`, `im`, `journals`, `meetings`, `notes`, `posts`, `rssfeeds`, `tasks`, or `voicemail`.</span></span>|[`me/messages?$search="kind:voicemail"`][search-kind-example]
| <span data-ttu-id="e67e9-256">**participants**</span><span class="sxs-lookup"><span data-stu-id="e67e9-256">**participants**</span></span>           | <span data-ttu-id="e67e9-257">Los campos **from**, **to**, **cc** y **bcc** de un mensaje de correo electrónico, especificados como una dirección SMTP, alias o nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="e67e9-257">The **from**, **to**, **cc**, and **bcc** fields of an email message, specified as an SMTP address, display name, or alias.</span></span>|[`me/messages?$search="participants:danas"`][search-part-example]
| <span data-ttu-id="e67e9-258">**received**</span><span class="sxs-lookup"><span data-stu-id="e67e9-258">**received**</span></span>           | <span data-ttu-id="e67e9-259">La fecha en la que un destinatario recibió un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e67e9-259">The date that an email message was received by a recipient.</span></span>|[`me/messages?$search="received:07/23/2018"&$select=subject,receivedDateTime`][search-rcvd-example]
| <span data-ttu-id="e67e9-260">**recipients**</span><span class="sxs-lookup"><span data-stu-id="e67e9-260">**recipients**</span></span>           | <span data-ttu-id="e67e9-261">Los campos**to**, **cc** y **bcc** especificados como una dirección SMTP, alias o nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="e67e9-261">The **to**, **cc**, and **bcc** fields of an email meesage, specified as an SMTP address, display name, or alias.</span></span>|[`me/messages?$search="recipients:randiq"&$select=subject,toRecipients,ccRecipients,bccRecipients`][search-rcpts-example]
| <span data-ttu-id="e67e9-262">**sent**</span><span class="sxs-lookup"><span data-stu-id="e67e9-262">**sent**</span></span>           | <span data-ttu-id="e67e9-263">La fecha en la que un remitente envió un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e67e9-263">The date that an email message was sent by the sender.</span></span>|[`me/messages?$search="sent:07/23/2018"&$select=subject,sentDateTime`][search-sent-example]
| <span data-ttu-id="e67e9-264">**size**</span><span class="sxs-lookup"><span data-stu-id="e67e9-264">**size**</span></span>           | <span data-ttu-id="e67e9-265">El tamaño de un elemento, en bytes.</span><span class="sxs-lookup"><span data-stu-id="e67e9-265">The size of an item in bytes.</span></span>|[`me/messages?$search="size:1..500000"`][search-size-example]
| <span data-ttu-id="e67e9-266">**subject**</span><span class="sxs-lookup"><span data-stu-id="e67e9-266">**subject**</span></span>           | <span data-ttu-id="e67e9-267">El texto en la línea de asunto de un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e67e9-267">The text in the subject line of an email message.</span></span> <span data-ttu-id="e67e9-268">.</span><span class="sxs-lookup"><span data-stu-id="e67e9-268">.</span></span>|[`me/messages?$search="subject:has"&$select=subject`][search-sbj-example]
| <span data-ttu-id="e67e9-269">**to**</span><span class="sxs-lookup"><span data-stu-id="e67e9-269">**to**</span></span>           | <span data-ttu-id="e67e9-270">El campo **to** de un mensaje de correo electrónico, especificado como una dirección SMTP, alias o nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="e67e9-270">The **to** field of an email message, specified as an SMTP address, display name, or alias.</span></span>|[`me/messages?$search="to:randiw"&$select=subject,toRecipients`][search-to-example]


<span data-ttu-id="e67e9-271">Para obtener más información sobre las propiedades de correo electrónico que permiten búsquedas, la sintaxis KQL, los operadores compatibles y las sugerencias de búsqueda, vea los artículos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e67e9-271">For more information about searchable email properties, KQL syntax, supported operators, and tips on searching, see the following articles:</span></span>

- <span data-ttu-id="e67e9-272">[Propiedades que permiten búsquedas en Exchange](https://docs.microsoft.com/es-ES/Exchange/policy-and-compliance/ediscovery/message-properties-and-search-operators#searchable-properties-in-exchange).</span><span class="sxs-lookup"><span data-stu-id="e67e9-272">[Searchable properties in Exchange](https://docs.microsoft.com/es-ES/Exchange/policy-and-compliance/ediscovery/message-properties-and-search-operators#searchable-properties-in-exchange).</span></span>

- [<span data-ttu-id="e67e9-273">Referencia de la sintaxis del lenguaje de consultas de palabras clave (KQL)</span><span class="sxs-lookup"><span data-stu-id="e67e9-273">Keyword Query Language (KQL) syntax reference</span></span>](https://docs.microsoft.com/es-ES/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference)

- <span data-ttu-id="e67e9-274">
  [Propiedades de mensajes y operadores de búsqueda para eDiscovery local en Exchange 2016](https://technet.microsoft.com/en-us/library/dn774955(v=exchg.160).aspx)</span><span class="sxs-lookup"><span data-stu-id="e67e9-274">[Message properties and search operators for In-Place eDiscovery in Exchange 2016](https://technet.microsoft.com/en-us/library/dn774955(v=exchg.160).aspx)</span></span>

### <a name="using-search-on-person-collections"></a><span data-ttu-id="e67e9-275">Uso de $search en colecciones de usuarios</span><span class="sxs-lookup"><span data-stu-id="e67e9-275">Using $search on person collections</span></span>

<span data-ttu-id="e67e9-p125">Puede usar la API de contactos de Microsoft Graph para recuperar los contactos más relevantes para un usuario. La relevancia viene determinada por las relaciones empresariales y los patrones de comunicación y colaboración del usuario. La API de contactos admite el parámetro de consulta `$search`.</span><span class="sxs-lookup"><span data-stu-id="e67e9-p125">You can use the Microsoft Graph People API to retrieve the people who are most relevant to a user. Relevance is determined by the user’s communication and collaboration patterns and business relationships. The People API supports the `$search` query parameter.</span></span>

<span data-ttu-id="e67e9-279">Las búsquedas de contactos se realizan en las propiedades **displayName** y **emailAddress** del recurso [person](/graph/api/resources/person?view=graph-rest-1.0).</span><span class="sxs-lookup"><span data-stu-id="e67e9-279">Searches on people occur on both the **displayName** and **emailAddress** properties of the [person](/graph/api/resources/person?view=graph-rest-1.0) resource.</span></span>

<span data-ttu-id="e67e9-280">La solicitud siguiente busca una persona llamada "Irene McGowen" en las propiedades **displayName** y **emailAddress** de todos los miembros de la colección **people** del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="e67e9-280">The following request does a search for a person named "Irene McGowen" in the **displayName** and **emailAddress** properties in each person in the **people** collection of the signed-in user.</span></span> <span data-ttu-id="e67e9-281">Dado que existe una persona llamada "Irene McGowan" relevante para el usuario que ha iniciado sesión, se devuelve la información de "Irene McGowan".</span><span class="sxs-lookup"><span data-stu-id="e67e9-281">Because a person named "Irene McGowan" is relevant to the signed-in user, the information for "Irene McGowan" is returned.</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/people/?$search="Irene McGowen"
```

<span data-ttu-id="e67e9-282">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e67e9-282">The following example shows the response.</span></span> 

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

<span data-ttu-id="e67e9-283">Para más información sobre la API de contactos, vea [Obtener información sobre contactos relevantes](./people-example.md#search-people).</span><span class="sxs-lookup"><span data-stu-id="e67e9-283">To learn more about the People API, see [Get information about relevant people](./people-example.md#search-people).</span></span>  

## <a name="select-parameter"></a><span data-ttu-id="e67e9-284">parámetro de selección</span><span class="sxs-lookup"><span data-stu-id="e67e9-284">select parameter</span></span>

<span data-ttu-id="e67e9-285">Use el parámetro de consulta `$select` para devolver un conjunto de propiedades diferente al predeterminado para un recurso individual o una colección de recursos.</span><span class="sxs-lookup"><span data-stu-id="e67e9-285">Use the `$select` query parameter to return a set of properties that are different than the default set for an individual resource or a collection of resources.</span></span> <span data-ttu-id="e67e9-286">Con $select, puede especificar un subconjunto o un superconjunto de las propiedades predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="e67e9-286">With $select, you can specify a subset or a superset of the default properties.</span></span>

<span data-ttu-id="e67e9-287">Por ejemplo, al recuperar los mensajes del usuario que ha iniciado sesión, puede especificar que solo se devuelvan las propiedades **from** y **subject**:</span><span class="sxs-lookup"><span data-stu-id="e67e9-287">For example, when retrieving the messages of the signed-in user, you can specify that only the **from** and **subject** properties be returned:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/messages?$select=from,subject
```

<span data-ttu-id="e67e9-288">[Probar en el Probador de Graph][select-example]</span><span class="sxs-lookup"><span data-stu-id="e67e9-288">[Try in Graph Explorer][select-example]</span></span>

> <span data-ttu-id="e67e9-289">**Importante:** En general, se recomienda usar `$select` para limitar las propiedades devueltas por una consulta a las necesarias para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e67e9-289">**Important:** In general, we recommend that you use `$select` to limit the properties returned by a query to those needed by your app.</span></span> <span data-ttu-id="e67e9-290">Esto es especialmente cierto para las consultas que potencialmente pueden devolver un conjunto de resultados grande.</span><span class="sxs-lookup"><span data-stu-id="e67e9-290">This is especially true of queries that might potentially return a large result set.</span></span> <span data-ttu-id="e67e9-291">Limitar las propiedades devueltas en cada fila reducirá la carga en la red y ayudará a mejorar el rendimiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e67e9-291">Limiting the properties returned in each row will reduce network load and help improve your app's performance.</span></span>
>
> <span data-ttu-id="e67e9-p129">En `v1.0`, algunos recursos de Azure AD que se derivan de [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-1.0), como [user](/graph/api/resources/user?view=graph-rest-1.0) y [group](/graph/api/resources/group?view=graph-rest-1.0), devuelven un subconjunto predeterminado limitado de propiedades en las operaciones de lectura. Para estos recursos, debe usar `$select` para devolver propiedades fuera el conjunto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e67e9-p129">In `v1.0`, some Azure AD resources that derive from [directoryObject](/graph/api/resources/directoryobject?view=graph-rest-1.0), like [user](/graph/api/resources/user?view=graph-rest-1.0) and [group](/graph/api/resources/group?view=graph-rest-1.0), return a limited, default subset of properties on reads. For these resources, you must use `$select` to return properties outside of the default set.</span></span>  

## <a name="skip-parameter"></a><span data-ttu-id="e67e9-294">parámetros de omisión</span><span class="sxs-lookup"><span data-stu-id="e67e9-294">skip parameter</span></span>

<span data-ttu-id="e67e9-p130">Use el parámetro de consulta `$skip` para establecer el número de elementos que se omitirán al inicio de una colección. Por ejemplo, la solicitud siguiente devuelve eventos para el usuario ordenados por fecha de creación, empezando por el evento 21 de la colección:</span><span class="sxs-lookup"><span data-stu-id="e67e9-p130">Use the `$skip` query parameter to set the number of items to skip at the start of a collection. For example, the following request returns events for the user sorted by date created, starting with the 21st event in the collection:</span></span>

```http
GET  https://graph.microsoft.com/v1.0/me/events?$orderby=createdDateTime&$skip=20
```
<span data-ttu-id="e67e9-297">[Probar en el Probador de Graph][skip-example]</span><span class="sxs-lookup"><span data-stu-id="e67e9-297">[Try in Graph Explorer][skip-example]</span></span>

> <span data-ttu-id="e67e9-298">**Nota:** En algunas API de Microsoft Graph, como Correo y Calendario de Outlook (**message**, **event** y **calendar**), se usa `$skip` para implementar la paginación.</span><span class="sxs-lookup"><span data-stu-id="e67e9-298">**Note:** Some Microsoft Graph APIs, like Outlook Mail and Calendars (**message**, **event**, and **calendar**), use `$skip` to implement paging.</span></span> <span data-ttu-id="e67e9-299">Cuando los resultados de una consulta ocupen varias páginas, estas API devolverán una propiedad `@odata:nextLink` con una dirección URL que contendrá un parámetro `$skip`.</span><span class="sxs-lookup"><span data-stu-id="e67e9-299">When results of a query span multiple pages, these APIs will return an `@odata:nextLink` property with a URL that contains a `$skip` parameter.</span></span> <span data-ttu-id="e67e9-300">Puede usar esta dirección URL para devolver la siguiente página de resultados.</span><span class="sxs-lookup"><span data-stu-id="e67e9-300">You can use this URL to return the next page of results.</span></span> <span data-ttu-id="e67e9-301">Para obtener más información, vea [Paginación](./paging.md).</span><span class="sxs-lookup"><span data-stu-id="e67e9-301">To learn more, see [Paging](./paging.md).</span></span>

## <a name="skiptoken-parameter"></a><span data-ttu-id="e67e9-302">parámetro skipToken</span><span class="sxs-lookup"><span data-stu-id="e67e9-302">skipToken parameter</span></span>

<span data-ttu-id="e67e9-p132">Algunas consultas devuelven varias páginas de datos debido a la paginación del servidor o al uso del parámetro [`$top`](#top-parameter) para limitar el tamaño de página de la respuesta. Muchas API de Microsoft Graph usan el parámetro de consulta `skipToken` para hacer referencia a las páginas siguientes del resultado. El parámetro `$skiptoken` contiene un token opaco que hace referencia a la siguiente página de resultados y se devuelve en la dirección URL proporcionada en la propiedad `@odata.nextLink` en la respuesta. Para obtener más información, vea [Paginación](./paging.md).</span><span class="sxs-lookup"><span data-stu-id="e67e9-p132">Some requests return multiple pages of data either due to server-side paging or due to the use of the [`$top`](#top-parameter) parameter to limit the page size of the response. Many Microsoft Graph APIs use the `skipToken` query parameter to reference subsequent pages of the result. The `$skiptoken` parameter contains an opaque token that references the next page of results and is returned in the URL provided in the `@odata.nextLink` property in the response. To learn more, see [Paging](./paging.md).</span></span>


## <a name="top-parameter"></a><span data-ttu-id="e67e9-307">parámetro superior</span><span class="sxs-lookup"><span data-stu-id="e67e9-307">top parameter</span></span>

<span data-ttu-id="e67e9-308">Use el parámetro de consulta `$top` para especificar el tamaño de página del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="e67e9-308">Use the `$top` query parameter to specify the page size of the result set.</span></span> 

<span data-ttu-id="e67e9-309">Si quedan más elementos en el conjunto de resultados, el cuerpo de la respuesta contendrá un parámetro `@odata.nextLink`.</span><span class="sxs-lookup"><span data-stu-id="e67e9-309">If more items remain in the result set, the response body will contain an `@odata.nextLink` parameter.</span></span> <span data-ttu-id="e67e9-310">Este parámetro contiene una dirección URL que se puede usar para obtener la siguiente página de resultados.</span><span class="sxs-lookup"><span data-stu-id="e67e9-310">This parameter contains a URL that you can use to get the next page of results.</span></span> <span data-ttu-id="e67e9-311">Para obtener más información, vea [Paginación](./paging.md).</span><span class="sxs-lookup"><span data-stu-id="e67e9-311">To learn more, see [Paging](./paging.md).</span></span> 

<span data-ttu-id="e67e9-312">Por ejemplo, la solicitud siguiente devuelve los cinco primeros mensajes en el buzón del usuario:</span><span class="sxs-lookup"><span data-stu-id="e67e9-312">For example, the following request returns the first five messages in the user's mailbox:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/messages?$top=5
```

<span data-ttu-id="e67e9-313">[Probar en el Probador de Graph][top-example]</span><span class="sxs-lookup"><span data-stu-id="e67e9-313">[Try in Graph Explorer][top-example]</span></span>


## <a name="error-handling-for-query-parameters"></a><span data-ttu-id="e67e9-314">Control de errores para parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="e67e9-314">Error handling for query parameters</span></span>

<span data-ttu-id="e67e9-p134">Algunas solicitudes devolverán un mensaje de error si no se admite un parámetro de consulta especificado. Por ejemplo, no se puede usar `$expand` en la relación `user/photo`.</span><span class="sxs-lookup"><span data-stu-id="e67e9-p134">Some requests will return an error message if a specified query parameter is not supported. For example, you cannot use `$expand` on the `user/photo` relationship.</span></span> 

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

<span data-ttu-id="e67e9-317">Pero es importante tener en cuenta que los parámetros de consulta especificados en una solicitud pueden devolver un error silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="e67e9-317">However, it is important to note that query parameters specified in a request might fail silently.</span></span> <span data-ttu-id="e67e9-318">Esto puede suceder con parámetros de consulta no admitidos, así como con combinaciones no compatibles de parámetros de consulta.</span><span class="sxs-lookup"><span data-stu-id="e67e9-318">This can be true for unsupported query parameters as well as for unsupported combinations of query parameters.</span></span> <span data-ttu-id="e67e9-319">En estos casos, debe examinar los datos devueltos por la solicitud para determinar si los parámetros de consulta especificados tuvieron el efecto previsto.</span><span class="sxs-lookup"><span data-stu-id="e67e9-319">In these cases, you should examine the data returned by the request to determine whether the query parameters you specified had the desired effect.</span></span> 

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

