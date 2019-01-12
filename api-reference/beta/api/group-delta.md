---
title: 'grupo: delta'
description: Get recién creado, actualiza o elimina grupos, incluidos los cambios de pertenencia de grupo, sin tener que realizar un acceso completo de lectura de la colección de todo grupo. Para obtener más información, vea Uso de consulta de Delta.
localization_priority: Normal
author: dkershaw10
ms.prod: groups
ms.openlocfilehash: 032dc8906c14ad0ea89ca8eda55d4dc53637efe6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27936329"
---
# <a name="group-delta"></a><span data-ttu-id="b91c9-104">grupo: delta</span><span class="sxs-lookup"><span data-stu-id="b91c9-104">group: delta</span></span>

> <span data-ttu-id="b91c9-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b91c9-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b91c9-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b91c9-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b91c9-107">Get recién creado, actualiza o elimina grupos, incluidos los cambios de pertenencia de grupo, sin tener que realizar un acceso completo de lectura de la colección de todo grupo.</span><span class="sxs-lookup"><span data-stu-id="b91c9-107">Get newly created, updated, or deleted groups, including group membership changes, without having to perform a full read of the entire group collection.</span></span> <span data-ttu-id="b91c9-108">Para obtener más información, vea [Uso de consulta de Delta](/graph/delta-query-overview) .</span><span class="sxs-lookup"><span data-stu-id="b91c9-108">See [Using Delta Query](/graph/delta-query-overview) for details.</span></span>

## <a name="permissions"></a><span data-ttu-id="b91c9-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="b91c9-109">Permissions</span></span>

<span data-ttu-id="b91c9-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b91c9-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b91c9-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b91c9-112">Permission type</span></span>      | <span data-ttu-id="b91c9-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b91c9-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b91c9-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b91c9-114">Delegated (work or school account)</span></span> | <span data-ttu-id="b91c9-115">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b91c9-115">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="b91c9-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b91c9-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b91c9-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b91c9-117">Not supported.</span></span>    |
|<span data-ttu-id="b91c9-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b91c9-118">Application</span></span> | <span data-ttu-id="b91c9-119">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b91c9-119">Group.Read.All, Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="b91c9-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b91c9-120">HTTP request</span></span>

