---
title: Tipo de recurso deviceAndAppManagementRoleDefinition
description: 'El recurso de la definición de rol. La definición de rol es el pilar del acceso basado en roles en Intune. El rol combina un recurso de Intune, como una aplicación móvil, y los permisos de rol asociados para el recurso, como Creación o Lectura. Hay dos tipos de roles: personalizados e integrados. Los roles integrados no se pueden modificar. Tanto los roles personalizados como los integrados deben tener asignaciones que se aplicarán. Cree roles personalizados para definir un rol que permita que se combine cualquier recurso disponible y permiso de rol en un solo rol.'
ms.openlocfilehash: 90c701afc33a16cfb2747c40d53d47e74c3cedde
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086414"
---
# <a name="deviceandappmanagementroledefinition-resource-type"></a><span data-ttu-id="504fc-109">Tipo de recurso deviceAndAppManagementRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="504fc-109">deviceAndAppManagementRoleDefinition resource type</span></span>

> <span data-ttu-id="504fc-110">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="504fc-110">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="504fc-111">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="504fc-111">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="504fc-112">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="504fc-112">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="504fc-113">El recurso de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="504fc-113">The Role Definition resource.</span></span> <span data-ttu-id="504fc-114">La definición de rol es el pilar del acceso basado en roles en Intune.</span><span class="sxs-lookup"><span data-stu-id="504fc-114">The role definition is the foundation of role based access in Intune.</span></span> <span data-ttu-id="504fc-115">El rol combina un recurso de Intune, como una aplicación móvil, y los permisos de rol asociados para el recurso, como Creación o Lectura.</span><span class="sxs-lookup"><span data-stu-id="504fc-115">The role combines an Intune resource such as a Mobile App and associated role permissions such as Create or Read for the resource.</span></span> <span data-ttu-id="504fc-116">Hay dos tipos de roles: personalizados e integrados.</span><span class="sxs-lookup"><span data-stu-id="504fc-116">There are two types of roles, built-in and custom.</span></span> <span data-ttu-id="504fc-117">Los roles integrados no se pueden modificar.</span><span class="sxs-lookup"><span data-stu-id="504fc-117">Built-in roles cannot be modified.</span></span> <span data-ttu-id="504fc-118">Tanto los roles personalizados como los integrados deben tener asignaciones que se aplicarán.</span><span class="sxs-lookup"><span data-stu-id="504fc-118">Both built-in roles and custom roles must have assignments to be enforced.</span></span> <span data-ttu-id="504fc-119">Cree roles personalizados para definir un rol que permita que se combine cualquier recurso disponible y permiso de rol en un solo rol.</span><span class="sxs-lookup"><span data-stu-id="504fc-119">Create custom roles if you want to define a role that allows any of the available resources and role permissions to be combined into a single role.</span></span>

<span data-ttu-id="504fc-120">Hereda de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="504fc-120">Inherits from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>

