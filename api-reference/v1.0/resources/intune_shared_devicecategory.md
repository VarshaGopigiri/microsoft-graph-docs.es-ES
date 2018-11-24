# <a name="devicecategory-resource-type"></a><span data-ttu-id="642dc-101">Tipo de recurso deviceCategory</span><span class="sxs-lookup"><span data-stu-id="642dc-101">deviceCategory resource type</span></span>

> <span data-ttu-id="642dc-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="642dc-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="642dc-103">Las categorías de dispositivo proporcionan una forma de organizar sus dispositivos.</span><span class="sxs-lookup"><span data-stu-id="642dc-103">Device categories provides a way to organize your devices.</span></span> <span data-ttu-id="642dc-104">Al usar categorías de dispositivos, los administradores de la compañía pueden definir las categorías de forma pertinente para su empresa.</span><span class="sxs-lookup"><span data-stu-id="642dc-104">Using device categories, company administrators can define their own categories that make sense to their company.</span></span><span data-ttu-id="642dc-105">A continuación, estas categorías se pueden aplicar a un dispositivo en la consola de Azure de Intune o un usuario puede seleccionarlas durante la inscripción de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="642dc-105"> These categories can then be applied to a device in the Intune Azure console or selected by a user during device enrollment.</span></span> <span data-ttu-id="642dc-106">Puede filtrar los informes y crear grupos de dispositivos de Azure Active Directory dinámicos según las categorías de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="642dc-106">You can filter reports and create dynamic Azure Active Directory device groups based on device categories.</span></span>

## <a name="methods"></a><span data-ttu-id="642dc-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="642dc-107">Methods</span></span>
|<span data-ttu-id="642dc-108">Método</span><span class="sxs-lookup"><span data-stu-id="642dc-108">Method</span></span>|<span data-ttu-id="642dc-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="642dc-109">Return Type</span></span>|<span data-ttu-id="642dc-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="642dc-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="642dc-111">Colección de [lista deviceCategories](../api/intune_shared_devicecategory_list.md)</span><span class="sxs-lookup"><span data-stu-id="642dc-111">[List deviceCategories](../api/intune_shared_devicecategory_list.md) collection</span></span>|<span data-ttu-id="642dc-112">Enumere las propiedades y las relaciones de los objetos [deviceCategory](../resources/intune_shared_devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="642dc-112">List properties and relationships of the [deviceCategory](../resources/intune_shared_devicecategory.md) objects.</span></span>|
|[<span data-ttu-id="642dc-113">Obtener deviceCategory</span><span class="sxs-lookup"><span data-stu-id="642dc-113">Get deviceCategory</span></span>](../api/intune_shared_devicecategory_get.md)|<span data-ttu-id="642dc-114">Lea las propiedades y las relaciones del objeto [deviceCategory](../resources/intune_shared_devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="642dc-114">Read properties and relationships of the [deviceCategory](../resources/intune_shared_devicecategory.md) object.</span></span>|
|[<span data-ttu-id="642dc-115">Crear deviceCategory</span><span class="sxs-lookup"><span data-stu-id="642dc-115">Create deviceCategory</span></span>](../api/intune_shared_devicecategory_create.md)|<span data-ttu-id="642dc-116">Cree un objeto [deviceCategory](../resources/intune_shared_devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="642dc-116">Create a new [deviceCategory](../resources/intune_shared_devicecategory.md) object.</span></span>|
|<span data-ttu-id="642dc-117">[Eliminar deviceCategory](../api/intune_shared_devicecategory_delete.md).</span><span class="sxs-lookup"><span data-stu-id="642dc-117">[Delete deviceCategory](../api/intune_shared_devicecategory_delete.md).</span></span>|
|[<span data-ttu-id="642dc-118">Actualizar deviceCategory</span><span class="sxs-lookup"><span data-stu-id="642dc-118">Update deviceCategory</span></span>](../api/intune_shared_devicecategory_update.md)|<span data-ttu-id="642dc-119">Actualice las propiedades de un objeto [deviceCategory](../resources/intune_shared_devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="642dc-119">Update the properties of a [deviceCategory](../resources/intune_shared_devicecategory.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="642dc-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="642dc-120">Properties</span></span>
|<span data-ttu-id="642dc-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="642dc-121">Property</span></span>|<span data-ttu-id="642dc-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="642dc-122">Type</span></span>|<span data-ttu-id="642dc-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="642dc-123">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="642dc-124">id</span><span class="sxs-lookup"><span data-stu-id="642dc-124">id</span></span>|<span data-ttu-id="642dc-125">String</span><span class="sxs-lookup"><span data-stu-id="642dc-125">String</span></span>|<span data-ttu-id="642dc-126">El identificador único de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="642dc-126">Unique identifier for the device category.</span></span> <span data-ttu-id="642dc-127">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="642dc-127">Read-only.</span></span>|
|<span data-ttu-id="642dc-128">**Incorporación de redes**</span><span class="sxs-lookup"><span data-stu-id="642dc-128">**Onboarding**</span></span>|
|<span data-ttu-id="642dc-129">displayName</span><span class="sxs-lookup"><span data-stu-id="642dc-129">displayName</span></span>|<span data-ttu-id="642dc-130">String</span><span class="sxs-lookup"><span data-stu-id="642dc-130">String</span></span>|<span data-ttu-id="642dc-131">Nombre para mostrar de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="642dc-131">Display name for the device category.</span></span>|
|<span data-ttu-id="642dc-132">descripción</span><span class="sxs-lookup"><span data-stu-id="642dc-132">description</span></span>|<span data-ttu-id="642dc-133">String</span><span class="sxs-lookup"><span data-stu-id="642dc-133">String</span></span>|<span data-ttu-id="642dc-134">Descripción opcional de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="642dc-134">Optional description for the device category.</span></span>|

## <a name="relationships"></a><span data-ttu-id="642dc-135">Relaciones</span><span class="sxs-lookup"><span data-stu-id="642dc-135">Relationships</span></span>
<span data-ttu-id="642dc-136">Ninguna</span><span class="sxs-lookup"><span data-stu-id="642dc-136">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="642dc-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="642dc-137">JSON Representation</span></span>
<span data-ttu-id="642dc-138">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="642dc-138">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.deviceCategory"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceCategory",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String"
}
```



