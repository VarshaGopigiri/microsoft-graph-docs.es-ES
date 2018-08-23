# <a name="group-delta"></a><span data-ttu-id="ac58e-101">grupo: delta</span><span class="sxs-lookup"><span data-stu-id="ac58e-101">group: delta</span></span>
<span data-ttu-id="ac58e-p101">La [consulta delta](../../../concepts/delta_query_overview.md) permite a las aplicaciones detectar entidades recién creadas, actualizadas o eliminadas sin realizar una operación de lectura completa del recurso de destino con cada solicitud. Para detectar cambios en grupos, realice una solicitud usando la función *delta*. Consulte [Usar la consulta delta](../../../concepts/delta_query_overview.md) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="ac58e-p101">[Delta query](../../../concepts/delta_query_overview.md) enables applications to discover newly created, updated, or deleted entities without performing a full read of the target resource with every request. To discover changes to groups, perform a request using the *delta* function. See [Using Delta Query](../../../concepts/delta_query_overview.md) for details.</span></span>

## <a name="permissions"></a><span data-ttu-id="ac58e-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="ac58e-105">Permissions</span></span>
<span data-ttu-id="ac58e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ac58e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ac58e-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ac58e-108">Permission type</span></span>      | <span data-ttu-id="ac58e-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ac58e-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ac58e-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ac58e-110">Delegated (work or school account)</span></span> | <span data-ttu-id="ac58e-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ac58e-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="ac58e-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ac58e-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ac58e-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ac58e-113">Not supported.</span></span>    |
|<span data-ttu-id="ac58e-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ac58e-114">Application</span></span> | <span data-ttu-id="ac58e-115">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ac58e-115">Group.Read.All, Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="ac58e-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ac58e-116">HTTP request</span></span>
<span data-ttu-id="ac58e-117">Para comenzar los cambios, debe realizar una solicitud incluyendo la función delta en el recurso grupo.</span><span class="sxs-lookup"><span data-stu-id="ac58e-117">To begin tracking changes, you make a request including the delta function on the groups resource.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /groups/delta
```

## <a name="query-parameters"></a><span data-ttu-id="ac58e-118">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="ac58e-118">Query parameters</span></span>
<span data-ttu-id="ac58e-p103">El seguimiento de cambios en grupos conlleva al menos una llamada de una función **delta**. Si usa cualquier parámetro de consulta (uno diferente a `$deltatoken` y `$skiptoken`), debe especificarlo en la solicitud **delta** inicial. Microsoft Graph codifica automáticamente cualquier parámetro especificado en la parte del token de la URL `nextLink` o `deltaLink` proporcionada en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ac58e-p103">Tracking changes in groups incurs a round of one or more **delta** function calls. If you use any query parameter (other than `$deltatoken` and `$skiptoken`), you must specify it in the initial **delta** request. Microsoft Graph automatically encodes any specified parameters into the token portion of the `nextLink` or `deltaLink` URL provided in the response.</span></span>

<span data-ttu-id="ac58e-122">Solo debe especificar una vez por adelantado los parámetros de consulta deseados.</span><span class="sxs-lookup"><span data-stu-id="ac58e-122">You only need to specify any desired query parameters once upfront.</span></span>

<span data-ttu-id="ac58e-123">En solicitudes posteriores, copie y aplique la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.</span><span class="sxs-lookup"><span data-stu-id="ac58e-123">In subsequent requests, copy and apply the `nextLink` or `deltaLink` URL from the previous response, as that URL already includes the encoded, desired parameters.</span></span>

| <span data-ttu-id="ac58e-124">Parámetro de consulta</span><span class="sxs-lookup"><span data-stu-id="ac58e-124">Query parameter</span></span>      | <span data-ttu-id="ac58e-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="ac58e-125">Type</span></span>   |<span data-ttu-id="ac58e-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac58e-126">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="ac58e-127">$deltatoken</span><span class="sxs-lookup"><span data-stu-id="ac58e-127">$deltatoken</span></span> | <span data-ttu-id="ac58e-128">cadena</span><span class="sxs-lookup"><span data-stu-id="ac58e-128">string</span></span> | <span data-ttu-id="ac58e-p104">Un [token de estado](../../../concepts/delta_query_overview.md) que se devuelve en la URL de `deltaLink` de la llamada de función **delta** anterior para la misma colección de grupos. Indica el progreso de la ronda de seguimiento de cambios. Guarde y aplique toda la dirección URL `deltaLink`, incluido este token, en la primera solicitud de la siguiente ronda de seguimiento de cambios de la colección.</span><span class="sxs-lookup"><span data-stu-id="ac58e-p104">A [state token](../../../concepts/delta_query_overview.md) returned in the `deltaLink` URL of the previous **delta** function call for the same group collection, indicating the completion of that round of change tracking. Save and apply the entire `deltaLink` URL including this token in the first request of the next round of change tracking for that collection.</span></span>|
| <span data-ttu-id="ac58e-131">$skiptoken</span><span class="sxs-lookup"><span data-stu-id="ac58e-131">$skiptoken</span></span> | <span data-ttu-id="ac58e-132">cadena</span><span class="sxs-lookup"><span data-stu-id="ac58e-132">string</span></span> | <span data-ttu-id="ac58e-133">Un [token de estado](../../../concepts/delta_query_overview.md) que se devuelve en la URL de `nextLink` de la llamada de función **delta**. Indica que debe realizarse el seguimiento de más cambios en la misma colección de grupos.</span><span class="sxs-lookup"><span data-stu-id="ac58e-133">A [state token](../../../concepts/delta_query_overview.md) returned in the `nextLink` URL of the previous **delta** function call, indicating there are further changes to be tracked in the same group collection.</span></span> |

### <a name="odata-query-parameters"></a><span data-ttu-id="ac58e-134">Parámetros de consulta de OData</span><span class="sxs-lookup"><span data-stu-id="ac58e-134">OData query parameters</span></span>
<span data-ttu-id="ac58e-135">Este método admite los parámetros opcionales de consulta de OData a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ac58e-135">This method supports the OData Query Parameters to help customize the response.</span></span>

- <span data-ttu-id="ac58e-p105">Puede utilizar un parámetro de consulta `$select` como en cualquier solicitud GET para especificar solo las propiedades que necesita para un mejor rendimiento. Siempre se devuelve la propiedad _id_.</span><span class="sxs-lookup"><span data-stu-id="ac58e-p105">You can use a `$select` query parameter as in any GET request to specify only the properties your need for best performance. The _id_ property is always returned.</span></span>
- <span data-ttu-id="ac58e-138">Compatibilidad con consultas delta `$select`, `$top`, y `$expand` para los grupos.</span><span class="sxs-lookup"><span data-stu-id="ac58e-138">Delta query support `$select`, `$top`, and `$expand` for groups.</span></span>
- <span data-ttu-id="ac58e-139">Hay compatibilidad limitada para `$filter` y `$orderby`:</span><span class="sxs-lookup"><span data-stu-id="ac58e-139">There is limited support for `$filter` and `$orderby`:</span></span>
  * <span data-ttu-id="ac58e-140">La única expresión `$filter` admitida es para realizar un seguimiento de los cambios en un objeto específico: `$filter=id+eq+{value}`.</span><span class="sxs-lookup"><span data-stu-id="ac58e-140">The only supported `$filter` expression is for tracking changes on a specific object: `$filter=id+eq+{value}`.</span></span> <span data-ttu-id="ac58e-141">Puede filtrar varios objetos.</span><span class="sxs-lookup"><span data-stu-id="ac58e-141">You can filter multiple objects.</span></span> <span data-ttu-id="ac58e-142">Por ejemplo, `https://graph.microsoft.com/v1.0/groups/delta/?$filter= id eq '477e9fc6-5de7-4406-bb2a-7e5c83c9ffff' or id eq '004d6a07-fe70-4b92-add5-e6e37b8affff`.</span><span class="sxs-lookup"><span data-stu-id="ac58e-142">For example, `https://graph.microsoft.com/v1.0/groups/delta/?$filter= id eq '477e9fc6-5de7-4406-bb2a-7e5c83c9ffff' or id eq '004d6a07-fe70-4b92-add5-e6e37b8affff`.</span></span> <span data-ttu-id="ac58e-143">Hay un límite de 50 objetos filtrados.</span><span class="sxs-lookup"><span data-stu-id="ac58e-143">There is a limit of 50 filtered objects.</span></span>
