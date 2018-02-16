# <a name="deviceappmanagement-resource-type"></a><span data-ttu-id="a2cc1-101">Tipo de recurso deviceAppManagement</span><span class="sxs-lookup"><span data-stu-id="a2cc1-101">deviceAppManagement resource type</span></span>

> <span data-ttu-id="a2cc1-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a2cc1-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a2cc1-103">Entidad singleton que actúa como un contenedor para todas las funcionalidades de administración de aplicaciones de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a2cc1-103">Singleton entity that acts as a container for all device app management functionality.</span></span>
## <a name="methods"></a><span data-ttu-id="a2cc1-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="a2cc1-104">Methods</span></span>
|<span data-ttu-id="a2cc1-105">Método</span><span class="sxs-lookup"><span data-stu-id="a2cc1-105">Method</span></span>|<span data-ttu-id="a2cc1-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2cc1-106">Return Type</span></span>|<span data-ttu-id="a2cc1-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2cc1-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="a2cc1-108">Obtener deviceAppManagement</span><span class="sxs-lookup"><span data-stu-id="a2cc1-108">Get deviceAppManagement</span></span>](../api/intune_apps_deviceappmanagement_get.md)|[<span data-ttu-id="a2cc1-109">deviceAppManagement</span><span class="sxs-lookup"><span data-stu-id="a2cc1-109">deviceAppManagement</span></span>](../resources/intune_apps_deviceappmanagement.md)|<span data-ttu-id="a2cc1-110">Lea las propiedades y las relaciones del objeto [deviceAppManagement](../resources/intune_apps_deviceappmanagement.md).</span><span class="sxs-lookup"><span data-stu-id="a2cc1-110">Read properties and relationships of [plannerTaskDetails](../resources/intune_apps_deviceappmanagement.md) object.</span></span>|
|[<span data-ttu-id="a2cc1-111">Actualizar deviceAppManagement</span><span class="sxs-lookup"><span data-stu-id="a2cc1-111">Update deviceAppManagement</span></span>](../api/intune_apps_deviceappmanagement_update.md)|[<span data-ttu-id="a2cc1-112">deviceAppManagement</span><span class="sxs-lookup"><span data-stu-id="a2cc1-112">deviceAppManagement</span></span>](../resources/intune_apps_deviceappmanagement.md)|<span data-ttu-id="a2cc1-113">Actualice las propiedades de un objeto [deviceAppManagement](../resources/intune_apps_deviceappmanagement.md).</span><span class="sxs-lookup"><span data-stu-id="a2cc1-113">Update the properties of a [calendar](../resources/intune_apps_deviceappmanagement.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="a2cc1-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a2cc1-114">Properties</span></span>
|<span data-ttu-id="a2cc1-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a2cc1-115">Property</span></span>|<span data-ttu-id="a2cc1-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="a2cc1-116">Type</span></span>|<span data-ttu-id="a2cc1-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2cc1-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a2cc1-118">id</span><span class="sxs-lookup"><span data-stu-id="a2cc1-118">id</span></span>|<span data-ttu-id="a2cc1-119">cadena</span><span class="sxs-lookup"><span data-stu-id="a2cc1-119">String</span></span>|<span data-ttu-id="a2cc1-120">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a2cc1-120">Key of the setting.</span></span>|

## <a name="relationships"></a><span data-ttu-id="a2cc1-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a2cc1-121">Relationships</span></span>
|<span data-ttu-id="a2cc1-122">Relación</span><span class="sxs-lookup"><span data-stu-id="a2cc1-122">Relationship</span></span>|<span data-ttu-id="a2cc1-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="a2cc1-123">Type</span></span>|<span data-ttu-id="a2cc1-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2cc1-124">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a2cc1-125">mobileApps</span><span class="sxs-lookup"><span data-stu-id="a2cc1-125">mobileApps</span></span>|<span data-ttu-id="a2cc1-126">Colección [mobileApp](../resources/intune_apps_mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="a2cc1-126">[mobileApp](../resources/intune_apps_mobileapp.md) collection</span></span>|<span data-ttu-id="a2cc1-127">Las aplicaciones móviles.</span><span class="sxs-lookup"><span data-stu-id="a2cc1-127">The mobile apps.</span></span>|
|<span data-ttu-id="a2cc1-128">mobileAppCategories</span><span class="sxs-lookup"><span data-stu-id="a2cc1-128">mobileAppCategories</span></span>|<span data-ttu-id="a2cc1-129">Colección [mobileAppCategory](../resources/intune_apps_mobileappcategory.md)</span><span class="sxs-lookup"><span data-stu-id="a2cc1-129">[mobileAppCategory](../resources/intune_apps_mobileappcategory.md) collection</span></span>|<span data-ttu-id="a2cc1-130">Las categorías de las aplicaciones para móviles.</span><span class="sxs-lookup"><span data-stu-id="a2cc1-130">The mobile app categories.</span></span>|
|<span data-ttu-id="a2cc1-131">mobileAppConfigurations</span><span class="sxs-lookup"><span data-stu-id="a2cc1-131">mobileAppConfigurations</span></span>|<span data-ttu-id="a2cc1-132">Colección [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a2cc1-132">[managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md) collection</span></span>|<span data-ttu-id="a2cc1-133">La configuración de aplicaciones móviles para dispositivo administrado.</span><span class="sxs-lookup"><span data-stu-id="a2cc1-133">The Managed Device Mobile Application Configurations.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="a2cc1-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a2cc1-134">JSON Representation</span></span>
<span data-ttu-id="a2cc1-135">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a2cc1-135">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceAppManagement"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceAppManagement",
  "id": "String (identifier)"
}
```



