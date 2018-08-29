# <a name="devicecompliancedeviceoverview-resource-type"></a><span data-ttu-id="18a5d-101">Tipo de recurso deviceComplianceDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="18a5d-101">deviceComplianceDeviceOverview resource type</span></span>

> <span data-ttu-id="18a5d-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="18a5d-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="18a5d-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="18a5d-103">Not yet documented</span></span>
## <a name="methods"></a><span data-ttu-id="18a5d-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="18a5d-104">Methods</span></span>
|<span data-ttu-id="18a5d-105">Método</span><span class="sxs-lookup"><span data-stu-id="18a5d-105">Method</span></span>|<span data-ttu-id="18a5d-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="18a5d-106">Return Type</span></span>|<span data-ttu-id="18a5d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="18a5d-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="18a5d-108">Obtener deviceComplianceDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="18a5d-108">Get deviceComplianceDeviceOverview</span></span>](../api/intune_deviceconfig_devicecompliancedeviceoverview_get.md)|[<span data-ttu-id="18a5d-109">deviceComplianceDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="18a5d-109">deviceComplianceDeviceOverview</span></span>](../resources/intune_deviceconfig_devicecompliancedeviceoverview.md)|<span data-ttu-id="18a5d-110">Lea las propiedades y las relaciones del objeto [deviceComplianceDeviceOverview](../resources/intune_deviceconfig_devicecompliancedeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="18a5d-110">Read properties and relationships of the [deviceComplianceDeviceOverview](../resources/intune_deviceconfig_devicecompliancedeviceoverview.md) object.</span></span>|
|[<span data-ttu-id="18a5d-111">Actualizar deviceComplianceDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="18a5d-111">Update deviceComplianceDeviceOverview</span></span>](../api/intune_deviceconfig_devicecompliancedeviceoverview_update.md)|[<span data-ttu-id="18a5d-112">deviceComplianceDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="18a5d-112">deviceComplianceDeviceOverview</span></span>](../resources/intune_deviceconfig_devicecompliancedeviceoverview.md)|<span data-ttu-id="18a5d-113">Actualice las propiedades de un objeto [deviceComplianceDeviceOverview](../resources/intune_deviceconfig_devicecompliancedeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="18a5d-113">Update the properties of a [deviceComplianceDeviceOverview](../resources/intune_deviceconfig_devicecompliancedeviceoverview.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="18a5d-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="18a5d-114">Properties</span></span>
|<span data-ttu-id="18a5d-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="18a5d-115">Property</span></span>|<span data-ttu-id="18a5d-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="18a5d-116">Type</span></span>|<span data-ttu-id="18a5d-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="18a5d-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="18a5d-118">id</span><span class="sxs-lookup"><span data-stu-id="18a5d-118">id</span></span>|<span data-ttu-id="18a5d-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="18a5d-119">String</span></span>|<span data-ttu-id="18a5d-120">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="18a5d-120">Key of the entity.</span></span>|
|<span data-ttu-id="18a5d-121">pendingCount</span><span class="sxs-lookup"><span data-stu-id="18a5d-121">pendingCount</span></span>|<span data-ttu-id="18a5d-122">Int32</span><span class="sxs-lookup"><span data-stu-id="18a5d-122">Int32</span></span>|<span data-ttu-id="18a5d-123">Número de dispositivos pendientes</span><span class="sxs-lookup"><span data-stu-id="18a5d-123">Number of pending devices</span></span>|
|<span data-ttu-id="18a5d-124">notApplicableCount</span><span class="sxs-lookup"><span data-stu-id="18a5d-124">notApplicableCount</span></span>|<span data-ttu-id="18a5d-125">Int32</span><span class="sxs-lookup"><span data-stu-id="18a5d-125">Int32</span></span>|<span data-ttu-id="18a5d-126">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="18a5d-126">Number of not applicable devices</span></span>|
|<span data-ttu-id="18a5d-127">successCount</span><span class="sxs-lookup"><span data-stu-id="18a5d-127">successCount</span></span>|<span data-ttu-id="18a5d-128">Int32</span><span class="sxs-lookup"><span data-stu-id="18a5d-128">Int32</span></span>|<span data-ttu-id="18a5d-129">Número de dispositivos correctos</span><span class="sxs-lookup"><span data-stu-id="18a5d-129">Number of succeeded devices</span></span>|
|<span data-ttu-id="18a5d-130">errorCount</span><span class="sxs-lookup"><span data-stu-id="18a5d-130">errorCount</span></span>|<span data-ttu-id="18a5d-131">Int32</span><span class="sxs-lookup"><span data-stu-id="18a5d-131">Int32</span></span>|<span data-ttu-id="18a5d-132">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="18a5d-132">Number of error devices</span></span>|
|<span data-ttu-id="18a5d-133">failedCount</span><span class="sxs-lookup"><span data-stu-id="18a5d-133">failedCount</span></span>|<span data-ttu-id="18a5d-134">Int32</span><span class="sxs-lookup"><span data-stu-id="18a5d-134">Int32</span></span>|<span data-ttu-id="18a5d-135">Número de dispositivos erróneos</span><span class="sxs-lookup"><span data-stu-id="18a5d-135">Number of failed devices</span></span>|
|<span data-ttu-id="18a5d-136">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="18a5d-136">lastUpdateDateTime</span></span>|<span data-ttu-id="18a5d-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="18a5d-137">DateTimeOffset</span></span>|<span data-ttu-id="18a5d-138">Última hora de actualización</span><span class="sxs-lookup"><span data-stu-id="18a5d-138">Last update time</span></span>|
|<span data-ttu-id="18a5d-139">configurationVersion</span><span class="sxs-lookup"><span data-stu-id="18a5d-139">configurationVersion</span></span>|<span data-ttu-id="18a5d-140">Int32</span><span class="sxs-lookup"><span data-stu-id="18a5d-140">Int32</span></span>|<span data-ttu-id="18a5d-141">Versión de la directiva para esa información general</span><span class="sxs-lookup"><span data-stu-id="18a5d-141">Version of the policy for that overview</span></span>|

## <a name="relationships"></a><span data-ttu-id="18a5d-142">Relaciones</span><span class="sxs-lookup"><span data-stu-id="18a5d-142">Relationships</span></span>
<span data-ttu-id="18a5d-143">Ninguna</span><span class="sxs-lookup"><span data-stu-id="18a5d-143">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="18a5d-144">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="18a5d-144">JSON Representation</span></span>
<span data-ttu-id="18a5d-145">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="18a5d-145">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.deviceComplianceDeviceOverview"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceComplianceDeviceOverview",
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



