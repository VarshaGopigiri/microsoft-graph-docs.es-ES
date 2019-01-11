---
title: 'user: delta'
description: Get recién creado, actualiza o elimina los usuarios sin tener que realizar un acceso completo de lectura de la colección completa de usuario. Vea control de cambios para obtener información detallada.
localization_priority: Normal
ms.openlocfilehash: 2aaee8a5722c22ad8fc381f0a4b1d577461b3991
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27856199"
---
# <a name="user-delta"></a><span data-ttu-id="c0a40-104">user: delta</span><span class="sxs-lookup"><span data-stu-id="c0a40-104">user: delta</span></span>

> <span data-ttu-id="c0a40-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c0a40-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c0a40-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c0a40-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c0a40-107">Get recién creado, actualiza o elimina los usuarios sin tener que realizar un acceso completo de lectura de la colección completa de usuario.</span><span class="sxs-lookup"><span data-stu-id="c0a40-107">Get newly created, updated, or deleted users without having to perform a full read of the entire user collection.</span></span> <span data-ttu-id="c0a40-108">Para obtener información detallada, vea [control de cambios](/graph/delta-query-overview) .</span><span class="sxs-lookup"><span data-stu-id="c0a40-108">See [Track changes](/graph/delta-query-overview) for details.</span></span>

## <a name="permissions"></a><span data-ttu-id="c0a40-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="c0a40-109">Permissions</span></span>

<span data-ttu-id="c0a40-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c0a40-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="c0a40-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c0a40-112">Permission type</span></span>      | <span data-ttu-id="c0a40-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c0a40-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c0a40-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c0a40-114">Delegated (work or school account)</span></span> | <span data-ttu-id="c0a40-115">User.Read, User.ReadWrite, User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="c0a40-115">User.Read, User.ReadWrite, User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="c0a40-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c0a40-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c0a40-117">User.Read, User.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c0a40-117">User.Read, User.ReadWrite</span></span>    |
|<span data-ttu-id="c0a40-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c0a40-118">Application</span></span> | <span data-ttu-id="c0a40-119">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c0a40-119">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c0a40-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c0a40-120">HTTP request</span></span>

