---
title: 'aplicación: delta'
description: Get recién creado, actualiza o elimina aplicaciones sin tener que realizar un acceso completo de lectura de la colección completa de recursos. Para obtener más información, vea Uso de consulta de Delta.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 4479048865d50cb0887d938708cb44ff62a4a9b2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27917198"
---
# <a name="application-delta"></a><span data-ttu-id="5f4cc-104">aplicación: delta</span><span class="sxs-lookup"><span data-stu-id="5f4cc-104">application: delta</span></span>

> <span data-ttu-id="5f4cc-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5f4cc-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5f4cc-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5f4cc-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5f4cc-107">Get recién creado, actualiza o elimina aplicaciones sin tener que realizar un acceso completo de lectura de la colección completa de recursos.</span><span class="sxs-lookup"><span data-stu-id="5f4cc-107">Get newly created, updated, or deleted applications without having to perform a full read of the entire resource collection.</span></span> <span data-ttu-id="5f4cc-108">Para obtener más información, vea [Uso de consulta de Delta](/graph/delta-query-overview) .</span><span class="sxs-lookup"><span data-stu-id="5f4cc-108">See [Using Delta Query](/graph/delta-query-overview) for details.</span></span>

## <a name="permissions"></a><span data-ttu-id="5f4cc-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="5f4cc-109">Permissions</span></span>

<span data-ttu-id="5f4cc-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5f4cc-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="5f4cc-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5f4cc-112">Permission type</span></span>      | <span data-ttu-id="5f4cc-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5f4cc-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5f4cc-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5f4cc-114">Delegated (work or school account)</span></span> | <span data-ttu-id="5f4cc-115">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="5f4cc-115">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="5f4cc-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5f4cc-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5f4cc-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5f4cc-117">Not supported.</span></span>    |
|<span data-ttu-id="5f4cc-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5f4cc-118">Application</span></span> | <span data-ttu-id="5f4cc-119">Application.ReadWrite.All, Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="5f4cc-119">Application.ReadWrite.All, Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="5f4cc-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5f4cc-120">HTTP request</span></span>

<span data-ttu-id="5f4cc-121">Para comenzar el seguimiento de los cambios, realizar una solicitud que incluya la función delta en el recurso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5f4cc-121">To begin tracking changes, you make a request including the delta function on the application resource.</span></span> 

<!-- { "blockType": "ignored" } -->
```http
GET /applications/delta
```

### <a name="query-parameters"></a><span data-ttu-id="5f4cc-122">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="5f4cc-122">Query parameters</span></span>

<span data-ttu-id="5f4cc-123">Seguimiento de los cambios incurre una ronda de una o más llamadas de función de **delta** .</span><span class="sxs-lookup"><span data-stu-id="5f4cc-123">Tracking changes incurs a round of one or more **delta** function calls.</span></span> <span data-ttu-id="5f4cc-124">Si usa cualquier parámetro de consulta (distinto de `$deltatoken` y `$skiptoken`), debe especificar en la solicitud inicial del **delta** .</span><span class="sxs-lookup"><span data-stu-id="5f4cc-124">If you use any query parameter (other than `$deltatoken` and `$skiptoken`), you must specify it in the initial **delta** request.</span></span> <span data-ttu-id="5f4cc-125">Microsoft Graph codifica automáticamente los parámetros especificados en la parte de símbolo (token) de la `nextLink` o `deltaLink` dirección URL proporcionada en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5f4cc-125">Microsoft Graph automatically encodes any specified parameters into the token portion of the `nextLink` or `deltaLink` URL provided in the response.</span></span> <span data-ttu-id="5f4cc-126">Solo debe especificar una vez por adelantado los parámetros de consulta deseados.</span><span class="sxs-lookup"><span data-stu-id="5f4cc-126">You only need to specify any desired query parameters once upfront.</span></span> <span data-ttu-id="5f4cc-127">En solicitudes posteriores, copie y aplique la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.</span><span class="sxs-lookup"><span data-stu-id="5f4cc-127">In subsequent requests, copy and apply the `nextLink` or `deltaLink` URL from the previous response, as that URL already includes the encoded, desired parameters.</span></span>

