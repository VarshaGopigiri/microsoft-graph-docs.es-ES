# <a name="directoryrole-delta"></a><span data-ttu-id="71abe-101">directoryRole: delta</span><span class="sxs-lookup"><span data-stu-id="71abe-101">directoryRole: delta</span></span>

<span data-ttu-id="71abe-102">Get recién creado, actualiza o elimina roles de Active directory sin tener que realizar un acceso completo de lectura de la colección completa de recursos.</span><span class="sxs-lookup"><span data-stu-id="71abe-102">Get newly created, updated, or deleted directory roles without having to perform a full read of the entire resource collection.</span></span> <span data-ttu-id="71abe-103">Para obtener más información, vea [Uso de consulta de Delta](../../../concepts/delta_query_overview.md) .</span><span class="sxs-lookup"><span data-stu-id="71abe-103">See [Using Delta Query](../../../concepts/delta_query_overview.md) for details.</span></span>

## <a name="permissions"></a><span data-ttu-id="71abe-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="71abe-104">Permissions</span></span>

<span data-ttu-id="71abe-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="71abe-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="71abe-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="71abe-107">Permission type</span></span>      | <span data-ttu-id="71abe-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="71abe-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="71abe-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="71abe-109">Delegated (work or school account)</span></span> | <span data-ttu-id="71abe-110">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="71abe-110">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="71abe-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="71abe-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="71abe-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="71abe-112">Not supported.</span></span>    |
|<span data-ttu-id="71abe-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="71abe-113">Application</span></span> | <span data-ttu-id="71abe-114">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="71abe-114">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="71abe-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="71abe-115">HTTP request</span></span>