<span data-ttu-id="c0a40-121">Para comenzar los cambios, debe realizar una solicitud incluyendo la función delta en el recurso de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="c0a40-121">To begin tracking changes, you make a request including the delta function on the users resource.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /users/delta
```

## <a name="query-parameters"></a><span data-ttu-id="c0a40-122">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="c0a40-122">Query parameters</span></span>

<span data-ttu-id="c0a40-123">Seguimiento de los cambios en los usuarios incurre en una ronda de una o más llamadas de función de **delta** .</span><span class="sxs-lookup"><span data-stu-id="c0a40-123">Tracking changes in users incurs a round of one or more **delta** function calls.</span></span> <span data-ttu-id="c0a40-124">Si usa cualquier parámetro de consulta (distinto de `$deltatoken` y `$skiptoken`), debe especificar en la solicitud inicial del **delta** .</span><span class="sxs-lookup"><span data-stu-id="c0a40-124">If you use any query parameter (other than `$deltatoken` and `$skiptoken`), you must specify it in the initial **delta** request.</span></span> <span data-ttu-id="c0a40-125">Microsoft Graph codifica automáticamente los parámetros especificados en la parte de símbolo (token) de la `nextLink` o `deltaLink` dirección URL proporcionada en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0a40-125">Microsoft Graph automatically encodes any specified parameters into the token portion of the `nextLink` or `deltaLink` URL provided in the response.</span></span>

<span data-ttu-id="c0a40-126">Solo debe especificar una vez por adelantado los parámetros de consulta deseados.</span><span class="sxs-lookup"><span data-stu-id="c0a40-126">You only need to specify any desired query parameters once upfront.</span></span>

<span data-ttu-id="c0a40-127">En solicitudes posteriores, copie y aplique la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.</span><span class="sxs-lookup"><span data-stu-id="c0a40-127">In subsequent requests, copy and apply the `nextLink` or `deltaLink` URL from the previous response, as that URL already includes the encoded, desired parameters.</span></span>

| <span data-ttu-id="c0a40-128">Parámetro de consulta</span><span class="sxs-lookup"><span data-stu-id="c0a40-128">Query parameter</span></span>      | <span data-ttu-id="c0a40-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="c0a40-129">Type</span></span>   |<span data-ttu-id="c0a40-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0a40-130">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="c0a40-131">$deltatoken</span><span class="sxs-lookup"><span data-stu-id="c0a40-131">$deltatoken</span></span> | <span data-ttu-id="c0a40-132">string</span><span class="sxs-lookup"><span data-stu-id="c0a40-132">string</span></span> | <span data-ttu-id="c0a40-p106">Un [token de estado](/graph/delta-query-overview) que se devuelve en la dirección URL de `deltaLink` de la llamada de función **delta** anterior para la misma colección de usuarios. Indica el progreso de la ronda de seguimiento de cambios. Guarde y aplique toda la dirección URL `deltaLink`, incluido este token, en la primera solicitud de la siguiente ronda de seguimiento de cambios de la colección.</span><span class="sxs-lookup"><span data-stu-id="c0a40-p106">A [state token](/graph/delta-query-overview) returned in the `deltaLink` URL of the previous **delta** function call for the same user collection, indicating the completion of that round of change tracking. Save and apply the entire `deltaLink` URL including this token in the first request of the next round of change tracking for that collection.</span></span>|
| <span data-ttu-id="c0a40-135">$skiptoken</span><span class="sxs-lookup"><span data-stu-id="c0a40-135">$skiptoken</span></span> | <span data-ttu-id="c0a40-136">string</span><span class="sxs-lookup"><span data-stu-id="c0a40-136">string</span></span> | <span data-ttu-id="c0a40-137">Un [token de estado](/graph/delta-query-overview) que se devuelve en la dirección URL de `nextLink` de la llamada de función **delta**. Indica que debe realizarse el seguimiento de más cambios en la misma colección de usuarios.</span><span class="sxs-lookup"><span data-stu-id="c0a40-137">A [state token](/graph/delta-query-overview) returned in the `nextLink` URL of the previous **delta** function call, indicating there are further changes to be tracked in the same user collection.</span></span> |

### <a name="odata-query-parameters"></a><span data-ttu-id="c0a40-138">Parámetros de consulta de OData</span><span class="sxs-lookup"><span data-stu-id="c0a40-138">OData query parameters</span></span>

<span data-ttu-id="c0a40-139">Este método es compatible con parámetros opcionales de consulta de OData para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0a40-139">This method supports optional OData Query Parameters to help customize the response.</span></span>

- <span data-ttu-id="c0a40-p107">Puede utilizar un parámetro de consulta `$select` como en cualquier solicitud GET para especificar solo las propiedades que necesita para un mejor rendimiento. Siempre se devuelve la propiedad *id*.</span><span class="sxs-lookup"><span data-stu-id="c0a40-p107">You can use a `$select` query parameter as in any GET request to specify only the properties your need for best performance. The *id* property is always returned.</span></span>
- <span data-ttu-id="c0a40-142">No hay compatibilidad limitada para `$filter`:</span><span class="sxs-lookup"><span data-stu-id="c0a40-142">There is limited support for `$filter`:</span></span>
  - <span data-ttu-id="c0a40-143">La única expresión `$filter` admitida es para realizar un seguimiento de los cambios en un objeto específico: `$filter=id+eq+{value}`.</span><span class="sxs-lookup"><span data-stu-id="c0a40-143">The only supported `$filter` expression is for tracking changes on a specific object: `$filter=id+eq+{value}`.</span></span> <span data-ttu-id="c0a40-144">Puede filtrar varios objetos.</span><span class="sxs-lookup"><span data-stu-id="c0a40-144">You can filter multiple objects.</span></span> <span data-ttu-id="c0a40-145">Por ejemplo, `https://graph.microsoft.com/beta/users/delta/?$filter= id eq '477e9fc6-5de7-4406-bb2a-7e5c83c9ffff' or id eq '004d6a07-fe70-4b92-add5-e6e37b8affff'`.</span><span class="sxs-lookup"><span data-stu-id="c0a40-145">For example, `https://graph.microsoft.com/beta/users/delta/?$filter= id eq '477e9fc6-5de7-4406-bb2a-7e5c83c9ffff' or id eq '004d6a07-fe70-4b92-add5-e6e37b8affff'`.</span></span> <span data-ttu-id="c0a40-146">Hay un límite de 50 objetos filtrados.</span><span class="sxs-lookup"><span data-stu-id="c0a40-146">There is a limit of 50 filtered objects.</span></span>

