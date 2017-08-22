# <a name="user-delta"></a><span data-ttu-id="1c1a5-101">user: delta</span><span class="sxs-lookup"><span data-stu-id="1c1a5-101">user: delta</span></span>

<span data-ttu-id="1c1a5-p101">La [consulta delta](../../../concepts/delta_query_overview.md) permite a las aplicaciones detectar entidades recién creadas, actualizadas o eliminadas sin realizar una operación de lectura completa del recurso de destino con cada solicitud. Para detectar cambios en los usuarios, realice una solicitud usando la función *delta*. Consulte [Usar la consulta delta](../../../concepts/delta_query_overview.md) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="1c1a5-p101">[Delta query](../../../concepts/delta_query_overview.md) enables applications to discover newly created, updated, or deleted entities without performing a full read of the target resource with every request. To discover changes to users, perform a request using the *delta* function. See [Using Delta Query](../../../concepts/delta_query_overview.md) for details.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1c1a5-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1c1a5-105">Prerequisites</span></span>

<span data-ttu-id="1c1a5-106">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *User.Read; User.ReadWrite; User.ReadBasic.All; User.Read.All; User.ReadWrite.All; Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="1c1a5-106">One of the following **scopes** is required to execute this API: *User.Read; User.ReadWrite; User.ReadBasic.All; User.Read.All; User.ReadWrite.All; Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="1c1a5-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1c1a5-107">HTTP request</span></span>

<span data-ttu-id="1c1a5-108">Para comenzar los cambios, debe realizar una solicitud incluyendo la función delta en el recurso de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="1c1a5-108">To begin tracking changes, you make a request including the delta function on the users resource.</span></span> 

<!-- { "blockType": "ignored" } -->
```http
GET /users/delta
```

### <a name="query-parameters"></a><span data-ttu-id="1c1a5-109">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="1c1a5-109">Query parameters</span></span>

<span data-ttu-id="1c1a5-p102">El seguimiento de cambios en los usuarios conlleva al menos una llamada de una función **delta**. Si usa cualquier parámetro de consulta (distinto de `$deltatoken` y `$skiptoken`), debe especificarlo en la solicitud **delta** inicial. Microsoft Graph codifica automáticamente cualquier parámetro especificado en la parte del token de la URL `nextLink` o `deltaLink` proporcionada en la respuesta. Solo debe especificar los parámetros de consulta deseados una vez por adelantado. En solicitudes posteriores, copie y aplique la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.</span><span class="sxs-lookup"><span data-stu-id="1c1a5-p102">Tracking changes in users incurs a round of one or more **delta** function calls. If you use any query parameter (other than `$deltatoken` and `$skiptoken`), you must specify it in the initial **delta** request. Microsoft Graph automatically encodes any specified parameters into the token portion of the `nextLink` or `deltaLink` URL provided in the response. You only need to specify any desired query parameters once upfront. In subsequent requests, copy and apply the `nextLink` or `deltaLink` URL from the previous response, as that URL already includes the encoded, desired parameters.</span></span>

| <span data-ttu-id="1c1a5-115">Parámetro de consulta</span><span class="sxs-lookup"><span data-stu-id="1c1a5-115">Query parameter</span></span>      | <span data-ttu-id="1c1a5-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="1c1a5-116">Type</span></span>   |<span data-ttu-id="1c1a5-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c1a5-117">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="1c1a5-118">$deltatoken</span><span class="sxs-lookup"><span data-stu-id="1c1a5-118">$deltatoken</span></span> | <span data-ttu-id="1c1a5-119">string</span><span class="sxs-lookup"><span data-stu-id="1c1a5-119">string</span></span> | <span data-ttu-id="1c1a5-p103">Un [token de estado](../../../concepts/delta_query_overview.md) que se devuelve en la dirección URL de `deltaLink` de la llamada de función **delta** anterior para la misma colección de usuarios. Indica el progreso de la ronda de seguimiento de cambios. Guarde y aplique toda la dirección URL `deltaLink`, incluido este token, en la primera solicitud de la siguiente ronda de seguimiento de cambios de la colección.</span><span class="sxs-lookup"><span data-stu-id="1c1a5-p103">A [state token](../../../concepts/delta_query_overview.md) returned in the `deltaLink` URL of the previous **delta** function call for the same user collection, indicating the completion of that round of change tracking. Save and apply the entire `deltaLink` URL including this token in the first request of the next round of change tracking for that collection.</span></span>|
| <span data-ttu-id="1c1a5-122">$skiptoken</span><span class="sxs-lookup"><span data-stu-id="1c1a5-122">$skiptoken</span></span> | <span data-ttu-id="1c1a5-123">string</span><span class="sxs-lookup"><span data-stu-id="1c1a5-123">string</span></span> | <span data-ttu-id="1c1a5-124">Un [token de estado](../../../concepts/delta_query_overview.md) que se devuelve en la dirección URL de `nextLink` de la llamada de función **delta**. Indica que debe realizarse el seguimiento de más cambios en la misma colección de usuarios.</span><span class="sxs-lookup"><span data-stu-id="1c1a5-124">A [state token](../../../concepts/delta_query_overview.md) returned in the `nextLink` URL of the previous **delta** function call, indicating there are further changes to be tracked in the same user collection.</span></span> |

## <a name="optional-query-parameters"></a><span data-ttu-id="1c1a5-125">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1c1a5-125">Optional query parameters</span></span>