<span data-ttu-id="71abe-116">Para comenzar el seguimiento de los cambios, realizar una solicitud que incluya la función **delta** en el recurso [directoryRole](../resources/directoryrole.md) .</span><span class="sxs-lookup"><span data-stu-id="71abe-116">To begin tracking changes, you make a request including the **delta** function on the [directoryRole](../resources/directoryrole.md) resource.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /directoryRoles/delta
```

## <a name="query-parameters"></a><span data-ttu-id="71abe-117">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="71abe-117">Query parameters</span></span>

<span data-ttu-id="71abe-118">Seguimiento de los cambios incurre una ronda de una o más llamadas de función de **delta** .</span><span class="sxs-lookup"><span data-stu-id="71abe-118">Tracking changes incurs a round of one or more **delta** function calls.</span></span> <span data-ttu-id="71abe-119">Si usa cualquier parámetro de consulta (distinto de `$deltatoken` y `$skiptoken`), debe especificar en la solicitud inicial del **delta** .</span><span class="sxs-lookup"><span data-stu-id="71abe-119">If you use any query parameter (other than `$deltatoken` and `$skiptoken`), you must specify it in the initial **delta** request.</span></span> <span data-ttu-id="71abe-120">Microsoft Graph codifica automáticamente los parámetros especificados en la parte de símbolo (token) de la `nextLink` o `deltaLink` dirección URL proporcionada en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71abe-120">Microsoft Graph automatically encodes any specified parameters into the token portion of the `nextLink` or `deltaLink` URL provided in the response.</span></span> <span data-ttu-id="71abe-121">Solo debe especificar una vez por adelantado los parámetros de consulta deseados.</span><span class="sxs-lookup"><span data-stu-id="71abe-121">You only need to specify any desired query parameters once upfront.</span></span> <span data-ttu-id="71abe-122">En solicitudes posteriores, copie y aplique la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.</span><span class="sxs-lookup"><span data-stu-id="71abe-122">In subsequent requests, copy and apply the `nextLink` or `deltaLink` URL from the previous response, as that URL already includes the encoded, desired parameters.</span></span>

| <span data-ttu-id="71abe-123">Parámetro de consulta</span><span class="sxs-lookup"><span data-stu-id="71abe-123">Query parameter</span></span>      | <span data-ttu-id="71abe-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="71abe-124">Type</span></span>   |<span data-ttu-id="71abe-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="71abe-125">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="71abe-126">$deltatoken</span><span class="sxs-lookup"><span data-stu-id="71abe-126">$deltatoken</span></span> | <span data-ttu-id="71abe-127">string</span><span class="sxs-lookup"><span data-stu-id="71abe-127">string</span></span> | <span data-ttu-id="71abe-128">Un [símbolo (token) de estado](../../../concepts/delta_query_overview.md) devuelto en el `deltaLink` dirección URL de la llamada de función **delta** anterior para la misma colección de recursos, que indica la finalización de ese round de seguimiento de cambios.</span><span class="sxs-lookup"><span data-stu-id="71abe-128">A [state token](../../../concepts/delta_query_overview.md) returned in the `deltaLink` URL of the previous **delta** function call for the same resource collection, indicating the completion of that round of change tracking.</span></span> <span data-ttu-id="71abe-129">Guardar y aplicar todo el `deltaLink` dirección URL incluido este token en la primera solicitud de la siguiente ronda de seguimiento de cambios para esa colección.</span><span class="sxs-lookup"><span data-stu-id="71abe-129">Save and apply the entire `deltaLink` URL including this token in the first request of the next round of change tracking for that collection.</span></span>|
| <span data-ttu-id="71abe-130">$skiptoken</span><span class="sxs-lookup"><span data-stu-id="71abe-130">$skiptoken</span></span> | <span data-ttu-id="71abe-131">string</span><span class="sxs-lookup"><span data-stu-id="71abe-131">string</span></span> | <span data-ttu-id="71abe-132">Un [símbolo (token) de estado](../../../concepts/delta_query_overview.md) devuelto en el `nextLink` dirección URL de la llamada de función **delta** anterior, que indica que hay más cambios para realizar un seguimiento en la misma colección de recursos.</span><span class="sxs-lookup"><span data-stu-id="71abe-132">A [state token](../../../concepts/delta_query_overview.md) returned in the `nextLink` URL of the previous **delta** function call, indicating there are further changes to be tracked in the same resource collection.</span></span> |

### <a name="odata-query-parameters"></a><span data-ttu-id="71abe-133">Parámetros de consulta de OData</span><span class="sxs-lookup"><span data-stu-id="71abe-133">OData query parameters</span></span>

<span data-ttu-id="71abe-134">Este método es compatible con los parámetros de consulta de OData para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71abe-134">This method supports OData query parameters to help customize the response.</span></span>

- <span data-ttu-id="71abe-p105">Puede utilizar un parámetro de consulta `$select` como en cualquier solicitud GET para especificar solo las propiedades que necesita para un mejor rendimiento. Siempre se devuelve la propiedad _id_.</span><span class="sxs-lookup"><span data-stu-id="71abe-p105">You can use a `$select` query parameter as in any GET request to specify only the properties your need for best performance. The _id_ property is always returned.</span></span>

- <span data-ttu-id="71abe-137">No hay compatibilidad limitada para `$filter`:</span><span class="sxs-lookup"><span data-stu-id="71abe-137">There is limited support for `$filter`:</span></span>

  - <span data-ttu-id="71abe-138">El único admitido `$filter` expresión es para realizar un seguimiento de cambios para recursos específicos, por su identificador: `$filter=id+eq+{value}` o `$filter=id+eq+{value1}+or+id+eq+{value2}`.</span><span class="sxs-lookup"><span data-stu-id="71abe-138">The only supported `$filter` expression is for tracking changes for specific resources, by their id:  `$filter=id+eq+{value}` or `$filter=id+eq+{value1}+or+id+eq+{value2}`.</span></span> <span data-ttu-id="71abe-139">El número de identificadores que puede especificar está limitado por la longitud máxima de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="71abe-139">The number of ids you can specify is limited by the maximum URL length.</span></span>

## <a name="request-headers"></a><span data-ttu-id="71abe-140">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="71abe-140">Request headers</span></span>

| <span data-ttu-id="71abe-141">Nombre</span><span class="sxs-lookup"><span data-stu-id="71abe-141">Name</span></span>       | <span data-ttu-id="71abe-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="71abe-142">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="71abe-143">Authorization</span><span class="sxs-lookup"><span data-stu-id="71abe-143">Authorization</span></span>  | <span data-ttu-id="71abe-144">&lt;token&gt; de portador</span><span class="sxs-lookup"><span data-stu-id="71abe-144">Bearer &lt;token&gt;</span></span>|
| <span data-ttu-id="71abe-145">Content-Type</span><span class="sxs-lookup"><span data-stu-id="71abe-145">Content-Type</span></span>  | <span data-ttu-id="71abe-146">application/json</span><span class="sxs-lookup"><span data-stu-id="71abe-146">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="71abe-147">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="71abe-147">Request body</span></span>

<span data-ttu-id="71abe-148">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="71abe-148">Do not supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="71abe-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71abe-149">Response</span></span>

<span data-ttu-id="71abe-150">Si tiene éxito, este método devuelve `200 OK` objeto de colección de respuesta código y [directoryRole](../resources/directoryrole.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71abe-150">If successful, this method returns `200 OK` response code and [directoryRole](../resources/directoryrole.md) collection object in the response body.</span></span> <span data-ttu-id="71abe-151">La respuesta incluye también un `nextLink` dirección URL o un `deltaLink` dirección URL.</span><span class="sxs-lookup"><span data-stu-id="71abe-151">The response also includes a `nextLink` URL or a `deltaLink` URL.</span></span>

- <span data-ttu-id="71abe-152">Si un `nextLink` se devuelve la dirección URL, hay páginas adicionales de datos que se recuperarán en la sesión.</span><span class="sxs-lookup"><span data-stu-id="71abe-152">If a `nextLink` URL is returned, there are additional pages of data to be retrieved in the session.</span></span> <span data-ttu-id="71abe-153">La aplicación continúa realizar solicitudes mediante el `nextLink` dirección URL hasta un `deltaLink` dirección URL se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71abe-153">The application continues making requests using the `nextLink` URL until a `deltaLink` URL is included in the response.</span></span>

- <span data-ttu-id="71abe-154">Si un `deltaLink` se devuelve la dirección URL, no hay ningún dato más sobre el estado existente del recurso que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="71abe-154">If a `deltaLink` URL is returned, there is no more data about the existing state of the resource to be returned.</span></span> <span data-ttu-id="71abe-155">Guardar `deltaLink` dirección URL y aplicar en la siguiente llamada **delta** para obtener más información acerca de los cambios realizados en el recurso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="71abe-155">Save `deltaLink` URL and apply it in the next **delta** call to learn about changes to the resource in the future.</span></span>

### <a name="example"></a><span data-ttu-id="71abe-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="71abe-156">Example</span></span>

##### <a name="request"></a><span data-ttu-id="71abe-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="71abe-157">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "directoryRole_delta"
}-->

```http
GET https://graph.microsoft.com/v1.0/directoryRoles/delta
```

##### <a name="response"></a><span data-ttu-id="71abe-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71abe-158">Response</span></span>

<span data-ttu-id="71abe-p110">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="71abe-p110">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- { 
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryRole",
  "isCollection": true 
} --> 
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#directoryRoles",
  "@odata.nextLink":"https://graph.microsoft.com/v1.0/directoryRoles/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjsXoYQp_dpA3cNJWc",
  "value": [
      {
      "description": "description-value",
      "displayName": "displayName-value",
      "roleTemplateId": "roleTemplateId-value",
      "id": "id-value"
    }
  ]
}
```

### <a name="see-also"></a><span data-ttu-id="71abe-161">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="71abe-161">See also</span></span>

- <span data-ttu-id="71abe-162">[Consulta de delta de uso para realizar un seguimiento de los cambios en datos de Microsoft Graph](../../../concepts/delta_query_overview.md) para obtener más detalles</span><span class="sxs-lookup"><span data-stu-id="71abe-162">[Use delta query to track changes in Microsoft Graph data](../../../concepts/delta_query_overview.md) for more details</span></span>
- <span data-ttu-id="71abe-163">[Obtener los cambios incrementales de usuarios](../../../concepts/delta_query_users.md) para obtener un ejemplo de solicitud.</span><span class="sxs-lookup"><span data-stu-id="71abe-163">[Get incremental changes for users](../../../concepts/delta_query_users.md) for an example requests.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryRole: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->