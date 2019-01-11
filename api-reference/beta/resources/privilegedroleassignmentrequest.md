---
title: tipo de recurso privilegedRoleAssignmentRequest
description: Representa la solicitud para operaciones de asignación de rol de administración de identidades de Privilegd.
localization_priority: Normal
ms.openlocfilehash: bfe3b6802136b2848f36abef08134efd0eb82518
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27880132"
---
# <a name="privilegedroleassignmentrequest-resource-type"></a><span data-ttu-id="16cac-103">tipo de recurso privilegedRoleAssignmentRequest</span><span class="sxs-lookup"><span data-stu-id="16cac-103">privilegedRoleAssignmentRequest resource type</span></span>

> <span data-ttu-id="16cac-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="16cac-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="16cac-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="16cac-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="16cac-106">Representa la solicitud para operaciones de asignación de rol de administración de identidades de Privilegd.</span><span class="sxs-lookup"><span data-stu-id="16cac-106">Represents the request for role assignment operations in Privilegd Identity Management.</span></span>

<span data-ttu-id="16cac-107">`privilegedRoleAssignmentRequest`se utiliza una entidad modelar vale para administrar el ciclo de vida de las asignaciones de roles.</span><span class="sxs-lookup"><span data-stu-id="16cac-107">`privilegedRoleAssignmentRequest` is a ticket-modeled entity used to manage the lifecycle of role assignments.</span></span> <span data-ttu-id="16cac-108">Representa la intención o la decisión de los usuarios y administradores y también proporciona la flexibilidad necesaria para permitir la implementación de schduling periódico, puertas de aprobación y así sucesivamente, con respecto a exponer directamente `POST` y `LIST` operaciones, así como `MY` y `Cancel` funciona en `governanceRoleAssignment`.</span><span class="sxs-lookup"><span data-stu-id="16cac-108">It represents the intention/decision of the users and administrators, and also provides the flexibility to enable implementation of recurrent schduling, approval gates, and so on, as compared to directly exposing `POST` and `LIST` operations as well as `MY` and `Cancel` functions on `governanceRoleAssignment`.</span></span>

## <a name="methods"></a><span data-ttu-id="16cac-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="16cac-109">Methods</span></span>

| <span data-ttu-id="16cac-110">Método</span><span class="sxs-lookup"><span data-stu-id="16cac-110">Method</span></span>       | <span data-ttu-id="16cac-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="16cac-111">Return Type</span></span> | <span data-ttu-id="16cac-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="16cac-112">Description</span></span> |
|:-------------|:------------|:------------|
|[<span data-ttu-id="16cac-113">List</span><span class="sxs-lookup"><span data-stu-id="16cac-113">List</span></span>](../api/privilegedroleassignmentrequest-list.md) | <span data-ttu-id="16cac-114">colección de [privilegedroleassignmentrequest](../resources/privilegedroleassignmentrequest.md)</span><span class="sxs-lookup"><span data-stu-id="16cac-114">[privilegedroleassignmentrequest](../resources/privilegedroleassignmentrequest.md)  collection</span></span>|<span data-ttu-id="16cac-115">Las solicitudes de asignación de rol de la lista.</span><span class="sxs-lookup"><span data-stu-id="16cac-115">List role assignment requests.</span></span>|
|[<span data-ttu-id="16cac-116">Create</span><span class="sxs-lookup"><span data-stu-id="16cac-116">Create</span></span>](../api/privilegedroleassignmentrequest-post.md)|  [<span data-ttu-id="16cac-117">privilegedroleassignmentrequest</span><span class="sxs-lookup"><span data-stu-id="16cac-117">privilegedroleassignmentrequest</span></span>](../resources/privilegedroleassignmentrequest.md)|<span data-ttu-id="16cac-118">Cree una solicitud para administrar el ciclo de vida de la asignación de rol nuevo o existente.</span><span class="sxs-lookup"><span data-stu-id="16cac-118">Create a request to manage the lifecycle of existing or new role assignment.</span></span>|
|[<span data-ttu-id="16cac-119">Cancel</span><span class="sxs-lookup"><span data-stu-id="16cac-119">Cancel</span></span>](../api/privilegedroleassignmentrequest-cancel.md)|  |<span data-ttu-id="16cac-120">Cancelar una solicitud de asignación de roles pendiente.</span><span class="sxs-lookup"><span data-stu-id="16cac-120">Cancel a pending role assignment request.</span></span>|
|[<span data-ttu-id="16cac-121">My</span><span class="sxs-lookup"><span data-stu-id="16cac-121">My</span></span>](../api/privilegedroleassignmentrequest-my.md)|  |<span data-ttu-id="16cac-122">Obtener la solicitud de asignación de rol para requstor actual.</span><span class="sxs-lookup"><span data-stu-id="16cac-122">Get role assignment request for current requstor.</span></span>|

