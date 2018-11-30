---
title: Crear governanceRoleAssignmentRequest
description: Cree una solicitud de asignación de rol para representar la operación que desee en una asignación de roles. En la siguiente tabla se enumera las operaciones.
ms.openlocfilehash: b0d9edab1182d4a6fa620cfb953df1cb8af20c66
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086018"
---
# <a name="create-governanceroleassignmentrequest"></a><span data-ttu-id="16b63-104">Crear governanceRoleAssignmentRequest</span><span class="sxs-lookup"><span data-stu-id="16b63-104">Create governanceRoleAssignmentRequest</span></span>

> <span data-ttu-id="16b63-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="16b63-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="16b63-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="16b63-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="16b63-107">Cree una solicitud de asignación de rol para representar la operación que desee en una asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="16b63-107">Create a role assignment request to represent the operation you want on a role assignment.</span></span> <span data-ttu-id="16b63-108">En la siguiente tabla se enumera las operaciones.</span><span class="sxs-lookup"><span data-stu-id="16b63-108">The following table lists the operations.</span></span>

| <span data-ttu-id="16b63-109">Operación</span><span class="sxs-lookup"><span data-stu-id="16b63-109">Operation</span></span>       | <span data-ttu-id="16b63-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="16b63-110">Type</span></span> | 
|:---------------|:----------|
| <span data-ttu-id="16b63-111">Asignar una asignación de roles</span><span class="sxs-lookup"><span data-stu-id="16b63-111">Assign a role assignment</span></span>| <span data-ttu-id="16b63-112">AdminAdd</span><span class="sxs-lookup"><span data-stu-id="16b63-112">AdminAdd</span></span> |
| <span data-ttu-id="16b63-113">Activar una asignación de rol optan</span><span class="sxs-lookup"><span data-stu-id="16b63-113">Activate an eligible role assignment</span></span>| <span data-ttu-id="16b63-114">Comandos UserAdd</span><span class="sxs-lookup"><span data-stu-id="16b63-114">UserAdd</span></span> | 
| <span data-ttu-id="16b63-115">Desactivación de una asignación de rol activada</span><span class="sxs-lookup"><span data-stu-id="16b63-115">Deactivate an activated role assignment</span></span>| <span data-ttu-id="16b63-116">UserRemove</span><span class="sxs-lookup"><span data-stu-id="16b63-116">UserRemove</span></span> | 
| <span data-ttu-id="16b63-117">Quitar una asignación de roles</span><span class="sxs-lookup"><span data-stu-id="16b63-117">Remove a role assignment</span></span>| <span data-ttu-id="16b63-118">AdminRemove</span><span class="sxs-lookup"><span data-stu-id="16b63-118">AdminRemove</span></span> |
| <span data-ttu-id="16b63-119">Actualizar una asignación de roles</span><span class="sxs-lookup"><span data-stu-id="16b63-119">Update a role assignment</span></span>| <span data-ttu-id="16b63-120">AdminUpdate</span><span class="sxs-lookup"><span data-stu-id="16b63-120">AdminUpdate</span></span> |
| <span data-ttu-id="16b63-121">Solicitud para ampliar la asignación de roles</span><span class="sxs-lookup"><span data-stu-id="16b63-121">Request to extend my role assignment</span></span>| <span data-ttu-id="16b63-122">UserExtend</span><span class="sxs-lookup"><span data-stu-id="16b63-122">UserExtend</span></span> | 
| <span data-ttu-id="16b63-123">Extender una asignación de roles</span><span class="sxs-lookup"><span data-stu-id="16b63-123">Extend a role assignment</span></span>| <span data-ttu-id="16b63-124">AdminExtend</span><span class="sxs-lookup"><span data-stu-id="16b63-124">AdminExtend</span></span> | 
| <span data-ttu-id="16b63-125">Solicitud para renovar la asignación de rol que han expirado</span><span class="sxs-lookup"><span data-stu-id="16b63-125">Request to renew my expired role assignment</span></span>| <span data-ttu-id="16b63-126">UserRenew</span><span class="sxs-lookup"><span data-stu-id="16b63-126">UserRenew</span></span> | 
| <span data-ttu-id="16b63-127">Renovar una asignación de rol que han expirado</span><span class="sxs-lookup"><span data-stu-id="16b63-127">Renew an expired role assignment</span></span>| <span data-ttu-id="16b63-128">AdminRenew</span><span class="sxs-lookup"><span data-stu-id="16b63-128">AdminRenew</span></span> | 

 
## <a name="permissions"></a><span data-ttu-id="16b63-129">Permisos</span><span class="sxs-lookup"><span data-stu-id="16b63-129">Permissions</span></span>
<span data-ttu-id="16b63-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="16b63-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="16b63-132">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="16b63-132">Permission type</span></span>      | <span data-ttu-id="16b63-133">Permissions</span><span class="sxs-lookup"><span data-stu-id="16b63-133">Permissions</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="16b63-134">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="16b63-134">Delegated (work or school account)</span></span> | <span data-ttu-id="16b63-135">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="16b63-135">PrivilegedAccess.ReadWrite.AzureResources</span></span>  |
|<span data-ttu-id="16b63-136">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="16b63-136">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="16b63-137">No admitida.</span><span class="sxs-lookup"><span data-stu-id="16b63-137">Not supported.</span></span>    |
|<span data-ttu-id="16b63-138">Aplicación</span><span class="sxs-lookup"><span data-stu-id="16b63-138">Application</span></span> | <span data-ttu-id="16b63-139">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="16b63-139">PrivilegedAccess.ReadWrite.AzureResources</span></span> |

