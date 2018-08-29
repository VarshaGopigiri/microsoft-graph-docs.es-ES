# <a name="devicecompliancepolicydevicestatesummary-resource-type"></a><span data-ttu-id="6acce-101">Tipo de recurso deviceCompliancePolicyDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="6acce-101">deviceCompliancePolicyDeviceStateSummary resource type</span></span>

> <span data-ttu-id="6acce-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6acce-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6acce-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="6acce-103">Not yet documented</span></span>
## <a name="methods"></a><span data-ttu-id="6acce-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="6acce-104">Methods</span></span>
|<span data-ttu-id="6acce-105">Método</span><span class="sxs-lookup"><span data-stu-id="6acce-105">Method</span></span>|<span data-ttu-id="6acce-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6acce-106">Return Type</span></span>|<span data-ttu-id="6acce-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="6acce-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="6acce-108">Obtener deviceCompliancePolicyDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="6acce-108">Get deviceCompliancePolicyDeviceStateSummary</span></span>](../api/intune_deviceconfig_devicecompliancepolicydevicestatesummary_get.md)|[<span data-ttu-id="6acce-109">deviceCompliancePolicyDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="6acce-109">deviceCompliancePolicyDeviceStateSummary</span></span>](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md)|<span data-ttu-id="6acce-110">Lea las propiedades y las relaciones del objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="6acce-110">Read properties and relationships of the [deviceCompliancePolicyDeviceStateSummary](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md) object.</span></span>|
|[<span data-ttu-id="6acce-111">Actualizar deviceCompliancePolicyDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="6acce-111">Update deviceCompliancePolicyDeviceStateSummary</span></span>](../api/intune_deviceconfig_devicecompliancepolicydevicestatesummary_update.md)|[<span data-ttu-id="6acce-112">deviceCompliancePolicyDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="6acce-112">deviceCompliancePolicyDeviceStateSummary</span></span>](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md)|<span data-ttu-id="6acce-113">Actualice las propiedades de un objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="6acce-113">Update the properties of a [deviceCompliancePolicyDeviceStateSummary](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="6acce-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6acce-114">Properties</span></span>
|<span data-ttu-id="6acce-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6acce-115">Property</span></span>|<span data-ttu-id="6acce-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="6acce-116">Type</span></span>|<span data-ttu-id="6acce-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="6acce-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6acce-118">inGracePeriodCount</span><span class="sxs-lookup"><span data-stu-id="6acce-118">inGracePeriodCount</span></span>|<span data-ttu-id="6acce-119">Int32</span><span class="sxs-lookup"><span data-stu-id="6acce-119">Int32</span></span>|<span data-ttu-id="6acce-120">Número de dispositivos que se encuentran en el período de gracia</span><span class="sxs-lookup"><span data-stu-id="6acce-120">Number of devices that are in grace period</span></span>|
|<span data-ttu-id="6acce-121">configManagerCount</span><span class="sxs-lookup"><span data-stu-id="6acce-121">configManagerCount</span></span>|<span data-ttu-id="6acce-122">Int32</span><span class="sxs-lookup"><span data-stu-id="6acce-122">Int32</span></span>|<span data-ttu-id="6acce-123">Número de dispositivos cuyo cumplimiento lo administra System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6acce-123">Number of devices that have compliance managed by System Center Configuration Manager</span></span>|
|<span data-ttu-id="6acce-124">id</span><span class="sxs-lookup"><span data-stu-id="6acce-124">id</span></span>|<span data-ttu-id="6acce-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="6acce-125">String</span></span>|<span data-ttu-id="6acce-126">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="6acce-126">Key of the entity.</span></span>|
|<span data-ttu-id="6acce-127">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6acce-127">unknownDeviceCount</span></span>|<span data-ttu-id="6acce-128">Int32</span><span class="sxs-lookup"><span data-stu-id="6acce-128">Int32</span></span>|<span data-ttu-id="6acce-129">Número de dispositivos desconocidos</span><span class="sxs-lookup"><span data-stu-id="6acce-129">Number of unknown devices</span></span>|
|<span data-ttu-id="6acce-130">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6acce-130">notApplicableDeviceCount</span></span>|<span data-ttu-id="6acce-131">Int32</span><span class="sxs-lookup"><span data-stu-id="6acce-131">Int32</span></span>|<span data-ttu-id="6acce-132">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="6acce-132">Number of not applicable devices</span></span>|
|<span data-ttu-id="6acce-133">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6acce-133">compliantDeviceCount</span></span>|<span data-ttu-id="6acce-134">Int32</span><span class="sxs-lookup"><span data-stu-id="6acce-134">Int32</span></span>|<span data-ttu-id="6acce-135">Número de dispositivos compatibles</span><span class="sxs-lookup"><span data-stu-id="6acce-135">Number of compliant devices</span></span>|
|<span data-ttu-id="6acce-136">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6acce-136">remediatedDeviceCount</span></span>|<span data-ttu-id="6acce-137">Int32</span><span class="sxs-lookup"><span data-stu-id="6acce-137">Int32</span></span>|<span data-ttu-id="6acce-138">Número de dispositivos corregidos</span><span class="sxs-lookup"><span data-stu-id="6acce-138">Number of remediated devices</span></span>|
|<span data-ttu-id="6acce-139">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6acce-139">nonCompliantDeviceCount</span></span>|<span data-ttu-id="6acce-140">Int32</span><span class="sxs-lookup"><span data-stu-id="6acce-140">Int32</span></span>|<span data-ttu-id="6acce-141">Número de dispositivos no compatibles</span><span class="sxs-lookup"><span data-stu-id="6acce-141">Number of NonCompliant devices</span></span>|
|<span data-ttu-id="6acce-142">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6acce-142">errorDeviceCount</span></span>|<span data-ttu-id="6acce-143">Int32</span><span class="sxs-lookup"><span data-stu-id="6acce-143">Int32</span></span>|<span data-ttu-id="6acce-144">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="6acce-144">Number of error devices</span></span>|
|<span data-ttu-id="6acce-145">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6acce-145">conflictDeviceCount</span></span>|<span data-ttu-id="6acce-146">Int32</span><span class="sxs-lookup"><span data-stu-id="6acce-146">Int32</span></span>|<span data-ttu-id="6acce-147">Número de dispositivos en conflicto</span><span class="sxs-lookup"><span data-stu-id="6acce-147">Number of conflict devices</span></span>|

## <a name="relationships"></a><span data-ttu-id="6acce-148">Relaciones</span><span class="sxs-lookup"><span data-stu-id="6acce-148">Relationships</span></span>
<span data-ttu-id="6acce-149">Ninguna</span><span class="sxs-lookup"><span data-stu-id="6acce-149">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="6acce-150">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6acce-150">JSON Representation</span></span>
<span data-ttu-id="6acce-151">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="6acce-151">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.deviceCompliancePolicyDeviceStateSummary"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicyDeviceStateSummary",
  "inGracePeriodCount": 1024,
  "configManagerCount": 1024,
  "id": "String (identifier)",
  "unknownDeviceCount": 1024,
  "notApplicableDeviceCount": 1024,
  "compliantDeviceCount": 1024,
  "remediatedDeviceCount": 1024,
  "nonCompliantDeviceCount": 1024,
  "errorDeviceCount": 1024,
  "conflictDeviceCount": 1024
}
```



