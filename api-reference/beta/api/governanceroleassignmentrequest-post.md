---
title: Crear governanceRoleAssignmentRequest
description: Cree una solicitud de asignación de rol para representar la operación que desee en una asignación de roles. En la siguiente tabla se enumera las operaciones.
localization_priority: Normal
ms.openlocfilehash: 09adb824147dba745649efc7589ca763f815278d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27823775"
---
# <a name="create-governanceroleassignmentrequest"></a><span data-ttu-id="bfe01-104">Crear governanceRoleAssignmentRequest</span><span class="sxs-lookup"><span data-stu-id="bfe01-104">Create governanceRoleAssignmentRequest</span></span>

> <span data-ttu-id="bfe01-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bfe01-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bfe01-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bfe01-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="bfe01-107">Cree una solicitud de asignación de rol para representar la operación que desee en una asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="bfe01-107">Create a role assignment request to represent the operation you want on a role assignment.</span></span> <span data-ttu-id="bfe01-108">En la siguiente tabla se enumera las operaciones.</span><span class="sxs-lookup"><span data-stu-id="bfe01-108">The following table lists the operations.</span></span>

| <span data-ttu-id="bfe01-109">Operación</span><span class="sxs-lookup"><span data-stu-id="bfe01-109">Operation</span></span>       | <span data-ttu-id="bfe01-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="bfe01-110">Type</span></span> | 
|:---------------|:----------|
| <span data-ttu-id="bfe01-111">Asignar una asignación de roles</span><span class="sxs-lookup"><span data-stu-id="bfe01-111">Assign a role assignment</span></span>| <span data-ttu-id="bfe01-112">AdminAdd</span><span class="sxs-lookup"><span data-stu-id="bfe01-112">AdminAdd</span></span> |
| <span data-ttu-id="bfe01-113">Activar una asignación de rol optan</span><span class="sxs-lookup"><span data-stu-id="bfe01-113">Activate an eligible role assignment</span></span>| <span data-ttu-id="bfe01-114">Comandos UserAdd</span><span class="sxs-lookup"><span data-stu-id="bfe01-114">UserAdd</span></span> | 
| <span data-ttu-id="bfe01-115">Desactivación de una asignación de rol activada</span><span class="sxs-lookup"><span data-stu-id="bfe01-115">Deactivate an activated role assignment</span></span>| <span data-ttu-id="bfe01-116">UserRemove</span><span class="sxs-lookup"><span data-stu-id="bfe01-116">UserRemove</span></span> | 
| <span data-ttu-id="bfe01-117">Quitar una asignación de roles</span><span class="sxs-lookup"><span data-stu-id="bfe01-117">Remove a role assignment</span></span>| <span data-ttu-id="bfe01-118">AdminRemove</span><span class="sxs-lookup"><span data-stu-id="bfe01-118">AdminRemove</span></span> |
| <span data-ttu-id="bfe01-119">Actualizar una asignación de roles</span><span class="sxs-lookup"><span data-stu-id="bfe01-119">Update a role assignment</span></span>| <span data-ttu-id="bfe01-120">AdminUpdate</span><span class="sxs-lookup"><span data-stu-id="bfe01-120">AdminUpdate</span></span> |
| <span data-ttu-id="bfe01-121">Solicitud para ampliar la asignación de roles</span><span class="sxs-lookup"><span data-stu-id="bfe01-121">Request to extend my role assignment</span></span>| <span data-ttu-id="bfe01-122">UserExtend</span><span class="sxs-lookup"><span data-stu-id="bfe01-122">UserExtend</span></span> | 
| <span data-ttu-id="bfe01-123">Extender una asignación de roles</span><span class="sxs-lookup"><span data-stu-id="bfe01-123">Extend a role assignment</span></span>| <span data-ttu-id="bfe01-124">AdminExtend</span><span class="sxs-lookup"><span data-stu-id="bfe01-124">AdminExtend</span></span> | 
| <span data-ttu-id="bfe01-125">Solicitud para renovar la asignación de rol que han expirado</span><span class="sxs-lookup"><span data-stu-id="bfe01-125">Request to renew my expired role assignment</span></span>| <span data-ttu-id="bfe01-126">UserRenew</span><span class="sxs-lookup"><span data-stu-id="bfe01-126">UserRenew</span></span> | 
| <span data-ttu-id="bfe01-127">Renovar una asignación de rol que han expirado</span><span class="sxs-lookup"><span data-stu-id="bfe01-127">Renew an expired role assignment</span></span>| <span data-ttu-id="bfe01-128">AdminRenew</span><span class="sxs-lookup"><span data-stu-id="bfe01-128">AdminRenew</span></span> | 

 
## <a name="permissions"></a><span data-ttu-id="bfe01-129">Permisos</span><span class="sxs-lookup"><span data-stu-id="bfe01-129">Permissions</span></span>
<span data-ttu-id="bfe01-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bfe01-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bfe01-132">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bfe01-132">Permission type</span></span>      | <span data-ttu-id="bfe01-133">Permisos</span><span class="sxs-lookup"><span data-stu-id="bfe01-133">Permissions</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bfe01-134">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bfe01-134">Delegated (work or school account)</span></span> | <span data-ttu-id="bfe01-135">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="bfe01-135">PrivilegedAccess.ReadWrite.AzureResources</span></span>  |
|<span data-ttu-id="bfe01-136">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bfe01-136">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bfe01-137">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bfe01-137">Not supported.</span></span>    |
|<span data-ttu-id="bfe01-138">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bfe01-138">Application</span></span> | <span data-ttu-id="bfe01-139">PrivilegedAccess.ReadWrite.AzureResources</span><span class="sxs-lookup"><span data-stu-id="bfe01-139">PrivilegedAccess.ReadWrite.AzureResources</span></span> |

