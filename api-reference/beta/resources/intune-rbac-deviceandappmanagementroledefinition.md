---
title: Tipo de recurso deviceAndAppManagementRoleDefinition
description: 'El recurso de la definición de rol. La definición de rol es el pilar del acceso basado en roles en Intune. El rol combina un recurso de Intune, como una aplicación móvil, y los permisos de rol asociados para el recurso, como Creación o Lectura. Hay dos tipos de roles: personalizados e integrados. Los roles integrados no se pueden modificar. Tanto los roles personalizados como los integrados deben tener asignaciones que se aplicarán. Cree roles personalizados para definir un rol que permita que se combine cualquier recurso disponible y permiso de rol en un solo rol.'
localization_priority: Normal
ms.openlocfilehash: a7bdf06be22c2efb11e7fbccf2bd76e5bb9459a5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805260"
---
# <a name="deviceandappmanagementroledefinition-resource-type"></a><span data-ttu-id="7370e-109">Tipo de recurso deviceAndAppManagementRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7370e-109">deviceAndAppManagementRoleDefinition resource type</span></span>

> <span data-ttu-id="7370e-110">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7370e-110">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7370e-111">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7370e-111">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7370e-112">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7370e-112">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7370e-113">El recurso de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="7370e-113">The Role Definition resource.</span></span> <span data-ttu-id="7370e-114">La definición de rol es el pilar del acceso basado en roles en Intune.</span><span class="sxs-lookup"><span data-stu-id="7370e-114">The role definition is the foundation of role based access in Intune.</span></span> <span data-ttu-id="7370e-115">El rol combina un recurso de Intune, como una aplicación móvil, y los permisos de rol asociados para el recurso, como Creación o Lectura.</span><span class="sxs-lookup"><span data-stu-id="7370e-115">The role combines an Intune resource such as a Mobile App and associated role permissions such as Create or Read for the resource.</span></span> <span data-ttu-id="7370e-116">Hay dos tipos de roles: personalizados e integrados.</span><span class="sxs-lookup"><span data-stu-id="7370e-116">There are two types of roles, built-in and custom.</span></span> <span data-ttu-id="7370e-117">Los roles integrados no se pueden modificar.</span><span class="sxs-lookup"><span data-stu-id="7370e-117">Built-in roles cannot be modified.</span></span> <span data-ttu-id="7370e-118">Tanto los roles personalizados como los integrados deben tener asignaciones que se aplicarán.</span><span class="sxs-lookup"><span data-stu-id="7370e-118">Both built-in roles and custom roles must have assignments to be enforced.</span></span> <span data-ttu-id="7370e-119">Cree roles personalizados para definir un rol que permita que se combine cualquier recurso disponible y permiso de rol en un solo rol.</span><span class="sxs-lookup"><span data-stu-id="7370e-119">Create custom roles if you want to define a role that allows any of the available resources and role permissions to be combined into a single role.</span></span>

<span data-ttu-id="7370e-120">Hereda de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="7370e-120">Inherits from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>

