---
title: 'directoryRole: delta'
description: Get recién creado, actualiza o elimina roles de Active directory sin tener que realizar un acceso completo de lectura de la colección completa de recursos. Para obtener más información, vea Uso de consulta de Delta.
localization_priority: Normal
ms.openlocfilehash: 9eb847f390b4f05f56945a6496325bbeaccdf410
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27809124"
---
# <a name="directoryrole-delta"></a><span data-ttu-id="68e3f-104">directoryRole: delta</span><span class="sxs-lookup"><span data-stu-id="68e3f-104">directoryRole: delta</span></span>

> <span data-ttu-id="68e3f-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="68e3f-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="68e3f-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="68e3f-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="68e3f-107">Get recién creado, actualiza o elimina roles de Active directory sin tener que realizar un acceso completo de lectura de la colección completa de recursos.</span><span class="sxs-lookup"><span data-stu-id="68e3f-107">Get newly created, updated, or deleted directory roles without having to perform a full read of the entire resource collection.</span></span> <span data-ttu-id="68e3f-108">Para obtener más información, vea [Uso de consulta de Delta](/graph/delta-query-overview) .</span><span class="sxs-lookup"><span data-stu-id="68e3f-108">See [Using Delta Query](/graph/delta-query-overview) for details.</span></span>

## <a name="permissions"></a><span data-ttu-id="68e3f-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="68e3f-109">Permissions</span></span>

<span data-ttu-id="68e3f-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="68e3f-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="68e3f-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="68e3f-112">Permission type</span></span>      | <span data-ttu-id="68e3f-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="68e3f-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="68e3f-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="68e3f-114">Delegated (work or school account)</span></span> | <span data-ttu-id="68e3f-115">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="68e3f-115">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="68e3f-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="68e3f-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="68e3f-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="68e3f-117">Not supported.</span></span>    |
|<span data-ttu-id="68e3f-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="68e3f-118">Application</span></span> | <span data-ttu-id="68e3f-119">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="68e3f-119">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="68e3f-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="68e3f-120">HTTP request</span></span>

<span data-ttu-id="68e3f-121">Para comenzar el seguimiento de los cambios, realizar una solicitud que incluya la función delta en el recurso directoryRole.</span><span class="sxs-lookup"><span data-stu-id="68e3f-121">To begin tracking changes, you make a request including the delta function on the directoryRole resource.</span></span> 

<!-- { "blockType": "ignored" } -->
```http
GET /directoryRoles/delta
```

### <a name="query-parameters"></a><span data-ttu-id="68e3f-122">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="68e3f-122">Query parameters</span></span>

<span data-ttu-id="68e3f-123">Seguimiento de los cambios incurre una ronda de una o más llamadas de función de **delta** .</span><span class="sxs-lookup"><span data-stu-id="68e3f-123">Tracking changes incurs a round of one or more **delta** function calls.</span></span> <span data-ttu-id="68e3f-124">Si usa cualquier parámetro de consulta (distinto de `$deltatoken` y `$skiptoken`), debe especificar en la solicitud inicial del **delta** .</span><span class="sxs-lookup"><span data-stu-id="68e3f-124">If you use any query parameter (other than `$deltatoken` and `$skiptoken`), you must specify it in the initial **delta** request.</span></span> <span data-ttu-id="68e3f-125">Microsoft Graph codifica automáticamente los parámetros especificados en la parte de símbolo (token) de la `nextLink` o `deltaLink` dirección URL proporcionada en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="68e3f-125">Microsoft Graph automatically encodes any specified parameters into the token portion of the `nextLink` or `deltaLink` URL provided in the response.</span></span> <span data-ttu-id="68e3f-126">Solo debe especificar una vez por adelantado los parámetros de consulta deseados.</span><span class="sxs-lookup"><span data-stu-id="68e3f-126">You only need to specify any desired query parameters once upfront.</span></span> <span data-ttu-id="68e3f-127">En solicitudes posteriores, copie y aplique la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.</span><span class="sxs-lookup"><span data-stu-id="68e3f-127">In subsequent requests, copy and apply the `nextLink` or `deltaLink` URL from the previous response, as that URL already includes the encoded, desired parameters.</span></span>

