# <a name="get-incremental-changes-for-groups"></a><span data-ttu-id="3e2cb-101">Obtener los cambios incrementales de grupos</span><span class="sxs-lookup"><span data-stu-id="3e2cb-101">Get incremental changes for groups</span></span>

<span data-ttu-id="3e2cb-p101">[Consulta de delta](./delta_query_overview.md) permite consultar las adiciones, eliminaciones o actualizaciones a grupos, por medio de una serie de llamadas a función [delta](../api-reference/v1.0/api/group_delta.md). La consulta de delta le permite descubrir cambios en grupos sin tener que acceder a todo el conjunto de grupos de Microsoft Graph para comparar los cambios.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-p101">[Delta query](./delta_query_overview.md) lets you query for additions, deletions, or updates to groups, by way of a series of [delta](../api-reference/v1.0/api/group_delta.md) function calls. Delta query enables you discover changes to groups without having to fetch the entire set of groups from Microsoft Graph and compare changes.</span></span>

<span data-ttu-id="3e2cb-p102">Los clientes que utilizan grupos de sincronización con un almacén de perfil local pueden utilizar la consulta delta para su sincronización completa inicial y sus sincronizaciones incrementales futuras. Normalmente, el cliente debería realizar una sincronización completa inicial de todos los grupos de inquilino y, después, obtener los cambios incrementales en los grupos de forma periódica.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-p102">Clients using synchronizing groups with a local profile store can use Delta Query for both their initial full synchronization along with incremental synchronizations in the future. Typically, a client would do an initial full synchronization of all the groups in a tenant, and subsequently, get incremental changes to groups periodically.</span></span>

## <a name="tracking-group-changes"></a><span data-ttu-id="3e2cb-106">Seguimiento de los cambios de grupos</span><span class="sxs-lookup"><span data-stu-id="3e2cb-106">Tracking group changes</span></span>

<span data-ttu-id="3e2cb-p103">El seguimiento de los cambios de grupos normalmente es una ronda de una o varias solicitudes GET con la función **delta**. Realiza una solicitud GET de una forma muy similar a cómo [lista grupos](../api-reference/v1.0/api/group_list.md), excepto que incluye lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3e2cb-p103">Tracking group changes is a round of one or more GET requests with the **delta** function. You make a GET request much like the way you [list groups](../api-reference/v1.0/api/group_list.md), except that you include the following:</span></span>

- <span data-ttu-id="3e2cb-109">La función **delta**</span><span class="sxs-lookup"><span data-stu-id="3e2cb-109">The **delta** function.</span></span>
- <span data-ttu-id="3e2cb-110">Un [token de estado](./delta_query_overview.md) (*deltaToken* o *skipToken*) de la anterior llamada a función **delta** GET.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-110">A [state token](./delta_query_overview.md) (*deltaToken* or *skipToken*) from the previous GET **delta** function call.</span></span>

## <a name="example"></a><span data-ttu-id="3e2cb-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3e2cb-111">Example</span></span>

<span data-ttu-id="3e2cb-112">El ejemplo siguiente muestra una serie de solicitudes para seguir cambios en grupos:</span><span class="sxs-lookup"><span data-stu-id="3e2cb-112">The following example shows a series  requests to track changes to groups:</span></span>