## <a name="request-headers"></a><span data-ttu-id="c0a40-147">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c0a40-147">Request headers</span></span>
| <span data-ttu-id="c0a40-148">Nombre</span><span class="sxs-lookup"><span data-stu-id="c0a40-148">Name</span></span>       | <span data-ttu-id="c0a40-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0a40-149">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="c0a40-150">Authorization</span><span class="sxs-lookup"><span data-stu-id="c0a40-150">Authorization</span></span>  | <span data-ttu-id="c0a40-151">&lt;token&gt; de portador</span><span class="sxs-lookup"><span data-stu-id="c0a40-151">Bearer &lt;token&gt;</span></span>|
| <span data-ttu-id="c0a40-152">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c0a40-152">Content-Type</span></span>  | <span data-ttu-id="c0a40-153">application/json</span><span class="sxs-lookup"><span data-stu-id="c0a40-153">application/json</span></span> |
| <span data-ttu-id="c0a40-154">Prefer</span><span class="sxs-lookup"><span data-stu-id="c0a40-154">Prefer</span></span> | <span data-ttu-id="c0a40-155">devolver = mínimo</span><span class="sxs-lookup"><span data-stu-id="c0a40-155">return=minimal</span></span> <br><br><span data-ttu-id="c0a40-156">Si se especifica este encabezado con una solicitud que utiliza un `deltaLink` devolvería sólo las propiedades del objeto que han cambiado desde la última round.</span><span class="sxs-lookup"><span data-stu-id="c0a40-156">Specifying this header with a request that uses a `deltaLink` would return only the object properties that have changed since the last round.</span></span> <span data-ttu-id="c0a40-157">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c0a40-157">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c0a40-158">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c0a40-158">Request body</span></span>
<span data-ttu-id="c0a40-159">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c0a40-159">Do not supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="c0a40-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c0a40-160">Response</span></span>

