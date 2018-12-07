---
title: Lista governanceRoleAssignmentRequests
description: 'Recuperar una colección de governanceRoleAssignmentRequests. '
ms.openlocfilehash: 89cb6130b586a44723ec636cbdbe311e0bf8d510
ms.sourcegitcommit: 82f9d0d10388572a3073b2dde8ca0a7b409135b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/07/2018
ms.locfileid: "27191161"
---
# <a name="list-governanceroleassignmentrequests"></a><span data-ttu-id="505b0-103">Lista governanceRoleAssignmentRequests</span><span class="sxs-lookup"><span data-stu-id="505b0-103">List governanceRoleAssignmentRequests</span></span>

> <span data-ttu-id="505b0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="505b0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="505b0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="505b0-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="505b0-106">Recuperar una colección de [governanceRoleAssignmentRequests](../resources/governanceroleassignmentrequest.md).</span><span class="sxs-lookup"><span data-stu-id="505b0-106">Retrieve a collection of [governanceRoleAssignmentRequests](../resources/governanceroleassignmentrequest.md).</span></span> 

## <a name="permissions"></a><span data-ttu-id="505b0-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="505b0-107">Permissions</span></span>
<span data-ttu-id="505b0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="505b0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="505b0-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="505b0-110">Permission type</span></span>      | <span data-ttu-id="505b0-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="505b0-111">Permissions</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="505b0-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="505b0-112">Delegated (work or school account)</span></span> | <span data-ttu-id="505b0-113">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="505b0-113">PrivilegedAccess.ReadWrite.AzureResources</span></span>  |
|<span data-ttu-id="505b0-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="505b0-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="505b0-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="505b0-115">Not supported.</span></span>    |
|<span data-ttu-id="505b0-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="505b0-116">Application</span></span> | <span data-ttu-id="505b0-117">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="505b0-117">PrivilegedAccess.ReadWrite.AzureResources</span></span> |

## <a name="http-request"></a><span data-ttu-id="505b0-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="505b0-118">HTTP request</span></span>
<span data-ttu-id="505b0-119"><!-- { "blockType": "ignored" } -->Una colección de [governanceRoleAssignmentRequests](../resources/governanceroleassignmentrequest.md) en un recurso de la lista.</span><span class="sxs-lookup"><span data-stu-id="505b0-119"><!-- { "blockType": "ignored" } --> List a collection of [governanceRoleAssignmentRequests](../resources/governanceroleassignmentrequest.md) on a resource.</span></span>
    
><span data-ttu-id="505b0-120">**Nota:** Además el ámbito de permiso, la solicitud requiere que el solicitante puede tener al menos una asignación de funciones en el recurso.</span><span class="sxs-lookup"><span data-stu-id="505b0-120">**Note:** Besides the permission scope, the request requires the requestor to have at least one role assignment on the resource.</span></span>

```http
GET /privilegedAccess/azureResources/resources/{resourceId}/roleAssignmentRequests
GET /privilegedAccess/azureResources/roleAssignmentRequests?$filter=resourceId+eq+'{resourceId}'
```
<span data-ttu-id="505b0-121">Lista de una colección de [governanceRoleAssignmentRequests](../resources/governanceroleassignmentrequest.md) mío.</span><span class="sxs-lookup"><span data-stu-id="505b0-121">List a collection of [governanceRoleAssignmentRequests](../resources/governanceroleassignmentrequest.md) of mine.</span></span>

```http
GET /privilegedAccess/azureResources/roleAssignmentRequests?$filter=subjectId+eq+'{myId}'
```

<span data-ttu-id="505b0-122">Una colección de [governanceRoleAssignmentRequests](../resources/governanceroleassignmentrequest.md) que son las decisiones de administrador de la pendiente de la lista.</span><span class="sxs-lookup"><span data-stu-id="505b0-122">List a collection of [governanceRoleAssignmentRequests](../resources/governanceroleassignmentrequest.md) that are pending administrator decisions.</span></span>
    
><span data-ttu-id="505b0-123">**Nota:** El ámbito de permiso, además de esta solicitud requiere que el solicitante puede tener al menos uno `Active` asignación de roles de administrador (`owner` o `user access administrator`) en el recurso.</span><span class="sxs-lookup"><span data-stu-id="505b0-123">**Note:** Besides the permission scope, this request requires the requestor to have at least one `Active` administrator role assignment (`owner` or `user access administrator`) on the resource.</span></span>

