# <a name="user-delta"></a><span data-ttu-id="4a542-101">user: delta</span><span class="sxs-lookup"><span data-stu-id="4a542-101">user: delta</span></span>

<span data-ttu-id="4a542-102">Get recién creado, actualiza o elimina los usuarios sin tener que realizar un acceso completo de lectura de la colección completa de usuario.</span><span class="sxs-lookup"><span data-stu-id="4a542-102">Get newly created, updated, or deleted users without having to perform a full read of the entire user collection.</span></span> <span data-ttu-id="4a542-103">Para obtener información detallada, vea [control de cambios](../../../concepts/delta_query_overview.md) .</span><span class="sxs-lookup"><span data-stu-id="4a542-103">See [Track changes](../../../concepts/delta_query_overview.md) for details.</span></span>

## <a name="permissions"></a><span data-ttu-id="4a542-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="4a542-104">Permissions</span></span>

<span data-ttu-id="4a542-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="4a542-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="4a542-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4a542-107">Permission type</span></span>      | <span data-ttu-id="4a542-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4a542-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4a542-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4a542-109">Delegated (work or school account)</span></span> | <span data-ttu-id="4a542-110">User.Read, User.ReadWrite, User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="4a542-110">User.Read, User.ReadWrite, User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="4a542-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4a542-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4a542-112">User.Read, User.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4a542-112">User.Read, User.ReadWrite</span></span>    |
|<span data-ttu-id="4a542-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4a542-113">Application</span></span> | <span data-ttu-id="4a542-114">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4a542-114">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="4a542-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4a542-115">HTTP request</span></span>

