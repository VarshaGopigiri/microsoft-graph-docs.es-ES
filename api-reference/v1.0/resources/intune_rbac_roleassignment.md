# <a name="roleassignment-resource-type"></a><span data-ttu-id="c32d6-101">Tipo de recurso roleAssignment</span><span class="sxs-lookup"><span data-stu-id="c32d6-101">roleAssignment resource type</span></span>

> <span data-ttu-id="c32d6-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c32d6-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c32d6-103">El recurso de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="c32d6-103">The Role Assignment resource.</span></span> <span data-ttu-id="c32d6-104">Las asignaciones de roles unen la definición de rol con miembros y ámbitos.</span><span class="sxs-lookup"><span data-stu-id="c32d6-104">Role assignments tie together a role definition with members and scopes.</span></span> <span data-ttu-id="c32d6-105">Puede haber una o más asignaciones de roles por rol.</span><span class="sxs-lookup"><span data-stu-id="c32d6-105">There can be one or more role assignments per role.</span></span> <span data-ttu-id="c32d6-106">Esto se aplica a los roles integrados y personalizados.</span><span class="sxs-lookup"><span data-stu-id="c32d6-106">This applies to custom and built-in roles.</span></span>
## <a name="methods"></a><span data-ttu-id="c32d6-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="c32d6-107">Methods</span></span>
|<span data-ttu-id="c32d6-108">Método</span><span class="sxs-lookup"><span data-stu-id="c32d6-108">Method</span></span>|<span data-ttu-id="c32d6-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c32d6-109">Return Type</span></span>|<span data-ttu-id="c32d6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c32d6-110">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="c32d6-111">Enumerar roleAssignments</span><span class="sxs-lookup"><span data-stu-id="c32d6-111">List roleAssignments</span></span>](../api/intune_rbac_roleassignment_list.md)|<span data-ttu-id="c32d6-112">Colección [roleAssignment](../resources/intune_rbac_roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="c32d6-112">[roleAssignment](../resources/intune_rbac_roleassignment.md) collection</span></span>|<span data-ttu-id="c32d6-113">Enumere las propiedades y las relaciones de los objetos [roleAssignment](../resources/intune_rbac_roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="c32d6-113">List properties and relationships of the [roleAssignment](../resources/intune_rbac_roleassignment.md) objects.</span></span>|
|[<span data-ttu-id="c32d6-114">Obtener roleAssignment</span><span class="sxs-lookup"><span data-stu-id="c32d6-114">Get roleAssignment</span></span>](../api/intune_rbac_roleassignment_get.md)|[<span data-ttu-id="c32d6-115">roleAssignment</span><span class="sxs-lookup"><span data-stu-id="c32d6-115">roleAssignment</span></span>](../resources/intune_rbac_roleassignment.md)|<span data-ttu-id="c32d6-116">Lea las propiedades y las relaciones del objeto [roleAssignment](../resources/intune_rbac_roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="c32d6-116">Read properties and relationships of the [roleAssignment](../resources/intune_rbac_roleassignment.md) object.</span></span>|
|[<span data-ttu-id="c32d6-117">Crear roleAssignment</span><span class="sxs-lookup"><span data-stu-id="c32d6-117">Create roleAssignment</span></span>](../api/intune_rbac_roleassignment_create.md)|[<span data-ttu-id="c32d6-118">roleAssignment</span><span class="sxs-lookup"><span data-stu-id="c32d6-118">roleAssignment</span></span>](../resources/intune_rbac_roleassignment.md)|<span data-ttu-id="c32d6-119">Cree un objeto [roleAssignment](../resources/intune_rbac_roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="c32d6-119">Create a new [roleAssignment](../resources/intune_rbac_roleassignment.md) object.</span></span>|
|[<span data-ttu-id="c32d6-120">Eliminar roleAssignment</span><span class="sxs-lookup"><span data-stu-id="c32d6-120">Delete roleAssignment</span></span>](../api/intune_rbac_roleassignment_delete.md)|<span data-ttu-id="c32d6-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c32d6-121">None</span></span>|<span data-ttu-id="c32d6-122">Elimina un [roleAssignment](../resources/intune_rbac_roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="c32d6-122">Deletes a [roleAssignment](../resources/intune_rbac_roleassignment.md).</span></span>|
|[<span data-ttu-id="c32d6-123">Actualizar roleAssignment</span><span class="sxs-lookup"><span data-stu-id="c32d6-123">Update roleAssignment</span></span>](../api/intune_rbac_roleassignment_update.md)|[<span data-ttu-id="c32d6-124">roleAssignment</span><span class="sxs-lookup"><span data-stu-id="c32d6-124">roleAssignment</span></span>](../resources/intune_rbac_roleassignment.md)|<span data-ttu-id="c32d6-125">Actualice las propiedades de un objeto [roleAssignment](../resources/intune_rbac_roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="c32d6-125">Update the properties of a [roleAssignment](../resources/intune_rbac_roleassignment.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="c32d6-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c32d6-126">Properties</span></span>
|<span data-ttu-id="c32d6-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c32d6-127">Property</span></span>|<span data-ttu-id="c32d6-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="c32d6-128">Type</span></span>|<span data-ttu-id="c32d6-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="c32d6-129">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c32d6-130">id</span><span class="sxs-lookup"><span data-stu-id="c32d6-130">id</span></span>|<span data-ttu-id="c32d6-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="c32d6-131">String</span></span>|<span data-ttu-id="c32d6-132">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="c32d6-132">Key of the entity.</span></span> <span data-ttu-id="c32d6-133">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="c32d6-133">This is read-only and automatically generated.</span></span>|
|<span data-ttu-id="c32d6-134">displayName</span><span class="sxs-lookup"><span data-stu-id="c32d6-134">displayName</span></span>|<span data-ttu-id="c32d6-135">String</span><span class="sxs-lookup"><span data-stu-id="c32d6-135">String</span></span>|<span data-ttu-id="c32d6-136">El nombre descriptivo o para mostrar de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="c32d6-136">The display or friendly name of the role Assignment.</span></span>|
|<span data-ttu-id="c32d6-137">descripción</span><span class="sxs-lookup"><span data-stu-id="c32d6-137">description</span></span>|<span data-ttu-id="c32d6-138">String</span><span class="sxs-lookup"><span data-stu-id="c32d6-138">String</span></span>|<span data-ttu-id="c32d6-139">Descripción de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="c32d6-139">Description of the Role Assignment.</span></span>|
|<span data-ttu-id="c32d6-140">resourceScopes</span><span class="sxs-lookup"><span data-stu-id="c32d6-140">resourceScopes</span></span>|<span data-ttu-id="c32d6-141">Colección string</span><span class="sxs-lookup"><span data-stu-id="c32d6-141">String collection</span></span>|<span data-ttu-id="c32d6-142">Lista de identificadores de grupos de seguridad de miembros del ámbito de roles.</span><span class="sxs-lookup"><span data-stu-id="c32d6-142">List of ids of role scope member security groups.</span></span>  <span data-ttu-id="c32d6-143">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c32d6-143">These are IDs from Azure Active Directory.</span></span>|

## <a name="relationships"></a><span data-ttu-id="c32d6-144">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c32d6-144">Relationships</span></span>
|<span data-ttu-id="c32d6-145">Relación</span><span class="sxs-lookup"><span data-stu-id="c32d6-145">Relationship</span></span>|<span data-ttu-id="c32d6-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="c32d6-146">Type</span></span>|<span data-ttu-id="c32d6-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="c32d6-147">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c32d6-148">roleDefinition</span><span class="sxs-lookup"><span data-stu-id="c32d6-148">roleDefinition</span></span>|[<span data-ttu-id="c32d6-149">roleDefinition</span><span class="sxs-lookup"><span data-stu-id="c32d6-149">roleDefinition</span></span>](../resources/intune_rbac_roledefinition.md)|<span data-ttu-id="c32d6-150">Definición de rol del que forma parte esta asignación.</span><span class="sxs-lookup"><span data-stu-id="c32d6-150">Role definition this assignment is part of.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="c32d6-151">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c32d6-151">JSON Representation</span></span>
<span data-ttu-id="c32d6-152">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c32d6-152">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.roleAssignment"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.roleAssignment",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "resourceScopes": [
    "String"
  ]
}
```








