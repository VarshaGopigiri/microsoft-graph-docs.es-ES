---
title: Tipo de recurso roleDefinition
description: 'El recurso de la definición de rol. La definición de rol es el pilar del acceso basado en roles en Intune. El rol combina un recurso de Intune, como una aplicación móvil, y los permisos de rol asociados para el recurso, como Creación o Lectura. Hay dos tipos de roles: personalizados e integrados. Los roles integrados no se pueden modificar. Tanto los roles personalizados como los integrados deben tener asignaciones que se aplicarán. Cree roles personalizados para definir un rol que permita que se combine cualquier recurso disponible y permiso de rol en un solo rol.'
ms.openlocfilehash: 15be13c0a893ed0cdc7b77b47591cc28d32c9889
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030676"
---
# <a name="roledefinition-resource-type"></a><span data-ttu-id="c6027-109">Tipo de recurso roleDefinition</span><span class="sxs-lookup"><span data-stu-id="c6027-109">roleDefinition resource type</span></span>

> <span data-ttu-id="c6027-110">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c6027-110">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c6027-111">El recurso de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="c6027-111">The Role Definition resource.</span></span> <span data-ttu-id="c6027-112">La definición de rol es el pilar del acceso basado en roles en Intune.</span><span class="sxs-lookup"><span data-stu-id="c6027-112">The role definition is the foundation of role based access in Intune.</span></span> <span data-ttu-id="c6027-113">El rol combina un recurso de Intune, como una aplicación móvil, y los permisos de rol asociados para el recurso, como Creación o Lectura.</span><span class="sxs-lookup"><span data-stu-id="c6027-113">The role combines an Intune resource such as a Mobile App and associated role permissions such as Create or Read for the resource.</span></span> <span data-ttu-id="c6027-114">Hay dos tipos de roles: personalizados e integrados.</span><span class="sxs-lookup"><span data-stu-id="c6027-114">There are two types of roles, built-in and custom.</span></span> <span data-ttu-id="c6027-115">Los roles integrados no se pueden modificar.</span><span class="sxs-lookup"><span data-stu-id="c6027-115">Built-in roles cannot be modified.</span></span> <span data-ttu-id="c6027-116">Tanto los roles personalizados como los integrados deben tener asignaciones que se aplicarán.</span><span class="sxs-lookup"><span data-stu-id="c6027-116">Both built-in roles and custom roles must have assignments to be enforced.</span></span> <span data-ttu-id="c6027-117">Cree roles personalizados para definir un rol que permita que se combine cualquier recurso disponible y permiso de rol en un solo rol.</span><span class="sxs-lookup"><span data-stu-id="c6027-117">Create custom roles if you want to define a role that allows any of the available resources and role permissions to be combined into a single role.</span></span>
## <a name="methods"></a><span data-ttu-id="c6027-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="c6027-118">Methods</span></span>
|<span data-ttu-id="c6027-119">Método</span><span class="sxs-lookup"><span data-stu-id="c6027-119">Method</span></span>|<span data-ttu-id="c6027-120">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6027-120">Return Type</span></span>|<span data-ttu-id="c6027-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6027-121">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="c6027-122">Enumerar roleDefinitions</span><span class="sxs-lookup"><span data-stu-id="c6027-122">List roleDefinitions</span></span>](../api/intune-rbac-roledefinition-list.md)|<span data-ttu-id="c6027-123">Colección [roleDefinition](../resources/intune-rbac-roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="c6027-123">[roleDefinition](../resources/intune-rbac-roledefinition.md) collection</span></span>|<span data-ttu-id="c6027-124">Enumere las propiedades y las relaciones de los objetos [roleDefinition](../resources/intune-rbac-roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="c6027-124">List properties and relationships of the [roleDefinition](../resources/intune-rbac-roledefinition.md) objects.</span></span>|
|[<span data-ttu-id="c6027-125">Obtener roleDefinition</span><span class="sxs-lookup"><span data-stu-id="c6027-125">Get roleDefinition</span></span>](../api/intune-rbac-roledefinition-get.md)|[<span data-ttu-id="c6027-126">roleDefinition</span><span class="sxs-lookup"><span data-stu-id="c6027-126">roleDefinition</span></span>](../resources/intune-rbac-roledefinition.md)|<span data-ttu-id="c6027-127">Lea las propiedades y las relaciones del objeto [roleDefinition](../resources/intune-rbac-roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="c6027-127">Read properties and relationships of the [roleDefinition](../resources/intune-rbac-roledefinition.md) object.</span></span>|
|[<span data-ttu-id="c6027-128">Crear roleDefinition</span><span class="sxs-lookup"><span data-stu-id="c6027-128">Create roleDefinition</span></span>](../api/intune-rbac-roledefinition-create.md)|[<span data-ttu-id="c6027-129">roleDefinition</span><span class="sxs-lookup"><span data-stu-id="c6027-129">roleDefinition</span></span>](../resources/intune-rbac-roledefinition.md)|<span data-ttu-id="c6027-130">Cree un objeto [roleDefinition](../resources/intune-rbac-roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="c6027-130">Create a new [roleDefinition](../resources/intune-rbac-roledefinition.md) object.</span></span>|
|[<span data-ttu-id="c6027-131">Eliminar roleDefinition</span><span class="sxs-lookup"><span data-stu-id="c6027-131">Delete roleDefinition</span></span>](../api/intune-rbac-roledefinition-delete.md)|<span data-ttu-id="c6027-132">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c6027-132">None</span></span>|<span data-ttu-id="c6027-133">Elimina un [roleDefinition](../resources/intune-rbac-roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="c6027-133">Deletes a [roleDefinition](../resources/intune-rbac-roledefinition.md).</span></span>|
|[<span data-ttu-id="c6027-134">Actualizar roleDefinition</span><span class="sxs-lookup"><span data-stu-id="c6027-134">Update roleDefinition</span></span>](../api/intune-rbac-roledefinition-update.md)|[<span data-ttu-id="c6027-135">roleDefinition</span><span class="sxs-lookup"><span data-stu-id="c6027-135">roleDefinition</span></span>](../resources/intune-rbac-roledefinition.md)|<span data-ttu-id="c6027-136">Actualice las propiedades de un objeto [roleDefinition](../resources/intune-rbac-roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="c6027-136">Update the properties of a [roleDefinition](../resources/intune-rbac-roledefinition.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="c6027-137">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c6027-137">Properties</span></span>
|<span data-ttu-id="c6027-138">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c6027-138">Property</span></span>|<span data-ttu-id="c6027-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="c6027-139">Type</span></span>|<span data-ttu-id="c6027-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6027-140">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c6027-141">id</span><span class="sxs-lookup"><span data-stu-id="c6027-141">id</span></span>|<span data-ttu-id="c6027-142">String</span><span class="sxs-lookup"><span data-stu-id="c6027-142">String</span></span>|<span data-ttu-id="c6027-143">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="c6027-143">Key of the entity.</span></span> <span data-ttu-id="c6027-144">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="c6027-144">This is read-only and automatically generated.</span></span>|
|<span data-ttu-id="c6027-145">displayName</span><span class="sxs-lookup"><span data-stu-id="c6027-145">displayName</span></span>|<span data-ttu-id="c6027-146">String</span><span class="sxs-lookup"><span data-stu-id="c6027-146">String</span></span>|<span data-ttu-id="c6027-147">Nombre para mostrar de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="c6027-147">Display Name of the Role definition.</span></span>|
|<span data-ttu-id="c6027-148">description</span><span class="sxs-lookup"><span data-stu-id="c6027-148">description</span></span>|<span data-ttu-id="c6027-149">String</span><span class="sxs-lookup"><span data-stu-id="c6027-149">String</span></span>|<span data-ttu-id="c6027-150">Descripción de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="c6027-150">Description of the Role definition.</span></span>|
|<span data-ttu-id="c6027-151">rolePermissions</span><span class="sxs-lookup"><span data-stu-id="c6027-151">rolePermissions</span></span>|<span data-ttu-id="c6027-152">Colección [rolePermission](../resources/intune-rbac-rolepermission.md)</span><span class="sxs-lookup"><span data-stu-id="c6027-152">[rolePermission](../resources/intune-rbac-rolepermission.md) collection</span></span>|<span data-ttu-id="c6027-153">Lista de los permisos de rol que puede realizar este rol.</span><span class="sxs-lookup"><span data-stu-id="c6027-153">List of Role Permissions this role is allowed to perform.</span></span> <span data-ttu-id="c6027-154">Estos deben coincidir con el actionName que se definió como parte de rolePermission.</span><span class="sxs-lookup"><span data-stu-id="c6027-154">These must match the actionName that is defined as part of the rolePermission.</span></span>|
|<span data-ttu-id="c6027-155">isBuiltIn</span><span class="sxs-lookup"><span data-stu-id="c6027-155">isBuiltIn</span></span>|<span data-ttu-id="c6027-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="c6027-156">Boolean</span></span>|<span data-ttu-id="c6027-157">Tipo de rol.</span><span class="sxs-lookup"><span data-stu-id="c6027-157">Type of Role.</span></span> <span data-ttu-id="c6027-158">Se establece en True si está integrado o en False si es una definición de rol personalizada.</span><span class="sxs-lookup"><span data-stu-id="c6027-158">Set to True if it is built-in, or set to False if it is a custom role definition.</span></span>|

## <a name="relationships"></a><span data-ttu-id="c6027-159">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c6027-159">Relationships</span></span>
|<span data-ttu-id="c6027-160">Relación</span><span class="sxs-lookup"><span data-stu-id="c6027-160">Relationship</span></span>|<span data-ttu-id="c6027-161">Tipo</span><span class="sxs-lookup"><span data-stu-id="c6027-161">Type</span></span>|<span data-ttu-id="c6027-162">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6027-162">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c6027-163">roleAssignments</span><span class="sxs-lookup"><span data-stu-id="c6027-163">roleAssignments</span></span>|<span data-ttu-id="c6027-164">Colección [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="c6027-164">[roleAssignment](../resources/intune-rbac-roleassignment.md) collection</span></span>|<span data-ttu-id="c6027-165">Lista de asignaciones de rol para este rol.</span><span class="sxs-lookup"><span data-stu-id="c6027-165">List of Role assignments for this role definition.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="c6027-166">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c6027-166">JSON Representation</span></span>
<span data-ttu-id="c6027-167">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c6027-167">Here is a JSON representation of the resource.</span></span>
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
  "rolePermissions": [
    {
      "@odata.type": "microsoft.graph.rolePermission",
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
  "isBuiltIn": true
}
```