<span data-ttu-id="4a542-116">Para comenzar los cambios, debe realizar una solicitud incluyendo la función delta en el recurso de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="4a542-116">To begin tracking changes, you make a request including the delta function on the users resource.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /users/delta
```

## <a name="query-parameters"></a><span data-ttu-id="4a542-117">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="4a542-117">Query parameters</span></span>

<span data-ttu-id="4a542-118">Seguimiento de los cambios en los usuarios incurre en una ronda de una o más llamadas de función de **delta** .</span><span class="sxs-lookup"><span data-stu-id="4a542-118">Tracking changes in users incurs a round of one or more **delta** function calls.</span></span> <span data-ttu-id="4a542-119">Si usa cualquier parámetro de consulta (distinto de `$deltatoken` y `$skiptoken`), debe especificar en la solicitud inicial del **delta** .</span><span class="sxs-lookup"><span data-stu-id="4a542-119">If you use any query parameter (other than `$deltatoken` and `$skiptoken`), you must specify it in the initial **delta** request.</span></span> <span data-ttu-id="4a542-120">Microsoft Graph codifica automáticamente los parámetros especificados en la parte de símbolo (token) de la `nextLink` o `deltaLink` dirección URL proporcionada en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4a542-120">Microsoft Graph automatically encodes any specified parameters into the token portion of the `nextLink` or `deltaLink` URL provided in the response.</span></span>

<span data-ttu-id="4a542-121">Solo debe especificar una vez por adelantado los parámetros de consulta deseados.</span><span class="sxs-lookup"><span data-stu-id="4a542-121">You only need to specify any desired query parameters once upfront.</span></span>

<span data-ttu-id="4a542-122">En solicitudes posteriores, copie y aplique la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.</span><span class="sxs-lookup"><span data-stu-id="4a542-122">In subsequent requests, copy and apply the `nextLink` or `deltaLink` URL from the previous response, as that URL already includes the encoded, desired parameters.</span></span>

| <span data-ttu-id="4a542-123">Parámetro de consulta</span><span class="sxs-lookup"><span data-stu-id="4a542-123">Query parameter</span></span>      | <span data-ttu-id="4a542-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="4a542-124">Type</span></span>   |<span data-ttu-id="4a542-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a542-125">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="4a542-126">$deltatoken</span><span class="sxs-lookup"><span data-stu-id="4a542-126">$deltatoken</span></span> | <span data-ttu-id="4a542-127">string</span><span class="sxs-lookup"><span data-stu-id="4a542-127">string</span></span> | <span data-ttu-id="4a542-p104">Un [token de estado](../../../concepts/delta_query_overview.md) que se devuelve en la dirección URL de `deltaLink` de la llamada de función **delta** anterior para la misma colección de usuarios. Indica el progreso de la ronda de seguimiento de cambios. Guarde y aplique toda la dirección URL `deltaLink`, incluido este token, en la primera solicitud de la siguiente ronda de seguimiento de cambios de la colección.</span><span class="sxs-lookup"><span data-stu-id="4a542-p104">A [state token](../../../concepts/delta_query_overview.md) returned in the `deltaLink` URL of the previous **delta** function call for the same user collection, indicating the completion of that round of change tracking. Save and apply the entire `deltaLink` URL including this token in the first request of the next round of change tracking for that collection.</span></span>|
| <span data-ttu-id="4a542-130">$skiptoken</span><span class="sxs-lookup"><span data-stu-id="4a542-130">$skiptoken</span></span> | <span data-ttu-id="4a542-131">string</span><span class="sxs-lookup"><span data-stu-id="4a542-131">string</span></span> | <span data-ttu-id="4a542-132">Un [token de estado](../../../concepts/delta_query_overview.md) que se devuelve en la dirección URL de `nextLink` de la llamada de función **delta**. Indica que debe realizarse el seguimiento de más cambios en la misma colección de usuarios.</span><span class="sxs-lookup"><span data-stu-id="4a542-132">A [state token](../../../concepts/delta_query_overview.md) returned in the `nextLink` URL of the previous **delta** function call, indicating there are further changes to be tracked in the same user collection.</span></span> |

### <a name="odata-query-parameters"></a><span data-ttu-id="4a542-133">Parámetros de consulta de OData</span><span class="sxs-lookup"><span data-stu-id="4a542-133">OData query parameters</span></span>

<span data-ttu-id="4a542-134">Este método es compatible con parámetros opcionales de consulta de OData para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4a542-134">This method supports optional OData Query Parameters to help customize the response.</span></span>

- <span data-ttu-id="4a542-p105">Puede utilizar un parámetro de consulta `$select` como en cualquier solicitud GET para especificar solo las propiedades que necesita para un mejor rendimiento. Siempre se devuelve la propiedad *id*.</span><span class="sxs-lookup"><span data-stu-id="4a542-p105">You can use a `$select` query parameter as in any GET request to specify only the properties your need for best performance. The *id* property is always returned.</span></span>
- <span data-ttu-id="4a542-137">No hay compatibilidad limitada para `$filter`:</span><span class="sxs-lookup"><span data-stu-id="4a542-137">There is limited support for `$filter`:</span></span>
  - <span data-ttu-id="4a542-138">La única expresión `$filter` admitida es para realizar un seguimiento de los cambios en un objeto específico: `$filter=id+eq+{value}`.</span><span class="sxs-lookup"><span data-stu-id="4a542-138">The only supported `$filter` expression is for tracking changes on a specific object: `$filter=id+eq+{value}`.</span></span> <span data-ttu-id="4a542-139">Puede filtrar varios objetos.</span><span class="sxs-lookup"><span data-stu-id="4a542-139">You can filter multiple objects.</span></span> <span data-ttu-id="4a542-140">Por ejemplo, `https://graph.microsoft.com/v1.0/users/delta/?$filter= id eq '477e9fc6-5de7-4406-bb2a-7e5c83c9ffff' or id eq '004d6a07-fe70-4b92-add5-e6e37b8affff'`.</span><span class="sxs-lookup"><span data-stu-id="4a542-140">For example, `https://graph.microsoft.com/v1.0/users/delta/?$filter= id eq '477e9fc6-5de7-4406-bb2a-7e5c83c9ffff' or id eq '004d6a07-fe70-4b92-add5-e6e37b8affff'`.</span></span> <span data-ttu-id="4a542-141">Hay un límite de 50 objetos filtrados.</span><span class="sxs-lookup"><span data-stu-id="4a542-141">There is a limit of 50 filtered objects.</span></span>

