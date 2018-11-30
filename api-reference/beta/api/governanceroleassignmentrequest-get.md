---
title: Obtener governanceRoleAssignmentRequest
description: 'Obtenga una governanceRoleAssignmentRequest. '
ms.openlocfilehash: 4dca14c081edc9cd3609bd4eab1c79a10953e433
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087721"
---
# <a name="get-governanceroleassignmentrequest"></a><span data-ttu-id="e4fdc-103">Obtener governanceRoleAssignmentRequest</span><span class="sxs-lookup"><span data-stu-id="e4fdc-103">Get governanceRoleAssignmentRequest</span></span>

> <span data-ttu-id="e4fdc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e4fdc-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e4fdc-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e4fdc-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e4fdc-106">Obtenga una [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md).</span><span class="sxs-lookup"><span data-stu-id="e4fdc-106">Get a [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md).</span></span> 

## <a name="permissions"></a><span data-ttu-id="e4fdc-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="e4fdc-107">Permissions</span></span>
<span data-ttu-id="e4fdc-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e4fdc-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e4fdc-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e4fdc-110">Permission type</span></span>      | <span data-ttu-id="e4fdc-111">Permissions</span><span class="sxs-lookup"><span data-stu-id="e4fdc-111">Permissions</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e4fdc-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e4fdc-112">Delegated (work or school account)</span></span> | <span data-ttu-id="e4fdc-113">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="e4fdc-113">PrivilegedAccess.ReadWrite.AzureResources</span></span>  |
|<span data-ttu-id="e4fdc-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e4fdc-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e4fdc-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e4fdc-115">Not supported.</span></span>    |
|<span data-ttu-id="e4fdc-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e4fdc-116">Application</span></span> | <span data-ttu-id="e4fdc-117">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="e4fdc-117">PrivilegedAccess.ReadWrite.AzureResources</span></span> |

<span data-ttu-id="e4fdc-118">Además del ámbito de permiso, requiere el solicitante</span><span class="sxs-lookup"><span data-stu-id="e4fdc-118">Besides the permission scope, it requires the requestor</span></span> 
*   <span data-ttu-id="e4fdc-119">tener al menos una asignación de funciones en el recurso; o</span><span class="sxs-lookup"><span data-stu-id="e4fdc-119">to have at least one role assignment on the resource; or</span></span>
*   <span data-ttu-id="e4fdc-120">es el asunto de la [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md).</span><span class="sxs-lookup"><span data-stu-id="e4fdc-120">is the subject of the [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md).</span></span>

## <a name="http-request"></a><span data-ttu-id="e4fdc-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e4fdc-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /privilegedAccess/azureResources/roleAssignmentRequests/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="e4fdc-122">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e4fdc-122">Optional query parameters</span></span>
<span data-ttu-id="e4fdc-123">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e4fdc-123">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="e4fdc-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e4fdc-124">Request headers</span></span>
| <span data-ttu-id="e4fdc-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="e4fdc-125">Name</span></span>      |<span data-ttu-id="e4fdc-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4fdc-126">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="e4fdc-127">Autorización</span><span class="sxs-lookup"><span data-stu-id="e4fdc-127">Authorization</span></span>  | <span data-ttu-id="e4fdc-128">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="e4fdc-128">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="e4fdc-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e4fdc-129">Request body</span></span>
<span data-ttu-id="e4fdc-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e4fdc-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e4fdc-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e4fdc-131">Response</span></span>
<span data-ttu-id="e4fdc-132">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e4fdc-132">If successful, this method returns a `200 OK` response code and a [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e4fdc-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e4fdc-133">Example</span></span>
<span data-ttu-id="e4fdc-134">Obtener una solicitud de asignación de rol</span><span class="sxs-lookup"><span data-stu-id="e4fdc-134">Get a role assignment request</span></span>
<!-- {
  "blockType": "request",
  "name": "get_governanceroleassignmentrequest"
}-->
##### <a name="request"></a><span data-ttu-id="e4fdc-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e4fdc-135">Request</span></span>

```http
GET https://graph.microsoft.com/beta/privilegedAccess/azureResources/roleAssignmentRequests/e68ff888-4af5-4ccb-8b74-39156090344b
```
##### <a name="response"></a><span data-ttu-id="e4fdc-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e4fdc-136">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.governanceRoleAssignmentRequest"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 279

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#governanceRoleAssignmentRequests/$entity",
  "id":"e68ff888-4af5-4ccb-8b74-39156090344b",
  "resourceId":"ec3a00f7-81dc-43b3-bbe7-650d3a5f7d46",
  "roleDefinitionId":"be0767b9-2c31-4b0d-b820-726228e7ff5c",
  "subjectId":"a4c5a837-b546-4ec5-a7df-e61547a46a4b",
  "linkedEligibleRoleAssignmentId":"",
  "type":"AdminRemove",
  "assignmentState":"Eligible",
  "requestedDateTime":"2018-05-09T21:26:15.73-07:00",
  "roleAssignmentStartDateTime":null,
  "roleAssignmentEndDateTime":null,
  "reason":null,
  "status":{
    "status":"Closed",
    "subStatus":"Revoked",
    "statusDetails":[]
  },
  "schedule":null
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get governanceRoleAssignmentRequest",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->