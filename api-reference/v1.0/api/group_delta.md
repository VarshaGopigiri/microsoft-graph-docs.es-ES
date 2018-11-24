# <a name="group-delta"></a><span data-ttu-id="b44a2-101">grupo: delta</span><span class="sxs-lookup"><span data-stu-id="b44a2-101">group: delta</span></span>
<span data-ttu-id="b44a2-102">Get recién creado, actualiza o elimina grupos, incluidos los cambios de pertenencia de grupo, sin tener que realizar un acceso completo de lectura de la colección de todo grupo.</span><span class="sxs-lookup"><span data-stu-id="b44a2-102">Get newly created, updated, or deleted groups, including group membership changes, without having to perform a full read of the entire group collection.</span></span> <span data-ttu-id="b44a2-103">Para obtener más información, vea [Uso de consulta de Delta](../../../concepts/delta_query_overview.md) .</span><span class="sxs-lookup"><span data-stu-id="b44a2-103">See [Using Delta Query](../../../concepts/delta_query_overview.md) for details.</span></span>

## <a name="permissions"></a><span data-ttu-id="b44a2-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="b44a2-104">Permissions</span></span>

<span data-ttu-id="b44a2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b44a2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b44a2-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b44a2-107">Permission type</span></span>      | <span data-ttu-id="b44a2-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b44a2-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b44a2-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b44a2-109">Delegated (work or school account)</span></span> | <span data-ttu-id="b44a2-110">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b44a2-110">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="b44a2-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b44a2-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b44a2-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b44a2-112">Not supported.</span></span>    |
|<span data-ttu-id="b44a2-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b44a2-113">Application</span></span> | <span data-ttu-id="b44a2-114">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b44a2-114">Group.Read.All, Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="b44a2-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b44a2-115">HTTP request</span></span>

