---
title: 'grupo: delta'
description: Get recién creado, actualiza o elimina grupos, incluidos los cambios de pertenencia de grupo, sin tener que realizar un acceso completo de lectura de la colección de todo grupo. Para obtener más información, vea Uso de consulta de Delta.
localization_priority: Normal
ms.openlocfilehash: d9032b6066184ddf993f7fa4645cae00ed1d48b9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27815144"
---
# <a name="group-delta"></a><span data-ttu-id="6fb84-104">grupo: delta</span><span class="sxs-lookup"><span data-stu-id="6fb84-104">group: delta</span></span>
<span data-ttu-id="6fb84-105">Get recién creado, actualiza o elimina grupos, incluidos los cambios de pertenencia de grupo, sin tener que realizar un acceso completo de lectura de la colección de todo grupo.</span><span class="sxs-lookup"><span data-stu-id="6fb84-105">Get newly created, updated, or deleted groups, including group membership changes, without having to perform a full read of the entire group collection.</span></span> <span data-ttu-id="6fb84-106">Para obtener más información, vea [Uso de consulta de Delta](/graph/delta-query-overview) .</span><span class="sxs-lookup"><span data-stu-id="6fb84-106">See [Using Delta Query](/graph/delta-query-overview) for details.</span></span>

## <a name="permissions"></a><span data-ttu-id="6fb84-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="6fb84-107">Permissions</span></span>

<span data-ttu-id="6fb84-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6fb84-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6fb84-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6fb84-110">Permission type</span></span>      | <span data-ttu-id="6fb84-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6fb84-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6fb84-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6fb84-112">Delegated (work or school account)</span></span> | <span data-ttu-id="6fb84-113">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6fb84-113">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="6fb84-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6fb84-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6fb84-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6fb84-115">Not supported.</span></span>    |
|<span data-ttu-id="6fb84-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6fb84-116">Application</span></span> | <span data-ttu-id="6fb84-117">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6fb84-117">Group.Read.All, Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="6fb84-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6fb84-118">HTTP request</span></span>

