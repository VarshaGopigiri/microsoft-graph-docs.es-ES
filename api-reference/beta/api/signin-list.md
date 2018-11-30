---
title: Lista signIns
description: Recupera los inicios de sesión de usuario de Azure AD para el inquilino. Inicios de sesión que son interactivas en naturaleza (donde un nombre de usuario y contraseña se pasa como parte de símbolo (token) de autorización) y los inicios de sesión federados correctos actualmente se incluyen en los registros de inicio de sesión.  La signIns más recientes se devuelven en primer lugar.
ms.openlocfilehash: 3abca59187dcc9667789e33bcefc1bcc51d5ab10
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084758"
---
# <a name="list-signins"></a><span data-ttu-id="6b531-105">Lista signIns</span><span class="sxs-lookup"><span data-stu-id="6b531-105">List signIns</span></span>

<span data-ttu-id="6b531-106">Recupera los inicios de sesión de usuario de Azure AD para el inquilino.</span><span class="sxs-lookup"><span data-stu-id="6b531-106">Retrieves the Azure AD user sign-ins for your tenant.</span></span> <span data-ttu-id="6b531-107">Inicios de sesión que son interactivas en naturaleza (donde un nombre de usuario y contraseña se pasa como parte de símbolo (token) de autorización) y los inicios de sesión federados correctos actualmente se incluyen en los registros de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="6b531-107">Sign-ins that are interactive in nature (where a username/password is passed as part of authorization token) and successful federated sign-ins are currently included in the sign-in logs.</span></span>  <span data-ttu-id="6b531-108">La signIns más recientes se devuelven en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="6b531-108">The most recent signIns are returned first.</span></span>


## <a name="permissions"></a><span data-ttu-id="6b531-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="6b531-109">Permissions</span></span>
<span data-ttu-id="6b531-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6b531-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6b531-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6b531-112">Permission type</span></span>      | <span data-ttu-id="6b531-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6b531-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6b531-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6b531-114">Delegated (work or school account)</span></span> | <span data-ttu-id="6b531-115">AuditLog.Read.All</span><span class="sxs-lookup"><span data-stu-id="6b531-115">AuditLog.Read.All</span></span> |
|<span data-ttu-id="6b531-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6b531-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6b531-117">No admitido</span><span class="sxs-lookup"><span data-stu-id="6b531-117">Not supported</span></span>   |
|<span data-ttu-id="6b531-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6b531-118">Application</span></span> | <span data-ttu-id="6b531-119">AuditLog.Read.All</span><span class="sxs-lookup"><span data-stu-id="6b531-119">AuditLog.Read.All</span></span> | 

<span data-ttu-id="6b531-120">Además, las aplicaciones deben estar [registrado correctamente](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-prerequisites-azure-portal) a Azure AD.</span><span class="sxs-lookup"><span data-stu-id="6b531-120">In addition, apps must be [properly registered](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-prerequisites-azure-portal) to Azure AD.</span></span>