## <a name="http-request"></a><span data-ttu-id="16b63-140">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="16b63-140">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /privilegedAccess/azureResources/roleAssignmentRequests
```

## <a name="optional-query-parameters"></a><span data-ttu-id="16b63-141">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="16b63-141">Optional query parameters</span></span>
<span data-ttu-id="16b63-142">Este método no **no** hay compatibilidad con [los parámetros de consulta de OData](/graph/query-parameters).</span><span class="sxs-lookup"><span data-stu-id="16b63-142">This method does **not** support [OData query parameters](/graph/query-parameters).</span></span>

### <a name="request-headers"></a><span data-ttu-id="16b63-143">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="16b63-143">Request headers</span></span>
| <span data-ttu-id="16b63-144">Nombre</span><span class="sxs-lookup"><span data-stu-id="16b63-144">Name</span></span>       | <span data-ttu-id="16b63-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="16b63-145">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="16b63-146">Autorización</span><span class="sxs-lookup"><span data-stu-id="16b63-146">Authorization</span></span>  | <span data-ttu-id="16b63-147">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="16b63-147">Bearer {code}</span></span>|
| <span data-ttu-id="16b63-148">Tipo de contenido</span><span class="sxs-lookup"><span data-stu-id="16b63-148">Content-type</span></span>  | <span data-ttu-id="16b63-149">application/json</span><span class="sxs-lookup"><span data-stu-id="16b63-149">application/json</span></span>|

### <a name="request-body"></a><span data-ttu-id="16b63-150">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="16b63-150">Request body</span></span>
<span data-ttu-id="16b63-151">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) .</span><span class="sxs-lookup"><span data-stu-id="16b63-151">In the request body, supply a JSON representation of [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) object.</span></span> 

| <span data-ttu-id="16b63-152">Propiedad</span><span class="sxs-lookup"><span data-stu-id="16b63-152">Property</span></span>     | <span data-ttu-id="16b63-153">Tipo</span><span class="sxs-lookup"><span data-stu-id="16b63-153">Type</span></span>    |<span data-ttu-id="16b63-154">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="16b63-154">Required</span></span>|  <span data-ttu-id="16b63-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="16b63-155">Description</span></span>|
|:---------------|:--------|:----------|:----------|
|<span data-ttu-id="16b63-156">resourceId</span><span class="sxs-lookup"><span data-stu-id="16b63-156">resourceId</span></span>|<span data-ttu-id="16b63-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-157">String</span></span>|<span data-ttu-id="16b63-158">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-158">Yes</span></span>|<span data-ttu-id="16b63-159">El identificador del recurso.</span><span class="sxs-lookup"><span data-stu-id="16b63-159">The ID of the resource.</span></span>|
|<span data-ttu-id="16b63-160">roleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="16b63-160">roleDefinitionId</span></span>|<span data-ttu-id="16b63-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-161">String</span></span>|<span data-ttu-id="16b63-162">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-162">Yes</span></span>|<span data-ttu-id="16b63-163">El identificador de la definición de roles.</span><span class="sxs-lookup"><span data-stu-id="16b63-163">The ID of the role definition.</span></span>|
|<span data-ttu-id="16b63-164">///SubjectID</span><span class="sxs-lookup"><span data-stu-id="16b63-164">subjectId</span></span>|<span data-ttu-id="16b63-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-165">String</span></span>|<span data-ttu-id="16b63-166">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-166">Yes</span></span>|<span data-ttu-id="16b63-167">El identificador del tema.</span><span class="sxs-lookup"><span data-stu-id="16b63-167">The ID of the subject.</span></span>|
|<span data-ttu-id="16b63-168">assignmentState</span><span class="sxs-lookup"><span data-stu-id="16b63-168">assignmentState</span></span>|<span data-ttu-id="16b63-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-169">String</span></span>|<span data-ttu-id="16b63-170">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-170">Yes</span></span>|<span data-ttu-id="16b63-171">El estado de asignación.</span><span class="sxs-lookup"><span data-stu-id="16b63-171">The state of assignment.</span></span> <span data-ttu-id="16b63-172">El valor puede ser ``Eligible`` y ``Active``.</span><span class="sxs-lookup"><span data-stu-id="16b63-172">The value can be ``Eligible`` and ``Active``.</span></span>|
|<span data-ttu-id="16b63-173">type</span><span class="sxs-lookup"><span data-stu-id="16b63-173">type</span></span>|<span data-ttu-id="16b63-174">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-174">String</span></span>|<span data-ttu-id="16b63-175">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-175">Yes</span></span>|<span data-ttu-id="16b63-176">El tipo de solicitud.</span><span class="sxs-lookup"><span data-stu-id="16b63-176">The request type.</span></span> <span data-ttu-id="16b63-177">El valor puede ser `AdminAdd`, `UserAdd`, `AdminUpdate`, `AdminRemove`, `UserRemove`, `UserExtend`, `UserRenew`, `AdminRenew`y `AdminExtend`.</span><span class="sxs-lookup"><span data-stu-id="16b63-177">The value can be `AdminAdd`, `UserAdd`, `AdminUpdate`, `AdminRemove`, `UserRemove`, `UserExtend`, `UserRenew`, `AdminRenew`and `AdminExtend`.</span></span>|
|<span data-ttu-id="16b63-178">motivo</span><span class="sxs-lookup"><span data-stu-id="16b63-178">reason</span></span>|<span data-ttu-id="16b63-179">String</span><span class="sxs-lookup"><span data-stu-id="16b63-179">String</span></span>| |<span data-ttu-id="16b63-180">Necesita la razón por la que se proporcionará para la solicitud de asignación de rol para auditoría y revise el propósito.</span><span class="sxs-lookup"><span data-stu-id="16b63-180">The reason needs to be provided for the role assignment request for audit and review purpose.</span></span>|
|<span data-ttu-id="16b63-181">programación</span><span class="sxs-lookup"><span data-stu-id="16b63-181">schedule</span></span>|[<span data-ttu-id="16b63-182">governanceSchedule</span><span class="sxs-lookup"><span data-stu-id="16b63-182">governanceSchedule</span></span>](../resources/governanceschedule.md)| | <span data-ttu-id="16b63-183">La programación de la solicitud de asignación de rol.</span><span class="sxs-lookup"><span data-stu-id="16b63-183">The schedule of the role assignment request.</span></span> <span data-ttu-id="16b63-184">Para tipo de solicitud de `UserAdd`, `AdminAdd`, `AdminUpdate`, y `AdminExtend`, es necesario.</span><span class="sxs-lookup"><span data-stu-id="16b63-184">For request type of `UserAdd`, `AdminAdd`, `AdminUpdate`, and `AdminExtend`, it is required.</span></span>|

### <a name="response"></a><span data-ttu-id="16b63-185">Respuesta</span><span class="sxs-lookup"><span data-stu-id="16b63-185">Response</span></span>
<span data-ttu-id="16b63-186">Si tiene éxito, este método devuelve una `201, Created` código de respuesta y un objeto [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="16b63-186">If successful, this method returns a `201, Created` response code and a [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) object in the response body.</span></span>

## <a name="error-codes"></a><span data-ttu-id="16b63-187">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="16b63-187">Error codes</span></span>
<span data-ttu-id="16b63-188">Esta API sigue el estándar de los códigos de HTTP, además de los códigos de error que aparecen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="16b63-188">This API follows the standard of HTTP codes, in addition to the error codes listed in the following table.</span></span>

|<span data-ttu-id="16b63-189">Código de error</span><span class="sxs-lookup"><span data-stu-id="16b63-189">Error code</span></span>     | <span data-ttu-id="16b63-190">Mensaje de error</span><span class="sxs-lookup"><span data-stu-id="16b63-190">Error message</span></span>              | <span data-ttu-id="16b63-191">Detalles</span><span class="sxs-lookup"><span data-stu-id="16b63-191">Details</span></span> |
|:--------------------| :---------------------|:--------------------|
| <span data-ttu-id="16b63-192">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="16b63-192">400 BadRequest</span></span> | <span data-ttu-id="16b63-193">RoleNotFound</span><span class="sxs-lookup"><span data-stu-id="16b63-193">RoleNotFound</span></span>    | <span data-ttu-id="16b63-194">El `roleDefinitionId` proporcionado en la solicitud no se encuentra el cuerpo.</span><span class="sxs-lookup"><span data-stu-id="16b63-194">The `roleDefinitionId` provided in the request body cannot be found.</span></span>
| <span data-ttu-id="16b63-195">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="16b63-195">400 BadRequest</span></span> | <span data-ttu-id="16b63-196">ResourceIsLocked</span><span class="sxs-lookup"><span data-stu-id="16b63-196">ResourceIsLocked</span></span>    | <span data-ttu-id="16b63-197">El recurso proporcionado en el cuerpo de la solicitud se encuentra en estado de `Locked` y no se puede crear solicitudes de asignación de rol.</span><span class="sxs-lookup"><span data-stu-id="16b63-197">The resource provided in the request body is in state of `Locked` and cannot create role assignment requests.</span></span>
| <span data-ttu-id="16b63-198">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="16b63-198">400 BadRequest</span></span> | <span data-ttu-id="16b63-199">SubjectNotFound</span><span class="sxs-lookup"><span data-stu-id="16b63-199">SubjectNotFound</span></span>    | <span data-ttu-id="16b63-200">El `subjectId` proporcionado en la solicitud no se encuentra el cuerpo.</span><span class="sxs-lookup"><span data-stu-id="16b63-200">The `subjectId` provided in the request body cannot be found.</span></span>
| <span data-ttu-id="16b63-201">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="16b63-201">400 BadRequest</span></span> | <span data-ttu-id="16b63-202">PendingRoleAssignmentRequest</span><span class="sxs-lookup"><span data-stu-id="16b63-202">PendingRoleAssignmentRequest</span></span>    | <span data-ttu-id="16b63-203">Ya existe una pendiente [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) en el sistema.</span><span class="sxs-lookup"><span data-stu-id="16b63-203">There already exists a pending [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) in the system.</span></span>
| <span data-ttu-id="16b63-204">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="16b63-204">400 BadRequest</span></span> | <span data-ttu-id="16b63-205">RoleAssignmentExists</span><span class="sxs-lookup"><span data-stu-id="16b63-205">RoleAssignmentExists</span></span>    | <span data-ttu-id="16b63-206">El [governanceRoleAssignment](../resources/governanceroleassignment.md) solicitada que se va a crear ya existe en el sistema.</span><span class="sxs-lookup"><span data-stu-id="16b63-206">The [governanceRoleAssignment](../resources/governanceroleassignment.md) requested to be created already exists in the system.</span></span>
| <span data-ttu-id="16b63-207">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="16b63-207">400 BadRequest</span></span> | <span data-ttu-id="16b63-208">RoleAssignmentDoesNotExist</span><span class="sxs-lookup"><span data-stu-id="16b63-208">RoleAssignmentDoesNotExist</span></span>    | <span data-ttu-id="16b63-209">El [governanceRoleAssignment](../resources/governanceroleassignment.md) solicitado se actualizó y ampliar no existe en el sistema.</span><span class="sxs-lookup"><span data-stu-id="16b63-209">The [governanceRoleAssignment](../resources/governanceroleassignment.md) requested to be updated/extended does not exist in the system.</span></span>
| <span data-ttu-id="16b63-210">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="16b63-210">400 BadRequest</span></span> | <span data-ttu-id="16b63-211">RoleAssignmentRequestPolicyValidationFailed</span><span class="sxs-lookup"><span data-stu-id="16b63-211">RoleAssignmentRequestPolicyValidationFailed</span></span> | <span data-ttu-id="16b63-212">La [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) no cumple las políticas internas y no se puede crear.</span><span class="sxs-lookup"><span data-stu-id="16b63-212">The [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) does not meet internal policies and cannot be created.</span></span>

## <a name="example-1"></a><span data-ttu-id="16b63-213">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="16b63-213">Example 1</span></span>
<span data-ttu-id="16b63-214">En este ejemplo, los administradores asignan nawu@fimdev.net usuario a la función de lector de facturación.</span><span class="sxs-lookup"><span data-stu-id="16b63-214">In this example, administrators assign user nawu@fimdev.net to the Billing Reader role.</span></span>

 ><span data-ttu-id="16b63-215">**Nota:** Además de los permisos, en este ejemplo se requiere que el solicitante puede tener al menos uno `Active` asignación de roles de administrador (`owner` o `user access administrator`) en el recurso.</span><span class="sxs-lookup"><span data-stu-id="16b63-215">**Note:** Besides the permission, this example requires the requestor to have at least one `Active` adminstrator role assignment (`owner` or `user access administrator`) on the resource.</span></span> 

| <span data-ttu-id="16b63-216">Propiedad</span><span class="sxs-lookup"><span data-stu-id="16b63-216">Property</span></span>     | <span data-ttu-id="16b63-217">Tipo</span><span class="sxs-lookup"><span data-stu-id="16b63-217">Type</span></span>    |<span data-ttu-id="16b63-218">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="16b63-218">Required</span></span>|  <span data-ttu-id="16b63-219">Valor</span><span class="sxs-lookup"><span data-stu-id="16b63-219">Value</span></span> |
|:---------------|:--------|:----------|:----------|
|<span data-ttu-id="16b63-220">resourceId</span><span class="sxs-lookup"><span data-stu-id="16b63-220">resourceId</span></span>|<span data-ttu-id="16b63-221">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-221">String</span></span>|<span data-ttu-id="16b63-222">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-222">Yes</span></span>|<span data-ttu-id="16b63-223">\<resourceId\></span><span class="sxs-lookup"><span data-stu-id="16b63-223">\<resourceId\></span></span>|
|<span data-ttu-id="16b63-224">roleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="16b63-224">roleDefinitionId</span></span>|<span data-ttu-id="16b63-225">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-225">String</span></span>|<span data-ttu-id="16b63-226">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-226">Yes</span></span>|<span data-ttu-id="16b63-227">\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="16b63-227">\<roleDefinitionId\></span></span>|
|<span data-ttu-id="16b63-228">///SubjectID</span><span class="sxs-lookup"><span data-stu-id="16b63-228">subjectId</span></span>|<span data-ttu-id="16b63-229">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-229">String</span></span>|<span data-ttu-id="16b63-230">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-230">Yes</span></span>|<span data-ttu-id="16b63-231">\<///SubjectID\></span><span class="sxs-lookup"><span data-stu-id="16b63-231">\<subjectId\></span></span>|
|<span data-ttu-id="16b63-232">assignmentState</span><span class="sxs-lookup"><span data-stu-id="16b63-232">assignmentState</span></span>|<span data-ttu-id="16b63-233">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-233">String</span></span>|<span data-ttu-id="16b63-234">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-234">Yes</span></span>| <span data-ttu-id="16b63-235">Optan / activo</span><span class="sxs-lookup"><span data-stu-id="16b63-235">Eligible / Active</span></span>|
|<span data-ttu-id="16b63-236">type</span><span class="sxs-lookup"><span data-stu-id="16b63-236">type</span></span>|<span data-ttu-id="16b63-237">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-237">String</span></span>|<span data-ttu-id="16b63-238">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-238">Yes</span></span>| <span data-ttu-id="16b63-239">AdminAdd</span><span class="sxs-lookup"><span data-stu-id="16b63-239">AdminAdd</span></span>|
|<span data-ttu-id="16b63-240">motivo</span><span class="sxs-lookup"><span data-stu-id="16b63-240">reason</span></span>|<span data-ttu-id="16b63-241">String</span><span class="sxs-lookup"><span data-stu-id="16b63-241">String</span></span>| <span data-ttu-id="16b63-242">depende de la función configuración</span><span class="sxs-lookup"><span data-stu-id="16b63-242">depends on role Settings</span></span>||
|<span data-ttu-id="16b63-243">programación</span><span class="sxs-lookup"><span data-stu-id="16b63-243">schedule</span></span>|[<span data-ttu-id="16b63-244">governanceSchedule</span><span class="sxs-lookup"><span data-stu-id="16b63-244">governanceSchedule</span></span>](../resources/governanceschedule.md)|<span data-ttu-id="16b63-245">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-245">Yes</span></span>|        |
##### <a name="request"></a><span data-ttu-id="16b63-246">Solicitud</span><span class="sxs-lookup"><span data-stu-id="16b63-246">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "governanceroleassignmentrequest_post"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedAccess/azureResources/roleAssignmentRequests
Content-type: application/json

{"roleDefinitionId":"ea48ad5e-e3b0-4d10-af54-39a45bbfe68d",
"resourceId":"e5e7d29d-5465-45ac-885f-4716a5ee74b5",
"subjectId":"918e54be-12c4-4f4c-a6d3-2ee0e3661c51",
"assignmentState":"Eligible",
"type":"AdminAdd",
"reason":"Assign an eligible role",
"schedule":{
  "startDateTime":"2018-05-12T23:37:43.356Z",
  "endDateTime":"2018-11-08T23:37:43.356Z",
  "type":"Once"
  }
}
```
##### <a name="response"></a><span data-ttu-id="16b63-247">Respuesta</span><span class="sxs-lookup"><span data-stu-id="16b63-247">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.governanceRoleAssignmentRequest"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 226

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#governanceRoleAssignmentRequests/$entity",
    "id": "1232e4ea-741a-4be5-8044-5edabdd61672",
    "resourceId": "e5e7d29d-5465-45ac-885f-4716a5ee74b5",
    "roleDefinitionId": "ea48ad5e-e3b0-4d10-af54-39a45bbfe68d",
    "subjectId": "918e54be-12c4-4f4c-a6d3-2ee0e3661c51",
    "linkedEligibleRoleAssignmentId": "",
    "type": "AdminAdd",
    "assignmentState": "Eligible",
    "requestedDateTime": "0001-01-01T00:00:00Z",
    "roleAssignmentStartDateTime": "2018-05-12T23:38:34.6007266Z",
    "roleAssignmentEndDateTime": "2018-11-08T23:37:43.356Z",
    "reason": "Evaluate Only",
    "status": {
        "status": "InProgress",
        "subStatus": "Granted",
        "statusDetails": [
            {
                "key": "AdminRequestRule",
                "value": "Grant"
            },
            {
                "key": "ExpirationRule",
                "value": "Grant"
            },
            {
                "key": "MfaRule",
                "value": "Grant"
            }
        ]
    },
    "schedule": {
        "type": "Once",
        "startDateTime": "2018-05-12T23:37:43.356Z",
        "endDateTime": "2018-11-08T23:37:43.356Z",
        "duration": "PT0S"
    }
}
```

## <a name="example-2"></a><span data-ttu-id="16b63-248">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="16b63-248">Example 2</span></span>
<span data-ttu-id="16b63-249">En este ejemplo, el usuario nawu@fimdev.net activa la función de lector de facturación optan.</span><span class="sxs-lookup"><span data-stu-id="16b63-249">In this example, the user nawu@fimdev.net activates the eligible Billing Reader role.</span></span>

| <span data-ttu-id="16b63-250">Propiedad</span><span class="sxs-lookup"><span data-stu-id="16b63-250">Property</span></span>     | <span data-ttu-id="16b63-251">Tipo</span><span class="sxs-lookup"><span data-stu-id="16b63-251">Type</span></span>    |<span data-ttu-id="16b63-252">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="16b63-252">Required</span></span>|  <span data-ttu-id="16b63-253">Valor</span><span class="sxs-lookup"><span data-stu-id="16b63-253">Value</span></span> |
|:---------------|:--------|:----------|:----------|
|<span data-ttu-id="16b63-254">resourceId</span><span class="sxs-lookup"><span data-stu-id="16b63-254">resourceId</span></span>|<span data-ttu-id="16b63-255">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-255">String</span></span>|<span data-ttu-id="16b63-256">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-256">Yes</span></span>|<span data-ttu-id="16b63-257">\<resourceId\></span><span class="sxs-lookup"><span data-stu-id="16b63-257">\<resourceId\></span></span>|
|<span data-ttu-id="16b63-258">roleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="16b63-258">roleDefinitionId</span></span>|<span data-ttu-id="16b63-259">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-259">String</span></span>|<span data-ttu-id="16b63-260">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-260">Yes</span></span>|<span data-ttu-id="16b63-261">\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="16b63-261">\<roleDefinitionId\></span></span>|
|<span data-ttu-id="16b63-262">///SubjectID</span><span class="sxs-lookup"><span data-stu-id="16b63-262">subjectId</span></span>|<span data-ttu-id="16b63-263">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-263">String</span></span>|<span data-ttu-id="16b63-264">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-264">Yes</span></span>|<span data-ttu-id="16b63-265">\<///SubjectID\></span><span class="sxs-lookup"><span data-stu-id="16b63-265">\<subjectId\></span></span>|
|<span data-ttu-id="16b63-266">assignmentState</span><span class="sxs-lookup"><span data-stu-id="16b63-266">assignmentState</span></span>|<span data-ttu-id="16b63-267">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-267">String</span></span>|<span data-ttu-id="16b63-268">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-268">Yes</span></span>| <span data-ttu-id="16b63-269">Activo</span><span class="sxs-lookup"><span data-stu-id="16b63-269">Active</span></span>|
|<span data-ttu-id="16b63-270">type</span><span class="sxs-lookup"><span data-stu-id="16b63-270">type</span></span>|<span data-ttu-id="16b63-271">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-271">String</span></span>|<span data-ttu-id="16b63-272">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-272">Yes</span></span>| <span data-ttu-id="16b63-273">Comandos UserAdd</span><span class="sxs-lookup"><span data-stu-id="16b63-273">UserAdd</span></span>|
|<span data-ttu-id="16b63-274">motivo</span><span class="sxs-lookup"><span data-stu-id="16b63-274">reason</span></span>|<span data-ttu-id="16b63-275">String</span><span class="sxs-lookup"><span data-stu-id="16b63-275">String</span></span>| <span data-ttu-id="16b63-276">depende de la función configuración</span><span class="sxs-lookup"><span data-stu-id="16b63-276">depends on role Settings</span></span>||
|<span data-ttu-id="16b63-277">programación</span><span class="sxs-lookup"><span data-stu-id="16b63-277">schedule</span></span>|[<span data-ttu-id="16b63-278">governanceSchedule</span><span class="sxs-lookup"><span data-stu-id="16b63-278">governanceSchedule</span></span>](../resources/governanceschedule.md)|<span data-ttu-id="16b63-279">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-279">Yes</span></span>|        |
##### <a name="request"></a><span data-ttu-id="16b63-280">Solicitud</span><span class="sxs-lookup"><span data-stu-id="16b63-280">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "governanceroleassignmentrequest_post"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedAccess/azureResources/roleAssignmentRequests
Content-type: application/json

{"roleDefinitionId":"8b4d1d51-08e9-4254-b0a6-b16177aae376",
"resourceId":"e5e7d29d-5465-45ac-885f-4716a5ee74b5",
"subjectId":"918e54be-12c4-4f4c-a6d3-2ee0e3661c51",
"assignmentState":"Active",
"type":"UserAdd",
"reason": "Activate the owner role",
"schedule":{
  "type":"Once",
  "startDateTime":"2018-05-12T23:28:43.537Z",
  "duration":"PT9H"
  },
"linkedEligibleRoleAssignmentId":"e327f4be-42a0-47a2-8579-0a39b025b394"
}
```
##### <a name="response"></a><span data-ttu-id="16b63-281">Respuesta</span><span class="sxs-lookup"><span data-stu-id="16b63-281">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.governanceRoleAssignmentRequest"
} -->
```json
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#governanceRoleAssignmentRequests/$entity",
    "id": "3ad49a7c-918e-4d86-9f84-fab28f8658c0",
    "resourceId": "e5e7d29d-5465-45ac-885f-4716a5ee74b5",
    "roleDefinitionId": "8b4d1d51-08e9-4254-b0a6-b16177aae376",
    "subjectId": "918e54be-12c4-4f4c-a6d3-2ee0e3661c51",
    "linkedEligibleRoleAssignmentId": "e327f4be-42a0-47a2-8579-0a39b025b394",
    "type": "UserAdd",
    "assignmentState": "Active",
    "requestedDateTime": "0001-01-01T00:00:00Z",
    "roleAssignmentStartDateTime": "2018-05-12T23:29:29.5123911Z",
    "roleAssignmentEndDateTime": "2018-05-13T08:28:43.537Z",
    "reason": "Activate the owner role",
    "status": {
        "status": "InProgress",
        "subStatus": "Granted",
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
        "startDateTime": "2018-05-12T23:28:43.537Z",
        "endDateTime": "0001-01-01T00:00:00Z",
        "duration": "PT9H"
    }
}
```

