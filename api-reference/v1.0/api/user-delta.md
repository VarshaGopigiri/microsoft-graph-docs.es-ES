---
title: 'user: delta'
description: Get recién creado, actualiza o elimina los usuarios sin tener que realizar un acceso completo de lectura de la colección completa de usuario. Vea control de cambios para obtener información detallada.
localization_priority: Priority
author: dkershaw10
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 6464e8ad975a5fc996c671df5a01df2988dbf79d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27945618"
---
# <a name="user-delta"></a><span data-ttu-id="4d9a1-104">user: delta</span><span class="sxs-lookup"><span data-stu-id="4d9a1-104">user: delta</span></span>

<span data-ttu-id="4d9a1-105">Get recién creado, actualiza o elimina los usuarios sin tener que realizar un acceso completo de lectura de la colección completa de usuario.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-105">Get newly created, updated, or deleted users without having to perform a full read of the entire user collection.</span></span> <span data-ttu-id="4d9a1-106">Para obtener información detallada, vea [control de cambios](/graph/delta-query-overview) .</span><span class="sxs-lookup"><span data-stu-id="4d9a1-106">See [Track changes](/graph/delta-query-overview) for details.</span></span>

## <a name="permissions"></a><span data-ttu-id="4d9a1-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="4d9a1-107">Permissions</span></span>

<span data-ttu-id="4d9a1-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4d9a1-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="4d9a1-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4d9a1-110">Permission type</span></span>      | <span data-ttu-id="4d9a1-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4d9a1-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4d9a1-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4d9a1-112">Delegated (work or school account)</span></span> | <span data-ttu-id="4d9a1-113">User.Read, User.ReadWrite, User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="4d9a1-113">User.Read, User.ReadWrite, User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="4d9a1-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4d9a1-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4d9a1-115">User.Read, User.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4d9a1-115">User.Read, User.ReadWrite</span></span>    |
|<span data-ttu-id="4d9a1-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4d9a1-116">Application</span></span> | <span data-ttu-id="4d9a1-117">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4d9a1-117">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="4d9a1-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4d9a1-118">HTTP request</span></span>

