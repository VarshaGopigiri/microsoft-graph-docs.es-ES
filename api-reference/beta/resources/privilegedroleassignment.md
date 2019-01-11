---
title: tipo de recurso privilegedRoleAssignment
description: 'Representa una asignación de roles con privilegios de un usuario concreto. '
localization_priority: Normal
ms.openlocfilehash: ec6bc34ecd56839c764592ff298475e8648f300b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27823320"
---
# <a name="privilegedroleassignment-resource-type"></a><span data-ttu-id="060c7-103">tipo de recurso privilegedRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="060c7-103">privilegedRoleAssignment resource type</span></span>

> <span data-ttu-id="060c7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="060c7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="060c7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="060c7-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="060c7-106">Representa una asignación de roles con privilegios de un usuario concreto.</span><span class="sxs-lookup"><span data-stu-id="060c7-106">Represents a privileged role assignment for a particular user.</span></span> 


## <a name="methods"></a><span data-ttu-id="060c7-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="060c7-107">Methods</span></span>

| <span data-ttu-id="060c7-108">Método</span><span class="sxs-lookup"><span data-stu-id="060c7-108">Method</span></span>           | <span data-ttu-id="060c7-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="060c7-109">Return Type</span></span>    |<span data-ttu-id="060c7-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="060c7-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="060c7-111">Colección de listas de privilegedRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="060c7-111">List privilegedRoleAssignment collection</span></span>](../api/privilegedroleassignment-list.md) | <span data-ttu-id="060c7-112">colección de [privilegedRoleAssignment](privilegedroleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="060c7-112">[privilegedRoleAssignment](privilegedroleassignment.md) collection</span></span>|<span data-ttu-id="060c7-113">Obtener la colección de objetos privilegedRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="060c7-113">Get the collection of privilegedRoleAssignment objects.</span></span>|
|[<span data-ttu-id="060c7-114">Obtener privilegedRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="060c7-114">Get privilegedRoleAssignment</span></span>](../api/privilegedroleassignment-get.md) | [<span data-ttu-id="060c7-115">privilegedRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="060c7-115">privilegedRoleAssignment</span></span>](privilegedroleassignment.md) |<span data-ttu-id="060c7-116">Leer las propiedades y las relaciones del objeto privilegedRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="060c7-116">Read properties and relationships of privilegedRoleAssignment object.</span></span>|
|[<span data-ttu-id="060c7-117">Crear asignación</span><span class="sxs-lookup"><span data-stu-id="060c7-117">Create assignment</span></span>](../api/privilegedroleassignment-post-privilegedroleassignments.md) |[<span data-ttu-id="060c7-118">privilegedRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="060c7-118">privilegedRoleAssignment</span></span>](privilegedroleassignment.md)| <span data-ttu-id="060c7-119">Crear una nueva asignación de la publicación de la colección de asignaciones.</span><span class="sxs-lookup"><span data-stu-id="060c7-119">Create a new assignment by posting to the assignments collection.</span></span>|
|[<span data-ttu-id="060c7-120">Delete</span><span class="sxs-lookup"><span data-stu-id="060c7-120">Delete</span></span>](../api/privilegedroleassignment-delete.md) | <span data-ttu-id="060c7-121">Ninguno</span><span class="sxs-lookup"><span data-stu-id="060c7-121">None</span></span> |<span data-ttu-id="060c7-122">Eliminar el objeto privilegedRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="060c7-122">Delete privilegedRoleAssignment object.</span></span> |
|[<span data-ttu-id="060c7-123">makePermanent</span><span class="sxs-lookup"><span data-stu-id="060c7-123">makePermanent</span></span>](../api/privilegedroleassignment-makepermanent.md)|[<span data-ttu-id="060c7-124">privilegedRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="060c7-124">privilegedRoleAssignment</span></span>](privilegedroleassignment.md)|<span data-ttu-id="060c7-125">Hacer que la asignación de rol como permanente.</span><span class="sxs-lookup"><span data-stu-id="060c7-125">Make the role assignment as permanent.</span></span>|
|[<span data-ttu-id="060c7-126">makeEligible</span><span class="sxs-lookup"><span data-stu-id="060c7-126">makeEligible</span></span>](../api/privilegedroleassignment-makeeligible.md)|[<span data-ttu-id="060c7-127">privilegedRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="060c7-127">privilegedRoleAssignment</span></span>](privilegedroleassignment.md)|<span data-ttu-id="060c7-128">Hacer que la asignación de rol como elegibles.</span><span class="sxs-lookup"><span data-stu-id="060c7-128">Make the role assignment as eligible.</span></span>|
|[<span data-ttu-id="060c7-129">Mi</span><span class="sxs-lookup"><span data-stu-id="060c7-129">my</span></span>](../api/privilegedroleassignment-my.md)|<span data-ttu-id="060c7-130">colección de [privilegedRoleAssignment](privilegedroleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="060c7-130">[privilegedRoleAssignment](privilegedroleassignment.md) collection</span></span>|<span data-ttu-id="060c7-131">Obtener las asignaciones de roles con privilegios del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="060c7-131">Get the current user's privileged role assignments.</span></span>|

## <a name="properties"></a><span data-ttu-id="060c7-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="060c7-132">Properties</span></span>
| <span data-ttu-id="060c7-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="060c7-133">Property</span></span>     | <span data-ttu-id="060c7-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="060c7-134">Type</span></span>   |<span data-ttu-id="060c7-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="060c7-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="060c7-136">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="060c7-136">expirationDateTime</span></span>|<span data-ttu-id="060c7-137">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="060c7-137">dateTimeOffset</span></span>|<span data-ttu-id="060c7-138">La estructura de DateTime de UTC cuando la asignación de roles con privilegios temporal caducará.</span><span class="sxs-lookup"><span data-stu-id="060c7-138">The UTC DateTime when the temporary privileged role assignment will be expired.</span></span> <span data-ttu-id="060c7-139">Para la asignación de rol permanente, el valor es null.</span><span class="sxs-lookup"><span data-stu-id="060c7-139">For permanent role assignment, the value is null.</span></span>|
|<span data-ttu-id="060c7-140">id</span><span class="sxs-lookup"><span data-stu-id="060c7-140">id</span></span>|<span data-ttu-id="060c7-141">string</span><span class="sxs-lookup"><span data-stu-id="060c7-141">string</span></span>| <span data-ttu-id="060c7-142">El identificador único para la asignación de roles con privilegios.</span><span class="sxs-lookup"><span data-stu-id="060c7-142">The unique identifier for the privileged role assignment.</span></span> <span data-ttu-id="060c7-143">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="060c7-143">Read-only.</span></span> <span data-ttu-id="060c7-144">Está en el formato de 'userId_roleId', donde userId es la cadena GUID para el identificador de usuario de Azure AD y el identificador de función es la cadena GUID para el identificador de rol de administrador de Azure.</span><span class="sxs-lookup"><span data-stu-id="060c7-144">It is in the format of 'userId_roleId', where userId is the GUID string for Azure AD user id, and roleId is the GUID string for Azure administrator role id.</span></span>|
|<span data-ttu-id="060c7-145">isElevated</span><span class="sxs-lookup"><span data-stu-id="060c7-145">isElevated</span></span>|<span data-ttu-id="060c7-146">boolean</span><span class="sxs-lookup"><span data-stu-id="060c7-146">boolean</span></span>|<span data-ttu-id="060c7-147">**true** si se activa la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="060c7-147">**true** if the role assignment is activated.</span></span> <span data-ttu-id="060c7-148">**false** si se desactiva la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="060c7-148">**false** if the role assignment is deactivated.</span></span>|
|<span data-ttu-id="060c7-149">resultMessage</span><span class="sxs-lookup"><span data-stu-id="060c7-149">resultMessage</span></span>|<span data-ttu-id="060c7-150">string</span><span class="sxs-lookup"><span data-stu-id="060c7-150">string</span></span>|<span data-ttu-id="060c7-151">Mensaje de resultado establecido por el servicio.</span><span class="sxs-lookup"><span data-stu-id="060c7-151">Result message set by the service.</span></span>|
|<span data-ttu-id="060c7-152">identificador de función</span><span class="sxs-lookup"><span data-stu-id="060c7-152">roleId</span></span>|<span data-ttu-id="060c7-153">string</span><span class="sxs-lookup"><span data-stu-id="060c7-153">string</span></span>|<span data-ttu-id="060c7-154">Identificador de rol.</span><span class="sxs-lookup"><span data-stu-id="060c7-154">Role identifier.</span></span> <span data-ttu-id="060c7-155">GUID en formato de cadena.</span><span class="sxs-lookup"><span data-stu-id="060c7-155">In GUID string format.</span></span>|
|<span data-ttu-id="060c7-156">userId</span><span class="sxs-lookup"><span data-stu-id="060c7-156">userId</span></span>|<span data-ttu-id="060c7-157">string</span><span class="sxs-lookup"><span data-stu-id="060c7-157">string</span></span>|<span data-ttu-id="060c7-158">Identificador de usuario.</span><span class="sxs-lookup"><span data-stu-id="060c7-158">User identifier.</span></span> <span data-ttu-id="060c7-159">GUID en formato de cadena.</span><span class="sxs-lookup"><span data-stu-id="060c7-159">In GUID string format.</span></span>|

## <a name="relationships"></a><span data-ttu-id="060c7-160">Relaciones</span><span class="sxs-lookup"><span data-stu-id="060c7-160">Relationships</span></span>
| <span data-ttu-id="060c7-161">Relación</span><span class="sxs-lookup"><span data-stu-id="060c7-161">Relationship</span></span> | <span data-ttu-id="060c7-162">Tipo</span><span class="sxs-lookup"><span data-stu-id="060c7-162">Type</span></span>   |<span data-ttu-id="060c7-163">Description</span><span class="sxs-lookup"><span data-stu-id="060c7-163">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="060c7-164">roleInfo</span><span class="sxs-lookup"><span data-stu-id="060c7-164">roleInfo</span></span>|[<span data-ttu-id="060c7-165">privilegedRole</span><span class="sxs-lookup"><span data-stu-id="060c7-165">privilegedRole</span></span>](privilegedrole.md)| <span data-ttu-id="060c7-166">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="060c7-166">Read-only.</span></span> <span data-ttu-id="060c7-167">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="060c7-167">Nullable.</span></span> <span data-ttu-id="060c7-168">La información de la función asociada.</span><span class="sxs-lookup"><span data-stu-id="060c7-168">The associated role information.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="060c7-169">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="060c7-169">JSON representation</span></span>

<span data-ttu-id="060c7-170">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="060c7-170">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.privilegedRoleAssignment"
}-->

```json
{
  "expirationDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "isElevated": true,
  "resultMessage": "string",
  "roleId": "string",
  "userId": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "privilegedRoleAssignment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