## <a name="example-3"></a><span data-ttu-id="16b63-282">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="16b63-282">Example 3</span></span>
<span data-ttu-id="16b63-283">En este ejemplo, el usuario nawu@fimdev.net desactiva la función de lector de facturación activada.</span><span class="sxs-lookup"><span data-stu-id="16b63-283">In this example, the user nawu@fimdev.net deactivates the active Billing Reader role.</span></span>

| <span data-ttu-id="16b63-284">Propiedad</span><span class="sxs-lookup"><span data-stu-id="16b63-284">Property</span></span>     | <span data-ttu-id="16b63-285">Tipo</span><span class="sxs-lookup"><span data-stu-id="16b63-285">Type</span></span>    |<span data-ttu-id="16b63-286">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="16b63-286">Required</span></span>|  <span data-ttu-id="16b63-287">Valor</span><span class="sxs-lookup"><span data-stu-id="16b63-287">Value</span></span> |
|:---------------|:--------|:----------|:----------|
|<span data-ttu-id="16b63-288">resourceId</span><span class="sxs-lookup"><span data-stu-id="16b63-288">resourceId</span></span>|<span data-ttu-id="16b63-289">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-289">String</span></span>|<span data-ttu-id="16b63-290">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-290">Yes</span></span>|<span data-ttu-id="16b63-291">\<resourceId\></span><span class="sxs-lookup"><span data-stu-id="16b63-291">\<resourceId\></span></span>|
|<span data-ttu-id="16b63-292">roleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="16b63-292">roleDefinitionId</span></span>|<span data-ttu-id="16b63-293">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-293">String</span></span>|<span data-ttu-id="16b63-294">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-294">Yes</span></span>|<span data-ttu-id="16b63-295">\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="16b63-295">\<roleDefinitionId\></span></span>|
|<span data-ttu-id="16b63-296">///SubjectID</span><span class="sxs-lookup"><span data-stu-id="16b63-296">subjectId</span></span>|<span data-ttu-id="16b63-297">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-297">String</span></span>|<span data-ttu-id="16b63-298">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-298">Yes</span></span>|<span data-ttu-id="16b63-299">\<///SubjectID\></span><span class="sxs-lookup"><span data-stu-id="16b63-299">\<subjectId\></span></span>|
|<span data-ttu-id="16b63-300">assignmentState</span><span class="sxs-lookup"><span data-stu-id="16b63-300">assignmentState</span></span>|<span data-ttu-id="16b63-301">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-301">String</span></span>|<span data-ttu-id="16b63-302">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-302">Yes</span></span>| <span data-ttu-id="16b63-303">Activo</span><span class="sxs-lookup"><span data-stu-id="16b63-303">Active</span></span>|
|<span data-ttu-id="16b63-304">type</span><span class="sxs-lookup"><span data-stu-id="16b63-304">type</span></span>|<span data-ttu-id="16b63-305">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-305">String</span></span>|<span data-ttu-id="16b63-306">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-306">Yes</span></span>| <span data-ttu-id="16b63-307">UserRemove</span><span class="sxs-lookup"><span data-stu-id="16b63-307">UserRemove</span></span>|
|<span data-ttu-id="16b63-308">motivo</span><span class="sxs-lookup"><span data-stu-id="16b63-308">reason</span></span>|<span data-ttu-id="16b63-309">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-309">String</span></span>| <span data-ttu-id="16b63-310">No</span><span class="sxs-lookup"><span data-stu-id="16b63-310">No</span></span>||
|<span data-ttu-id="16b63-311">programación</span><span class="sxs-lookup"><span data-stu-id="16b63-311">schedule</span></span>|[<span data-ttu-id="16b63-312">governanceSchedule</span><span class="sxs-lookup"><span data-stu-id="16b63-312">governanceSchedule</span></span>](../resources/governanceschedule.md)|<span data-ttu-id="16b63-313">No</span><span class="sxs-lookup"><span data-stu-id="16b63-313">No</span></span>|        |
##### <a name="request"></a><span data-ttu-id="16b63-314">Solicitud</span><span class="sxs-lookup"><span data-stu-id="16b63-314">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "governanceroleassignmentrequest_post"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedAccess/azureResources/roleAssignmentRequests
Content-type: application/json