## <a name="properties"></a><span data-ttu-id="16cac-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="16cac-123">Properties</span></span>

| <span data-ttu-id="16cac-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="16cac-124">Property</span></span>     | <span data-ttu-id="16cac-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="16cac-125">Type</span></span>        | <span data-ttu-id="16cac-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="16cac-126">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="16cac-127">id</span><span class="sxs-lookup"><span data-stu-id="16cac-127">id</span></span>|<span data-ttu-id="16cac-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="16cac-128">String</span></span>| <span data-ttu-id="16cac-129">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="16cac-129">Read-only.</span></span> <span data-ttu-id="16cac-130">El identificador de la solicitud de asignación de rol.</span><span class="sxs-lookup"><span data-stu-id="16cac-130">The id of the role assignment request.</span></span>|
|<span data-ttu-id="16cac-131">assignmentState</span><span class="sxs-lookup"><span data-stu-id="16cac-131">assignmentState</span></span>|<span data-ttu-id="16cac-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="16cac-132">String</span></span>| <span data-ttu-id="16cac-133">El estado de la asignación.</span><span class="sxs-lookup"><span data-stu-id="16cac-133">The state of the assignment.</span></span> <span data-ttu-id="16cac-134">El valor puede ser `Eligible` para asignación optan `Active` - si está asignada directamente `Active` por los administradores, o activado en una asignación optan por los usuarios.</span><span class="sxs-lookup"><span data-stu-id="16cac-134">The value can be `Eligible` for eligible assignment `Active` - if it is directly assigned `Active` by administrators, or activated on an eligible assignment by the users.</span></span>|
|<span data-ttu-id="16cac-135">duration</span><span class="sxs-lookup"><span data-stu-id="16cac-135">duration</span></span>|<span data-ttu-id="16cac-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="16cac-136">String</span></span>| <span data-ttu-id="16cac-137">La duración de una asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="16cac-137">The duration of a role assignment.</span></span>|
|<span data-ttu-id="16cac-138">motivo</span><span class="sxs-lookup"><span data-stu-id="16cac-138">reason</span></span>|<span data-ttu-id="16cac-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="16cac-139">String</span></span>| <span data-ttu-id="16cac-140">El motivo de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="16cac-140">The reason for the role assignment.</span></span>|
|<span data-ttu-id="16cac-141">requestedDateTime</span><span class="sxs-lookup"><span data-stu-id="16cac-141">requestedDateTime</span></span>|<span data-ttu-id="16cac-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="16cac-142">DateTimeOffset</span></span>| <span data-ttu-id="16cac-143">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="16cac-143">Read-only.</span></span> <span data-ttu-id="16cac-144">La solicitud de creación de tiempo.</span><span class="sxs-lookup"><span data-stu-id="16cac-144">The request create time.</span></span> <span data-ttu-id="16cac-145">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="16cac-145">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="16cac-146">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="16cac-146">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="16cac-147">identificador de función</span><span class="sxs-lookup"><span data-stu-id="16cac-147">roleId</span></span>|<span data-ttu-id="16cac-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="16cac-148">String</span></span>| <span data-ttu-id="16cac-149">El identificador de la función.</span><span class="sxs-lookup"><span data-stu-id="16cac-149">The id of the role.</span></span>|
|<span data-ttu-id="16cac-150">programación</span><span class="sxs-lookup"><span data-stu-id="16cac-150">schedule</span></span>|[<span data-ttu-id="16cac-151">governanceSchedule</span><span class="sxs-lookup"><span data-stu-id="16cac-151">governanceSchedule</span></span>](governanceschedule.md)| <span data-ttu-id="16cac-152">El objeto de programación de la solicitud de asignación de rol.</span><span class="sxs-lookup"><span data-stu-id="16cac-152">The schedule object of the role assignment request.</span></span>|
|<span data-ttu-id="16cac-153">status</span><span class="sxs-lookup"><span data-stu-id="16cac-153">status</span></span>|<span data-ttu-id="16cac-154">Cadena</span><span class="sxs-lookup"><span data-stu-id="16cac-154">String</span></span>| <span data-ttu-id="16cac-155">Lectura cascada.se el estado de la solicitud de asignación de rol.</span><span class="sxs-lookup"><span data-stu-id="16cac-155">Read-only.The status of the role assignment request.</span></span> <span data-ttu-id="16cac-156">El valor puede ser `NotStarted`,`Completed`,`RequestedApproval`,`Scheduled`,`Approved`,`ApprovalDenied`,`ApprovalAborted`,`Cancelling`,`Cancelled`,`Revoked`,`RequestExpired`.</span><span class="sxs-lookup"><span data-stu-id="16cac-156">The value can be `NotStarted`,`Completed`,`RequestedApproval`,`Scheduled`,`Approved`,`ApprovalDenied`,`ApprovalAborted`,`Cancelling`,`Cancelled`,`Revoked`,`RequestExpired`.</span></span>|
|<span data-ttu-id="16cac-157">ticketNumber</span><span class="sxs-lookup"><span data-stu-id="16cac-157">ticketNumber</span></span>|<span data-ttu-id="16cac-158">Cadena</span><span class="sxs-lookup"><span data-stu-id="16cac-158">String</span></span>| <span data-ttu-id="16cac-159">TicketNumber para la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="16cac-159">The ticketNumber for the role assignment.</span></span> |
|<span data-ttu-id="16cac-160">ticketSystem</span><span class="sxs-lookup"><span data-stu-id="16cac-160">ticketSystem</span></span>|<span data-ttu-id="16cac-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="16cac-161">String</span></span>| <span data-ttu-id="16cac-162">TicketSystem para la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="16cac-162">The ticketSystem for the role assignment.</span></span>|
|<span data-ttu-id="16cac-163">type</span><span class="sxs-lookup"><span data-stu-id="16cac-163">type</span></span>|<span data-ttu-id="16cac-164">Cadena</span><span class="sxs-lookup"><span data-stu-id="16cac-164">String</span></span>| <span data-ttu-id="16cac-165">Que representa el tipo de la operación en la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="16cac-165">Representing the the type of the operation on the role assignment.</span></span> <span data-ttu-id="16cac-166">El valor puede ser `AdminAdd`: administradores agregar usuarios a funciones; `UserAdd`: Los usuarios agregar las asignaciones de roles.</span><span class="sxs-lookup"><span data-stu-id="16cac-166">The value can be `AdminAdd`: Adminstrators add users to roles;`UserAdd`: Users add role assignments.</span></span>|
|<span data-ttu-id="16cac-167">userId</span><span class="sxs-lookup"><span data-stu-id="16cac-167">userId</span></span>|<span data-ttu-id="16cac-168">Cadena</span><span class="sxs-lookup"><span data-stu-id="16cac-168">String</span></span>| <span data-ttu-id="16cac-169">El identificador del usuario.</span><span class="sxs-lookup"><span data-stu-id="16cac-169">The id of the user.</span></span>|