<span data-ttu-id="b44a2-116">Para comenzar los cambios, debe realizar una solicitud incluyendo la función delta en el recurso grupo.</span><span class="sxs-lookup"><span data-stu-id="b44a2-116">To begin tracking changes, you make a request including the delta function on the groups resource.</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /groups/delta
```

## <a name="query-parameters"></a><span data-ttu-id="b44a2-117">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="b44a2-117">Query parameters</span></span>

<span data-ttu-id="b44a2-p103">El seguimiento de cambios en grupos conlleva al menos una llamada de una función **delta**. Si usa cualquier parámetro de consulta (uno diferente a `$deltatoken` y `$skiptoken`), debe especificarlo en la solicitud **delta** inicial. Microsoft Graph codifica automáticamente cualquier parámetro especificado en la parte del token de la URL `nextLink` o `deltaLink` proporcionada en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b44a2-p103">Tracking changes in groups incurs a round of one or more **delta** function calls. If you use any query parameter (other than `$deltatoken` and `$skiptoken`), you must specify it in the initial **delta** request. Microsoft Graph automatically encodes any specified parameters into the token portion of the `nextLink` or `deltaLink` URL provided in the response.</span></span>

<span data-ttu-id="b44a2-121">Solo debe especificar una vez por adelantado los parámetros de consulta deseados.</span><span class="sxs-lookup"><span data-stu-id="b44a2-121">You only need to specify any desired query parameters once upfront.</span></span>

<span data-ttu-id="b44a2-122">En solicitudes posteriores, copie y aplique la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.</span><span class="sxs-lookup"><span data-stu-id="b44a2-122">In subsequent requests, copy and apply the `nextLink` or `deltaLink` URL from the previous response, as that URL already includes the encoded, desired parameters.</span></span>

| <span data-ttu-id="b44a2-123">Parámetro de consulta</span><span class="sxs-lookup"><span data-stu-id="b44a2-123">Query parameter</span></span> | <span data-ttu-id="b44a2-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="b44a2-124">Type</span></span>  |<span data-ttu-id="b44a2-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="b44a2-125">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="b44a2-126">$deltatoken</span><span class="sxs-lookup"><span data-stu-id="b44a2-126">$deltatoken</span></span> | <span data-ttu-id="b44a2-127">string</span><span class="sxs-lookup"><span data-stu-id="b44a2-127">string</span></span> | <span data-ttu-id="b44a2-p104">Un [token de estado](../../../concepts/delta_query_overview.md) que se devuelve en la URL de `deltaLink` de la llamada de función **delta** anterior para la misma colección de grupos. Indica el progreso de la ronda de seguimiento de cambios. Guarde y aplique toda la dirección URL `deltaLink`, incluido este token, en la primera solicitud de la siguiente ronda de seguimiento de cambios de la colección.</span><span class="sxs-lookup"><span data-stu-id="b44a2-p104">A [state token](../../../concepts/delta_query_overview.md) returned in the `deltaLink` URL of the previous **delta** function call for the same group collection, indicating the completion of that round of change tracking. Save and apply the entire `deltaLink` URL including this token in the first request of the next round of change tracking for that collection.</span></span>|
| <span data-ttu-id="b44a2-130">$skiptoken</span><span class="sxs-lookup"><span data-stu-id="b44a2-130">$skiptoken</span></span> | <span data-ttu-id="b44a2-131">string</span><span class="sxs-lookup"><span data-stu-id="b44a2-131">string</span></span> | <span data-ttu-id="b44a2-132">Un [token de estado](../../../concepts/delta_query_overview.md) que se devuelve en la URL de `nextLink` de la llamada de función **delta**. Indica que debe realizarse el seguimiento de más cambios en la misma colección de grupos.</span><span class="sxs-lookup"><span data-stu-id="b44a2-132">A [state token](../../../concepts/delta_query_overview.md) returned in the `nextLink` URL of the previous **delta** function call, indicating there are further changes to be tracked in the same group collection.</span></span> |

### <a name="odata-query-parameters"></a><span data-ttu-id="b44a2-133">Parámetros de consulta de OData</span><span class="sxs-lookup"><span data-stu-id="b44a2-133">OData query parameters</span></span>

<span data-ttu-id="b44a2-134">Este método es compatible con parámetros opcionales de consulta de OData para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b44a2-134">This method supports optional OData query parameters to help customize the response.</span></span>

- <span data-ttu-id="b44a2-p105">Puede utilizar un parámetro de consulta `$select` como en cualquier solicitud GET para especificar solo las propiedades que necesita para un mejor rendimiento. Siempre se devuelve la propiedad *id*.</span><span class="sxs-lookup"><span data-stu-id="b44a2-p105">You can use a `$select` query parameter as in any GET request to specify only the properties your need for best performance. The *id* property is always returned.</span></span>
- <span data-ttu-id="b44a2-137">Puede usar `$expand=members` para obtener los cambios de pertenencia.</span><span class="sxs-lookup"><span data-stu-id="b44a2-137">You can use `$expand=members` to get membership changes.</span></span>
- <span data-ttu-id="b44a2-138">No hay compatibilidad limitada para `$filter`:</span><span class="sxs-lookup"><span data-stu-id="b44a2-138">There is limited support for `$filter`:</span></span>
  - <span data-ttu-id="b44a2-139">La única expresión `$filter` admitida es para realizar un seguimiento de los cambios en un objeto específico: `$filter=id+eq+{value}`.</span><span class="sxs-lookup"><span data-stu-id="b44a2-139">The only supported `$filter` expression is for tracking changes on a specific object: `$filter=id+eq+{value}`.</span></span> <span data-ttu-id="b44a2-140">Puede filtrar varios objetos.</span><span class="sxs-lookup"><span data-stu-id="b44a2-140">You can filter multiple objects.</span></span> <span data-ttu-id="b44a2-141">Por ejemplo, `https://graph.microsoft.com/v1.0/groups/delta/?$filter= id eq '477e9fc6-5de7-4406-bb2a-7e5c83c9ffff' or id eq '004d6a07-fe70-4b92-add5-e6e37b8affff'`.</span><span class="sxs-lookup"><span data-stu-id="b44a2-141">For example, `https://graph.microsoft.com/v1.0/groups/delta/?$filter= id eq '477e9fc6-5de7-4406-bb2a-7e5c83c9ffff' or id eq '004d6a07-fe70-4b92-add5-e6e37b8affff'`.</span></span> <span data-ttu-id="b44a2-142">Hay un límite de 50 objetos filtrados.</span><span class="sxs-lookup"><span data-stu-id="b44a2-142">There is a limit of 50 filtered objects.</span></span>