## <a name="request-headers"></a><span data-ttu-id="4a542-142">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4a542-142">Request headers</span></span>
| <span data-ttu-id="4a542-143">Nombre</span><span class="sxs-lookup"><span data-stu-id="4a542-143">Name</span></span>       | <span data-ttu-id="4a542-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a542-144">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="4a542-145">Authorization</span><span class="sxs-lookup"><span data-stu-id="4a542-145">Authorization</span></span>  | <span data-ttu-id="4a542-146">&lt;token&gt; de portador</span><span class="sxs-lookup"><span data-stu-id="4a542-146">Bearer &lt;token&gt;</span></span>|
| <span data-ttu-id="4a542-147">Content-Type</span><span class="sxs-lookup"><span data-stu-id="4a542-147">Content-Type</span></span>  | <span data-ttu-id="4a542-148">application/json</span><span class="sxs-lookup"><span data-stu-id="4a542-148">application/json</span></span> |
| <span data-ttu-id="4a542-149">Prefer</span><span class="sxs-lookup"><span data-stu-id="4a542-149">Prefer</span></span> | <span data-ttu-id="4a542-150">devolver = mínimo</span><span class="sxs-lookup"><span data-stu-id="4a542-150">return=minimal</span></span> <br><br><span data-ttu-id="4a542-151">Si se especifica este encabezado con una solicitud que utiliza un `deltaLink` devolvería sólo las propiedades del objeto que han cambiado desde la última round.</span><span class="sxs-lookup"><span data-stu-id="4a542-151">Specifying this header with a request that uses a `deltaLink` would return only the object properties that have changed since the last round.</span></span> <span data-ttu-id="4a542-152">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4a542-152">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4a542-153">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4a542-153">Request body</span></span>
<span data-ttu-id="4a542-154">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4a542-154">Do not supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="4a542-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4a542-155">Response</span></span>

