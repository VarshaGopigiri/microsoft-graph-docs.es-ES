# <a name="roledefinition-resource-type"></a><span data-ttu-id="272f4-101">Tipo de recurso roleDefinition</span><span class="sxs-lookup"><span data-stu-id="272f4-101">roleDefinition resource type</span></span>

> <span data-ttu-id="272f4-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="272f4-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="272f4-103">El recurso de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="272f4-103">The Role Definition resource.</span></span> <span data-ttu-id="272f4-104">La definición de rol es el pilar del acceso basado en roles en Intune.</span><span class="sxs-lookup"><span data-stu-id="272f4-104">The role definition is the foundation of role based access in Intune.</span></span> <span data-ttu-id="272f4-105">El rol combina un recurso de Intune, como una aplicación móvil, y los permisos de rol asociados para el recurso, como Creación o Lectura.</span><span class="sxs-lookup"><span data-stu-id="272f4-105">The role combines an Intune resource such as a Mobile App and associated role permissions such as Create or Read for the resource.</span></span> <span data-ttu-id="272f4-106">Hay dos tipos de roles: personalizados e integrados.</span><span class="sxs-lookup"><span data-stu-id="272f4-106">There are two types of roles, built-in and custom.</span></span> <span data-ttu-id="272f4-107">Los roles integrados no se pueden modificar.</span><span class="sxs-lookup"><span data-stu-id="272f4-107">Built-in roles cannot be modified.</span></span> <span data-ttu-id="272f4-108">Tanto los roles personalizados como los integrados deben tener asignaciones que se aplicarán.</span><span class="sxs-lookup"><span data-stu-id="272f4-108">Both built-in roles and custom roles must have assignments to be enforced.</span></span> <span data-ttu-id="272f4-109">Cree roles personalizados para definir un rol que permita que se combine cualquier recurso disponible y permiso de rol en un solo rol.</span><span class="sxs-lookup"><span data-stu-id="272f4-109">Create custom roles if you want to define a role that allows any of the available resources and role permissions to be combined into a single role.</span></span>
## <a name="methods"></a><span data-ttu-id="272f4-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="272f4-110">Methods</span></span>
|<span data-ttu-id="272f4-111">Método</span><span class="sxs-lookup"><span data-stu-id="272f4-111">Method</span></span>|<span data-ttu-id="272f4-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="272f4-112">Return Type</span></span>|<span data-ttu-id="272f4-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="272f4-113">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="272f4-114">Enumerar roleDefinitions</span><span class="sxs-lookup"><span data-stu-id="272f4-114">List roleDefinitions</span></span>](../api/intune_rbac_roledefinition_list.md)|<span data-ttu-id="272f4-115">Colección [roleDefinition](../resources/intune_rbac_roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="272f4-115">[roleDefinition](../resources/intune_rbac_roledefinition.md) collection</span></span>|<span data-ttu-id="272f4-116">Enumere las propiedades y las relaciones de los objetos [roleDefinition](../resources/intune_rbac_roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="272f4-116">List properties and relationships of the [roleDefinition](../resources/intune_rbac_roledefinition.md) objects.</span></span>|
|[<span data-ttu-id="272f4-117">Obtener roleDefinition</span><span class="sxs-lookup"><span data-stu-id="272f4-117">Get roleDefinition</span></span>](../api/intune_rbac_roledefinition_get.md)|[<span data-ttu-id="272f4-118">roleDefinition</span><span class="sxs-lookup"><span data-stu-id="272f4-118">roleDefinition</span></span>](../resources/intune_rbac_roledefinition.md)|<span data-ttu-id="272f4-119">Lea las propiedades y las relaciones del objeto [roleDefinition](../resources/intune_rbac_roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="272f4-119">Read properties and relationships of [plannerProgressTaskBoardTaskFormat](../resources/intune_rbac_roledefinition.md) object.</span></span>|
|[<span data-ttu-id="272f4-120">Crear roleDefinition</span><span class="sxs-lookup"><span data-stu-id="272f4-120">Create roleDefinition</span></span>](../api/intune_rbac_roledefinition_create.md)|[<span data-ttu-id="272f4-121">roleDefinition</span><span class="sxs-lookup"><span data-stu-id="272f4-121">roleDefinition</span></span>](../resources/intune_rbac_roledefinition.md)|<span data-ttu-id="272f4-122">Cree un objeto [roleDefinition](../resources/intune_rbac_roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="272f4-122">Create a new [plannerBucket](../resources/intune_rbac_roledefinition.md) object.</span></span>|
|[<span data-ttu-id="272f4-123">Eliminar roleDefinition</span><span class="sxs-lookup"><span data-stu-id="272f4-123">Delete roleDefinition</span></span>](../api/intune_rbac_roledefinition_delete.md)|<span data-ttu-id="272f4-124">Ninguno</span><span class="sxs-lookup"><span data-stu-id="272f4-124">None</span></span>|<span data-ttu-id="272f4-125">Elimina un [roleDefinition](../resources/intune_rbac_roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="272f4-125">Deletes a [roleDefinition](../resources/intune_rbac_roledefinition.md).</span></span>|
|[<span data-ttu-id="272f4-126">Actualizar roleDefinition</span><span class="sxs-lookup"><span data-stu-id="272f4-126">Update roleDefinition</span></span>](../api/intune_rbac_roledefinition_update.md)|[<span data-ttu-id="272f4-127">roleDefinition</span><span class="sxs-lookup"><span data-stu-id="272f4-127">roleDefinition</span></span>](../resources/intune_rbac_roledefinition.md)|<span data-ttu-id="272f4-128">Actualice las propiedades de un objeto [roleDefinition](../resources/intune_rbac_roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="272f4-128">Update the properties of a [calendar](../resources/intune_rbac_roledefinition.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="272f4-129">Propiedades</span><span class="sxs-lookup"><span data-stu-id="272f4-129">Properties</span></span>
|<span data-ttu-id="272f4-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="272f4-130">Property</span></span>|<span data-ttu-id="272f4-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="272f4-131">Type</span></span>|<span data-ttu-id="272f4-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="272f4-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="272f4-133">id</span><span class="sxs-lookup"><span data-stu-id="272f4-133">id</span></span>|<span data-ttu-id="272f4-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="272f4-134">String</span></span>|<span data-ttu-id="272f4-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="272f4-135">Key of the setting.</span></span> <span data-ttu-id="272f4-136">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="272f4-136">This is read-only and automatically generated.</span></span>|
|<span data-ttu-id="272f4-137">displayName</span><span class="sxs-lookup"><span data-stu-id="272f4-137">displayName</span></span>|<span data-ttu-id="272f4-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="272f4-138">String</span></span>|<span data-ttu-id="272f4-139">Nombre para mostrar de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="272f4-139">Display Name of the Role definition.</span></span>|
|<span data-ttu-id="272f4-140">description</span><span class="sxs-lookup"><span data-stu-id="272f4-140">description</span></span>|<span data-ttu-id="272f4-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="272f4-141">String</span></span>|<span data-ttu-id="272f4-142">Descripción de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="272f4-142">Description of the Role definition.</span></span>|
|<span data-ttu-id="272f4-143">rolePermissions</span><span class="sxs-lookup"><span data-stu-id="272f4-143">rolePermissions</span></span>|<span data-ttu-id="272f4-144">Colección [rolePermission](../resources/intune_rbac_rolepermission.md)</span><span class="sxs-lookup"><span data-stu-id="272f4-144">[rolePermission](../resources/intune_rbac_rolepermission.md) collection</span></span>|<span data-ttu-id="272f4-145">Lista de los permisos de rol que puede realizar este rol.</span><span class="sxs-lookup"><span data-stu-id="272f4-145">List of Role Permissions this role is allowed to perform.</span></span> <span data-ttu-id="272f4-146">Estos deben coincidir con el actionName que se definió como parte de rolePermission.</span><span class="sxs-lookup"><span data-stu-id="272f4-146">These must match the actionName that is defined as part of the rolePermission.</span></span>|
|<span data-ttu-id="272f4-147">isBuiltIn</span><span class="sxs-lookup"><span data-stu-id="272f4-147">isBuiltIn</span></span>|<span data-ttu-id="272f4-148">Booleano</span><span class="sxs-lookup"><span data-stu-id="272f4-148">Boolean</span></span>|<span data-ttu-id="272f4-149">Tipo de rol.</span><span class="sxs-lookup"><span data-stu-id="272f4-149">Type of Role.</span></span> <span data-ttu-id="272f4-150">Se establece en True si está integrado o en False si es una definición de rol personalizada.</span><span class="sxs-lookup"><span data-stu-id="272f4-150">Set to True if it is built-in, or set to False if it is a custom role definition.</span></span>|

## <a name="relationships"></a><span data-ttu-id="272f4-151">Relaciones</span><span class="sxs-lookup"><span data-stu-id="272f4-151">Relationships</span></span>
|<span data-ttu-id="272f4-152">Relación</span><span class="sxs-lookup"><span data-stu-id="272f4-152">Relationship</span></span>|<span data-ttu-id="272f4-153">Tipo</span><span class="sxs-lookup"><span data-stu-id="272f4-153">Type</span></span>|<span data-ttu-id="272f4-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="272f4-154">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="272f4-155">roleAssignments</span><span class="sxs-lookup"><span data-stu-id="272f4-155">roleAssignments</span></span>|<span data-ttu-id="272f4-156">Colección [roleAssignment](../resources/intune_rbac_roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="272f4-156">[roleAssignment](../resources/intune_rbac_roleassignment.md) collection</span></span>|<span data-ttu-id="272f4-157">Lista de asignaciones de rol para este rol.</span><span class="sxs-lookup"><span data-stu-id="272f4-157">List of Role assignments for this role definition.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="272f4-158">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="272f4-158">JSON Representation</span></span>
<span data-ttu-id="272f4-159">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="272f4-159">Here is a JSON representation of the resource.</span></span>
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



