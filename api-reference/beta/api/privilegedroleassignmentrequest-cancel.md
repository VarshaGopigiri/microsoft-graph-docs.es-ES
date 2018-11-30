---
title: Cancelar privilegedRoleAssignmentRequest
description: Cancelar un privilegedRoleAssignmentRequest.
ms.openlocfilehash: 99c1102235e93ca365dcdd0e619bcceac9f396f1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087871"
---
# <a name="cancel-privilegedroleassignmentrequest"></a><span data-ttu-id="137d0-103">Cancelar privilegedRoleAssignmentRequest</span><span class="sxs-lookup"><span data-stu-id="137d0-103">Cancel privilegedRoleAssignmentRequest</span></span>

> <span data-ttu-id="137d0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="137d0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="137d0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="137d0-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="137d0-106">Cancelar un [privilegedRoleAssignmentRequest](../resources/privilegedroleassignmentrequest.md).</span><span class="sxs-lookup"><span data-stu-id="137d0-106">Cancel a [privilegedRoleAssignmentRequest](../resources/privilegedroleassignmentrequest.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="137d0-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="137d0-107">Permissions</span></span>
<span data-ttu-id="137d0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="137d0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="137d0-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="137d0-110">Permission type</span></span>                        | <span data-ttu-id="137d0-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="137d0-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="137d0-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="137d0-112">Delegated (work or school account)</span></span> | <span data-ttu-id="137d0-113">PrivilegedAccess.ReadWrite.AzureAD, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="137d0-113">PrivilegedAccess.ReadWrite.AzureAD, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="137d0-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="137d0-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="137d0-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="137d0-115">Not supported.</span></span> |
|<span data-ttu-id="137d0-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="137d0-116">Application</span></span>                            | <span data-ttu-id="137d0-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="137d0-117">Not supported.</span></span> |


### <a name="http-request"></a><span data-ttu-id="137d0-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="137d0-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /privilegedRoleAssignmentRequests({requestid})/cancel
```

## <a name="request-headers"></a><span data-ttu-id="137d0-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="137d0-119">Request headers</span></span>
| <span data-ttu-id="137d0-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="137d0-120">Name</span></span>      |<span data-ttu-id="137d0-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="137d0-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="137d0-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="137d0-122">Authorization</span></span>  | <span data-ttu-id="137d0-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="137d0-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="137d0-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="137d0-125">Request body</span></span>
<span data-ttu-id="137d0-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="137d0-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="137d0-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="137d0-127">Response</span></span>
<span data-ttu-id="137d0-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 Ok`.</span><span class="sxs-lookup"><span data-stu-id="137d0-128">If successful, this method returns a `200 Ok` response code.</span></span> <span data-ttu-id="137d0-129">Devuelve [privilegedRoleAssignmentRequest] (.. / resources/privilegedRoleAssignmentRequest.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="137d0-129">It returns [privilegedRoleAssignmentRequest] (../resources/privilegedRoleAssignmentRequest.md) in the response body.</span></span>

### <a name="error-codes"></a><span data-ttu-id="137d0-130">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="137d0-130">Error codes</span></span>
<span data-ttu-id="137d0-131">Esta API devuelve los códigos de error HTTP estándares.</span><span class="sxs-lookup"><span data-stu-id="137d0-131">This API returns the standard HTTP error codes.</span></span> <span data-ttu-id="137d0-132">Además, devuelve los códigos de error personalizados que aparecen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="137d0-132">In addition, it returns the custom error codes listed in the following table.</span></span>

|<span data-ttu-id="137d0-133">Código de error</span><span class="sxs-lookup"><span data-stu-id="137d0-133">Error code</span></span>     | <span data-ttu-id="137d0-134">Mensaje de error</span><span class="sxs-lookup"><span data-stu-id="137d0-134">Error message</span></span>              |
|:--------------------| :---------------------|
| <span data-ttu-id="137d0-135">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="137d0-135">400 BadRequest</span></span> | <span data-ttu-id="137d0-136">RequestId no puede ser Null.</span><span class="sxs-lookup"><span data-stu-id="137d0-136">RequestId cannot be Null.</span></span> |
| <span data-ttu-id="137d0-137">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="137d0-137">400 BadRequest</span></span> | <span data-ttu-id="137d0-138">Solicitar con el identificador de la solicitud no se ha encontrado.</span><span class="sxs-lookup"><span data-stu-id="137d0-138">Request with request ID not found.</span></span> |
| <span data-ttu-id="137d0-139">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="137d0-139">400 BadRequest</span></span> | <span data-ttu-id="137d0-140">Cancelación puede realizarse sólo en estado programadas y pendiente de aprobación.</span><span class="sxs-lookup"><span data-stu-id="137d0-140">Cancellation can be done only on status Scheduled and PendingApproval.</span></span> |
| <span data-ttu-id="137d0-141">403 no autorizado</span><span class="sxs-lookup"><span data-stu-id="137d0-141">403 UnAuthorized</span></span> | <span data-ttu-id="137d0-142">Solicitante no puedo realizar llamadas de cancelar o la solicitud que no se ha encontrado.</span><span class="sxs-lookup"><span data-stu-id="137d0-142">Requester not allowed to make Cancel call or request not found.</span></span> |

## <a name="example"></a><span data-ttu-id="137d0-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="137d0-143">Example</span></span>
##### <a name="request"></a><span data-ttu-id="137d0-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="137d0-144">Request</span></span>
<span data-ttu-id="137d0-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="137d0-145">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "cancel_privilegedRoleAssignmentRequests"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedRoleAssignmentRequests('7c53453e-d5a4-41e0-8eb1-32d5ec8bfdee')/cancel
```

##### <a name="response"></a><span data-ttu-id="137d0-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="137d0-146">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.privilegedRoleAssignmentRequests"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 304

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#privilegedRoleAssignmentRequests/$entity",
    "schedule": {
        "type": "activation",
        "startDateTime": "2018-02-08T02:35:17.903Z",
        "endDateTime": null,
        "duration" : null
    },
    "id": "bcfb11e3-fc0d-49ea-b3d5-7d60a48e5043",
    "evaluateOnly": false,
    "type": "UserAdd",
    "assignmentState": "Active",
    "requestedDateTime": "2018-02-08T02:35:42.9137335Z",
    "status": "Cancelling",
    "duration": "2",
    "reason": "Activate the role for business purpose",
    "ticketNumber": "234",
    "ticketSystem": "system",
    "userId": "Self"，
    "roleId": "88d8e3e3-8f55-4a1e-953a-9b9898b8876b"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Cancel privilegedRoleAssignmentRequests",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->