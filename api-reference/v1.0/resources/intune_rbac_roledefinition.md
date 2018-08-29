# <a name="roledefinition-resource-type"></a><span data-ttu-id="ce894-101">Tipo de recurso roleDefinition</span><span class="sxs-lookup"><span data-stu-id="ce894-101">roleDefinition resource type</span></span>

> <span data-ttu-id="ce894-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ce894-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ce894-103">El recurso de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="ce894-103">The Role Definition resource.</span></span> <span data-ttu-id="ce894-104">La definición de rol es el pilar del acceso basado en roles en Intune.</span><span class="sxs-lookup"><span data-stu-id="ce894-104">The role definition is the foundation of role based access in Intune.</span></span> <span data-ttu-id="ce894-105">El rol combina un recurso de Intune, como una aplicación móvil, y los permisos de rol asociados para el recurso, como Creación o Lectura.</span><span class="sxs-lookup"><span data-stu-id="ce894-105">The role combines an Intune resource such as a Mobile App and associated role permissions such as Create or Read for the resource.</span></span> <span data-ttu-id="ce894-106">Hay dos tipos de roles: personalizados e integrados.</span><span class="sxs-lookup"><span data-stu-id="ce894-106">There are two types of roles, built-in and custom.</span></span> <span data-ttu-id="ce894-107">Los roles integrados no se pueden modificar.</span><span class="sxs-lookup"><span data-stu-id="ce894-107">Built-in roles cannot be modified.</span></span> <span data-ttu-id="ce894-108">Tanto los roles personalizados como los integrados deben tener asignaciones que se aplicarán.</span><span class="sxs-lookup"><span data-stu-id="ce894-108">Both built-in roles and custom roles must have assignments to be enforced.</span></span> <span data-ttu-id="ce894-109">Cree roles personalizados para definir un rol que permita que se combine cualquier recurso disponible y permiso de rol en un solo rol.</span><span class="sxs-lookup"><span data-stu-id="ce894-109">Create custom roles if you want to define a role that allows any of the available resources and role permissions to be combined into a single role.</span></span>
## <a name="methods"></a><span data-ttu-id="ce894-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="ce894-110">Methods</span></span>
|<span data-ttu-id="ce894-111">Método</span><span class="sxs-lookup"><span data-stu-id="ce894-111">Method</span></span>|<span data-ttu-id="ce894-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce894-112">Return Type</span></span>|<span data-ttu-id="ce894-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce894-113">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="ce894-114">Enumerar roleDefinitions</span><span class="sxs-lookup"><span data-stu-id="ce894-114">List roleDefinitions</span></span>](../api/intune_rbac_roledefinition_list.md)|<span data-ttu-id="ce894-115">Colección [roleDefinition](../resources/intune_rbac_roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="ce894-115">[roleDefinition](../resources/intune_rbac_roledefinition.md) collection</span></span>|<span data-ttu-id="ce894-116">Enumere las propiedades y las relaciones de los objetos [roleDefinition](../resources/intune_rbac_roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="ce894-116">List properties and relationships of the [roleDefinition](../resources/intune_rbac_roledefinition.md) objects.</span></span>|
|[<span data-ttu-id="ce894-117">Obtener roleDefinition</span><span class="sxs-lookup"><span data-stu-id="ce894-117">Get roleDefinition</span></span>](../api/intune_rbac_roledefinition_get.md)|[<span data-ttu-id="ce894-118">roleDefinition</span><span class="sxs-lookup"><span data-stu-id="ce894-118">roleDefinition</span></span>](../resources/intune_rbac_roledefinition.md)|<span data-ttu-id="ce894-119">Lea las propiedades y las relaciones del objeto [roleDefinition](../resources/intune_rbac_roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="ce894-119">Read properties and relationships of the [roleDefinition](../resources/intune_rbac_roledefinition.md) object.</span></span>|
|[<span data-ttu-id="ce894-120">Crear roleDefinition</span><span class="sxs-lookup"><span data-stu-id="ce894-120">Create roleDefinition</span></span>](../api/intune_rbac_roledefinition_create.md)|[<span data-ttu-id="ce894-121">roleDefinition</span><span class="sxs-lookup"><span data-stu-id="ce894-121">roleDefinition</span></span>](../resources/intune_rbac_roledefinition.md)|<span data-ttu-id="ce894-122">Cree un objeto [roleDefinition](../resources/intune_rbac_roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="ce894-122">Create a new [roleDefinition](../resources/intune_rbac_roledefinition.md) object.</span></span>|
|[<span data-ttu-id="ce894-123">Eliminar roleDefinition</span><span class="sxs-lookup"><span data-stu-id="ce894-123">Delete roleDefinition</span></span>](../api/intune_rbac_roledefinition_delete.md)|<span data-ttu-id="ce894-124">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ce894-124">None</span></span>|<span data-ttu-id="ce894-125">Elimina un [roleDefinition](../resources/intune_rbac_roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="ce894-125">Deletes a [roleDefinition](../resources/intune_rbac_roledefinition.md).</span></span>|
|[<span data-ttu-id="ce894-126">Actualizar roleDefinition</span><span class="sxs-lookup"><span data-stu-id="ce894-126">Update roleDefinition</span></span>](../api/intune_rbac_roledefinition_update.md)|[<span data-ttu-id="ce894-127">roleDefinition</span><span class="sxs-lookup"><span data-stu-id="ce894-127">roleDefinition</span></span>](../resources/intune_rbac_roledefinition.md)|<span data-ttu-id="ce894-128">Actualice las propiedades de un objeto [roleDefinition](../resources/intune_rbac_roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="ce894-128">Update the properties of a [roleDefinition](../resources/intune_rbac_roledefinition.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="ce894-129">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ce894-129">Properties</span></span>
|<span data-ttu-id="ce894-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ce894-130">Property</span></span>|<span data-ttu-id="ce894-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="ce894-131">Type</span></span>|<span data-ttu-id="ce894-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce894-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ce894-133">id</span><span class="sxs-lookup"><span data-stu-id="ce894-133">id</span></span>|<span data-ttu-id="ce894-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="ce894-134">String</span></span>|<span data-ttu-id="ce894-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ce894-135">Key of the entity.</span></span> <span data-ttu-id="ce894-136">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="ce894-136">This is read-only and automatically generated.</span></span>|
|<span data-ttu-id="ce894-137">displayName</span><span class="sxs-lookup"><span data-stu-id="ce894-137">displayName</span></span>|<span data-ttu-id="ce894-138">String</span><span class="sxs-lookup"><span data-stu-id="ce894-138">String</span></span>|<span data-ttu-id="ce894-139">Nombre para mostrar de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="ce894-139">Display Name of the Role definition.</span></span>|
|<span data-ttu-id="ce894-140">description</span><span class="sxs-lookup"><span data-stu-id="ce894-140">description</span></span>|<span data-ttu-id="ce894-141">String</span><span class="sxs-lookup"><span data-stu-id="ce894-141">String</span></span>|<span data-ttu-id="ce894-142">Descripción de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="ce894-142">Description of the Role definition.</span></span>|
|<span data-ttu-id="ce894-143">rolePermissions</span><span class="sxs-lookup"><span data-stu-id="ce894-143">rolePermissions</span></span>|<span data-ttu-id="ce894-144">Colección [rolePermission](../resources/intune_rbac_rolepermission.md)</span><span class="sxs-lookup"><span data-stu-id="ce894-144">[rolePermission](../resources/intune_rbac_rolepermission.md) collection</span></span>|<span data-ttu-id="ce894-145">Lista de los permisos de rol que puede realizar este rol.</span><span class="sxs-lookup"><span data-stu-id="ce894-145">List of Role Permissions this role is allowed to perform.</span></span> <span data-ttu-id="ce894-146">Estos deben coincidir con el actionName que se definió como parte de rolePermission.</span><span class="sxs-lookup"><span data-stu-id="ce894-146">These must match the actionName that is defined as part of the rolePermission.</span></span>|
|<span data-ttu-id="ce894-147">isBuiltIn</span><span class="sxs-lookup"><span data-stu-id="ce894-147">isBuiltIn</span></span>|<span data-ttu-id="ce894-148">Boolean</span><span class="sxs-lookup"><span data-stu-id="ce894-148">Boolean</span></span>|<span data-ttu-id="ce894-149">Tipo de rol.</span><span class="sxs-lookup"><span data-stu-id="ce894-149">Type of Role.</span></span> <span data-ttu-id="ce894-150">Se establece en True si está integrado o en False si es una definición de rol personalizada.</span><span class="sxs-lookup"><span data-stu-id="ce894-150">Set to True if it is built-in, or set to False if it is a custom role definition.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ce894-151">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ce894-151">Relationships</span></span>
|<span data-ttu-id="ce894-152">Relación</span><span class="sxs-lookup"><span data-stu-id="ce894-152">Relationship</span></span>|<span data-ttu-id="ce894-153">Tipo</span><span class="sxs-lookup"><span data-stu-id="ce894-153">Type</span></span>|<span data-ttu-id="ce894-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce894-154">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ce894-155">roleAssignments</span><span class="sxs-lookup"><span data-stu-id="ce894-155">roleAssignments</span></span>|<span data-ttu-id="ce894-156">Colección [roleAssignment](../resources/intune_rbac_roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="ce894-156">[roleAssignment](../resources/intune_rbac_roleassignment.md) collection</span></span>|<span data-ttu-id="ce894-157">Lista de asignaciones de rol para este rol.</span><span class="sxs-lookup"><span data-stu-id="ce894-157">List of Role assignments for this role definition.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ce894-158">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ce894-158">JSON Representation</span></span>
<span data-ttu-id="ce894-159">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ce894-159">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.roleDefinition"
}-->
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



