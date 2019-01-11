---
title: 'directoryObject: delta'
description: 'Get recién creado, actualizar o eliminar objetos de Active directory de los siguientes tipos: usuario, grupo y contacto organizativa, en una consulta de delta único. Vea control de cambios para obtener información detallada.'
localization_priority: Normal
ms.openlocfilehash: 823107bce56d77c4e9c29a77405ac014443f5190
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27854498"
---
# <a name="directoryobject-delta"></a><span data-ttu-id="f1bf3-104">directoryObject: delta</span><span class="sxs-lookup"><span data-stu-id="f1bf3-104">directoryObject: delta</span></span>

> <span data-ttu-id="f1bf3-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f1bf3-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f1bf3-107">Get recién creado, actualizar o eliminar objetos de Active directory de los siguientes tipos: [usuario](../resources/user.md), [grupo](../resources/group.md) y [contacto organizativa](../resources/orgcontact.md), en una consulta de delta único.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-107">Get newly created, updated, or deleted directory objects of the following types: [user](../resources/user.md), [group](../resources/group.md) and [organizational contact](../resources/orgcontact.md), in a single delta query.</span></span> <span data-ttu-id="f1bf3-108">Para obtener información detallada, vea [control de cambios](/graph/delta-query-overview) .</span><span class="sxs-lookup"><span data-stu-id="f1bf3-108">See [Track changes](/graph/delta-query-overview) for details.</span></span>

## <a name="permissions"></a><span data-ttu-id="f1bf3-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="f1bf3-109">Permissions</span></span>

<span data-ttu-id="f1bf3-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f1bf3-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f1bf3-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f1bf3-112">Permission type</span></span>      | <span data-ttu-id="f1bf3-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f1bf3-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f1bf3-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f1bf3-114">Delegated (work or school account)</span></span> | <span data-ttu-id="f1bf3-115">Directory.Read.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="f1bf3-115">Directory.Read.All, Directory.AccessAsUser.All</span></span>  |
|<span data-ttu-id="f1bf3-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f1bf3-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f1bf3-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-117">Not supported.</span></span>  |
|<span data-ttu-id="f1bf3-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f1bf3-118">Application</span></span> | <span data-ttu-id="f1bf3-119">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f1bf3-119">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="f1bf3-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f1bf3-120">HTTP request</span></span>

