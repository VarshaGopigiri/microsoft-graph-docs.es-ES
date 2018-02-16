# <a name="devicecompliancepolicydevicestatesummary-resource-type"></a><span data-ttu-id="40dda-101">Tipo de recurso deviceCompliancePolicyDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="40dda-101">deviceCompliancePolicyDeviceStateSummary resource type</span></span>

> <span data-ttu-id="40dda-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="40dda-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="40dda-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="40dda-103">Not yet documented</span></span>
## <a name="methods"></a><span data-ttu-id="40dda-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="40dda-104">Methods</span></span>
|<span data-ttu-id="40dda-105">Método</span><span class="sxs-lookup"><span data-stu-id="40dda-105">Method</span></span>|<span data-ttu-id="40dda-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="40dda-106">Return Type</span></span>|<span data-ttu-id="40dda-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="40dda-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="40dda-108">Obtener deviceCompliancePolicyDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="40dda-108">Get deviceCompliancePolicyDeviceStateSummary</span></span>](../api/intune_deviceconfig_devicecompliancepolicydevicestatesummary_get.md)|[<span data-ttu-id="40dda-109">deviceCompliancePolicyDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="40dda-109">deviceCompliancePolicyDeviceStateSummary</span></span>](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md)|<span data-ttu-id="40dda-110">Lea las propiedades y las relaciones del objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="40dda-110">Read properties and relationships of [plannerTaskDetails](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md) object.</span></span>|
|[<span data-ttu-id="40dda-111">Actualizar deviceCompliancePolicyDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="40dda-111">Update deviceCompliancePolicyDeviceStateSummary</span></span>](../api/intune_deviceconfig_devicecompliancepolicydevicestatesummary_update.md)|[<span data-ttu-id="40dda-112">deviceCompliancePolicyDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="40dda-112">deviceCompliancePolicyDeviceStateSummary</span></span>](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md)|<span data-ttu-id="40dda-113">Actualice las propiedades de un objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="40dda-113">Update the properties of a [calendar](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="40dda-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="40dda-114">Properties</span></span>
|<span data-ttu-id="40dda-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="40dda-115">Property</span></span>|<span data-ttu-id="40dda-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="40dda-116">Type</span></span>|<span data-ttu-id="40dda-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="40dda-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="40dda-118">inGracePeriodCount</span><span class="sxs-lookup"><span data-stu-id="40dda-118">inGracePeriodCount</span></span>|<span data-ttu-id="40dda-119">Int32</span><span class="sxs-lookup"><span data-stu-id="40dda-119">Int32</span></span>|<span data-ttu-id="40dda-120">Número de dispositivos que se encuentran en el período de gracia</span><span class="sxs-lookup"><span data-stu-id="40dda-120">Number of devices that are in grace period</span></span>|
|<span data-ttu-id="40dda-121">configManagerCount</span><span class="sxs-lookup"><span data-stu-id="40dda-121">configManagerCount</span></span>|<span data-ttu-id="40dda-122">Int32</span><span class="sxs-lookup"><span data-stu-id="40dda-122">Int32</span></span>|<span data-ttu-id="40dda-123">Número de dispositivos cuyo cumplimiento lo administra System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="40dda-123">Number of devices that have compliance managed by System Center Configuration Manager</span></span>|
|<span data-ttu-id="40dda-124">id</span><span class="sxs-lookup"><span data-stu-id="40dda-124">id</span></span>|<span data-ttu-id="40dda-125">cadena</span><span class="sxs-lookup"><span data-stu-id="40dda-125">String</span></span>|<span data-ttu-id="40dda-126">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="40dda-126">Key of the setting.</span></span>|
|<span data-ttu-id="40dda-127">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="40dda-127">unknownDeviceCount</span></span>|<span data-ttu-id="40dda-128">Int32</span><span class="sxs-lookup"><span data-stu-id="40dda-128">Int32</span></span>|<span data-ttu-id="40dda-129">Número de dispositivos desconocidos</span><span class="sxs-lookup"><span data-stu-id="40dda-129">Number of unknown devices</span></span>|
|<span data-ttu-id="40dda-130">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="40dda-130">notApplicableDeviceCount</span></span>|<span data-ttu-id="40dda-131">Int32</span><span class="sxs-lookup"><span data-stu-id="40dda-131">Int32</span></span>|<span data-ttu-id="40dda-132">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="40dda-132">Number of not applicable devices</span></span>|
|<span data-ttu-id="40dda-133">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="40dda-133">compliantDeviceCount</span></span>|<span data-ttu-id="40dda-134">Int32</span><span class="sxs-lookup"><span data-stu-id="40dda-134">Int32</span></span>|<span data-ttu-id="40dda-135">Número de dispositivos compatibles</span><span class="sxs-lookup"><span data-stu-id="40dda-135">Number of compliant devices</span></span>|
|<span data-ttu-id="40dda-136">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="40dda-136">remediatedDeviceCount</span></span>|<span data-ttu-id="40dda-137">Int32</span><span class="sxs-lookup"><span data-stu-id="40dda-137">Int32</span></span>|<span data-ttu-id="40dda-138">Número de dispositivos corregidos</span><span class="sxs-lookup"><span data-stu-id="40dda-138">Number of remediated devices</span></span>|
|<span data-ttu-id="40dda-139">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="40dda-139">nonCompliantDeviceCount</span></span>|<span data-ttu-id="40dda-140">Int32</span><span class="sxs-lookup"><span data-stu-id="40dda-140">Int32</span></span>|<span data-ttu-id="40dda-141">Número de dispositivos no compatibles</span><span class="sxs-lookup"><span data-stu-id="40dda-141">Number of NonCompliant devices</span></span>|
|<span data-ttu-id="40dda-142">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="40dda-142">errorDeviceCount</span></span>|<span data-ttu-id="40dda-143">Int32</span><span class="sxs-lookup"><span data-stu-id="40dda-143">Int32</span></span>|<span data-ttu-id="40dda-144">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="40dda-144">Number of error devices</span></span>|
|<span data-ttu-id="40dda-145">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="40dda-145">conflictDeviceCount</span></span>|<span data-ttu-id="40dda-146">Int32</span><span class="sxs-lookup"><span data-stu-id="40dda-146">Int32</span></span>|<span data-ttu-id="40dda-147">Número de dispositivos en conflicto</span><span class="sxs-lookup"><span data-stu-id="40dda-147">Number of conflict devices</span></span>|

## <a name="relationships"></a><span data-ttu-id="40dda-148">Relaciones</span><span class="sxs-lookup"><span data-stu-id="40dda-148">Relationships</span></span>
<span data-ttu-id="40dda-149">Ninguna</span><span class="sxs-lookup"><span data-stu-id="40dda-149">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="40dda-150">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="40dda-150">JSON Representation</span></span>
<span data-ttu-id="40dda-151">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="40dda-151">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceCompliancePolicyDeviceStateSummary"
}
-->
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