## <a name="request-headers"></a><span data-ttu-id="b44a2-143">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b44a2-143">Request headers</span></span>

| <span data-ttu-id="b44a2-144">Nombre</span><span class="sxs-lookup"><span data-stu-id="b44a2-144">Name</span></span>       | <span data-ttu-id="b44a2-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="b44a2-145">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="b44a2-146">Authorization</span><span class="sxs-lookup"><span data-stu-id="b44a2-146">Authorization</span></span>  | <span data-ttu-id="b44a2-147">&lt;token&gt; de portador</span><span class="sxs-lookup"><span data-stu-id="b44a2-147">Bearer &lt;token&gt;</span></span>|
| <span data-ttu-id="b44a2-148">Content-Type</span><span class="sxs-lookup"><span data-stu-id="b44a2-148">Content-Type</span></span>  | <span data-ttu-id="b44a2-149">application/json</span><span class="sxs-lookup"><span data-stu-id="b44a2-149">application/json</span></span> |
| <span data-ttu-id="b44a2-150">Prefer</span><span class="sxs-lookup"><span data-stu-id="b44a2-150">Prefer</span></span> | <span data-ttu-id="b44a2-151">devolver = mínimo</span><span class="sxs-lookup"><span data-stu-id="b44a2-151">return=minimal</span></span> <br><br><span data-ttu-id="b44a2-152">Si se especifica este encabezado con una solicitud que utiliza un `deltaLink` devolvería sólo las propiedades del objeto que han cambiado desde la última round.</span><span class="sxs-lookup"><span data-stu-id="b44a2-152">Specifying this header with a request that uses a `deltaLink` would return only the object properties that have changed since the last round.</span></span> <span data-ttu-id="b44a2-153">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b44a2-153">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b44a2-154">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b44a2-154">Request body</span></span>

<span data-ttu-id="b44a2-155">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b44a2-155">Do not supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="b44a2-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b44a2-156">Response</span></span>