<span data-ttu-id="1c1a5-126">Este método admite parámetros de consulta de OData a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1c1a5-126">This method supports OData Query Parameters to help customize the response.</span></span>

- <span data-ttu-id="1c1a5-p104">Puede utilizar un parámetro de consulta `$select` como en cualquier solicitud GET para especificar solo las propiedades que necesita para un mejor rendimiento. Siempre se devuelve la propiedad _id_.</span><span class="sxs-lookup"><span data-stu-id="1c1a5-p104">You can use a `$select` query parameter as in any GET request to specify only the properties your need for best performance. The _id_ property is always returned.</span></span> 
- <span data-ttu-id="1c1a5-129">Compatibilidad con consultas de delta `$select`, `$top` y `$expand` para los mensajes.</span><span class="sxs-lookup"><span data-stu-id="1c1a5-129">Delta query support `$select`, `$top`, and `$expand` for messages.</span></span> 
- <span data-ttu-id="1c1a5-p105">Hay compatibilidad limitada para `$orderby`: La única expresión `$orderby` admitida es `$orderby=receivedDateTime+desc`. Si no incluye ninguna expresión `$orderby`, no se garantizará el orden de devolución.</span><span class="sxs-lookup"><span data-stu-id="1c1a5-p105">There is limited support for `$orderby`: The only supported `$orderby` expression is `$orderby=receivedDateTime+desc`. If you do not include  an `$orderby` expression, the return order is not guaranteed.</span></span> 
- <span data-ttu-id="1c1a5-132">No hay compatibilidad con `$search`.</span><span class="sxs-lookup"><span data-stu-id="1c1a5-132">There is no support for `$search`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="1c1a5-133">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1c1a5-133">Request headers</span></span>
| <span data-ttu-id="1c1a5-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="1c1a5-134">Name</span></span>       | <span data-ttu-id="1c1a5-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c1a5-135">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="1c1a5-136">Authorization</span><span class="sxs-lookup"><span data-stu-id="1c1a5-136">Authorization</span></span>  | <span data-ttu-id="1c1a5-137">&lt;token&gt; de portador</span><span class="sxs-lookup"><span data-stu-id="1c1a5-137">Bearer &lt;token&gt;</span></span>|
| <span data-ttu-id="1c1a5-138">Content-Type</span><span class="sxs-lookup"><span data-stu-id="1c1a5-138">Content-Type</span></span>  | <span data-ttu-id="1c1a5-139">application/json</span><span class="sxs-lookup"><span data-stu-id="1c1a5-139">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="1c1a5-140">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1c1a5-140">Request body</span></span>
<span data-ttu-id="1c1a5-141">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1c1a5-141">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1c1a5-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1c1a5-142">Response</span></span>

<span data-ttu-id="1c1a5-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto de colección [user](../resources/user.md) en el cuerpo de la respuesta. La respuesta también incluye una dirección URL nextLink o deltaLink.</span><span class="sxs-lookup"><span data-stu-id="1c1a5-p106">If successful, this method returns `200, OK` response code and [user](../resources/user.md) collection object in the response body. The response also includes a nextLink URL or a deltaLink URL.</span></span> 

- <span data-ttu-id="1c1a5-p107">Si se devuelve una dirección URL nextLink, hay más páginas de datos para recuperar en la sesión. La aplicación continúa realizando solicitudes mediante la dirección URL nextLink hasta que se incluya una dirección URL deltaLink en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1c1a5-p107">If a nextLink URL is returned, there are additional pages of data to be retrieved in the session. The application continues making requests using the nextLink URL until a deltaLink URL is included in the response.</span></span>

- <span data-ttu-id="1c1a5-p108">Si se devuelve la dirección URL deltaLink, no hay que devolver más datos sobre el estado existente del recurso. En solicitudes futuras, la aplicación usa la dirección URL deltaLink para obtener información sobre los cambios en el recurso.</span><span class="sxs-lookup"><span data-stu-id="1c1a5-p108">If a deltaLink URL is returned, there is no more data about the existing state of the resource to be returned. For future requests, the application uses the deltaLink URL to learn about changes to the resource.</span></span>

<span data-ttu-id="1c1a5-149">Vea:</span><span class="sxs-lookup"><span data-stu-id="1c1a5-149">See:</span></span></br>
- <span data-ttu-id="1c1a5-150">[Usar la consulta delta](../../../concepts/delta_query_overview.md) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="1c1a5-150">[Using Delta Query](../../../concepts/delta_query_overview.md) for more details</span></span></br>
- <span data-ttu-id="1c1a5-151">[Obtener los cambios incrementales de usuarios](../../../concepts/delta_query_users.md) para obtener un ejemplo de solicitud.</span><span class="sxs-lookup"><span data-stu-id="1c1a5-151">[Get incremental changes for users](../../../concepts/delta_query_users.md) for an example requests.</span></span></br>

## <a name="example"></a><span data-ttu-id="1c1a5-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1c1a5-152">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1c1a5-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1c1a5-153">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "user_delta"
}-->
```http
GET https://graph.microsoft.com/v1.0/users/delta
```

##### <a name="response"></a><span data-ttu-id="1c1a5-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1c1a5-154">Response</span></span>
<span data-ttu-id="1c1a5-p109">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1c1a5-p109">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->