| <span data-ttu-id="5f4cc-128">Parámetro de consulta</span><span class="sxs-lookup"><span data-stu-id="5f4cc-128">Query parameter</span></span>      | <span data-ttu-id="5f4cc-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f4cc-129">Type</span></span>   |<span data-ttu-id="5f4cc-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f4cc-130">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="5f4cc-131">$deltatoken</span><span class="sxs-lookup"><span data-stu-id="5f4cc-131">$deltatoken</span></span> | <span data-ttu-id="5f4cc-132">string</span><span class="sxs-lookup"><span data-stu-id="5f4cc-132">string</span></span> | <span data-ttu-id="5f4cc-133">Un [símbolo (token) de estado](/graph/delta-query-overview) devuelto en el `deltaLink` dirección URL de la llamada de función **delta** anterior para la misma colección de recursos, que indica la finalización de ese round de seguimiento de cambios.</span><span class="sxs-lookup"><span data-stu-id="5f4cc-133">A [state token](/graph/delta-query-overview) returned in the `deltaLink` URL of the previous **delta** function call for the same resource collection, indicating the completion of that round of change tracking.</span></span> <span data-ttu-id="5f4cc-134">Guardar y aplicar todo el `deltaLink` dirección URL incluido este token en la primera solicitud de la siguiente ronda de seguimiento de cambios para esa colección.</span><span class="sxs-lookup"><span data-stu-id="5f4cc-134">Save and apply the entire `deltaLink` URL including this token in the first request of the next round of change tracking for that collection.</span></span>|
| <span data-ttu-id="5f4cc-135">$skiptoken</span><span class="sxs-lookup"><span data-stu-id="5f4cc-135">$skiptoken</span></span> | <span data-ttu-id="5f4cc-136">string</span><span class="sxs-lookup"><span data-stu-id="5f4cc-136">string</span></span> | <span data-ttu-id="5f4cc-137">Un [símbolo (token) de estado](/graph/delta-query-overview) devuelto en el `nextLink` dirección URL de la llamada de función **delta** anterior, que indica que hay más cambios para realizar un seguimiento en la misma colección de recursos.</span><span class="sxs-lookup"><span data-stu-id="5f4cc-137">A [state token](/graph/delta-query-overview) returned in the `nextLink` URL of the previous **delta** function call, indicating there are further changes to be tracked in the same resource collection.</span></span> |

## <a name="optional-query-parameters"></a><span data-ttu-id="5f4cc-138">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="5f4cc-138">Optional query parameters</span></span>

<span data-ttu-id="5f4cc-139">Este método admite parámetros de consulta de OData a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5f4cc-139">This method supports OData Query Parameters to help customize the response.</span></span>

- <span data-ttu-id="5f4cc-p107">Puede utilizar un parámetro de consulta `$select` como en cualquier solicitud GET para especificar solo las propiedades que necesita para un mejor rendimiento. Siempre se devuelve la propiedad _id_.</span><span class="sxs-lookup"><span data-stu-id="5f4cc-p107">You can use a `$select` query parameter as in any GET request to specify only the properties your need for best performance. The _id_ property is always returned.</span></span> 

- <span data-ttu-id="5f4cc-142">No hay compatibilidad limitada para `$filter`:</span><span class="sxs-lookup"><span data-stu-id="5f4cc-142">There is limited support for `$filter`:</span></span>
  * <span data-ttu-id="5f4cc-143">El único admitido `$filter` expresión es para realizar un seguimiento de cambios para recursos específicos, por su identificador: `$filter=id+eq+{value}` o `$filter=id+eq+{value1}+or+id+eq+{value2}`.</span><span class="sxs-lookup"><span data-stu-id="5f4cc-143">The only supported `$filter` expression is for tracking changes for specific resources, by their id:  `$filter=id+eq+{value}` or `$filter=id+eq+{value1}+or+id+eq+{value2}`.</span></span> <span data-ttu-id="5f4cc-144">El número de identificadores que puede especificar está limitado por la longitud máxima de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="5f4cc-144">The number of ids you can specify is limited by the maximum URL length.</span></span>


## <a name="request-headers"></a><span data-ttu-id="5f4cc-145">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5f4cc-145">Request headers</span></span>
| <span data-ttu-id="5f4cc-146">Nombre</span><span class="sxs-lookup"><span data-stu-id="5f4cc-146">Name</span></span>       | <span data-ttu-id="5f4cc-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f4cc-147">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="5f4cc-148">Authorization</span><span class="sxs-lookup"><span data-stu-id="5f4cc-148">Authorization</span></span>  | <span data-ttu-id="5f4cc-149">&lt;token&gt; de portador</span><span class="sxs-lookup"><span data-stu-id="5f4cc-149">Bearer &lt;token&gt;</span></span>|
| <span data-ttu-id="5f4cc-150">Content-Type</span><span class="sxs-lookup"><span data-stu-id="5f4cc-150">Content-Type</span></span>  | <span data-ttu-id="5f4cc-151">application/json</span><span class="sxs-lookup"><span data-stu-id="5f4cc-151">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="5f4cc-152">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5f4cc-152">Request body</span></span>
<span data-ttu-id="5f4cc-153">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5f4cc-153">Do not supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="5f4cc-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5f4cc-154">Response</span></span>