## <a name="http-request"></a><span data-ttu-id="bfe01-140">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bfe01-140">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /privilegedAccess/azureResources/roleAssignmentRequests
```

## <a name="request-headers"></a><span data-ttu-id="bfe01-141">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bfe01-141">Request headers</span></span>
| <span data-ttu-id="bfe01-142">Nombre</span><span class="sxs-lookup"><span data-stu-id="bfe01-142">Name</span></span>       | <span data-ttu-id="bfe01-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="bfe01-143">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="bfe01-144">Autorización</span><span class="sxs-lookup"><span data-stu-id="bfe01-144">Authorization</span></span>  | <span data-ttu-id="bfe01-145">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="bfe01-145">Bearer {code}</span></span>|
| <span data-ttu-id="bfe01-146">Tipo de contenido</span><span class="sxs-lookup"><span data-stu-id="bfe01-146">Content-type</span></span>  | <span data-ttu-id="bfe01-147">application/json</span><span class="sxs-lookup"><span data-stu-id="bfe01-147">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bfe01-148">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bfe01-148">Request body</span></span>
<span data-ttu-id="bfe01-149">En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) .</span><span class="sxs-lookup"><span data-stu-id="bfe01-149">In the request body, supply a JSON representation of a [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) object.</span></span> 

| <span data-ttu-id="bfe01-150">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bfe01-150">Property</span></span>     | <span data-ttu-id="bfe01-151">Tipo</span><span class="sxs-lookup"><span data-stu-id="bfe01-151">Type</span></span>    |<span data-ttu-id="bfe01-152">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="bfe01-152">Required</span></span>|  <span data-ttu-id="bfe01-153">Description</span><span class="sxs-lookup"><span data-stu-id="bfe01-153">Description</span></span>|
|:---------------|:--------|:----------|:----------|
|<span data-ttu-id="bfe01-154">resourceId</span><span class="sxs-lookup"><span data-stu-id="bfe01-154">resourceId</span></span>|<span data-ttu-id="bfe01-155">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-155">String</span></span>|<span data-ttu-id="bfe01-156">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-156">Yes</span></span>|<span data-ttu-id="bfe01-157">El identificador del recurso.</span><span class="sxs-lookup"><span data-stu-id="bfe01-157">The ID of the resource.</span></span>|
|<span data-ttu-id="bfe01-158">roleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="bfe01-158">roleDefinitionId</span></span>|<span data-ttu-id="bfe01-159">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-159">String</span></span>|<span data-ttu-id="bfe01-160">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-160">Yes</span></span>|<span data-ttu-id="bfe01-161">El identificador de la definición de roles.</span><span class="sxs-lookup"><span data-stu-id="bfe01-161">The ID of the role definition.</span></span>|
|<span data-ttu-id="bfe01-162">///SubjectID</span><span class="sxs-lookup"><span data-stu-id="bfe01-162">subjectId</span></span>|<span data-ttu-id="bfe01-163">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-163">String</span></span>|<span data-ttu-id="bfe01-164">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-164">Yes</span></span>|<span data-ttu-id="bfe01-165">El identificador del tema.</span><span class="sxs-lookup"><span data-stu-id="bfe01-165">The ID of the subject.</span></span>|
|<span data-ttu-id="bfe01-166">assignmentState</span><span class="sxs-lookup"><span data-stu-id="bfe01-166">assignmentState</span></span>|<span data-ttu-id="bfe01-167">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-167">String</span></span>|<span data-ttu-id="bfe01-168">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-168">Yes</span></span>|<span data-ttu-id="bfe01-169">El estado de asignación.</span><span class="sxs-lookup"><span data-stu-id="bfe01-169">The state of assignment.</span></span> <span data-ttu-id="bfe01-170">El valor puede ser ``Eligible`` y ``Active``.</span><span class="sxs-lookup"><span data-stu-id="bfe01-170">The value can be ``Eligible`` and ``Active``.</span></span>|
|<span data-ttu-id="bfe01-171">type</span><span class="sxs-lookup"><span data-stu-id="bfe01-171">type</span></span>|<span data-ttu-id="bfe01-172">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-172">String</span></span>|<span data-ttu-id="bfe01-173">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-173">Yes</span></span>|<span data-ttu-id="bfe01-174">El tipo de solicitud.</span><span class="sxs-lookup"><span data-stu-id="bfe01-174">The request type.</span></span> <span data-ttu-id="bfe01-175">El valor puede ser `AdminAdd`, `UserAdd`, `AdminUpdate`, `AdminRemove`, `UserRemove`, `UserExtend`, `UserRenew`, `AdminRenew`y `AdminExtend`.</span><span class="sxs-lookup"><span data-stu-id="bfe01-175">The value can be `AdminAdd`, `UserAdd`, `AdminUpdate`, `AdminRemove`, `UserRemove`, `UserExtend`, `UserRenew`, `AdminRenew`and `AdminExtend`.</span></span>|
|<span data-ttu-id="bfe01-176">motivo</span><span class="sxs-lookup"><span data-stu-id="bfe01-176">reason</span></span>|<span data-ttu-id="bfe01-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-177">String</span></span>| |<span data-ttu-id="bfe01-178">Necesita la razón por la que se proporcionará para la solicitud de asignación de rol para auditoría y revise el propósito.</span><span class="sxs-lookup"><span data-stu-id="bfe01-178">The reason needs to be provided for the role assignment request for audit and review purpose.</span></span>|
|<span data-ttu-id="bfe01-179">programación</span><span class="sxs-lookup"><span data-stu-id="bfe01-179">schedule</span></span>|[<span data-ttu-id="bfe01-180">governanceSchedule</span><span class="sxs-lookup"><span data-stu-id="bfe01-180">governanceSchedule</span></span>](../resources/governanceschedule.md)| | <span data-ttu-id="bfe01-181">La programación de la solicitud de asignación de rol.</span><span class="sxs-lookup"><span data-stu-id="bfe01-181">The schedule of the role assignment request.</span></span> <span data-ttu-id="bfe01-182">Para tipo de solicitud de `UserAdd`, `AdminAdd`, `AdminUpdate`, y `AdminExtend`, es necesario.</span><span class="sxs-lookup"><span data-stu-id="bfe01-182">For request type of `UserAdd`, `AdminAdd`, `AdminUpdate`, and `AdminExtend`, it is required.</span></span>|

## <a name="response"></a><span data-ttu-id="bfe01-183">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bfe01-183">Response</span></span>
<span data-ttu-id="bfe01-184">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bfe01-184">If successful, this method returns a `201 Created` response code and a [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) object in the response body.</span></span>

### <a name="error-codes"></a><span data-ttu-id="bfe01-185">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="bfe01-185">Error codes</span></span>
<span data-ttu-id="bfe01-186">Esta API devuelve los códigos de error HTTP estándares.</span><span class="sxs-lookup"><span data-stu-id="bfe01-186">This API returns the standard HTTP error codes.</span></span> <span data-ttu-id="bfe01-187">Además, también devuelve los códigos de error que aparecen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="bfe01-187">In addition, it also returns the error codes listed in the following table.</span></span>

|<span data-ttu-id="bfe01-188">Código de error</span><span class="sxs-lookup"><span data-stu-id="bfe01-188">Error code</span></span>     | <span data-ttu-id="bfe01-189">Mensaje de error</span><span class="sxs-lookup"><span data-stu-id="bfe01-189">Error message</span></span>              | <span data-ttu-id="bfe01-190">Detalles</span><span class="sxs-lookup"><span data-stu-id="bfe01-190">Details</span></span> |
|:--------------------| :---------------------|:--------------------|
| <span data-ttu-id="bfe01-191">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="bfe01-191">400 BadRequest</span></span> | <span data-ttu-id="bfe01-192">RoleNotFound</span><span class="sxs-lookup"><span data-stu-id="bfe01-192">RoleNotFound</span></span>    | <span data-ttu-id="bfe01-193">El `roleDefinitionId` proporcionado en la solicitud no se encuentra el cuerpo.</span><span class="sxs-lookup"><span data-stu-id="bfe01-193">The `roleDefinitionId` provided in the request body cannot be found.</span></span>
| <span data-ttu-id="bfe01-194">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="bfe01-194">400 BadRequest</span></span> | <span data-ttu-id="bfe01-195">ResourceIsLocked</span><span class="sxs-lookup"><span data-stu-id="bfe01-195">ResourceIsLocked</span></span>    | <span data-ttu-id="bfe01-196">El recurso proporcionado en el cuerpo de la solicitud se encuentra en estado de `Locked` y no se puede crear solicitudes de asignación de rol.</span><span class="sxs-lookup"><span data-stu-id="bfe01-196">The resource provided in the request body is in state of `Locked` and cannot create role assignment requests.</span></span>
| <span data-ttu-id="bfe01-197">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="bfe01-197">400 BadRequest</span></span> | <span data-ttu-id="bfe01-198">SubjectNotFound</span><span class="sxs-lookup"><span data-stu-id="bfe01-198">SubjectNotFound</span></span>    | <span data-ttu-id="bfe01-199">El `subjectId` proporcionado en la solicitud no se encuentra el cuerpo.</span><span class="sxs-lookup"><span data-stu-id="bfe01-199">The `subjectId` provided in the request body cannot be found.</span></span>
| <span data-ttu-id="bfe01-200">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="bfe01-200">400 BadRequest</span></span> | <span data-ttu-id="bfe01-201">PendingRoleAssignmentRequest</span><span class="sxs-lookup"><span data-stu-id="bfe01-201">PendingRoleAssignmentRequest</span></span>    | <span data-ttu-id="bfe01-202">Ya existe una pendiente [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) en el sistema.</span><span class="sxs-lookup"><span data-stu-id="bfe01-202">There already exists a pending [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) in the system.</span></span>
| <span data-ttu-id="bfe01-203">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="bfe01-203">400 BadRequest</span></span> | <span data-ttu-id="bfe01-204">RoleAssignmentExists</span><span class="sxs-lookup"><span data-stu-id="bfe01-204">RoleAssignmentExists</span></span>    | <span data-ttu-id="bfe01-205">El [governanceRoleAssignment](../resources/governanceroleassignment.md) solicitada que se va a crear ya existe en el sistema.</span><span class="sxs-lookup"><span data-stu-id="bfe01-205">The [governanceRoleAssignment](../resources/governanceroleassignment.md) requested to be created already exists in the system.</span></span>
| <span data-ttu-id="bfe01-206">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="bfe01-206">400 BadRequest</span></span> | <span data-ttu-id="bfe01-207">RoleAssignmentDoesNotExist</span><span class="sxs-lookup"><span data-stu-id="bfe01-207">RoleAssignmentDoesNotExist</span></span>    | <span data-ttu-id="bfe01-208">El [governanceRoleAssignment](../resources/governanceroleassignment.md) solicitado se actualizó y ampliar no existe en el sistema.</span><span class="sxs-lookup"><span data-stu-id="bfe01-208">The [governanceRoleAssignment](../resources/governanceroleassignment.md) requested to be updated/extended does not exist in the system.</span></span>
| <span data-ttu-id="bfe01-209">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="bfe01-209">400 BadRequest</span></span> | <span data-ttu-id="bfe01-210">RoleAssignmentRequestPolicyValidationFailed</span><span class="sxs-lookup"><span data-stu-id="bfe01-210">RoleAssignmentRequestPolicyValidationFailed</span></span> | <span data-ttu-id="bfe01-211">La [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) no cumple las políticas internas y no se puede crear.</span><span class="sxs-lookup"><span data-stu-id="bfe01-211">The [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) does not meet internal policies and cannot be created.</span></span>

## <a name="examples"></a><span data-ttu-id="bfe01-212">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bfe01-212">Examples</span></span>
<span data-ttu-id="bfe01-213">Los siguientes ejemplos muestran cómo usar esta API.</span><span class="sxs-lookup"><span data-stu-id="bfe01-213">The following examples show how to use this API.</span></span>

### <a name="example-1"></a><span data-ttu-id="bfe01-214">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="bfe01-214">Example 1</span></span>
<span data-ttu-id="bfe01-215">En este ejemplo, los administradores asignan nawu@fimdev.net usuario a la función de lector de facturación.</span><span class="sxs-lookup"><span data-stu-id="bfe01-215">In this example, administrators assign user nawu@fimdev.net to the Billing Reader role.</span></span>

 ><span data-ttu-id="bfe01-216">**Nota:** Además de los permisos, en este ejemplo se requiere que el solicitante tiene al menos una `Active` asignación de roles de administrador (`owner` o `user access administrator`) en el recurso.</span><span class="sxs-lookup"><span data-stu-id="bfe01-216">**Note:** In addition to the permission, this example requires that the requester have at least one `Active` adminstrator role assignment (`owner` or `user access administrator`) on the resource.</span></span> 

| <span data-ttu-id="bfe01-217">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bfe01-217">Property</span></span>     | <span data-ttu-id="bfe01-218">Tipo</span><span class="sxs-lookup"><span data-stu-id="bfe01-218">Type</span></span>    |<span data-ttu-id="bfe01-219">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="bfe01-219">Required</span></span>|  <span data-ttu-id="bfe01-220">Valor</span><span class="sxs-lookup"><span data-stu-id="bfe01-220">Value</span></span> |
|:---------------|:--------|:----------|:----------|
|<span data-ttu-id="bfe01-221">resourceId</span><span class="sxs-lookup"><span data-stu-id="bfe01-221">resourceId</span></span>|<span data-ttu-id="bfe01-222">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-222">String</span></span>|<span data-ttu-id="bfe01-223">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-223">Yes</span></span>|<span data-ttu-id="bfe01-224">\<resourceId\></span><span class="sxs-lookup"><span data-stu-id="bfe01-224">\<resourceId\></span></span>|
|<span data-ttu-id="bfe01-225">roleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="bfe01-225">roleDefinitionId</span></span>|<span data-ttu-id="bfe01-226">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-226">String</span></span>|<span data-ttu-id="bfe01-227">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-227">Yes</span></span>|<span data-ttu-id="bfe01-228">\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="bfe01-228">\<roleDefinitionId\></span></span>|
|<span data-ttu-id="bfe01-229">///SubjectID</span><span class="sxs-lookup"><span data-stu-id="bfe01-229">subjectId</span></span>|<span data-ttu-id="bfe01-230">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-230">String</span></span>|<span data-ttu-id="bfe01-231">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-231">Yes</span></span>|<span data-ttu-id="bfe01-232">\<///SubjectID\></span><span class="sxs-lookup"><span data-stu-id="bfe01-232">\<subjectId\></span></span>|
|<span data-ttu-id="bfe01-233">assignmentState</span><span class="sxs-lookup"><span data-stu-id="bfe01-233">assignmentState</span></span>|<span data-ttu-id="bfe01-234">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-234">String</span></span>|<span data-ttu-id="bfe01-235">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-235">Yes</span></span>| <span data-ttu-id="bfe01-236">Optan / activo</span><span class="sxs-lookup"><span data-stu-id="bfe01-236">Eligible / Active</span></span>|
|<span data-ttu-id="bfe01-237">type</span><span class="sxs-lookup"><span data-stu-id="bfe01-237">type</span></span>|<span data-ttu-id="bfe01-238">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-238">String</span></span>|<span data-ttu-id="bfe01-239">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-239">Yes</span></span>| <span data-ttu-id="bfe01-240">AdminAdd</span><span class="sxs-lookup"><span data-stu-id="bfe01-240">AdminAdd</span></span>|
|<span data-ttu-id="bfe01-241">motivo</span><span class="sxs-lookup"><span data-stu-id="bfe01-241">reason</span></span>|<span data-ttu-id="bfe01-242">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-242">String</span></span>| <span data-ttu-id="bfe01-243">depende de la función configuración</span><span class="sxs-lookup"><span data-stu-id="bfe01-243">depends on role Settings</span></span>||
|<span data-ttu-id="bfe01-244">programación</span><span class="sxs-lookup"><span data-stu-id="bfe01-244">schedule</span></span>|[<span data-ttu-id="bfe01-245">governanceSchedule</span><span class="sxs-lookup"><span data-stu-id="bfe01-245">governanceSchedule</span></span>](../resources/governanceschedule.md)|<span data-ttu-id="bfe01-246">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-246">Yes</span></span>|        |
##### <a name="request"></a><span data-ttu-id="bfe01-247">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bfe01-247">Request</span></span>
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
##### <a name="response"></a><span data-ttu-id="bfe01-248">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bfe01-248">Response</span></span>
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

### <a name="example-2"></a><span data-ttu-id="bfe01-249">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="bfe01-249">Example 2</span></span>
<span data-ttu-id="bfe01-250">En este ejemplo, el usuario nawu@fimdev.net activa la función de lector de facturación optan.</span><span class="sxs-lookup"><span data-stu-id="bfe01-250">In this example, the user nawu@fimdev.net activates the eligible Billing Reader role.</span></span>

| <span data-ttu-id="bfe01-251">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bfe01-251">Property</span></span>     | <span data-ttu-id="bfe01-252">Tipo</span><span class="sxs-lookup"><span data-stu-id="bfe01-252">Type</span></span>    |<span data-ttu-id="bfe01-253">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="bfe01-253">Required</span></span>|  <span data-ttu-id="bfe01-254">Valor</span><span class="sxs-lookup"><span data-stu-id="bfe01-254">Value</span></span> |
|:---------------|:--------|:----------|:----------|
|<span data-ttu-id="bfe01-255">resourceId</span><span class="sxs-lookup"><span data-stu-id="bfe01-255">resourceId</span></span>|<span data-ttu-id="bfe01-256">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-256">String</span></span>|<span data-ttu-id="bfe01-257">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-257">Yes</span></span>|<span data-ttu-id="bfe01-258">\<resourceId\></span><span class="sxs-lookup"><span data-stu-id="bfe01-258">\<resourceId\></span></span>|
|<span data-ttu-id="bfe01-259">roleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="bfe01-259">roleDefinitionId</span></span>|<span data-ttu-id="bfe01-260">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-260">String</span></span>|<span data-ttu-id="bfe01-261">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-261">Yes</span></span>|<span data-ttu-id="bfe01-262">\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="bfe01-262">\<roleDefinitionId\></span></span>|
|<span data-ttu-id="bfe01-263">///SubjectID</span><span class="sxs-lookup"><span data-stu-id="bfe01-263">subjectId</span></span>|<span data-ttu-id="bfe01-264">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-264">String</span></span>|<span data-ttu-id="bfe01-265">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-265">Yes</span></span>|<span data-ttu-id="bfe01-266">\<///SubjectID\></span><span class="sxs-lookup"><span data-stu-id="bfe01-266">\<subjectId\></span></span>|
|<span data-ttu-id="bfe01-267">assignmentState</span><span class="sxs-lookup"><span data-stu-id="bfe01-267">assignmentState</span></span>|<span data-ttu-id="bfe01-268">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-268">String</span></span>|<span data-ttu-id="bfe01-269">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-269">Yes</span></span>| <span data-ttu-id="bfe01-270">Activo</span><span class="sxs-lookup"><span data-stu-id="bfe01-270">Active</span></span>|
|<span data-ttu-id="bfe01-271">type</span><span class="sxs-lookup"><span data-stu-id="bfe01-271">type</span></span>|<span data-ttu-id="bfe01-272">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-272">String</span></span>|<span data-ttu-id="bfe01-273">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-273">Yes</span></span>| <span data-ttu-id="bfe01-274">Comandos UserAdd</span><span class="sxs-lookup"><span data-stu-id="bfe01-274">UserAdd</span></span>|
|<span data-ttu-id="bfe01-275">motivo</span><span class="sxs-lookup"><span data-stu-id="bfe01-275">reason</span></span>|<span data-ttu-id="bfe01-276">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-276">String</span></span>| <span data-ttu-id="bfe01-277">depende de la función configuración</span><span class="sxs-lookup"><span data-stu-id="bfe01-277">depends on role Settings</span></span>||
|<span data-ttu-id="bfe01-278">programación</span><span class="sxs-lookup"><span data-stu-id="bfe01-278">schedule</span></span>|[<span data-ttu-id="bfe01-279">governanceSchedule</span><span class="sxs-lookup"><span data-stu-id="bfe01-279">governanceSchedule</span></span>](../resources/governanceschedule.md)|<span data-ttu-id="bfe01-280">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-280">Yes</span></span>|        |
##### <a name="request"></a><span data-ttu-id="bfe01-281">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bfe01-281">Request</span></span>
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
##### <a name="response"></a><span data-ttu-id="bfe01-282">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bfe01-282">Response</span></span>
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

### <a name="example-3"></a><span data-ttu-id="bfe01-283">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="bfe01-283">Example 3</span></span>
<span data-ttu-id="bfe01-284">En este ejemplo, el usuario nawu@fimdev.net desactiva la función de lector de facturación activada.</span><span class="sxs-lookup"><span data-stu-id="bfe01-284">In this example, the user nawu@fimdev.net deactivates the active Billing Reader role.</span></span>

| <span data-ttu-id="bfe01-285">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bfe01-285">Property</span></span>     | <span data-ttu-id="bfe01-286">Tipo</span><span class="sxs-lookup"><span data-stu-id="bfe01-286">Type</span></span>    |<span data-ttu-id="bfe01-287">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="bfe01-287">Required</span></span>|  <span data-ttu-id="bfe01-288">Valor</span><span class="sxs-lookup"><span data-stu-id="bfe01-288">Value</span></span> |
|:---------------|:--------|:----------|:----------|
|<span data-ttu-id="bfe01-289">resourceId</span><span class="sxs-lookup"><span data-stu-id="bfe01-289">resourceId</span></span>|<span data-ttu-id="bfe01-290">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-290">String</span></span>|<span data-ttu-id="bfe01-291">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-291">Yes</span></span>|<span data-ttu-id="bfe01-292">\<resourceId\></span><span class="sxs-lookup"><span data-stu-id="bfe01-292">\<resourceId\></span></span>|
|<span data-ttu-id="bfe01-293">roleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="bfe01-293">roleDefinitionId</span></span>|<span data-ttu-id="bfe01-294">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-294">String</span></span>|<span data-ttu-id="bfe01-295">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-295">Yes</span></span>|<span data-ttu-id="bfe01-296">\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="bfe01-296">\<roleDefinitionId\></span></span>|
|<span data-ttu-id="bfe01-297">///SubjectID</span><span class="sxs-lookup"><span data-stu-id="bfe01-297">subjectId</span></span>|<span data-ttu-id="bfe01-298">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-298">String</span></span>|<span data-ttu-id="bfe01-299">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-299">Yes</span></span>|<span data-ttu-id="bfe01-300">\<///SubjectID\></span><span class="sxs-lookup"><span data-stu-id="bfe01-300">\<subjectId\></span></span>|
|<span data-ttu-id="bfe01-301">assignmentState</span><span class="sxs-lookup"><span data-stu-id="bfe01-301">assignmentState</span></span>|<span data-ttu-id="bfe01-302">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-302">String</span></span>|<span data-ttu-id="bfe01-303">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-303">Yes</span></span>| <span data-ttu-id="bfe01-304">Activo</span><span class="sxs-lookup"><span data-stu-id="bfe01-304">Active</span></span>|
|<span data-ttu-id="bfe01-305">type</span><span class="sxs-lookup"><span data-stu-id="bfe01-305">type</span></span>|<span data-ttu-id="bfe01-306">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-306">String</span></span>|<span data-ttu-id="bfe01-307">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-307">Yes</span></span>| <span data-ttu-id="bfe01-308">UserRemove</span><span class="sxs-lookup"><span data-stu-id="bfe01-308">UserRemove</span></span>|
|<span data-ttu-id="bfe01-309">motivo</span><span class="sxs-lookup"><span data-stu-id="bfe01-309">reason</span></span>|<span data-ttu-id="bfe01-310">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-310">String</span></span>| <span data-ttu-id="bfe01-311">No</span><span class="sxs-lookup"><span data-stu-id="bfe01-311">No</span></span>||
|<span data-ttu-id="bfe01-312">programación</span><span class="sxs-lookup"><span data-stu-id="bfe01-312">schedule</span></span>|[<span data-ttu-id="bfe01-313">governanceSchedule</span><span class="sxs-lookup"><span data-stu-id="bfe01-313">governanceSchedule</span></span>](../resources/governanceschedule.md)|<span data-ttu-id="bfe01-314">No</span><span class="sxs-lookup"><span data-stu-id="bfe01-314">No</span></span>|        |
##### <a name="request"></a><span data-ttu-id="bfe01-315">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bfe01-315">Request</span></span>
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
##### <a name="response"></a><span data-ttu-id="bfe01-316">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bfe01-316">Response</span></span>
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
    "reason": "Evaluate only",
    "schedule": null,
    "status": {
        "status": "Closed",
        "subStatus": "Revoked",
        "statusDetails": []
    }
}
```