## <a name="relationships"></a><span data-ttu-id="16cac-170">Relaciones</span><span class="sxs-lookup"><span data-stu-id="16cac-170">Relationships</span></span>
| <span data-ttu-id="16cac-171">Relación</span><span class="sxs-lookup"><span data-stu-id="16cac-171">Relationship</span></span> | <span data-ttu-id="16cac-172">Tipo</span><span class="sxs-lookup"><span data-stu-id="16cac-172">Type</span></span>        | <span data-ttu-id="16cac-173">Description</span><span class="sxs-lookup"><span data-stu-id="16cac-173">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="16cac-174">roleInfo</span><span class="sxs-lookup"><span data-stu-id="16cac-174">roleInfo</span></span>|[<span data-ttu-id="16cac-175">privilegedRole</span><span class="sxs-lookup"><span data-stu-id="16cac-175">privilegedRole</span></span>](privilegedrole.md)| <span data-ttu-id="16cac-176">El objeto roleInfo de la solicitud de asignación de rol.</span><span class="sxs-lookup"><span data-stu-id="16cac-176">The roleInfo object of the role assignment request.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="16cac-177">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="16cac-177">JSON representation</span></span>

<span data-ttu-id="16cac-178">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="16cac-178">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.privilegedRoleAssignmentRequest"
}-->

```json
{
  "assignmentState": "String",
  "duration": "String",
  "id": "String (identifier)",
  "reason": "String",
  "requestedDateTime": "String (timestamp)",
  "roleId": "String",
  "schedule": {"@odata.type": "microsoft.graph.governanceSchedule"},
  "status": "String",
  "ticketNumber": "String",
  "ticketSystem": "String",
  "type": "String",
  "userId": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "privilegedRoleAssignmentRequest resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