<span data-ttu-id="b44a2-157">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección [grupo](../resources/group.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b44a2-157">If successful, this method returns `200 OK` response code and [group](../resources/group.md) collection object in the response body.</span></span> <span data-ttu-id="b44a2-158">La respuesta incluye también un símbolo (token) de estado que puede ser un `nextLink` dirección URL o un `deltaLink` dirección URL.</span><span class="sxs-lookup"><span data-stu-id="b44a2-158">The response also includes a state token which is either a `nextLink` URL or a `deltaLink` URL.</span></span>

- <span data-ttu-id="b44a2-159">Si un `nextLink` se devuelve la dirección URL:</span><span class="sxs-lookup"><span data-stu-id="b44a2-159">If a `nextLink` URL is returned:</span></span>
  - <span data-ttu-id="b44a2-160">Esto indica que hay páginas adicionales de datos que se recuperarán en la sesión.</span><span class="sxs-lookup"><span data-stu-id="b44a2-160">This indicates there are additional pages of data to be retrieved in the session.</span></span> <span data-ttu-id="b44a2-161">La aplicación continúa realizar solicitudes mediante el `nextLink` dirección URL hasta un `deltaLink` dirección URL se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b44a2-161">The application continues making requests using the `nextLink` URL until a `deltaLink` URL is included in the response.</span></span>
  - <span data-ttu-id="b44a2-162">La respuesta incluye el mismo conjunto de propiedades como se muestra en la solicitud de consulta delta inicial.</span><span class="sxs-lookup"><span data-stu-id="b44a2-162">The response includes the same set of properties as in the initial delta query request.</span></span> <span data-ttu-id="b44a2-163">Esto le permite capturar el estado actual y completa de los objetos al iniciar el ciclo de delta.</span><span class="sxs-lookup"><span data-stu-id="b44a2-163">This allows you to capture the full current state of the objects when initiating the delta cycle.</span></span>

- <span data-ttu-id="b44a2-164">Si un `deltaLink` se devuelve la dirección URL:</span><span class="sxs-lookup"><span data-stu-id="b44a2-164">If a `deltaLink` URL is returned:</span></span>
  - <span data-ttu-id="b44a2-165">Esto indica que no hay ningún dato más sobre el estado existente del recurso que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="b44a2-165">This indicates there is no more data about the existing state of the resource to be returned.</span></span> <span data-ttu-id="b44a2-166">Guardar y utilizar el `deltaLink` dirección URL para obtener más información acerca de cambia para el recurso en la ronda siguiente.</span><span class="sxs-lookup"><span data-stu-id="b44a2-166">Save and use the `deltaLink` URL to learn about changes to the resource in the next round.</span></span>
  - <span data-ttu-id="b44a2-167">Tiene una opción para especificar el `Prefer:return=minimal` encabezado, que se incluirá en los valores de respuesta sólo para las propiedades que han cambiado desde el momento en que el `deltaLink` se emitió.</span><span class="sxs-lookup"><span data-stu-id="b44a2-167">You have a choice to specify the `Prefer:return=minimal` header, to include in the response values for only the properties that have changed since the time the `deltaLink` was issued.</span></span>

#### <a name="default-return-the-same-properties-as-initial-delta-request"></a><span data-ttu-id="b44a2-168">Valor predeterminado: devolver las mismas propiedades que la solicitud inicial del delta</span><span class="sxs-lookup"><span data-stu-id="b44a2-168">Default: return the same properties as initial delta request</span></span>

<span data-ttu-id="b44a2-169">De forma predeterminada, las solicitudes con un `deltaLink` o `nextLink` devolver las mismas propiedades como seleccionado en la consulta inicial del delta de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="b44a2-169">By default, requests using a `deltaLink` or `nextLink` return the same properties as selected in the initial delta query in the following ways:</span></span>

- <span data-ttu-id="b44a2-170">Si la propiedad ha cambiado, devuelva la propiedad en la respuesta JSON.</span><span class="sxs-lookup"><span data-stu-id="b44a2-170">If the property has changed, return the property in the JSON response.</span></span>
- <span data-ttu-id="b44a2-171">Si se ha establecido la propiedad en un valor vacío, devuelve el valor de la propiedad como null.</span><span class="sxs-lookup"><span data-stu-id="b44a2-171">If the property has been set to an empty value, return the property value as null.</span></span>
- <span data-ttu-id="b44a2-172">Si la propiedad no ha cambiado, devolver el valor como null.</span><span class="sxs-lookup"><span data-stu-id="b44a2-172">If the property has not changed, return the value as null.</span></span>

> <span data-ttu-id="b44a2-173">**Nota:** Con el comportamiento anterior, no es posible diferenciar entre una propiedad que no ha cambiado y uno que ha cambiado a un `null` valor.</span><span class="sxs-lookup"><span data-stu-id="b44a2-173">**Note:** With the above behavior, it is not possible to differentiate between a property that has not changed and one that has changed to a `null` value.</span></span> <span data-ttu-id="b44a2-174">Vea el [segundo ejemplo](#request-2) siguiente.</span><span class="sxs-lookup"><span data-stu-id="b44a2-174">See the [second example](#request-2) below.</span></span> <span data-ttu-id="b44a2-175">Si esto es importante, se recomienda usar el comportamiento alternativo que se describen en la siguiente sección.</span><span class="sxs-lookup"><span data-stu-id="b44a2-175">If this is important, we recommend using the alternative behavior described in the next section.</span></span>

#### <a name="alternative-return-only-the-changed-properties"></a><span data-ttu-id="b44a2-176">Alternativa: devolver sólo las propiedades modificadas</span><span class="sxs-lookup"><span data-stu-id="b44a2-176">Alternative: return only the changed properties</span></span>

<span data-ttu-id="b44a2-177">Adición de un encabezado de solicitud opcional - `prefer:return=minimal` -da como resultado el siguiente comportamiento:</span><span class="sxs-lookup"><span data-stu-id="b44a2-177">Adding an optional request header - `prefer:return=minimal` - results in the following behavior:</span></span>

- <span data-ttu-id="b44a2-178">Si la propiedad ha cambiado, devuelva la propiedad en la respuesta JSON.</span><span class="sxs-lookup"><span data-stu-id="b44a2-178">If the property has changed, return the property in the JSON response.</span></span>
- <span data-ttu-id="b44a2-179">Si se ha establecido la propiedad en un valor vacío, devuelve el valor de la propiedad como null.</span><span class="sxs-lookup"><span data-stu-id="b44a2-179">If the property has been set to an empty value, return the property value as null.</span></span>
- <span data-ttu-id="b44a2-180">Si la propiedad no ha cambiado, no incluya la propiedad en la respuesta JSON.</span><span class="sxs-lookup"><span data-stu-id="b44a2-180">If the property has not changed, do not include the property in the JSON response.</span></span> <span data-ttu-id="b44a2-181">(Distinto del comportamiento predeterminado).</span><span class="sxs-lookup"><span data-stu-id="b44a2-181">(Different from the default behavior.)</span></span>

> <span data-ttu-id="b44a2-182">**Nota:** El encabezado puede agregarse a un `deltaLink` solicitud en cualquier momento en el ciclo de delta.</span><span class="sxs-lookup"><span data-stu-id="b44a2-182">**Note:** The header can be added to a `deltaLink` request at any point in time in the delta cycle.</span></span> <span data-ttu-id="b44a2-183">El encabezado sólo afecta el conjunto de propiedades que se incluyen en la respuesta y no afecta a cómo se ejecuta la consulta de delta.</span><span class="sxs-lookup"><span data-stu-id="b44a2-183">The header only affects the set of properties included in the response and it does not affect how the delta query is executed.</span></span> <span data-ttu-id="b44a2-184">Vea el [tercer ejemplo](#request-3) siguiente.</span><span class="sxs-lookup"><span data-stu-id="b44a2-184">See the [third example](#request-3) below.</span></span>

### <a name="example"></a><span data-ttu-id="b44a2-185">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b44a2-185">Example</span></span>

#### <a name="request-1"></a><span data-ttu-id="b44a2-186">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="b44a2-186">Request 1</span></span>

<span data-ttu-id="b44a2-187">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b44a2-187">The following is an example of the request.</span></span> <span data-ttu-id="b44a2-188">No hay ningún `$select` parámetro, por lo que se realiza un seguimiento y devuelve un conjunto predeterminado de propiedades.</span><span class="sxs-lookup"><span data-stu-id="b44a2-188">There is no `$select` parameter, so a default set of properties is tracked and returned.</span></span>
<!-- {
  "blockType": "request",
  "name": "group_delta"
}-->

```http
GET https://graph.microsoft.com/v1.0/groups/delta
```

#### <a name="response-1"></a><span data-ttu-id="b44a2-189">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="b44a2-189">Response 1</span></span>

<span data-ttu-id="b44a2-190">El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="b44a2-190">The following is an example of the response when using `deltaLink` obtained from the query initialization.</span></span>

><span data-ttu-id="b44a2-191">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="b44a2-191">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="b44a2-192">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b44a2-192">All the properties will be returned from an actual call.</span></span>
>
> <span data-ttu-id="b44a2-193">Tenga en cuenta la presencia de la propiedad *members@delta* que incluye los identificadores de objetos miembros en el grupo.</span><span class="sxs-lookup"><span data-stu-id="b44a2-193">Note the presence of the *members@delta* property which includes the ids of member objects in the group.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.group",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups","@odata.nextLink":"https://graph.microsoft.com/v1.0/groups/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjvY1FSSc_",
  "value":[
    {
      "classification": "classification-value",
      "createdDateTime":"datetime-value",
      "description":"Test group 1",
      "displayName":"TestGroup1",
      "groupTypes": [
        "groupTypes-value"
      ],
      "mail": "mail-value",
      "members@delta": [
               {
                   "@odata.type": "#microsoft.graph.user",
                   "id": "693acd06-2877-4339-8ade-b704261fe7a0"
               },
               {
                   "@odata.type": "#microsoft.graph.user",
                   "id": "49320844-be99-4164-8167-87ff5d047ace"
               }
      ]
    }
  ]
}
```

#### <a name="request-2"></a><span data-ttu-id="b44a2-194">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="b44a2-194">Request 2</span></span>

<span data-ttu-id="b44a2-195">En el ejemplo siguiente se muestra la solicitud inicial seleccionando 3 propiedades para el seguimiento de cambios, con comportamiento de respuesta predeterminado:</span><span class="sxs-lookup"><span data-stu-id="b44a2-195">The next example shows the initial request selecting 3 properties for change tracking, with default response behavior:</span></span>
<!-- {
  "blockType": "request",
  "name": "group_delta"
}-->

```http
GET https://graph.microsoft.com/v1.0/groups/delta?$select=displayName,description,mailNickname
```

#### <a name="response-2"></a><span data-ttu-id="b44a2-196">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="b44a2-196">Response 2</span></span>

<span data-ttu-id="b44a2-197">El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="b44a2-197">The following is an example of the response when using `deltaLink` obtained from the query initialization.</span></span> <span data-ttu-id="b44a2-198">Tenga en cuenta que `description` y `mailNickname` tienen el valor de `null` lo que significa que es posible que no se han cambiado o se han establecido en un valor vacío.</span><span class="sxs-lookup"><span data-stu-id="b44a2-198">Note that `description` and `mailNickname` have the value of `null` which means that they may have not changed or have been set to an empty value.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.group",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups",
  "@odata.nextLink":"https://graph.microsoft.com/v1.0/groups/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjsXoYQp_dpA3cNJWc",
  "value": [
    {
      "displayName": "displayName-value",
      "description": null,
      "mailNickname": null
    }
  ]
}
```

#### <a name="request-3"></a><span data-ttu-id="b44a2-199">Solicitud 3</span><span class="sxs-lookup"><span data-stu-id="b44a2-199">Request 3</span></span>

<span data-ttu-id="b44a2-200">En el ejemplo siguiente se muestra la solicitud inicial seleccionando 3 propiedades para el seguimiento de cambios, con el comportamiento de respuesta mínimo alternativo:</span><span class="sxs-lookup"><span data-stu-id="b44a2-200">The next example shows the initial request selecting 3 properties for change tracking, with alternative minimal response behavior:</span></span>
<!-- {
  "blockType": "request",
  "name": "group_delta"
}-->

```http
GET https://graph.microsoft.com/v1.0/groups/delta?$select=displayName,description,mailNickname
Prefer: return=minimal
```

#### <a name="response-3"></a><span data-ttu-id="b44a2-201">Respuesta 3</span><span class="sxs-lookup"><span data-stu-id="b44a2-201">Response 3</span></span>

<span data-ttu-id="b44a2-202">El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="b44a2-202">The following is an example of the response when using `deltaLink` obtained from the query initialization.</span></span> <span data-ttu-id="b44a2-203">Tenga en cuenta que el `mailNickname` (propiedad) no se incluye, lo que significa que no ha cambiado desde la última consulta delta; `displayName` y `description` se incluyen lo que significa que se han cambiado sus valores.</span><span class="sxs-lookup"><span data-stu-id="b44a2-203">Note that the `mailNickname` property is not included, which means it has not changed since the last delta query; `displayName` and `description` are included which means their values have changed.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.group",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups",
  "@odata.nextLink":"https://graph.microsoft.com/v1.0/groups/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjsXoYQp_dpA3cNJWc",
  "value": [
    {
      "displayName": "displayName-value",
      "description": null
    }
  ]
}
```

## <a name="see-also"></a><span data-ttu-id="b44a2-204">Vea también</span><span class="sxs-lookup"><span data-stu-id="b44a2-204">See also</span></span>

- <span data-ttu-id="b44a2-205">[Consulta de delta de uso para realizar un seguimiento de los cambios en datos de Microsoft Graph](../../../concepts/delta_query_overview.md).</span><span class="sxs-lookup"><span data-stu-id="b44a2-205">[Use delta query to track changes in Microsoft Graph data](../../../concepts/delta_query_overview.md).</span></span>
- <span data-ttu-id="b44a2-206">[Obtener los cambios incrementales de grupos](../../../concepts/delta_query_groups.md).</span><span class="sxs-lookup"><span data-stu-id="b44a2-206">[Get incremental changes for groups](../../../concepts/delta_query_groups.md).</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
