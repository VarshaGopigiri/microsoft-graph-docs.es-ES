# <a name="manageddevice-resource-type"></a><span data-ttu-id="5cb4f-101">Tipo de recurso managedDevice</span><span class="sxs-lookup"><span data-stu-id="5cb4f-101">managedDevice resource type</span></span>

> <span data-ttu-id="5cb4f-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5cb4f-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5cb4f-103">Dispositivos administrados o inscritos previamente a través de Intune</span><span class="sxs-lookup"><span data-stu-id="5cb4f-103">Devices that are managed or pre-enrolled through Intune</span></span>
## <a name="methods"></a><span data-ttu-id="5cb4f-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="5cb4f-104">Methods</span></span>
|<span data-ttu-id="5cb4f-105">Método</span><span class="sxs-lookup"><span data-stu-id="5cb4f-105">Method</span></span>|<span data-ttu-id="5cb4f-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5cb4f-106">Return Type</span></span>|<span data-ttu-id="5cb4f-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="5cb4f-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="5cb4f-108">Enumerar managedDevices</span><span class="sxs-lookup"><span data-stu-id="5cb4f-108">List managedDevices</span></span>](../api/intune_deviceconfig_manageddevice_list.md)|<span data-ttu-id="5cb4f-109">Colección [managedDevice](../resources/intune_deviceconfig_manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="5cb4f-109">[managedDevice](../resources/intune_deviceconfig_manageddevice.md) collection</span></span>|<span data-ttu-id="5cb4f-110">Enumere las propiedades y las relaciones de los objetos [managedDevice](../resources/intune_deviceconfig_manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="5cb4f-110">List properties and relationships of the [managedDevice](../resources/intune_deviceconfig_manageddevice.md) objects.</span></span>|
|[<span data-ttu-id="5cb4f-111">Obtener managedDevice</span><span class="sxs-lookup"><span data-stu-id="5cb4f-111">Get managedDevice</span></span>](../api/intune_deviceconfig_manageddevice_get.md)|[<span data-ttu-id="5cb4f-112">managedDevice</span><span class="sxs-lookup"><span data-stu-id="5cb4f-112">managedDevice</span></span>](../resources/intune_deviceconfig_manageddevice.md)|<span data-ttu-id="5cb4f-113">Lea las propiedades y las relaciones del objeto [managedDevice](../resources/intune_deviceconfig_manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="5cb4f-113">Read properties and relationships of [plannerPlanDetails](../resources/intune_deviceconfig_manageddevice.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="5cb4f-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5cb4f-114">Properties</span></span>
|<span data-ttu-id="5cb4f-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5cb4f-115">Property</span></span>|<span data-ttu-id="5cb4f-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="5cb4f-116">Type</span></span>|<span data-ttu-id="5cb4f-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="5cb4f-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5cb4f-118">id</span><span class="sxs-lookup"><span data-stu-id="5cb4f-118">id</span></span>|<span data-ttu-id="5cb4f-119">cadena</span><span class="sxs-lookup"><span data-stu-id="5cb4f-119">String</span></span>|<span data-ttu-id="5cb4f-120">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="5cb4f-120">Not yet documented</span></span>|

## <a name="relationships"></a><span data-ttu-id="5cb4f-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5cb4f-121">Relationships</span></span>
|<span data-ttu-id="5cb4f-122">Relación</span><span class="sxs-lookup"><span data-stu-id="5cb4f-122">Relationship</span></span>|<span data-ttu-id="5cb4f-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="5cb4f-123">Type</span></span>|<span data-ttu-id="5cb4f-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="5cb4f-124">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5cb4f-125">deviceConfigurationStates</span><span class="sxs-lookup"><span data-stu-id="5cb4f-125">deviceConfigurationStates</span></span>|<span data-ttu-id="5cb4f-126">Colección [deviceConfigurationState](../resources/intune_deviceconfig_deviceconfigurationstate.md)</span><span class="sxs-lookup"><span data-stu-id="5cb4f-126">[deviceConfigurationState](../resources/intune_deviceconfig_deviceconfigurationstate.md) collection</span></span>|<span data-ttu-id="5cb4f-127">Estados de configuración del dispositivo para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5cb4f-127">Device configuration states for this device.</span></span>|
|<span data-ttu-id="5cb4f-128">deviceCompliancePolicyStates</span><span class="sxs-lookup"><span data-stu-id="5cb4f-128">deviceCompliancePolicyStates</span></span>|<span data-ttu-id="5cb4f-129">Colección [deviceCompliancePolicyState](../resources/intune_deviceconfig_devicecompliancepolicystate.md)</span><span class="sxs-lookup"><span data-stu-id="5cb4f-129">[deviceCompliancePolicyState](../resources/intune_deviceconfig_devicecompliancepolicystate.md) collection</span></span>|<span data-ttu-id="5cb4f-130">Estados de directivas de cumplimiento del dispositivo para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5cb4f-130">Device compliance policy states for this device.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="5cb4f-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5cb4f-131">JSON Representation</span></span>
<span data-ttu-id="5cb4f-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5cb4f-132">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedDevice"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDevice",
  "id": "String (identifier)"
}
```