<span data-ttu-id="6fb84-119">Para comenzar los cambios, debe realizar una solicitud incluyendo la función delta en el recurso grupo.</span><span class="sxs-lookup"><span data-stu-id="6fb84-119">To begin tracking changes, you make a request including the delta function on the groups resource.</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /groups/delta
```

## <a name="query-parameters"></a><span data-ttu-id="6fb84-120">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="6fb84-120">Query parameters</span></span>

<span data-ttu-id="6fb84-p104">El seguimiento de cambios en grupos conlleva al menos una llamada de una función **delta**. Si usa cualquier parámetro de consulta (uno diferente a `$deltatoken` y `$skiptoken`), debe especificarlo en la solicitud **delta** inicial. Microsoft Graph codifica automáticamente cualquier parámetro especificado en la parte del token de la URL `nextLink` o `deltaLink` proporcionada en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6fb84-p104">Tracking changes in groups incurs a round of one or more **delta** function calls. If you use any query parameter (other than `$deltatoken` and `$skiptoken`), you must specify it in the initial **delta** request. Microsoft Graph automatically encodes any specified parameters into the token portion of the `nextLink` or `deltaLink` URL provided in the response.</span></span>

<span data-ttu-id="6fb84-124">Solo debe especificar una vez por adelantado los parámetros de consulta deseados.</span><span class="sxs-lookup"><span data-stu-id="6fb84-124">You only need to specify any desired query parameters once upfront.</span></span>

<span data-ttu-id="6fb84-125">En solicitudes posteriores, copie y aplique la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.</span><span class="sxs-lookup"><span data-stu-id="6fb84-125">In subsequent requests, copy and apply the `nextLink` or `deltaLink` URL from the previous response, as that URL already includes the encoded, desired parameters.</span></span>

| <span data-ttu-id="6fb84-126">Parámetro de consulta</span><span class="sxs-lookup"><span data-stu-id="6fb84-126">Query parameter</span></span> | <span data-ttu-id="6fb84-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="6fb84-127">Type</span></span>  |<span data-ttu-id="6fb84-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="6fb84-128">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="6fb84-129">$deltatoken</span><span class="sxs-lookup"><span data-stu-id="6fb84-129">$deltatoken</span></span> | <span data-ttu-id="6fb84-130">string</span><span class="sxs-lookup"><span data-stu-id="6fb84-130">string</span></span> | <span data-ttu-id="6fb84-p105">Un [token de estado](/graph/delta-query-overview) que se devuelve en la URL de `deltaLink` de la llamada de función **delta** anterior para la misma colección de grupos. Indica el progreso de la ronda de seguimiento de cambios. Guarde y aplique toda la dirección URL `deltaLink`, incluido este token, en la primera solicitud de la siguiente ronda de seguimiento de cambios de la colección.</span><span class="sxs-lookup"><span data-stu-id="6fb84-p105">A [state token](/graph/delta-query-overview) returned in the `deltaLink` URL of the previous **delta** function call for the same group collection, indicating the completion of that round of change tracking. Save and apply the entire `deltaLink` URL including this token in the first request of the next round of change tracking for that collection.</span></span>|
| <span data-ttu-id="6fb84-133">$skiptoken</span><span class="sxs-lookup"><span data-stu-id="6fb84-133">$skiptoken</span></span> | <span data-ttu-id="6fb84-134">string</span><span class="sxs-lookup"><span data-stu-id="6fb84-134">string</span></span> | <span data-ttu-id="6fb84-135">Un [token de estado](/graph/delta-query-overview) que se devuelve en la URL de `nextLink` de la llamada de función **delta**. Indica que debe realizarse el seguimiento de más cambios en la misma colección de grupos.</span><span class="sxs-lookup"><span data-stu-id="6fb84-135">A [state token](/graph/delta-query-overview) returned in the `nextLink` URL of the previous **delta** function call, indicating there are further changes to be tracked in the same group collection.</span></span> |

### <a name="odata-query-parameters"></a><span data-ttu-id="6fb84-136">Parámetros de consulta de OData</span><span class="sxs-lookup"><span data-stu-id="6fb84-136">OData query parameters</span></span>

<span data-ttu-id="6fb84-137">Este método es compatible con parámetros opcionales de consulta de OData para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6fb84-137">This method supports optional OData query parameters to help customize the response.</span></span>

- <span data-ttu-id="6fb84-p106">Puede utilizar un parámetro de consulta `$select` como en cualquier solicitud GET para especificar solo las propiedades que necesita para un mejor rendimiento. Siempre se devuelve la propiedad *id*.</span><span class="sxs-lookup"><span data-stu-id="6fb84-p106">You can use a `$select` query parameter as in any GET request to specify only the properties your need for best performance. The *id* property is always returned.</span></span>
- <span data-ttu-id="6fb84-140">Puede usar `$expand=members` para obtener los cambios de pertenencia.</span><span class="sxs-lookup"><span data-stu-id="6fb84-140">You can use `$expand=members` to get membership changes.</span></span>
- <span data-ttu-id="6fb84-141">No hay compatibilidad limitada para `$filter`:</span><span class="sxs-lookup"><span data-stu-id="6fb84-141">There is limited support for `$filter`:</span></span>
  - <span data-ttu-id="6fb84-142">La única expresión `$filter` admitida es para realizar un seguimiento de los cambios en un objeto específico: `$filter=id+eq+{value}`.</span><span class="sxs-lookup"><span data-stu-id="6fb84-142">The only supported `$filter` expression is for tracking changes on a specific object: `$filter=id+eq+{value}`.</span></span> <span data-ttu-id="6fb84-143">Puede filtrar varios objetos.</span><span class="sxs-lookup"><span data-stu-id="6fb84-143">You can filter multiple objects.</span></span> <span data-ttu-id="6fb84-144">Por ejemplo, `https://graph.microsoft.com/v1.0/groups/delta/?$filter= id eq '477e9fc6-5de7-4406-bb2a-7e5c83c9ffff' or id eq '004d6a07-fe70-4b92-add5-e6e37b8affff'`.</span><span class="sxs-lookup"><span data-stu-id="6fb84-144">For example, `https://graph.microsoft.com/v1.0/groups/delta/?$filter= id eq '477e9fc6-5de7-4406-bb2a-7e5c83c9ffff' or id eq '004d6a07-fe70-4b92-add5-e6e37b8affff'`.</span></span> <span data-ttu-id="6fb84-145">Hay un límite de 50 objetos filtrados.</span><span class="sxs-lookup"><span data-stu-id="6fb84-145">There is a limit of 50 filtered objects.</span></span>

