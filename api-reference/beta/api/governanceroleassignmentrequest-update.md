---
title: Actualizar governanceRoleAssignmentRequests
description: Permiten a los administradores actualizar sus decisiones (`AdminApproved` o `AdminDenied`) en governanceRoleAssignmentRequests que se encuentran en estado de `PendingAdminDecision`.
localization_priority: Normal
ms.openlocfilehash: 3d68e06688922177e2a1a183a9fe4bfc6be6a91d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27874938"
---
# <a name="update-governanceroleassignmentrequests"></a><span data-ttu-id="dd444-103">Actualizar governanceRoleAssignmentRequests</span><span class="sxs-lookup"><span data-stu-id="dd444-103">Update governanceRoleAssignmentRequests</span></span>

> <span data-ttu-id="dd444-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dd444-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dd444-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dd444-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="dd444-106">Permiten a los administradores actualizar sus decisiones (`AdminApproved` o `AdminDenied`) en [governanceRoleAssignmentRequests](../resources/governanceroleassignmentrequest.md) que se encuentran en estado de `PendingAdminDecision`.</span><span class="sxs-lookup"><span data-stu-id="dd444-106">Enable administrators to update their decisions (`AdminApproved` or `AdminDenied`) on [governanceRoleAssignmentRequests](../resources/governanceroleassignmentrequest.md) that are in status of `PendingAdminDecision`.</span></span>

## <a name="permissions"></a><span data-ttu-id="dd444-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="dd444-107">Permissions</span></span>
<span data-ttu-id="dd444-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dd444-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

><span data-ttu-id="dd444-110">**Nota:** Esta API también requiere que el solicitante tiene al menos una `Active` asignación de roles de administrador (`owner` o `user access administrator`) en el recurso al que pertenece el [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) .</span><span class="sxs-lookup"><span data-stu-id="dd444-110">**Note:** This API also requires that the requester have at least one `Active` adminstrator role assignment (`owner` or `user access administrator`) on the resource that the [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) belongs to.</span></span> 

|<span data-ttu-id="dd444-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dd444-111">Permission type</span></span>      | <span data-ttu-id="dd444-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="dd444-112">Permissions</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="dd444-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dd444-113">Delegated (work or school account)</span></span> | <span data-ttu-id="dd444-114">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="dd444-114">PrivilegedAccess.ReadWrite.AzureResources</span></span>  |
|<span data-ttu-id="dd444-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dd444-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dd444-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dd444-116">Not supported.</span></span>    |
|<span data-ttu-id="dd444-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dd444-117">Application</span></span> | <span data-ttu-id="dd444-118">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="dd444-118">PrivilegedAccess.ReadWrite.AzureResources</span></span> |