- <span data-ttu-id="ac58e-144">No hay compatibilidad con `$search`.</span><span class="sxs-lookup"><span data-stu-id="ac58e-144">There is no support for `$search`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="ac58e-145">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ac58e-145">Request headers</span></span>
| <span data-ttu-id="ac58e-146">Nombre</span><span class="sxs-lookup"><span data-stu-id="ac58e-146">Name</span></span>       | <span data-ttu-id="ac58e-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac58e-147">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="ac58e-148">Authorization</span><span class="sxs-lookup"><span data-stu-id="ac58e-148">Authorization</span></span>  | <span data-ttu-id="ac58e-149">token&gt; de portador&gt;</span><span class="sxs-lookup"><span data-stu-id="ac58e-149">Bearer &lt;token&gt;</span></span>|
| <span data-ttu-id="ac58e-150">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ac58e-150">Content-Type</span></span>  | <span data-ttu-id="ac58e-151">application/json</span><span class="sxs-lookup"><span data-stu-id="ac58e-151">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="ac58e-152">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ac58e-152">Request body</span></span>
<span data-ttu-id="ac58e-153">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ac58e-153">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ac58e-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ac58e-154">Response</span></span>
<span data-ttu-id="ac58e-p107">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección [grupo](../resources/group.md) en el cuerpo de la respuesta. La respuesta también incluye un token de estado, que puede ser una URL de nextLink o de deltaLink.</span><span class="sxs-lookup"><span data-stu-id="ac58e-p107">If successful, this method returns `200 OK` response code and [group](../resources/group.md) collection object in the response body. The response also includes a state token which is either a nextLink URL or a deltaLink URL.</span></span>