```http
GET /privilegedAccess/azureResources/roleAssignmentRequests?$filter=status/subStatus+eq+'PendingAdminDecision'
```

## <a name="optional-query-parameters"></a><span data-ttu-id="505b0-124">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="505b0-124">Optional query parameters</span></span>
<span data-ttu-id="505b0-125">Este método es compatible con los [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="505b0-125">This method supports the [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="505b0-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="505b0-126">Request headers</span></span>
| <span data-ttu-id="505b0-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="505b0-127">Name</span></span>      |<span data-ttu-id="505b0-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="505b0-128">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="505b0-129">Autorización</span><span class="sxs-lookup"><span data-stu-id="505b0-129">Authorization</span></span>  | <span data-ttu-id="505b0-130">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="505b0-130">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="505b0-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="505b0-131">Request body</span></span>
<span data-ttu-id="505b0-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="505b0-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="505b0-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="505b0-133">Response</span></span>
<span data-ttu-id="505b0-134">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="505b0-134">If successful, this method returns a `200 OK` response code and a collection of [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="505b0-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="505b0-135">Example</span></span>
<!-- {
  "blockType": "request",
  "name": "get_governanceroleassignmentrequests"
}-->
<span data-ttu-id="505b0-136">Los administradores consultan las solicitudes de asignación de roles pendiente de suscripción Wingtip Toys - Prod.</span><span class="sxs-lookup"><span data-stu-id="505b0-136">Administrators query pending role assignment requests for subscription Wingtip Toys - Prod.</span></span>
##### <a name="request"></a><span data-ttu-id="505b0-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="505b0-137">Request</span></span>

```http
GET https://graph.microsoft.com/beta/privilegedAccess/azureResources/roleAssignmentRequests?$filter=resourceId+eq+'e5e7d29d-5465-45ac-885f-4716a5ee74b5'
```
##### <a name="response"></a><span data-ttu-id="505b0-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="505b0-138">Response</span></span>
<span data-ttu-id="505b0-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="505b0-139">Here is an example of the response.</span></span> 

><span data-ttu-id="505b0-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="505b0-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.governanceRoleAssignmentRequest",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 279

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#governanceRoleAssignmentRequests",
    "value": [
        {
            "id": "d75c65d8-9e66-44ff-b1cd-1ab0947fde1d",
            "resourceId": "e5e7d29d-5465-45ac-885f-4716a5ee74b5",
            "roleDefinitionId": "8b4d1d51-08e9-4254-b0a6-b16177aae376",
            "subjectId": "918e54be-12c4-4f4c-a6d3-2ee0e3661c51",
            "linkedEligibleRoleAssignmentId": "",
            "type": "UserRemove",
            "assignmentState": "Active",
            "requestedDateTime": "2018-01-09T23:41:34.367Z",
            "reason": "Deactivation request",
            "schedule": null,
            "status": {
                "status": "Closed",
                "subStatus": "Revoked",
                "statusDetails": []
            }
        },
        {
            "id": "38f42071-3e81-4191-8c0b-11450fb6b547",
            "resourceId": "e5e7d29d-5465-45ac-885f-4716a5ee74b5",
            "roleDefinitionId": "8b4d1d51-08e9-4254-b0a6-b16177aae376",
            "subjectId": "918e54be-12c4-4f4c-a6d3-2ee0e3661c51",
            "linkedEligibleRoleAssignmentId": "",
            "type": "UserAdd",
            "assignmentState": "Active",
            "requestedDateTime": "2018-01-10T20:58:09.163Z",
            "reason": "test activations",
            "status": {
                "status": "Closed",
                "subStatus": "Provisioned",
                "statusDetails": [
                    {
                        "key": "EligibilityRule",
                        "value": "Grant"
                    },
                    {
                        "key": "ExpirationRule",
                        "value": "Grant"
                    },
                    {
                        "key": "MfaRule",
                        "value": "Grant"
                    },
                    {
                        "key": "JustificationRule",
                        "value": "Grant"
                    },
                    {
                        "key": "ActivationDayRule",
                        "value": "Grant"
                    },
                    {
                        "key": "ApprovalRule",
                        "value": "Grant"
                    }
                ]
            },
            "schedule": {
                "type": "Once",
                "startDateTime": "2018-01-10T20:58:11.363914Z",
                "endDateTime": "0001-01-01T00:00:00Z",
                "duration": "PT5H"
            }
        },
        ...
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List governanceRoleAssignmentRequests",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