<span data-ttu-id="4d9a1-119">Para comenzar los cambios, debe realizar una solicitud incluyendo la función delta en el recurso de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-119">To begin tracking changes, you make a request including the delta function on the users resource.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /users/delta
```

## <a name="query-parameters"></a><span data-ttu-id="4d9a1-120">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="4d9a1-120">Query parameters</span></span>

<span data-ttu-id="4d9a1-121">Seguimiento de los cambios en los usuarios incurre en una ronda de una o más llamadas de función de **delta** .</span><span class="sxs-lookup"><span data-stu-id="4d9a1-121">Tracking changes in users incurs a round of one or more **delta** function calls.</span></span> <span data-ttu-id="4d9a1-122">Si usa cualquier parámetro de consulta (distinto de `$deltatoken` y `$skiptoken`), debe especificar en la solicitud inicial del **delta** .</span><span class="sxs-lookup"><span data-stu-id="4d9a1-122">If you use any query parameter (other than `$deltatoken` and `$skiptoken`), you must specify it in the initial **delta** request.</span></span> <span data-ttu-id="4d9a1-123">Microsoft Graph codifica automáticamente los parámetros especificados en la parte de símbolo (token) de la `nextLink` o `deltaLink` dirección URL proporcionada en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-123">Microsoft Graph automatically encodes any specified parameters into the token portion of the `nextLink` or `deltaLink` URL provided in the response.</span></span>

<span data-ttu-id="4d9a1-124">Solo debe especificar una vez por adelantado los parámetros de consulta deseados.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-124">You only need to specify any desired query parameters once upfront.</span></span>

<span data-ttu-id="4d9a1-125">En solicitudes posteriores, copie y aplique la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-125">In subsequent requests, copy and apply the `nextLink` or `deltaLink` URL from the previous response, as that URL already includes the encoded, desired parameters.</span></span>

| <span data-ttu-id="4d9a1-126">Parámetro de consulta</span><span class="sxs-lookup"><span data-stu-id="4d9a1-126">Query parameter</span></span>      | <span data-ttu-id="4d9a1-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="4d9a1-127">Type</span></span>   |<span data-ttu-id="4d9a1-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d9a1-128">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="4d9a1-129">$deltatoken</span><span class="sxs-lookup"><span data-stu-id="4d9a1-129">$deltatoken</span></span> | <span data-ttu-id="4d9a1-130">string</span><span class="sxs-lookup"><span data-stu-id="4d9a1-130">string</span></span> | <span data-ttu-id="4d9a1-p105">Un [token de estado](/graph/delta-query-overview) que se devuelve en la dirección URL de `deltaLink` de la llamada de función **delta** anterior para la misma colección de usuarios. Indica el progreso de la ronda de seguimiento de cambios. Guarde y aplique toda la dirección URL `deltaLink`, incluido este token, en la primera solicitud de la siguiente ronda de seguimiento de cambios de la colección.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-p105">A [state token](/graph/delta-query-overview) returned in the `deltaLink` URL of the previous **delta** function call for the same user collection, indicating the completion of that round of change tracking. Save and apply the entire `deltaLink` URL including this token in the first request of the next round of change tracking for that collection.</span></span>|
| <span data-ttu-id="4d9a1-133">$skiptoken</span><span class="sxs-lookup"><span data-stu-id="4d9a1-133">$skiptoken</span></span> | <span data-ttu-id="4d9a1-134">string</span><span class="sxs-lookup"><span data-stu-id="4d9a1-134">string</span></span> | <span data-ttu-id="4d9a1-135">Un [token de estado](/graph/delta-query-overview) que se devuelve en la dirección URL de `nextLink` de la llamada de función **delta**. Indica que debe realizarse el seguimiento de más cambios en la misma colección de usuarios.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-135">A [state token](/graph/delta-query-overview) returned in the `nextLink` URL of the previous **delta** function call, indicating there are further changes to be tracked in the same user collection.</span></span> |

### <a name="odata-query-parameters"></a><span data-ttu-id="4d9a1-136">Parámetros de consulta de OData</span><span class="sxs-lookup"><span data-stu-id="4d9a1-136">OData query parameters</span></span>

<span data-ttu-id="4d9a1-137">Este método es compatible con parámetros opcionales de consulta de OData para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-137">This method supports optional OData Query Parameters to help customize the response.</span></span>

- <span data-ttu-id="4d9a1-p106">Puede utilizar un parámetro de consulta `$select` como en cualquier solicitud GET para especificar solo las propiedades que necesita para un mejor rendimiento. Siempre se devuelve la propiedad *id*.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-p106">You can use a `$select` query parameter as in any GET request to specify only the properties your need for best performance. The *id* property is always returned.</span></span>
- <span data-ttu-id="4d9a1-140">No hay compatibilidad limitada para `$filter`:</span><span class="sxs-lookup"><span data-stu-id="4d9a1-140">There is limited support for `$filter`:</span></span>
  - <span data-ttu-id="4d9a1-141">La única expresión `$filter` admitida es para realizar un seguimiento de los cambios en un objeto específico: `$filter=id+eq+{value}`.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-141">The only supported `$filter` expression is for tracking changes on a specific object: `$filter=id+eq+{value}`.</span></span> <span data-ttu-id="4d9a1-142">Puede filtrar varios objetos.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-142">You can filter multiple objects.</span></span> <span data-ttu-id="4d9a1-143">Por ejemplo, `https://graph.microsoft.com/v1.0/users/delta/?$filter= id eq '477e9fc6-5de7-4406-bb2a-7e5c83c9ffff' or id eq '004d6a07-fe70-4b92-add5-e6e37b8affff'`.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-143">For example, `https://graph.microsoft.com/v1.0/users/delta/?$filter= id eq '477e9fc6-5de7-4406-bb2a-7e5c83c9ffff' or id eq '004d6a07-fe70-4b92-add5-e6e37b8affff'`.</span></span> <span data-ttu-id="4d9a1-144">Hay un límite de 50 objetos filtrados.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-144">There is a limit of 50 filtered objects.</span></span>

