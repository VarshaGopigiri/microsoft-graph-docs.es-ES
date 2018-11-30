---
title: 'directoryRole: delta'
description: Get recién creado, actualiza o elimina roles de Active directory sin tener que realizar un acceso completo de lectura de la colección completa de recursos. Para obtener más información, vea Uso de consulta de Delta.
ms.openlocfilehash: 17a1f19252817ed31fab814b6150edeaedaa1143
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031180"
---
# <a name="directoryrole-delta"></a><span data-ttu-id="32f0b-104">directoryRole: delta</span><span class="sxs-lookup"><span data-stu-id="32f0b-104">directoryRole: delta</span></span>

<span data-ttu-id="32f0b-105">Get recién creado, actualiza o elimina roles de Active directory sin tener que realizar un acceso completo de lectura de la colección completa de recursos.</span><span class="sxs-lookup"><span data-stu-id="32f0b-105">Get newly created, updated, or deleted directory roles without having to perform a full read of the entire resource collection.</span></span> <span data-ttu-id="32f0b-106">Para obtener más información, vea [Uso de consulta de Delta](/graph/delta-query-overview) .</span><span class="sxs-lookup"><span data-stu-id="32f0b-106">See [Using Delta Query](/graph/delta-query-overview) for details.</span></span>

## <a name="permissions"></a><span data-ttu-id="32f0b-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="32f0b-107">Permissions</span></span>

<span data-ttu-id="32f0b-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="32f0b-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="32f0b-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="32f0b-110">Permission type</span></span>      | <span data-ttu-id="32f0b-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="32f0b-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="32f0b-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="32f0b-112">Delegated (work or school account)</span></span> | <span data-ttu-id="32f0b-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="32f0b-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="32f0b-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="32f0b-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="32f0b-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="32f0b-115">Not supported.</span></span>    |
|<span data-ttu-id="32f0b-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="32f0b-116">Application</span></span> | <span data-ttu-id="32f0b-117">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="32f0b-117">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="32f0b-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="32f0b-118">HTTP request</span></span>