{"roleDefinitionId":"bc75b4e6-7403-4243-bf2f-d1f6990be122",
"resourceId":"fb016e3a-c3ed-4d9d-96b6-a54cd4f0b735",
"subjectId":"918e54be-12c4-4f4c-a6d3-2ee0e3661c51",
"assignmentState":"Active",
"type":"UserRemove",
"reason":"Deactivate the role",
"linkedEligibleRoleAssignmentId":"cb8a533e-02d5-42ad-8499-916b1e4822ec"
}
```
##### <a name="response"></a><span data-ttu-id="16b63-315">Respuesta</span><span class="sxs-lookup"><span data-stu-id="16b63-315">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.governanceRoleAssignmentRequest"
} -->
```json
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 226

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#governanceRoleAssignmentRequests/$entity",
    "id": "abfcdb57-8e5d-42a0-ae67-7598b96fddb1",
    "resourceId": "fb016e3a-c3ed-4d9d-96b6-a54cd4f0b735",
    "roleDefinitionId": "bc75b4e6-7403-4243-bf2f-d1f6990be122",
    "subjectId": "918e54be-12c4-4f4c-a6d3-2ee0e3661c51",
    "linkedEligibleRoleAssignmentId": "cb8a533e-02d5-42ad-8499-916b1e4822ec",
    "type": "UserRemove",
    "assignmentState": "Active",
    "requestedDateTime": "0001-01-01T00:00:00Z",
    "roleAssignmentStartDateTime": null,
    "roleAssignmentEndDateTime": null,
    "reason": "Evaluate only",
    "schedule": null,
    "status": {
        "status": "Closed",
        "subStatus": "Revoked",
        "statusDetails": []
    }
}
```

### <a name="example-4"></a><span data-ttu-id="16b63-316">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="16b63-316">Example 4</span></span>
<span data-ttu-id="16b63-317">En este ejemplo, los administradores de quitar el usuario nawu@fimdev.net de la función de lector de facturación.</span><span class="sxs-lookup"><span data-stu-id="16b63-317">In this example, administrators remove the user nawu@fimdev.net from the Billing Reader role.</span></span>

 ><span data-ttu-id="16b63-318">**Nota:** Además el ámbito de permisos, en este ejemplo se requiere que el solicitante puede tener al menos uno `Active` asignación de roles de administrador (`owner` o `user access administrator`) en el recurso.</span><span class="sxs-lookup"><span data-stu-id="16b63-318">**Note:** Besides the permission scope, this example requires the requestor to have at least one `Active` adminstrator role assignment (`owner` or `user access administrator`) on the resource.</span></span>
 
| <span data-ttu-id="16b63-319">Propiedad</span><span class="sxs-lookup"><span data-stu-id="16b63-319">Property</span></span>     | <span data-ttu-id="16b63-320">Tipo</span><span class="sxs-lookup"><span data-stu-id="16b63-320">Type</span></span>    |<span data-ttu-id="16b63-321">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="16b63-321">Required</span></span>|  <span data-ttu-id="16b63-322">Valor</span><span class="sxs-lookup"><span data-stu-id="16b63-322">Value</span></span> |
|:---------------|:--------|:----------|:----------|
|<span data-ttu-id="16b63-323">resourceId</span><span class="sxs-lookup"><span data-stu-id="16b63-323">resourceId</span></span>|<span data-ttu-id="16b63-324">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-324">String</span></span>|<span data-ttu-id="16b63-325">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-325">Yes</span></span>|<span data-ttu-id="16b63-326">\<resourceId\></span><span class="sxs-lookup"><span data-stu-id="16b63-326">\<resourceId\></span></span>|
|<span data-ttu-id="16b63-327">roleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="16b63-327">roleDefinitionId</span></span>|<span data-ttu-id="16b63-328">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-328">String</span></span>|<span data-ttu-id="16b63-329">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-329">Yes</span></span>|<span data-ttu-id="16b63-330">\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="16b63-330">\<roleDefinitionId\></span></span>|
|<span data-ttu-id="16b63-331">///SubjectID</span><span class="sxs-lookup"><span data-stu-id="16b63-331">subjectId</span></span>|<span data-ttu-id="16b63-332">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-332">String</span></span>|<span data-ttu-id="16b63-333">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-333">Yes</span></span>|<span data-ttu-id="16b63-334">\<///SubjectID\></span><span class="sxs-lookup"><span data-stu-id="16b63-334">\<subjectId\></span></span>|
|<span data-ttu-id="16b63-335">assignmentState</span><span class="sxs-lookup"><span data-stu-id="16b63-335">assignmentState</span></span>|<span data-ttu-id="16b63-336">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-336">String</span></span>|<span data-ttu-id="16b63-337">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-337">Yes</span></span>| <span data-ttu-id="16b63-338">Optan / activo</span><span class="sxs-lookup"><span data-stu-id="16b63-338">Eligible / Active</span></span>|
|<span data-ttu-id="16b63-339">type</span><span class="sxs-lookup"><span data-stu-id="16b63-339">type</span></span>|<span data-ttu-id="16b63-340">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-340">String</span></span>|<span data-ttu-id="16b63-341">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-341">Yes</span></span>| <span data-ttu-id="16b63-342">AdminRemove</span><span class="sxs-lookup"><span data-stu-id="16b63-342">AdminRemove</span></span>|
|<span data-ttu-id="16b63-343">motivo</span><span class="sxs-lookup"><span data-stu-id="16b63-343">reason</span></span>|<span data-ttu-id="16b63-344">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-344">String</span></span>| <span data-ttu-id="16b63-345">No</span><span class="sxs-lookup"><span data-stu-id="16b63-345">No</span></span>||
|<span data-ttu-id="16b63-346">programación</span><span class="sxs-lookup"><span data-stu-id="16b63-346">schedule</span></span>|[<span data-ttu-id="16b63-347">governanceSchedule</span><span class="sxs-lookup"><span data-stu-id="16b63-347">governanceSchedule</span></span>](../resources/governanceschedule.md)|<span data-ttu-id="16b63-348">No</span><span class="sxs-lookup"><span data-stu-id="16b63-348">No</span></span>|        |
##### <a name="request"></a><span data-ttu-id="16b63-349">Solicitud</span><span class="sxs-lookup"><span data-stu-id="16b63-349">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "governanceroleassignmentrequest_post"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedAccess/azureResources/roleAssignmentRequests
Content-type: application/json

{
  "roleDefinitionId":"65bb4622-61f5-4f25-9d75-d0e20cf92019",
  "resourceId":"e5e7d29d-5465-45ac-885f-4716a5ee74b5",
  "subjectId":"74765671-9ca4-40d7-9e36-2f4a570608a6",
  "assignmentState":"Eligible",
  "type":"AdminRemove"
}
```
##### <a name="response"></a><span data-ttu-id="16b63-350">Respuesta</span><span class="sxs-lookup"><span data-stu-id="16b63-350">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.governanceRoleAssignmentRequest"
} -->
```json
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 226

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#governanceRoleAssignmentRequests/$entity",
  "id":"c934fcb9-cf53-42ac-a8b4-6246f6726299",
  "resourceId":"e5e7d29d-5465-45ac-885f-4716a5ee74b5",
  "roleDefinitionId":"65bb4622-61f5-4f25-9d75-d0e20cf92019",
  "subjectId":"74765671-9ca4-40d7-9e36-2f4a570608a6",
  "linkedEligibleRoleAssignmentId":"",
  "type":"AdminRemove",
  "assignmentState":"Eligible",
  "requestedDateTime":"0001-01-01T00:00:00Z",
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

### <a name="example-5"></a><span data-ttu-id="16b63-351">Ejemplo 5</span><span class="sxs-lookup"><span data-stu-id="16b63-351">Example 5</span></span>
<span data-ttu-id="16b63-352">En este ejemplo, los administradores actualizar la asignación de rol para el usuario nawu@fimdev.net al propietario.</span><span class="sxs-lookup"><span data-stu-id="16b63-352">In this example, administrators update the role assignment for the user nawu@fimdev.net to Owner.</span></span>

 ><span data-ttu-id="16b63-353">**Nota:** Además el ámbito de permisos, en este ejemplo se requiere que el solicitante puede tener al menos uno `Active` asignación de roles de administrador (`owner` o `user access administrator`) en el recurso.</span><span class="sxs-lookup"><span data-stu-id="16b63-353">**Note:** Besides the permission scope, this example requires the requestor to have at least one `Active` adminstrator role assignment (`owner` or `user access administrator`) on the resource.</span></span> 
| <span data-ttu-id="16b63-354">Propiedad</span><span class="sxs-lookup"><span data-stu-id="16b63-354">Property</span></span>     | <span data-ttu-id="16b63-355">Tipo</span><span class="sxs-lookup"><span data-stu-id="16b63-355">Type</span></span>    |<span data-ttu-id="16b63-356">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="16b63-356">Required</span></span>|  <span data-ttu-id="16b63-357">Valor</span><span class="sxs-lookup"><span data-stu-id="16b63-357">Value</span></span> |
|:---------------|:--------|:----------|:----------|
|<span data-ttu-id="16b63-358">resourceId</span><span class="sxs-lookup"><span data-stu-id="16b63-358">resourceId</span></span>|<span data-ttu-id="16b63-359">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-359">String</span></span>|<span data-ttu-id="16b63-360">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-360">Yes</span></span>|<span data-ttu-id="16b63-361">\<resourceId\></span><span class="sxs-lookup"><span data-stu-id="16b63-361">\<resourceId\></span></span>|
|<span data-ttu-id="16b63-362">roleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="16b63-362">roleDefinitionId</span></span>|<span data-ttu-id="16b63-363">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-363">String</span></span>|<span data-ttu-id="16b63-364">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-364">Yes</span></span>|<span data-ttu-id="16b63-365">\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="16b63-365">\<roleDefinitionId\></span></span>|
|<span data-ttu-id="16b63-366">///SubjectID</span><span class="sxs-lookup"><span data-stu-id="16b63-366">subjectId</span></span>|<span data-ttu-id="16b63-367">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-367">String</span></span>|<span data-ttu-id="16b63-368">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-368">Yes</span></span>|<span data-ttu-id="16b63-369">\<///SubjectID\></span><span class="sxs-lookup"><span data-stu-id="16b63-369">\<subjectId\></span></span>|
|<span data-ttu-id="16b63-370">assignmentState</span><span class="sxs-lookup"><span data-stu-id="16b63-370">assignmentState</span></span>|<span data-ttu-id="16b63-371">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-371">String</span></span>|<span data-ttu-id="16b63-372">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-372">Yes</span></span>| <span data-ttu-id="16b63-373">Optan / activo</span><span class="sxs-lookup"><span data-stu-id="16b63-373">Eligible / Active</span></span>|
|<span data-ttu-id="16b63-374">type</span><span class="sxs-lookup"><span data-stu-id="16b63-374">type</span></span>|<span data-ttu-id="16b63-375">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-375">String</span></span>|<span data-ttu-id="16b63-376">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-376">Yes</span></span>| <span data-ttu-id="16b63-377">AdminUpdate</span><span class="sxs-lookup"><span data-stu-id="16b63-377">AdminUpdate</span></span>|
|<span data-ttu-id="16b63-378">motivo</span><span class="sxs-lookup"><span data-stu-id="16b63-378">reason</span></span>|<span data-ttu-id="16b63-379">String</span><span class="sxs-lookup"><span data-stu-id="16b63-379">String</span></span>| <span data-ttu-id="16b63-380">depende de roleSettings</span><span class="sxs-lookup"><span data-stu-id="16b63-380">depends on roleSettings</span></span>||
|<span data-ttu-id="16b63-381">programación</span><span class="sxs-lookup"><span data-stu-id="16b63-381">schedule</span></span>|[<span data-ttu-id="16b63-382">governanceSchedule</span><span class="sxs-lookup"><span data-stu-id="16b63-382">governanceSchedule</span></span>](../resources/governanceschedule.md)|<span data-ttu-id="16b63-383">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-383">Yes</span></span>|        |
##### <a name="request"></a><span data-ttu-id="16b63-384">Solicitud</span><span class="sxs-lookup"><span data-stu-id="16b63-384">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "governanceroleassignmentrequest_post"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedAccess/azureResources/roleAssignmentRequests
Content-type: application/json

{
  "roleDefinitionId":"70521f3e-3b95-4e51-b4d2-a2f485b02103",
  "resourceId":"e5e7d29d-5465-45ac-885f-4716a5ee74b5",
  "subjectId":"1566d11d-d2b6-444a-a8de-28698682c445",
  "assignmentState":"Eligible",
  "type":"AdminUpdate",
  "schedule":{
    "type":"Once",
    "startDateTime":"2018-03-08T05:42:45.317Z",
    "endDateTime":"2018-06-05T05:42:31.000Z"
  }
}
```
##### <a name="response"></a><span data-ttu-id="16b63-385">Respuesta</span><span class="sxs-lookup"><span data-stu-id="16b63-385">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.governanceRoleAssignmentRequest"
} -->
```json
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 226

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#governanceRoleAssignmentRequests/$entity",
  "id":"4f6d4802-b3ac-4f5a-86d7-a6a4edd7d383",
  "resourceId":"e5e7d29d-5465-45ac-885f-4716a5ee74b5",
  "roleDefinitionId":"70521f3e-3b95-4e51-b4d2-a2f485b02103",
  "subjectId":"1566d11d-d2b6-444a-a8de-28698682c445",
  "linkedEligibleRoleAssignmentId":"",
  "type":"AdminUpdate",
  "assignmentState":"Eligible",
  "requestedDateTime":"0001-01-01T00:00:00Z",
  "roleAssignmentStartDateTime":"2018-05-12T23:50:03.4755896Z",
  "roleAssignmentEndDateTime":"2018-06-05T05:42:31Z",
  "reason":null,
  "status":{
    "status":"InProgress",
    "subStatus":"Granted",
    "statusDetails":[
      {
        "key":"AdminRequestRule","value":"Grant"
      },{
        "key":"ExpirationRule","value":"Grant"
      },{
        "key":"MfaRule","value":"Grant"
      }
    ]
  },
  "schedule":{
    "type":"Once",
    "startDateTime":"2018-03-08T05:42:45.317Z",
    "endDateTime":"2018-06-05T05:42:31Z",
    "duration":"PT0S"
  }
}
```