<span data-ttu-id="4a542-156">Si tiene éxito, este método devuelve `200 OK` objeto de colección de respuesta código y [usuario](../resources/user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4a542-156">If successful, this method returns `200 OK` response code and [user](../resources/user.md) collection object in the response body.</span></span> <span data-ttu-id="4a542-157">La respuesta incluye también un `nextLink` dirección URL o un `deltaLink` dirección URL.</span><span class="sxs-lookup"><span data-stu-id="4a542-157">The response also includes a `nextLink` URL or a `deltaLink` URL.</span></span>

- <span data-ttu-id="4a542-158">Si un `nextLink` se devuelve la dirección URL:</span><span class="sxs-lookup"><span data-stu-id="4a542-158">If a `nextLink` URL is returned:</span></span>
  - <span data-ttu-id="4a542-159">Esto indica que hay páginas adicionales de datos que se recuperarán en la sesión.</span><span class="sxs-lookup"><span data-stu-id="4a542-159">This indicates there are additional pages of data to be retrieved in the session.</span></span> <span data-ttu-id="4a542-160">La aplicación continúa realizar solicitudes mediante el `nextLink` dirección URL hasta un `deltaLink` dirección URL se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4a542-160">The application continues making requests using the `nextLink` URL until a `deltaLink` URL is included in the response.</span></span>
  - <span data-ttu-id="4a542-161">La respuesta incluye el mismo conjunto de propiedades como se muestra en la solicitud de consulta delta inicial.</span><span class="sxs-lookup"><span data-stu-id="4a542-161">The response includes the same set of properties as in the initial delta query request.</span></span> <span data-ttu-id="4a542-162">Esto le permite capturar el estado actual y completa de los objetos al iniciar el ciclo de delta.</span><span class="sxs-lookup"><span data-stu-id="4a542-162">This allows you to capture the full current state of the objects when initiating the delta cycle.</span></span>

- <span data-ttu-id="4a542-163">Si un `deltaLink` se devuelve la dirección URL:</span><span class="sxs-lookup"><span data-stu-id="4a542-163">If a `deltaLink` URL is returned:</span></span>
  - <span data-ttu-id="4a542-164">Esto indica que no hay ningún dato más sobre el estado existente del recurso que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="4a542-164">This indicates there is no more data about the existing state of the resource to be returned.</span></span> <span data-ttu-id="4a542-165">Guardar y utilizar el `deltaLink` dirección URL para obtener más información acerca de cambia para el recurso en la ronda siguiente.</span><span class="sxs-lookup"><span data-stu-id="4a542-165">Save and use the `deltaLink` URL to learn about changes to the resource in the next round.</span></span>
  - <span data-ttu-id="4a542-166">Tiene una opción para especificar el `Prefer:return=minimal` encabezado, que se incluirá en los valores de respuesta sólo para las propiedades que han cambiado desde el momento en que el `deltaLink` se emitió.</span><span class="sxs-lookup"><span data-stu-id="4a542-166">You have a choice to specify the `Prefer:return=minimal` header, to include in the response values for only the properties that have changed since the time the `deltaLink` was issued.</span></span>

#### <a name="default-return-the-same-properties-as-initial-delta-request"></a><span data-ttu-id="4a542-167">Valor predeterminado: devolver las mismas propiedades que la solicitud inicial del delta</span><span class="sxs-lookup"><span data-stu-id="4a542-167">Default: return the same properties as initial delta request</span></span>

<span data-ttu-id="4a542-168">De forma predeterminada, las solicitudes con un `deltaLink` o `nextLink` devolver las mismas propiedades como seleccionado en la consulta inicial del delta de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="4a542-168">By default, requests using a `deltaLink` or `nextLink` return the same properties as selected in the initial delta query in the following ways:</span></span>

- <span data-ttu-id="4a542-169">Si la propiedad ha cambiado, devuelva la propiedad en la respuesta JSON.</span><span class="sxs-lookup"><span data-stu-id="4a542-169">If the property has changed, return the property in the JSON response.</span></span>
- <span data-ttu-id="4a542-170">Si se ha establecido la propiedad en un valor vacío, devuelve el valor de la propiedad como null.</span><span class="sxs-lookup"><span data-stu-id="4a542-170">If the property has been set to an empty value, return the property value as null.</span></span>
- <span data-ttu-id="4a542-171">Si la propiedad no ha cambiado, devolver el valor como null.</span><span class="sxs-lookup"><span data-stu-id="4a542-171">If the property has not changed, return the value as null.</span></span>

> <span data-ttu-id="4a542-172">**Nota:** Con el comportamiento anterior, no es posible diferenciar entre una propiedad que no ha cambiado y uno que ha cambiado a un `null` valor.</span><span class="sxs-lookup"><span data-stu-id="4a542-172">**Note:** With the above behavior, it is not possible to differentiate between a property that has not changed and one that has changed to a `null` value.</span></span> <span data-ttu-id="4a542-173">Vea el [segundo ejemplo](#request-2) siguiente.</span><span class="sxs-lookup"><span data-stu-id="4a542-173">See the [second example](#request-2) below.</span></span> <span data-ttu-id="4a542-174">Si esto es importante, se recomienda usar el comportamiento alternativo que se describen en la siguiente sección.</span><span class="sxs-lookup"><span data-stu-id="4a542-174">If this is important, we recommend using the alternative behavior described in the next section.</span></span>

#### <a name="alternative-return-only-the-changed-properties"></a><span data-ttu-id="4a542-175">Alternativa: devolver sólo las propiedades modificadas</span><span class="sxs-lookup"><span data-stu-id="4a542-175">Alternative: return only the changed properties</span></span>

<span data-ttu-id="4a542-176">Adición de un encabezado de solicitud opcional - `prefer:return=minimal` -da como resultado el siguiente comportamiento:</span><span class="sxs-lookup"><span data-stu-id="4a542-176">Adding an optional request header - `prefer:return=minimal` - results in the following behavior:</span></span>

- <span data-ttu-id="4a542-177">Si la propiedad ha cambiado, devuelva la propiedad en la respuesta JSON.</span><span class="sxs-lookup"><span data-stu-id="4a542-177">If the property has changed, return the property in the JSON response.</span></span>
- <span data-ttu-id="4a542-178">Si se ha establecido la propiedad en un valor vacío, devuelve el valor de la propiedad como null.</span><span class="sxs-lookup"><span data-stu-id="4a542-178">If the property has been set to an empty value, return the property value as null.</span></span>
- <span data-ttu-id="4a542-179">Si la propiedad no ha cambiado, no incluya la propiedad en la respuesta JSON.</span><span class="sxs-lookup"><span data-stu-id="4a542-179">If the property has not changed, do not include the property in the JSON response.</span></span> <span data-ttu-id="4a542-180">(Distinto del comportamiento predeterminado).</span><span class="sxs-lookup"><span data-stu-id="4a542-180">(Different from the default behavior.)</span></span>

> <span data-ttu-id="4a542-181">**Nota:** El encabezado puede agregarse a un `deltaLink` solicitud en cualquier momento en el ciclo de delta.</span><span class="sxs-lookup"><span data-stu-id="4a542-181">**Note:** The header can be added to a `deltaLink` request at any point in time in the delta cycle.</span></span> <span data-ttu-id="4a542-182">El encabezado sólo afecta el conjunto de propiedades que se incluyen en la respuesta y no afecta a cómo se ejecuta la consulta de delta.</span><span class="sxs-lookup"><span data-stu-id="4a542-182">The header only affects the set of properties included in the response and it does not affect how the delta query is executed.</span></span> <span data-ttu-id="4a542-183">Vea el [tercer ejemplo](#request-3) siguiente.</span><span class="sxs-lookup"><span data-stu-id="4a542-183">See the [third example](#request-3) below.</span></span>

### <a name="example"></a><span data-ttu-id="4a542-184">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4a542-184">Example</span></span>

#### <a name="request-1"></a><span data-ttu-id="4a542-185">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="4a542-185">Request 1</span></span>

<span data-ttu-id="4a542-186">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4a542-186">The following is an example of the request.</span></span> <span data-ttu-id="4a542-187">No hay ningún `$select` parámetro, por lo que se realiza un seguimiento y devuelve un conjunto predeterminado de propiedades.</span><span class="sxs-lookup"><span data-stu-id="4a542-187">There is no `$select` parameter, so a default set of properties is tracked and returned.</span></span>
<!-- {
  "blockType": "request",
  "name": "user_delta"
}-->

```http
GET https://graph.microsoft.com/v1.0/users/delta
```

#### <a name="response-1"></a><span data-ttu-id="4a542-188">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="4a542-188">Response 1</span></span>

<span data-ttu-id="4a542-189">El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="4a542-189">The following is an example of the response when using `deltaLink` obtained from the query initialization.</span></span>

><span data-ttu-id="4a542-p116">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4a542-p116">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users",
  "@odata.nextLink":"https://graph.microsoft.com/v1.0/users/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjsXoYQp_dpA3cNJWc",
  "value": [
    {
      "businessPhones": [
          "businessPhones-value"
      ],
      "displayName": "displayName-value",
      "givenName": "givenName-value",
      "jobTitle": "jobTitle-value",
      "mail": "mail-value",
      "mobilePhone": "mobilePhone-value",
      "officeLocation": "officeLocation-value",
      "preferredLanguage": "preferredLanguage-value",
      "surname": "surname-value",
      "userPrincipalName": "userPrincipalName-value",
      "id": "id-value"
    }
  ]
}
```

#### <a name="request-2"></a><span data-ttu-id="4a542-192">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="4a542-192">Request 2</span></span>

<span data-ttu-id="4a542-193">En el ejemplo siguiente se muestra la solicitud inicial seleccionando 3 propiedades para el seguimiento de cambios, con comportamiento de respuesta predeterminado:</span><span class="sxs-lookup"><span data-stu-id="4a542-193">The next example shows the initial request selecting 3 properties for change tracking, with default response behavior:</span></span>
<!-- {
  "blockType": "request",
  "name": "user_delta"
}-->

```http
GET https://graph.microsoft.com/v1.0/users/delta?$select=displayName,jobTitle,mobilePhone
```

#### <a name="response-2"></a><span data-ttu-id="4a542-194">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="4a542-194">Response 2</span></span>

<span data-ttu-id="4a542-195">El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="4a542-195">The following is an example of the response when using `deltaLink` obtained from the query initialization.</span></span> <span data-ttu-id="4a542-196">Tenga en cuenta que `jobTitle` y `mobilePhone` tienen el valor de `null` lo que significa que es posible que no se han cambiado o se han establecido en un valor vacío.</span><span class="sxs-lookup"><span data-stu-id="4a542-196">Note that `jobTitle` and `mobilePhone` have the value of `null` which means that they may have not changed or have been set to an empty value.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users",
  "@odata.nextLink":"https://graph.microsoft.com/v1.0/users/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjsXoYQp_dpA3cNJWc",
  "value": [
    {
      "displayName": "displayName-value",
      "jobTitle": null,
      "mobilePhone": null
    }
  ]
}
```

#### <a name="request-3"></a><span data-ttu-id="4a542-197">Solicitud 3</span><span class="sxs-lookup"><span data-stu-id="4a542-197">Request 3</span></span>

<span data-ttu-id="4a542-198">En el ejemplo siguiente se muestra la solicitud inicial seleccionando 3 propiedades para el seguimiento de cambios, con el comportamiento de respuesta mínimo alternativo:</span><span class="sxs-lookup"><span data-stu-id="4a542-198">The next example shows the initial request selecting 3 properties for change tracking, with alternative minimal response behavior:</span></span>
<!-- {
  "blockType": "request",
  "name": "user_delta"
}-->

```http
GET https://graph.microsoft.com/v1.0/users/delta?$select=displayName,jobTitle,mobilePhone
Prefer: return=minimal
```

#### <a name="response-3"></a><span data-ttu-id="4a542-199">Respuesta 3</span><span class="sxs-lookup"><span data-stu-id="4a542-199">Response 3</span></span>

<span data-ttu-id="4a542-200">El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="4a542-200">The following is an example of the response when using `deltaLink` obtained from the query initialization.</span></span> <span data-ttu-id="4a542-201">Tenga en cuenta que el `mobilePhone` (propiedad) no se incluye, lo que significa que no ha cambiado desde la última consulta delta; `displayName` y `jobTitle` se incluyen lo que significa que se han cambiado sus valores.</span><span class="sxs-lookup"><span data-stu-id="4a542-201">Note that the `mobilePhone` property is not included, which means it has not changed since the last delta query; `displayName` and `jobTitle` are included which means their values have changed.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users",
  "@odata.nextLink":"https://graph.microsoft.com/v1.0/users/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjsXoYQp_dpA3cNJWc",
  "value": [
    {
      "displayName": "displayName-value",
      "jobTitle": null
    }
  ]
}
```

- <span data-ttu-id="4a542-202">[Consulta de delta de uso para realizar un seguimiento de los cambios en datos de Microsoft Graph](../../../concepts/delta_query_overview.md).</span><span class="sxs-lookup"><span data-stu-id="4a542-202">[Use delta query to track changes in Microsoft Graph data](../../../concepts/delta_query_overview.md).</span></span>
- <span data-ttu-id="4a542-203">[Obtener cambios incrementales para los usuarios](../../../concepts/delta_query_users.md).</span><span class="sxs-lookup"><span data-stu-id="4a542-203">[Get incremental changes for users](../../../concepts/delta_query_users.md).</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->