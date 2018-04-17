# <a name="devicemanagement-resource-type"></a><span data-ttu-id="cb201-101">Tipo de recurso deviceManagement</span><span class="sxs-lookup"><span data-stu-id="cb201-101">deviceManagement resource type</span></span>

> <span data-ttu-id="cb201-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cb201-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cb201-103">El recurso deviceManagement representa las identidades de dispositivo de colección de un espacio empresarial que se han preconfigurado en Intune y los perfiles de inscripción que se pueden asignar a las identidades de dispositivos compatibles con la configuración de preinscripción.</span><span class="sxs-lookup"><span data-stu-id="cb201-103">The deviceManagement resource represents a tenant's collection device identities that have been pre-staged in Intune, and the enrollment profiles that may be assigned to device identities that support pre-enrollment configuration.</span></span>
## <a name="methods"></a><span data-ttu-id="cb201-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="cb201-104">Methods</span></span>
|<span data-ttu-id="cb201-105">Método</span><span class="sxs-lookup"><span data-stu-id="cb201-105">Method</span></span>|<span data-ttu-id="cb201-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb201-106">Return Type</span></span>|<span data-ttu-id="cb201-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="cb201-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="cb201-108">Obtener deviceManagement</span><span class="sxs-lookup"><span data-stu-id="cb201-108">Get deviceManagement</span></span>](../api/intune_enrollment_devicemanagement_get.md)|[<span data-ttu-id="cb201-109">deviceManagement</span><span class="sxs-lookup"><span data-stu-id="cb201-109">deviceManagement</span></span>](../resources/intune_enrollment_devicemanagement.md)|<span data-ttu-id="cb201-110">Lea las propiedades y las relaciones del objeto [deviceManagement](../resources/intune_enrollment_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="cb201-110">Read properties and relationships of the [deviceManagement](../resources/intune_enrollment_devicemanagement.md) object.</span></span>|
|[<span data-ttu-id="cb201-111">Actualizar deviceManagement</span><span class="sxs-lookup"><span data-stu-id="cb201-111">Update deviceManagement</span></span>](../api/intune_enrollment_devicemanagement_update.md)|[<span data-ttu-id="cb201-112">deviceManagement</span><span class="sxs-lookup"><span data-stu-id="cb201-112">deviceManagement</span></span>](../resources/intune_enrollment_devicemanagement.md)|<span data-ttu-id="cb201-113">Actualice las propiedades de un objeto [deviceManagement](../resources/intune_enrollment_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="cb201-113">Update the properties of a [deviceManagement](../resources/intune_enrollment_devicemanagement.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="cb201-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cb201-114">Properties</span></span>
|<span data-ttu-id="cb201-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cb201-115">Property</span></span>|<span data-ttu-id="cb201-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="cb201-116">Type</span></span>|<span data-ttu-id="cb201-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="cb201-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cb201-118">id</span><span class="sxs-lookup"><span data-stu-id="cb201-118">id</span></span>|<span data-ttu-id="cb201-119">String</span><span class="sxs-lookup"><span data-stu-id="cb201-119">String</span></span>|<span data-ttu-id="cb201-120">El GUID para el objeto.</span><span class="sxs-lookup"><span data-stu-id="cb201-120">The GUID for the object.</span></span>|

## <a name="relationships"></a><span data-ttu-id="cb201-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="cb201-121">Relationships</span></span>
|<span data-ttu-id="cb201-122">Relación</span><span class="sxs-lookup"><span data-stu-id="cb201-122">Relationship</span></span>|<span data-ttu-id="cb201-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="cb201-123">Type</span></span>|<span data-ttu-id="cb201-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="cb201-124">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cb201-125">importedWindowsAutopilotDeviceIdentities</span><span class="sxs-lookup"><span data-stu-id="cb201-125">importedWindowsAutopilotDeviceIdentities</span></span>|<span data-ttu-id="cb201-126">Colección [importedWindowsAutopilotDeviceIdentity](../resources/intune_enrollment_importedwindowsautopilotdeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="cb201-126">[importedWindowsAutopilotDeviceIdentity](../resources/intune_enrollment_importedwindowsautopilotdeviceidentity.md) collection</span></span>|<span data-ttu-id="cb201-127">Colección de dispositivos importados de Windows Autopilot</span><span class="sxs-lookup"><span data-stu-id="cb201-127">Collection of imported Windows autopilot devices.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="cb201-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cb201-128">JSON Representation</span></span>
<span data-ttu-id="cb201-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="cb201-129">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagement"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagement",
  "id": "String (identifier)"
}
```