1. <span data-ttu-id="3e2cb-113">[Solicitud inicial](#initial-request) y [respuesta](#initial-response)</span><span class="sxs-lookup"><span data-stu-id="3e2cb-113">[Initial request](#initial-request) and [response](#initial-response)</span></span>
2. <span data-ttu-id="3e2cb-114">[Solicitud nextLink](#nextlink-request) y [respuesta](#nextlink-response)</span><span class="sxs-lookup"><span data-stu-id="3e2cb-114">[nextLink request](#nextlink-request) and [response](#nextlink-response)</span></span>
3. <span data-ttu-id="3e2cb-115">[Solicitud nextLink final](#final-nextlink-request) y [respuesta](#final-nextlink-response)</span><span class="sxs-lookup"><span data-stu-id="3e2cb-115">[Final nextLink request](#final-nextlink-request) and [response](#final-nextlink-response)</span></span>
4. <span data-ttu-id="3e2cb-116">[Solicitud de deltaLink](#deltalink-request) y [respuesta deltaLink](#deltalink-response)</span><span class="sxs-lookup"><span data-stu-id="3e2cb-116">[deltaLink request](#deltalink-request) and [deltaLink response](#deltalink-response)</span></span>

## <a name="initial-request"></a><span data-ttu-id="3e2cb-117">Solicitud inicial</span><span class="sxs-lookup"><span data-stu-id="3e2cb-117">Initial request</span></span>

<span data-ttu-id="3e2cb-118">Para comenzar los cambios de seguimiento en el recurso grupo, debe realizar una solicitud incluyendo la función delta en el recurso grupo.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-118">To begin tracking changes in the group resource, you make a request including the delta function on the group resource.</span></span>

<span data-ttu-id="3e2cb-119">Tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3e2cb-119">Note the following:</span></span>

- <span data-ttu-id="3e2cb-120">El parámetro de consulta `$select` opcional se incluye en la solicitud para demostrar cómo los parámetros de consulta se incluyen automáticamente en futuras solicitudes.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-120">The optional `$select` query parameter is included in the request to demonstrate how query parameters are automatically included in future requests.</span></span>
- <span data-ttu-id="3e2cb-121">El parámetro de consulta `$expand` opcional se incluye para mostrar cómo se pueden recuperar los miembros del grupo con los objetos del grupo.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-121">The optional `$expand` query parameter is included to show how group members can be retrieved together with group objects.</span></span> <span data-ttu-id="3e2cb-122">Esto permite realizar un seguimiento de los cambios de la suscripción, como cuando se agregan o se quitan de grupos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-122">This allows tracking of membership changes, such as when users are added or removed from groups.</span></span>
- <span data-ttu-id="3e2cb-p105">La solicitud inicial no incluye un token del estado. Los tokens de estado se utilizarán en solicitudes posteriores.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-p105">The initial request does not include a state token. State tokens will be used in subsequent requests.</span></span>

``` http
GET https://graph.microsoft.com/v1.0/groups/delta?$select=displayName,description&$expand=members
```

## <a name="initial-response"></a><span data-ttu-id="3e2cb-125">Respuesta inicial</span><span class="sxs-lookup"><span data-stu-id="3e2cb-125">Initial response</span></span>

<span data-ttu-id="3e2cb-126">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección [grupo](../api-reference/v1.0/resources/group.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-126">If successful, this method returns `200 OK` response code and [group](../api-reference/v1.0/resources/group.md) collection object in the response body.</span></span> <span data-ttu-id="3e2cb-127">Si todo el conjunto de grupos es demasiado grande para que quepa en una respuesta, también se incluirá un `nextLink` que contiene un token de estado.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-127">If the entire set of groups is too large to fit in one response, a `nextLink` containing a state token will also be included.</span></span>

<span data-ttu-id="3e2cb-128">En este ejemplo, se incluyó un `nextLink`; los parámetros de consulta `$select` y `$expand` originales están codificados en el token de estado.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-128">In this example, a `nextLink` was included; the original `$select` and `$expand` query parameters are encoded in the state token.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups(displayName,description)",
  "@odata.nextLink":"https://graph.microsoft.com/v1.0/groups/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjvB7XnF_yllFsCrZJ",
  "value": [
    {
      "displayName":"TestGroup1",
      "description":"Employees in test group 1",
      "id":"c2f798fd-f95d-4623-8824-63aec21fffff",
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
    },
    {
      "displayName":"TestGroup2",
      "description":"Employees in test group 2",
      "id":"ec22655c-8eb2-432a-b4ea-8b8a254bffff"
    }
  ]
}
```

><span data-ttu-id="3e2cb-129">**Nota:** la propiedad `members@delta` se incluye en el primer objeto de grupo, TestGroup1, y contiene los dos miembros actuales del grupo.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-129">**Note:** The `members@delta` property is included in the first group object - TestGroup1 - and contains the two current members of the group.</span></span> <span data-ttu-id="3e2cb-130">TestGroup2 no contiene esta propiedad porque el grupo no tiene ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-130">TestGroup2 does not contain that property because the group does not have any members.</span></span>

## <a name="nextlink-request"></a><span data-ttu-id="3e2cb-131">Solicitud de nextLink</span><span class="sxs-lookup"><span data-stu-id="3e2cb-131">nextLink request</span></span>

<span data-ttu-id="3e2cb-132">La segunda petición usa el `nextLink` de la respuesta anterior, que contiene el `skipToken`.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-132">The second request uses the `nextLink` from the previous response, which contains the `skipToken`.</span></span> <span data-ttu-id="3e2cb-133">Tenga en cuenta que los parámetros `$select` y `$expand` no están presentes explícitamente, ya que se codifican en el token.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-133">Notice the `$select` and `$expand` parameters are not explicitly present as they are encoded in the token.</span></span>

``` http
GET https://graph.microsoft.com/v1.0/groups/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjvB7XnF_yllFsCrZJ
```

## <a name="nextlink-response"></a><span data-ttu-id="3e2cb-134">Respuesta de nextLink</span><span class="sxs-lookup"><span data-stu-id="3e2cb-134">nextLink response</span></span>

<span data-ttu-id="3e2cb-135">La respuesta contiene otro `nextLink` con un nuevo valor `skipToken`, indicando que hay más grupos disponibles.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-135">The response contains another `nextLink` with a new `skipToken` value, indicating there are more groups available.</span></span> <span data-ttu-id="3e2cb-136">Siga realizando solicitudes con la dirección URL `nextLink` hasta obtener una dirección URL `deltaLink` en la respuesta final.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-136">You continue making requests using the `nextLink` URL until a `deltaLink` URL is returned in the final response.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups",
  "@odata.nextLink":"https://graph.microsoft.com/v1.0/groups/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjtQ5LOhVoS7qQG_wdVCHHlbQpga7",
  "value": [
    {
      "displayName":"TestGroup3",
      "description":"Employees in test group 3",
      "id":"2e5807ce-58f3-4a94-9b37-ffff2e085957",
      "members@delta": [
               {
                   "@odata.type": "#microsoft.graph.user",
                   "id": "632f6bb2-3ec8-4c1f-9073-0027a8c68593"
               }
      ]
    },
    {
      "displayName":"TestGroup4",
      "description":"Employees in test group 4",
      "id":"421e797f-9406-4934-b778-4908421e3505",
      "members@delta": [
               {
                   "@odata.type": "#microsoft.graph.user",
                   "id": "3c8ac7c4-d365-4df9-abfa-356a9dd7763c"
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

## <a name="final-nextlink-request"></a><span data-ttu-id="3e2cb-137">Solicitud de nextLink final</span><span class="sxs-lookup"><span data-stu-id="3e2cb-137">Final nextLink request</span></span>

<span data-ttu-id="3e2cb-138">La tercera solicitud vuelve a usar la última `nextLink`.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-138">The third request again uses the latest `nextLink`.</span></span>

``` http
GET https://graph.microsoft.com/v1.0/groups/delta?$skiptoken=ppqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjtQ5LOhVoS7qQG_wdVCHHlbQpga7
```

## <a name="final-nextlink-response"></a><span data-ttu-id="3e2cb-139">Respuesta de nextLink final</span><span class="sxs-lookup"><span data-stu-id="3e2cb-139">Final nextLink response</span></span>

<span data-ttu-id="3e2cb-140">Por último, se devuelve la dirección URL `deltaLink`, lo que significa que no hay ningún dato más para el estado de los grupos existente.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-140">Finally, the `deltaLink` URL is returned, which means there is no more data for the existing state of groups.</span></span> <span data-ttu-id="3e2cb-141">Para las solicitudes futuras, la aplicación usa los valores `deltaLink` y `deltaToken` que contiene para obtener información sobre los cambios a los grupos.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-141">For future requests, the application uses the `deltaLink` and the `deltaToken` value it contains to learn about new changes to groups.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups",
  "@odata.deltaLink":"https://graph.microsoft.com/v1.0/groups/delta?$deltatoken=sZwAFZibx-LQOdZIo1hHhmmDhHzCY0Hs6snoIHJCSIfCHdqKdWNZ2VX3kErpyna9GygROwBk-rqWWMFxJC3pw",
  "value": [
    {
      "displayName":"TestGroup5",
      "description":"Employees in test group 5",
      "id":"bed7f0d4-750e-4e7e-ffff-169002d06fc9"
    },
    {
      "displayName":"TestGroup6",
      "description":"Employees in test group 6",
      "id":"421e797f-9406-ffff-b778-4908421e3505"
    }
  ]
}
```

## <a name="deltalink-request"></a><span data-ttu-id="3e2cb-142">Solicitud de deltaLink</span><span class="sxs-lookup"><span data-stu-id="3e2cb-142">deltaLink request</span></span>

<span data-ttu-id="3e2cb-143">Con el `deltaLink` de la [última respuesta](#final-nextlink-response), podrá obtener nuevos cambios a los grupos desde la última solicitud.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-143">Using the `deltaLink` from the [last response](#final-nextlink-response), you will be able to get net new changes to groups since the last request.</span></span> <span data-ttu-id="3e2cb-144">Los cambios incluyen:</span><span class="sxs-lookup"><span data-stu-id="3e2cb-144">Changes include:</span></span>
- <span data-ttu-id="3e2cb-145">Nuevos objetos de grupo creados.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-145">Newly created group objects.</span></span>
- <span data-ttu-id="3e2cb-146">Objetos de grupo eliminados.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-146">Deleted group objects.</span></span>
- <span data-ttu-id="3e2cb-147">Agrupar objetos para los que se ha cambiado una propiedad (por ejemplo, se ha modificado **displayName**).</span><span class="sxs-lookup"><span data-stu-id="3e2cb-147">Group objects for which a property has changed (e.g. **displayName** has been modified).</span></span>
- <span data-ttu-id="3e2cb-148">Agrupar objetos a los que se han agregado o quitado objetos de miembro.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-148">Group objects for which member objects have been added or removed.</span></span>

``` http
GET https://graph.microsoft.com/v1.0/groups/delta?$deltatoken=sZwAFZibx-LQOdZIo1hHhmmDhHzCY0Hs6snoIHJCSIfCHdqKdWNZ2VX3kErpyna9GygROwBk-rqWWMFxJC3pw
```

## <a name="deltalink-response"></a><span data-ttu-id="3e2cb-149">Respuesta de deltaLink</span><span class="sxs-lookup"><span data-stu-id="3e2cb-149">deltaLink response</span></span>

<span data-ttu-id="3e2cb-150">Si no ha habido cambios, se devuelve un `deltaLink` sin resultados, la propiedad `value` está vacía.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-150">If no changes have occurred, a `deltaLink` is returned with no results - the `value` property is empty.</span></span> <span data-ttu-id="3e2cb-151">Asegúrese de que reemplaza el vínculo anterior en la aplicación con el nuevo para usar en futuras llamadas.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-151">Make sure to replace the previous link in the application with the new one for use in future calls.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups",
  "@odata.deltaLink":"https://graph.microsoft.com/v1.0/groups/delta?$deltatoken=sZwAFZibx-LQOdZIo1hHhmmDhHzCY0Hs6snoIHJCSIfCHdqKdWNZ2VX3kErpyna9GygROwBk-rqWWMFxJC3pw",
  "value": []
}
```

<span data-ttu-id="3e2cb-152">Si se han producido cambios, se incluye una colección de grupos cambiados.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-152">If changes have occurred, a collection of changed groups is included.</span></span> <span data-ttu-id="3e2cb-153">La respuesta también contiene un `nextLink`, en caso de que haya varias páginas de cambios para recuperar, o un `deltaLink`.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-153">The response also contains either a `nextLink` - in case there are multiple pages of changes to retrieve - or a `deltaLink`.</span></span> <span data-ttu-id="3e2cb-154">Debe implementar el mismo modelo de procedimientos siguiendo el `nextLinks` como antes y conservar el último `deltaLink` para llamadas futuras.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-154">You should implement the same pattern of following the `nextLinks` as before and persist the final `deltaLink` for future calls.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups",
  "@odata.deltaLink":"https://graph.microsoft.com/v1.0/groups/delta?$deltatoken=sZwAFZibx-LQOdZIo1hHhmmDhHzCY0Hs6snoIHJCSIfCHdqKdWNZ2VX3kErpyna9GygROwBk-rqWWMFxJC3pw",
  "value": [
          {
              "displayName": "TestGroup3",
              "description": "A test group for change tracking",
              "id": "2e5807ce-58f3-4a94-9b37-ffff2e085957",
              "members@delta": [
                  {
                      "@odata.type": "#microsoft.graph.user",
                      "id": "632f6bb2-3ec8-4c1f-9073-0027a8c6859",
                      "@removed": {
                          "reason": "deleted"
                      }
                  },
                  {
                      "@odata.type": "#microsoft.graph.user",
                      "id": "37de1ae3-408f-4702-8636-20824abda004"
                  }
              ]
          }
      ]
}
```
<span data-ttu-id="3e2cb-155">Algunas cosas que debe tener en cuenta sobre la respuesta del ejemplo anterior:</span><span class="sxs-lookup"><span data-stu-id="3e2cb-155">Some things to note about the example response above:</span></span>
- <span data-ttu-id="3e2cb-156">Se devuelven los objetos con el mismo conjunto de propiedades especificadas originalmente a través de los parámetros de consulta `$select` y `$expand`.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-156">The objects are returned with the same set of properties originally specified via the `$select` and `$expand` query parameters.</span></span>
- <span data-ttu-id="3e2cb-157">Se incluyen propiedades cambiadas y sin cambios.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-157">Both changed and unchanged properties are included.</span></span> <span data-ttu-id="3e2cb-158">En el ejemplo anterior, la propiedad `description` tiene un nuevo valor, mientras que la propiedad `displayName` no ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-158">In the example above, the `description` property has a new value, while the `displayName` property has not changed.</span></span>
- <span data-ttu-id="3e2cb-159">`members@delta` contiene los cambios a la suscripción.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-159">`members@delta` contains any changes to membership.</span></span>
  - <span data-ttu-id="3e2cb-160">El primer usuario en la lista se quitó del grupo, quitando la pertenencia o eliminando el propio objeto de usuario.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-160">The first user in the list has been removed from the group - either by removing the membership or by deleting the user object itself.</span></span> <span data-ttu-id="3e2cb-161">La propiedad `@removed` lo describe.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-161">The `@removed` property describes that.</span></span>
  - <span data-ttu-id="3e2cb-162">Se ha agregado al grupo el segundo usuario.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-162">The second user has been added to the group.</span></span>

## <a name="paging-through-members-in-a-large-group"></a><span data-ttu-id="3e2cb-163">Navegar por los miembros en un grupo grande</span><span class="sxs-lookup"><span data-stu-id="3e2cb-163">Paging through members in a large group</span></span>
<span data-ttu-id="3e2cb-164">La propiedad `members@delta` se incluye en los objetos de grupo de forma predeterminada, cuando no se ha especificado el parámetro de consulta `$select`, o cuando el parámetro `$expand=members` se especifica explícitamente.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-164">The `members@delta` property is included in group objects by default, when the `$select` query parameter has not been specified, or when the `$expand=members` parameter is explicitly specified.</span></span> <span data-ttu-id="3e2cb-165">Es posible que en los grupos con muchos miembros no quepan todos los miembros en una sola respuesta; en esta sección se explica el patrón que debe implementar para tratar estos casos.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-165">For groups with many members it is possible that all members cannot fit into a single response; in this section we describe the pattern you should implement to handle such cases.</span></span>

><span data-ttu-id="3e2cb-166">**Nota:** este patrón se aplica tanto a la recuperación de estado de grupo inicial como a las llamadas posteriores para obtener los cambios delta.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-166">**Note:** This pattern applies to both the initial retrieval of group state as well as to subsequent calls to get delta changes.</span></span>

<span data-ttu-id="3e2cb-167">Supongamos que ejecuta la siguiente consulta delta, ya sea para capturar el estado completo de los grupos inicial o más adelante para obtener cambios delta:</span><span class="sxs-lookup"><span data-stu-id="3e2cb-167">Let's assume you are executing the following delta query - either to capture the initial full state of groups, or later on to get delta changes:</span></span>

``` http
GET https://graph.microsoft.com/v1.0/groups/delta?$select=displayName,description&$expand=members
```

1. <span data-ttu-id="3e2cb-168">Microsoft Graph puede devolver una respuesta que contenga solo un objeto de grupo, con una gran lista de miembros de la propiedad `members@delta`:</span><span class="sxs-lookup"><span data-stu-id="3e2cb-168">Microsoft Graph may return a response that contains just one group object, with a large list of members in the `members@delta` property:</span></span>

<span data-ttu-id="3e2cb-169">**Primera Página**</span><span class="sxs-lookup"><span data-stu-id="3e2cb-169">**First page**</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups",
  "@odata.nextLink":"https://graph.microsoft.com/v1.0/groups/delta?$skiptoken=<...>",
  "value": [
    {
      "displayName":"LargeGroup",
      "description":"A group containing thousands of users",
      "id":"2e5807ce-58f3-4a94-9b37-ffff2e085957",
      "members@delta": [
          {
              "@odata.type": "#microsoft.graph.user",
              "id": "632f6bb2-3ec8-4c1f-9073-0027a8c6859",
              "@removed": {
                  "reason": "deleted"
              }
          },
          {
              "@odata.type": "#microsoft.graph.user",
              "id": "37de1ae3-408f-4702-8636-20824abda004"
          },
          <...more users here...>
      ]
    }
    <...no more groups included - this group filled out the entire response...>
  ]
}
```

2. <span data-ttu-id="3e2cb-170">Cuando siga el `nextLink`, es posible que reciba una respuesta de nuevo con el mismo objeto de grupo.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-170">When you follow the `nextLink` you may receive a response again containing the same group object.</span></span> <span data-ttu-id="3e2cb-171">Se devolverán los mismos valores de propiedad, pero la propiedad `members@delta` expandida ahora contiene una lista de usuarios diferente.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-171">The same property values will be returned but the expanded `members@delta` property now contains a different list of users.</span></span>

<span data-ttu-id="3e2cb-172">**Segunda página**</span><span class="sxs-lookup"><span data-stu-id="3e2cb-172">**Second page**</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json
{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups",
  "@odata.nextLink":"https://graph.microsoft.com/v1.0/groups/delta?$skiptoken=<...>",
  "value": [
    {
      "displayName":"LargeGroup",
      "description":"A group containing thousands of users",
      "id":"2e5807ce-58f3-4a94-9b37-ffff2e085957",
      "members@delta": [
          {
              "@odata.type": "#microsoft.graph.user",
              "id": "c08a463b-7b8a-40a4-aa31-f9bf690b9551",
              "@removed": {
                  "reason": "deleted"
              }
          },
          {
              "@odata.type": "#microsoft.graph.user",
              "id": "23423fa6-821e-44b2-aae4-d039d33884c2"
          },
          <...more users here...>
      ]
    }
    <...no more groups included - this group filled out the entire response...>
  ]
}
```

3. <span data-ttu-id="3e2cb-173">Finalmente, se devolverá la lista completa de miembros de este modo y otros grupos empezarán a mostrarse en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-173">Eventually, the entire member list will be returned in this fashion, and other groups will start showing up in the response.</span></span>

<span data-ttu-id="3e2cb-174">Le recomendamos los siguientes procedimientos para administrar correctamente este patrón:</span><span class="sxs-lookup"><span data-stu-id="3e2cb-174">We recommend the following best practices to correctly handle this pattern:</span></span>
- <span data-ttu-id="3e2cb-175">Siga siempre `nextLink` y combine de forma local cada estado de grupo: a medida que reciba respuestas relacionadas con el mismo grupo, puede usarlas para crear la lista de pertenencia completa en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-175">Always follow `nextLink` and locally merge each group's state: as you receive responses related to the same group, use them to build the full membership list in your application.</span></span>
- <span data-ttu-id="3e2cb-176">Es mejor que no suponga una secuencia específica de las respuestas.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-176">It is best not to assume a specific sequence of the responses.</span></span> <span data-ttu-id="3e2cb-177">Suponga que el mismo grupo podría mostrarse en cualquier lugar en la secuencia `nextLink` y téngalo en cuenta en la lógica de combinación.</span><span class="sxs-lookup"><span data-stu-id="3e2cb-177">Assume that the same group could show up anywhere in the `nextLink` sequence and handle that in your merge logic.</span></span>


## <a name="see-also"></a><span data-ttu-id="3e2cb-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e2cb-178">See also</span></span>
<span data-ttu-id="3e2cb-179">Información general sobre [Consulta de delta de Microsoft Graph](../concepts/delta_query_overview.md).</span><span class="sxs-lookup"><span data-stu-id="3e2cb-179">[Microsoft Graph delta query](../concepts/delta_query_overview.md) overview.</span></span>
