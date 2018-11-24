# <a name="get-singlevaluelegacyextendedproperty"></a><span data-ttu-id="4e3fe-101">Obtener singleValueLegacyExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="4e3fe-101">Get singleValueLegacyExtendedProperty</span></span>

<span data-ttu-id="4e3fe-102">Puede expandir una única instancia de recursos con una propiedad extendida determinada o una colección de instancias de recursos que incluya propiedades extendidas que coinciden con un filtro.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-102">You can get a single resource instance expanded with a specific extended property, or a collection of resource instances that include extended properties matching a filter.</span></span>

<span data-ttu-id="4e3fe-103">El uso del parámetro de consulta `$expand` le permite expandir la instancia de recursos especificada con una propiedad extendida específica.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-103">Using the query parameter `$expand` allows you to get the specified resource instance expanded with a specific extended property.</span></span> <span data-ttu-id="4e3fe-104">Use un operador `$filter` y `eq` en la propiedad **id** para especificar las propiedades extendidas.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-104">Use a `$filter` and `eq` operator on the **id** property to specify the extended property.</span></span> <span data-ttu-id="4e3fe-105">Actualmente, esta es la única forma de obtener el objeto [singleValueLegacyExtendedProperty](../resources/singleValueLegacyExtendedProperty.md) que representa una propiedad extendida.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-105">This is currently the only way to get the [singleValueLegacyExtendedProperty](../resources/singleValueLegacyExtendedProperty.md) object that represents an extended property.</span></span> 

<span data-ttu-id="4e3fe-106">Para obtener las instancias de recursos que tengan ciertas propiedades extendidas, use el parámetro de consulta `$filter` y aplique un operador `eq` en la propiedad **id**.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-106">To get resource instances that have certain extended properties, use the `$filter` query parameter and apply an `eq` operator on the **id** property.</span></span> <span data-ttu-id="4e3fe-107">Además, para las propiedades extendidas numéricas, aplique uno de los siguientes operadores en la propiedad **value**: `eq`, `ne`,`ge`, `gt`, `le` o `lt`.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-107">In addition, for numeric extended properties, apply one of the following operators on the **value** property: `eq`, `ne`,`ge`, `gt`, `le`, or `lt`.</span></span> <span data-ttu-id="4e3fe-108">Para las propiedades extendidas de tipo cadena, aplique un operador `contains`, `startswith`, `eq` o `ne` en **value**.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-108">For string-typed extended properties, apply a `contains`, `startswith`, `eq`, or `ne` operator on **value**.</span></span>

<span data-ttu-id="4e3fe-109">El filtro se aplica a todas las instancias del recurso en el buzón del usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-109">The filter is applied to all instances of the resource in the signed-in user's mailbox.</span></span> 

<span data-ttu-id="4e3fe-110">El filtrado del nombre de la cadena (`Name`) en el **id** de una propiedad extendida distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-110">Filtering the string name (`Name`) in the **id** of an extended property is case-sensitive.</span></span> <span data-ttu-id="4e3fe-111">El filtrado de la propiedad **value** de una propiedad extendida no distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-111">Filtering the **value** property of an extended property is case-insensitive.</span></span>

<span data-ttu-id="4e3fe-112">Se admiten los siguientes recursos de usuario:</span><span class="sxs-lookup"><span data-stu-id="4e3fe-112">The following user resources are supported:</span></span>

- [<span data-ttu-id="4e3fe-113">calendar</span><span class="sxs-lookup"><span data-stu-id="4e3fe-113">calendar</span></span>](../resources/calendar.md)
- [<span data-ttu-id="4e3fe-114">contact</span><span class="sxs-lookup"><span data-stu-id="4e3fe-114">contact</span></span>](../resources/contact.md)
- [<span data-ttu-id="4e3fe-115">contactFolder</span><span class="sxs-lookup"><span data-stu-id="4e3fe-115">contactFolder</span></span>](../resources/contactfolder.md) 
- [<span data-ttu-id="4e3fe-116">event</span><span class="sxs-lookup"><span data-stu-id="4e3fe-116">event</span></span>](../resources/event.md)
- [<span data-ttu-id="4e3fe-117">mailFolder</span><span class="sxs-lookup"><span data-stu-id="4e3fe-117">mailFolder</span></span>](../resources/mailfolder.md)
- [<span data-ttu-id="4e3fe-118">message</span><span class="sxs-lookup"><span data-stu-id="4e3fe-118">message</span></span>](../resources/message.md) 

<span data-ttu-id="4e3fe-119">También los siguientes recursos de grupo:</span><span class="sxs-lookup"><span data-stu-id="4e3fe-119">As well as the following group resources:</span></span>