| <span data-ttu-id="68e3f-128">Parámetro de consulta</span><span class="sxs-lookup"><span data-stu-id="68e3f-128">Query parameter</span></span>      | <span data-ttu-id="68e3f-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="68e3f-129">Type</span></span>   |<span data-ttu-id="68e3f-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="68e3f-130">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="68e3f-131">$deltatoken</span><span class="sxs-lookup"><span data-stu-id="68e3f-131">$deltatoken</span></span> | <span data-ttu-id="68e3f-132">string</span><span class="sxs-lookup"><span data-stu-id="68e3f-132">string</span></span> | <span data-ttu-id="68e3f-133">Un [símbolo (token) de estado](/graph/delta-query-overview) devuelto en el `deltaLink` dirección URL de la llamada de función **delta** anterior para la misma colección de recursos, que indica la finalización de ese round de seguimiento de cambios.</span><span class="sxs-lookup"><span data-stu-id="68e3f-133">A [state token](/graph/delta-query-overview) returned in the `deltaLink` URL of the previous **delta** function call for the same resource collection, indicating the completion of that round of change tracking.</span></span> <span data-ttu-id="68e3f-134">Guardar y aplicar todo el `deltaLink` dirección URL incluido este token en la primera solicitud de la siguiente ronda de seguimiento de cambios para esa colección.</span><span class="sxs-lookup"><span data-stu-id="68e3f-134">Save and apply the entire `deltaLink` URL including this token in the first request of the next round of change tracking for that collection.</span></span>|
| <span data-ttu-id="68e3f-135">$skiptoken</span><span class="sxs-lookup"><span data-stu-id="68e3f-135">$skiptoken</span></span> | <span data-ttu-id="68e3f-136">string</span><span class="sxs-lookup"><span data-stu-id="68e3f-136">string</span></span> | <span data-ttu-id="68e3f-137">Un [símbolo (token) de estado](/graph/delta-query-overview) devuelto en el `nextLink` dirección URL de la llamada de función **delta** anterior, que indica que hay más cambios para realizar un seguimiento en la misma colección de recursos.</span><span class="sxs-lookup"><span data-stu-id="68e3f-137">A [state token](/graph/delta-query-overview) returned in the `nextLink` URL of the previous **delta** function call, indicating there are further changes to be tracked in the same resource collection.</span></span> |

## <a name="optional-query-parameters"></a><span data-ttu-id="68e3f-138">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="68e3f-138">Optional query parameters</span></span>

<span data-ttu-id="68e3f-139">Este método admite parámetros de consulta de OData a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="68e3f-139">This method supports OData Query Parameters to help customize the response.</span></span>

- <span data-ttu-id="68e3f-p107">Puede utilizar un parámetro de consulta `$select` como en cualquier solicitud GET para especificar solo las propiedades que necesita para un mejor rendimiento. Siempre se devuelve la propiedad _id_.</span><span class="sxs-lookup"><span data-stu-id="68e3f-p107">You can use a `$select` query parameter as in any GET request to specify only the properties your need for best performance. The _id_ property is always returned.</span></span> 

- <span data-ttu-id="68e3f-142">No hay compatibilidad limitada para `$filter`:</span><span class="sxs-lookup"><span data-stu-id="68e3f-142">There is limited support for `$filter`:</span></span>
  * <span data-ttu-id="68e3f-143">El único admitido `$filter` expresión es para realizar un seguimiento de cambios para recursos específicos, por su identificador: `$filter=id+eq+{value}` o `$filter=id+eq+{value1}+or+id+eq+{value2}`.</span><span class="sxs-lookup"><span data-stu-id="68e3f-143">The only supported `$filter` expression is for tracking changes for specific resources, by their id:  `$filter=id+eq+{value}` or `$filter=id+eq+{value1}+or+id+eq+{value2}`.</span></span> <span data-ttu-id="68e3f-144">El número de identificadores que puede especificar está limitado por la longitud máxima de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="68e3f-144">The number of ids you can specify is limited by the maximum URL length.</span></span>