- <span data-ttu-id="ac58e-p108">Si se devuelve una dirección URL nextLink, hay más páginas de datos para recuperar en la sesión. La aplicación continúa realizando solicitudes mediante la dirección URL nextLink hasta que se incluya una dirección URL deltaLink en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ac58e-p108">If a nextLink URL is returned, there are additional pages of data to be retrieved in the session. The application continues making requests using the nextLink URL until a deltaLink URL is included in the response.</span></span>

- <span data-ttu-id="ac58e-p109">Si se devuelve la dirección URL deltaLink, no hay que devolver más datos sobre el estado existente del recurso. En solicitudes futuras, la aplicación usa la dirección URL deltaLink para obtener información sobre los cambios en el recurso.</span><span class="sxs-lookup"><span data-stu-id="ac58e-p109">If a deltaLink URL is returned, there is no more data about the existing state of the resource to be returned. For future requests, the application uses the deltaLink URL to learn about changes to the resource.</span></span>

<span data-ttu-id="ac58e-161">Vea:</span><span class="sxs-lookup"><span data-stu-id="ac58e-161">See:</span></span></br>
- <span data-ttu-id="ac58e-162">[Usar la consulta delta](../../../concepts/delta_query_overview.md) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="ac58e-162">[Using Delta Query](../../../concepts/delta_query_overview.md) for more details</span></span></br>
- <span data-ttu-id="ac58e-163">[Obtener cambios incrementales de grupos](../../../concepts/delta_query_groups.md) para obtener una explicación más detallada.</span><span class="sxs-lookup"><span data-stu-id="ac58e-163">[Get incremental changes for groups](../../../concepts/delta_query_groups.md) for a more detailed walkthrough.</span></span></br>

## <a name="example"></a><span data-ttu-id="ac58e-164">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ac58e-164">Example</span></span>
#### <a name="request"></a><span data-ttu-id="ac58e-165">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ac58e-165">Request</span></span>
<span data-ttu-id="ac58e-166">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ac58e-166">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "group_delta"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/delta
```

#### <a name="response"></a><span data-ttu-id="ac58e-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ac58e-167">Response</span></span>
<span data-ttu-id="ac58e-168">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ac58e-168">The following is an example of the response.</span></span>
><span data-ttu-id="ac58e-p110">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ac58e-p110">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
>
> <span data-ttu-id="ac58e-171">Tenga en cuenta la presencia de la propiedad *members@delta*, que incluye los identificadores de objetos miembros en el grupo.</span><span class="sxs-lookup"><span data-stu-id="ac58e-171">Note the presence of the *members@delta* property which includes the ids of member objects in the group.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="ac58e-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac58e-172">See also</span></span>
- <span data-ttu-id="ac58e-173">[Usar la consulta delta](../../../concepts/delta_query_overview.md) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="ac58e-173">[Using Delta Query](../../../concepts/delta_query_overview.md) for more details</span></span>
- <span data-ttu-id="ac58e-174">[Obtener cambios incrementales de grupos](../../../concepts/delta_query_groups.md) para obtener una explicación más detallada.</span><span class="sxs-lookup"><span data-stu-id="ac58e-174">[Get incremental changes for groups](../../../concepts/delta_query_groups.md) for a more detailed walkthrough.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