<span data-ttu-id="b91c9-121">Para comenzar los cambios, debe realizar una solicitud incluyendo la función delta en el recurso grupo.</span><span class="sxs-lookup"><span data-stu-id="b91c9-121">To begin tracking changes, you make a request including the delta function on the groups resource.</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /groups/delta
```

## <a name="query-parameters"></a><span data-ttu-id="b91c9-122">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="b91c9-122">Query parameters</span></span>

<span data-ttu-id="b91c9-p105">El seguimiento de cambios en grupos conlleva al menos una llamada de una función **delta**. Si usa cualquier parámetro de consulta (uno diferente a `$deltatoken` y `$skiptoken`), debe especificarlo en la solicitud **delta** inicial. Microsoft Graph codifica automáticamente cualquier parámetro especificado en la parte del token de la URL `nextLink` o `deltaLink` proporcionada en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b91c9-p105">Tracking changes in groups incurs a round of one or more **delta** function calls. If you use any query parameter (other than `$deltatoken` and `$skiptoken`), you must specify it in the initial **delta** request. Microsoft Graph automatically encodes any specified parameters into the token portion of the `nextLink` or `deltaLink` URL provided in the response.</span></span>

<span data-ttu-id="b91c9-126">Solo debe especificar una vez por adelantado los parámetros de consulta deseados.</span><span class="sxs-lookup"><span data-stu-id="b91c9-126">You only need to specify any desired query parameters once upfront.</span></span>

<span data-ttu-id="b91c9-127">En solicitudes posteriores, copie y aplique la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.</span><span class="sxs-lookup"><span data-stu-id="b91c9-127">In subsequent requests, copy and apply the `nextLink` or `deltaLink` URL from the previous response, as that URL already includes the encoded, desired parameters.</span></span>

| <span data-ttu-id="b91c9-128">Parámetro de consulta</span><span class="sxs-lookup"><span data-stu-id="b91c9-128">Query parameter</span></span> | <span data-ttu-id="b91c9-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="b91c9-129">Type</span></span>  |<span data-ttu-id="b91c9-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="b91c9-130">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="b91c9-131">$deltatoken</span><span class="sxs-lookup"><span data-stu-id="b91c9-131">$deltatoken</span></span> | <span data-ttu-id="b91c9-132">string</span><span class="sxs-lookup"><span data-stu-id="b91c9-132">string</span></span> | <span data-ttu-id="b91c9-p106">Un [token de estado](/graph/delta-query-overview) que se devuelve en la URL de `deltaLink` de la llamada de función **delta** anterior para la misma colección de grupos. Indica el progreso de la ronda de seguimiento de cambios. Guarde y aplique toda la dirección URL `deltaLink`, incluido este token, en la primera solicitud de la siguiente ronda de seguimiento de cambios de la colección.</span><span class="sxs-lookup"><span data-stu-id="b91c9-p106">A [state token](/graph/delta-query-overview) returned in the `deltaLink` URL of the previous **delta** function call for the same group collection, indicating the completion of that round of change tracking. Save and apply the entire `deltaLink` URL including this token in the first request of the next round of change tracking for that collection.</span></span>|
| <span data-ttu-id="b91c9-135">$skiptoken</span><span class="sxs-lookup"><span data-stu-id="b91c9-135">$skiptoken</span></span> | <span data-ttu-id="b91c9-136">string</span><span class="sxs-lookup"><span data-stu-id="b91c9-136">string</span></span> | <span data-ttu-id="b91c9-137">Un [token de estado](/graph/delta-query-overview) que se devuelve en la URL de `nextLink` de la llamada de función **delta**. Indica que debe realizarse el seguimiento de más cambios en la misma colección de grupos.</span><span class="sxs-lookup"><span data-stu-id="b91c9-137">A [state token](/graph/delta-query-overview) returned in the `nextLink` URL of the previous **delta** function call, indicating there are further changes to be tracked in the same group collection.</span></span> |

### <a name="odata-query-parameters"></a><span data-ttu-id="b91c9-138">Parámetros de consulta de OData</span><span class="sxs-lookup"><span data-stu-id="b91c9-138">OData query parameters</span></span>

<span data-ttu-id="b91c9-139">Este método es compatible con parámetros opcionales de consulta de OData para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b91c9-139">This method supports optional OData query parameters to help customize the response.</span></span>

- <span data-ttu-id="b91c9-p107">Puede utilizar un parámetro de consulta `$select` como en cualquier solicitud GET para especificar solo las propiedades que necesita para un mejor rendimiento. Siempre se devuelve la propiedad *id*.</span><span class="sxs-lookup"><span data-stu-id="b91c9-p107">You can use a `$select` query parameter as in any GET request to specify only the properties your need for best performance. The *id* property is always returned.</span></span>
- <span data-ttu-id="b91c9-142">Puede usar `$expand=members` para obtener los cambios de pertenencia.</span><span class="sxs-lookup"><span data-stu-id="b91c9-142">You can use `$expand=members` to get membership changes.</span></span>
- <span data-ttu-id="b91c9-143">No hay compatibilidad limitada para `$filter`:</span><span class="sxs-lookup"><span data-stu-id="b91c9-143">There is limited support for `$filter`:</span></span>
  - <span data-ttu-id="b91c9-144">La única expresión `$filter` admitida es para realizar un seguimiento de los cambios en un objeto específico: `$filter=id+eq+{value}`.</span><span class="sxs-lookup"><span data-stu-id="b91c9-144">The only supported `$filter` expression is for tracking changes on a specific object: `$filter=id+eq+{value}`.</span></span> <span data-ttu-id="b91c9-145">Puede filtrar varios objetos.</span><span class="sxs-lookup"><span data-stu-id="b91c9-145">You can filter multiple objects.</span></span> <span data-ttu-id="b91c9-146">Por ejemplo, `https://graph.microsoft.com/beta/groups/delta/?$filter= id eq '477e9fc6-5de7-4406-bb2a-7e5c83c9ffff' or id eq '004d6a07-fe70-4b92-add5-e6e37b8affff'`.</span><span class="sxs-lookup"><span data-stu-id="b91c9-146">For example, `https://graph.microsoft.com/beta/groups/delta/?$filter= id eq '477e9fc6-5de7-4406-bb2a-7e5c83c9ffff' or id eq '004d6a07-fe70-4b92-add5-e6e37b8affff'`.</span></span> <span data-ttu-id="b91c9-147">Hay un límite de 50 objetos filtrados.</span><span class="sxs-lookup"><span data-stu-id="b91c9-147">There is a limit of 50 filtered objects.</span></span>