### <a name="example-4"></a><span data-ttu-id="bfe01-317">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="bfe01-317">Example 4</span></span>
<span data-ttu-id="bfe01-318">En este ejemplo, los administradores de quitar el usuario nawu@fimdev.net de la función de lector de facturación.</span><span class="sxs-lookup"><span data-stu-id="bfe01-318">In this example, administrators remove the user nawu@fimdev.net from the Billing Reader role.</span></span>

 ><span data-ttu-id="bfe01-319">**Nota:** Además de los permisos, en este ejemplo se requiere que el solicitante tiene al menos una `Active` asignación de roles de administrador (`owner` o `user access administrator`) en el recurso.</span><span class="sxs-lookup"><span data-stu-id="bfe01-319">**Note:** In addition to the permission, this example requires that the requester have at least one `Active` adminstrator role assignment (`owner` or `user access administrator`) on the resource.</span></span>
 
| <span data-ttu-id="bfe01-320">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bfe01-320">Property</span></span>     | <span data-ttu-id="bfe01-321">Tipo</span><span class="sxs-lookup"><span data-stu-id="bfe01-321">Type</span></span>    |<span data-ttu-id="bfe01-322">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="bfe01-322">Required</span></span>|  <span data-ttu-id="bfe01-323">Valor</span><span class="sxs-lookup"><span data-stu-id="bfe01-323">Value</span></span> |
|:---------------|:--------|:----------|:----------|
|<span data-ttu-id="bfe01-324">resourceId</span><span class="sxs-lookup"><span data-stu-id="bfe01-324">resourceId</span></span>|<span data-ttu-id="bfe01-325">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-325">String</span></span>|<span data-ttu-id="bfe01-326">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-326">Yes</span></span>|<span data-ttu-id="bfe01-327">\<resourceId\></span><span class="sxs-lookup"><span data-stu-id="bfe01-327">\<resourceId\></span></span>|
|<span data-ttu-id="bfe01-328">roleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="bfe01-328">roleDefinitionId</span></span>|<span data-ttu-id="bfe01-329">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-329">String</span></span>|<span data-ttu-id="bfe01-330">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-330">Yes</span></span>|<span data-ttu-id="bfe01-331">\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="bfe01-331">\<roleDefinitionId\></span></span>|
|<span data-ttu-id="bfe01-332">///SubjectID</span><span class="sxs-lookup"><span data-stu-id="bfe01-332">subjectId</span></span>|<span data-ttu-id="bfe01-333">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-333">String</span></span>|<span data-ttu-id="bfe01-334">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-334">Yes</span></span>|<span data-ttu-id="bfe01-335">\<///SubjectID\></span><span class="sxs-lookup"><span data-stu-id="bfe01-335">\<subjectId\></span></span>|
|<span data-ttu-id="bfe01-336">assignmentState</span><span class="sxs-lookup"><span data-stu-id="bfe01-336">assignmentState</span></span>|<span data-ttu-id="bfe01-337">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-337">String</span></span>|<span data-ttu-id="bfe01-338">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-338">Yes</span></span>| <span data-ttu-id="bfe01-339">Optan / activo</span><span class="sxs-lookup"><span data-stu-id="bfe01-339">Eligible / Active</span></span>|
|<span data-ttu-id="bfe01-340">type</span><span class="sxs-lookup"><span data-stu-id="bfe01-340">type</span></span>|<span data-ttu-id="bfe01-341">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-341">String</span></span>|<span data-ttu-id="bfe01-342">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-342">Yes</span></span>| <span data-ttu-id="bfe01-343">AdminRemove</span><span class="sxs-lookup"><span data-stu-id="bfe01-343">AdminRemove</span></span>|
|<span data-ttu-id="bfe01-344">motivo</span><span class="sxs-lookup"><span data-stu-id="bfe01-344">reason</span></span>|<span data-ttu-id="bfe01-345">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-345">String</span></span>| <span data-ttu-id="bfe01-346">No</span><span class="sxs-lookup"><span data-stu-id="bfe01-346">No</span></span>||
|<span data-ttu-id="bfe01-347">programación</span><span class="sxs-lookup"><span data-stu-id="bfe01-347">schedule</span></span>|[<span data-ttu-id="bfe01-348">governanceSchedule</span><span class="sxs-lookup"><span data-stu-id="bfe01-348">governanceSchedule</span></span>](../resources/governanceschedule.md)|<span data-ttu-id="bfe01-349">No</span><span class="sxs-lookup"><span data-stu-id="bfe01-349">No</span></span>|        |
##### <a name="request"></a><span data-ttu-id="bfe01-350">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bfe01-350">Request</span></span>
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
##### <a name="response"></a><span data-ttu-id="bfe01-351">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bfe01-351">Response</span></span>
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
  "reason":null,
  "status":{
    "status":"Closed",
    "subStatus":"Revoked",
    "statusDetails":[]
  },
  "schedule":null
}
```

### <a name="example-5"></a><span data-ttu-id="bfe01-352">Ejemplo 5</span><span class="sxs-lookup"><span data-stu-id="bfe01-352">Example 5</span></span>
<span data-ttu-id="bfe01-353">En este ejemplo, los administradores actualizar la asignación de rol para el usuario nawu@fimdev.net al propietario.</span><span class="sxs-lookup"><span data-stu-id="bfe01-353">In this example, administrators update the role assignment for the user nawu@fimdev.net to Owner.</span></span>

 ><span data-ttu-id="bfe01-354">**Nota:** Además de los permisos, en este ejemplo se requiere que el solicitante tiene al menos una `Active` asignación de roles de administrador (`owner` o `user access administrator`) en el recurso.</span><span class="sxs-lookup"><span data-stu-id="bfe01-354">**Note:** In addition to the permission, this example requires that the requester have at least one `Active` adminstrator role assignment (`owner` or `user access administrator`) on the resource.</span></span> 

| <span data-ttu-id="bfe01-355">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bfe01-355">Property</span></span>     | <span data-ttu-id="bfe01-356">Tipo</span><span class="sxs-lookup"><span data-stu-id="bfe01-356">Type</span></span>    |<span data-ttu-id="bfe01-357">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="bfe01-357">Required</span></span>|  <span data-ttu-id="bfe01-358">Valor</span><span class="sxs-lookup"><span data-stu-id="bfe01-358">Value</span></span> |
|:---------------|:--------|:----------|:----------|
|<span data-ttu-id="bfe01-359">resourceId</span><span class="sxs-lookup"><span data-stu-id="bfe01-359">resourceId</span></span>|<span data-ttu-id="bfe01-360">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-360">String</span></span>|<span data-ttu-id="bfe01-361">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-361">Yes</span></span>|<span data-ttu-id="bfe01-362">\<resourceId\></span><span class="sxs-lookup"><span data-stu-id="bfe01-362">\<resourceId\></span></span>|
|<span data-ttu-id="bfe01-363">roleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="bfe01-363">roleDefinitionId</span></span>|<span data-ttu-id="bfe01-364">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-364">String</span></span>|<span data-ttu-id="bfe01-365">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-365">Yes</span></span>|<span data-ttu-id="bfe01-366">\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="bfe01-366">\<roleDefinitionId\></span></span>|
|<span data-ttu-id="bfe01-367">///SubjectID</span><span class="sxs-lookup"><span data-stu-id="bfe01-367">subjectId</span></span>|<span data-ttu-id="bfe01-368">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-368">String</span></span>|<span data-ttu-id="bfe01-369">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-369">Yes</span></span>|<span data-ttu-id="bfe01-370">\<///SubjectID\></span><span class="sxs-lookup"><span data-stu-id="bfe01-370">\<subjectId\></span></span>|
|<span data-ttu-id="bfe01-371">assignmentState</span><span class="sxs-lookup"><span data-stu-id="bfe01-371">assignmentState</span></span>|<span data-ttu-id="bfe01-372">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-372">String</span></span>|<span data-ttu-id="bfe01-373">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-373">Yes</span></span>| <span data-ttu-id="bfe01-374">Optan / activo</span><span class="sxs-lookup"><span data-stu-id="bfe01-374">Eligible / Active</span></span>|
|<span data-ttu-id="bfe01-375">type</span><span class="sxs-lookup"><span data-stu-id="bfe01-375">type</span></span>|<span data-ttu-id="bfe01-376">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-376">String</span></span>|<span data-ttu-id="bfe01-377">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-377">Yes</span></span>| <span data-ttu-id="bfe01-378">AdminUpdate</span><span class="sxs-lookup"><span data-stu-id="bfe01-378">AdminUpdate</span></span>|
|<span data-ttu-id="bfe01-379">motivo</span><span class="sxs-lookup"><span data-stu-id="bfe01-379">reason</span></span>|<span data-ttu-id="bfe01-380">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-380">String</span></span>| <span data-ttu-id="bfe01-381">depende de roleSettings</span><span class="sxs-lookup"><span data-stu-id="bfe01-381">depends on roleSettings</span></span>||
|<span data-ttu-id="bfe01-382">programación</span><span class="sxs-lookup"><span data-stu-id="bfe01-382">schedule</span></span>|[<span data-ttu-id="bfe01-383">governanceSchedule</span><span class="sxs-lookup"><span data-stu-id="bfe01-383">governanceSchedule</span></span>](../resources/governanceschedule.md)|<span data-ttu-id="bfe01-384">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-384">Yes</span></span>|        |
##### <a name="request"></a><span data-ttu-id="bfe01-385">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bfe01-385">Request</span></span>
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
##### <a name="response"></a><span data-ttu-id="bfe01-386">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bfe01-386">Response</span></span>
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

### <a name="example-6"></a><span data-ttu-id="bfe01-387">Ejemplo 6</span><span class="sxs-lookup"><span data-stu-id="bfe01-387">Example 6</span></span>
<span data-ttu-id="bfe01-388">En este ejemplo se extiende la asignación de roles a punto de expirar para usuario ANUJCUSER a la API de administración de servicio colaborador.</span><span class="sxs-lookup"><span data-stu-id="bfe01-388">This example extends the expiring role assignment for user ANUJCUSER to API Management Service Contributor.</span></span>

 ><span data-ttu-id="bfe01-389">**Nota:** Aparte de los permisos, en este ejemplo se requiere que el solicitante tiene al menos una `Active` asignación de roles de administrador (`owner` o `user access administrator`) en el recurso.</span><span class="sxs-lookup"><span data-stu-id="bfe01-389">**Note:** In additon to the permission, this example requires that the requester have at least one `Active` adminstrator role assignment (`owner` or `user access administrator`) on the resource.</span></span>
 
| <span data-ttu-id="bfe01-390">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bfe01-390">Property</span></span>     | <span data-ttu-id="bfe01-391">Tipo</span><span class="sxs-lookup"><span data-stu-id="bfe01-391">Type</span></span>    |<span data-ttu-id="bfe01-392">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="bfe01-392">Required</span></span>|  <span data-ttu-id="bfe01-393">Valor</span><span class="sxs-lookup"><span data-stu-id="bfe01-393">Value</span></span> |
|:---------------|:--------|:----------|:----------|
|<span data-ttu-id="bfe01-394">resourceId</span><span class="sxs-lookup"><span data-stu-id="bfe01-394">resourceId</span></span>|<span data-ttu-id="bfe01-395">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-395">String</span></span>|<span data-ttu-id="bfe01-396">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-396">Yes</span></span>|<span data-ttu-id="bfe01-397">\<resourceId\></span><span class="sxs-lookup"><span data-stu-id="bfe01-397">\<resourceId\></span></span>|
|<span data-ttu-id="bfe01-398">roleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="bfe01-398">roleDefinitionId</span></span>|<span data-ttu-id="bfe01-399">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-399">String</span></span>|<span data-ttu-id="bfe01-400">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-400">Yes</span></span>|<span data-ttu-id="bfe01-401">\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="bfe01-401">\<roleDefinitionId\></span></span>|
|<span data-ttu-id="bfe01-402">///SubjectID</span><span class="sxs-lookup"><span data-stu-id="bfe01-402">subjectId</span></span>|<span data-ttu-id="bfe01-403">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-403">String</span></span>|<span data-ttu-id="bfe01-404">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-404">Yes</span></span>|<span data-ttu-id="bfe01-405">\<///SubjectID\></span><span class="sxs-lookup"><span data-stu-id="bfe01-405">\<subjectId\></span></span>|
|<span data-ttu-id="bfe01-406">assignmentState</span><span class="sxs-lookup"><span data-stu-id="bfe01-406">assignmentState</span></span>|<span data-ttu-id="bfe01-407">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-407">String</span></span>|<span data-ttu-id="bfe01-408">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-408">Yes</span></span>| <span data-ttu-id="bfe01-409">Optan / activo</span><span class="sxs-lookup"><span data-stu-id="bfe01-409">Eligible / Active</span></span> |
|<span data-ttu-id="bfe01-410">type</span><span class="sxs-lookup"><span data-stu-id="bfe01-410">type</span></span>|<span data-ttu-id="bfe01-411">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-411">String</span></span>|<span data-ttu-id="bfe01-412">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-412">Yes</span></span>| <span data-ttu-id="bfe01-413">AdminExtend</span><span class="sxs-lookup"><span data-stu-id="bfe01-413">AdminExtend</span></span>|
|<span data-ttu-id="bfe01-414">motivo</span><span class="sxs-lookup"><span data-stu-id="bfe01-414">reason</span></span>|<span data-ttu-id="bfe01-415">Cadena</span><span class="sxs-lookup"><span data-stu-id="bfe01-415">String</span></span>| <span data-ttu-id="bfe01-416">depende de roleSettings</span><span class="sxs-lookup"><span data-stu-id="bfe01-416">depends on roleSettings</span></span>||
|<span data-ttu-id="bfe01-417">programación</span><span class="sxs-lookup"><span data-stu-id="bfe01-417">schedule</span></span>|[<span data-ttu-id="bfe01-418">governanceSchedule</span><span class="sxs-lookup"><span data-stu-id="bfe01-418">governanceSchedule</span></span>](../resources/governanceschedule.md)|<span data-ttu-id="bfe01-419">Sí</span><span class="sxs-lookup"><span data-stu-id="bfe01-419">Yes</span></span>|        |
##### <a name="request"></a><span data-ttu-id="bfe01-420">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bfe01-420">Request</span></span>
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
##### <a name="response"></a><span data-ttu-id="bfe01-421">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bfe01-421">Response</span></span>
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
