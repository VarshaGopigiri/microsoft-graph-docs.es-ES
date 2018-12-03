---
title: Obtener el inicio de sesión
description: Recupera los inicios de sesión de usuario de Azure AD para el inquilino. Inicios de sesión que son interactivas en naturaleza (donde un nombre de usuario y contraseña se pasa como parte de símbolo (token) de autorización) y los inicios de sesión federados correctos actualmente se incluyen en los registros de inicio de sesión.
ms.openlocfilehash: 1934af9b918dc976ef7f3fc6cdd21c04f6fcc705
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089382"
---
# <a name="get-signin"></a><span data-ttu-id="d7036-104">Obtener el inicio de sesión</span><span class="sxs-lookup"><span data-stu-id="d7036-104">Get signIn</span></span>
<span data-ttu-id="d7036-105">Recupera los inicios de sesión de usuario de Azure AD para el inquilino.</span><span class="sxs-lookup"><span data-stu-id="d7036-105">Retrieves the Azure AD user sign-ins for your tenant.</span></span> <span data-ttu-id="d7036-106">Inicios de sesión que son interactivas en naturaleza (donde un nombre de usuario y contraseña se pasa como parte de símbolo (token) de autorización) y los inicios de sesión federados correctos actualmente se incluyen en los registros de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="d7036-106">Sign-ins that are interactive in nature (where a username/password is passed as part of authorization token) and successful federated sign-ins are currently included in the sign-in logs.</span></span>


## <a name="permissions"></a><span data-ttu-id="d7036-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="d7036-107">Permissions</span></span>
<span data-ttu-id="d7036-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d7036-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d7036-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d7036-110">Permission type</span></span>      | <span data-ttu-id="d7036-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d7036-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d7036-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d7036-112">Delegated (work or school account)</span></span> | <span data-ttu-id="d7036-113">AuditLog.Read.All</span><span class="sxs-lookup"><span data-stu-id="d7036-113">AuditLog.Read.All</span></span> |
|<span data-ttu-id="d7036-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d7036-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d7036-115">No admitido</span><span class="sxs-lookup"><span data-stu-id="d7036-115">Not supported</span></span>   |
|<span data-ttu-id="d7036-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d7036-116">Application</span></span> | <span data-ttu-id="d7036-117">AuditLog.Read.All</span><span class="sxs-lookup"><span data-stu-id="d7036-117">AuditLog.Read.All</span></span> | 

<span data-ttu-id="d7036-118">Además, las aplicaciones deben estar [registrado correctamente](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-prerequisites-azure-portal) a Azure AD.</span><span class="sxs-lookup"><span data-stu-id="d7036-118">In addition, apps must be [properly registered](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-prerequisites-azure-portal) to Azure AD.</span></span>

## <a name="http-request"></a><span data-ttu-id="d7036-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d7036-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /auditLogs/signIns/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="d7036-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="d7036-120">Optional query parameters</span></span>
<span data-ttu-id="d7036-121">Este método admite los siguientes parámetros de consulta de OData a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d7036-121">This method supports the following OData Query Parameters to help customize the response.</span></span> <span data-ttu-id="d7036-122">Compruebe [Los parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para el uso de estos parámetros.</span><span class="sxs-lookup"><span data-stu-id="d7036-122">Check [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) for how to use these parameters.</span></span>

## <a name="request-headers"></a><span data-ttu-id="d7036-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d7036-123">Request headers</span></span>
| <span data-ttu-id="d7036-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="d7036-124">Name</span></span>      |<span data-ttu-id="d7036-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7036-125">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="d7036-126">Autorización</span><span class="sxs-lookup"><span data-stu-id="d7036-126">Authorization</span></span>  | <span data-ttu-id="d7036-127">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="d7036-127">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="d7036-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d7036-128">Request body</span></span>
<span data-ttu-id="d7036-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d7036-129">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="d7036-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d7036-130">Response</span></span>
<span data-ttu-id="d7036-131">Si tiene éxito, este método devuelve una `200 OK` objeto de [Inicio de sesión](../resources/signin.md) y de código de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d7036-131">If successful, this method returns a `200 OK` response code and [signIn](../resources/signin.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="d7036-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d7036-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d7036-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d7036-133">Request</span></span>
<span data-ttu-id="d7036-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d7036-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "reque|location/city| eq, startswith|
st",
  "name": "get_signin"
}-->
```http
GET https://graph.microsoft.com/beta/auditLogs/signIns/{id}
```
##### <a name="response"></a><span data-ttu-id="d7036-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d7036-135">Response</span></span>
<span data-ttu-id="d7036-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d7036-136">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.signIn"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 211
```
```json
{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#auditLogs/signIns",
    "value": [{
        "id": "id",
        "createdDateTime": "2018-01-09T21:17:21.5077253Z",
        "userDisplayName": "Jamie Doe",
        "userPrincipalName": "jdoe@contoso.com",
        "userId": "bbb3b4b5-e6e6-f7f5-f7f5-090805040302",
        "appId": "d3590ed6-52b3-4102-aeff-aad2292ab01c",
        "appDisplayName": "Azure",
        "ipAddress": "127.0.0.1",
        "status": {
            "errorCode": 0,
            "failureReason": null,
            "additionalDetails": "SignIn Success & CA Sucess"
        },
        "clientAppUsed": null,
        "deviceDetail": {
            "deviceId": "34390ed6-52b3-4102-aeff-aad2292abac3",
            "displayName": "DeviceName",
            "operatingSystem": "Windows 10",
            "browser": "Rich Client v1.0.2016.0",
            "isCompliant": true,
            "isManaged": true,
            "trustType": ""
        },
        "location": {
            "city": "Redmond",
            "state": "WA",
            "countryOrRegion": "USA",
            "geoCoordinates": {
                "altitude": 41.589,
                "latitude": 41.589,
                "longitude": -93.6151
            }
        },
        "mfaDetail": {
            "mfaAuthMethod": "Phone Auth",
            "mfaAuthDetail": null
        },
        "correlationId": "17c47d3c-593d-4d08-ac20-813892b87e42",
        "conditionalAccessApplied": true,
        "conditionalAccessPolicies": [{
            "id": "26490ed6-52b3-4102-aeff-aad2292abacf",
            "displayName": "capPolicy",
            "enforcedAccessControls": ["MFA", "TOU"],
            "enforcedSessionControls": ["CloudAppSecurity"],
            "result": "success"
        }],
        "isRisky": false,
        "riskLevel": "low"
    }]
}

```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get signIn",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->