---
title: Obtener los cambios incrementales de grupos
description: La consulta delta permite consultar las adiciones, eliminaciones o actualizaciones a grupos, por medio de una serie de llamadas a la función delta. La consulta delta le permite descubrir cambios en grupos
ms.openlocfilehash: b043d62e0d99b4d71e25a8367abc731d39ad6d45
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092759"
---
# <a name="get-incremental-changes-for-groups"></a><span data-ttu-id="40324-104">Obtener los cambios incrementales de grupos</span><span class="sxs-lookup"><span data-stu-id="40324-104">Get incremental changes for groups</span></span>

<span data-ttu-id="40324-p102">[Consulta de delta](./delta-query-overview.md) permite consultar las adiciones, eliminaciones o actualizaciones a grupos, por medio de una serie de llamadas a función [delta](/graph/api/group-delta?view=graph-rest-1.0). La consulta de delta le permite descubrir cambios en grupos sin tener que acceder a todo el conjunto de grupos de Microsoft Graph para comparar los cambios.</span><span class="sxs-lookup"><span data-stu-id="40324-p102">[Delta query](./delta-query-overview.md) lets you query for additions, deletions, or updates to groups, by way of a series of [delta](/graph/api/group-delta?view=graph-rest-1.0) function calls. Delta query enables you discover changes to groups without having to fetch the entire set of groups from Microsoft Graph and compare changes.</span></span>

<span data-ttu-id="40324-p103">Los clientes que utilizan grupos de sincronización con un almacén de perfil local pueden utilizar la consulta delta para su sincronización completa inicial y sus sincronizaciones incrementales futuras. Normalmente, el cliente debería realizar una sincronización completa inicial de todos los grupos de inquilino y, después, obtener los cambios incrementales en los grupos de forma periódica.</span><span class="sxs-lookup"><span data-stu-id="40324-p103">Clients using synchronizing groups with a local profile store can use Delta Query for both their initial full synchronization along with incremental synchronizations in the future. Typically, a client would do an initial full synchronization of all the groups in a tenant, and subsequently, get incremental changes to groups periodically.</span></span>

## <a name="tracking-group-changes"></a><span data-ttu-id="40324-109">Seguimiento de los cambios de grupos</span><span class="sxs-lookup"><span data-stu-id="40324-109">Tracking group changes</span></span>

<span data-ttu-id="40324-p104">El seguimiento de los cambios de grupos normalmente es una ronda de una o varias solicitudes GET con la función **delta**. Realiza una solicitud GET de una forma muy similar a cómo [lista grupos](/graph/api/group-list?view=graph-rest-1.0), excepto que incluye lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="40324-p104">Tracking group changes is a round of one or more GET requests with the **delta** function. You make a GET request much like the way you [list groups](/graph/api/group-list?view=graph-rest-1.0), except that you include the following:</span></span>

- <span data-ttu-id="40324-112">La función **delta**</span><span class="sxs-lookup"><span data-stu-id="40324-112">The **delta** function.</span></span>
- <span data-ttu-id="40324-113">Un [token de estado](./delta-query-overview.md) (*deltaToken* o *skipToken*) de la anterior llamada a función **delta** GET.</span><span class="sxs-lookup"><span data-stu-id="40324-113">A [state token](./delta-query-overview.md) (*deltaToken* or *skipToken*) from the previous GET **delta** function call.</span></span>

## <a name="example"></a><span data-ttu-id="40324-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="40324-114">Example</span></span>

<span data-ttu-id="40324-115">El ejemplo siguiente muestra una serie de solicitudes para seguir cambios en grupos:</span><span class="sxs-lookup"><span data-stu-id="40324-115">The following example shows a series  requests to track changes to groups:</span></span>