## <a name="request-headers"></a><span data-ttu-id="6fb84-146">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6fb84-146">Request headers</span></span>

| <span data-ttu-id="6fb84-147">Nombre</span><span class="sxs-lookup"><span data-stu-id="6fb84-147">Name</span></span>       | <span data-ttu-id="6fb84-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="6fb84-148">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="6fb84-149">Authorization</span><span class="sxs-lookup"><span data-stu-id="6fb84-149">Authorization</span></span>  | <span data-ttu-id="6fb84-150">&lt;token&gt; de portador</span><span class="sxs-lookup"><span data-stu-id="6fb84-150">Bearer &lt;token&gt;</span></span>|
| <span data-ttu-id="6fb84-151">Content-Type</span><span class="sxs-lookup"><span data-stu-id="6fb84-151">Content-Type</span></span>  | <span data-ttu-id="6fb84-152">application/json</span><span class="sxs-lookup"><span data-stu-id="6fb84-152">application/json</span></span> |
| <span data-ttu-id="6fb84-153">Prefer</span><span class="sxs-lookup"><span data-stu-id="6fb84-153">Prefer</span></span> | <span data-ttu-id="6fb84-154">devolver = mínimo</span><span class="sxs-lookup"><span data-stu-id="6fb84-154">return=minimal</span></span> <br><br><span data-ttu-id="6fb84-155">Si se especifica este encabezado con una solicitud que utiliza un `deltaLink` devolvería sólo las propiedades del objeto que han cambiado desde la última round.</span><span class="sxs-lookup"><span data-stu-id="6fb84-155">Specifying this header with a request that uses a `deltaLink` would return only the object properties that have changed since the last round.</span></span> <span data-ttu-id="6fb84-156">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6fb84-156">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6fb84-157">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6fb84-157">Request body</span></span>

<span data-ttu-id="6fb84-158">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6fb84-158">Do not supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="6fb84-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6fb84-159">Response</span></span>

