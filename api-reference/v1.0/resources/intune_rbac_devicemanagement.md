# <a name="devicemanagement-resource-type"></a><span data-ttu-id="8d97d-101">Tipo de recurso deviceManagement</span><span class="sxs-lookup"><span data-stu-id="8d97d-101">deviceManagement resource type</span></span>

> <span data-ttu-id="8d97d-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8d97d-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8d97d-103">Entidad singleton que actúa como un contenedor para todas las funcionalidades de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="8d97d-103">Singleton entity that acts as a container for all device management functionality.</span></span>
## <a name="methods"></a><span data-ttu-id="8d97d-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="8d97d-104">Methods</span></span>
|<span data-ttu-id="8d97d-105">Método</span><span class="sxs-lookup"><span data-stu-id="8d97d-105">Method</span></span>|<span data-ttu-id="8d97d-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d97d-106">Return Type</span></span>|<span data-ttu-id="8d97d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d97d-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="8d97d-108">Obtener deviceManagement</span><span class="sxs-lookup"><span data-stu-id="8d97d-108">Get deviceManagement</span></span>](../api/intune_rbac_devicemanagement_get.md)|[<span data-ttu-id="8d97d-109">deviceManagement</span><span class="sxs-lookup"><span data-stu-id="8d97d-109">deviceManagement</span></span>](../resources/intune_rbac_devicemanagement.md)|<span data-ttu-id="8d97d-110">Lea las propiedades y las relaciones del objeto [deviceManagement](../resources/intune_rbac_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="8d97d-110">Read properties and relationships of [plannerTaskDetails](../resources/intune_rbac_devicemanagement.md) object.</span></span>|
|[<span data-ttu-id="8d97d-111">Actualizar deviceManagement</span><span class="sxs-lookup"><span data-stu-id="8d97d-111">Update deviceManagement</span></span>](../api/intune_rbac_devicemanagement_update.md)|[<span data-ttu-id="8d97d-112">deviceManagement</span><span class="sxs-lookup"><span data-stu-id="8d97d-112">deviceManagement</span></span>](../resources/intune_rbac_devicemanagement.md)|<span data-ttu-id="8d97d-113">Actualice las propiedades de un objeto [deviceManagement](../resources/intune_rbac_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="8d97d-113">Update the properties of a [calendar](../resources/intune_rbac_devicemanagement.md) object.</span></span>|
|[<span data-ttu-id="8d97d-114">Función getEffectivePermissions</span><span class="sxs-lookup"><span data-stu-id="8d97d-114">getEffectivePermissions function</span></span>](../api/intune_rbac_devicemanagement_geteffectivepermissions.md)|<span data-ttu-id="8d97d-115">Colección [rolePermission](../resources/intune_rbac_rolepermission.md)</span><span class="sxs-lookup"><span data-stu-id="8d97d-115">[rolePermission](../resources/intune_rbac_rolepermission.md) collection</span></span>|<span data-ttu-id="8d97d-116">Recupera los permisos efectivos del usuario autenticado actualmente</span><span class="sxs-lookup"><span data-stu-id="8d97d-116">Retrieves the effective permissions of the currently authenticated user</span></span>|

## <a name="properties"></a><span data-ttu-id="8d97d-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8d97d-117">Properties</span></span>
|<span data-ttu-id="8d97d-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8d97d-118">Property</span></span>|<span data-ttu-id="8d97d-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="8d97d-119">Type</span></span>|<span data-ttu-id="8d97d-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d97d-120">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8d97d-121">id</span><span class="sxs-lookup"><span data-stu-id="8d97d-121">id</span></span>|<span data-ttu-id="8d97d-122">cadena</span><span class="sxs-lookup"><span data-stu-id="8d97d-122">String</span></span>|<span data-ttu-id="8d97d-123">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="8d97d-123">Not yet documented</span></span>|

## <a name="relationships"></a><span data-ttu-id="8d97d-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8d97d-124">Relationships</span></span>
|<span data-ttu-id="8d97d-125">Relación</span><span class="sxs-lookup"><span data-stu-id="8d97d-125">Relationship</span></span>|<span data-ttu-id="8d97d-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="8d97d-126">Type</span></span>|<span data-ttu-id="8d97d-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d97d-127">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8d97d-128">roleDefinitions</span><span class="sxs-lookup"><span data-stu-id="8d97d-128">roleDefinitions</span></span>|<span data-ttu-id="8d97d-129">Colección [roleDefinition](../resources/intune_rbac_roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="8d97d-129">[roleDefinition](../resources/intune_rbac_roledefinition.md) collection</span></span>|<span data-ttu-id="8d97d-130">Las definiciones de roles.</span><span class="sxs-lookup"><span data-stu-id="8d97d-130">The Role Definitions.</span></span>|
|<span data-ttu-id="8d97d-131">roleAssignments</span><span class="sxs-lookup"><span data-stu-id="8d97d-131">roleAssignments</span></span>|<span data-ttu-id="8d97d-132">Colección [deviceAndAppManagementRoleAssignment](../resources/intune_rbac_deviceandappmanagementroleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="8d97d-132">[deviceAndAppManagementRoleAssignment](../resources/intune_rbac_deviceandappmanagementroleassignment.md) collection</span></span>|<span data-ttu-id="8d97d-133">Las asignaciones de roles.</span><span class="sxs-lookup"><span data-stu-id="8d97d-133">The Role Assignments.</span></span>|
|<span data-ttu-id="8d97d-134">resourceOperations</span><span class="sxs-lookup"><span data-stu-id="8d97d-134">resourceOperations</span></span>|<span data-ttu-id="8d97d-135">Colección [resourceOperation](../resources/intune_rbac_resourceoperation.md)</span><span class="sxs-lookup"><span data-stu-id="8d97d-135">[resourceOperation](../resources/intune_rbac_resourceoperation.md) collection</span></span>|<span data-ttu-id="8d97d-136">Las operaciones de recursos.</span><span class="sxs-lookup"><span data-stu-id="8d97d-136">The Resource Operations.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="8d97d-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8d97d-137">JSON Representation</span></span>
<span data-ttu-id="8d97d-138">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8d97d-138">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagement"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagement",
  "id": "String (identifier)"
}
```