<span data-ttu-id="f1bf3-121">Para comenzar el seguimiento de los cambios, realizar una solicitud que incluya la función delta en el recurso directoryObjects.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-121">To begin tracking changes, you make a request including the delta function on the directoryObjects resource.</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /directoryObjects/delta
```

## <a name="query-parameters"></a><span data-ttu-id="f1bf3-122">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="f1bf3-122">Query parameters</span></span>

<span data-ttu-id="f1bf3-123">Seguimiento de los cambios incurre una ronda de una o más llamadas de función de **delta** .</span><span class="sxs-lookup"><span data-stu-id="f1bf3-123">Tracking changes incurs a round of one or more **delta** function calls.</span></span> <span data-ttu-id="f1bf3-124">Si usa cualquier parámetro de consulta (distinto de `$deltatoken` y `$skiptoken`), debe especificar en la solicitud inicial del **delta** .</span><span class="sxs-lookup"><span data-stu-id="f1bf3-124">If you use any query parameter (other than `$deltatoken` and `$skiptoken`), you must specify it in the initial **delta** request.</span></span> <span data-ttu-id="f1bf3-125">Microsoft Graph codifica automáticamente los parámetros especificados en la parte de símbolo (token) de la `nextLink` o `deltaLink` dirección URL proporcionada en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-125">Microsoft Graph automatically encodes any specified parameters into the token portion of the `nextLink` or `deltaLink` URL provided in the response.</span></span>

<span data-ttu-id="f1bf3-126">Solo debe especificar una vez por adelantado los parámetros de consulta deseados.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-126">You only need to specify any desired query parameters once upfront.</span></span>

<span data-ttu-id="f1bf3-127">En solicitudes posteriores, copie y aplique la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-127">In subsequent requests, copy and apply the `nextLink` or `deltaLink` URL from the previous response, as that URL already includes the encoded, desired parameters.</span></span>

| <span data-ttu-id="f1bf3-128">Parámetro de consulta</span><span class="sxs-lookup"><span data-stu-id="f1bf3-128">Query parameter</span></span> | <span data-ttu-id="f1bf3-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="f1bf3-129">Type</span></span> |<span data-ttu-id="f1bf3-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="f1bf3-130">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="f1bf3-131">$deltatoken</span><span class="sxs-lookup"><span data-stu-id="f1bf3-131">$deltatoken</span></span> | <span data-ttu-id="f1bf3-132">string</span><span class="sxs-lookup"><span data-stu-id="f1bf3-132">string</span></span> | <span data-ttu-id="f1bf3-p106">Un [token de estado](/graph/delta-query-overview) que se devuelve en la dirección URL de `deltaLink` de la llamada de función **delta** anterior para la misma colección de usuarios. Indica el progreso de la ronda de seguimiento de cambios. Guarde y aplique toda la dirección URL `deltaLink`, incluido este token, en la primera solicitud de la siguiente ronda de seguimiento de cambios de la colección.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-p106">A [state token](/graph/delta-query-overview) returned in the `deltaLink` URL of the previous **delta** function call for the same user collection, indicating the completion of that round of change tracking. Save and apply the entire `deltaLink` URL including this token in the first request of the next round of change tracking for that collection.</span></span>|
| <span data-ttu-id="f1bf3-135">$skiptoken</span><span class="sxs-lookup"><span data-stu-id="f1bf3-135">$skiptoken</span></span> | <span data-ttu-id="f1bf3-136">string</span><span class="sxs-lookup"><span data-stu-id="f1bf3-136">string</span></span> | <span data-ttu-id="f1bf3-137">Un [token de estado](/graph/delta-query-overview) que se devuelve en la dirección URL de `nextLink` de la llamada de función **delta**. Indica que debe realizarse el seguimiento de más cambios en la misma colección de usuarios.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-137">A [state token](/graph/delta-query-overview) returned in the `nextLink` URL of the previous **delta** function call, indicating there are further changes to be tracked in the same user collection.</span></span> |

### <a name="odata-query-parameters"></a><span data-ttu-id="f1bf3-138">Parámetros de consulta de OData</span><span class="sxs-lookup"><span data-stu-id="f1bf3-138">OData query parameters</span></span>

<span data-ttu-id="f1bf3-139">Este método es compatible con parámetros opcionales de consulta de OData para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-139">This method supports optional OData Query Parameters to help customize the response.</span></span>

- <span data-ttu-id="f1bf3-140">Puede usar `$filter` con especial `isOf` operador que se debe filtrar un subconjunto de tipos derivados de directoryObject.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-140">You can use `$filter` with the special `isOf` operator to filter a subset of types derived from directoryObject.</span></span>
  - <span data-ttu-id="f1bf3-141">Puede combinar varias expresiones con una `or`, que le permite tener una consulta delta único varios tipos de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-141">You can combine multiple expressions using an `or`, which allows you to have a single delta query tracking multiple types.</span></span> <span data-ttu-id="f1bf3-142">Vea el [tercer ejemplo](#request-3) para obtener información detallada.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-142">See the [third example](#request-3) for details.</span></span>

## <a name="request-headers"></a><span data-ttu-id="f1bf3-143">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f1bf3-143">Request headers</span></span>

| <span data-ttu-id="f1bf3-144">Nombre</span><span class="sxs-lookup"><span data-stu-id="f1bf3-144">Name</span></span>       | <span data-ttu-id="f1bf3-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="f1bf3-145">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="f1bf3-146">Authorization</span><span class="sxs-lookup"><span data-stu-id="f1bf3-146">Authorization</span></span>  | <span data-ttu-id="f1bf3-147">&lt;token&gt; de portador</span><span class="sxs-lookup"><span data-stu-id="f1bf3-147">Bearer &lt;token&gt;</span></span>|
| <span data-ttu-id="f1bf3-148">Content-Type</span><span class="sxs-lookup"><span data-stu-id="f1bf3-148">Content-Type</span></span>  | <span data-ttu-id="f1bf3-149">application/json</span><span class="sxs-lookup"><span data-stu-id="f1bf3-149">application/json</span></span> |
| <span data-ttu-id="f1bf3-150">Prefer</span><span class="sxs-lookup"><span data-stu-id="f1bf3-150">Prefer</span></span> | <span data-ttu-id="f1bf3-151">devolver = mínimo</span><span class="sxs-lookup"><span data-stu-id="f1bf3-151">return=minimal</span></span> <br><br><span data-ttu-id="f1bf3-152">Si se especifica este encabezado con una solicitud que utiliza un `deltaLink` devolvería sólo las propiedades del objeto que han cambiado desde la última round.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-152">Specifying this header with a request that uses a `deltaLink` would return only the object properties that have changed since the last round.</span></span> <span data-ttu-id="f1bf3-153">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-153">Optional.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f1bf3-154">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f1bf3-154">Request body</span></span>

<span data-ttu-id="f1bf3-155">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-155">Do not supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="f1bf3-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f1bf3-156">Response</span></span>

<span data-ttu-id="f1bf3-157">Si tiene éxito, este método devuelve `200 OK` objeto de colección de respuesta código y [usuario](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-157">If successful, this method returns `200 OK` response code and [user](../resources/directoryobject.md) collection object in the response body.</span></span> <span data-ttu-id="f1bf3-158">La respuesta incluye también un `nextLink` dirección URL o un `deltaLink` dirección URL.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-158">The response also includes a `nextLink` URL or a `deltaLink` URL.</span></span>

- <span data-ttu-id="f1bf3-159">Si un `nextLink` se devuelve la dirección URL:</span><span class="sxs-lookup"><span data-stu-id="f1bf3-159">If a `nextLink` URL is returned:</span></span>
  - <span data-ttu-id="f1bf3-160">Esto indica que hay páginas adicionales de datos que se recuperarán en la sesión.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-160">This indicates there are additional pages of data to be retrieved in the session.</span></span> <span data-ttu-id="f1bf3-161">La aplicación continúa realizar solicitudes mediante el `nextLink` dirección URL hasta un `deltaLink` dirección URL se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-161">The application continues making requests using the `nextLink` URL until a `deltaLink` URL is included in the response.</span></span>
  - <span data-ttu-id="f1bf3-162">La respuesta incluye el mismo conjunto de propiedades como se muestra en la solicitud de consulta delta inicial.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-162">The response includes the same set of properties as in the initial delta query request.</span></span> <span data-ttu-id="f1bf3-163">Esto le permite capturar el estado actual y completa de los objetos al iniciar el ciclo de delta.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-163">This allows you to capture the full current state of the objects when initiating the delta cycle.</span></span>

- <span data-ttu-id="f1bf3-164">Si un `deltaLink` se devuelve la dirección URL:</span><span class="sxs-lookup"><span data-stu-id="f1bf3-164">If a `deltaLink` URL is returned:</span></span>
  - <span data-ttu-id="f1bf3-165">Esto indica que no hay ningún dato más sobre el estado existente del recurso que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-165">This indicates there is no more data about the existing state of the resource to be returned.</span></span> <span data-ttu-id="f1bf3-166">Guardar y utilizar el `deltaLink` dirección URL para obtener más información acerca de cambia para el recurso en la ronda siguiente.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-166">Save and use the `deltaLink` URL to learn about changes to the resource in the next round.</span></span>
  - <span data-ttu-id="f1bf3-167">Tiene una opción para especificar el `Prefer:return=minimal` encabezado, que se incluirá en los valores de respuesta sólo para las propiedades que han cambiado desde el momento en que el `deltaLink` se emitió.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-167">You have a choice to specify the `Prefer:return=minimal` header, to include in the response values for only the properties that have changed since the time the `deltaLink` was issued.</span></span>

#### <a name="default-return-the-same-properties-as-initial-delta-request"></a><span data-ttu-id="f1bf3-168">Valor predeterminado: devolver las mismas propiedades que la solicitud inicial del delta</span><span class="sxs-lookup"><span data-stu-id="f1bf3-168">Default: return the same properties as initial delta request</span></span>

<span data-ttu-id="f1bf3-169">De forma predeterminada, las solicitudes con un `deltaLink` o `nextLink` devolver las mismas propiedades como seleccionado en la consulta inicial del delta de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="f1bf3-169">By default, requests using a `deltaLink` or `nextLink` return the same properties as selected in the initial delta query in the following ways:</span></span>

- <span data-ttu-id="f1bf3-170">Si la propiedad ha cambiado, el nuevo valor se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-170">If the property has changed, the new value is included in the response.</span></span> <span data-ttu-id="f1bf3-171">Esto incluye las propiedades que se establezca en un valor null.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-171">This includes properties being set to null value.</span></span>
- <span data-ttu-id="f1bf3-172">Si no ha cambiado la propiedad, el valor anterior se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-172">If the property has not changed, the old value is included in the response.</span></span>
- <span data-ttu-id="f1bf3-173">Si nunca se ha establecido la propiedad antes de no se incluirá en la respuesta en absoluto.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-173">If the property has never been set before it will not be included in the response at all.</span></span>


> <span data-ttu-id="f1bf3-174">**Nota:** Con este comportamiento observando la respuesta no es posible saber si va a cambiar de una propiedad o no.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-174">**Note:** With this behavior, by looking at the response it is not possible to tell whether a property is changing or not.</span></span> <span data-ttu-id="f1bf3-175">Además, las respuestas de delta tienden a ser grandes porque contienen todos los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-175">Also, the delta responses tend to be large because they contain all property values.</span></span>

#### <a name="alternative-return-only-the-changed-properties"></a><span data-ttu-id="f1bf3-176">Alternativa: devolver sólo las propiedades modificadas</span><span class="sxs-lookup"><span data-stu-id="f1bf3-176">Alternative: return only the changed properties</span></span>

<span data-ttu-id="f1bf3-177">Adición de un encabezado de solicitud opcional - `prefer:return=minimal` -da como resultado el siguiente comportamiento:</span><span class="sxs-lookup"><span data-stu-id="f1bf3-177">Adding an optional request header - `prefer:return=minimal` - results in the following behavior:</span></span>

- <span data-ttu-id="f1bf3-178">Si la propiedad ha cambiado, el nuevo valor se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-178">If the property has changed, the new value is included in the response.</span></span> <span data-ttu-id="f1bf3-179">Esto incluye las propiedades que se establezca en un valor null.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-179">This includes properties being set to null value.</span></span>
- <span data-ttu-id="f1bf3-180">Si no ha cambiado la propiedad, la propiedad no se incluye en la respuesta en absoluto.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-180">If the property has not changed, the property is not included in the response at all.</span></span> <span data-ttu-id="f1bf3-181">(Distinto del comportamiento predeterminado).</span><span class="sxs-lookup"><span data-stu-id="f1bf3-181">(Different from the default behavior.)</span></span>

> <span data-ttu-id="f1bf3-182">**Nota:** El encabezado puede agregarse a un `deltaLink` solicitud en cualquier momento en el ciclo de delta.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-182">**Note:** The header can be added to a `deltaLink` request at any point in time in the delta cycle.</span></span> <span data-ttu-id="f1bf3-183">El encabezado sólo afecta el conjunto de propiedades que se incluyen en la respuesta y no afecta a cómo se ejecuta la consulta de delta.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-183">The header only affects the set of properties included in the response and it does not affect how the delta query is executed.</span></span>

## <a name="example"></a><span data-ttu-id="f1bf3-184">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f1bf3-184">Example</span></span>

### <a name="request-1"></a><span data-ttu-id="f1bf3-185">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="f1bf3-185">Request 1</span></span>

<span data-ttu-id="f1bf3-186">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-186">The following is an example of the request.</span></span> <span data-ttu-id="f1bf3-187">No hay ningún `$select` parámetro, por lo que se realiza un seguimiento y devuelve un conjunto predeterminado de propiedades.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-187">There is no `$select` parameter, so a default set of properties is tracked and returned.</span></span>
<!-- {
  "blockType": "request",
  "name": "user_delta"
}-->

```http
GET https://graph.microsoft.com/beta/directoryObjects/delta
```

### <a name="response-1"></a><span data-ttu-id="f1bf3-188">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="f1bf3-188">Response 1</span></span>

<span data-ttu-id="f1bf3-189">El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-189">The following is an example of the response when using `deltaLink` obtained from the query initialization.</span></span> <span data-ttu-id="f1bf3-190">No `isOf` utiliza filtro, por lo que se devuelven todos los tipos derivados de directoryObject.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-190">No `isOf` filter has been used, so all types derived from directoryObject are returned.</span></span>

><span data-ttu-id="f1bf3-p120">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-p120">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#directoryObjects",
  "@odata.nextLink":"https://graph.microsoft.com/beta/directoryObjects/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjsXoYQp_dpA3cNJWc",
  "value": [
    {
      "@odata.type": "#microsoft.graph.user",
      "id": "01754bb5-89de-4003-be72-9106a9fb16f2",
      "deletedDateTime": null,
      "accountEnabled": true,
      "ageGroup": null,
      "city": null,
      "companyName": null,
      "consentProvidedForMinor": null,
      "country": null,
      "createdDateTime": null,
      "department": null,
      "displayName": "John Smith",
      "givenName": null,
      "jobTitle": null,
      <...response trimmed for brevity...>
    },
    {
      "@odata.type": "#microsoft.graph.group",
      "id": "cf33844a-b6f8-4d4d-84f4-54e8d45094f0",
      "deletedDateTime": null,
      "classification": null,
      "createdDateTime": "2018-06-20T16:50:09Z",
      "description": null,
      "displayName": "testgp",
      <...response trimmed for brevity...>
    },
    {
      "@odata.type": "#microsoft.graph.orgContact",
      "id": "8f301319-4b4e-493f-8067-bce1dec76e7a",
      "businessPhones": ["string"],
      "city": "string",
      "companyName": "string",
      "country": "string",
      "department": "string",
      "displayName": "string",
      "givenName": "string",
      "id": "string (identifier)",
      "jobTitle": "string",
      <...response trimmed for brevity...>
    },
    <...response trimmed for brevity...>
  ]
}
```