## <a name="request-headers"></a><span data-ttu-id="68e3f-145">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="68e3f-145">Request headers</span></span>
| <span data-ttu-id="68e3f-146">Nombre</span><span class="sxs-lookup"><span data-stu-id="68e3f-146">Name</span></span>       | <span data-ttu-id="68e3f-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="68e3f-147">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="68e3f-148">Authorization</span><span class="sxs-lookup"><span data-stu-id="68e3f-148">Authorization</span></span>  | <span data-ttu-id="68e3f-149">&lt;token&gt; de portador</span><span class="sxs-lookup"><span data-stu-id="68e3f-149">Bearer &lt;token&gt;</span></span>|
| <span data-ttu-id="68e3f-150">Content-Type</span><span class="sxs-lookup"><span data-stu-id="68e3f-150">Content-Type</span></span>  | <span data-ttu-id="68e3f-151">application/json</span><span class="sxs-lookup"><span data-stu-id="68e3f-151">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="68e3f-152">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="68e3f-152">Request body</span></span>
<span data-ttu-id="68e3f-153">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="68e3f-153">Do not supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="68e3f-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="68e3f-154">Response</span></span>

<span data-ttu-id="68e3f-155">Si tiene éxito, este método devuelve `200 OK` objeto de colección de respuesta código y [directoryRole](../resources/directoryrole.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="68e3f-155">If successful, this method returns `200 OK` response code and [directoryRole](../resources/directoryrole.md) collection object in the response body.</span></span> <span data-ttu-id="68e3f-156">La respuesta incluye también una dirección URL de nextLink o una dirección URL de deltaLink.</span><span class="sxs-lookup"><span data-stu-id="68e3f-156">The response also includes a nextLink URL or a deltaLink URL.</span></span> 

- <span data-ttu-id="68e3f-157">Si un `nextLink` se devuelve la dirección URL, hay páginas adicionales de datos que se recuperarán en la sesión.</span><span class="sxs-lookup"><span data-stu-id="68e3f-157">If a `nextLink` URL is returned, there are additional pages of data to be retrieved in the session.</span></span> <span data-ttu-id="68e3f-158">La aplicación continúa realizar solicitudes mediante el `nextLink` dirección URL hasta un `deltaLink` dirección URL se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="68e3f-158">The application continues making requests using the `nextLink` URL until a `deltaLink` URL is included in the response.</span></span>

- <span data-ttu-id="68e3f-159">Si un `deltaLink` se devuelve la dirección URL, no hay ningún dato más sobre el estado existente del recurso que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="68e3f-159">If a `deltaLink` URL is returned, there is no more data about the existing state of the resource to be returned.</span></span> <span data-ttu-id="68e3f-160">Conservar y utilizar el `deltaLink` dirección URL para obtener más información acerca de los cambios realizados en el recurso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="68e3f-160">Persist and use the `deltaLink` URL to learn about changes to the resource in the future.</span></span>

<span data-ttu-id="68e3f-161">Vea:</span><span class="sxs-lookup"><span data-stu-id="68e3f-161">See:</span></span></br>
- <span data-ttu-id="68e3f-162">[Usar la consulta delta](/graph/delta-query-overview) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="68e3f-162">[Using Delta Query](/graph/delta-query-overview) for more details</span></span></br>
- <span data-ttu-id="68e3f-163">[Obtener los cambios incrementales de usuarios](/graph/delta-query-users) para obtener un ejemplo de solicitud.</span><span class="sxs-lookup"><span data-stu-id="68e3f-163">[Get incremental changes for users](/graph/delta-query-users) for an example requests.</span></span></br>

### <a name="example"></a><span data-ttu-id="68e3f-164">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="68e3f-164">Example</span></span>
##### <a name="request"></a><span data-ttu-id="68e3f-165">Solicitud</span><span class="sxs-lookup"><span data-stu-id="68e3f-165">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "directoryRole_delta"
}-->
```http
GET https://graph.microsoft.com/beta/directoryRoles/delta
```

##### <a name="response"></a><span data-ttu-id="68e3f-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="68e3f-166">Response</span></span>
<span data-ttu-id="68e3f-p112">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="68e3f-p112">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#directoryRoles",
  "@odata.nextLink":"https://graph.microsoft.com/beta/directoryRoles/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjsXoYQp_dpA3cNJWc",
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

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryRole: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