### <a name="example-6"></a><span data-ttu-id="16b63-386">Ejemplo 6</span><span class="sxs-lookup"><span data-stu-id="16b63-386">Example 6</span></span>
<span data-ttu-id="16b63-387">En este ejemplo se extiende la asignación de roles a punto de expirar para usuario ANUJCUSER a la API de administración de servicio colaborador.</span><span class="sxs-lookup"><span data-stu-id="16b63-387">This example extends the expiring role assignment for user ANUJCUSER to API Management Service Contributor.</span></span>

 ><span data-ttu-id="16b63-388">**Nota:** Además el ámbito de permisos, en este ejemplo se requiere que el solicitante puede tener al menos uno `Active` asignación de roles de administrador (`owner` o `user access administrator`) en el recurso.</span><span class="sxs-lookup"><span data-stu-id="16b63-388">**Note:** Besides the permission scope, this example requires the requestor to have at least one `Active` adminstrator role assignment (`owner` or `user access administrator`) on the resource.</span></span>
 
| <span data-ttu-id="16b63-389">Propiedad</span><span class="sxs-lookup"><span data-stu-id="16b63-389">Property</span></span>     | <span data-ttu-id="16b63-390">Tipo</span><span class="sxs-lookup"><span data-stu-id="16b63-390">Type</span></span>    |<span data-ttu-id="16b63-391">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="16b63-391">Required</span></span>|  <span data-ttu-id="16b63-392">Valor</span><span class="sxs-lookup"><span data-stu-id="16b63-392">Value</span></span> |
|:---------------|:--------|:----------|:----------|
|<span data-ttu-id="16b63-393">resourceId</span><span class="sxs-lookup"><span data-stu-id="16b63-393">resourceId</span></span>|<span data-ttu-id="16b63-394">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-394">String</span></span>|<span data-ttu-id="16b63-395">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-395">Yes</span></span>|<span data-ttu-id="16b63-396">\<resourceId\></span><span class="sxs-lookup"><span data-stu-id="16b63-396">\<resourceId\></span></span>|
|<span data-ttu-id="16b63-397">roleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="16b63-397">roleDefinitionId</span></span>|<span data-ttu-id="16b63-398">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-398">String</span></span>|<span data-ttu-id="16b63-399">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-399">Yes</span></span>|<span data-ttu-id="16b63-400">\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="16b63-400">\<roleDefinitionId\></span></span>|
|<span data-ttu-id="16b63-401">///SubjectID</span><span class="sxs-lookup"><span data-stu-id="16b63-401">subjectId</span></span>|<span data-ttu-id="16b63-402">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-402">String</span></span>|<span data-ttu-id="16b63-403">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-403">Yes</span></span>|<span data-ttu-id="16b63-404">\<///SubjectID\></span><span class="sxs-lookup"><span data-stu-id="16b63-404">\<subjectId\></span></span>|
|<span data-ttu-id="16b63-405">assignmentState</span><span class="sxs-lookup"><span data-stu-id="16b63-405">assignmentState</span></span>|<span data-ttu-id="16b63-406">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-406">String</span></span>|<span data-ttu-id="16b63-407">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-407">Yes</span></span>| <span data-ttu-id="16b63-408">Optan / activo</span><span class="sxs-lookup"><span data-stu-id="16b63-408">Eligible / Active</span></span> |
|<span data-ttu-id="16b63-409">type</span><span class="sxs-lookup"><span data-stu-id="16b63-409">type</span></span>|<span data-ttu-id="16b63-410">Cadena</span><span class="sxs-lookup"><span data-stu-id="16b63-410">String</span></span>|<span data-ttu-id="16b63-411">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-411">Yes</span></span>| <span data-ttu-id="16b63-412">AdminExtend</span><span class="sxs-lookup"><span data-stu-id="16b63-412">AdminExtend</span></span>|
|<span data-ttu-id="16b63-413">motivo</span><span class="sxs-lookup"><span data-stu-id="16b63-413">reason</span></span>|<span data-ttu-id="16b63-414">String</span><span class="sxs-lookup"><span data-stu-id="16b63-414">String</span></span>| <span data-ttu-id="16b63-415">depende de roleSettings</span><span class="sxs-lookup"><span data-stu-id="16b63-415">depends on roleSettings</span></span>||
|<span data-ttu-id="16b63-416">programación</span><span class="sxs-lookup"><span data-stu-id="16b63-416">schedule</span></span>|[<span data-ttu-id="16b63-417">governanceSchedule</span><span class="sxs-lookup"><span data-stu-id="16b63-417">governanceSchedule</span></span>](../resources/governanceschedule.md)|<span data-ttu-id="16b63-418">Sí</span><span class="sxs-lookup"><span data-stu-id="16b63-418">Yes</span></span>|        |
##### <a name="request"></a><span data-ttu-id="16b63-419">Solicitud</span><span class="sxs-lookup"><span data-stu-id="16b63-419">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "governanceroleassignmentrequest_post"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedAccess/azureResources/roleAssignmentRequests
Content-type: application/json