<span data-ttu-id="32f0b-119">Para comenzar el seguimiento de los cambios, realizar una solicitud que incluya la función **delta** en el recurso [directoryRole](../resources/directoryrole.md) .</span><span class="sxs-lookup"><span data-stu-id="32f0b-119">To begin tracking changes, you make a request including the **delta** function on the [directoryRole](../resources/directoryrole.md) resource.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /directoryRoles/delta
```

## <a name="query-parameters"></a><span data-ttu-id="32f0b-120">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="32f0b-120">Query parameters</span></span>

<span data-ttu-id="32f0b-121">Seguimiento de los cambios incurre una ronda de una o más llamadas de función de **delta** .</span><span class="sxs-lookup"><span data-stu-id="32f0b-121">Tracking changes incurs a round of one or more **delta** function calls.</span></span> <span data-ttu-id="32f0b-122">Si usa cualquier parámetro de consulta (distinto de `$deltatoken` y `$skiptoken`), debe especificar en la solicitud inicial del **delta** .</span><span class="sxs-lookup"><span data-stu-id="32f0b-122">If you use any query parameter (other than `$deltatoken` and `$skiptoken`), you must specify it in the initial **delta** request.</span></span> <span data-ttu-id="32f0b-123">Microsoft Graph codifica automáticamente los parámetros especificados en la parte de símbolo (token) de la `nextLink` o `deltaLink` dirección URL proporcionada en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="32f0b-123">Microsoft Graph automatically encodes any specified parameters into the token portion of the `nextLink` or `deltaLink` URL provided in the response.</span></span> <span data-ttu-id="32f0b-124">Solo debe especificar una vez por adelantado los parámetros de consulta deseados.</span><span class="sxs-lookup"><span data-stu-id="32f0b-124">You only need to specify any desired query parameters once upfront.</span></span> <span data-ttu-id="32f0b-125">En solicitudes posteriores, copie y aplique la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.</span><span class="sxs-lookup"><span data-stu-id="32f0b-125">In subsequent requests, copy and apply the `nextLink` or `deltaLink` URL from the previous response, as that URL already includes the encoded, desired parameters.</span></span>

| <span data-ttu-id="32f0b-126">Parámetro de consulta</span><span class="sxs-lookup"><span data-stu-id="32f0b-126">Query parameter</span></span>      | <span data-ttu-id="32f0b-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="32f0b-127">Type</span></span>   |<span data-ttu-id="32f0b-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="32f0b-128">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="32f0b-129">$deltatoken</span><span class="sxs-lookup"><span data-stu-id="32f0b-129">$deltatoken</span></span> | <span data-ttu-id="32f0b-130">string</span><span class="sxs-lookup"><span data-stu-id="32f0b-130">string</span></span> | <span data-ttu-id="32f0b-131">Un [símbolo (token) de estado](/graph/delta-query-overview) devuelto en el `deltaLink` dirección URL de la llamada de función **delta** anterior para la misma colección de recursos, que indica la finalización de ese round de seguimiento de cambios.</span><span class="sxs-lookup"><span data-stu-id="32f0b-131">A [state token](/graph/delta-query-overview) returned in the `deltaLink` URL of the previous **delta** function call for the same resource collection, indicating the completion of that round of change tracking.</span></span> <span data-ttu-id="32f0b-132">Guardar y aplicar todo el `deltaLink` dirección URL incluido este token en la primera solicitud de la siguiente ronda de seguimiento de cambios para esa colección.</span><span class="sxs-lookup"><span data-stu-id="32f0b-132">Save and apply the entire `deltaLink` URL including this token in the first request of the next round of change tracking for that collection.</span></span>|
| <span data-ttu-id="32f0b-133">$skiptoken</span><span class="sxs-lookup"><span data-stu-id="32f0b-133">$skiptoken</span></span> | <span data-ttu-id="32f0b-134">string</span><span class="sxs-lookup"><span data-stu-id="32f0b-134">string</span></span> | <span data-ttu-id="32f0b-135">Un [símbolo (token) de estado](/graph/delta-query-overview) devuelto en el `nextLink` dirección URL de la llamada de función **delta** anterior, que indica que hay más cambios para realizar un seguimiento en la misma colección de recursos.</span><span class="sxs-lookup"><span data-stu-id="32f0b-135">A [state token](/graph/delta-query-overview) returned in the `nextLink` URL of the previous **delta** function call, indicating there are further changes to be tracked in the same resource collection.</span></span> |

### <a name="odata-query-parameters"></a><span data-ttu-id="32f0b-136">Parámetros de consulta de OData</span><span class="sxs-lookup"><span data-stu-id="32f0b-136">OData query parameters</span></span>

<span data-ttu-id="32f0b-137">Este método es compatible con los parámetros de consulta de OData para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="32f0b-137">This method supports OData query parameters to help customize the response.</span></span>

- <span data-ttu-id="32f0b-p106">Puede utilizar un parámetro de consulta `$select` como en cualquier solicitud GET para especificar solo las propiedades que necesita para un mejor rendimiento. Siempre se devuelve la propiedad _id_.</span><span class="sxs-lookup"><span data-stu-id="32f0b-p106">You can use a `$select` query parameter as in any GET request to specify only the properties your need for best performance. The _id_ property is always returned.</span></span>

- <span data-ttu-id="32f0b-140">No hay compatibilidad limitada para `$filter`:</span><span class="sxs-lookup"><span data-stu-id="32f0b-140">There is limited support for `$filter`:</span></span>

  - <span data-ttu-id="32f0b-141">El único admitido `$filter` expresión es para realizar un seguimiento de cambios para recursos específicos, por su identificador: `$filter=id+eq+{value}` o `$filter=id+eq+{value1}+or+id+eq+{value2}`.</span><span class="sxs-lookup"><span data-stu-id="32f0b-141">The only supported `$filter` expression is for tracking changes for specific resources, by their id:  `$filter=id+eq+{value}` or `$filter=id+eq+{value1}+or+id+eq+{value2}`.</span></span> <span data-ttu-id="32f0b-142">El número de identificadores que puede especificar está limitado por la longitud máxima de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="32f0b-142">The number of ids you can specify is limited by the maximum URL length.</span></span>

## <a name="request-headers"></a><span data-ttu-id="32f0b-143">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="32f0b-143">Request headers</span></span>

| <span data-ttu-id="32f0b-144">Nombre</span><span class="sxs-lookup"><span data-stu-id="32f0b-144">Name</span></span>       | <span data-ttu-id="32f0b-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="32f0b-145">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="32f0b-146">Authorization</span><span class="sxs-lookup"><span data-stu-id="32f0b-146">Authorization</span></span>  | <span data-ttu-id="32f0b-147">&lt;token&gt; de portador</span><span class="sxs-lookup"><span data-stu-id="32f0b-147">Bearer &lt;token&gt;</span></span>|
| <span data-ttu-id="32f0b-148">Content-Type</span><span class="sxs-lookup"><span data-stu-id="32f0b-148">Content-Type</span></span>  | <span data-ttu-id="32f0b-149">application/json</span><span class="sxs-lookup"><span data-stu-id="32f0b-149">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="32f0b-150">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="32f0b-150">Request body</span></span>

<span data-ttu-id="32f0b-151">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="32f0b-151">Do not supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="32f0b-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="32f0b-152">Response</span></span>

<span data-ttu-id="32f0b-153">Si tiene éxito, este método devuelve `200 OK` objeto de colección de respuesta código y [directoryRole](../resources/directoryrole.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="32f0b-153">If successful, this method returns `200 OK` response code and [directoryRole](../resources/directoryrole.md) collection object in the response body.</span></span> <span data-ttu-id="32f0b-154">La respuesta incluye también un `nextLink` dirección URL o un `deltaLink` dirección URL.</span><span class="sxs-lookup"><span data-stu-id="32f0b-154">The response also includes a `nextLink` URL or a `deltaLink` URL.</span></span>

- <span data-ttu-id="32f0b-155">Si un `nextLink` se devuelve la dirección URL, hay páginas adicionales de datos que se recuperarán en la sesión.</span><span class="sxs-lookup"><span data-stu-id="32f0b-155">If a `nextLink` URL is returned, there are additional pages of data to be retrieved in the session.</span></span> <span data-ttu-id="32f0b-156">La aplicación continúa realizar solicitudes mediante el `nextLink` dirección URL hasta un `deltaLink` dirección URL se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="32f0b-156">The application continues making requests using the `nextLink` URL until a `deltaLink` URL is included in the response.</span></span>

- <span data-ttu-id="32f0b-157">Si un `deltaLink` se devuelve la dirección URL, no hay ningún dato más sobre el estado existente del recurso que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="32f0b-157">If a `deltaLink` URL is returned, there is no more data about the existing state of the resource to be returned.</span></span> <span data-ttu-id="32f0b-158">Guardar `deltaLink` dirección URL y aplicar en la siguiente llamada **delta** para obtener más información acerca de los cambios realizados en el recurso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="32f0b-158">Save `deltaLink` URL and apply it in the next **delta** call to learn about changes to the resource in the future.</span></span>

### <a name="example"></a><span data-ttu-id="32f0b-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="32f0b-159">Example</span></span>

##### <a name="request"></a><span data-ttu-id="32f0b-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="32f0b-160">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "directoryRole_delta"
}-->

```http
GET https://graph.microsoft.com/v1.0/directoryRoles/delta
```

##### <a name="response"></a><span data-ttu-id="32f0b-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="32f0b-161">Response</span></span>

<span data-ttu-id="32f0b-p111">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="32f0b-p111">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

### <a name="see-also"></a><span data-ttu-id="32f0b-164">Consulte también</span><span class="sxs-lookup"><span data-stu-id="32f0b-164">See also</span></span>

- <span data-ttu-id="32f0b-165">[Consulta de delta de uso para realizar un seguimiento de los cambios en datos de Microsoft Graph](/graph/delta-query-overview) para obtener más detalles</span><span class="sxs-lookup"><span data-stu-id="32f0b-165">[Use delta query to track changes in Microsoft Graph data](/graph/delta-query-overview) for more details</span></span>
- <span data-ttu-id="32f0b-166">[Obtener los cambios incrementales de usuarios](/graph/delta-query-users) para obtener un ejemplo de solicitud.</span><span class="sxs-lookup"><span data-stu-id="32f0b-166">[Get incremental changes for users](/graph/delta-query-users) for an example requests.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryRole: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->