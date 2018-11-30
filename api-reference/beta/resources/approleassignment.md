---
title: tipo de recurso appRoleAssignment
description: Se usa para registrar cuándo un usuario o grupo se asigna a una aplicación. En este caso, la asignación de roles, se producirá un icono de aplicación visible copia de seguridad en el panel de acceso de aplicación del usuario. Esta entidad también se puede usar para conceder acceso de otra aplicación (que se modela como un entidad de seguridad de servicio) a una aplicación de recursos en una función determinada. Puede crear, leer, actualizar y eliminar las asignaciones de roles.
ms.openlocfilehash: 97155bde12735ebd8a7674e0dbf20dae30e53f14
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084604"
---
# <a name="approleassignment-resource-type"></a><span data-ttu-id="fb611-106">tipo de recurso appRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="fb611-106">appRoleAssignment resource type</span></span>

> <span data-ttu-id="fb611-107">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fb611-107">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fb611-108">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fb611-108">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fb611-109">Se usa para registrar cuándo un usuario o grupo se asigna a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="fb611-109">Used to record when a user or group is assigned to an application.</span></span> <span data-ttu-id="fb611-110">En este caso, la asignación de roles, se producirá un icono de aplicación visible copia de seguridad en el panel de acceso de aplicación del usuario.</span><span class="sxs-lookup"><span data-stu-id="fb611-110">In this case, the role assignment will result in an application tile showing up on the user's app access panel.</span></span> <span data-ttu-id="fb611-111">Esta entidad también se puede usar para conceder acceso de otra aplicación (que se modela como un entidad de seguridad de servicio) a una aplicación de recursos en una función determinada.</span><span class="sxs-lookup"><span data-stu-id="fb611-111">This entity may also be used to grant another application (modeled as a service principal) access to a resource application in a particular role.</span></span> <span data-ttu-id="fb611-112">Puede crear, leer, actualizar y eliminar las asignaciones de roles.</span><span class="sxs-lookup"><span data-stu-id="fb611-112">You can create, read, update, and delete role assignments.</span></span>


## <a name="json-representation"></a><span data-ttu-id="fb611-113">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fb611-113">JSON representation</span></span>

<span data-ttu-id="fb611-114">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="fb611-114">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.approleassignment"
}-->

