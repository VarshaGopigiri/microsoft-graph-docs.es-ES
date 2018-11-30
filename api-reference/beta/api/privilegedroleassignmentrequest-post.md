---
title: Crear privilegedRoleAssignmentRequest
description: Crear un objeto privilegedroleassignmentrequest.
ms.openlocfilehash: e262682b5a5e8bffa7fb089ae783f3bb7e67803c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087071"
---
# <a name="create-privilegedroleassignmentrequest"></a><span data-ttu-id="f7cd2-103">Crear privilegedRoleAssignmentRequest</span><span class="sxs-lookup"><span data-stu-id="f7cd2-103">Create privilegedRoleAssignmentRequest</span></span>

> <span data-ttu-id="f7cd2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f7cd2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f7cd2-106">Crear un objeto [privilegedroleassignmentrequest](../resources/privilegedroleassignmentrequest.md) .</span><span class="sxs-lookup"><span data-stu-id="f7cd2-106">Create a [privilegedroleassignmentrequest](../resources/privilegedroleassignmentrequest.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="f7cd2-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="f7cd2-107">Permissions</span></span>
<span data-ttu-id="f7cd2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f7cd2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f7cd2-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f7cd2-110">Permission type</span></span>                        | <span data-ttu-id="f7cd2-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f7cd2-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="f7cd2-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f7cd2-112">Delegated (work or school account)</span></span> | <span data-ttu-id="f7cd2-113">PrivilegedAccess.ReadWrite.AzureAD, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="f7cd2-113">PrivilegedAccess.ReadWrite.AzureAD, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="f7cd2-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f7cd2-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f7cd2-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-115">Not supported.</span></span> |
|<span data-ttu-id="f7cd2-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f7cd2-116">Application</span></span>                            | <span data-ttu-id="f7cd2-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f7cd2-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f7cd2-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /privilegedRoleAssignmentRequests
```

## <a name="request-headers"></a><span data-ttu-id="f7cd2-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f7cd2-119">Request headers</span></span>
| <span data-ttu-id="f7cd2-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7cd2-120">Name</span></span>      |<span data-ttu-id="f7cd2-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7cd2-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="f7cd2-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="f7cd2-122">Authorization</span></span>  | <span data-ttu-id="f7cd2-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f7cd2-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f7cd2-125">Request body</span></span>
<span data-ttu-id="f7cd2-126">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [privilegedroleassignmentrequest](../resources/privilegedroleassignmentrequest.md) .</span><span class="sxs-lookup"><span data-stu-id="f7cd2-126">In the request body, supply a JSON representation of [privilegedroleassignmentrequest](../resources/privilegedroleassignmentrequest.md) object.</span></span> 

| <span data-ttu-id="f7cd2-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f7cd2-127">Property</span></span>     | <span data-ttu-id="f7cd2-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="f7cd2-128">Type</span></span>    |  <span data-ttu-id="f7cd2-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7cd2-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f7cd2-130">identificador de función</span><span class="sxs-lookup"><span data-stu-id="f7cd2-130">roleId</span></span>|<span data-ttu-id="f7cd2-131">String</span><span class="sxs-lookup"><span data-stu-id="f7cd2-131">String</span></span>|<span data-ttu-id="f7cd2-132">El identificador de la función.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-132">The ID of the role.</span></span> <span data-ttu-id="f7cd2-133">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-133">Required.</span></span>|
|<span data-ttu-id="f7cd2-134">type</span><span class="sxs-lookup"><span data-stu-id="f7cd2-134">type</span></span>|<span data-ttu-id="f7cd2-135">String</span><span class="sxs-lookup"><span data-stu-id="f7cd2-135">String</span></span>|<span data-ttu-id="f7cd2-136">Representa el tipo de la operación en la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-136">Represents the the type of the operation on the role assignment.</span></span> <span data-ttu-id="f7cd2-137">El valor puede ser `AdminAdd`: administradores agregar usuarios a funciones; `UserAdd`: Los usuarios agregar las asignaciones de roles.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-137">The value can be `AdminAdd`: Adminstrators add users to roles;`UserAdd`: Users add role assignments.</span></span> <span data-ttu-id="f7cd2-138">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-138">Required.</span></span>|
|<span data-ttu-id="f7cd2-139">assignmentState</span><span class="sxs-lookup"><span data-stu-id="f7cd2-139">assignmentState</span></span>|<span data-ttu-id="f7cd2-140">String</span><span class="sxs-lookup"><span data-stu-id="f7cd2-140">String</span></span>|<span data-ttu-id="f7cd2-141">El estado de la asignación.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-141">The state of the assignment.</span></span> <span data-ttu-id="f7cd2-142">El valor puede ser `Eligible` para asignación optan `Active` - si está asignada directamente `Active` por los administradores, o activado en una asignación optan por los usuarios.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-142">The value can be `Eligible` for eligible assignment `Active` - if it is directly assigned `Active` by administrators, or activated on an eligible assignment by the users.</span></span> <span data-ttu-id="f7cd2-143">Los valores posibles son: ``NotStarted``, `Completed`, `RequestedApproval`, `Scheduled`, `Approved`, `ApprovalDenied`, `ApprovalAborted`, `Cancelling`, `Cancelled`, `Revoked` y `RequestExpired`.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-143">Possible values are: ``NotStarted``, `Completed`, `RequestedApproval`, `Scheduled`, `Approved`, `ApprovalDenied`, `ApprovalAborted`, `Cancelling`, `Cancelled`, `Revoked`, `RequestExpired`.</span></span> <span data-ttu-id="f7cd2-144">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-144">Required.</span></span>|
|<span data-ttu-id="f7cd2-145">motivo</span><span class="sxs-lookup"><span data-stu-id="f7cd2-145">reason</span></span>|<span data-ttu-id="f7cd2-146">String</span><span class="sxs-lookup"><span data-stu-id="f7cd2-146">String</span></span>|<span data-ttu-id="f7cd2-147">Necesita la razón por la que se proporcionará para la solicitud de asignación de rol para auditoría y revise el propósito.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-147">The reason needs to be provided for the role assignment request for audit and review purpose.</span></span>|
|<span data-ttu-id="f7cd2-148">programación</span><span class="sxs-lookup"><span data-stu-id="f7cd2-148">schedule</span></span>|[<span data-ttu-id="f7cd2-149">governanceSchedule</span><span class="sxs-lookup"><span data-stu-id="f7cd2-149">governanceSchedule</span></span>](../resources/governanceschedule.md)|<span data-ttu-id="f7cd2-150">La programación de la solicitud de asignación de rol.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-150">The schedule of the role assignment request.</span></span>|

## <a name="response"></a><span data-ttu-id="f7cd2-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f7cd2-151">Response</span></span>
<span data-ttu-id="f7cd2-152">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [privilegedRoleAssignmentRequest](../resources/privilegedroleassignmentrequest.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-152">If successful, this method returns a `201 Created` response code and a [privilegedRoleAssignmentRequest](../resources/privilegedroleassignmentrequest.md) object in the response body.</span></span>

### <a name="error-codes"></a><span data-ttu-id="f7cd2-153">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="f7cd2-153">Error codes</span></span>
<span data-ttu-id="f7cd2-154">Esta API devuelve ese estándar de códigos de error HTTP.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-154">This API returns that standard HTTP error codes.</span></span> <span data-ttu-id="f7cd2-155">Además, puede devolver los códigos de error que aparecen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-155">In addition, it can return the error codes listed in the following table.</span></span>

|<span data-ttu-id="f7cd2-156">Código de error</span><span class="sxs-lookup"><span data-stu-id="f7cd2-156">Error code</span></span>     | <span data-ttu-id="f7cd2-157">Mensaje de error</span><span class="sxs-lookup"><span data-stu-id="f7cd2-157">Error message</span></span>              | 
|:--------------------| :---------------------|
| <span data-ttu-id="f7cd2-158">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="f7cd2-158">400 BadRequest</span></span> | <span data-ttu-id="f7cd2-159">Propiedad RoleAssignmentRequest es NULL.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-159">RoleAssignmentRequest property was NULL</span></span> |
| <span data-ttu-id="f7cd2-160">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="f7cd2-160">400 BadRequest</span></span> | <span data-ttu-id="f7cd2-161">No se puede deserializar roleAssignmentRequest objeto.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-161">Unable to deserialize roleAssignmentRequest Object.</span></span> |
| <span data-ttu-id="f7cd2-162">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="f7cd2-162">400 BadRequest</span></span> | <span data-ttu-id="f7cd2-163">Se requiere el identificador de función.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-163">RoleId is required.</span></span> |
| <span data-ttu-id="f7cd2-164">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="f7cd2-164">400 BadRequest</span></span> | <span data-ttu-id="f7cd2-165">Fecha de inicio de la programación debe especificarse y debe ser mayor que este momento.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-165">Schedule start date must be specified and should be greater than Now.</span></span> |
| <span data-ttu-id="f7cd2-166">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="f7cd2-166">400 BadRequest</span></span> | <span data-ttu-id="f7cd2-167">Ya existe una programación para este tipo de usuario, la función y la programación.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-167">A schedule already exists for this user, role and schedule type.</span></span> |
| <span data-ttu-id="f7cd2-168">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="f7cd2-168">400 BadRequest</span></span> | <span data-ttu-id="f7cd2-169">Una aprobación pendiente ya existe para este tipo de usuario, la función y la aprobación.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-169">A pending approval already exists for this user, role and approval type.</span></span> |
| <span data-ttu-id="f7cd2-170">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="f7cd2-170">400 BadRequest</span></span> | <span data-ttu-id="f7cd2-171">Falta la razón del solicitante.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-171">Requestor reason is missing.</span></span> |
| <span data-ttu-id="f7cd2-172">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="f7cd2-172">400 BadRequest</span></span> | <span data-ttu-id="f7cd2-173">Razón del solicitante debe ser inferior a 500 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-173">Requestor reason should be less than 500 characters.</span></span> |
| <span data-ttu-id="f7cd2-174">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="f7cd2-174">400 BadRequest</span></span> | <span data-ttu-id="f7cd2-175">Duración de elevación debe estar entre 0,5 y {desde configuración}.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-175">Elevation duration must be between 0.5 and {from setting}.</span></span> |
| <span data-ttu-id="f7cd2-176">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="f7cd2-176">400 BadRequest</span></span> | <span data-ttu-id="f7cd2-177">Hay una superposición entre la activación programada y la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-177">There is a overlap between scheduled activation and the request.</span></span> |
| <span data-ttu-id="f7cd2-178">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="f7cd2-178">400 BadRequest</span></span> | <span data-ttu-id="f7cd2-179">La función ya está activada.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-179">The role is already activated.</span></span> |
| <span data-ttu-id="f7cd2-180">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="f7cd2-180">400 BadRequest</span></span> | <span data-ttu-id="f7cd2-181">GenericElevateUserToRoleAssignments: Tickting información es necesaria y no se proporciona en el proceso de activación.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-181">GenericElevateUserToRoleAssignments: Tickting information is required and not supplied in the activation process.</span></span> |
| <span data-ttu-id="f7cd2-182">400 BadRequest</span><span class="sxs-lookup"><span data-stu-id="f7cd2-182">400 BadRequest</span></span> | <span data-ttu-id="f7cd2-183">Hay una superposición entre la activación programada y la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-183">There is a overlap between scheduled activation and the request.</span></span> |
| <span data-ttu-id="f7cd2-184">403 no autorizado</span><span class="sxs-lookup"><span data-stu-id="f7cd2-184">403 UnAuthorized</span></span> | <span data-ttu-id="f7cd2-185">Elevación requiere autenticación multifactor.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-185">Elevation requires Multi-Factor Authentication.</span></span> |
| <span data-ttu-id="f7cd2-186">403 no autorizado</span><span class="sxs-lookup"><span data-stu-id="f7cd2-186">403 UnAuthorized</span></span> | <span data-ttu-id="f7cd2-187">No se permite en nombre de elevación.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-187">On behalf of elevation is not allowed.</span></span> |

## <a name="example"></a><span data-ttu-id="f7cd2-188">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7cd2-188">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f7cd2-189">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f7cd2-189">Request</span></span>
<span data-ttu-id="f7cd2-190">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-190">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "post_privilegedroleassignmentrequest"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedRoleAssignmentRequests
Content-type: application/json

{
    "duration": "2",
    "reason": "Activate the role for business purpose",
    "ticketNumber": "234",
    "ticketSystem": "system",
    "schedule": {
        "startDateTime": "2018-02-08T02:35:17.903Z"
    },
    "evaluateOnly": false,
    "type": "UserAdd",
    "assignmentState": "Active",
    "roleId": "88d8e3e3-8f55-4a1e-953a-9b9898b8876b"
}
```
##### <a name="response"></a><span data-ttu-id="f7cd2-191">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f7cd2-191">Response</span></span>
<span data-ttu-id="f7cd2-192">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-192">The following is an example of the response.</span></span> <span data-ttu-id="f7cd2-193">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-193">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="f7cd2-194">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f7cd2-194">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedRoleAssignmentRequest"
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
    "id": "e13ef8a0-c1cb-4d03-aaae-9cd1c8ede2d1",
    "evaluateOnly": false,
    "type": "UserAdd",
    "assignmentState": "Active",
    "requestedDateTime": "2018-02-08T02:35:42.9137335Z",
    "status": "NotStarted",
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
  "description": "Post privilegedRoleAssignmentRequest",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
