---
title: Obtener governanceRoleAssignmentRequest
description: 'Obtenga una governanceRoleAssignmentRequest. '
localization_priority: Normal
ms.openlocfilehash: 190e79787b32e7e21e9d321ee6f3d90dc27605ea
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27887454"
---
# <a name="get-governanceroleassignmentrequest"></a><span data-ttu-id="f927c-103">Obtener governanceRoleAssignmentRequest</span><span class="sxs-lookup"><span data-stu-id="f927c-103">Get governanceRoleAssignmentRequest</span></span>

> <span data-ttu-id="f927c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f927c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f927c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f927c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f927c-106">Obtenga una [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md).</span><span class="sxs-lookup"><span data-stu-id="f927c-106">Get a [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md).</span></span> 

## <a name="permissions"></a><span data-ttu-id="f927c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="f927c-107">Permissions</span></span>
<span data-ttu-id="f927c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f927c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f927c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f927c-110">Permission type</span></span>      | <span data-ttu-id="f927c-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="f927c-111">Permissions</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f927c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f927c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="f927c-113">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="f927c-113">PrivilegedAccess.ReadWrite.AzureResources</span></span>  |
|<span data-ttu-id="f927c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f927c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f927c-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f927c-115">Not supported.</span></span>    |
|<span data-ttu-id="f927c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f927c-116">Application</span></span> | <span data-ttu-id="f927c-117">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="f927c-117">PrivilegedAccess.ReadWrite.AzureResources</span></span> |

<span data-ttu-id="f927c-118">Además del ámbito de permiso, requiere el solicitante</span><span class="sxs-lookup"><span data-stu-id="f927c-118">Besides the permission scope, it requires the requestor</span></span> 
*   <span data-ttu-id="f927c-119">tener al menos una asignación de funciones en el recurso; o</span><span class="sxs-lookup"><span data-stu-id="f927c-119">to have at least one role assignment on the resource; or</span></span>
*   <span data-ttu-id="f927c-120">es el asunto de la [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md).</span><span class="sxs-lookup"><span data-stu-id="f927c-120">is the subject of the [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md).</span></span>

## <a name="http-request"></a><span data-ttu-id="f927c-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f927c-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /privilegedAccess/azureResources/roleAssignmentRequests/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="f927c-122">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f927c-122">Optional query parameters</span></span>
<span data-ttu-id="f927c-123">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f927c-123">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="f927c-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f927c-124">Request headers</span></span>
| <span data-ttu-id="f927c-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="f927c-125">Name</span></span>      |<span data-ttu-id="f927c-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="f927c-126">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="f927c-127">Autorización</span><span class="sxs-lookup"><span data-stu-id="f927c-127">Authorization</span></span>  | <span data-ttu-id="f927c-128">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="f927c-128">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="f927c-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f927c-129">Request body</span></span>
<span data-ttu-id="f927c-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f927c-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f927c-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f927c-131">Response</span></span>
<span data-ttu-id="f927c-132">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f927c-132">If successful, this method returns a `200 OK` response code and a [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f927c-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f927c-133">Example</span></span>
<span data-ttu-id="f927c-134">Obtener una solicitud de asignación de rol</span><span class="sxs-lookup"><span data-stu-id="f927c-134">Get a role assignment request</span></span>
<!-- {
  "blockType": "request",
  "name": "get_governanceroleassignmentrequest"
}-->
##### <a name="request"></a><span data-ttu-id="f927c-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f927c-135">Request</span></span>

```http
GET https://graph.microsoft.com/beta/privilegedAccess/azureResources/roleAssignmentRequests/e68ff888-4af5-4ccb-8b74-39156090344b
```
##### <a name="response"></a><span data-ttu-id="f927c-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f927c-136">Response</span></span>
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