## <a name="methods"></a><span data-ttu-id="7370e-121">Métodos</span><span class="sxs-lookup"><span data-stu-id="7370e-121">Methods</span></span>
|<span data-ttu-id="7370e-122">Método</span><span class="sxs-lookup"><span data-stu-id="7370e-122">Method</span></span>|<span data-ttu-id="7370e-123">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7370e-123">Return Type</span></span>|<span data-ttu-id="7370e-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="7370e-124">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="7370e-125">Enumerar deviceAndAppManagementRoleDefinitions</span><span class="sxs-lookup"><span data-stu-id="7370e-125">List deviceAndAppManagementRoleDefinitions</span></span>](../api/intune-rbac-deviceandappmanagementroledefinition-list.md)|<span data-ttu-id="7370e-126">Colección [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="7370e-126">[deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md) collection</span></span>|<span data-ttu-id="7370e-127">Enumere las propiedades y las relaciones de los objetos [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="7370e-127">List properties and relationships of the [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md) objects.</span></span>|
|[<span data-ttu-id="7370e-128">Obtener deviceAndAppManagementRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7370e-128">Get deviceAndAppManagementRoleDefinition</span></span>](../api/intune-rbac-deviceandappmanagementroledefinition-get.md)|[<span data-ttu-id="7370e-129">deviceAndAppManagementRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7370e-129">deviceAndAppManagementRoleDefinition</span></span>](../resources/intune-rbac-deviceandappmanagementroledefinition.md)|<span data-ttu-id="7370e-130">Lea las propiedades y las relaciones del objeto [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="7370e-130">Read properties and relationships of the [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md) object.</span></span>|
|[<span data-ttu-id="7370e-131">Crear deviceAndAppManagementRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7370e-131">Create deviceAndAppManagementRoleDefinition</span></span>](../api/intune-rbac-deviceandappmanagementroledefinition-create.md)|[<span data-ttu-id="7370e-132">deviceAndAppManagementRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7370e-132">deviceAndAppManagementRoleDefinition</span></span>](../resources/intune-rbac-deviceandappmanagementroledefinition.md)|<span data-ttu-id="7370e-133">Cree un objeto [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="7370e-133">Create a new [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md) object.</span></span>|
|[<span data-ttu-id="7370e-134">Eliminar deviceAndAppManagementRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7370e-134">Delete deviceAndAppManagementRoleDefinition</span></span>](../api/intune-rbac-deviceandappmanagementroledefinition-delete.md)|<span data-ttu-id="7370e-135">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7370e-135">None</span></span>|<span data-ttu-id="7370e-136">Elimina un[deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="7370e-136">Deletes a [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).</span></span>|
|[<span data-ttu-id="7370e-137">Actualizar deviceAndAppManagementRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7370e-137">Update deviceAndAppManagementRoleDefinition</span></span>](../api/intune-rbac-deviceandappmanagementroledefinition-update.md)|[<span data-ttu-id="7370e-138">deviceAndAppManagementRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7370e-138">deviceAndAppManagementRoleDefinition</span></span>](../resources/intune-rbac-deviceandappmanagementroledefinition.md)|<span data-ttu-id="7370e-139">Actualice las propiedades de un objeto [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="7370e-139">Update the properties of a [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="7370e-140">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7370e-140">Properties</span></span>
|<span data-ttu-id="7370e-141">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7370e-141">Property</span></span>|<span data-ttu-id="7370e-142">Tipo</span><span class="sxs-lookup"><span data-stu-id="7370e-142">Type</span></span>|<span data-ttu-id="7370e-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="7370e-143">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7370e-144">id</span><span class="sxs-lookup"><span data-stu-id="7370e-144">id</span></span>|<span data-ttu-id="7370e-145">Cadena</span><span class="sxs-lookup"><span data-stu-id="7370e-145">String</span></span>|<span data-ttu-id="7370e-146">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7370e-146">Key of the entity.</span></span> <span data-ttu-id="7370e-147">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="7370e-147">This is read-only and automatically generated.</span></span> <span data-ttu-id="7370e-148">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="7370e-148">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|
|<span data-ttu-id="7370e-149">displayName</span><span class="sxs-lookup"><span data-stu-id="7370e-149">displayName</span></span>|<span data-ttu-id="7370e-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="7370e-150">String</span></span>|<span data-ttu-id="7370e-151">Nombre para mostrar de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="7370e-151">Display Name of the Role definition.</span></span> <span data-ttu-id="7370e-152">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="7370e-152">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|
|<span data-ttu-id="7370e-153">descripción</span><span class="sxs-lookup"><span data-stu-id="7370e-153">description</span></span>|<span data-ttu-id="7370e-154">Cadena</span><span class="sxs-lookup"><span data-stu-id="7370e-154">String</span></span>|<span data-ttu-id="7370e-155">Descripción de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="7370e-155">Description of the Role definition.</span></span> <span data-ttu-id="7370e-156">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="7370e-156">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|
|<span data-ttu-id="7370e-157">permissions</span><span class="sxs-lookup"><span data-stu-id="7370e-157">permissions</span></span>|<span data-ttu-id="7370e-158">Colección [rolePermission](../resources/intune-rbac-rolepermission.md)</span><span class="sxs-lookup"><span data-stu-id="7370e-158">[rolePermission](../resources/intune-rbac-rolepermission.md) collection</span></span>|<span data-ttu-id="7370e-159">Lista de los permisos de rol que puede realizar este rol.</span><span class="sxs-lookup"><span data-stu-id="7370e-159">List of Role Permissions this role is allowed to perform.</span></span> <span data-ttu-id="7370e-160">Estos deben coincidir con el actionName que se definió como parte de rolePermission.</span><span class="sxs-lookup"><span data-stu-id="7370e-160">These must match the actionName that is defined as part of the rolePermission.</span></span> <span data-ttu-id="7370e-161">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="7370e-161">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|
|<span data-ttu-id="7370e-162">rolePermissions</span><span class="sxs-lookup"><span data-stu-id="7370e-162">rolePermissions</span></span>|<span data-ttu-id="7370e-163">Colección [rolePermission](../resources/intune-rbac-rolepermission.md)</span><span class="sxs-lookup"><span data-stu-id="7370e-163">[rolePermission](../resources/intune-rbac-rolepermission.md) collection</span></span>|<span data-ttu-id="7370e-164">Lista de los permisos de rol que puede realizar este rol.</span><span class="sxs-lookup"><span data-stu-id="7370e-164">List of Role Permissions this role is allowed to perform.</span></span> <span data-ttu-id="7370e-165">Estos deben coincidir con el actionName que se definió como parte de rolePermission.</span><span class="sxs-lookup"><span data-stu-id="7370e-165">These must match the actionName that is defined as part of the rolePermission.</span></span> <span data-ttu-id="7370e-166">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="7370e-166">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|
|<span data-ttu-id="7370e-167">isBuiltInRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7370e-167">isBuiltInRoleDefinition</span></span>|<span data-ttu-id="7370e-168">Booleano</span><span class="sxs-lookup"><span data-stu-id="7370e-168">Boolean</span></span>|<span data-ttu-id="7370e-169">Tipo de rol.</span><span class="sxs-lookup"><span data-stu-id="7370e-169">Type of Role.</span></span> <span data-ttu-id="7370e-170">Se establece en True si está integrado o en False si es una definición de rol personalizada.</span><span class="sxs-lookup"><span data-stu-id="7370e-170">Set to True if it is built-in, or set to False if it is a custom role definition.</span></span> <span data-ttu-id="7370e-171">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="7370e-171">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|
|<span data-ttu-id="7370e-172">isBuiltIn</span><span class="sxs-lookup"><span data-stu-id="7370e-172">isBuiltIn</span></span>|<span data-ttu-id="7370e-173">Booleano</span><span class="sxs-lookup"><span data-stu-id="7370e-173">Boolean</span></span>|<span data-ttu-id="7370e-174">Tipo de rol.</span><span class="sxs-lookup"><span data-stu-id="7370e-174">Type of Role.</span></span> <span data-ttu-id="7370e-175">Se establece en True si está integrado o en False si es una definición de rol personalizada.</span><span class="sxs-lookup"><span data-stu-id="7370e-175">Set to True if it is built-in, or set to False if it is a custom role definition.</span></span> <span data-ttu-id="7370e-176">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="7370e-176">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|

## <a name="relationships"></a><span data-ttu-id="7370e-177">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7370e-177">Relationships</span></span>
|<span data-ttu-id="7370e-178">Relación</span><span class="sxs-lookup"><span data-stu-id="7370e-178">Relationship</span></span>|<span data-ttu-id="7370e-179">Tipo</span><span class="sxs-lookup"><span data-stu-id="7370e-179">Type</span></span>|<span data-ttu-id="7370e-180">Descripción</span><span class="sxs-lookup"><span data-stu-id="7370e-180">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7370e-181">roleAssignments</span><span class="sxs-lookup"><span data-stu-id="7370e-181">roleAssignments</span></span>|<span data-ttu-id="7370e-182">Colección [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="7370e-182">[roleAssignment](../resources/intune-rbac-roleassignment.md) collection</span></span>|<span data-ttu-id="7370e-183">Lista de asignaciones de rol para este rol.</span><span class="sxs-lookup"><span data-stu-id="7370e-183">List of Role assignments for this role definition.</span></span> <span data-ttu-id="7370e-184">Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="7370e-184">Inherited from [roleDefinition](../resources/intune-rbac-roledefinition.md)</span></span>|

## <a name="json-representation"></a><span data-ttu-id="7370e-185">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7370e-185">JSON Representation</span></span>
<span data-ttu-id="7370e-186">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7370e-186">Here is a JSON representation of the resource.</span></span>
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





