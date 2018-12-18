---
title: Tipo de recurso roleAssignment
description: El recurso de la asignación de roles. Las asignaciones de roles unen la definición de rol con miembros y ámbitos. Puede haber una o más asignaciones de roles por rol. Esto se aplica a los roles integrados y personalizados.
author: tfitzmac
ms.openlocfilehash: 5c4b09151a7957f52dbaa525f696b89479a898ef
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27302103"
---
# <a name="roleassignment-resource-type"></a><span data-ttu-id="b02dc-106">Tipo de recurso roleAssignment</span><span class="sxs-lookup"><span data-stu-id="b02dc-106">roleAssignment resource type</span></span>

> <span data-ttu-id="b02dc-107">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b02dc-107">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b02dc-108">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b02dc-108">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b02dc-109">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b02dc-109">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b02dc-110">El recurso de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="b02dc-110">The Role Assignment resource.</span></span> <span data-ttu-id="b02dc-111">Las asignaciones de roles unen la definición de rol con miembros y ámbitos.</span><span class="sxs-lookup"><span data-stu-id="b02dc-111">Role assignments tie together a role definition with members and scopes.</span></span> <span data-ttu-id="b02dc-112">Puede haber una o más asignaciones de roles por rol.</span><span class="sxs-lookup"><span data-stu-id="b02dc-112">There can be one or more role assignments per role.</span></span> <span data-ttu-id="b02dc-113">Esto se aplica a los roles integrados y personalizados.</span><span class="sxs-lookup"><span data-stu-id="b02dc-113">This applies to custom and built-in roles.</span></span>
## <a name="methods"></a><span data-ttu-id="b02dc-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="b02dc-114">Methods</span></span>
|<span data-ttu-id="b02dc-115">Método</span><span class="sxs-lookup"><span data-stu-id="b02dc-115">Method</span></span>|<span data-ttu-id="b02dc-116">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b02dc-116">Return Type</span></span>|<span data-ttu-id="b02dc-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b02dc-117">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="b02dc-118">Enumerar roleAssignments</span><span class="sxs-lookup"><span data-stu-id="b02dc-118">List roleAssignments</span></span>](../api/intune-rbac-roleassignment-list.md)|<span data-ttu-id="b02dc-119">Colección [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="b02dc-119">[roleAssignment](../resources/intune-rbac-roleassignment.md) collection</span></span>|<span data-ttu-id="b02dc-120">Enumere las propiedades y las relaciones de los objetos [roleAssignment](../resources/intune-rbac-roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="b02dc-120">List properties and relationships of the [roleAssignment](../resources/intune-rbac-roleassignment.md) objects.</span></span>|
|[<span data-ttu-id="b02dc-121">Obtener roleAssignment</span><span class="sxs-lookup"><span data-stu-id="b02dc-121">Get roleAssignment</span></span>](../api/intune-rbac-roleassignment-get.md)|[<span data-ttu-id="b02dc-122">roleAssignment</span><span class="sxs-lookup"><span data-stu-id="b02dc-122">roleAssignment</span></span>](../resources/intune-rbac-roleassignment.md)|<span data-ttu-id="b02dc-123">Lea las propiedades y las relaciones del objeto [roleAssignment](../resources/intune-rbac-roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="b02dc-123">Read properties and relationships of the [roleAssignment](../resources/intune-rbac-roleassignment.md) object.</span></span>|
|[<span data-ttu-id="b02dc-124">Crear roleAssignment</span><span class="sxs-lookup"><span data-stu-id="b02dc-124">Create roleAssignment</span></span>](../api/intune-rbac-roleassignment-create.md)|[<span data-ttu-id="b02dc-125">roleAssignment</span><span class="sxs-lookup"><span data-stu-id="b02dc-125">roleAssignment</span></span>](../resources/intune-rbac-roleassignment.md)|<span data-ttu-id="b02dc-126">Cree un objeto [roleAssignment](../resources/intune-rbac-roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="b02dc-126">Create a new [roleAssignment](../resources/intune-rbac-roleassignment.md) object.</span></span>|
|[<span data-ttu-id="b02dc-127">Eliminar roleAssignment</span><span class="sxs-lookup"><span data-stu-id="b02dc-127">Delete roleAssignment</span></span>](../api/intune-rbac-roleassignment-delete.md)|<span data-ttu-id="b02dc-128">Ninguna</span><span class="sxs-lookup"><span data-stu-id="b02dc-128">None</span></span>|<span data-ttu-id="b02dc-129">Elimina un [roleAssignment](../resources/intune-rbac-roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="b02dc-129">Deletes a [roleAssignment](../resources/intune-rbac-roleassignment.md).</span></span>|
|[<span data-ttu-id="b02dc-130">Actualizar roleAssignment</span><span class="sxs-lookup"><span data-stu-id="b02dc-130">Update roleAssignment</span></span>](../api/intune-rbac-roleassignment-update.md)|[<span data-ttu-id="b02dc-131">roleAssignment</span><span class="sxs-lookup"><span data-stu-id="b02dc-131">roleAssignment</span></span>](../resources/intune-rbac-roleassignment.md)|<span data-ttu-id="b02dc-132">Actualice las propiedades de un objeto [roleAssignment](../resources/intune-rbac-roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="b02dc-132">Update the properties of a [roleAssignment](../resources/intune-rbac-roleassignment.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="b02dc-133">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b02dc-133">Properties</span></span>
|<span data-ttu-id="b02dc-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b02dc-134">Property</span></span>|<span data-ttu-id="b02dc-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="b02dc-135">Type</span></span>|<span data-ttu-id="b02dc-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="b02dc-136">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b02dc-137">id</span><span class="sxs-lookup"><span data-stu-id="b02dc-137">id</span></span>|<span data-ttu-id="b02dc-138">String</span><span class="sxs-lookup"><span data-stu-id="b02dc-138">String</span></span>|<span data-ttu-id="b02dc-139">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b02dc-139">Key of the entity.</span></span> <span data-ttu-id="b02dc-140">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="b02dc-140">This is read-only and automatically generated.</span></span>|
|<span data-ttu-id="b02dc-141">displayName</span><span class="sxs-lookup"><span data-stu-id="b02dc-141">displayName</span></span>|<span data-ttu-id="b02dc-142">String</span><span class="sxs-lookup"><span data-stu-id="b02dc-142">String</span></span>|<span data-ttu-id="b02dc-143">El nombre descriptivo o para mostrar de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="b02dc-143">The display or friendly name of the role Assignment.</span></span>|
|<span data-ttu-id="b02dc-144">descripción</span><span class="sxs-lookup"><span data-stu-id="b02dc-144">description</span></span>|<span data-ttu-id="b02dc-145">String</span><span class="sxs-lookup"><span data-stu-id="b02dc-145">String</span></span>|<span data-ttu-id="b02dc-146">Descripción de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="b02dc-146">Description of the Role Assignment.</span></span>|
|<span data-ttu-id="b02dc-147">scopeMembers</span><span class="sxs-lookup"><span data-stu-id="b02dc-147">scopeMembers</span></span>|<span data-ttu-id="b02dc-148">Colección string</span><span class="sxs-lookup"><span data-stu-id="b02dc-148">String collection</span></span>|<span data-ttu-id="b02dc-149">Lista de identificadores de grupos de seguridad de miembros del ámbito de roles.</span><span class="sxs-lookup"><span data-stu-id="b02dc-149">List of ids of role scope member security groups.</span></span>  <span data-ttu-id="b02dc-150">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b02dc-150">These are IDs from Azure Active Directory.</span></span>|
|<span data-ttu-id="b02dc-151">scopeType</span><span class="sxs-lookup"><span data-stu-id="b02dc-151">scopeType</span></span>|[<span data-ttu-id="b02dc-152">roleAssignmentScopeType</span><span class="sxs-lookup"><span data-stu-id="b02dc-152">roleAssignmentScopeType</span></span>](../resources/intune-rbac-roleassignmentscopetype.md)|<span data-ttu-id="b02dc-153">Especifica el tipo de ámbito para una asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="b02dc-153">Specifies the type of scope for a Role Assignment.</span></span> <span data-ttu-id="b02dc-154">El tipo predeterminado 'ResourceScope' permite la asignación de ResourceScopes.</span><span class="sxs-lookup"><span data-stu-id="b02dc-154">Default type 'ResourceScope' allows assignment of ResourceScopes.</span></span> <span data-ttu-id="b02dc-155">Para 'AllDevices', 'AllLicensedUsers' y 'AllDevicesAndLicensedUsers', la propiedad ResourceScopes debería dejarse vacía.</span><span class="sxs-lookup"><span data-stu-id="b02dc-155">For 'AllDevices', 'AllLicensedUsers', and 'AllDevicesAndLicensedUsers', the ResourceScopes property should be left empty.</span></span> <span data-ttu-id="b02dc-156">Los valores posibles son: `resourceScope`, `allDevices`, `allLicensedUsers` y `allDevicesAndLicensedUsers`.</span><span class="sxs-lookup"><span data-stu-id="b02dc-156">Possible values are: `resourceScope`, `allDevices`, `allLicensedUsers`, `allDevicesAndLicensedUsers`.</span></span>|
|<span data-ttu-id="b02dc-157">resourceScopes</span><span class="sxs-lookup"><span data-stu-id="b02dc-157">resourceScopes</span></span>|<span data-ttu-id="b02dc-158">Colección string</span><span class="sxs-lookup"><span data-stu-id="b02dc-158">String collection</span></span>|<span data-ttu-id="b02dc-159">Lista de identificadores de grupos de seguridad de miembros del ámbito de roles.</span><span class="sxs-lookup"><span data-stu-id="b02dc-159">List of ids of role scope member security groups.</span></span>  <span data-ttu-id="b02dc-160">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b02dc-160">These are IDs from Azure Active Directory.</span></span>|

## <a name="relationships"></a><span data-ttu-id="b02dc-161">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b02dc-161">Relationships</span></span>
|<span data-ttu-id="b02dc-162">Relación</span><span class="sxs-lookup"><span data-stu-id="b02dc-162">Relationship</span></span>|<span data-ttu-id="b02dc-163">Tipo</span><span class="sxs-lookup"><span data-stu-id="b02dc-163">Type</span></span>|<span data-ttu-id="b02dc-164">Descripción</span><span class="sxs-lookup"><span data-stu-id="b02dc-164">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b02dc-165">roleDefinition</span><span class="sxs-lookup"><span data-stu-id="b02dc-165">roleDefinition</span></span>|[<span data-ttu-id="b02dc-166">roleDefinition</span><span class="sxs-lookup"><span data-stu-id="b02dc-166">roleDefinition</span></span>](../resources/intune-rbac-roledefinition.md)|<span data-ttu-id="b02dc-167">Definición de rol del que forma parte esta asignación.</span><span class="sxs-lookup"><span data-stu-id="b02dc-167">Role definition this assignment is part of.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="b02dc-168">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b02dc-168">JSON Representation</span></span>
<span data-ttu-id="b02dc-169">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b02dc-169">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.roleAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.roleAssignment",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "scopeMembers": [
    "String"
  ],
  "scopeType": "String",
  "resourceScopes": [
    "String"
  ]
}
```