<span data-ttu-id="c0a40-161">Si tiene éxito, este método devuelve `200 OK` objeto de colección de respuesta código y [usuario](../resources/user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0a40-161">If successful, this method returns `200 OK` response code and [user](../resources/user.md) collection object in the response body.</span></span> <span data-ttu-id="c0a40-162">La respuesta incluye también un `nextLink` dirección URL o un `deltaLink` dirección URL.</span><span class="sxs-lookup"><span data-stu-id="c0a40-162">The response also includes a `nextLink` URL or a `deltaLink` URL.</span></span>

- <span data-ttu-id="c0a40-163">Si un `nextLink` se devuelve la dirección URL:</span><span class="sxs-lookup"><span data-stu-id="c0a40-163">If a `nextLink` URL is returned:</span></span>
  - <span data-ttu-id="c0a40-164">Esto indica que hay páginas adicionales de datos que se recuperarán en la sesión.</span><span class="sxs-lookup"><span data-stu-id="c0a40-164">This indicates there are additional pages of data to be retrieved in the session.</span></span> <span data-ttu-id="c0a40-165">La aplicación continúa realizar solicitudes mediante el `nextLink` dirección URL hasta un `deltaLink` dirección URL se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0a40-165">The application continues making requests using the `nextLink` URL until a `deltaLink` URL is included in the response.</span></span>
  - <span data-ttu-id="c0a40-166">La respuesta incluye el mismo conjunto de propiedades como se muestra en la solicitud de consulta delta inicial.</span><span class="sxs-lookup"><span data-stu-id="c0a40-166">The response includes the same set of properties as in the initial delta query request.</span></span> <span data-ttu-id="c0a40-167">Esto le permite capturar el estado actual y completa de los objetos al iniciar el ciclo de delta.</span><span class="sxs-lookup"><span data-stu-id="c0a40-167">This allows you to capture the full current state of the objects when initiating the delta cycle.</span></span>

- <span data-ttu-id="c0a40-168">Si un `deltaLink` se devuelve la dirección URL:</span><span class="sxs-lookup"><span data-stu-id="c0a40-168">If a `deltaLink` URL is returned:</span></span>
  - <span data-ttu-id="c0a40-169">Esto indica que no hay ningún dato más sobre el estado existente del recurso que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="c0a40-169">This indicates there is no more data about the existing state of the resource to be returned.</span></span> <span data-ttu-id="c0a40-170">Guardar y utilizar el `deltaLink` dirección URL para obtener más información acerca de cambia para el recurso en la ronda siguiente.</span><span class="sxs-lookup"><span data-stu-id="c0a40-170">Save and use the `deltaLink` URL to learn about changes to the resource in the next round.</span></span>
  - <span data-ttu-id="c0a40-171">Tiene una opción para especificar el `Prefer:return=minimal` encabezado, que se incluirá en los valores de respuesta sólo para las propiedades que han cambiado desde el momento en que el `deltaLink` se emitió.</span><span class="sxs-lookup"><span data-stu-id="c0a40-171">You have a choice to specify the `Prefer:return=minimal` header, to include in the response values for only the properties that have changed since the time the `deltaLink` was issued.</span></span>

#### <a name="default-return-the-same-properties-as-initial-delta-request"></a><span data-ttu-id="c0a40-172">Valor predeterminado: devolver las mismas propiedades que la solicitud inicial del delta</span><span class="sxs-lookup"><span data-stu-id="c0a40-172">Default: return the same properties as initial delta request</span></span>

<span data-ttu-id="c0a40-173">De forma predeterminada, las solicitudes con un `deltaLink` o `nextLink` devolver las mismas propiedades como seleccionado en la consulta inicial del delta de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="c0a40-173">By default, requests using a `deltaLink` or `nextLink` return the same properties as selected in the initial delta query in the following ways:</span></span>

- <span data-ttu-id="c0a40-174">Si la propiedad ha cambiado, el nuevo valor se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0a40-174">If the property has changed, the new value is included in the response.</span></span> <span data-ttu-id="c0a40-175">Esto incluye las propiedades que se establezca en un valor null.</span><span class="sxs-lookup"><span data-stu-id="c0a40-175">This includes properties being set to null value.</span></span>
- <span data-ttu-id="c0a40-176">Si no ha cambiado la propiedad, el valor anterior se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0a40-176">If the property has not changed, the old value is included in the response.</span></span>
- <span data-ttu-id="c0a40-177">Si nunca se ha establecido la propiedad antes de no se incluirá en la respuesta en absoluto.</span><span class="sxs-lookup"><span data-stu-id="c0a40-177">If the property has never been set before it will not be included in the response at all.</span></span>


> <span data-ttu-id="c0a40-178">**Nota:** Con este comportamiento observando la respuesta no es posible saber si va a cambiar de una propiedad o no.</span><span class="sxs-lookup"><span data-stu-id="c0a40-178">**Note:** With this behavior, by looking at the response it is not possible to tell whether a property is changing or not.</span></span> <span data-ttu-id="c0a40-179">Además, las respuestas de delta tienden a ser grandes porque contienen todos los valores de propiedad - tal como se muestra en el [segundo ejemplo](#request-2) siguiente.</span><span class="sxs-lookup"><span data-stu-id="c0a40-179">Also, the delta responses tend to be large because they contain all property values  - as shown in the [second example](#request-2) below.</span></span>

#### <a name="alternative-return-only-the-changed-properties"></a><span data-ttu-id="c0a40-180">Alternativa: devolver sólo las propiedades modificadas</span><span class="sxs-lookup"><span data-stu-id="c0a40-180">Alternative: return only the changed properties</span></span>

<span data-ttu-id="c0a40-181">Adición de un encabezado de solicitud opcional - `prefer:return=minimal` -da como resultado el siguiente comportamiento:</span><span class="sxs-lookup"><span data-stu-id="c0a40-181">Adding an optional request header - `prefer:return=minimal` - results in the following behavior:</span></span>

- <span data-ttu-id="c0a40-182">Si la propiedad ha cambiado, el nuevo valor se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0a40-182">If the property has changed, the new value is included in the response.</span></span> <span data-ttu-id="c0a40-183">Esto incluye las propiedades que se establezca en un valor null.</span><span class="sxs-lookup"><span data-stu-id="c0a40-183">This includes properties being set to null value.</span></span>
- <span data-ttu-id="c0a40-184">Si no ha cambiado la propiedad, la propiedad no se incluye en la respuesta en absoluto.</span><span class="sxs-lookup"><span data-stu-id="c0a40-184">If the property has not changed, the property is not included in the response at all.</span></span> <span data-ttu-id="c0a40-185">(Distinto del comportamiento predeterminado).</span><span class="sxs-lookup"><span data-stu-id="c0a40-185">(Different from the default behavior.)</span></span>

> <span data-ttu-id="c0a40-186">**Nota:** El encabezado puede agregarse a un `deltaLink` solicitud en cualquier momento en el ciclo de delta.</span><span class="sxs-lookup"><span data-stu-id="c0a40-186">**Note:** The header can be added to a `deltaLink` request at any point in time in the delta cycle.</span></span> <span data-ttu-id="c0a40-187">El encabezado sólo afecta el conjunto de propiedades que se incluyen en la respuesta y no afecta a cómo se ejecuta la consulta de delta.</span><span class="sxs-lookup"><span data-stu-id="c0a40-187">The header only affects the set of properties included in the response and it does not affect how the delta query is executed.</span></span> <span data-ttu-id="c0a40-188">Vea el [tercer ejemplo](#request-3) siguiente.</span><span class="sxs-lookup"><span data-stu-id="c0a40-188">See the [third example](#request-3) below.</span></span>

### <a name="example"></a><span data-ttu-id="c0a40-189">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c0a40-189">Example</span></span>

#### <a name="request-1"></a><span data-ttu-id="c0a40-190">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="c0a40-190">Request 1</span></span>

<span data-ttu-id="c0a40-191">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c0a40-191">The following is an example of the request.</span></span> <span data-ttu-id="c0a40-192">No hay ningún `$select` parámetro, por lo que se realiza un seguimiento y devuelve un conjunto predeterminado de propiedades.</span><span class="sxs-lookup"><span data-stu-id="c0a40-192">There is no `$select` parameter, so a default set of properties is tracked and returned.</span></span>
<!-- {
  "blockType": "request",
  "name": "user_delta"
}-->

```http
GET https://graph.microsoft.com/beta/users/delta
```

#### <a name="response-1"></a><span data-ttu-id="c0a40-193">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="c0a40-193">Response 1</span></span>

<span data-ttu-id="c0a40-194">El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="c0a40-194">The following is an example of the response when using `deltaLink` obtained from the query initialization.</span></span>

><span data-ttu-id="c0a40-p120">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c0a40-p120">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#users",
  "@odata.nextLink":"https://graph.microsoft.com/beta/users/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjsXoYQp_dpA3cNJWc",
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

#### <a name="request-2"></a><span data-ttu-id="c0a40-197">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="c0a40-197">Request 2</span></span>

<span data-ttu-id="c0a40-198">En el ejemplo siguiente se muestra la solicitud inicial seleccionando 3 propiedades para el seguimiento de cambios, con comportamiento de respuesta predeterminado:</span><span class="sxs-lookup"><span data-stu-id="c0a40-198">The next example shows the initial request selecting 3 properties for change tracking, with default response behavior:</span></span>
<!-- {
  "blockType": "request",
  "name": "user_delta"
}-->

```http
GET https://graph.microsoft.com/beta/users/delta?$select=displayName,jobTitle,mobilePhone
```

#### <a name="response-2"></a><span data-ttu-id="c0a40-199">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="c0a40-199">Response 2</span></span>

<span data-ttu-id="c0a40-200">El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="c0a40-200">The following is an example of the response when using `deltaLink` obtained from the query initialization.</span></span> <span data-ttu-id="c0a40-201">Tenga en cuenta que todas las 3 propiedades se incluyen en la respuesta y no se sabe cuáles han cambiado desde la `deltaLink` se ha obtenido.</span><span class="sxs-lookup"><span data-stu-id="c0a40-201">Note that all 3 properties are included in the response and it is not known which ones have changed since the `deltaLink` was obtained.</span></span>

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
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#users",
  "@odata.nextLink":"https://graph.microsoft.com/beta/users/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjsXoYQp_dpA3cNJWc",
  "value": [
    {
      "displayName": "displayName-value",
      "jobTitle": "jobTitle-value",
      "mobilePhone": null
    }
  ]
}
```

#### <a name="request-3"></a><span data-ttu-id="c0a40-202">Solicitud 3</span><span class="sxs-lookup"><span data-stu-id="c0a40-202">Request 3</span></span>

<span data-ttu-id="c0a40-203">En el ejemplo siguiente se muestra la solicitud inicial seleccionando 3 propiedades para el seguimiento de cambios, con el comportamiento de respuesta mínimo alternativo:</span><span class="sxs-lookup"><span data-stu-id="c0a40-203">The next example shows the initial request selecting 3 properties for change tracking, with alternative minimal response behavior:</span></span>
<!-- {
  "blockType": "request",
  "name": "user_delta"
}-->

```http
GET https://graph.microsoft.com/beta/users/delta?$select=displayName,jobTitle,mobilePhone
Prefer: return=minimal
```

#### <a name="response-3"></a><span data-ttu-id="c0a40-204">Respuesta 3</span><span class="sxs-lookup"><span data-stu-id="c0a40-204">Response 3</span></span>

<span data-ttu-id="c0a40-205">El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="c0a40-205">The following is an example of the response when using `deltaLink` obtained from the query initialization.</span></span> <span data-ttu-id="c0a40-206">Tenga en cuenta que el `mobilePhone` (propiedad) no se incluye, lo que significa que no ha cambiado desde la última consulta delta; `displayName` y `jobTitle` se incluyen lo que significa que se han cambiado sus valores.</span><span class="sxs-lookup"><span data-stu-id="c0a40-206">Note that the `mobilePhone` property is not included, which means it has not changed since the last delta query; `displayName` and `jobTitle` are included which means their values have changed.</span></span>

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
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#users",
  "@odata.nextLink":"https://graph.microsoft.com/beta/users/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjsXoYQp_dpA3cNJWc",
  "value": [
    {
      "displayName": "displayName-value",
      "jobTitle": null
    }
  ]
}
```

- <span data-ttu-id="c0a40-207">[Consulta de delta de uso para realizar un seguimiento de los cambios en datos de Microsoft Graph](/graph/delta-query-overview).</span><span class="sxs-lookup"><span data-stu-id="c0a40-207">[Use delta query to track changes in Microsoft Graph data](/graph/delta-query-overview).</span></span>
- <span data-ttu-id="c0a40-208">[Obtener cambios incrementales para los usuarios](/graph/delta-query-users).</span><span class="sxs-lookup"><span data-stu-id="c0a40-208">[Get incremental changes for users](/graph/delta-query-users).</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