## <a name="request-headers"></a><span data-ttu-id="b91c9-148">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b91c9-148">Request headers</span></span>

| <span data-ttu-id="b91c9-149">Nombre</span><span class="sxs-lookup"><span data-stu-id="b91c9-149">Name</span></span>       | <span data-ttu-id="b91c9-150">Descripción</span><span class="sxs-lookup"><span data-stu-id="b91c9-150">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="b91c9-151">Authorization</span><span class="sxs-lookup"><span data-stu-id="b91c9-151">Authorization</span></span>  | <span data-ttu-id="b91c9-152">&lt;token&gt; de portador</span><span class="sxs-lookup"><span data-stu-id="b91c9-152">Bearer &lt;token&gt;</span></span>|
| <span data-ttu-id="b91c9-153">Content-Type</span><span class="sxs-lookup"><span data-stu-id="b91c9-153">Content-Type</span></span>  | <span data-ttu-id="b91c9-154">application/json</span><span class="sxs-lookup"><span data-stu-id="b91c9-154">application/json</span></span> |
| <span data-ttu-id="b91c9-155">Prefer</span><span class="sxs-lookup"><span data-stu-id="b91c9-155">Prefer</span></span> | <span data-ttu-id="b91c9-156">devolver = mínimo</span><span class="sxs-lookup"><span data-stu-id="b91c9-156">return=minimal</span></span> <br><br><span data-ttu-id="b91c9-157">Si se especifica este encabezado con una solicitud que utiliza un `deltaLink` devolvería sólo las propiedades del objeto que han cambiado desde la última round.</span><span class="sxs-lookup"><span data-stu-id="b91c9-157">Specifying this header with a request that uses a `deltaLink` would return only the object properties that have changed since the last round.</span></span> <span data-ttu-id="b91c9-158">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b91c9-158">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b91c9-159">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b91c9-159">Request body</span></span>

<span data-ttu-id="b91c9-160">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b91c9-160">Do not supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="b91c9-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b91c9-161">Response</span></span>