## <a name="http-request"></a><span data-ttu-id="6b531-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6b531-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET auditLogs/signIns
```
## <a name="optional-query-parameters"></a><span data-ttu-id="6b531-122">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="6b531-122">Optional query parameters</span></span>
<span data-ttu-id="6b531-123">Este método admite los siguientes parámetros de consulta de OData a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6b531-123">This method supports the following OData Query Parameters to help customize the response.</span></span> <span data-ttu-id="6b531-124">Compruebe [Los parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para el uso de estos parámetros.</span><span class="sxs-lookup"><span data-stu-id="6b531-124">Check [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) for how to use these parameters.</span></span>

|<span data-ttu-id="6b531-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="6b531-125">Name</span></span>     |<span data-ttu-id="6b531-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b531-126">Description</span></span>                            |<span data-ttu-id="6b531-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6b531-127">Example</span></span>|
|:--------------------|----------------|------------------------------------------------------------------------|
|[<span data-ttu-id="6b531-128">$filter</span><span class="sxs-lookup"><span data-stu-id="6b531-128">$filter</span></span>](https://developer.microsoft.com/graph/docs/concepts/query_parameters#filter-parameter)|<span data-ttu-id="6b531-129">Filtra los resultados (filas).</span><span class="sxs-lookup"><span data-stu-id="6b531-129">Filters results (rows).</span></span> |`/auditLogs/signIns?&$filter=createdDateTime le 2018-01-24`
|[<span data-ttu-id="6b531-130">$top</span><span class="sxs-lookup"><span data-stu-id="6b531-130">$top</span></span>](https://developer.microsoft.com/graph/docs/concepts/query_parameters#top-parameter)|<span data-ttu-id="6b531-131">Establece el tamaño de la página de resultados.</span><span class="sxs-lookup"><span data-stu-id="6b531-131">Sets the page size of results.</span></span>|`/auditLogs/signIns?$top=1`|
|[<span data-ttu-id="6b531-132">$skiptoken</span><span class="sxs-lookup"><span data-stu-id="6b531-132">$skiptoken</span></span>](https://developer.microsoft.com/graph/docs/concepts/query_parameters#skiptoken-parameter)|<span data-ttu-id="6b531-133">Recupera que la siguiente página de resultados de resultado establece que abarcan varias páginas.</span><span class="sxs-lookup"><span data-stu-id="6b531-133">Retrieves the next page of results from result sets that span multiple pages.</span></span>|`/auditLogs/signIns?$skiptoken=01fa0e77c60c2d3d63226c8e3294c860__1`|

### <a name="list-of-attributes-supported-by-filter-parameter"></a><span data-ttu-id="6b531-134">Lista de atributos admitidos por el parámetro $filter</span><span class="sxs-lookup"><span data-stu-id="6b531-134">List of attributes supported by $filter parameter</span></span>
|<span data-ttu-id="6b531-135">Nombre del atributo</span><span class="sxs-lookup"><span data-stu-id="6b531-135">Attribute Name</span></span> |<span data-ttu-id="6b531-136">Operadores admitidos</span><span class="sxs-lookup"><span data-stu-id="6b531-136">Supported operators</span></span>|
|:----------------|:------|
|<span data-ttu-id="6b531-137">id</span><span class="sxs-lookup"><span data-stu-id="6b531-137">id</span></span>|<span data-ttu-id="6b531-138">eq</span><span class="sxs-lookup"><span data-stu-id="6b531-138">eq</span></span>|
|<span data-ttu-id="6b531-139">userId</span><span class="sxs-lookup"><span data-stu-id="6b531-139">userId</span></span>|<span data-ttu-id="6b531-140">eq</span><span class="sxs-lookup"><span data-stu-id="6b531-140">eq</span></span>|
|<span data-ttu-id="6b531-141">appId</span><span class="sxs-lookup"><span data-stu-id="6b531-141">appId</span></span>|<span data-ttu-id="6b531-142">eq</span><span class="sxs-lookup"><span data-stu-id="6b531-142">eq</span></span>|
|<span data-ttu-id="6b531-143">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="6b531-143">createdDateTime</span></span>| <span data-ttu-id="6b531-144">EQ, le, ge</span><span class="sxs-lookup"><span data-stu-id="6b531-144">eq, le, ge</span></span>|
|<span data-ttu-id="6b531-145">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="6b531-145">userDisplayName</span></span>| <span data-ttu-id="6b531-146">EQ, startswith</span><span class="sxs-lookup"><span data-stu-id="6b531-146">eq, startswith</span></span>|
|<span data-ttu-id="6b531-147">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="6b531-147">userPrincipalName</span></span>| <span data-ttu-id="6b531-148">EQ, startswith</span><span class="sxs-lookup"><span data-stu-id="6b531-148">eq, startswith</span></span>|
|<span data-ttu-id="6b531-149">appDisplayName</span><span class="sxs-lookup"><span data-stu-id="6b531-149">appDisplayName</span></span>| <span data-ttu-id="6b531-150">EQ, startswith</span><span class="sxs-lookup"><span data-stu-id="6b531-150">eq, startswith</span></span>|
|<span data-ttu-id="6b531-151">ipAddress</span><span class="sxs-lookup"><span data-stu-id="6b531-151">ipAddress</span></span>| <span data-ttu-id="6b531-152">EQ, startswith</span><span class="sxs-lookup"><span data-stu-id="6b531-152">eq, startswith</span></span>|
|<span data-ttu-id="6b531-153">ubicación o ciudad</span><span class="sxs-lookup"><span data-stu-id="6b531-153">location/city</span></span>| <span data-ttu-id="6b531-154">EQ, startswith</span><span class="sxs-lookup"><span data-stu-id="6b531-154">eq, startswith</span></span>|
|<span data-ttu-id="6b531-155">ubicación o estado</span><span class="sxs-lookup"><span data-stu-id="6b531-155">location/state</span></span>| <span data-ttu-id="6b531-156">EQ, startswith</span><span class="sxs-lookup"><span data-stu-id="6b531-156">eq, startswith</span></span>|
|<span data-ttu-id="6b531-157">ubicación/countryOrRegion</span><span class="sxs-lookup"><span data-stu-id="6b531-157">location/countryOrRegion</span></span>| <span data-ttu-id="6b531-158">EQ, startswith</span><span class="sxs-lookup"><span data-stu-id="6b531-158">eq, startswith</span></span>|
|<span data-ttu-id="6b531-159">estado/errorCode</span><span class="sxs-lookup"><span data-stu-id="6b531-159">status/errorCode</span></span>|<span data-ttu-id="6b531-160">eq</span><span class="sxs-lookup"><span data-stu-id="6b531-160">eq</span></span>|
|<span data-ttu-id="6b531-161">initiatedBy/usuario/Id.</span><span class="sxs-lookup"><span data-stu-id="6b531-161">initiatedBy/user/id</span></span>|<span data-ttu-id="6b531-162">eq</span><span class="sxs-lookup"><span data-stu-id="6b531-162">eq</span></span>|
|<span data-ttu-id="6b531-163">displayName, initiatedBy/usuario</span><span class="sxs-lookup"><span data-stu-id="6b531-163">initiatedBy/user/displayName</span></span>| <span data-ttu-id="6b531-164">eq</span><span class="sxs-lookup"><span data-stu-id="6b531-164">eq</span></span>|
|<span data-ttu-id="6b531-165">usuario/initiatedBy/userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="6b531-165">initiatedBy/user/userPrincipalName</span></span>| <span data-ttu-id="6b531-166">EQ, startswith</span><span class="sxs-lookup"><span data-stu-id="6b531-166">eq, startswith</span></span>|
|<span data-ttu-id="6b531-167">clientAppUsed</span><span class="sxs-lookup"><span data-stu-id="6b531-167">clientAppUsed</span></span>| <span data-ttu-id="6b531-168">eq</span><span class="sxs-lookup"><span data-stu-id="6b531-168">eq</span></span>|
|<span data-ttu-id="6b531-169">conditionalAccessStatus</span><span class="sxs-lookup"><span data-stu-id="6b531-169">conditionalAccessStatus</span></span> | <span data-ttu-id="6b531-170">eq</span><span class="sxs-lookup"><span data-stu-id="6b531-170">eq</span></span>|
|<span data-ttu-id="6b531-171">deviceDetail o explorador</span><span class="sxs-lookup"><span data-stu-id="6b531-171">deviceDetail/browser</span></span>| <span data-ttu-id="6b531-172">EQ, startswith</span><span class="sxs-lookup"><span data-stu-id="6b531-172">eq, startswith</span></span>|
|<span data-ttu-id="6b531-173">deviceDetail/operatingSystem</span><span class="sxs-lookup"><span data-stu-id="6b531-173">deviceDetail/operatingSystem</span></span>| <span data-ttu-id="6b531-174">EQ, startswith</span><span class="sxs-lookup"><span data-stu-id="6b531-174">eq, startswith</span></span>|
|<span data-ttu-id="6b531-175">correlationId</span><span class="sxs-lookup"><span data-stu-id="6b531-175">correlationId</span></span>| <span data-ttu-id="6b531-176">eq</span><span class="sxs-lookup"><span data-stu-id="6b531-176">eq</span></span>|
|<span data-ttu-id="6b531-177">riskDetail</span><span class="sxs-lookup"><span data-stu-id="6b531-177">riskDetail</span></span>| <span data-ttu-id="6b531-178">eq</span><span class="sxs-lookup"><span data-stu-id="6b531-178">eq</span></span>|
|<span data-ttu-id="6b531-179">riskLevelAggregated</span><span class="sxs-lookup"><span data-stu-id="6b531-179">riskLevelAggregated</span></span>| <span data-ttu-id="6b531-180">eq</span><span class="sxs-lookup"><span data-stu-id="6b531-180">eq</span></span>|
|<span data-ttu-id="6b531-181">riskLevelDuringSignIn</span><span class="sxs-lookup"><span data-stu-id="6b531-181">riskLevelDuringSignIn</span></span>| <span data-ttu-id="6b531-182">eq</span><span class="sxs-lookup"><span data-stu-id="6b531-182">eq</span></span>|
|<span data-ttu-id="6b531-183">riskEventTypes</span><span class="sxs-lookup"><span data-stu-id="6b531-183">riskEventTypes</span></span>| <span data-ttu-id="6b531-184">eq</span><span class="sxs-lookup"><span data-stu-id="6b531-184">eq</span></span>|
|<span data-ttu-id="6b531-185">riskState</span><span class="sxs-lookup"><span data-stu-id="6b531-185">riskState</span></span>| <span data-ttu-id="6b531-186">eq</span><span class="sxs-lookup"><span data-stu-id="6b531-186">eq</span></span>|
|<span data-ttu-id="6b531-187">originalRequestId</span><span class="sxs-lookup"><span data-stu-id="6b531-187">originalRequestId</span></span>| <span data-ttu-id="6b531-188">eq</span><span class="sxs-lookup"><span data-stu-id="6b531-188">eq</span></span>|
|<span data-ttu-id="6b531-189">tokenIssuerName</span><span class="sxs-lookup"><span data-stu-id="6b531-189">tokenIssuerName</span></span>| <span data-ttu-id="6b531-190">eq</span><span class="sxs-lookup"><span data-stu-id="6b531-190">eq</span></span>|
|<span data-ttu-id="6b531-191">tokenIssuerType</span><span class="sxs-lookup"><span data-stu-id="6b531-191">tokenIssuerType</span></span>| <span data-ttu-id="6b531-192">eq</span><span class="sxs-lookup"><span data-stu-id="6b531-192">eq</span></span>|
|<span data-ttu-id="6b531-193">resourceDisplayName</span><span class="sxs-lookup"><span data-stu-id="6b531-193">resourceDisplayName</span></span>| <span data-ttu-id="6b531-194">eq</span><span class="sxs-lookup"><span data-stu-id="6b531-194">eq</span></span>|
|<span data-ttu-id="6b531-195">resourceId</span><span class="sxs-lookup"><span data-stu-id="6b531-195">resourceId</span></span>| <span data-ttu-id="6b531-196">eq</span><span class="sxs-lookup"><span data-stu-id="6b531-196">eq</span></span>|


## <a name="response"></a><span data-ttu-id="6b531-197">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6b531-197">Response</span></span>
<span data-ttu-id="6b531-198">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [Inicio de sesión](../resources/signin.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6b531-198">If successful, this method returns a `200 OK` response code and collection of [signIn](../resources/signin.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6b531-199">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6b531-199">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6b531-200">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6b531-200">Request</span></span>
<span data-ttu-id="6b531-201">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6b531-201">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_signins"
}-->
```http
GET https://graph.microsoft.com/beta/auditLogs/signIns
```
##### <a name="response"></a><span data-ttu-id="6b531-202">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6b531-202">Response</span></span>
<span data-ttu-id="6b531-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6b531-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.signIn",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 264
```
```json
{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#auditLogs/signIns",
    "value": [{
        "id":"b01b1726-0147-425e-a7f7-21f252050400",
        "createdDateTime":"2018-11-06T18:48:33.8527147Z",
        "userDisplayName":"Jon Doe",
         "userPrincipalName":"admin@aad171.ccsctp.net",
         "userId":"d7cc485d-2c1b-422c-98fd-5ce52859a4a3",
        "appId":"c44b4083-3bb0-49c1-b47d-974e53cbdf3c",
         "appDisplayName":"Azure Portal",
         "ipAddress":"207.254.19.10",
         "clientAppUsed":"Browser",
        "mfaDetail":null,
         "correlationId":"65dd87ce-2183-419e-81a9-d6e20379bcc2",
         "conditionalAccessStatus":"notApplied",
        "originalRequestId":null,
        "isInteractive":true,
        "tokenIssuerName":null,
        "tokenIssuerType":"AzureAD",
        "processingTimeInMilliseconds":0,
        "riskDetail":"none",
        "riskLevelAggregated":"none",
        "riskLevelDuringSignIn":"none",
        "riskState":"none",
        "riskEventTypes":[

        ],
        "resourceDisplayName":"windows azure service management api",
        "resourceId":"797f4846-ba00-4fd7-ba43-dac1f8f63013",
        "authenticationMethodsUsed":[

        ],
        "status":{
            "errorCode":50140,
            "failureReason":"This error occurred due to 'Keep me signed in' interrupt when the user was signing-in.",
            "additionalDetails":null
        },
        "deviceDetail":{
            "deviceId":null,
            "displayName":null,
            "operatingSystem":"Windows 7",
            "browser":"Chrome 63.0.3239",
            "isCompliant":null,
            "isManaged":null,
            "trustType":null
        },
        "location":{
            "city":"Lithia Springs",
            "state":"Georgia",
            "countryOrRegion":"US",
            "geoCoordinates":{
                "altitude":null,
                "latitude":33.7930908203125,
                "longitude":-84.445358276367188
            }
        },
        "appliedConditionalAccessPolicies":[
            {
            "id":"6551c58c-e5da-4036-a6ea-c2c3fad264f1",
            "displayName":"New Name here4",
            "enforcedGrantControls":[
                "Mfa",
                "RequireCompliantDevice"
            ],
            "enforcedSessionControls":[

            ],
            "result":"notApplied"
            },
            {
            "id":"b645a140-20fe-4ce0-a724-18ab201e9026",
            "displayName":"PipelineTest4",
            "enforcedGrantControls":[

            ],
            "enforcedSessionControls":[

            ],
            "result":"notEnabled"
            }
        ],
        "authenticationProcessingDetails":[

        ],
        "networkLocationDetails":[

        ]
        }
    
    ]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List signIns",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