```json
{
  "creationTimestamp": "String (timestamp)",
  "id": "guid (identifier)",
  "principalDisplayName": "string",
  "principalId": "guid",
  "principalType": "string",
  "resourceDisplayName": "string",
  "resourceId": "guid"
}

```
## <a name="properties"></a><span data-ttu-id="fb611-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fb611-115">Properties</span></span>
| <span data-ttu-id="fb611-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fb611-116">Property</span></span>     | <span data-ttu-id="fb611-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb611-117">Type</span></span>   |<span data-ttu-id="fb611-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb611-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fb611-119">creationTimestamp</span><span class="sxs-lookup"><span data-stu-id="fb611-119">creationTimestamp</span></span>|<span data-ttu-id="fb611-120">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="fb611-120">DateTimeOffset</span></span>|<span data-ttu-id="fb611-121">La hora de creación de la concesión. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="fb611-121">The time when the grant was created.The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="fb611-122">Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="fb611-122">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="fb611-123">id</span><span class="sxs-lookup"><span data-stu-id="fb611-123">id</span></span>|<span data-ttu-id="fb611-124">Guid</span><span class="sxs-lookup"><span data-stu-id="fb611-124">Guid</span></span>|<span data-ttu-id="fb611-125">El identificador de rol que se asignó a la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="fb611-125">The role id that was assigned to the principal.</span></span>  <span data-ttu-id="fb611-126">Esta función se debe declarar por el de aplicación de destino recursos **resourceId** en su propiedad **appRoles** .</span><span class="sxs-lookup"><span data-stu-id="fb611-126">This role must be declared by the target resource application **resourceId** in its **appRoles** property.</span></span> <span data-ttu-id="fb611-127">Donde el recurso no declarar los permisos, debe especificarse un identificador predeterminado (identificador GUID cero).</span><span class="sxs-lookup"><span data-stu-id="fb611-127">Where the resource does not declare any permissions, a default id (zero GUID) must be specified.</span></span> <span data-ttu-id="fb611-128">Clave.</span><span class="sxs-lookup"><span data-stu-id="fb611-128">Key.</span></span> <span data-ttu-id="fb611-129">No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="fb611-129">Not nullable.</span></span> |
|<span data-ttu-id="fb611-130">principalDisplayName</span><span class="sxs-lookup"><span data-stu-id="fb611-130">principalDisplayName</span></span>|<span data-ttu-id="fb611-131">String</span><span class="sxs-lookup"><span data-stu-id="fb611-131">String</span></span>|<span data-ttu-id="fb611-132">El nombre para mostrar de la entidad de seguridad que se ha concedido el acceso.</span><span class="sxs-lookup"><span data-stu-id="fb611-132">The display name of the principal that was granted the access.</span></span>|
|<span data-ttu-id="fb611-133">principalId</span><span class="sxs-lookup"><span data-stu-id="fb611-133">principalId</span></span>|<span data-ttu-id="fb611-134">Guid</span><span class="sxs-lookup"><span data-stu-id="fb611-134">Guid</span></span>|<span data-ttu-id="fb611-135">El identificador único (**Id.**) de la entidad de seguridad que se van a conceder el acceso.</span><span class="sxs-lookup"><span data-stu-id="fb611-135">The unique identifier (**id**) for the principal being granted the access.</span></span> <span data-ttu-id="fb611-136">Necesarios en crear.</span><span class="sxs-lookup"><span data-stu-id="fb611-136">Required on create.</span></span>            |
|<span data-ttu-id="fb611-137">principalType</span><span class="sxs-lookup"><span data-stu-id="fb611-137">principalType</span></span>|<span data-ttu-id="fb611-138">String</span><span class="sxs-lookup"><span data-stu-id="fb611-138">String</span></span>|<span data-ttu-id="fb611-139">El tipo de entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="fb611-139">The type of principal.</span></span>  <span data-ttu-id="fb611-140">Esto puede ser "User", "ServicePrincipal" o "Grupo".</span><span class="sxs-lookup"><span data-stu-id="fb611-140">This can either be "User", "Group" or "ServicePrincipal".</span></span>|
|<span data-ttu-id="fb611-141">resourceDisplayName</span><span class="sxs-lookup"><span data-stu-id="fb611-141">resourceDisplayName</span></span>|<span data-ttu-id="fb611-142">String</span><span class="sxs-lookup"><span data-stu-id="fb611-142">String</span></span>|<span data-ttu-id="fb611-143">El nombre para mostrar del recurso al que se realizó la asignación.</span><span class="sxs-lookup"><span data-stu-id="fb611-143">The display name of the resource to which the assignment was made.</span></span>|
|<span data-ttu-id="fb611-144">resourceId</span><span class="sxs-lookup"><span data-stu-id="fb611-144">resourceId</span></span>|<span data-ttu-id="fb611-145">Guid</span><span class="sxs-lookup"><span data-stu-id="fb611-145">Guid</span></span>|<span data-ttu-id="fb611-146">El identificador único (**Id.**) para el recurso de destino (entidad de seguridad de servicio) para el que se realizó la asignación.</span><span class="sxs-lookup"><span data-stu-id="fb611-146">The unique identifier (**id**) for the target resource (service principal) for which the assignment was made.</span></span>|

## <a name="relationships"></a><span data-ttu-id="fb611-147">Relaciones</span><span class="sxs-lookup"><span data-stu-id="fb611-147">Relationships</span></span>
<span data-ttu-id="fb611-148">Ninguno</span><span class="sxs-lookup"><span data-stu-id="fb611-148">None</span></span>


## <a name="methods"></a><span data-ttu-id="fb611-149">Métodos</span><span class="sxs-lookup"><span data-stu-id="fb611-149">Methods</span></span>

| <span data-ttu-id="fb611-150">Método</span><span class="sxs-lookup"><span data-stu-id="fb611-150">Method</span></span>           | <span data-ttu-id="fb611-151">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb611-151">Return Type</span></span>    |<span data-ttu-id="fb611-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb611-152">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="fb611-153">Obtener appRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="fb611-153">Get appRoleAssignment</span></span>](../api/approleassignment-get.md) | [<span data-ttu-id="fb611-154">appRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="fb611-154">appRoleAssignment</span></span>](approleassignment.md) |<span data-ttu-id="fb611-155">Leer las propiedades y las relaciones del objeto appRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="fb611-155">Read properties and relationships of appRoleAssignment object.</span></span>|
|[<span data-ttu-id="fb611-156">Update</span><span class="sxs-lookup"><span data-stu-id="fb611-156">Update</span></span>](../api/approleassignment-update.md) | [<span data-ttu-id="fb611-157">appRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="fb611-157">appRoleAssignment</span></span>](approleassignment.md)   |<span data-ttu-id="fb611-158">Actualizar el objeto appRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="fb611-158">Update appRoleAssignment object.</span></span> |
|[<span data-ttu-id="fb611-159">Delete</span><span class="sxs-lookup"><span data-stu-id="fb611-159">Delete</span></span>](../api/approleassignment-delete.md) | <span data-ttu-id="fb611-160">Ninguno</span><span class="sxs-lookup"><span data-stu-id="fb611-160">None</span></span> |<span data-ttu-id="fb611-161">Eliminar el objeto appRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="fb611-161">Delete appRoleAssignment object.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "appRoleAssignment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->