## <a name="request-headers"></a><span data-ttu-id="4d9a1-145">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4d9a1-145">Request headers</span></span>
| <span data-ttu-id="4d9a1-146">Nombre</span><span class="sxs-lookup"><span data-stu-id="4d9a1-146">Name</span></span>       | <span data-ttu-id="4d9a1-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d9a1-147">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="4d9a1-148">Authorization</span><span class="sxs-lookup"><span data-stu-id="4d9a1-148">Authorization</span></span>  | <span data-ttu-id="4d9a1-149">&lt;token&gt; de portador</span><span class="sxs-lookup"><span data-stu-id="4d9a1-149">Bearer &lt;token&gt;</span></span>|
| <span data-ttu-id="4d9a1-150">Content-Type</span><span class="sxs-lookup"><span data-stu-id="4d9a1-150">Content-Type</span></span>  | <span data-ttu-id="4d9a1-151">application/json</span><span class="sxs-lookup"><span data-stu-id="4d9a1-151">application/json</span></span> |
| <span data-ttu-id="4d9a1-152">Prefer</span><span class="sxs-lookup"><span data-stu-id="4d9a1-152">Prefer</span></span> | <span data-ttu-id="4d9a1-153">devolver = mínimo</span><span class="sxs-lookup"><span data-stu-id="4d9a1-153">return=minimal</span></span> <br><br><span data-ttu-id="4d9a1-154">Si se especifica este encabezado con una solicitud que utiliza un `deltaLink` devolvería sólo las propiedades del objeto que han cambiado desde la última round.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-154">Specifying this header with a request that uses a `deltaLink` would return only the object properties that have changed since the last round.</span></span> <span data-ttu-id="4d9a1-155">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-155">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4d9a1-156">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4d9a1-156">Request body</span></span>
<span data-ttu-id="4d9a1-157">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-157">Do not supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="4d9a1-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4d9a1-158">Response</span></span>