<span data-ttu-id="5f4cc-155">Si tiene éxito, este método devuelve `200 OK` objeto de colección de respuesta código y la [aplicación](../resources/application.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5f4cc-155">If successful, this method returns `200 OK` response code and [application](../resources/application.md) collection object in the response body.</span></span> <span data-ttu-id="5f4cc-156">La respuesta incluye también una dirección URL de nextLink o una dirección URL de deltaLink.</span><span class="sxs-lookup"><span data-stu-id="5f4cc-156">The response also includes a nextLink URL or a deltaLink URL.</span></span> 

- <span data-ttu-id="5f4cc-157">Si un `nextLink` se devuelve la dirección URL, hay páginas adicionales de datos que se recuperarán en la sesión.</span><span class="sxs-lookup"><span data-stu-id="5f4cc-157">If a `nextLink` URL is returned, there are additional pages of data to be retrieved in the session.</span></span> <span data-ttu-id="5f4cc-158">La aplicación continúa realizar solicitudes mediante el `nextLink` dirección URL hasta un `deltaLink` dirección URL se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5f4cc-158">The application continues making requests using the `nextLink` URL until a `deltaLink` URL is included in the response.</span></span>

- <span data-ttu-id="5f4cc-159">Si un `deltaLink` se devuelve la dirección URL, no hay ningún dato más sobre el estado existente del recurso que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="5f4cc-159">If a `deltaLink` URL is returned, there is no more data about the existing state of the resource to be returned.</span></span> <span data-ttu-id="5f4cc-160">Conservar y utilizar el `deltaLink` dirección URL para obtener más información acerca de los cambios realizados en el recurso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="5f4cc-160">Persist and use the `deltaLink` URL to learn about changes to the resource in the future.</span></span>

<span data-ttu-id="5f4cc-161">Vea:</span><span class="sxs-lookup"><span data-stu-id="5f4cc-161">See:</span></span></br>
- <span data-ttu-id="5f4cc-162">[Usar la consulta delta](/graph/delta-query-overview) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="5f4cc-162">[Using Delta Query](/graph/delta-query-overview) for more details</span></span></br>
- <span data-ttu-id="5f4cc-163">[Obtener los cambios incrementales de usuarios](/graph/delta-query-users) para obtener un ejemplo de solicitud.</span><span class="sxs-lookup"><span data-stu-id="5f4cc-163">[Get incremental changes for users](/graph/delta-query-users) for an example requests.</span></span></br>

### <a name="example"></a><span data-ttu-id="5f4cc-164">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5f4cc-164">Example</span></span>
##### <a name="request"></a><span data-ttu-id="5f4cc-165">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5f4cc-165">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "application_delta"
}-->
```http
GET https://graph.microsoft.com/beta/applications/delta
```

##### <a name="response"></a><span data-ttu-id="5f4cc-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5f4cc-166">Response</span></span>
<span data-ttu-id="5f4cc-p112">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5f4cc-p112">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- { 
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.application",
  "isCollection": true 
} --> 
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#applications",
  "@odata.nextLink":"https://graph.microsoft.com/beta/applications/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjsXoYQp_dpA3cNJWc",
  "value": [
    {
      "api": {
        "acceptedAccessTokenVersion": 1,
        "publishedPermissionScopes": [
          {
            "adminConsentDescription": "adminConsentDescription-value",
            "adminConsentDisplayName": "adminConsentDisplayName-value",
            "id": "id-value",
            "isEnabled": true,
            "type": "type-value",
            "userConsentDescription": "userConsentDescription-value",
            "userConsentDisplayName": "userConsentDisplayName-value",
            "value": "value-value"
          }
        ]
      },
      "allowPublicClient": true,
      "applicationAliases": [
        "applicationAliases-value"
      ],
      "createdDateTime": "datetime-value",
      "installedClients": {
        "redirectUrls": [
          "redirectUrls-value"
        ]
      }
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "application: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