## <a name="methods"></a><span data-ttu-id="504fc-121">Métodos</span><span class="sxs-lookup"><span data-stu-id="504fc-121">Methods</span></span>
|<span data-ttu-id="504fc-122">Método</span><span class="sxs-lookup"><span data-stu-id="504fc-122">Method</span></span>|<span data-ttu-id="504fc-123">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="504fc-123">Return Type</span></span>|<span data-ttu-id="504fc-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="504fc-124">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="504fc-125">Enumerar deviceAndAppManagementRoleDefinitions</span><span class="sxs-lookup"><span data-stu-id="504fc-125">List deviceAndAppManagementRoleDefinitions</span></span>](../api/intune-rbac-deviceandappmanagementroledefinition-list.md)|<span data-ttu-id="504fc-126">Colección [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="504fc-126">[deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md) collection</span></span>|<span data-ttu-id="504fc-127">Enumere las propiedades y las relaciones de los objetos [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="504fc-127">List properties and relationships of the [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md) objects.</span></span>|
|[<span data-ttu-id="504fc-128">Obtener deviceAndAppManagementRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="504fc-128">Get deviceAndAppManagementRoleDefinition</span></span>](../api/intune-rbac-deviceandappmanagementroledefinition-get.md)|[<span data-ttu-id="504fc-129">deviceAndAppManagementRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="504fc-129">deviceAndAppManagementRoleDefinition</span></span>](../resources/intune-rbac-deviceandappmanagementroledefinition.md)|<span data-ttu-id="504fc-130">Lea las propiedades y las relaciones del objeto [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="504fc-130">Read properties and relationships of the [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md) object.</span></span>|
|[<span data-ttu-id="504fc-131">Crear deviceAndAppManagementRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="504fc-131">Create deviceAndAppManagementRoleDefinition</span></span>](../api/intune-rbac-deviceandappmanagementroledefinition-create.md)|[<span data-ttu-id="504fc-132">deviceAndAppManagementRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="504fc-132">deviceAndAppManagementRoleDefinition</span></span>](../resources/intune-rbac-deviceandappmanagementroledefinition.md)|<span data-ttu-id="504fc-133">Cree un objeto [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="504fc-133">Create a new [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md) object.</span></span>|
|[<span data-ttu-id="504fc-134">Eliminar deviceAndAppManagementRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="504fc-134">Delete deviceAndAppManagementRoleDefinition</span></span>](../api/intune-rbac-deviceandappmanagementroledefinition-delete.md)|<span data-ttu-id="504fc-135">Ninguna</span><span class="sxs-lookup"><span data-stu-id="504fc-135">None</span></span>|<span data-ttu-id="504fc-136">Elimina un[deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="504fc-136">Deletes a [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).</span></span>|
|[<span data-ttu-id="504fc-137">Actualizar deviceAndAppManagementRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="504fc-137">Update deviceAndAppManagementRoleDefinition</span></span>](../api/intune-rbac-deviceandappmanagementroledefinition-update.md)|[<span data-ttu-id="504fc-138">deviceAndAppManagementRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="504fc-138">deviceAndAppManagementRoleDefinition</span></span>](../resources/intune-rbac-deviceandappmanagementroledefinition.md)|<span data-ttu-id="504fc-139">Actualice las propiedades de un objeto [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="504fc-139">Update the properties of a [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="504fc-140">Propiedades</span><span class="sxs-lookup"><span data-stu-id="504fc-140">Properties</span></span>
|<span data-ttu-id="504fc-141">Propiedad</span><span class="sxs-lookup"><span data-stu-id="504fc-141">Property</span></span>|<span data-ttu-id="504fc-142">Tipo</span><span class="sxs-lookup"><span data-stu-id="504fc-142">Type</span></span>|<span data-ttu-id="504fc-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="504fc-143">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="504fc-144">id</span><span class="sxs-lookup"><span data-stu-id="504fc-144">id</span></span>|<span data-ttu-id="504fc-145">String</span><span class="sxs-lookup"><span data-stu-id="504fc-145">String</span></span>|<span data-ttu-id="504fc-146">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="504fc-146">Key of the entity.</span></span> <span data-ttu-id="504fc-147">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="504fc-147">This is read-only and automatically generated.</span></span> <span data-ttu-id="504fc-148">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="504fc-148">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|
|<span data-ttu-id="504fc-149">displayName</span><span class="sxs-lookup"><span data-stu-id="504fc-149">displayName</span></span>|<span data-ttu-id="504fc-150">String</span><span class="sxs-lookup"><span data-stu-id="504fc-150">String</span></span>|<span data-ttu-id="504fc-151">Nombre para mostrar de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="504fc-151">Display Name of the Role definition.</span></span> <span data-ttu-id="504fc-152">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="504fc-152">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|
|<span data-ttu-id="504fc-153">descripción</span><span class="sxs-lookup"><span data-stu-id="504fc-153">description</span></span>|<span data-ttu-id="504fc-154">String</span><span class="sxs-lookup"><span data-stu-id="504fc-154">String</span></span>|<span data-ttu-id="504fc-155">Descripción de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="504fc-155">Description of the Role definition.</span></span> <span data-ttu-id="504fc-156">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="504fc-156">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|
|<span data-ttu-id="504fc-157">permissions</span><span class="sxs-lookup"><span data-stu-id="504fc-157">permissions</span></span>|<span data-ttu-id="504fc-158">Colección [rolePermission](../resources/intune-rbac-rolepermission.md)</span><span class="sxs-lookup"><span data-stu-id="504fc-158">[rolePermission](../resources/intune-rbac-rolepermission.md) collection</span></span>|<span data-ttu-id="504fc-159">Lista de los permisos de rol que puede realizar este rol.</span><span class="sxs-lookup"><span data-stu-id="504fc-159">List of Role Permissions this role is allowed to perform.</span></span> <span data-ttu-id="504fc-160">Estos deben coincidir con el actionName que se definió como parte de rolePermission.</span><span class="sxs-lookup"><span data-stu-id="504fc-160">These must match the actionName that is defined as part of the rolePermission.</span></span> <span data-ttu-id="504fc-161">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="504fc-161">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|
|<span data-ttu-id="504fc-162">rolePermissions</span><span class="sxs-lookup"><span data-stu-id="504fc-162">rolePermissions</span></span>|<span data-ttu-id="504fc-163">Colección [rolePermission](../resources/intune-rbac-rolepermission.md)</span><span class="sxs-lookup"><span data-stu-id="504fc-163">[rolePermission](../resources/intune-rbac-rolepermission.md) collection</span></span>|<span data-ttu-id="504fc-164">Lista de los permisos de rol que puede realizar este rol.</span><span class="sxs-lookup"><span data-stu-id="504fc-164">List of Role Permissions this role is allowed to perform.</span></span> <span data-ttu-id="504fc-165">Estos deben coincidir con el actionName que se definió como parte de rolePermission.</span><span class="sxs-lookup"><span data-stu-id="504fc-165">These must match the actionName that is defined as part of the rolePermission.</span></span> <span data-ttu-id="504fc-166">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="504fc-166">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|
|<span data-ttu-id="504fc-167">isBuiltInRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="504fc-167">isBuiltInRoleDefinition</span></span>|<span data-ttu-id="504fc-168">Booleano</span><span class="sxs-lookup"><span data-stu-id="504fc-168">Boolean</span></span>|<span data-ttu-id="504fc-169">Tipo de rol.</span><span class="sxs-lookup"><span data-stu-id="504fc-169">Type of Role.</span></span> <span data-ttu-id="504fc-170">Se establece en True si está integrado o en False si es una definición de rol personalizada.</span><span class="sxs-lookup"><span data-stu-id="504fc-170">Set to True if it is built-in, or set to False if it is a custom role definition.</span></span> <span data-ttu-id="504fc-171">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="504fc-171">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|
|<span data-ttu-id="504fc-172">isBuiltIn</span><span class="sxs-lookup"><span data-stu-id="504fc-172">isBuiltIn</span></span>|<span data-ttu-id="504fc-173">Booleano</span><span class="sxs-lookup"><span data-stu-id="504fc-173">Boolean</span></span>|<span data-ttu-id="504fc-174">Tipo de rol.</span><span class="sxs-lookup"><span data-stu-id="504fc-174">Type of Role.</span></span> <span data-ttu-id="504fc-175">Se establece en True si está integrado o en False si es una definición de rol personalizada.</span><span class="sxs-lookup"><span data-stu-id="504fc-175">Set to True if it is built-in, or set to False if it is a custom role definition.</span></span> <span data-ttu-id="504fc-176">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="504fc-176">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|

## <a name="relationships"></a><span data-ttu-id="504fc-177">Relaciones</span><span class="sxs-lookup"><span data-stu-id="504fc-177">Relationships</span></span>
|<span data-ttu-id="504fc-178">Relación</span><span class="sxs-lookup"><span data-stu-id="504fc-178">Relationship</span></span>|<span data-ttu-id="504fc-179">Tipo</span><span class="sxs-lookup"><span data-stu-id="504fc-179">Type</span></span>|<span data-ttu-id="504fc-180">Descripción</span><span class="sxs-lookup"><span data-stu-id="504fc-180">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="504fc-181">roleAssignments</span><span class="sxs-lookup"><span data-stu-id="504fc-181">roleAssignments</span></span>|<span data-ttu-id="504fc-182">Colección [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="504fc-182">[roleAssignment](../resources/intune-rbac-roleassignment.md) collection</span></span>|<span data-ttu-id="504fc-183">Lista de asignaciones de rol para este rol.</span><span class="sxs-lookup"><span data-stu-id="504fc-183">List of Role assignments for this role definition.</span></span> <span data-ttu-id="504fc-184">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="504fc-184">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|

## <a name="json-representation"></a><span data-ttu-id="504fc-185">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="504fc-185">JSON Representation</span></span>
<span data-ttu-id="504fc-186">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="504fc-186">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceAndAppManagementRoleDefinition"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceAndAppManagementRoleDefinition",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "permissions": [
    {
      "@odata.type": "microsoft.graph.rolePermission",
      "actions": [
        "String"
      ],
      "resourceActions": [
        {
          "@odata.type": "microsoft.graph.resourceAction",
          "allowedResourceActions": [
            "String"
          ],
          "notAllowedResourceActions": [
            "String"
          ]
        }
      ]
    }
  ],
  "rolePermissions": [
    {
      "@odata.type": "microsoft.graph.rolePermission",
      "actions": [
        "String"
      ],
      "resourceActions": [
        {
          "@odata.type": "microsoft.graph.resourceAction",
          "allowedResourceActions": [
            "String"
          ],
          "notAllowedResourceActions": [
            "String"
          ]
        }
      ]
    }
  ],
  "isBuiltInRoleDefinition": true,
  "isBuiltIn": true
}
```





