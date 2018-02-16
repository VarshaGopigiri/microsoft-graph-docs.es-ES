# <a name="devicemanagement-resource-type"></a><span data-ttu-id="abff8-101">Tipo de recurso deviceManagement</span><span class="sxs-lookup"><span data-stu-id="abff8-101">deviceManagement resource type</span></span>

> <span data-ttu-id="abff8-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="abff8-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="abff8-103">Entidad singleton que actúa como un contenedor para todas las funcionalidades de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="abff8-103">Singleton entity that acts as a container for all device management functionality.</span></span>
## <a name="methods"></a><span data-ttu-id="abff8-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="abff8-104">Methods</span></span>
|<span data-ttu-id="abff8-105">Método</span><span class="sxs-lookup"><span data-stu-id="abff8-105">Method</span></span>|<span data-ttu-id="abff8-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="abff8-106">Return Type</span></span>|<span data-ttu-id="abff8-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="abff8-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="abff8-108">Obtener deviceManagement</span><span class="sxs-lookup"><span data-stu-id="abff8-108">Get deviceManagement</span></span>](../api/intune_devices_devicemanagement_get.md)|[<span data-ttu-id="abff8-109">deviceManagement</span><span class="sxs-lookup"><span data-stu-id="abff8-109">deviceManagement</span></span>](../resources/intune_devices_devicemanagement.md)|<span data-ttu-id="abff8-110">Lea las propiedades y las relaciones del objeto [deviceManagement](../resources/intune_devices_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="abff8-110">Read properties and relationships of [plannerTaskDetails](../resources/intune_devices_devicemanagement.md) object.</span></span>|
|[<span data-ttu-id="abff8-111">Actualizar deviceManagement</span><span class="sxs-lookup"><span data-stu-id="abff8-111">Update deviceManagement</span></span>](../api/intune_devices_devicemanagement_update.md)|[<span data-ttu-id="abff8-112">deviceManagement</span><span class="sxs-lookup"><span data-stu-id="abff8-112">deviceManagement</span></span>](../resources/intune_devices_devicemanagement.md)|<span data-ttu-id="abff8-113">Actualice las propiedades de un objeto [deviceManagement](../resources/intune_devices_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="abff8-113">Update the properties of a [calendar](../resources/intune_devices_devicemanagement.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="abff8-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="abff8-114">Properties</span></span>
|<span data-ttu-id="abff8-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="abff8-115">Property</span></span>|<span data-ttu-id="abff8-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="abff8-116">Type</span></span>|<span data-ttu-id="abff8-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="abff8-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="abff8-118">id</span><span class="sxs-lookup"><span data-stu-id="abff8-118">id</span></span>|<span data-ttu-id="abff8-119">cadena</span><span class="sxs-lookup"><span data-stu-id="abff8-119">String</span></span>|<span data-ttu-id="abff8-120">Identificador único del dispositivo</span><span class="sxs-lookup"><span data-stu-id="abff8-120">Unique Identifier for the device</span></span>|
|<span data-ttu-id="abff8-121">subscriptionState</span><span class="sxs-lookup"><span data-stu-id="abff8-121">subscriptionState</span></span>|<span data-ttu-id="abff8-122">cadena</span><span class="sxs-lookup"><span data-stu-id="abff8-122">String</span></span>|<span data-ttu-id="abff8-123">Estado de suscripción de administración de dispositivos móviles del espacio empresarial.</span><span class="sxs-lookup"><span data-stu-id="abff8-123">Tenant mobile device management subscription state.</span></span> <span data-ttu-id="abff8-124">Los valores posibles son: `pending`, `active`, `warning`, `disabled`, `deleted`, `blocked` y `lockedOut`.</span><span class="sxs-lookup"><span data-stu-id="abff8-124">Possible values are: `pending`, `active`, `warning`, `disabled`, `deleted`, `blocked`, `lockedOut`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="abff8-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="abff8-125">Relationships</span></span>
|<span data-ttu-id="abff8-126">Relación</span><span class="sxs-lookup"><span data-stu-id="abff8-126">Relationship</span></span>|<span data-ttu-id="abff8-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="abff8-127">Type</span></span>|<span data-ttu-id="abff8-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="abff8-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="abff8-129">applePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="abff8-129">applePushNotificationCertificate</span></span>|[<span data-ttu-id="abff8-130">applePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="abff8-130">applePushNotificationCertificate</span></span>](../resources/intune_devices_applepushnotificationcertificate.md)|<span data-ttu-id="abff8-131">Certificado de notificación de inserción de Apple.</span><span class="sxs-lookup"><span data-stu-id="abff8-131">Apple push notification certificate.</span></span>|
|<span data-ttu-id="abff8-132">managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="abff8-132">managedDeviceOverview</span></span>|[<span data-ttu-id="abff8-133">managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="abff8-133">managedDeviceOverview</span></span>](../resources/intune_devices_manageddeviceoverview.md)|<span data-ttu-id="abff8-134">Resumen de dispositivos</span><span class="sxs-lookup"><span data-stu-id="abff8-134">Device overview</span></span>|
|<span data-ttu-id="abff8-135">detectedApps</span><span class="sxs-lookup"><span data-stu-id="abff8-135">detectedApps</span></span>|<span data-ttu-id="abff8-136">Colección [detectedApp](../resources/intune_devices_detectedapp.md)</span><span class="sxs-lookup"><span data-stu-id="abff8-136">[detectedApp](../resources/intune_devices_detectedapp.md) collection</span></span>|<span data-ttu-id="abff8-137">La lista de aplicaciones detectadas asociadas a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="abff8-137">The list of detected apps associated with a device.</span></span>|
|<span data-ttu-id="abff8-138">managedDevices</span><span class="sxs-lookup"><span data-stu-id="abff8-138">managedDevices</span></span>|<span data-ttu-id="abff8-139">Colección [managedDevice](../resources/intune_devices_manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="abff8-139">[managedDevice](../resources/intune_devices_manageddevice.md) collection</span></span>|<span data-ttu-id="abff8-140">La lista de dispositivos administrados.</span><span class="sxs-lookup"><span data-stu-id="abff8-140">The list of managed devices.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="abff8-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="abff8-141">JSON Representation</span></span>
<span data-ttu-id="abff8-142">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="abff8-142">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagement"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagement",
  "id": "String (identifier)",
  "subscriptionState": "String"
}
```



