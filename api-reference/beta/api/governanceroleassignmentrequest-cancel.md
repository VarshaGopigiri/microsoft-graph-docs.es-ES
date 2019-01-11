---
title: Cancelar governanceRoleAssignmentRequest
description: Cancelar un governanceRoleAssignmentRequest.
localization_priority: Normal
ms.openlocfilehash: f155a832a0c29935216dbc740e7db6ae8708f429
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27809110"
---
# <a name="cancel-governanceroleassignmentrequest"></a><span data-ttu-id="10c2e-103">Cancelar governanceRoleAssignmentRequest</span><span class="sxs-lookup"><span data-stu-id="10c2e-103">Cancel governanceRoleAssignmentRequest</span></span>

> <span data-ttu-id="10c2e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="10c2e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="10c2e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="10c2e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="10c2e-106">Cancelar un [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md).</span><span class="sxs-lookup"><span data-stu-id="10c2e-106">Cancel a [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="10c2e-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="10c2e-107">Permissions</span></span>
<span data-ttu-id="10c2e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="10c2e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="10c2e-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="10c2e-110">Permission type</span></span>      | <span data-ttu-id="10c2e-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="10c2e-111">Permissions</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="10c2e-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="10c2e-112">Delegated (work or school account)</span></span> | <span data-ttu-id="10c2e-113">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="10c2e-113">PrivilegedAccess.ReadWrite.AzureResources</span></span>  |
|<span data-ttu-id="10c2e-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="10c2e-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="10c2e-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="10c2e-115">Not supported.</span></span>    |
|<span data-ttu-id="10c2e-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="10c2e-116">Application</span></span> | <span data-ttu-id="10c2e-117">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="10c2e-117">PrivilegedAccess.ReadWrite.AzureResources</span></span> |

## <a name="optional-query-parameters"></a><span data-ttu-id="10c2e-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="10c2e-118">Optional query parameters</span></span>
<span data-ttu-id="10c2e-119">Este método **no** admite los [parámetros de consulta de OData](/graph/query-parameters).</span><span class="sxs-lookup"><span data-stu-id="10c2e-119">This method does **not** support [OData Query Parameters](/graph/query-parameters).</span></span>

### <a name="http-request"></a><span data-ttu-id="10c2e-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="10c2e-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /privilegedAccess/azureResources/roleAssignmentRequests/{id}/cancel
```

## <a name="request-headers"></a><span data-ttu-id="10c2e-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="10c2e-121">Request headers</span></span>
| <span data-ttu-id="10c2e-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="10c2e-122">Name</span></span>       | <span data-ttu-id="10c2e-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="10c2e-123">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="10c2e-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="10c2e-124">Authorization</span></span>  | <span data-ttu-id="10c2e-125">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="10c2e-125">Bearer {code}</span></span>|
| <span data-ttu-id="10c2e-126">Tipo de contenido</span><span class="sxs-lookup"><span data-stu-id="10c2e-126">Content-type</span></span>  | <span data-ttu-id="10c2e-127">application/json</span><span class="sxs-lookup"><span data-stu-id="10c2e-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="10c2e-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="10c2e-128">Request body</span></span>
<span data-ttu-id="10c2e-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="10c2e-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="10c2e-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="10c2e-130">Response</span></span>
<span data-ttu-id="10c2e-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 NoContent`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="10c2e-p103">If successful, this method returns `204 NoContent` response code. It does not return anything in the response body.</span></span> 

## <a name="error-codes"></a><span data-ttu-id="10c2e-133">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="10c2e-133">Error codes</span></span>
<span data-ttu-id="10c2e-134">Esta API sigue el estándar de los códigos de HTTP.</span><span class="sxs-lookup"><span data-stu-id="10c2e-134">This API follows the standard of HTTP codes.</span></span> <span data-ttu-id="10c2e-135">Además, se muestran los códigos de error personalizados.</span><span class="sxs-lookup"><span data-stu-id="10c2e-135">Besides, the custom error codes are shown below.</span></span>
|<span data-ttu-id="10c2e-136">Código de error</span><span class="sxs-lookup"><span data-stu-id="10c2e-136">Error code</span></span>     | <span data-ttu-id="10c2e-137">Mensaje de error</span><span class="sxs-lookup"><span data-stu-id="10c2e-137">Error message</span></span>              | <span data-ttu-id="10c2e-138">Detalles</span><span class="sxs-lookup"><span data-stu-id="10c2e-138">Details</span></span> |
|:--------------------| :---------------------|:--------------------|
| <span data-ttu-id="10c2e-139">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="10c2e-139">400 BadRequest</span></span> | <span data-ttu-id="10c2e-140">RoleAssignmentRequestNotFound</span><span class="sxs-lookup"><span data-stu-id="10c2e-140">RoleAssignmentRequestNotFound</span></span> | <span data-ttu-id="10c2e-141">La governanceRoleAssignmentRequest no existe en el sistema.</span><span class="sxs-lookup"><span data-stu-id="10c2e-141">The governanceRoleAssignmentRequest does not exist in system.</span></span>
| <span data-ttu-id="10c2e-142">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="10c2e-142">400 BadRequest</span></span> | <span data-ttu-id="10c2e-143">RequestCannotBeCancelled</span><span class="sxs-lookup"><span data-stu-id="10c2e-143">RequestCannotBeCancelled</span></span>    | <span data-ttu-id="10c2e-144">Sólo se solicita en el estado de `Granted`, `PendingApproval`, `PendingApprovalProvisioning` y `PendingAdminDecision` se puede cancelar.</span><span class="sxs-lookup"><span data-stu-id="10c2e-144">Only requests in status of `Granted`, `PendingApproval`, `PendingApprovalProvisioning` and `PendingAdminDecision` can be cancelled.</span></span>

## <a name="example"></a><span data-ttu-id="10c2e-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="10c2e-145">Example</span></span>
##### <a name="request"></a><span data-ttu-id="10c2e-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="10c2e-146">Request</span></span>
<span data-ttu-id="10c2e-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="10c2e-147">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "cancel_governanceroleassignmentrequest"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedAccess/azureResources/roleAssignmentRequests/7c53453e-d5a4-41e0-8eb1-32d5ec8bfdee/cancel
```

##### <a name="response"></a><span data-ttu-id="10c2e-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="10c2e-148">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.None"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Cancel governanceRoleAssignmentRequest",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