{
  "roleDefinitionId":"0e88fd18-50f5-4ee1-9104-01c3ed910065",
  "resourceId":"e5e7d29d-5465-45ac-885f-4716a5ee74b5",
  "subjectId":"74765671-9ca4-40d7-9e36-2f4a570608a6",
  "assignmentState":"Eligible",
  "type":"AdminExtend",
  "reason":"extend role assignment",
  "schedule":{
    "type":"Once",
    "startDateTime":"2018-05-12T23:53:55.327Z",
    "endDateTime":"2018-08-10T23:53:55.327Z"
  }
}
```
##### <a name="response"></a><span data-ttu-id="16b63-420">Respuesta</span><span class="sxs-lookup"><span data-stu-id="16b63-420">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.governanceRoleAssignmentRequest"
} -->
```json
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 226

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#governanceRoleAssignmentRequests/$entity",
  "id":"486f0c05-47c8-4498-9c06-086a78c83004",
  "resourceId":"e5e7d29d-5465-45ac-885f-4716a5ee74b5",
  "roleDefinitionId":"0e88fd18-50f5-4ee1-9104-01c3ed910065",
  "subjectId":"74765671-9ca4-40d7-9e36-2f4a570608a6",
  "linkedEligibleRoleAssignmentId":"",
  "type":"AdminExtend",
  "assignmentState":"Eligible",
  "requestedDateTime":"0001-01-01T00:00:00Z",
  "roleAssignmentStartDateTime":"2018-05-12T23:54:09.7221332Z",
  "roleAssignmentEndDateTime":"2018-08-10T23:53:55.327Z",
  "reason":"extend role assignment",
  "status":{
    "status":"InProgress",
    "subStatus":"Granted",
    "statusDetails":[
      {
        "key":"AdminRequestRule","value":"Grant"
      },{
        "key":"ExpirationRule","value":"Grant"
      },{
        "key":"MfaRule","value":"Grant"
      }
    ]
  },
  "schedule":{
    "type":"Once",
    "startDateTime":"2018-05-12T23:53:55.327Z",
    "endDateTime":"2018-08-10T23:53:55.327Z",
    "duration":"PT0S"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Post roleAssignmentRequest",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
