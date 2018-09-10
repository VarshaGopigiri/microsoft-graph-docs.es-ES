# <a name="deviceconfigurationassignment-resource-type"></a><span data-ttu-id="17c32-101">Tipo de recurso deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="17c32-101">deviceConfigurationAssignment resource type</span></span>

> <span data-ttu-id="17c32-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="17c32-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="17c32-103">La entidad de asignación de la configuración de dispositivo asigna un grupo AAD a una configuración de dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="17c32-103">The device configuration assignment entity assigns an AAD group to a specific device configuration.</span></span>
## <a name="methods"></a><span data-ttu-id="17c32-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="17c32-104">Methods</span></span>
|<span data-ttu-id="17c32-105">Método</span><span class="sxs-lookup"><span data-stu-id="17c32-105">Method</span></span>|<span data-ttu-id="17c32-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17c32-106">Return Type</span></span>|<span data-ttu-id="17c32-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="17c32-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="17c32-108">Enumerar deviceConfigurationAssignments</span><span class="sxs-lookup"><span data-stu-id="17c32-108">List deviceConfigurationAssignments</span></span>](../api/intune_deviceconfig_deviceconfigurationassignment_list.md)|<span data-ttu-id="17c32-109">Colección [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md)</span><span class="sxs-lookup"><span data-stu-id="17c32-109">[deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md) collection</span></span>|<span data-ttu-id="17c32-110">Enumere las propiedades y las relaciones de los objetos [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="17c32-110">List properties and relationships of the [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md) objects.</span></span>|
|[<span data-ttu-id="17c32-111">Obtener deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="17c32-111">Get deviceConfigurationAssignment</span></span>](../api/intune_deviceconfig_deviceconfigurationassignment_get.md)|[<span data-ttu-id="17c32-112">deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="17c32-112">deviceConfigurationAssignment</span></span>](../resources/intune_deviceconfig_deviceconfigurationassignment.md)|<span data-ttu-id="17c32-113">Lea las propiedades y las relaciones del objeto [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="17c32-113">Read properties and relationships of the [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md) object.</span></span>|
|[<span data-ttu-id="17c32-114">Crear deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="17c32-114">Create deviceConfigurationAssignment</span></span>](../api/intune_deviceconfig_deviceconfigurationassignment_create.md)|[<span data-ttu-id="17c32-115">deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="17c32-115">deviceConfigurationAssignment</span></span>](../resources/intune_deviceconfig_deviceconfigurationassignment.md)|<span data-ttu-id="17c32-116">Cree un objeto [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="17c32-116">Create a new [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md) object.</span></span>|
|[<span data-ttu-id="17c32-117">Eliminar deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="17c32-117">Delete deviceConfigurationAssignment</span></span>](../api/intune_deviceconfig_deviceconfigurationassignment_delete.md)|<span data-ttu-id="17c32-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="17c32-118">None</span></span>|<span data-ttu-id="17c32-119">Elimina un [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="17c32-119">Deletes a [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md).</span></span>|
|[<span data-ttu-id="17c32-120">Actualizar deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="17c32-120">Update deviceConfigurationAssignment</span></span>](../api/intune_deviceconfig_deviceconfigurationassignment_update.md)|[<span data-ttu-id="17c32-121">deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="17c32-121">deviceConfigurationAssignment</span></span>](../resources/intune_deviceconfig_deviceconfigurationassignment.md)|<span data-ttu-id="17c32-122">Actualice las propiedades de un objeto [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="17c32-122">Update the properties of a [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="17c32-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="17c32-123">Properties</span></span>
|<span data-ttu-id="17c32-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="17c32-124">Property</span></span>|<span data-ttu-id="17c32-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="17c32-125">Type</span></span>|<span data-ttu-id="17c32-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="17c32-126">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="17c32-127">id</span><span class="sxs-lookup"><span data-stu-id="17c32-127">id</span></span>|<span data-ttu-id="17c32-128">String</span><span class="sxs-lookup"><span data-stu-id="17c32-128">String</span></span>|<span data-ttu-id="17c32-129">La clave de la asignación.</span><span class="sxs-lookup"><span data-stu-id="17c32-129">The key of the assignment.</span></span>|
|<span data-ttu-id="17c32-130">target</span><span class="sxs-lookup"><span data-stu-id="17c32-130">target</span></span>|[<span data-ttu-id="17c32-131">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="17c32-131">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune_shared_deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="17c32-132">El destino de la tarea para la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="17c32-132">The assignment target for the device configuration.</span></span>|

## <a name="relationships"></a><span data-ttu-id="17c32-133">Relaciones</span><span class="sxs-lookup"><span data-stu-id="17c32-133">Relationships</span></span>
<span data-ttu-id="17c32-134">Ninguna</span><span class="sxs-lookup"><span data-stu-id="17c32-134">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="17c32-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="17c32-135">JSON Representation</span></span>
<span data-ttu-id="17c32-136">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="17c32-136">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceConfigurationAssignment"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceConfigurationAssignment",
  "id": "String (identifier)",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```