### <a name="request-2"></a><span data-ttu-id="f1bf3-193">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="f1bf3-193">Request 2</span></span>

<span data-ttu-id="f1bf3-194">En el ejemplo siguiente se muestra el uso del comportamiento de respuesta mínimo alternativo:</span><span class="sxs-lookup"><span data-stu-id="f1bf3-194">The next example shows the use of the alternative minimal response behavior:</span></span>
<!-- {
  "blockType": "request",
  "name": "directoryObject_delta"
}-->

```http
GET https://graph.microsoft.com/beta/directoryObjects/delta
Prefer: return=minimal
```

### <a name="response-2"></a><span data-ttu-id="f1bf3-195">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="f1bf3-195">Response 2</span></span>

<span data-ttu-id="f1bf3-196">El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-196">The following is an example of the response when using `deltaLink` obtained from the query initialization.</span></span> <span data-ttu-id="f1bf3-197">Tenga en cuenta sólo las propiedades que han cambiado realmente se devuelven.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-197">Note only the properties that have actually changed are returned.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#directoryObjects",
  "@odata.nextLink":"https://graph.microsoft.com/beta/directoryObjects/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjsXoYQp_dpA3cNJWc",
  "value": [
    {
      "@odata.type": "#microsoft.graph.user",
      "id": "01754bb5-89de-4003-be72-9106a9fb16f2",
      "displayName": "John Smith"
    },
    {
      "@odata.type": "#microsoft.graph.group",
      "id": "cf33844a-b6f8-4d4d-84f4-54e8d45094f0",
      "description": null,
      "displayName": "testgp"
    },
    {
      "@odata.type": "#microsoft.graph.orgContact",
      "id": "8f301319-4b4e-493f-8067-bce1dec76e7a",
      "businessPhones": "12345"
    },
    <...response trimmed for brevity...>
  ]
}
```

### <a name="request-3"></a><span data-ttu-id="f1bf3-198">Solicitud 3</span><span class="sxs-lookup"><span data-stu-id="f1bf3-198">Request 3</span></span>

<span data-ttu-id="f1bf3-199">En el ejemplo siguiente se muestra el uso de la solicitud inicial la `isOf` operador para filtrar sólo las entidades de usuario y de grupo:</span><span class="sxs-lookup"><span data-stu-id="f1bf3-199">The next example shows the initial request using the `isOf` operator to filter out only user and group entities:</span></span>
<!-- {
  "blockType": "request",
  "name": "directoryobject_delta"
}-->

```http
GET https://graph.microsoft.com/beta/directoryObjects/delta?$filter=isOf('Microsoft.Graph.User')+or+isOf('Microsoft.Graph.Group')
```

### <a name="response-3"></a><span data-ttu-id="f1bf3-200">Respuesta 3</span><span class="sxs-lookup"><span data-stu-id="f1bf3-200">Response 3</span></span>

<span data-ttu-id="f1bf3-201">El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="f1bf3-201">The following is an example of the response when using `deltaLink` obtained from the query initialization.</span></span> <span data-ttu-id="f1bf3-202">Tenga en cuenta que se devuelven sólo los objetos de usuario y de grupo:</span><span class="sxs-lookup"><span data-stu-id="f1bf3-202">Note that only user and group objects are returned:</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#directoryObjects",
  "@odata.nextLink":"https://graph.microsoft.com/beta/directoryObjects/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjsXoYQp_dpA3cNJWc",
  "value": [
    {
      "@odata.type": "#microsoft.graph.user",
      "id": "01754bb5-89de-4003-be72-9106a9fb16f2",
      "deletedDateTime": null,
      "accountEnabled": true,
      "ageGroup": null,
      "city": null,
      "companyName": null,
      "consentProvidedForMinor": null,
      "country": null,
      "createdDateTime": null,
      "department": null,
      "displayName": "John Smith",
      "givenName": null,
      "jobTitle": null,
      <...response trimmed for brevity...>
    },
    {
      "@odata.type": "#microsoft.graph.group",
      "id": "cf33844a-b6f8-4d4d-84f4-54e8d45094f0",
      "deletedDateTime": null,
      "classification": null,
      "createdDateTime": "2018-06-20T16:50:09Z",
      "description": null,
      "displayName": "testgp",
      <...response trimmed for brevity...>
    },
    <...response trimmed for brevity...>
  ]
}
```

- <span data-ttu-id="f1bf3-203">[Consulta de delta de uso para realizar un seguimiento de los cambios en datos de Microsoft Graph](/graph/delta-query-overview).</span><span class="sxs-lookup"><span data-stu-id="f1bf3-203">[Use delta query to track changes in Microsoft Graph data](/graph/delta-query-overview).</span></span>
- <span data-ttu-id="f1bf3-204">[Obtener cambios incrementales para los usuarios](/graph/delta-query-users).</span><span class="sxs-lookup"><span data-stu-id="f1bf3-204">[Get incremental changes for users](/graph/delta-query-users).</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
