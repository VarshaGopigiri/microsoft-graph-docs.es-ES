# <a name="deviceconfigurationdevicestatesummary-resource-type"></a><span data-ttu-id="bda7d-101">Tipo de recurso deviceConfigurationDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="bda7d-101">deviceConfigurationDeviceStateSummary resource type</span></span>

> <span data-ttu-id="bda7d-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bda7d-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bda7d-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="bda7d-103">Not yet documented</span></span>
## <a name="methods"></a><span data-ttu-id="bda7d-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="bda7d-104">Methods</span></span>
|<span data-ttu-id="bda7d-105">Método</span><span class="sxs-lookup"><span data-stu-id="bda7d-105">Method</span></span>|<span data-ttu-id="bda7d-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bda7d-106">Return Type</span></span>|<span data-ttu-id="bda7d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="bda7d-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="bda7d-108">Obtener deviceConfigurationDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="bda7d-108">Get deviceConfigurationDeviceStateSummary</span></span>](../api/intune_deviceconfig_deviceconfigurationdevicestatesummary_get.md)|[<span data-ttu-id="bda7d-109">deviceConfigurationDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="bda7d-109">deviceConfigurationDeviceStateSummary</span></span>](../resources/intune_deviceconfig_deviceconfigurationdevicestatesummary.md)|<span data-ttu-id="bda7d-110">Lea las propiedades y las relaciones del objeto [deviceConfigurationDeviceStateSummary](../resources/intune_deviceconfig_deviceconfigurationdevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="bda7d-110">Read properties and relationships of [plannerTaskDetails](../resources/intune_deviceconfig_deviceconfigurationdevicestatesummary.md) object.</span></span>|
|[<span data-ttu-id="bda7d-111">Actualizar deviceConfigurationDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="bda7d-111">Update deviceConfigurationDeviceStateSummary</span></span>](../api/intune_deviceconfig_deviceconfigurationdevicestatesummary_update.md)|[<span data-ttu-id="bda7d-112">deviceConfigurationDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="bda7d-112">deviceConfigurationDeviceStateSummary</span></span>](../resources/intune_deviceconfig_deviceconfigurationdevicestatesummary.md)|<span data-ttu-id="bda7d-113">Actualice las propiedades de un objeto [deviceConfigurationDeviceStateSummary](../resources/intune_deviceconfig_deviceconfigurationdevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="bda7d-113">Update the properties of a [calendar](../resources/intune_deviceconfig_deviceconfigurationdevicestatesummary.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="bda7d-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bda7d-114">Properties</span></span>
|<span data-ttu-id="bda7d-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bda7d-115">Property</span></span>|<span data-ttu-id="bda7d-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="bda7d-116">Type</span></span>|<span data-ttu-id="bda7d-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="bda7d-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bda7d-118">id</span><span class="sxs-lookup"><span data-stu-id="bda7d-118">id</span></span>|<span data-ttu-id="bda7d-119">cadena</span><span class="sxs-lookup"><span data-stu-id="bda7d-119">String</span></span>|<span data-ttu-id="bda7d-120">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="bda7d-120">Key of the setting.</span></span>|
|<span data-ttu-id="bda7d-121">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="bda7d-121">unknownDeviceCount</span></span>|<span data-ttu-id="bda7d-122">Int32</span><span class="sxs-lookup"><span data-stu-id="bda7d-122">Int32</span></span>|<span data-ttu-id="bda7d-123">Número de dispositivos desconocidos</span><span class="sxs-lookup"><span data-stu-id="bda7d-123">Number of unknown devices</span></span>|
|<span data-ttu-id="bda7d-124">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="bda7d-124">notApplicableDeviceCount</span></span>|<span data-ttu-id="bda7d-125">Int32</span><span class="sxs-lookup"><span data-stu-id="bda7d-125">Int32</span></span>|<span data-ttu-id="bda7d-126">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="bda7d-126">Number of not applicable devices</span></span>|
|<span data-ttu-id="bda7d-127">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="bda7d-127">compliantDeviceCount</span></span>|<span data-ttu-id="bda7d-128">Int32</span><span class="sxs-lookup"><span data-stu-id="bda7d-128">Int32</span></span>|<span data-ttu-id="bda7d-129">Número de dispositivos compatibles</span><span class="sxs-lookup"><span data-stu-id="bda7d-129">Number of compliant devices</span></span>|
|<span data-ttu-id="bda7d-130">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="bda7d-130">remediatedDeviceCount</span></span>|<span data-ttu-id="bda7d-131">Int32</span><span class="sxs-lookup"><span data-stu-id="bda7d-131">Int32</span></span>|<span data-ttu-id="bda7d-132">Número de dispositivos corregidos</span><span class="sxs-lookup"><span data-stu-id="bda7d-132">Number of remediated devices</span></span>|
|<span data-ttu-id="bda7d-133">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="bda7d-133">nonCompliantDeviceCount</span></span>|<span data-ttu-id="bda7d-134">Int32</span><span class="sxs-lookup"><span data-stu-id="bda7d-134">Int32</span></span>|<span data-ttu-id="bda7d-135">Número de dispositivos no compatibles</span><span class="sxs-lookup"><span data-stu-id="bda7d-135">Number of NonCompliant devices</span></span>|
|<span data-ttu-id="bda7d-136">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="bda7d-136">errorDeviceCount</span></span>|<span data-ttu-id="bda7d-137">Int32</span><span class="sxs-lookup"><span data-stu-id="bda7d-137">Int32</span></span>|<span data-ttu-id="bda7d-138">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="bda7d-138">Number of error devices</span></span>|
|<span data-ttu-id="bda7d-139">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="bda7d-139">conflictDeviceCount</span></span>|<span data-ttu-id="bda7d-140">Int32</span><span class="sxs-lookup"><span data-stu-id="bda7d-140">Int32</span></span>|<span data-ttu-id="bda7d-141">Número de dispositivos en conflicto</span><span class="sxs-lookup"><span data-stu-id="bda7d-141">Number of conflict devices</span></span>|

## <a name="relationships"></a><span data-ttu-id="bda7d-142">Relaciones</span><span class="sxs-lookup"><span data-stu-id="bda7d-142">Relationships</span></span>
<span data-ttu-id="bda7d-143">Ninguna</span><span class="sxs-lookup"><span data-stu-id="bda7d-143">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="bda7d-144">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bda7d-144">JSON Representation</span></span>
<span data-ttu-id="bda7d-145">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="bda7d-145">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceConfigurationDeviceStateSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceConfigurationDeviceStateSummary",
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



