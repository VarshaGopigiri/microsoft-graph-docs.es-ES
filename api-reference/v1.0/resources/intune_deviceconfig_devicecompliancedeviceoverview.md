# <a name="devicecompliancedeviceoverview-resource-type"></a><span data-ttu-id="23acc-101">Tipo de recurso deviceComplianceDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="23acc-101">deviceComplianceDeviceOverview resource type</span></span>

> <span data-ttu-id="23acc-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="23acc-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="23acc-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="23acc-103">Not yet documented</span></span>
## <a name="methods"></a><span data-ttu-id="23acc-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="23acc-104">Methods</span></span>
|<span data-ttu-id="23acc-105">Método</span><span class="sxs-lookup"><span data-stu-id="23acc-105">Method</span></span>|<span data-ttu-id="23acc-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23acc-106">Return Type</span></span>|<span data-ttu-id="23acc-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="23acc-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="23acc-108">Obtener deviceComplianceDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="23acc-108">Get deviceComplianceDeviceOverview</span></span>](../api/intune_deviceconfig_devicecompliancedeviceoverview_get.md)|[<span data-ttu-id="23acc-109">deviceComplianceDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="23acc-109">deviceComplianceDeviceOverview</span></span>](../resources/intune_deviceconfig_devicecompliancedeviceoverview.md)|<span data-ttu-id="23acc-110">Lea las propiedades y las relaciones del objeto [deviceComplianceDeviceOverview](../resources/intune_deviceconfig_devicecompliancedeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="23acc-110">Read properties and relationships of the [deviceComplianceDeviceOverview](../resources/intune_deviceconfig_devicecompliancedeviceoverview.md) object.</span></span>|
|[<span data-ttu-id="23acc-111">Actualizar deviceComplianceDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="23acc-111">Update deviceComplianceDeviceOverview</span></span>](../api/intune_deviceconfig_devicecompliancedeviceoverview_update.md)|[<span data-ttu-id="23acc-112">deviceComplianceDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="23acc-112">deviceComplianceDeviceOverview</span></span>](../resources/intune_deviceconfig_devicecompliancedeviceoverview.md)|<span data-ttu-id="23acc-113">Actualice las propiedades de un objeto [deviceComplianceDeviceOverview](../resources/intune_deviceconfig_devicecompliancedeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="23acc-113">Update the properties of a [deviceComplianceDeviceOverview](../resources/intune_deviceconfig_devicecompliancedeviceoverview.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="23acc-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="23acc-114">Properties</span></span>
|<span data-ttu-id="23acc-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="23acc-115">Property</span></span>|<span data-ttu-id="23acc-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="23acc-116">Type</span></span>|<span data-ttu-id="23acc-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="23acc-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="23acc-118">id</span><span class="sxs-lookup"><span data-stu-id="23acc-118">id</span></span>|<span data-ttu-id="23acc-119">cadena</span><span class="sxs-lookup"><span data-stu-id="23acc-119">String</span></span>|<span data-ttu-id="23acc-120">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="23acc-120">Key of the entity.</span></span>|
|<span data-ttu-id="23acc-121">pendingCount</span><span class="sxs-lookup"><span data-stu-id="23acc-121">pendingCount</span></span>|<span data-ttu-id="23acc-122">Int32</span><span class="sxs-lookup"><span data-stu-id="23acc-122">Int32</span></span>|<span data-ttu-id="23acc-123">Número de dispositivos pendientes</span><span class="sxs-lookup"><span data-stu-id="23acc-123">Number of pending devices</span></span>|
|<span data-ttu-id="23acc-124">notApplicableCount</span><span class="sxs-lookup"><span data-stu-id="23acc-124">notApplicableCount</span></span>|<span data-ttu-id="23acc-125">Int32</span><span class="sxs-lookup"><span data-stu-id="23acc-125">Int32</span></span>|<span data-ttu-id="23acc-126">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="23acc-126">Number of not applicable devices</span></span>|
|<span data-ttu-id="23acc-127">successCount</span><span class="sxs-lookup"><span data-stu-id="23acc-127">successCount</span></span>|<span data-ttu-id="23acc-128">Int32</span><span class="sxs-lookup"><span data-stu-id="23acc-128">Int32</span></span>|<span data-ttu-id="23acc-129">Número de dispositivos correctos</span><span class="sxs-lookup"><span data-stu-id="23acc-129">Number of succeeded devices</span></span>|
|<span data-ttu-id="23acc-130">errorCount</span><span class="sxs-lookup"><span data-stu-id="23acc-130">errorCount</span></span>|<span data-ttu-id="23acc-131">Int32</span><span class="sxs-lookup"><span data-stu-id="23acc-131">Int32</span></span>|<span data-ttu-id="23acc-132">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="23acc-132">Number of error devices</span></span>|
|<span data-ttu-id="23acc-133">failedCount</span><span class="sxs-lookup"><span data-stu-id="23acc-133">failedCount</span></span>|<span data-ttu-id="23acc-134">Int32</span><span class="sxs-lookup"><span data-stu-id="23acc-134">Int32</span></span>|<span data-ttu-id="23acc-135">Número de dispositivos erróneos</span><span class="sxs-lookup"><span data-stu-id="23acc-135">Number of failed devices</span></span>|
|<span data-ttu-id="23acc-136">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="23acc-136">lastUpdateDateTime</span></span>|<span data-ttu-id="23acc-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="23acc-137">DateTimeOffset</span></span>|<span data-ttu-id="23acc-138">Última hora de actualización</span><span class="sxs-lookup"><span data-stu-id="23acc-138">Last update time</span></span>|
|<span data-ttu-id="23acc-139">configurationVersion</span><span class="sxs-lookup"><span data-stu-id="23acc-139">configurationVersion</span></span>|<span data-ttu-id="23acc-140">Int32</span><span class="sxs-lookup"><span data-stu-id="23acc-140">Int32</span></span>|<span data-ttu-id="23acc-141">Versión de la directiva para esa información general</span><span class="sxs-lookup"><span data-stu-id="23acc-141">Version of the policy for that overview</span></span>|

## <a name="relationships"></a><span data-ttu-id="23acc-142">Relaciones</span><span class="sxs-lookup"><span data-stu-id="23acc-142">Relationships</span></span>
<span data-ttu-id="23acc-143">Ninguna</span><span class="sxs-lookup"><span data-stu-id="23acc-143">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="23acc-144">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="23acc-144">JSON Representation</span></span>
<span data-ttu-id="23acc-145">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="23acc-145">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceComplianceDeviceOverview"
}
-->
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



