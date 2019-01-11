---
title: Tipo de recurso roleDefinition
description: 'El recurso de la definición de rol. La definición de rol es el pilar del acceso basado en roles en Intune. El rol combina un recurso de Intune, como una aplicación móvil, y los permisos de rol asociados para el recurso, como Creación o Lectura. Hay dos tipos de roles: personalizados e integrados. Los roles integrados no se pueden modificar. Tanto los roles personalizados como los integrados deben tener asignaciones que se aplicarán. Cree roles personalizados para definir un rol que permita que se combine cualquier recurso disponible y permiso de rol en un solo rol.'
localization_priority: Normal
ms.openlocfilehash: 27ded12110b7db9e329afc8c90ac114e9296646d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27835675"
---
# <a name="roledefinition-resource-type"></a><span data-ttu-id="08153-109">Tipo de recurso roleDefinition</span><span class="sxs-lookup"><span data-stu-id="08153-109">roleDefinition resource type</span></span>

> <span data-ttu-id="08153-110">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="08153-110">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="08153-111">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="08153-111">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="08153-112">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="08153-112">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="08153-113">El recurso de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="08153-113">The Role Definition resource.</span></span> <span data-ttu-id="08153-114">La definición de rol es el pilar del acceso basado en roles en Intune.</span><span class="sxs-lookup"><span data-stu-id="08153-114">The role definition is the foundation of role based access in Intune.</span></span> <span data-ttu-id="08153-115">El rol combina un recurso de Intune, como una aplicación móvil, y los permisos de rol asociados para el recurso, como Creación o Lectura.</span><span class="sxs-lookup"><span data-stu-id="08153-115">The role combines an Intune resource such as a Mobile App and associated role permissions such as Create or Read for the resource.</span></span> <span data-ttu-id="08153-116">Hay dos tipos de roles: personalizados e integrados.</span><span class="sxs-lookup"><span data-stu-id="08153-116">There are two types of roles, built-in and custom.</span></span> <span data-ttu-id="08153-117">Los roles integrados no se pueden modificar.</span><span class="sxs-lookup"><span data-stu-id="08153-117">Built-in roles cannot be modified.</span></span> <span data-ttu-id="08153-118">Tanto los roles personalizados como los integrados deben tener asignaciones que se aplicarán.</span><span class="sxs-lookup"><span data-stu-id="08153-118">Both built-in roles and custom roles must have assignments to be enforced.</span></span> <span data-ttu-id="08153-119">Cree roles personalizados para definir un rol que permita que se combine cualquier recurso disponible y permiso de rol en un solo rol.</span><span class="sxs-lookup"><span data-stu-id="08153-119">Create custom roles if you want to define a role that allows any of the available resources and role permissions to be combined into a single role.</span></span>
## <a name="methods"></a><span data-ttu-id="08153-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="08153-120">Methods</span></span>
|<span data-ttu-id="08153-121">Método</span><span class="sxs-lookup"><span data-stu-id="08153-121">Method</span></span>|<span data-ttu-id="08153-122">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08153-122">Return Type</span></span>|<span data-ttu-id="08153-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="08153-123">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="08153-124">Enumerar roleDefinitions</span><span class="sxs-lookup"><span data-stu-id="08153-124">List roleDefinitions</span></span>](../api/intune-rbac-roledefinition-list.md)|<span data-ttu-id="08153-125">Colección [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="08153-125">[roleDefinition](../resources/intune-rbac-roledefinition.md) collection</span></span>|<span data-ttu-id="08153-126">Enumere las propiedades y las relaciones de los objetos [roleDefinition](../resources/intune-rbac-roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="08153-126">List properties and relationships of the [roleDefinition](../resources/intune-rbac-roledefinition.md) objects.</span></span>|
|[<span data-ttu-id="08153-127">Obtener roleDefinition</span><span class="sxs-lookup"><span data-stu-id="08153-127">Get roleDefinition</span></span>](../api/intune-rbac-roledefinition-get.md)|[<span data-ttu-id="08153-128">roleDefinition</span><span class="sxs-lookup"><span data-stu-id="08153-128">roleDefinition</span></span>](../resources/intune-rbac-roledefinition.md)|<span data-ttu-id="08153-129">Lea las propiedades y las relaciones del objeto [roleDefinition](../resources/intune-rbac-roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="08153-129">Read properties and relationships of the [roleDefinition](../resources/intune-rbac-roledefinition.md) object.</span></span>|
|[<span data-ttu-id="08153-130">Crear roleDefinition</span><span class="sxs-lookup"><span data-stu-id="08153-130">Create roleDefinition</span></span>](../api/intune-rbac-roledefinition-create.md)|[<span data-ttu-id="08153-131">roleDefinition</span><span class="sxs-lookup"><span data-stu-id="08153-131">roleDefinition</span></span>](../resources/intune-rbac-roledefinition.md)|<span data-ttu-id="08153-132">Cree un objeto [roleDefinition](../resources/intune-rbac-roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="08153-132">Create a new [roleDefinition](../resources/intune-rbac-roledefinition.md) object.</span></span>|
|[<span data-ttu-id="08153-133">Eliminar roleDefinition</span><span class="sxs-lookup"><span data-stu-id="08153-133">Delete roleDefinition</span></span>](../api/intune-rbac-roledefinition-delete.md)|<span data-ttu-id="08153-134">Ninguno</span><span class="sxs-lookup"><span data-stu-id="08153-134">None</span></span>|<span data-ttu-id="08153-135">Elimina un [roleDefinition](../resources/intune-rbac-roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="08153-135">Deletes a [roleDefinition](../resources/intune-rbac-roledefinition.md).</span></span>|
|[<span data-ttu-id="08153-136">Actualizar roleDefinition</span><span class="sxs-lookup"><span data-stu-id="08153-136">Update roleDefinition</span></span>](../api/intune-rbac-roledefinition-update.md)|[<span data-ttu-id="08153-137">roleDefinition</span><span class="sxs-lookup"><span data-stu-id="08153-137">roleDefinition</span></span>](../resources/intune-rbac-roledefinition.md)|<span data-ttu-id="08153-138">Actualice las propiedades de un objeto [roleDefinition](../resources/intune-rbac-roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="08153-138">Update the properties of a [roleDefinition](../resources/intune-rbac-roledefinition.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="08153-139">Propiedades</span><span class="sxs-lookup"><span data-stu-id="08153-139">Properties</span></span>
|<span data-ttu-id="08153-140">Propiedad</span><span class="sxs-lookup"><span data-stu-id="08153-140">Property</span></span>|<span data-ttu-id="08153-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="08153-141">Type</span></span>|<span data-ttu-id="08153-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="08153-142">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="08153-143">id</span><span class="sxs-lookup"><span data-stu-id="08153-143">id</span></span>|<span data-ttu-id="08153-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="08153-144">String</span></span>|<span data-ttu-id="08153-145">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="08153-145">Key of the entity.</span></span> <span data-ttu-id="08153-146">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="08153-146">This is read-only and automatically generated.</span></span>|
|<span data-ttu-id="08153-147">displayName</span><span class="sxs-lookup"><span data-stu-id="08153-147">displayName</span></span>|<span data-ttu-id="08153-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="08153-148">String</span></span>|<span data-ttu-id="08153-149">Nombre para mostrar de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="08153-149">Display Name of the Role definition.</span></span>|
|<span data-ttu-id="08153-150">description</span><span class="sxs-lookup"><span data-stu-id="08153-150">description</span></span>|<span data-ttu-id="08153-151">Cadena</span><span class="sxs-lookup"><span data-stu-id="08153-151">String</span></span>|<span data-ttu-id="08153-152">Descripción de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="08153-152">Description of the Role definition.</span></span>|
|<span data-ttu-id="08153-153">permissions</span><span class="sxs-lookup"><span data-stu-id="08153-153">permissions</span></span>|<span data-ttu-id="08153-154">Colección [rolePermission](../resources/intune-rbac-rolepermission.md)</span><span class="sxs-lookup"><span data-stu-id="08153-154">[rolePermission](../resources/intune-rbac-rolepermission.md) collection</span></span>|<span data-ttu-id="08153-155">Lista de los permisos de rol que puede realizar este rol.</span><span class="sxs-lookup"><span data-stu-id="08153-155">List of Role Permissions this role is allowed to perform.</span></span> <span data-ttu-id="08153-156">Estos deben coincidir con el actionName que se definió como parte de rolePermission.</span><span class="sxs-lookup"><span data-stu-id="08153-156">These must match the actionName that is defined as part of the rolePermission.</span></span>|
|<span data-ttu-id="08153-157">rolePermissions</span><span class="sxs-lookup"><span data-stu-id="08153-157">rolePermissions</span></span>|<span data-ttu-id="08153-158">Colección [rolePermission](../resources/intune-rbac-rolepermission.md)</span><span class="sxs-lookup"><span data-stu-id="08153-158">[rolePermission](../resources/intune-rbac-rolepermission.md) collection</span></span>|<span data-ttu-id="08153-159">Lista de los permisos de rol que puede realizar este rol.</span><span class="sxs-lookup"><span data-stu-id="08153-159">List of Role Permissions this role is allowed to perform.</span></span> <span data-ttu-id="08153-160">Estos deben coincidir con el actionName que se definió como parte de rolePermission.</span><span class="sxs-lookup"><span data-stu-id="08153-160">These must match the actionName that is defined as part of the rolePermission.</span></span>|
|<span data-ttu-id="08153-161">isBuiltInRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="08153-161">isBuiltInRoleDefinition</span></span>|<span data-ttu-id="08153-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="08153-162">Boolean</span></span>|<span data-ttu-id="08153-163">Tipo de rol.</span><span class="sxs-lookup"><span data-stu-id="08153-163">Type of Role.</span></span> <span data-ttu-id="08153-164">Se establece en True si está integrado o en False si es una definición de rol personalizada.</span><span class="sxs-lookup"><span data-stu-id="08153-164">Set to True if it is built-in, or set to False if it is a custom role definition.</span></span>|
|<span data-ttu-id="08153-165">isBuiltIn</span><span class="sxs-lookup"><span data-stu-id="08153-165">isBuiltIn</span></span>|<span data-ttu-id="08153-166">Booleano</span><span class="sxs-lookup"><span data-stu-id="08153-166">Boolean</span></span>|<span data-ttu-id="08153-167">Tipo de rol.</span><span class="sxs-lookup"><span data-stu-id="08153-167">Type of Role.</span></span> <span data-ttu-id="08153-168">Se establece en True si está integrado o en False si es una definición de rol personalizada.</span><span class="sxs-lookup"><span data-stu-id="08153-168">Set to True if it is built-in, or set to False if it is a custom role definition.</span></span>|

## <a name="relationships"></a><span data-ttu-id="08153-169">Relaciones</span><span class="sxs-lookup"><span data-stu-id="08153-169">Relationships</span></span>
|<span data-ttu-id="08153-170">Relación</span><span class="sxs-lookup"><span data-stu-id="08153-170">Relationship</span></span>|<span data-ttu-id="08153-171">Tipo</span><span class="sxs-lookup"><span data-stu-id="08153-171">Type</span></span>|<span data-ttu-id="08153-172">Descripción</span><span class="sxs-lookup"><span data-stu-id="08153-172">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="08153-173">roleAssignments</span><span class="sxs-lookup"><span data-stu-id="08153-173">roleAssignments</span></span>|<span data-ttu-id="08153-174">Colección [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="08153-174">[roleAssignment](../resources/intune-rbac-roleassignment.md) collection</span></span>|<span data-ttu-id="08153-175">Lista de asignaciones de rol para este rol.</span><span class="sxs-lookup"><span data-stu-id="08153-175">List of Role assignments for this role definition.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="08153-176">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="08153-176">JSON Representation</span></span>
<span data-ttu-id="08153-177">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="08153-177">Here is a JSON representation of the resource.</span></span>
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





