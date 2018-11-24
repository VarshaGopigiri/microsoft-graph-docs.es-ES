# <a name="manageddevicemobileappconfigurationdevicesummary-resource-type"></a><span data-ttu-id="67590-101">Tipo de recurso managedDeviceMobileAppConfigurationDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="67590-101">managedDeviceMobileAppConfigurationDeviceSummary resource type</span></span>

> <span data-ttu-id="67590-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="67590-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="67590-103">Contiene las propiedades, las propiedades heredadas y las acciones para un resumen de estado de dispositivo de la configuración de aplicaciones móviles de MDM.</span><span class="sxs-lookup"><span data-stu-id="67590-103">Contains properties, inherited properties and actions for an MDM mobile app configuration device status summary.</span></span>
## <a name="methods"></a><span data-ttu-id="67590-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="67590-104">Methods</span></span>
|<span data-ttu-id="67590-105">Método</span><span class="sxs-lookup"><span data-stu-id="67590-105">Method</span></span>|<span data-ttu-id="67590-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67590-106">Return Type</span></span>|<span data-ttu-id="67590-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="67590-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="67590-108">Obtener managedDeviceMobileAppConfigurationDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="67590-108">Get managedDeviceMobileAppConfigurationDeviceSummary</span></span>](../api/intune_apps_manageddevicemobileappconfigurationdevicesummary_get.md)|[<span data-ttu-id="67590-109">managedDeviceMobileAppConfigurationDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="67590-109">managedDeviceMobileAppConfigurationDeviceSummary</span></span>](../resources/intune_apps_manageddevicemobileappconfigurationdevicesummary.md)|<span data-ttu-id="67590-110">Lea las propiedades y las relaciones del objeto [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune_apps_manageddevicemobileappconfigurationdevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="67590-110">Read properties and relationships of the [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune_apps_manageddevicemobileappconfigurationdevicesummary.md) object.</span></span>|
|[<span data-ttu-id="67590-111">Actualizar managedDeviceMobileAppConfigurationDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="67590-111">Update managedDeviceMobileAppConfigurationDeviceSummary</span></span>](../api/intune_apps_manageddevicemobileappconfigurationdevicesummary_update.md)|[<span data-ttu-id="67590-112">managedDeviceMobileAppConfigurationDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="67590-112">managedDeviceMobileAppConfigurationDeviceSummary</span></span>](../resources/intune_apps_manageddevicemobileappconfigurationdevicesummary.md)|<span data-ttu-id="67590-113">Actualice las propiedades y las relaciones de un objeto [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune_apps_manageddevicemobileappconfigurationdevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="67590-113">Update the properties of a [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune_apps_manageddevicemobileappconfigurationdevicesummary.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="67590-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="67590-114">Properties</span></span>
|<span data-ttu-id="67590-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="67590-115">Property</span></span>|<span data-ttu-id="67590-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="67590-116">Type</span></span>|<span data-ttu-id="67590-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="67590-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="67590-118">id</span><span class="sxs-lookup"><span data-stu-id="67590-118">id</span></span>|<span data-ttu-id="67590-119">cadena</span><span class="sxs-lookup"><span data-stu-id="67590-119">String</span></span>|<span data-ttu-id="67590-120">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="67590-120">Key of the entity.</span></span>|
|<span data-ttu-id="67590-121">pendingCount</span><span class="sxs-lookup"><span data-stu-id="67590-121">pendingCount</span></span>|<span data-ttu-id="67590-122">Int32</span><span class="sxs-lookup"><span data-stu-id="67590-122">Int32</span></span>|<span data-ttu-id="67590-123">Número de dispositivos pendientes</span><span class="sxs-lookup"><span data-stu-id="67590-123">Number of pending devices</span></span>|
|<span data-ttu-id="67590-124">notApplicableCount</span><span class="sxs-lookup"><span data-stu-id="67590-124">notApplicableCount</span></span>|<span data-ttu-id="67590-125">Int32</span><span class="sxs-lookup"><span data-stu-id="67590-125">Int32</span></span>|<span data-ttu-id="67590-126">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="67590-126">Number of not applicable devices</span></span>|
|<span data-ttu-id="67590-127">successCount</span><span class="sxs-lookup"><span data-stu-id="67590-127">successCount</span></span>|<span data-ttu-id="67590-128">Int32</span><span class="sxs-lookup"><span data-stu-id="67590-128">Int32</span></span>|<span data-ttu-id="67590-129">Número de dispositivos correctos</span><span class="sxs-lookup"><span data-stu-id="67590-129">Number of succeeded devices</span></span>|
|<span data-ttu-id="67590-130">errorCount</span><span class="sxs-lookup"><span data-stu-id="67590-130">errorCount</span></span>|<span data-ttu-id="67590-131">Int32</span><span class="sxs-lookup"><span data-stu-id="67590-131">Int32</span></span>|<span data-ttu-id="67590-132">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="67590-132">Number of error devices</span></span>|
|<span data-ttu-id="67590-133">failedCount</span><span class="sxs-lookup"><span data-stu-id="67590-133">failedCount</span></span>|<span data-ttu-id="67590-134">Int32</span><span class="sxs-lookup"><span data-stu-id="67590-134">Int32</span></span>|<span data-ttu-id="67590-135">Número de dispositivos erróneos</span><span class="sxs-lookup"><span data-stu-id="67590-135">Number of failed devices</span></span>|
|<span data-ttu-id="67590-136">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="67590-136">lastUpdateDateTime</span></span>|<span data-ttu-id="67590-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="67590-137">DateTimeOffset</span></span>|<span data-ttu-id="67590-138">Última hora de actualización</span><span class="sxs-lookup"><span data-stu-id="67590-138">Last update time</span></span>|
|<span data-ttu-id="67590-139">configurationVersion</span><span class="sxs-lookup"><span data-stu-id="67590-139">configurationVersion</span></span>|<span data-ttu-id="67590-140">Int32</span><span class="sxs-lookup"><span data-stu-id="67590-140">Int32</span></span>|<span data-ttu-id="67590-141">Versión de la directiva para esa información general</span><span class="sxs-lookup"><span data-stu-id="67590-141">Version of the policy for that overview</span></span>|

## <a name="relationships"></a><span data-ttu-id="67590-142">Relaciones</span><span class="sxs-lookup"><span data-stu-id="67590-142">Relationships</span></span>
<span data-ttu-id="67590-143">Ninguna</span><span class="sxs-lookup"><span data-stu-id="67590-143">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="67590-144">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="67590-144">JSON Representation</span></span>
<span data-ttu-id="67590-145">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="67590-145">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedDeviceMobileAppConfigurationDeviceSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationDeviceSummary",
  "id": "String (identifier)",
  "pendingCount": 1024,
  "notApplicableCount": 1024,
  "successCount": 1024,
  "errorCount": 1024,
  "failedCount": 1024,
  "lastUpdateDateTime": "String (timestamp)",
  "configurationVersion": 1024
}
```