<span data-ttu-id="4d9a1-159">Si tiene éxito, este método devuelve `200 OK` objeto de colección de respuesta código y [usuario](../resources/user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-159">If successful, this method returns `200 OK` response code and [user](../resources/user.md) collection object in the response body.</span></span> <span data-ttu-id="4d9a1-160">La respuesta incluye también un `nextLink` dirección URL o un `deltaLink` dirección URL.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-160">The response also includes a `nextLink` URL or a `deltaLink` URL.</span></span>

- <span data-ttu-id="4d9a1-161">Si un `nextLink` se devuelve la dirección URL:</span><span class="sxs-lookup"><span data-stu-id="4d9a1-161">If a `nextLink` URL is returned:</span></span>
  - <span data-ttu-id="4d9a1-162">Esto indica que hay páginas adicionales de datos que se recuperarán en la sesión.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-162">This indicates there are additional pages of data to be retrieved in the session.</span></span> <span data-ttu-id="4d9a1-163">La aplicación continúa realizar solicitudes mediante el `nextLink` dirección URL hasta un `deltaLink` dirección URL se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-163">The application continues making requests using the `nextLink` URL until a `deltaLink` URL is included in the response.</span></span>
  - <span data-ttu-id="4d9a1-164">La respuesta incluye el mismo conjunto de propiedades como se muestra en la solicitud de consulta delta inicial.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-164">The response includes the same set of properties as in the initial delta query request.</span></span> <span data-ttu-id="4d9a1-165">Esto le permite capturar el estado actual y completa de los objetos al iniciar el ciclo de delta.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-165">This allows you to capture the full current state of the objects when initiating the delta cycle.</span></span>

- <span data-ttu-id="4d9a1-166">Si un `deltaLink` se devuelve la dirección URL:</span><span class="sxs-lookup"><span data-stu-id="4d9a1-166">If a `deltaLink` URL is returned:</span></span>
  - <span data-ttu-id="4d9a1-167">Esto indica que no hay ningún dato más sobre el estado existente del recurso que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-167">This indicates there is no more data about the existing state of the resource to be returned.</span></span> <span data-ttu-id="4d9a1-168">Guardar y utilizar el `deltaLink` dirección URL para obtener más información acerca de cambia para el recurso en la ronda siguiente.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-168">Save and use the `deltaLink` URL to learn about changes to the resource in the next round.</span></span>
  - <span data-ttu-id="4d9a1-169">Tiene una opción para especificar el `Prefer:return=minimal` encabezado, que se incluirá en los valores de respuesta sólo para las propiedades que han cambiado desde el momento en que el `deltaLink` se emitió.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-169">You have a choice to specify the `Prefer:return=minimal` header, to include in the response values for only the properties that have changed since the time the `deltaLink` was issued.</span></span>

#### <a name="default-return-the-same-properties-as-initial-delta-request"></a><span data-ttu-id="4d9a1-170">Valor predeterminado: devolver las mismas propiedades que la solicitud inicial del delta</span><span class="sxs-lookup"><span data-stu-id="4d9a1-170">Default: return the same properties as initial delta request</span></span>

<span data-ttu-id="4d9a1-171">De forma predeterminada, las solicitudes con un `deltaLink` o `nextLink` devolver las mismas propiedades como seleccionado en la consulta inicial del delta de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="4d9a1-171">By default, requests using a `deltaLink` or `nextLink` return the same properties as selected in the initial delta query in the following ways:</span></span>

- <span data-ttu-id="4d9a1-172">Si la propiedad ha cambiado, el nuevo valor se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-172">If the property has changed, the new value is included in the response.</span></span> <span data-ttu-id="4d9a1-173">Esto incluye las propiedades que se establezca en un valor null.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-173">This includes properties being set to null value.</span></span>
- <span data-ttu-id="4d9a1-174">Si no ha cambiado la propiedad, el valor anterior se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-174">If the property has not changed, the old value is included in the response.</span></span>
- <span data-ttu-id="4d9a1-175">Si nunca se ha establecido la propiedad antes de no se incluirá en la respuesta en absoluto.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-175">If the property has never been set before it will not be included in the response at all.</span></span>


> <span data-ttu-id="4d9a1-176">**Nota:** Con este comportamiento observando la respuesta no es posible saber si va a cambiar de una propiedad o no.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-176">**Note:** With this behavior, by looking at the response it is not possible to tell whether a property is changing or not.</span></span> <span data-ttu-id="4d9a1-177">Además, las respuestas de delta tienden a ser grandes porque contienen todos los valores de propiedad - tal como se muestra en el [segundo ejemplo](#request-2) siguiente.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-177">Also, the delta responses tend to be large because they contain all property values  - as shown in the [second example](#request-2) below.</span></span>

#### <a name="alternative-return-only-the-changed-properties"></a><span data-ttu-id="4d9a1-178">Alternativa: devolver sólo las propiedades modificadas</span><span class="sxs-lookup"><span data-stu-id="4d9a1-178">Alternative: return only the changed properties</span></span>

<span data-ttu-id="4d9a1-179">Adición de un encabezado de solicitud opcional - `prefer:return=minimal` -da como resultado el siguiente comportamiento:</span><span class="sxs-lookup"><span data-stu-id="4d9a1-179">Adding an optional request header - `prefer:return=minimal` - results in the following behavior:</span></span>

- <span data-ttu-id="4d9a1-180">Si la propiedad ha cambiado, el nuevo valor se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-180">If the property has changed, the new value is included in the response.</span></span> <span data-ttu-id="4d9a1-181">Esto incluye las propiedades que se establezca en un valor null.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-181">This includes properties being set to null value.</span></span>
- <span data-ttu-id="4d9a1-182">Si no ha cambiado la propiedad, la propiedad no se incluye en la respuesta en absoluto.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-182">If the property has not changed, the property is not included in the response at all.</span></span> <span data-ttu-id="4d9a1-183">(Distinto del comportamiento predeterminado).</span><span class="sxs-lookup"><span data-stu-id="4d9a1-183">(Different from the default behavior.)</span></span>

> <span data-ttu-id="4d9a1-184">**Nota:** El encabezado puede agregarse a un `deltaLink` solicitud en cualquier momento en el ciclo de delta.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-184">**Note:** The header can be added to a `deltaLink` request at any point in time in the delta cycle.</span></span> <span data-ttu-id="4d9a1-185">El encabezado sólo afecta el conjunto de propiedades que se incluyen en la respuesta y no afecta a cómo se ejecuta la consulta de delta.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-185">The header only affects the set of properties included in the response and it does not affect how the delta query is executed.</span></span> <span data-ttu-id="4d9a1-186">Vea el [tercer ejemplo](#request-3) siguiente.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-186">See the [third example](#request-3) below.</span></span>

### <a name="example"></a><span data-ttu-id="4d9a1-187">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4d9a1-187">Example</span></span>

#### <a name="request-1"></a><span data-ttu-id="4d9a1-188">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="4d9a1-188">Request 1</span></span>

<span data-ttu-id="4d9a1-189">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-189">The following is an example of the request.</span></span> <span data-ttu-id="4d9a1-190">No hay ningún `$select` parámetro, por lo que se realiza un seguimiento y devuelve un conjunto predeterminado de propiedades.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-190">There is no `$select` parameter, so a default set of properties is tracked and returned.</span></span>
<!-- {
  "blockType": "request",
  "name": "user_delta"
}-->

```http
GET https://graph.microsoft.com/v1.0/users/delta
```

#### <a name="response-1"></a><span data-ttu-id="4d9a1-191">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="4d9a1-191">Response 1</span></span>

<span data-ttu-id="4d9a1-192">El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-192">The following is an example of the response when using `deltaLink` obtained from the query initialization.</span></span>

><span data-ttu-id="4d9a1-p119">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-p119">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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

#### <a name="request-2"></a><span data-ttu-id="4d9a1-195">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="4d9a1-195">Request 2</span></span>

<span data-ttu-id="4d9a1-196">En el ejemplo siguiente se muestra la solicitud inicial seleccionando 3 propiedades para el seguimiento de cambios, con comportamiento de respuesta predeterminado:</span><span class="sxs-lookup"><span data-stu-id="4d9a1-196">The next example shows the initial request selecting 3 properties for change tracking, with default response behavior:</span></span>
<!-- {
  "blockType": "request",
  "name": "user_delta"
}-->

```http
GET https://graph.microsoft.com/v1.0/users/delta?$select=displayName,jobTitle,mobilePhone
```

#### <a name="response-2"></a><span data-ttu-id="4d9a1-197">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="4d9a1-197">Response 2</span></span>

<span data-ttu-id="4d9a1-198">El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-198">The following is an example of the response when using `deltaLink` obtained from the query initialization.</span></span> <span data-ttu-id="4d9a1-199">Tenga en cuenta que todas las 3 propiedades se incluyen en la respuesta y no se sabe cuáles han cambiado desde la `deltaLink` se ha obtenido.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-199">Note that all 3 properties are included in the response and it is not known which ones have changed since the `deltaLink` was obtained.</span></span>

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
      "jobTitle": "jobTitle-value",
      "mobilePhone": null
    }
  ]
}
```

#### <a name="request-3"></a><span data-ttu-id="4d9a1-200">Solicitud 3</span><span class="sxs-lookup"><span data-stu-id="4d9a1-200">Request 3</span></span>

<span data-ttu-id="4d9a1-201">En el ejemplo siguiente se muestra la solicitud inicial seleccionando 3 propiedades para el seguimiento de cambios, con el comportamiento de respuesta mínimo alternativo:</span><span class="sxs-lookup"><span data-stu-id="4d9a1-201">The next example shows the initial request selecting 3 properties for change tracking, with alternative minimal response behavior:</span></span>
<!-- {
  "blockType": "request",
  "name": "user_delta"
}-->

```http
GET https://graph.microsoft.com/v1.0/users/delta?$select=displayName,jobTitle,mobilePhone
Prefer: return=minimal
```

#### <a name="response-3"></a><span data-ttu-id="4d9a1-202">Respuesta 3</span><span class="sxs-lookup"><span data-stu-id="4d9a1-202">Response 3</span></span>

<span data-ttu-id="4d9a1-203">El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-203">The following is an example of the response when using `deltaLink` obtained from the query initialization.</span></span> <span data-ttu-id="4d9a1-204">Tenga en cuenta que el `mobilePhone` (propiedad) no se incluye, lo que significa que no ha cambiado desde la última consulta delta; `displayName` y `jobTitle` se incluyen lo que significa que se han cambiado sus valores.</span><span class="sxs-lookup"><span data-stu-id="4d9a1-204">Note that the `mobilePhone` property is not included, which means it has not changed since the last delta query; `displayName` and `jobTitle` are included which means their values have changed.</span></span>

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

- <span data-ttu-id="4d9a1-205">[Consulta de delta de uso para realizar un seguimiento de los cambios en datos de Microsoft Graph](/graph/delta-query-overview).</span><span class="sxs-lookup"><span data-stu-id="4d9a1-205">[Use delta query to track changes in Microsoft Graph data](/graph/delta-query-overview).</span></span>
- <span data-ttu-id="4d9a1-206">[Obtener cambios incrementales para los usuarios](/graph/delta-query-users).</span><span class="sxs-lookup"><span data-stu-id="4d9a1-206">[Get incremental changes for users](/graph/delta-query-users).</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
