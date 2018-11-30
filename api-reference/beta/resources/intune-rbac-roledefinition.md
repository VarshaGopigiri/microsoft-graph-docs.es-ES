---
title: Tipo de recurso roleDefinition
description: 'El recurso de la definición de rol. La definición de rol es el pilar del acceso basado en roles en Intune. El rol combina un recurso de Intune, como una aplicación móvil, y los permisos de rol asociados para el recurso, como Creación o Lectura. Hay dos tipos de roles: personalizados e integrados. Los roles integrados no se pueden modificar. Tanto los roles personalizados como los integrados deben tener asignaciones que se aplicarán. Cree roles personalizados para definir un rol que permita que se combine cualquier recurso disponible y permiso de rol en un solo rol.'
ms.openlocfilehash: 872985dd3ba99d4afbdbee3b6bc37055f3800020
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090749"
---
# <a name="roledefinition-resource-type"></a><span data-ttu-id="8526a-109">Tipo de recurso roleDefinition</span><span class="sxs-lookup"><span data-stu-id="8526a-109">roleDefinition resource type</span></span>

> <span data-ttu-id="8526a-110">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8526a-110">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8526a-111">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8526a-111">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8526a-112">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8526a-112">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8526a-113">El recurso de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="8526a-113">The Role Definition resource.</span></span> <span data-ttu-id="8526a-114">La definición de rol es el pilar del acceso basado en roles en Intune.</span><span class="sxs-lookup"><span data-stu-id="8526a-114">The role definition is the foundation of role based access in Intune.</span></span> <span data-ttu-id="8526a-115">El rol combina un recurso de Intune, como una aplicación móvil, y los permisos de rol asociados para el recurso, como Creación o Lectura.</span><span class="sxs-lookup"><span data-stu-id="8526a-115">The role combines an Intune resource such as a Mobile App and associated role permissions such as Create or Read for the resource.</span></span> <span data-ttu-id="8526a-116">Hay dos tipos de roles: personalizados e integrados.</span><span class="sxs-lookup"><span data-stu-id="8526a-116">There are two types of roles, built-in and custom.</span></span> <span data-ttu-id="8526a-117">Los roles integrados no se pueden modificar.</span><span class="sxs-lookup"><span data-stu-id="8526a-117">Built-in roles cannot be modified.</span></span> <span data-ttu-id="8526a-118">Tanto los roles personalizados como los integrados deben tener asignaciones que se aplicarán.</span><span class="sxs-lookup"><span data-stu-id="8526a-118">Both built-in roles and custom roles must have assignments to be enforced.</span></span> <span data-ttu-id="8526a-119">Cree roles personalizados para definir un rol que permita que se combine cualquier recurso disponible y permiso de rol en un solo rol.</span><span class="sxs-lookup"><span data-stu-id="8526a-119">Create custom roles if you want to define a role that allows any of the available resources and role permissions to be combined into a single role.</span></span>
## <a name="methods"></a><span data-ttu-id="8526a-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="8526a-120">Methods</span></span>
|<span data-ttu-id="8526a-121">Método</span><span class="sxs-lookup"><span data-stu-id="8526a-121">Method</span></span>|<span data-ttu-id="8526a-122">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8526a-122">Return Type</span></span>|<span data-ttu-id="8526a-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="8526a-123">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="8526a-124">Enumerar roleDefinitions</span><span class="sxs-lookup"><span data-stu-id="8526a-124">List roleDefinitions</span></span>](../api/intune-rbac-roledefinition-list.md)|<span data-ttu-id="8526a-125">Colección [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="8526a-125">[roleDefinition](../resources/intune-rbac-roledefinition.md) collection</span></span>|<span data-ttu-id="8526a-126">Enumere las propiedades y las relaciones de los objetos [roleDefinition](../resources/intune-rbac-roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="8526a-126">List properties and relationships of the [roleDefinition](../resources/intune-rbac-roledefinition.md) objects.</span></span>|
|[<span data-ttu-id="8526a-127">Obtener roleDefinition</span><span class="sxs-lookup"><span data-stu-id="8526a-127">Get roleDefinition</span></span>](../api/intune-rbac-roledefinition-get.md)|[<span data-ttu-id="8526a-128">roleDefinition</span><span class="sxs-lookup"><span data-stu-id="8526a-128">roleDefinition</span></span>](../resources/intune-rbac-roledefinition.md)|<span data-ttu-id="8526a-129">Lea las propiedades y las relaciones del objeto [roleDefinition](../resources/intune-rbac-roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="8526a-129">Read properties and relationships of the [roleDefinition](../resources/intune-rbac-roledefinition.md) object.</span></span>|
|[<span data-ttu-id="8526a-130">Crear roleDefinition</span><span class="sxs-lookup"><span data-stu-id="8526a-130">Create roleDefinition</span></span>](../api/intune-rbac-roledefinition-create.md)|[<span data-ttu-id="8526a-131">roleDefinition</span><span class="sxs-lookup"><span data-stu-id="8526a-131">roleDefinition</span></span>](../resources/intune-rbac-roledefinition.md)|<span data-ttu-id="8526a-132">Cree un objeto [roleDefinition](../resources/intune-rbac-roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="8526a-132">Create a new [roleDefinition](../resources/intune-rbac-roledefinition.md) object.</span></span>|
|[<span data-ttu-id="8526a-133">Eliminar roleDefinition</span><span class="sxs-lookup"><span data-stu-id="8526a-133">Delete roleDefinition</span></span>](../api/intune-rbac-roledefinition-delete.md)|<span data-ttu-id="8526a-134">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8526a-134">None</span></span>|<span data-ttu-id="8526a-135">Elimina un [roleDefinition](../resources/intune-rbac-roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="8526a-135">Deletes a [roleDefinition](../resources/intune-rbac-roledefinition.md).</span></span>|
|[<span data-ttu-id="8526a-136">Actualizar roleDefinition</span><span class="sxs-lookup"><span data-stu-id="8526a-136">Update roleDefinition</span></span>](../api/intune-rbac-roledefinition-update.md)|[<span data-ttu-id="8526a-137">roleDefinition</span><span class="sxs-lookup"><span data-stu-id="8526a-137">roleDefinition</span></span>](../resources/intune-rbac-roledefinition.md)|<span data-ttu-id="8526a-138">Actualice las propiedades de un objeto [roleDefinition](../resources/intune-rbac-roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="8526a-138">Update the properties of a [roleDefinition](../resources/intune-rbac-roledefinition.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="8526a-139">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8526a-139">Properties</span></span>
|<span data-ttu-id="8526a-140">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8526a-140">Property</span></span>|<span data-ttu-id="8526a-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="8526a-141">Type</span></span>|<span data-ttu-id="8526a-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="8526a-142">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8526a-143">id</span><span class="sxs-lookup"><span data-stu-id="8526a-143">id</span></span>|<span data-ttu-id="8526a-144">String</span><span class="sxs-lookup"><span data-stu-id="8526a-144">String</span></span>|<span data-ttu-id="8526a-145">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8526a-145">Key of the entity.</span></span> <span data-ttu-id="8526a-146">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="8526a-146">This is read-only and automatically generated.</span></span>|
|<span data-ttu-id="8526a-147">displayName</span><span class="sxs-lookup"><span data-stu-id="8526a-147">displayName</span></span>|<span data-ttu-id="8526a-148">String</span><span class="sxs-lookup"><span data-stu-id="8526a-148">String</span></span>|<span data-ttu-id="8526a-149">Nombre para mostrar de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="8526a-149">Display Name of the Role definition.</span></span>|
|<span data-ttu-id="8526a-150">description</span><span class="sxs-lookup"><span data-stu-id="8526a-150">description</span></span>|<span data-ttu-id="8526a-151">String</span><span class="sxs-lookup"><span data-stu-id="8526a-151">String</span></span>|<span data-ttu-id="8526a-152">Descripción de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="8526a-152">Description of the Role definition.</span></span>|
|<span data-ttu-id="8526a-153">permissions</span><span class="sxs-lookup"><span data-stu-id="8526a-153">permissions</span></span>|<span data-ttu-id="8526a-154">Colección [rolePermission](../resources/intune-rbac-rolepermission.md)</span><span class="sxs-lookup"><span data-stu-id="8526a-154">[rolePermission](../resources/intune-rbac-rolepermission.md) collection</span></span>|<span data-ttu-id="8526a-155">Lista de los permisos de rol que puede realizar este rol.</span><span class="sxs-lookup"><span data-stu-id="8526a-155">List of Role Permissions this role is allowed to perform.</span></span> <span data-ttu-id="8526a-156">Estos deben coincidir con el actionName que se definió como parte de rolePermission.</span><span class="sxs-lookup"><span data-stu-id="8526a-156">These must match the actionName that is defined as part of the rolePermission.</span></span>|
|<span data-ttu-id="8526a-157">rolePermissions</span><span class="sxs-lookup"><span data-stu-id="8526a-157">rolePermissions</span></span>|<span data-ttu-id="8526a-158">Colección [rolePermission](../resources/intune-rbac-rolepermission.md)</span><span class="sxs-lookup"><span data-stu-id="8526a-158">[rolePermission](../resources/intune-rbac-rolepermission.md) collection</span></span>|<span data-ttu-id="8526a-159">Lista de los permisos de rol que puede realizar este rol.</span><span class="sxs-lookup"><span data-stu-id="8526a-159">List of Role Permissions this role is allowed to perform.</span></span> <span data-ttu-id="8526a-160">Estos deben coincidir con el actionName que se definió como parte de rolePermission.</span><span class="sxs-lookup"><span data-stu-id="8526a-160">These must match the actionName that is defined as part of the rolePermission.</span></span>|
|<span data-ttu-id="8526a-161">isBuiltInRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8526a-161">isBuiltInRoleDefinition</span></span>|<span data-ttu-id="8526a-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="8526a-162">Boolean</span></span>|<span data-ttu-id="8526a-163">Tipo de rol.</span><span class="sxs-lookup"><span data-stu-id="8526a-163">Type of Role.</span></span> <span data-ttu-id="8526a-164">Se establece en True si está integrado o en False si es una definición de rol personalizada.</span><span class="sxs-lookup"><span data-stu-id="8526a-164">Set to True if it is built-in, or set to False if it is a custom role definition.</span></span>|
|<span data-ttu-id="8526a-165">isBuiltIn</span><span class="sxs-lookup"><span data-stu-id="8526a-165">isBuiltIn</span></span>|<span data-ttu-id="8526a-166">Booleano</span><span class="sxs-lookup"><span data-stu-id="8526a-166">Boolean</span></span>|<span data-ttu-id="8526a-167">Tipo de rol.</span><span class="sxs-lookup"><span data-stu-id="8526a-167">Type of Role.</span></span> <span data-ttu-id="8526a-168">Se establece en True si está integrado o en False si es una definición de rol personalizada.</span><span class="sxs-lookup"><span data-stu-id="8526a-168">Set to True if it is built-in, or set to False if it is a custom role definition.</span></span>|

## <a name="relationships"></a><span data-ttu-id="8526a-169">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8526a-169">Relationships</span></span>
|<span data-ttu-id="8526a-170">Relación</span><span class="sxs-lookup"><span data-stu-id="8526a-170">Relationship</span></span>|<span data-ttu-id="8526a-171">Tipo</span><span class="sxs-lookup"><span data-stu-id="8526a-171">Type</span></span>|<span data-ttu-id="8526a-172">Descripción</span><span class="sxs-lookup"><span data-stu-id="8526a-172">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8526a-173">roleAssignments</span><span class="sxs-lookup"><span data-stu-id="8526a-173">roleAssignments</span></span>|<span data-ttu-id="8526a-174">Colección [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="8526a-174">[roleAssignment](../resources/intune-rbac-roleassignment.md) collection</span></span>|<span data-ttu-id="8526a-175">Lista de asignaciones de rol para este rol.</span><span class="sxs-lookup"><span data-stu-id="8526a-175">List of Role assignments for this role definition.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="8526a-176">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8526a-176">JSON Representation</span></span>
<span data-ttu-id="8526a-177">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8526a-177">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.roleDefinition"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.roleDefinition",
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