## <a name="http-request"></a><span data-ttu-id="dd444-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dd444-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /privilegedAccess/azureResources/roleAssignmentRequests/{id}/updateRequest   
```

## <a name="request-headers"></a><span data-ttu-id="dd444-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dd444-120">Request headers</span></span>
| <span data-ttu-id="dd444-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="dd444-121">Name</span></span>           | <span data-ttu-id="dd444-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd444-122">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="dd444-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="dd444-123">Authorization</span></span>  | <span data-ttu-id="dd444-124">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="dd444-124">Bearer {code}</span></span>|
| <span data-ttu-id="dd444-125">Tipo de contenido</span><span class="sxs-lookup"><span data-stu-id="dd444-125">Content-type</span></span>  | <span data-ttu-id="dd444-126">application/json</span><span class="sxs-lookup"><span data-stu-id="dd444-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="dd444-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dd444-127">Request body</span></span>

|<span data-ttu-id="dd444-128">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd444-128">Parameters</span></span>      |<span data-ttu-id="dd444-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="dd444-129">Type</span></span>                   |<span data-ttu-id="dd444-130">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="dd444-130">Required</span></span> |<span data-ttu-id="dd444-131">Description</span><span class="sxs-lookup"><span data-stu-id="dd444-131">Description</span></span>|
|:-------------|:----------------------|:--------|:----------|
|<span data-ttu-id="dd444-132">motivo</span><span class="sxs-lookup"><span data-stu-id="dd444-132">reason</span></span>        |<span data-ttu-id="dd444-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="dd444-133">String</span></span>                 |<span data-ttu-id="dd444-134">✓</span><span class="sxs-lookup"><span data-stu-id="dd444-134">✓</span></span>        |<span data-ttu-id="dd444-135">El motivo por el Administrador de su decisión.</span><span class="sxs-lookup"><span data-stu-id="dd444-135">The reason provided by the administrator for his decision.</span></span>|
|<span data-ttu-id="dd444-136">toma de decisiones</span><span class="sxs-lookup"><span data-stu-id="dd444-136">decision</span></span>        |<span data-ttu-id="dd444-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="dd444-137">String</span></span>                 |<span data-ttu-id="dd444-138">✓</span><span class="sxs-lookup"><span data-stu-id="dd444-138">✓</span></span>        |<span data-ttu-id="dd444-139">La Decisión del Administrador de la solicitud de asignación de rol.</span><span class="sxs-lookup"><span data-stu-id="dd444-139">The administrator decision of the role assignment request.</span></span> <span data-ttu-id="dd444-140">El valor debe actualizarse como `AdminApproved` o `AdminDenied`.</span><span class="sxs-lookup"><span data-stu-id="dd444-140">The value should be updated as `AdminApproved` or `AdminDenied`.</span></span>|
|<span data-ttu-id="dd444-141">programación</span><span class="sxs-lookup"><span data-stu-id="dd444-141">schedule</span></span>      |[<span data-ttu-id="dd444-142">governanceSchedule</span><span class="sxs-lookup"><span data-stu-id="dd444-142">governanceSchedule</span></span>](../resources/governanceschedule.md)|        | <span data-ttu-id="dd444-143">La programación de la solicitud de asignación de rol.</span><span class="sxs-lookup"><span data-stu-id="dd444-143">The schedule of the role assignment request.</span></span> <span data-ttu-id="dd444-144">Para el estado de `AdminApproved`, es necesario.</span><span class="sxs-lookup"><span data-stu-id="dd444-144">For status of `AdminApproved`, it is required.</span></span>|
|<span data-ttu-id="dd444-145">assignmentState</span><span class="sxs-lookup"><span data-stu-id="dd444-145">assignmentState</span></span>      |<span data-ttu-id="dd444-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="dd444-146">String</span></span>|         | <span data-ttu-id="dd444-147">Puede ser el estado de asignación y los valores `Eligible` o `Active`.</span><span class="sxs-lookup"><span data-stu-id="dd444-147">The state of assignment, and the values can be `Eligible` or `Active`.</span></span> <span data-ttu-id="dd444-148">Para la toma de decisiones de `AdminApproved`, es necesario.</span><span class="sxs-lookup"><span data-stu-id="dd444-148">For decision of `AdminApproved`, it is required.</span></span> |
### <a name="response"></a><span data-ttu-id="dd444-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dd444-149">Response</span></span>
<span data-ttu-id="dd444-150">Este método sólo se puede aplicar a las solicitudes que se encuentran en estado de `PendingAdminDecision`.</span><span class="sxs-lookup"><span data-stu-id="dd444-150">This method can only be applied to requests that are in status of `PendingAdminDecision`.</span></span>

<span data-ttu-id="dd444-p106">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dd444-p106">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="dd444-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dd444-153">Example</span></span>
##### <a name="request"></a><span data-ttu-id="dd444-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dd444-154">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "updaterequest_governanceroleassignmentrequest"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedAccess/azureResources/roleAssignmentRequests/7c53453e-d5a4-41e0-8eb1-32d5ec8bfdee/updateRequest
```
##### <a name="request-body"></a><span data-ttu-id="dd444-155">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dd444-155">Request body</span></span>
```json
{
  "reason":"approve the request to extend role assignment",
  "schedule":{
    "type":"Once",
    "startDateTime":"2018-02-20T07:31:13.451Z",
    "stopDateTime":"2018-05-21T07:31:13.451Z",
    },
  "decision":"AdminApproved",
  "assignmentState": "Eligible"
}
```

##### <a name="response"></a><span data-ttu-id="dd444-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dd444-156">Response</span></span>
<!-- {
  "blockType": "response",
  "@odata.type": "microsoft.graph.None"
} -->
```http
HTTP/1.1 204 No Content
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "UpdateRequest governanceRoleAssignmentRequest",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