<span data-ttu-id="b91c9-162">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección [grupo](../resources/group.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b91c9-162">If successful, this method returns `200 OK` response code and [group](../resources/group.md) collection object in the response body.</span></span> <span data-ttu-id="b91c9-163">La respuesta incluye también un símbolo (token) de estado que puede ser un `nextLink` dirección URL o un `deltaLink` dirección URL.</span><span class="sxs-lookup"><span data-stu-id="b91c9-163">The response also includes a state token which is either a `nextLink` URL or a `deltaLink` URL.</span></span>

- <span data-ttu-id="b91c9-164">Si un `nextLink` se devuelve la dirección URL:</span><span class="sxs-lookup"><span data-stu-id="b91c9-164">If a `nextLink` URL is returned:</span></span>
  - <span data-ttu-id="b91c9-165">Esto indica que hay páginas adicionales de datos que se recuperarán en la sesión.</span><span class="sxs-lookup"><span data-stu-id="b91c9-165">This indicates there are additional pages of data to be retrieved in the session.</span></span> <span data-ttu-id="b91c9-166">La aplicación continúa realizar solicitudes mediante el `nextLink` dirección URL hasta un `deltaLink` dirección URL se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b91c9-166">The application continues making requests using the `nextLink` URL until a `deltaLink` URL is included in the response.</span></span>
  - <span data-ttu-id="b91c9-167">La respuesta incluye el mismo conjunto de propiedades como se muestra en la solicitud de consulta delta inicial.</span><span class="sxs-lookup"><span data-stu-id="b91c9-167">The response includes the same set of properties as in the initial delta query request.</span></span> <span data-ttu-id="b91c9-168">Esto le permite capturar el estado actual y completa de los objetos al iniciar el ciclo de delta.</span><span class="sxs-lookup"><span data-stu-id="b91c9-168">This allows you to capture the full current state of the objects when initiating the delta cycle.</span></span>

- <span data-ttu-id="b91c9-169">Si un `deltaLink` se devuelve la dirección URL:</span><span class="sxs-lookup"><span data-stu-id="b91c9-169">If a `deltaLink` URL is returned:</span></span>
  - <span data-ttu-id="b91c9-170">Esto indica que no hay ningún dato más sobre el estado existente del recurso que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="b91c9-170">This indicates there is no more data about the existing state of the resource to be returned.</span></span> <span data-ttu-id="b91c9-171">Guardar y utilizar el `deltaLink` dirección URL para obtener más información acerca de cambia para el recurso en la ronda siguiente.</span><span class="sxs-lookup"><span data-stu-id="b91c9-171">Save and use the `deltaLink` URL to learn about changes to the resource in the next round.</span></span>
  - <span data-ttu-id="b91c9-172">Tiene una opción para especificar el `Prefer:return=minimal` encabezado, que se incluirá en los valores de respuesta sólo para las propiedades que han cambiado desde el momento en que el `deltaLink` se emitió.</span><span class="sxs-lookup"><span data-stu-id="b91c9-172">You have a choice to specify the `Prefer:return=minimal` header, to include in the response values for only the properties that have changed since the time the `deltaLink` was issued.</span></span>

#### <a name="default-return-the-same-properties-as-initial-delta-request"></a><span data-ttu-id="b91c9-173">Valor predeterminado: devolver las mismas propiedades que la solicitud inicial del delta</span><span class="sxs-lookup"><span data-stu-id="b91c9-173">Default: return the same properties as initial delta request</span></span>

<span data-ttu-id="b91c9-174">De forma predeterminada, las solicitudes con un `deltaLink` o `nextLink` devolver las mismas propiedades como seleccionado en la consulta inicial del delta de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="b91c9-174">By default, requests using a `deltaLink` or `nextLink` return the same properties as selected in the initial delta query in the following ways:</span></span>

- <span data-ttu-id="b91c9-175">Si la propiedad ha cambiado, el nuevo valor se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b91c9-175">If the property has changed, the new value is included in the response.</span></span> <span data-ttu-id="b91c9-176">Esto incluye las propiedades que se establezca en un valor null.</span><span class="sxs-lookup"><span data-stu-id="b91c9-176">This includes properties being set to null value.</span></span>
- <span data-ttu-id="b91c9-177">Si no ha cambiado la propiedad, el valor anterior se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b91c9-177">If the property has not changed, the old value is included in the response.</span></span>
- <span data-ttu-id="b91c9-178">Si nunca se ha establecido la propiedad antes de no se incluirá en la respuesta en absoluto.</span><span class="sxs-lookup"><span data-stu-id="b91c9-178">If the property has never been set before it will not be included in the response at all.</span></span>


> <span data-ttu-id="b91c9-179">**Nota:** Con este comportamiento observando la respuesta no es posible saber si va a cambiar de una propiedad o no.</span><span class="sxs-lookup"><span data-stu-id="b91c9-179">**Note:** With this behavior, by looking at the response it is not possible to tell whether a property is changing or not.</span></span> <span data-ttu-id="b91c9-180">Además, las respuestas de delta tienden a ser grandes porque contienen todos los valores de propiedad - tal como se muestra en el [segundo ejemplo](#request-2) siguiente.</span><span class="sxs-lookup"><span data-stu-id="b91c9-180">Also, the delta responses tend to be large because they contain all property values  - as shown in the [second example](#request-2) below.</span></span>

#### <a name="alternative-return-only-the-changed-properties"></a><span data-ttu-id="b91c9-181">Alternativa: devolver sólo las propiedades modificadas</span><span class="sxs-lookup"><span data-stu-id="b91c9-181">Alternative: return only the changed properties</span></span>

<span data-ttu-id="b91c9-182">Adición de un encabezado de solicitud opcional - `prefer:return=minimal` -da como resultado el siguiente comportamiento:</span><span class="sxs-lookup"><span data-stu-id="b91c9-182">Adding an optional request header - `prefer:return=minimal` - results in the following behavior:</span></span>

- <span data-ttu-id="b91c9-183">Si la propiedad ha cambiado, el nuevo valor se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b91c9-183">If the property has changed, the new value is included in the response.</span></span> <span data-ttu-id="b91c9-184">Esto incluye las propiedades que se establezca en un valor null.</span><span class="sxs-lookup"><span data-stu-id="b91c9-184">This includes properties being set to null value.</span></span>
- <span data-ttu-id="b91c9-185">Si no ha cambiado la propiedad, la propiedad no se incluye en la respuesta en absoluto.</span><span class="sxs-lookup"><span data-stu-id="b91c9-185">If the property has not changed, the property is not included in the response at all.</span></span> <span data-ttu-id="b91c9-186">(Distinto del comportamiento predeterminado).</span><span class="sxs-lookup"><span data-stu-id="b91c9-186">(Different from the default behavior.)</span></span>

> <span data-ttu-id="b91c9-187">**Nota:** El encabezado puede agregarse a un `deltaLink` solicitud en cualquier momento en el ciclo de delta.</span><span class="sxs-lookup"><span data-stu-id="b91c9-187">**Note:** The header can be added to a `deltaLink` request at any point in time in the delta cycle.</span></span> <span data-ttu-id="b91c9-188">El encabezado sólo afecta el conjunto de propiedades que se incluyen en la respuesta y no afecta a cómo se ejecuta la consulta de delta.</span><span class="sxs-lookup"><span data-stu-id="b91c9-188">The header only affects the set of properties included in the response and it does not affect how the delta query is executed.</span></span> <span data-ttu-id="b91c9-189">Vea el [tercer ejemplo](#request-3) siguiente.</span><span class="sxs-lookup"><span data-stu-id="b91c9-189">See the [third example](#request-3) below.</span></span>

### <a name="example"></a><span data-ttu-id="b91c9-190">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b91c9-190">Example</span></span>

#### <a name="request-1"></a><span data-ttu-id="b91c9-191">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="b91c9-191">Request 1</span></span>

<span data-ttu-id="b91c9-192">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b91c9-192">The following is an example of the request.</span></span> <span data-ttu-id="b91c9-193">No hay ningún `$select` parámetro, por lo que se realiza un seguimiento y devuelve un conjunto predeterminado de propiedades.</span><span class="sxs-lookup"><span data-stu-id="b91c9-193">There is no `$select` parameter, so a default set of properties is tracked and returned.</span></span>
<!-- {
  "blockType": "request",
  "name": "group_delta"
}-->

```http
GET https://graph.microsoft.com/beta/groups/delta
```

#### <a name="response-1"></a><span data-ttu-id="b91c9-194">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="b91c9-194">Response 1</span></span>

<span data-ttu-id="b91c9-195">El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="b91c9-195">The following is an example of the response when using `deltaLink` obtained from the query initialization.</span></span>

><span data-ttu-id="b91c9-196">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="b91c9-196">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="b91c9-197">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b91c9-197">All the properties will be returned from an actual call.</span></span>
>
> <span data-ttu-id="b91c9-198">Tenga en cuenta la presencia de la propiedad *members@delta* que incluye los identificadores de objetos miembros en el grupo.</span><span class="sxs-lookup"><span data-stu-id="b91c9-198">Note the presence of the *members@delta* property which includes the ids of member objects in the group.</span></span>

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
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#groups","@odata.nextLink":"https://graph.microsoft.com/beta/groups/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjvY1FSSc_",
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

#### <a name="request-2"></a><span data-ttu-id="b91c9-199">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="b91c9-199">Request 2</span></span>

<span data-ttu-id="b91c9-200">En el ejemplo siguiente se muestra la solicitud inicial seleccionando 3 propiedades para el seguimiento de cambios, con comportamiento de respuesta predeterminado:</span><span class="sxs-lookup"><span data-stu-id="b91c9-200">The next example shows the initial request selecting 3 properties for change tracking, with default response behavior:</span></span>
<!-- {
  "blockType": "request",
  "name": "group_delta"
}-->

```http
GET https://graph.microsoft.com/beta/groups/delta?$select=displayName,description,mailNickname
```

#### <a name="response-2"></a><span data-ttu-id="b91c9-201">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="b91c9-201">Response 2</span></span>

<span data-ttu-id="b91c9-202">El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="b91c9-202">The following is an example of the response when using `deltaLink` obtained from the query initialization.</span></span> <span data-ttu-id="b91c9-203">Tenga en cuenta que todas las 3 propiedades se incluyen en la respuesta y no se sabe cuáles han cambiado desde la `deltaLink` se ha obtenido.</span><span class="sxs-lookup"><span data-stu-id="b91c9-203">Note that all 3 properties are included in the response and it is not known which ones have changed since the `deltaLink` was obtained.</span></span>

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
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#groups",
  "@odata.nextLink":"https://graph.microsoft.com/beta/groups/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjsXoYQp_dpA3cNJWc",
  "value": [
    {
      "displayName": "displayName-value",
      "description": null,
      "mailNickname": "mailNickname-value"
    }
  ]
}
```

#### <a name="request-3"></a><span data-ttu-id="b91c9-204">Solicitud 3</span><span class="sxs-lookup"><span data-stu-id="b91c9-204">Request 3</span></span>

<span data-ttu-id="b91c9-205">En el ejemplo siguiente se muestra la solicitud inicial seleccionando 3 propiedades para el seguimiento de cambios, con el comportamiento de respuesta mínimo alternativo:</span><span class="sxs-lookup"><span data-stu-id="b91c9-205">The next example shows the initial request selecting 3 properties for change tracking, with alternative minimal response behavior:</span></span>
<!-- {
  "blockType": "request",
  "name": "group_delta"
}-->

```http
GET https://graph.microsoft.com/beta/groups/delta?$select=displayName,description,mailNickname
Prefer: return=minimal
```

#### <a name="response-3"></a><span data-ttu-id="b91c9-206">Respuesta 3</span><span class="sxs-lookup"><span data-stu-id="b91c9-206">Response 3</span></span>

<span data-ttu-id="b91c9-207">El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="b91c9-207">The following is an example of the response when using `deltaLink` obtained from the query initialization.</span></span> <span data-ttu-id="b91c9-208">Tenga en cuenta que el `mailNickname` (propiedad) no se incluye, lo que significa que no ha cambiado desde la última consulta delta; `displayName` y `description` se incluyen lo que significa que se han cambiado sus valores.</span><span class="sxs-lookup"><span data-stu-id="b91c9-208">Note that the `mailNickname` property is not included, which means it has not changed since the last delta query; `displayName` and `description` are included which means their values have changed.</span></span>

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
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#groups",
  "@odata.nextLink":"https://graph.microsoft.com/beta/groups/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjsXoYQp_dpA3cNJWc",
  "value": [
    {
      "displayName": "displayName-value",
      "description": null
    }
  ]
}
```

## <a name="see-also"></a><span data-ttu-id="b91c9-209">Vea también</span><span class="sxs-lookup"><span data-stu-id="b91c9-209">See also</span></span>

- <span data-ttu-id="b91c9-210">[Consulta de delta de uso para realizar un seguimiento de los cambios en datos de Microsoft Graph](/graph/delta-query-overview).</span><span class="sxs-lookup"><span data-stu-id="b91c9-210">[Use delta query to track changes in Microsoft Graph data](/graph/delta-query-overview).</span></span>
- <span data-ttu-id="b91c9-211">[Obtener los cambios incrementales de grupos](/graph/delta-query-groups).</span><span class="sxs-lookup"><span data-stu-id="b91c9-211">[Get incremental changes for groups](/graph/delta-query-groups).</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