<span data-ttu-id="6fb84-160">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección [grupo](../resources/group.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6fb84-160">If successful, this method returns `200 OK` response code and [group](../resources/group.md) collection object in the response body.</span></span> <span data-ttu-id="6fb84-161">La respuesta incluye también un símbolo (token) de estado que puede ser un `nextLink` dirección URL o un `deltaLink` dirección URL.</span><span class="sxs-lookup"><span data-stu-id="6fb84-161">The response also includes a state token which is either a `nextLink` URL or a `deltaLink` URL.</span></span>

- <span data-ttu-id="6fb84-162">Si un `nextLink` se devuelve la dirección URL:</span><span class="sxs-lookup"><span data-stu-id="6fb84-162">If a `nextLink` URL is returned:</span></span>
  - <span data-ttu-id="6fb84-163">Esto indica que hay páginas adicionales de datos que se recuperarán en la sesión.</span><span class="sxs-lookup"><span data-stu-id="6fb84-163">This indicates there are additional pages of data to be retrieved in the session.</span></span> <span data-ttu-id="6fb84-164">La aplicación continúa realizar solicitudes mediante el `nextLink` dirección URL hasta un `deltaLink` dirección URL se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6fb84-164">The application continues making requests using the `nextLink` URL until a `deltaLink` URL is included in the response.</span></span>
  - <span data-ttu-id="6fb84-165">La respuesta incluye el mismo conjunto de propiedades como se muestra en la solicitud de consulta delta inicial.</span><span class="sxs-lookup"><span data-stu-id="6fb84-165">The response includes the same set of properties as in the initial delta query request.</span></span> <span data-ttu-id="6fb84-166">Esto le permite capturar el estado actual y completa de los objetos al iniciar el ciclo de delta.</span><span class="sxs-lookup"><span data-stu-id="6fb84-166">This allows you to capture the full current state of the objects when initiating the delta cycle.</span></span>

- <span data-ttu-id="6fb84-167">Si un `deltaLink` se devuelve la dirección URL:</span><span class="sxs-lookup"><span data-stu-id="6fb84-167">If a `deltaLink` URL is returned:</span></span>
  - <span data-ttu-id="6fb84-168">Esto indica que no hay ningún dato más sobre el estado existente del recurso que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="6fb84-168">This indicates there is no more data about the existing state of the resource to be returned.</span></span> <span data-ttu-id="6fb84-169">Guardar y utilizar el `deltaLink` dirección URL para obtener más información acerca de cambia para el recurso en la ronda siguiente.</span><span class="sxs-lookup"><span data-stu-id="6fb84-169">Save and use the `deltaLink` URL to learn about changes to the resource in the next round.</span></span>
  - <span data-ttu-id="6fb84-170">Tiene una opción para especificar el `Prefer:return=minimal` encabezado, que se incluirá en los valores de respuesta sólo para las propiedades que han cambiado desde el momento en que el `deltaLink` se emitió.</span><span class="sxs-lookup"><span data-stu-id="6fb84-170">You have a choice to specify the `Prefer:return=minimal` header, to include in the response values for only the properties that have changed since the time the `deltaLink` was issued.</span></span>

#### <a name="default-return-the-same-properties-as-initial-delta-request"></a><span data-ttu-id="6fb84-171">Valor predeterminado: devolver las mismas propiedades que la solicitud inicial del delta</span><span class="sxs-lookup"><span data-stu-id="6fb84-171">Default: return the same properties as initial delta request</span></span>

<span data-ttu-id="6fb84-172">De forma predeterminada, las solicitudes con un `deltaLink` o `nextLink` devolver las mismas propiedades como seleccionado en la consulta inicial del delta de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="6fb84-172">By default, requests using a `deltaLink` or `nextLink` return the same properties as selected in the initial delta query in the following ways:</span></span>

- <span data-ttu-id="6fb84-173">Si la propiedad ha cambiado, el nuevo valor se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6fb84-173">If the property has changed, the new value is included in the response.</span></span> <span data-ttu-id="6fb84-174">Esto incluye las propiedades que se establezca en un valor null.</span><span class="sxs-lookup"><span data-stu-id="6fb84-174">This includes properties being set to null value.</span></span>
- <span data-ttu-id="6fb84-175">Si no ha cambiado la propiedad, el valor anterior se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6fb84-175">If the property has not changed, the old value is included in the response.</span></span>
- <span data-ttu-id="6fb84-176">Si nunca se ha establecido la propiedad antes de no se incluirá en la respuesta en absoluto.</span><span class="sxs-lookup"><span data-stu-id="6fb84-176">If the property has never been set before it will not be included in the response at all.</span></span>


> <span data-ttu-id="6fb84-177">**Nota:** Con este comportamiento observando la respuesta no es posible saber si va a cambiar de una propiedad o no.</span><span class="sxs-lookup"><span data-stu-id="6fb84-177">**Note:** With this behavior, by looking at the response it is not possible to tell whether a property is changing or not.</span></span> <span data-ttu-id="6fb84-178">Además, las respuestas de delta tienden a ser grandes porque contienen todos los valores de propiedad - tal como se muestra en el [segundo ejemplo](#request-2) siguiente.</span><span class="sxs-lookup"><span data-stu-id="6fb84-178">Also, the delta responses tend to be large because they contain all property values  - as shown in the [second example](#request-2) below.</span></span>

#### <a name="alternative-return-only-the-changed-properties"></a><span data-ttu-id="6fb84-179">Alternativa: devolver sólo las propiedades modificadas</span><span class="sxs-lookup"><span data-stu-id="6fb84-179">Alternative: return only the changed properties</span></span>

<span data-ttu-id="6fb84-180">Adición de un encabezado de solicitud opcional - `prefer:return=minimal` -da como resultado el siguiente comportamiento:</span><span class="sxs-lookup"><span data-stu-id="6fb84-180">Adding an optional request header - `prefer:return=minimal` - results in the following behavior:</span></span>

- <span data-ttu-id="6fb84-181">Si la propiedad ha cambiado, el nuevo valor se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6fb84-181">If the property has changed, the new value is included in the response.</span></span> <span data-ttu-id="6fb84-182">Esto incluye las propiedades que se establezca en un valor null.</span><span class="sxs-lookup"><span data-stu-id="6fb84-182">This includes properties being set to null value.</span></span>
- <span data-ttu-id="6fb84-183">Si no ha cambiado la propiedad, la propiedad no se incluye en la respuesta en absoluto.</span><span class="sxs-lookup"><span data-stu-id="6fb84-183">If the property has not changed, the property is not included in the response at all.</span></span> <span data-ttu-id="6fb84-184">(Distinto del comportamiento predeterminado).</span><span class="sxs-lookup"><span data-stu-id="6fb84-184">(Different from the default behavior.)</span></span>

> <span data-ttu-id="6fb84-185">**Nota:** El encabezado puede agregarse a un `deltaLink` solicitud en cualquier momento en el ciclo de delta.</span><span class="sxs-lookup"><span data-stu-id="6fb84-185">**Note:** The header can be added to a `deltaLink` request at any point in time in the delta cycle.</span></span> <span data-ttu-id="6fb84-186">El encabezado sólo afecta el conjunto de propiedades que se incluyen en la respuesta y no afecta a cómo se ejecuta la consulta de delta.</span><span class="sxs-lookup"><span data-stu-id="6fb84-186">The header only affects the set of properties included in the response and it does not affect how the delta query is executed.</span></span> <span data-ttu-id="6fb84-187">Vea el [tercer ejemplo](#request-3) siguiente.</span><span class="sxs-lookup"><span data-stu-id="6fb84-187">See the [third example](#request-3) below.</span></span>

### <a name="example"></a><span data-ttu-id="6fb84-188">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6fb84-188">Example</span></span>

#### <a name="request-1"></a><span data-ttu-id="6fb84-189">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="6fb84-189">Request 1</span></span>

<span data-ttu-id="6fb84-190">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6fb84-190">The following is an example of the request.</span></span> <span data-ttu-id="6fb84-191">No hay ningún `$select` parámetro, por lo que se realiza un seguimiento y devuelve un conjunto predeterminado de propiedades.</span><span class="sxs-lookup"><span data-stu-id="6fb84-191">There is no `$select` parameter, so a default set of properties is tracked and returned.</span></span>
<!-- {
  "blockType": "request",
  "name": "group_delta"
}-->

```http
GET https://graph.microsoft.com/v1.0/groups/delta
```

#### <a name="response-1"></a><span data-ttu-id="6fb84-192">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="6fb84-192">Response 1</span></span>

<span data-ttu-id="6fb84-193">El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="6fb84-193">The following is an example of the response when using `deltaLink` obtained from the query initialization.</span></span>

><span data-ttu-id="6fb84-194">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="6fb84-194">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="6fb84-195">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6fb84-195">All the properties will be returned from an actual call.</span></span>
>
> <span data-ttu-id="6fb84-196">Tenga en cuenta la presencia de la propiedad *members@delta* que incluye los identificadores de objetos miembros en el grupo.</span><span class="sxs-lookup"><span data-stu-id="6fb84-196">Note the presence of the *members@delta* property which includes the ids of member objects in the group.</span></span>

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

#### <a name="request-2"></a><span data-ttu-id="6fb84-197">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="6fb84-197">Request 2</span></span>

<span data-ttu-id="6fb84-198">En el ejemplo siguiente se muestra la solicitud inicial seleccionando 3 propiedades para el seguimiento de cambios, con comportamiento de respuesta predeterminado:</span><span class="sxs-lookup"><span data-stu-id="6fb84-198">The next example shows the initial request selecting 3 properties for change tracking, with default response behavior:</span></span>
<!-- {
  "blockType": "request",
  "name": "group_delta"
}-->

```http
GET https://graph.microsoft.com/v1.0/groups/delta?$select=displayName,description,mailNickname
```

#### <a name="response-2"></a><span data-ttu-id="6fb84-199">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="6fb84-199">Response 2</span></span>

<span data-ttu-id="6fb84-200">El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="6fb84-200">The following is an example of the response when using `deltaLink` obtained from the query initialization.</span></span> <span data-ttu-id="6fb84-201">Tenga en cuenta que todas las 3 propiedades se incluyen en la respuesta y no se sabe cuáles han cambiado desde la `deltaLink` se ha obtenido.</span><span class="sxs-lookup"><span data-stu-id="6fb84-201">Note that all 3 properties are included in the response and it is not known which ones have changed since the `deltaLink` was obtained.</span></span>

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
      "mailNickname": "mailNickname-value"
    }
  ]
}
```

#### <a name="request-3"></a><span data-ttu-id="6fb84-202">Solicitud 3</span><span class="sxs-lookup"><span data-stu-id="6fb84-202">Request 3</span></span>

<span data-ttu-id="6fb84-203">En el ejemplo siguiente se muestra la solicitud inicial seleccionando 3 propiedades para el seguimiento de cambios, con el comportamiento de respuesta mínimo alternativo:</span><span class="sxs-lookup"><span data-stu-id="6fb84-203">The next example shows the initial request selecting 3 properties for change tracking, with alternative minimal response behavior:</span></span>
<!-- {
  "blockType": "request",
  "name": "group_delta"
}-->

```http
GET https://graph.microsoft.com/v1.0/groups/delta?$select=displayName,description,mailNickname
Prefer: return=minimal
```

#### <a name="response-3"></a><span data-ttu-id="6fb84-204">Respuesta 3</span><span class="sxs-lookup"><span data-stu-id="6fb84-204">Response 3</span></span>

<span data-ttu-id="6fb84-205">El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="6fb84-205">The following is an example of the response when using `deltaLink` obtained from the query initialization.</span></span> <span data-ttu-id="6fb84-206">Tenga en cuenta que el `mailNickname` (propiedad) no se incluye, lo que significa que no ha cambiado desde la última consulta delta; `displayName` y `description` se incluyen lo que significa que se han cambiado sus valores.</span><span class="sxs-lookup"><span data-stu-id="6fb84-206">Note that the `mailNickname` property is not included, which means it has not changed since the last delta query; `displayName` and `description` are included which means their values have changed.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="6fb84-207">Vea también</span><span class="sxs-lookup"><span data-stu-id="6fb84-207">See also</span></span>

- <span data-ttu-id="6fb84-208">[Consulta de delta de uso para realizar un seguimiento de los cambios en datos de Microsoft Graph](/graph/delta-query-overview).</span><span class="sxs-lookup"><span data-stu-id="6fb84-208">[Use delta query to track changes in Microsoft Graph data](/graph/delta-query-overview).</span></span>
- <span data-ttu-id="6fb84-209">[Obtener los cambios incrementales de grupos](/graph/delta-query-groups).</span><span class="sxs-lookup"><span data-stu-id="6fb84-209">[Get incremental changes for groups](/graph/delta-query-groups).</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
