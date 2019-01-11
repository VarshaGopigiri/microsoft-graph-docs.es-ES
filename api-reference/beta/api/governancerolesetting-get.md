---
title: Obtener governanceRoleSetting
description: Recuperar las propiedades y relaciones de un governanceRoleSetting.
localization_priority: Normal
ms.openlocfilehash: db4c2a287ba1089c4aac73b9f0cf6e204a726c86
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27864515"
---
# <a name="get-governancerolesetting"></a><span data-ttu-id="f9e7a-103">Obtener governanceRoleSetting</span><span class="sxs-lookup"><span data-stu-id="f9e7a-103">Get governanceRoleSetting</span></span>


> <span data-ttu-id="f9e7a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f9e7a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f9e7a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f9e7a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f9e7a-106">Recuperar las propiedades y relaciones de un [governanceRoleSetting](../resources/governancerolesetting.md).</span><span class="sxs-lookup"><span data-stu-id="f9e7a-106">Retrieve the properties and relationships of a [governanceRoleSetting](../resources/governancerolesetting.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="f9e7a-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="f9e7a-107">Permissions</span></span>
<span data-ttu-id="f9e7a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f9e7a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f9e7a-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f9e7a-110">Permission type</span></span>      | <span data-ttu-id="f9e7a-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="f9e7a-111">Permissions</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f9e7a-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f9e7a-112">Delegated (work or school account)</span></span> | <span data-ttu-id="f9e7a-113">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="f9e7a-113">PrivilegedAccess.ReadWrite.AzureResources</span></span>  |
|<span data-ttu-id="f9e7a-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f9e7a-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f9e7a-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f9e7a-115">Not supported.</span></span>    |
|<span data-ttu-id="f9e7a-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f9e7a-116">Application</span></span> | <span data-ttu-id="f9e7a-117">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="f9e7a-117">PrivilegedAccess.ReadWrite.AzureResources</span></span> |

<span data-ttu-id="f9e7a-118">Además el ámbito de permiso, esta API requiere el solicitante tener al menos una asignación de funciones en el recurso, que pertenece el [governanceRoleSetting](../resources/governancerolesetting.md) .</span><span class="sxs-lookup"><span data-stu-id="f9e7a-118">Besides the permission scope, this API requires the requestor to have at least one role assignment on the resource, which the [governanceRoleSetting](../resources/governancerolesetting.md) belongs to.</span></span>
## <a name="http-request"></a><span data-ttu-id="f9e7a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f9e7a-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /privilegedAccess/azureResources/roleSettings/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="f9e7a-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f9e7a-120">Optional query parameters</span></span>
<span data-ttu-id="f9e7a-121">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f9e7a-121">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="f9e7a-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f9e7a-122">Request headers</span></span>
| <span data-ttu-id="f9e7a-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="f9e7a-123">Name</span></span>      |<span data-ttu-id="f9e7a-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9e7a-124">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="f9e7a-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="f9e7a-125">Authorization</span></span>  | <span data-ttu-id="f9e7a-126">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="f9e7a-126">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="f9e7a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f9e7a-127">Request body</span></span>
<span data-ttu-id="f9e7a-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f9e7a-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="f9e7a-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9e7a-129">Response</span></span>
<span data-ttu-id="f9e7a-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [governanceRoleSetting](../resources/governancerolesetting.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f9e7a-130">If successful, this method returns a `200 OK` response code and a [governanceRoleSetting](../resources/governancerolesetting.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="f9e7a-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f9e7a-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f9e7a-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f9e7a-132">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "get_governancerolesetting"
}-->
```http
GET https://graph.microsoft.com/beta/privilegedAccess/azureResources/roleSettings/80dc5d6f-8d89-47b3-953f-01dc909ed3f9
```
##### <a name="response"></a><span data-ttu-id="f9e7a-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9e7a-133">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.governanceRoleSetting"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 370

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#governanceRoleSettings/$entity",
    "id": "80dc5d6f-8d89-47b3-953f-01dc909ed3f9",
    "resourceId": "e5e7d29d-5465-45ac-885f-4716a5ee74b5",
    "roleDefinitionId": "5b8bea96-e9f6-4c63-a8e9-fb092c79f0a1",
    "isDefault": false,
    "lastUpdatedDateTime": "2018-03-26T21:21:43.113Z",
    "lastUpdatedBy": "Vishal Seri",
    "adminEligibleSettings": [
        {
            "ruleIdentifier": "ExpirationRule",
            "setting": "{\"permanentAssignment\":false,\"maximumGrantPeriodInMinutes\":129600}"
        }
    ],
    "adminMemberSettings": [
        {
            "ruleIdentifier": "ExpirationRule",
            "setting": "{\"permanentAssignment\":false,\"maximumGrantPeriodInMinutes\":43200}"
        },
        {
            "ruleIdentifier": "MfaRule",
            "setting": "{\"mfaRequired\":false}"
        },
        {
            "ruleIdentifier": "JustificationRule",
            "setting": "{\"required\":true}"
        }
    ],
    "userEligibleSettings": [],
    "userMemberSettings": [
        {
            "ruleIdentifier": "ExpirationRule",
            "setting": "{\"permanentAssignment\":false,\"maximumGrantPeriodInMinutes\":480}"
        },
        {
            "ruleIdentifier": "MfaRule",
            "setting": "{\"mfaRequired\":false}"
        },
        {
            "ruleIdentifier": "JustificationRule",
            "setting": "{\"required\":true}"
        },
        {
            "ruleIdentifier": "ApprovalRule",
            "setting": "{\"Enabled\":true,\"Approvers\":[{\"Id\":\"20083cf1-b8d8-43be-9d37-96adfb09e619\",\"Type\":\"User\",\"DisplayName\":\"Vishal Seri\",\"Email\":\"viseri@fimdev.net\"},{\"Id\":\"d158e1b0-5080-4088-a1e7-9ca54f39eb53\",\"Type\":\"User\",\"DisplayName\":\"viseri\",\"Email\":\"viseri@microsoft.com\"}],\"BusinessFlowId\":\"8df9e93a-6ba9-4453-af43-07cb95435032\"}"
        }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get governanceRoleSetting",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