- <span data-ttu-id="4e3fe-120">[calendar](../resources/calendar.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="4e3fe-120">group [calendar](../resources/calendar.md)</span></span>
- <span data-ttu-id="4e3fe-121">[event](../resources/event.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="4e3fe-121">group [event](../resources/event.md)</span></span>
- <span data-ttu-id="4e3fe-122">[post](../resources/post.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="4e3fe-122">group [post](../resources/post.md)</span></span> 

<span data-ttu-id="4e3fe-123">Consulte el artículo de [información general sobre las propiedades extendidas](../resources/extended-properties-overview.md) para obtener más información sobre cuándo usar las extensiones abiertas o las propiedades extendidas y cómo especificar las propiedades extendidas.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-123">See [Extended properties overview](../resources/extended-properties-overview.md) for more information about when to use open extensions or extended properties, and how to specify extended properties.</span></span>

## <a name="permissions"></a><span data-ttu-id="4e3fe-124">Permisos</span><span class="sxs-lookup"><span data-stu-id="4e3fe-124">Permissions</span></span>
<span data-ttu-id="4e3fe-125">Dependiendo del recurso está obteniendo la propiedad extendida desde y el permiso escriba (delegada o de la aplicación) se solicitud, el permiso especificado en la tabla siguiente es el requisito mínimo para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-125">Depending on the resource you're getting the extended property from and the permission type (delegated or application) you request, the permission specified in the following table is the minimum required to call this API.</span></span> <span data-ttu-id="4e3fe-126">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="4e3fe-126">To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="4e3fe-127">Recurso admitido</span><span class="sxs-lookup"><span data-stu-id="4e3fe-127">Supported resource</span></span> | <span data-ttu-id="4e3fe-128">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4e3fe-128">Delegated (work or school account)</span></span> | <span data-ttu-id="4e3fe-129">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4e3fe-129">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4e3fe-130">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4e3fe-130">Application</span></span> |
|:-----|:-----|:-----|:-----|
| [<span data-ttu-id="4e3fe-131">calendario</span><span class="sxs-lookup"><span data-stu-id="4e3fe-131">calendar</span></span>](../resources/calendar.md) | <span data-ttu-id="4e3fe-132">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="4e3fe-132">Calendars.Read</span></span> | <span data-ttu-id="4e3fe-133">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="4e3fe-133">Calendars.Read</span></span> | <span data-ttu-id="4e3fe-134">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="4e3fe-134">Calendars.Read</span></span> |
| [<span data-ttu-id="4e3fe-135">contact</span><span class="sxs-lookup"><span data-stu-id="4e3fe-135">contact</span></span>](../resources/contact.md) | <span data-ttu-id="4e3fe-136">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="4e3fe-136">Contacts.Read</span></span> | <span data-ttu-id="4e3fe-137">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="4e3fe-137">Contacts.Read</span></span> | <span data-ttu-id="4e3fe-138">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="4e3fe-138">Contacts.Read</span></span> |
| [<span data-ttu-id="4e3fe-139">contactFolder</span><span class="sxs-lookup"><span data-stu-id="4e3fe-139">contactFolder</span></span>](../resources/contactfolder.md) | <span data-ttu-id="4e3fe-140">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="4e3fe-140">Contacts.Read</span></span> | <span data-ttu-id="4e3fe-141">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="4e3fe-141">Contacts.Read</span></span> | <span data-ttu-id="4e3fe-142">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="4e3fe-142">Contacts.Read</span></span> |
| [<span data-ttu-id="4e3fe-143">event</span><span class="sxs-lookup"><span data-stu-id="4e3fe-143">event</span></span>](../resources/event.md) | <span data-ttu-id="4e3fe-144">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="4e3fe-144">Calendars.Read</span></span> | <span data-ttu-id="4e3fe-145">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="4e3fe-145">Calendars.Read</span></span> |  <span data-ttu-id="4e3fe-146">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="4e3fe-146">Calendars.Read</span></span>|
| <span data-ttu-id="4e3fe-147">[calendar](../resources/calendar.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="4e3fe-147">group [calendar](../resources/calendar.md)</span></span> | <span data-ttu-id="4e3fe-148">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="4e3fe-148">Group.Read.All</span></span> | <span data-ttu-id="4e3fe-149">No admitido</span><span class="sxs-lookup"><span data-stu-id="4e3fe-149">Not supported</span></span> | <span data-ttu-id="4e3fe-150">No admitido</span><span class="sxs-lookup"><span data-stu-id="4e3fe-150">Not supported</span></span> |
| <span data-ttu-id="4e3fe-151">[event](../resources/event.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="4e3fe-151">group [event](../resources/event.md)</span></span> | <span data-ttu-id="4e3fe-152">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="4e3fe-152">Group.Read.All</span></span> | <span data-ttu-id="4e3fe-153">No admitido</span><span class="sxs-lookup"><span data-stu-id="4e3fe-153">Not supported</span></span> | <span data-ttu-id="4e3fe-154">No admitido</span><span class="sxs-lookup"><span data-stu-id="4e3fe-154">Not supported</span></span> |
| <span data-ttu-id="4e3fe-155">[post](../resources/post.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="4e3fe-155">group [post](../resources/post.md)</span></span> | <span data-ttu-id="4e3fe-156">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="4e3fe-156">Group.Read.All</span></span> | <span data-ttu-id="4e3fe-157">No admitido</span><span class="sxs-lookup"><span data-stu-id="4e3fe-157">Not supported</span></span> | <span data-ttu-id="4e3fe-158">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="4e3fe-158">Group.Read.All</span></span> |
| [<span data-ttu-id="4e3fe-159">mailFolder</span><span class="sxs-lookup"><span data-stu-id="4e3fe-159">mailFolder</span></span>](../resources/mailfolder.md) | <span data-ttu-id="4e3fe-160">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="4e3fe-160">Mail.Read</span></span> | <span data-ttu-id="4e3fe-161">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="4e3fe-161">Mail.Read</span></span> | <span data-ttu-id="4e3fe-162">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="4e3fe-162">Mail.Read</span></span> |
| [<span data-ttu-id="4e3fe-163">message</span><span class="sxs-lookup"><span data-stu-id="4e3fe-163">message</span></span>](../resources/message.md) | <span data-ttu-id="4e3fe-164">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="4e3fe-164">Mail.Read</span></span> | <span data-ttu-id="4e3fe-165">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="4e3fe-165">Mail.Read</span></span> | <span data-ttu-id="4e3fe-166">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="4e3fe-166">Mail.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="4e3fe-167">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4e3fe-167">HTTP request</span></span>

#### <a name="get-a-resource-instance-expanded-with-an-extended-property-that-matches-a-filter"></a><span data-ttu-id="4e3fe-168">Expandir una instancia de recurso con una propiedad extendida que coincide con un filtro</span><span class="sxs-lookup"><span data-stu-id="4e3fe-168">GET a resource instance expanded with an extended property that matches a filter</span></span>
<span data-ttu-id="4e3fe-p105">Expanda una instancia de recurso con la propiedad extendida que coincida con un filtro en la propiedad **id**. Asegúrese de aplicar [la codificación de direcciones URL](https://www.w3schools.com/tags/ref_urlencode.asp) a los caracteres de espacio de la cadena de filtro.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-p105">Get a resource instance expanded with the extended property which matches a filter on the **id** property. Make sure you apply [URL encoding](https://www.w3schools.com/tags/ref_urlencode.asp) to the space characters in the filter string.</span></span>

<span data-ttu-id="4e3fe-171">Obtener una instancia de **mensaje** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="4e3fe-171">Get a **message** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/messages/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/messages/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /me/mailFolders/{id}/messages/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="4e3fe-172">Obtener una instancia de **mailFolder** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="4e3fe-172">Get a **mailFolder** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/mailFolders/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/mailFolders/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```

<span data-ttu-id="4e3fe-173">Obtener una instancia de **evento** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="4e3fe-173">Get an **event** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/events/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/events/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="4e3fe-174">Obtener una instancia de **calendario** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="4e3fe-174">Get a **calendar** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/calendars/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/calendars/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="4e3fe-175">Obtener una instancia de **ponerse en contacto con** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="4e3fe-175">Get a **contact** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/contacts/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/contacts/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /me/contactFolders/{id}/contacts/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/contactFolders/{id}/contacts/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="4e3fe-176">Obtener una instancia de **contactFolder** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="4e3fe-176">Get a **contactFolder** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/contactfolders/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/contactFolders/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="4e3fe-177">Obtener una instancia de **evento** de grupo:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="4e3fe-177">Get a group **event** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /groups/{id}/events/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```

<span data-ttu-id="4e3fe-178">Obtener una instancia de **entrada** de grupo:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="4e3fe-178">Get a group **post** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /groups/{id}/threads/{id}/posts/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /groups/{id}/conversations/{id}/threads/{id}/posts/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```

#### <a name="get-resource-instances-that-include-numeric-extended-properties-matching-a-filter"></a><span data-ttu-id="4e3fe-179">Obtener instancias de recursos que incluyan propiedades extendidas numéricas que coinciden con un filtro</span><span class="sxs-lookup"><span data-stu-id="4e3fe-179">GET resource instances that include numeric extended properties matching a filter</span></span>

<span data-ttu-id="4e3fe-180">Obtenga instancias de un recurso compatible que tenga una propiedad extendida numérica que coincide con un filtro.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-180">Get instances of a supported resource that have a numeric extended property matching a filter.</span></span> <span data-ttu-id="4e3fe-181">El filtro usa un operador `eq` en la propiedad **id** y uno de los siguientes operadores en la propiedad **value**: `eq`, `ne`,`ge`, `gt` , `le` o `lt`.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-181">The filter uses an `eq` operator on the **id** property, and one of the following operators on the **value** property: `eq`, `ne`,`ge`, `gt`, `le`, or `lt`.</span></span> <span data-ttu-id="4e3fe-182">Asegúrese de aplicar [la codificación de direcciones URL](https://www.w3schools.com/tags/ref_urlencode.asp) a los siguientes caracteres de la cadena de filtro: dos puntos, barra diagonal y espacio.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-182">Make sure you apply [URL encoding](https://www.w3schools.com/tags/ref_urlencode.asp) to the following characters in the filter string - colon, forward slash, and space.</span></span>

<span data-ttu-id="4e3fe-183">Las líneas de sintaxis siguientes muestran un filtro que usa un operador `eq` en el Id. y otro operador `eq` en el valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-183">The following syntax lines show a filter that uses an `eq` operator on the id, and another `eq` operator on the property value.</span></span> <span data-ttu-id="4e3fe-184">Puede sustituir el operador `eq` en el **valor** por alguno de los otros operadores (`ne`, `ge`, `gt`, `le` o `lt`) que se aplican a los valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-184">You can substitute the `eq` operator on the **value** by any one of the other operators (`ne`,`ge`, `gt`, `le`, or `lt`) that apply to numeric values.</span></span>

<span data-ttu-id="4e3fe-185">Obtener instancias de **mensaje** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="4e3fe-185">Get **message** instances: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /me/mailFolders/{id}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```
<span data-ttu-id="4e3fe-186">Obtener instancias de **mailFolder** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="4e3fe-186">Get **mailFolder** instances: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/mailFolders?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/mailFolders?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```

<span data-ttu-id="4e3fe-187">Obtener instancias de **eventos** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="4e3fe-187">Get **event** instances: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```
<span data-ttu-id="4e3fe-188">Obtener instancias de **calendario** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="4e3fe-188">Get **calendar** instances: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/calendars?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/calendars?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```
<span data-ttu-id="4e3fe-189">Obtener instancias **póngase en contacto con** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="4e3fe-189">Get **contact** instances: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/contacts?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/contacts?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /me/contactFolders/{id}/contacts?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/contactFolders/{id}/contacts?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```
<span data-ttu-id="4e3fe-190">Obtener instancias de **contactFolder** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="4e3fe-190">Get **contactFolder** instances: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/contactfolders?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/contactFolders?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```
<span data-ttu-id="4e3fe-191">Obtener instancias de **eventos** de grupo:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="4e3fe-191">Get group **event** instances: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /groups/{id}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```

<span data-ttu-id="4e3fe-192">Obtener instancias de **entrada** de grupo:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="4e3fe-192">Get group **post** instances: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /groups/{id}/threads/{id}/posts?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /groups/{id}/conversations/{id}/threads/{id}/posts?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```

#### <a name="get-resource-instances-with-string-typed-extended-properties-matching-a-filter"></a><span data-ttu-id="4e3fe-193">Obtener instancias de recursos con propiedades extendidas de tipo cadena que coinciden con un filtro</span><span class="sxs-lookup"><span data-stu-id="4e3fe-193">GET resource instances with string-typed extended properties matching a filter</span></span>

<span data-ttu-id="4e3fe-194">Obtenga instancias del recurso **mensaje** o **evento** recursos que tienen una propiedad extendida de tipo cadena que coincide con un filtro.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-194">Get instances of the **message** or **event** resource that have a string-typed extended property matching a filter.</span></span> <span data-ttu-id="4e3fe-195">El filtro usa un operador `eq` en la propiedad **id** y uno de los siguientes operadores en la propiedad **value**: `contains`, `startswith`,`eq` o `ne`.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-195">The filter uses an `eq` operator on the **id** property, and one of the following operators on the **value** property: `contains`, `startswith`, `eq`, or `ne`.</span></span> <span data-ttu-id="4e3fe-196">Asegúrese de aplicar [la codificación de direcciones URL](https://www.w3schools.com/tags/ref_urlencode.asp) a los siguientes caracteres de la cadena de filtro: dos puntos, barra diagonal y espacio.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-196">Make sure you apply [URL encoding](https://www.w3schools.com/tags/ref_urlencode.asp) to the following characters in the filter string - colon, forward slash, and space.</span></span>


<span data-ttu-id="4e3fe-197">Obtener instancias de **mensaje** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="4e3fe-197">Get **message** instances: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and contains(ep/value, '{property_value}'))
GET /users/{id|userPrincipalName}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and contains(ep/value, '{property_value}'))
GET /me/mailFolders/{id}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and contains(ep/value, '{property_value}'))

GET /me/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and startswith(ep/value, '{property_value}'))
GET /users/{id|userPrincipalName}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and startswith(ep/value, '{property_value}'))
GET /me/mailFolders/{id}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and startswith(ep/value, '{property_value}'))

GET /me/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /me/mailFolders/{id}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')

GET /me/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value ne '{property_value}')
GET /users/{id|userPrincipalName}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value ne '{property_value}')
GET /me/mailFolders/{id}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value ne '{property_value}')
```

<span data-ttu-id="4e3fe-198">Obtener instancias de **eventos** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="4e3fe-198">Get **event** instances: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and contains(ep/value, '{property_value}'))
GET /users/{id|userPrincipalName}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and contains(ep/value, '{property_value}'))

GET /me/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and startswith(ep/value, '{property_value}'))
GET /users/{id|userPrincipalName}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and startswith(ep/value, '{property_value}'))

GET /me/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')

GET /me/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value ne '{property_value}')
GET /users/{id|userPrincipalName}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value ne '{property_value}')
```

<span data-ttu-id="4e3fe-199">Obtener instancias de **eventos** de grupo:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="4e3fe-199">Get group **event** instances: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /groups/{id}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and contains(ep/value, '{property_value}'))
GET /groups/{id}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and startswith(ep/value, '{property_value}'))
GET /groups/{id}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /groups/{id}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value ne '{property_value}')
```

## <a name="path-parameters"></a><span data-ttu-id="4e3fe-200">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="4e3fe-200">Path parameters</span></span>
|<span data-ttu-id="4e3fe-201">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4e3fe-201">Parameter</span></span>|<span data-ttu-id="4e3fe-202">Tipo</span><span class="sxs-lookup"><span data-stu-id="4e3fe-202">Type</span></span>|<span data-ttu-id="4e3fe-203">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e3fe-203">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4e3fe-204">id_value</span><span class="sxs-lookup"><span data-stu-id="4e3fe-204">id_value</span></span>|<span data-ttu-id="4e3fe-205">String</span><span class="sxs-lookup"><span data-stu-id="4e3fe-205">String</span></span>|<span data-ttu-id="4e3fe-p109">El identificador de la propiedad extendida que debe coincidir. Debe tener uno de los formatos compatibles. Consulte la [Información general de las propiedades extendidas de Outlook](../resources/extended-properties-overview.md) para obtener más información. Necesario.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-p109">The ID of the extended property to match. It must follow one of the supported formats. See [Outlook extended properties overview](../resources/extended-properties-overview.md) for more information. Required.</span></span>|
|<span data-ttu-id="4e3fe-210">property_value</span><span class="sxs-lookup"><span data-stu-id="4e3fe-210">property_value</span></span> |<span data-ttu-id="4e3fe-211">Cadena</span><span class="sxs-lookup"><span data-stu-id="4e3fe-211">String</span></span>|<span data-ttu-id="4e3fe-212">El valor de la propiedad extendida que debe coincidir.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-212">The value of the extended property to match.</span></span> <span data-ttu-id="4e3fe-213">Es necesario donde aparece en la sección anterior **Solicitud HTTP**.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-213">Required where listed in the **HTTP request** section above.</span></span> <span data-ttu-id="4e3fe-214">Si {property_value} no es una cadena, asegúrese de convertir explícitamente `ep/value` en el tipo de datos Edm apropiado cuando se compare con {property_value}.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-214">If {property_value} is not a string, make sure you explicitly cast `ep/value` to the appropriate Edm data type when comparing it with {property_value}.</span></span> <span data-ttu-id="4e3fe-215">Vea la [solicitud 4](#request-4) a continuación para obtener ejemplos.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-215">See [request 4](#request-4) below for examples.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="4e3fe-216">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4e3fe-216">Request headers</span></span>
| <span data-ttu-id="4e3fe-217">Nombre</span><span class="sxs-lookup"><span data-stu-id="4e3fe-217">Name</span></span>      |<span data-ttu-id="4e3fe-218">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e3fe-218">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="4e3fe-219">Authorization</span><span class="sxs-lookup"><span data-stu-id="4e3fe-219">Authorization</span></span>  | <span data-ttu-id="4e3fe-p111">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-p111">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4e3fe-222">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4e3fe-222">Request body</span></span>
<span data-ttu-id="4e3fe-223">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-223">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4e3fe-224">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4e3fe-224">Response</span></span>

<span data-ttu-id="4e3fe-225">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-225">If successful, this method returns a `200 OK` response code.</span></span>

#### <a name="get-resource-instance-expanded-with-a-matching-extended-property"></a><span data-ttu-id="4e3fe-226">Expandir una instancia de recurso con una propiedad extendida coincidente</span><span class="sxs-lookup"><span data-stu-id="4e3fe-226">GET resource instance expanded with a matching extended property</span></span>
<span data-ttu-id="4e3fe-227">El cuerpo de la respuesta incluye un objeto que representa la instancia de recurso solicitada y expandida con el objeto coincidente [singleValueLegacyExtendedProperty](../resources/singlevaluelegacyextendedproperty.md).</span><span class="sxs-lookup"><span data-stu-id="4e3fe-227">The response body includes an object representing the requested resource instance, expanded with the matching [singleValueLegacyExtendedProperty](../resources/singlevaluelegacyextendedproperty.md) object.</span></span>
  
#### <a name="get-resource-instances-that-contain-an-extended-property-matching-a-filter"></a><span data-ttu-id="4e3fe-228">Obtener instancias de recurso que contienen una propiedad extendida que coincide con un filtro</span><span class="sxs-lookup"><span data-stu-id="4e3fe-228">GET resource instances that contain an extended property matching a filter</span></span>
<span data-ttu-id="4e3fe-229">El cuerpo de la respuesta incluye uno o varios objetos que representan las instancias de recurso que contienen una propiedad extendida coincidente.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-229">The response body includes one or more objects representing the resource instances that contain a matching extended property.</span></span> <span data-ttu-id="4e3fe-230">El cuerpo de la respuesta no incluye la propiedad extendida.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-230">The response body does not include the extended property.</span></span>

## <a name="example"></a><span data-ttu-id="4e3fe-231">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4e3fe-231">Example</span></span>
#### <a name="request-1"></a><span data-ttu-id="4e3fe-232">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="4e3fe-232">Request 1</span></span>

<span data-ttu-id="4e3fe-p113">El primer ejemplo obtiene y expande el mensaje especificado al incluir una propiedad extendida de valor único. El filtro devuelve la propiedad extendida cuyo **identificador** coincide con la cadena `String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color` (la codificación de dirección URL se ha eliminado aquí para facilitar la lectura).</span><span class="sxs-lookup"><span data-stu-id="4e3fe-p113">The first example gets and expands the specified message by including a single-value extended property. The filter returns the extended property that has its **id** matching the string `String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color` (with URL encoding removed here for ease of reading).</span></span>

<!-- {
  "blockType": "request",
  "sampleKeys": ["AAMkAGE1M2_bs88AACHsLqWAAA="],
  "name": "get_singlevaluelegacyextendedproperty_1"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages/AAMkAGE1M2_bs88AACHsLqWAAA=?$expand=singleValueExtendedProperties($filter=id%20eq%20'String%20{66f5a359-4659-4830-9070-00047ec6ac6e}%20Name%20Color')
```
#### <a name="response-1"></a><span data-ttu-id="4e3fe-235">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="4e3fe-235">Response 1</span></span>
<span data-ttu-id="4e3fe-236">El cuerpo de la respuesta incluye todas las propiedades del mensaje especificado y devuelve la propiedad extendida del filtro.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-236">The response body includes all the properties of the specified message and extended property returned from the filter.</span></span>

<span data-ttu-id="4e3fe-p114">Nota: El objeto del **mensaje** que aparece aquí está truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-p114">Note: The **message** object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Me/messages/$entity",
    "@odata.id": "https://graph.microsoft.com/v1.0/users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/messages('AAMkAGE1M2_bs88AACHsLqWAAA=')",
    "@odata.etag": "W/\"CQAAABYAAACY4MQpaFz9SbqUDe4+bs88AACbyS4H\"",
    "id": "AAMkAGE1M2_bs88AACHsLqWAAA=",
    "subject": "RE: Talk about emergency prep",
    "sender": {
        "emailAddress": {
            "name": "Christine Irwin",
            "address": "christine@contoso.com"
        }
    },
    "from": null,
    "toRecipients": [
        {
            "emailAddress": {
                "name": "Christine Irwin",
                "address": "christine@contoso.com"
            }
        }
    ],
    "singleValueExtendedProperties@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Me/messages('AAMkAGE1M2_bs88AACHsLqWAAA%3D')/singleValueExtendedProperties",
    "singleValueExtendedProperties": [
        {
            "id": "String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color",
            "value": "Green"
        }
    ]
}
```

#### <a name="request-2"></a><span data-ttu-id="4e3fe-239">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="4e3fe-239">Request 2</span></span>

<span data-ttu-id="4e3fe-240">En el segundo ejemplo, se obtienen mensajes con la propiedad extendida de valor único de tipo cadena especificada en el filtro.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-240">The second example gets messages that have the string-typed single-value extended property specified in the filter.</span></span> <span data-ttu-id="4e3fe-241">El filtro busca una propiedad extendida que tenga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4e3fe-241">The filter looks for the extended property that has:</span></span>

- <span data-ttu-id="4e3fe-242">Un **id.** igual a la cadena `String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color` (con la codificación de direcciones URL quitada aquí para facilitar la lectura).</span><span class="sxs-lookup"><span data-stu-id="4e3fe-242">Its **id** equal to the string `String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color` (with URL encoding removed here for ease of reading).</span></span>

- <span data-ttu-id="4e3fe-243">Un **valor** igual a la cadena `Green`.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-243">Its **value** equal to the string `Green`.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/v1.0/me/messages?$filter=singleValueExtendedProperties%2FAny(ep%3A%20ep%2Fid%20eq%20'String%20{66f5a359-4659-4830-9070-00047ec6ac6e}%20Name%20Color'%20and%20ep%2Fvalue%20eq%20'Green')
```

#### <a name="response-2"></a><span data-ttu-id="4e3fe-244">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="4e3fe-244">Response 2</span></span>

<span data-ttu-id="4e3fe-p116">Un código de respuesta `HTTP 200 OK` indica una respuesta correcta y el cuerpo de la respuesta incluye todas las propiedades de los mensajes cuya propiedad extendida coincide con el filtro. El cuerpo de la respuesta es similar a la respuesta al [obtener una colección de mensajes](../api/user_list_messages.md). El cuerpo de la respuesta no incluye la propiedad extendida coincidente.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-p116">A successful response is indicated by an `HTTP 200 OK` response code, and the response body includes all the properties of the messages that have the extended property matching the filter. The response body is similar to the response from [getting a message collection](../api/user_list_messages.md). The response does not include the matching extended property.</span></span>


#### <a name="request-3"></a><span data-ttu-id="4e3fe-248">Solicitud 3</span><span class="sxs-lookup"><span data-stu-id="4e3fe-248">Request 3</span></span>

<span data-ttu-id="4e3fe-249">En el tercer ejemplo, se obtienen mensajes con la propiedad extendida de valor único de tipo cadena especificada en el filtro.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-249">The third example gets messages that have the string-typed single-value extended property specified in the filter.</span></span> <span data-ttu-id="4e3fe-250">El filtro busca una propiedad extendida que tenga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4e3fe-250">The filter looks for the extended property that has:</span></span>

- <span data-ttu-id="4e3fe-251">Un **id.** igual a la cadena `String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color` (con la codificación de direcciones URL quitada aquí para facilitar la lectura).</span><span class="sxs-lookup"><span data-stu-id="4e3fe-251">Its **id** equal to the string `String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color` (with URL encoding removed here for ease of reading).</span></span>

- <span data-ttu-id="4e3fe-252">Su **valor** que contiene la cadena `green`.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-252">Its **value** containing the string `green`.</span></span> 

<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/v1.0/Me/messages?$filter=singleValueExtendedProperties/any(ep:ep/Id eq 'String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color' and contains(ep/Value, 'green'))
```

#### <a name="response-3"></a><span data-ttu-id="4e3fe-253">Respuesta 3</span><span class="sxs-lookup"><span data-stu-id="4e3fe-253">Response 3</span></span>

<span data-ttu-id="4e3fe-254">Un código de respuesta `HTTP 200 OK` indica una respuesta correcta y el cuerpo de la respuesta incluye todas las propiedades de los mensajes cuya propiedad extendida coincide con el filtro.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-254">A successful response is indicated by an `HTTP 200 OK` response code, and the response body includes all the properties of the messages that have the extended property matching the filter.</span></span> <span data-ttu-id="4e3fe-255">Por ejemplo, un mensaje que tiene una propiedad extendida de valor único con el **id** igual a la cadena `String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color` y el **valor** `Light green`, debería coincidir con el filtro y se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-255">For example, a message that has a single-value extended property with the **id** equal to the string `String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color`, and the **value** `Light green`, would match the filter and be included in the response.</span></span>

<span data-ttu-id="4e3fe-256">El cuerpo de la respuesta es similar a la respuesta de la [obtención de una colección de mensajes](../api/user_list_messages.md).</span><span class="sxs-lookup"><span data-stu-id="4e3fe-256">The response body is similar to the response from [getting a message collection](../api/user_list_messages.md).</span></span> <span data-ttu-id="4e3fe-257">El cuerpo de la respuesta no incluye la propiedad extendida coincidente.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-257">The response does not include the matching extended property.</span></span>


#### <a name="request-4"></a><span data-ttu-id="4e3fe-258">Solicitud 4</span><span class="sxs-lookup"><span data-stu-id="4e3fe-258">Request 4</span></span>

<span data-ttu-id="4e3fe-259">En los siguientes dos ejemplos, se muestra cómo obtener mensajes que tengan propiedades extendidas de valor único que no sean de tipo cadena.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-259">The next 2 examples show how to get messages that have non-string typed single-value extended properties.</span></span> <span data-ttu-id="4e3fe-260">Para facilitar la lectura, no incluyen la codificación de direcciones URL necesaria.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-260">For ease of reading, they do not include the necessary URL encoding.</span></span>

<span data-ttu-id="4e3fe-261">En el siguiente ejemplo, se muestra un filtro que busca una propiedad extendida que tenga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4e3fe-261">The following example shows a filter that looks for the extended property that has:</span></span>

- <span data-ttu-id="4e3fe-262">Un **id.** coincidente con la cadena `CLSID {00062008-0000-0000-C000-000000000046} Name ConnectorSenderGuid`.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-262">Its **id** matching the string `CLSID {00062008-0000-0000-C000-000000000046} Name ConnectorSenderGuid`.</span></span>

- <span data-ttu-id="4e3fe-263">El GUID `b9cf8971-7d55-4b73-9ffa-a584611b600b` como **valor**.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-263">Its **value** being the GUID `b9cf8971-7d55-4b73-9ffa-a584611b600b`.</span></span> <span data-ttu-id="4e3fe-264">Para comparar el valor de propiedad con un GUID, convierta `ep/value` en `Edm.Guid`.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-264">To compare the property value with a GUID, cast `ep/value` to `Edm.Guid`.</span></span>


<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/v1.0/me/messages?$filter=singleValueExtendedProperties/any(ep:ep/id eq 'CLSID {00062008-0000-0000-C000-000000000046} Name ConnectorSenderGuid' and cast(ep/value, Edm.Guid) eq (b9cf8971-7d55-4b73-9ffa-a584611b600b))
```

<span data-ttu-id="4e3fe-265">En el siguiente ejemplo, se muestra un filtro que busca una propiedad extendida que tenga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4e3fe-265">The next example shows a filter that looks for the extended property that has:</span></span>

- <span data-ttu-id="4e3fe-266">Un **id.** coincidente con la cadena `Integer {66f5a359-4659-4830-9070-00047ec6ac6e} Name Pallete`.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-266">Its **id** matching the string `Integer {66f5a359-4659-4830-9070-00047ec6ac6e} Name Pallete`.</span></span>

- <span data-ttu-id="4e3fe-267">Un **valor** igual que el número entero 12.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-267">Its **value** equal to the integer 12.</span></span> <span data-ttu-id="4e3fe-268">Para comparar el valor de propiedad con un número entero, convierta `ep/value` en `Edm.Int32`.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-268">To compare the property value with an integer, cast `ep/value` to `Edm.Int32`.</span></span>


<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/v1.0/me/messages?$filter=singleValueExtendedProperties/any(ep:ep/id eq 'Integer {66f5a359-4659-4830-9070-00047ec6ac6e} Name Pallete' and cast(ep/value, Edm.Int32) eq 12)
```


#### <a name="response-4"></a><span data-ttu-id="4e3fe-269">Respuesta 4</span><span class="sxs-lookup"><span data-stu-id="4e3fe-269">Response 4</span></span>

<span data-ttu-id="4e3fe-270">Para cada uno de los dos ejemplos anteriores, un código de respuesta `HTTP 200 OK` indica una respuesta correcta y el cuerpo de la respuesta incluye todas las propiedades de los mensajes cuya propiedad extendida coincide con el filtro correspondiente.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-270">For each of the preceding 2 examples, a successful response is indicated by an `HTTP 200 OK` response code, and the response body includes all the properties of the messages that have the extended property matching the corresponding filter.</span></span> <span data-ttu-id="4e3fe-271">El cuerpo de la respuesta es similar a la respuesta de la [obtención de una colección de mensajes](../api/user_list_messages.md).</span><span class="sxs-lookup"><span data-stu-id="4e3fe-271">The response body is similar to the response from [getting a message collection](../api/user_list_messages.md).</span></span> <span data-ttu-id="4e3fe-272">El cuerpo de la respuesta no incluye la propiedad extendida coincidente.</span><span class="sxs-lookup"><span data-stu-id="4e3fe-272">The response does not include the matching extended property.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get singleValueLegacyExtendedProperty",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->