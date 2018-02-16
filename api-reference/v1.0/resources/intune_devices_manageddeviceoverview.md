# <a name="manageddeviceoverview-resource-type"></a><span data-ttu-id="80edb-101">Tipo de recurso managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="80edb-101">managedDeviceOverview resource type</span></span>

> <span data-ttu-id="80edb-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="80edb-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="80edb-103">Datos de resumen de los dispositivos administrados</span><span class="sxs-lookup"><span data-stu-id="80edb-103">Summary data for managed devices</span></span>
## <a name="methods"></a><span data-ttu-id="80edb-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="80edb-104">Methods</span></span>
|<span data-ttu-id="80edb-105">Método</span><span class="sxs-lookup"><span data-stu-id="80edb-105">Method</span></span>|<span data-ttu-id="80edb-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80edb-106">Return Type</span></span>|<span data-ttu-id="80edb-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="80edb-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="80edb-108">Obtener managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="80edb-108">Get managedDeviceOverview</span></span>](../api/intune_devices_manageddeviceoverview_get.md)|[<span data-ttu-id="80edb-109">managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="80edb-109">managedDeviceOverview</span></span>](../resources/intune_devices_manageddeviceoverview.md)|<span data-ttu-id="80edb-110">Lea las propiedades y las relaciones del objeto [managedDeviceOverview](../resources/intune_devices_manageddeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="80edb-110">Read properties and relationships of [plannerTaskDetails](../resources/intune_devices_manageddeviceoverview.md) object.</span></span>|
|[<span data-ttu-id="80edb-111">Actualizar managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="80edb-111">Update managedDeviceOverview</span></span>](../api/intune_devices_manageddeviceoverview_update.md)|[<span data-ttu-id="80edb-112">managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="80edb-112">managedDeviceOverview</span></span>](../resources/intune_devices_manageddeviceoverview.md)|<span data-ttu-id="80edb-113">Actualice las propiedades de un objeto [managedDeviceOverview](../resources/intune_devices_manageddeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="80edb-113">Update the properties of a [calendar](../resources/intune_devices_manageddeviceoverview.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="80edb-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="80edb-114">Properties</span></span>
|<span data-ttu-id="80edb-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="80edb-115">Property</span></span>|<span data-ttu-id="80edb-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="80edb-116">Type</span></span>|<span data-ttu-id="80edb-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="80edb-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="80edb-118">id</span><span class="sxs-lookup"><span data-stu-id="80edb-118">id</span></span>|<span data-ttu-id="80edb-119">cadena</span><span class="sxs-lookup"><span data-stu-id="80edb-119">String</span></span>|<span data-ttu-id="80edb-120">Identificador único del resumen</span><span class="sxs-lookup"><span data-stu-id="80edb-120">Unique Identifier for the summary</span></span>|
|<span data-ttu-id="80edb-121">enrolledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="80edb-121">enrolledDeviceCount</span></span>|<span data-ttu-id="80edb-122">Int32</span><span class="sxs-lookup"><span data-stu-id="80edb-122">Int32</span></span>|<span data-ttu-id="80edb-123">Número total de dispositivos inscritos.</span><span class="sxs-lookup"><span data-stu-id="80edb-123">Total enrolled device count.</span></span> <span data-ttu-id="80edb-124">No incluye equipos administrados mediante el agente de PC de Intune</span><span class="sxs-lookup"><span data-stu-id="80edb-124">Does not include PC devices managed via Intune PC Agent</span></span>|
|<span data-ttu-id="80edb-125">mdmEnrolledCount</span><span class="sxs-lookup"><span data-stu-id="80edb-125">mdmEnrolledCount</span></span>|<span data-ttu-id="80edb-126">Int32</span><span class="sxs-lookup"><span data-stu-id="80edb-126">Int32</span></span>|<span data-ttu-id="80edb-127">El número de dispositivos inscritos en MDM</span><span class="sxs-lookup"><span data-stu-id="80edb-127">The number of devices enrolled in MDM</span></span>|
|<span data-ttu-id="80edb-128">dualEnrolledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="80edb-128">dualEnrolledDeviceCount</span></span>|<span data-ttu-id="80edb-129">Int32</span><span class="sxs-lookup"><span data-stu-id="80edb-129">Int32</span></span>|<span data-ttu-id="80edb-130">El número de dispositivos inscritos tanto en MDM como EAS</span><span class="sxs-lookup"><span data-stu-id="80edb-130">The number of devices enrolled in both MDM and EAS</span></span>|
|<span data-ttu-id="80edb-131">deviceOperatingSystemSummary</span><span class="sxs-lookup"><span data-stu-id="80edb-131">deviceOperatingSystemSummary</span></span>|[<span data-ttu-id="80edb-132">deviceOperatingSystemSummary</span><span class="sxs-lookup"><span data-stu-id="80edb-132">deviceOperatingSystemSummary</span></span>](../resources/intune_devices_deviceoperatingsystemsummary.md)|<span data-ttu-id="80edb-133">Resumen de sistemas operativos de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="80edb-133">Device operating system summary.</span></span>|
|<span data-ttu-id="80edb-134">deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="80edb-134">deviceExchangeAccessStateSummary</span></span>|[<span data-ttu-id="80edb-135">deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="80edb-135">deviceExchangeAccessStateSummary</span></span>](../resources/intune_devices_deviceexchangeaccessstatesummary.md)|<span data-ttu-id="80edb-136">Distribución del estado de acceso de Exchange en Intune</span><span class="sxs-lookup"><span data-stu-id="80edb-136">Distribution of Exchange Access State in Intune</span></span>|

## <a name="relationships"></a><span data-ttu-id="80edb-137">Relaciones</span><span class="sxs-lookup"><span data-stu-id="80edb-137">Relationships</span></span>
<span data-ttu-id="80edb-138">Ninguna</span><span class="sxs-lookup"><span data-stu-id="80edb-138">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="80edb-139">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="80edb-139">JSON Representation</span></span>
<span data-ttu-id="80edb-140">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="80edb-140">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedDeviceOverview"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDeviceOverview",
  "id": "String (identifier)",
  "enrolledDeviceCount": 1024,
  "mdmEnrolledCount": 1024,
  "dualEnrolledDeviceCount": 1024,
  "deviceOperatingSystemSummary": {
    "@odata.type": "microsoft.graph.deviceOperatingSystemSummary",
    "androidCount": 1024,
    "iosCount": 1024,
    "macOSCount": 1024,
    "windowsMobileCount": 1024,
    "windowsCount": 1024,
    "unknownCount": 1024
  },
  "deviceExchangeAccessStateSummary": {
    "@odata.type": "microsoft.graph.deviceExchangeAccessStateSummary",
    "allowedDeviceCount": 1024,
    "blockedDeviceCount": 1024,
    "quarantinedDeviceCount": 1024,
    "unknownDeviceCount": 1024,
    "unavailableDeviceCount": 1024
  }
}
```