1. <span data-ttu-id="40324-116">[Solicitud inicial](#initial-request) y [respuesta](#initial-response)</span><span class="sxs-lookup"><span data-stu-id="40324-116">[Initial request](#initial-request) and [response](#initial-response)</span></span>
2. <span data-ttu-id="40324-117">[Solicitud nextLink](#nextlink-request) y [respuesta](#nextlink-response)</span><span class="sxs-lookup"><span data-stu-id="40324-117">[nextLink request](#nextlink-request) and [response](#nextlink-response)</span></span>
3. <span data-ttu-id="40324-118">[Solicitud nextLink final](#final-nextlink-request) y [respuesta](#final-nextlink-response)</span><span class="sxs-lookup"><span data-stu-id="40324-118">[Final nextLink request](#final-nextlink-request) and [response](#final-nextlink-response)</span></span>
4. <span data-ttu-id="40324-119">[Solicitud de deltaLink](#deltalink-request) y [respuesta deltaLink](#deltalink-response)</span><span class="sxs-lookup"><span data-stu-id="40324-119">[deltaLink request](#deltalink-request) and [deltaLink response](#deltalink-response)</span></span>

## <a name="initial-request"></a><span data-ttu-id="40324-120">Solicitud inicial</span><span class="sxs-lookup"><span data-stu-id="40324-120">Initial request</span></span>

<span data-ttu-id="40324-121">Para comenzar los cambios de seguimiento en el recurso grupo, debe realizar una solicitud incluyendo la función delta en el recurso grupo.</span><span class="sxs-lookup"><span data-stu-id="40324-121">To begin tracking changes in the group resource, you make a request including the delta function on the group resource.</span></span>

<span data-ttu-id="40324-122">Tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="40324-122">Note the following:</span></span>

- <span data-ttu-id="40324-123">El parámetro de consulta `$select` opcional se incluye en la solicitud para demostrar cómo los parámetros de consulta se incluyen automáticamente en futuras solicitudes.</span><span class="sxs-lookup"><span data-stu-id="40324-123">The optional `$select` query parameter is included in the request to demonstrate how query parameters are automatically included in future requests.</span></span>
- <span data-ttu-id="40324-124">El parámetro de consulta `$expand` opcional se incluye para mostrar cómo se pueden recuperar los miembros del grupo con los objetos del grupo.</span><span class="sxs-lookup"><span data-stu-id="40324-124">The optional `$expand` query parameter is included to show how group members can be retrieved together with group objects.</span></span> <span data-ttu-id="40324-125">Esto permite realizar un seguimiento de los cambios de la suscripción, como cuando se agregan o se quitan de grupos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="40324-125">This allows tracking of membership changes, such as when users are added or removed from groups.</span></span>
- <span data-ttu-id="40324-p106">La solicitud inicial no incluye un token del estado. Los tokens de estado se utilizarán en solicitudes posteriores.</span><span class="sxs-lookup"><span data-stu-id="40324-p106">The initial request does not include a state token. State tokens will be used in subsequent requests.</span></span>

``` http
GET https://graph.microsoft.com/v1.0/groups/delta?$select=displayName,description&$expand=members
```

## <a name="initial-response"></a><span data-ttu-id="40324-128">Respuesta inicial</span><span class="sxs-lookup"><span data-stu-id="40324-128">Initial response</span></span>

<span data-ttu-id="40324-129">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección [grupo](/graph/api/resources/group?view=graph-rest-1.0) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="40324-129">If successful, this method returns `200 OK` response code and [group](/graph/api/resources/group?view=graph-rest-1.0) collection object in the response body.</span></span> <span data-ttu-id="40324-130">Si todo el conjunto de grupos es demasiado grande para que quepa en una respuesta, también se incluirá un `nextLink` que contiene un token de estado.</span><span class="sxs-lookup"><span data-stu-id="40324-130">If the entire set of groups is too large to fit in one response, a `nextLink` containing a state token will also be included.</span></span>

<span data-ttu-id="40324-131">En este ejemplo, se incluyó un `nextLink`; los parámetros de consulta `$select` y `$expand` originales están codificados en el token de estado.</span><span class="sxs-lookup"><span data-stu-id="40324-131">In this example, a `nextLink` was included; the original `$select` and `$expand` query parameters are encoded in the state token.</span></span>

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

><span data-ttu-id="40324-132">**Nota:** La propiedad `members@delta` se incluye en el primer objeto de grupo, TestGroup1, y contiene los dos miembros actuales del grupo.</span><span class="sxs-lookup"><span data-stu-id="40324-132">**Note:** The   property is included in the first group object - TestGroup1 - and contains the two current members of the group.</span></span> <span data-ttu-id="40324-133">TestGroup2 no contiene esta propiedad porque el grupo no tiene ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="40324-133">TestGroup2 does not contain that property because the group does not have any members.</span></span>

## <a name="nextlink-request"></a><span data-ttu-id="40324-134">Solicitud de nextLink</span><span class="sxs-lookup"><span data-stu-id="40324-134">nextLink request</span></span>

<span data-ttu-id="40324-135">La segunda petición usa el `nextLink` de la respuesta anterior, que contiene el `skipToken`.</span><span class="sxs-lookup"><span data-stu-id="40324-135">The second request uses the `nextLink` from the previous response, which contains the `skipToken`.</span></span> <span data-ttu-id="40324-136">Tenga en cuenta que los parámetros `$select` y `$expand` no están presentes explícitamente, ya que se codifican en el token.</span><span class="sxs-lookup"><span data-stu-id="40324-136">Notice the `$select` and `$expand` parameters are not explicitly present as they are encoded in the token.</span></span>

``` http
GET https://graph.microsoft.com/v1.0/groups/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjvB7XnF_yllFsCrZJ
```

## <a name="nextlink-response"></a><span data-ttu-id="40324-137">Respuesta de nextLink</span><span class="sxs-lookup"><span data-stu-id="40324-137">nextLink response</span></span>

<span data-ttu-id="40324-138">La respuesta contiene otro `nextLink` con un nuevo valor `skipToken`, indicando que hay más grupos disponibles.</span><span class="sxs-lookup"><span data-stu-id="40324-138">The response contains another `nextLink` with a new `skipToken` value, indicating there are more groups available.</span></span> <span data-ttu-id="40324-139">Siga realizando solicitudes con la dirección URL `nextLink` hasta obtener una dirección URL `deltaLink` en la respuesta final.</span><span class="sxs-lookup"><span data-stu-id="40324-139">You continue making requests using the `nextLink` URL until a `deltaLink` URL is returned in the final response.</span></span>

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

## <a name="final-nextlink-request"></a><span data-ttu-id="40324-140">Solicitud de nextLink final</span><span class="sxs-lookup"><span data-stu-id="40324-140">Final nextLink request</span></span>

<span data-ttu-id="40324-141">La tercera solicitud vuelve a usar la última `nextLink`.</span><span class="sxs-lookup"><span data-stu-id="40324-141">The third request again uses the latest `nextLink`.</span></span>

``` http
GET https://graph.microsoft.com/v1.0/groups/delta?$skiptoken=ppqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjtQ5LOhVoS7qQG_wdVCHHlbQpga7
```

## <a name="final-nextlink-response"></a><span data-ttu-id="40324-142">Respuesta de nextLink final</span><span class="sxs-lookup"><span data-stu-id="40324-142">Final nextLink response</span></span>

<span data-ttu-id="40324-143">Por último, se devuelve la dirección URL `deltaLink`, lo que significa que no hay ningún dato más para el estado de los grupos existente.</span><span class="sxs-lookup"><span data-stu-id="40324-143">Finally, the `deltaLink` URL is returned, which means there is no more data for the existing state of groups.</span></span> <span data-ttu-id="40324-144">Para las solicitudes futuras, la aplicación usa los valores `deltaLink` y `deltaToken` que contiene para obtener información sobre los cambios a los grupos.</span><span class="sxs-lookup"><span data-stu-id="40324-144">For future requests, the application uses the `deltaLink` and the `deltaToken` value it contains to learn about new changes to groups.</span></span>

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

## <a name="deltalink-request"></a><span data-ttu-id="40324-145">Solicitud de deltaLink</span><span class="sxs-lookup"><span data-stu-id="40324-145">deltaLink request</span></span>

<span data-ttu-id="40324-146">Con el `deltaLink` de la [última respuesta](#final-nextlink-response), podrá obtener nuevos cambios a los grupos desde la última solicitud.</span><span class="sxs-lookup"><span data-stu-id="40324-146">Using the `deltaLink` from the [last response](#final-nextlink-response), you will be able to get net new changes to groups since the last request.</span></span> <span data-ttu-id="40324-147">Los cambios incluyen:</span><span class="sxs-lookup"><span data-stu-id="40324-147">Changes include:</span></span>
- <span data-ttu-id="40324-148">Nuevos objetos de grupo creados.</span><span class="sxs-lookup"><span data-stu-id="40324-148">Newly created group objects.</span></span>
- <span data-ttu-id="40324-149">Objetos de grupo eliminados.</span><span class="sxs-lookup"><span data-stu-id="40324-149">Deleted group objects.</span></span>
- <span data-ttu-id="40324-150">Agrupar objetos para los que se ha cambiado una propiedad (por ejemplo, se ha modificado **displayName**).</span><span class="sxs-lookup"><span data-stu-id="40324-150">Group objects for which a property has changed (e.g. **displayName** has been modified).</span></span>
- <span data-ttu-id="40324-151">Agrupar objetos a los que se han agregado o quitado objetos de miembro.</span><span class="sxs-lookup"><span data-stu-id="40324-151">Group objects for which member objects have been added or removed.</span></span>

``` http
GET https://graph.microsoft.com/v1.0/groups/delta?$deltatoken=sZwAFZibx-LQOdZIo1hHhmmDhHzCY0Hs6snoIHJCSIfCHdqKdWNZ2VX3kErpyna9GygROwBk-rqWWMFxJC3pw
```

## <a name="deltalink-response"></a><span data-ttu-id="40324-152">Respuesta de deltaLink</span><span class="sxs-lookup"><span data-stu-id="40324-152">deltaLink response</span></span>

<span data-ttu-id="40324-153">Si no ha habido cambios, se devuelve un `deltaLink` sin resultados, la propiedad `value` está vacía.</span><span class="sxs-lookup"><span data-stu-id="40324-153">If no changes have occurred, a `deltaLink` is returned with no results - the `value` property is empty.</span></span> <span data-ttu-id="40324-154">Asegúrese de que reemplaza el vínculo anterior en la aplicación con el nuevo para usar en futuras llamadas.</span><span class="sxs-lookup"><span data-stu-id="40324-154">Make sure to replace the previous link in the application with the new one for use in future calls.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups",
  "@odata.deltaLink":"https://graph.microsoft.com/v1.0/groups/delta?$deltatoken=sZwAFZibx-LQOdZIo1hHhmmDhHzCY0Hs6snoIHJCSIfCHdqKdWNZ2VX3kErpyna9GygROwBk-rqWWMFxJC3pw",
  "value": []
}
```

<span data-ttu-id="40324-155">Si se han producido cambios, se incluye una colección de grupos cambiados.</span><span class="sxs-lookup"><span data-stu-id="40324-155">If changes have occurred, a collection of changed groups is included.</span></span> <span data-ttu-id="40324-156">La respuesta también contiene un `nextLink`, en caso de que haya varias páginas de cambios para recuperar, o un `deltaLink`.</span><span class="sxs-lookup"><span data-stu-id="40324-156">The response also contains either a `nextLink` - in case there are multiple pages of changes to retrieve - or a `deltaLink`.</span></span> <span data-ttu-id="40324-157">Debe implementar el mismo modelo de procedimientos siguiendo el `nextLinks` como antes y conservar el último `deltaLink` para llamadas futuras.</span><span class="sxs-lookup"><span data-stu-id="40324-157">You should implement the same pattern of following the `nextLinks` as before and persist the final `deltaLink` for future calls.</span></span>

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

<span data-ttu-id="40324-158">Algunas cosas que debe tener en cuenta sobre la respuesta del ejemplo anterior:</span><span class="sxs-lookup"><span data-stu-id="40324-158">Some things to note about the example response above:</span></span>

- <span data-ttu-id="40324-159">Se devuelven los objetos con el mismo conjunto de propiedades especificadas originalmente a través de los parámetros de consulta `$select` y `$expand`.</span><span class="sxs-lookup"><span data-stu-id="40324-159">The objects are returned with the same set of properties originally specified via the `$select` and `$expand` query parameters.</span></span>

- <span data-ttu-id="40324-160">Se incluyen propiedades cambiadas y sin cambios.</span><span class="sxs-lookup"><span data-stu-id="40324-160">Both changed and unchanged properties are included.</span></span> <span data-ttu-id="40324-161">En el ejemplo anterior, la propiedad `description` tiene un nuevo valor, mientras que la propiedad `displayName` no ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="40324-161">In the example above, the `description` property has a new value, while the `displayName` property has not changed.</span></span>

- <span data-ttu-id="40324-162">`members@delta` contiene los cambios a la suscripción.</span><span class="sxs-lookup"><span data-stu-id="40324-162">`members@delta` contains any changes to membership.</span></span>

  - <span data-ttu-id="40324-163">El primer usuario en la lista se quitó del grupo, quitando la pertenencia o eliminando el propio objeto de usuario.</span><span class="sxs-lookup"><span data-stu-id="40324-163">The first user in the list has been removed from the group - either by removing the membership or by deleting the user object itself.</span></span> <span data-ttu-id="40324-164">La propiedad `@removed` lo describe.</span><span class="sxs-lookup"><span data-stu-id="40324-164">The `@removed` property describes that.</span></span>

  - <span data-ttu-id="40324-165">Se ha agregado al grupo el segundo usuario.</span><span class="sxs-lookup"><span data-stu-id="40324-165">The second user has been added to the group.</span></span>

## <a name="paging-through-members-in-a-large-group"></a><span data-ttu-id="40324-166">Navegar por los miembros en un grupo grande</span><span class="sxs-lookup"><span data-stu-id="40324-166">Paging through members in a large group</span></span>

<span data-ttu-id="40324-167">La propiedad `members@delta` se incluye en los objetos de grupo de forma predeterminada, cuando no se ha especificado el parámetro de consulta `$select`, o cuando el parámetro `$expand=members` se especifica explícitamente.</span><span class="sxs-lookup"><span data-stu-id="40324-167">The `members@delta` property is included in group objects by default, when the `$select` query parameter has not been specified, or when the `$expand=members` parameter is explicitly specified.</span></span> <span data-ttu-id="40324-168">Es posible que en los grupos con muchos miembros no quepan todos los miembros en una sola respuesta; en esta sección se explica el patrón que debe implementar para tratar estos casos.</span><span class="sxs-lookup"><span data-stu-id="40324-168">For groups with many members it is possible that all members cannot fit into a single response; in this section we describe the pattern you should implement to handle such cases.</span></span>

><span data-ttu-id="40324-169">**Nota:** este patrón se aplica tanto a la recuperación de estado de grupo inicial como a las llamadas posteriores para obtener los cambios delta.</span><span class="sxs-lookup"><span data-stu-id="40324-169">**Note:** This pattern applies to both the initial retrieval of group state as well as to subsequent calls to get delta changes.</span></span>

<span data-ttu-id="40324-170">Supongamos que ejecuta la siguiente consulta delta, ya sea para capturar el estado completo de los grupos inicial o más adelante para obtener cambios delta:</span><span class="sxs-lookup"><span data-stu-id="40324-170">Let's assume you are executing the following delta query - either to capture the initial full state of groups, or later on to get delta changes:</span></span>

``` http
GET https://graph.microsoft.com/v1.0/groups/delta?$select=displayName,description&$expand=members
```

1. <span data-ttu-id="40324-171">Microsoft Graph puede devolver una respuesta que contenga solo un objeto de grupo, con una gran lista de miembros de la propiedad `members@delta`:</span><span class="sxs-lookup"><span data-stu-id="40324-171">Microsoft Graph may return a response that contains just one group object, with a large list of members in the `members@delta` property:</span></span>

<span data-ttu-id="40324-172">**Primera Página**</span><span class="sxs-lookup"><span data-stu-id="40324-172">**First page**</span></span>

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

2. <span data-ttu-id="40324-173">Cuando siga el `nextLink`, es posible que reciba una respuesta de nuevo con el mismo objeto de grupo.</span><span class="sxs-lookup"><span data-stu-id="40324-173">When you follow the `nextLink` you may receive a response again containing the same group object.</span></span> <span data-ttu-id="40324-174">Se devolverán los mismos valores de propiedad, pero la propiedad `members@delta` expandida ahora contiene una lista de usuarios diferente.</span><span class="sxs-lookup"><span data-stu-id="40324-174">The same property values will be returned but the expanded `members@delta` property now contains a different list of users.</span></span>

<span data-ttu-id="40324-175">**Segunda página**</span><span class="sxs-lookup"><span data-stu-id="40324-175">**Second page**</span></span>

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

3. <span data-ttu-id="40324-176">Finalmente, se devolverá la lista completa de miembros de este modo y otros grupos empezarán a mostrarse en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="40324-176">Eventually, the entire member list will be returned in this fashion, and other groups will start showing up in the response.</span></span>

<span data-ttu-id="40324-177">Le recomendamos los siguientes procedimientos para administrar correctamente este patrón:</span><span class="sxs-lookup"><span data-stu-id="40324-177">We recommend the following best practices to correctly handle this pattern:</span></span>
- <span data-ttu-id="40324-178">Siga siempre `nextLink` y combine de forma local cada estado de grupo: a medida que reciba respuestas relacionadas con el mismo grupo, puede usarlas para crear la lista de pertenencia completa en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="40324-178">Always follow `nextLink` and locally merge each group's state: as you receive responses related to the same group, use them to build the full membership list in your application.</span></span>
- <span data-ttu-id="40324-179">Es mejor que no suponga una secuencia específica de las respuestas.</span><span class="sxs-lookup"><span data-stu-id="40324-179">It is best not to assume a specific sequence of the responses.</span></span> <span data-ttu-id="40324-180">Suponga que el mismo grupo podría mostrarse en cualquier lugar en la secuencia `nextLink` y téngalo en cuenta en la lógica de combinación.</span><span class="sxs-lookup"><span data-stu-id="40324-180">Assume that the same group could show up anywhere in the `nextLink` sequence and handle that in your merge logic.</span></span>


## <a name="see-also"></a><span data-ttu-id="40324-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="40324-181">See also</span></span>
<span data-ttu-id="40324-182">Información general sobre [Consulta de delta de Microsoft Graph](delta-query-overview.md).</span><span class="sxs-lookup"><span data-stu-id="40324-182">[Microsoft Graph delta query](delta-query-overview.md) overview.</span></span>
