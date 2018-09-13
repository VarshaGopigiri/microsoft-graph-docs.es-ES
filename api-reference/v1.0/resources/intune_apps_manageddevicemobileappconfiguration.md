# <a name="manageddevicemobileappconfiguration-resource-type"></a><span data-ttu-id="94ad9-101">Tipo de recurso managedDeviceMobileAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="94ad9-101">managedDeviceMobileAppConfiguration resource type</span></span>

> <span data-ttu-id="94ad9-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="94ad9-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="94ad9-103">Una clase abstracta para la configuración de aplicaciones móviles para dispositivos inscritos.</span><span class="sxs-lookup"><span data-stu-id="94ad9-103">An abstract class for Mobile app configuration for enrolled devices.</span></span>
## <a name="methods"></a><span data-ttu-id="94ad9-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="94ad9-104">Methods</span></span>
|<span data-ttu-id="94ad9-105">Método</span><span class="sxs-lookup"><span data-stu-id="94ad9-105">Method</span></span>|<span data-ttu-id="94ad9-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94ad9-106">Return Type</span></span>|<span data-ttu-id="94ad9-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="94ad9-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="94ad9-108">Enumerar managedDeviceMobileAppConfigurations</span><span class="sxs-lookup"><span data-stu-id="94ad9-108">List managedDeviceMobileAppConfigurations</span></span>](../api/intune_apps_manageddevicemobileappconfiguration_list.md)|<span data-ttu-id="94ad9-109">Colección [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="94ad9-109">[managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md) collection</span></span>|<span data-ttu-id="94ad9-110">Enumere las propiedades y las relaciones de los objetos [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="94ad9-110">List properties and relationships of the [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md) objects.</span></span>|
|[<span data-ttu-id="94ad9-111">Obtener managedDeviceMobileAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="94ad9-111">Get managedDeviceMobileAppConfiguration</span></span>](../api/intune_apps_manageddevicemobileappconfiguration_get.md)|[<span data-ttu-id="94ad9-112">managedDeviceMobileAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="94ad9-112">managedDeviceMobileAppConfiguration</span></span>](../resources/intune_apps_manageddevicemobileappconfiguration.md)|<span data-ttu-id="94ad9-113">Lea las propiedades y las relaciones del objeto [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="94ad9-113">Read properties and relationships of the [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="94ad9-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="94ad9-114">Properties</span></span>
|<span data-ttu-id="94ad9-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="94ad9-115">Property</span></span>|<span data-ttu-id="94ad9-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="94ad9-116">Type</span></span>|<span data-ttu-id="94ad9-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="94ad9-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="94ad9-118">id</span><span class="sxs-lookup"><span data-stu-id="94ad9-118">id</span></span>|<span data-ttu-id="94ad9-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="94ad9-119">String</span></span>|<span data-ttu-id="94ad9-120">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="94ad9-120">Key of the entity.</span></span>|
|<span data-ttu-id="94ad9-121">targetedMobileApps</span><span class="sxs-lookup"><span data-stu-id="94ad9-121">targetedMobileApps</span></span>|<span data-ttu-id="94ad9-122">Colección string</span><span class="sxs-lookup"><span data-stu-id="94ad9-122">String collection</span></span>|<span data-ttu-id="94ad9-123">La aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="94ad9-123">the associated app.</span></span>|
|<span data-ttu-id="94ad9-124">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="94ad9-124">createdDateTime</span></span>|<span data-ttu-id="94ad9-125">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="94ad9-125">DateTimeOffset</span></span>|<span data-ttu-id="94ad9-126">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="94ad9-126">DateTime the object was created.</span></span>|
|<span data-ttu-id="94ad9-127">descripción</span><span class="sxs-lookup"><span data-stu-id="94ad9-127">description</span></span>|<span data-ttu-id="94ad9-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="94ad9-128">String</span></span>|<span data-ttu-id="94ad9-129">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="94ad9-129">Admin provided description of the Device Configuration.</span></span>|
|<span data-ttu-id="94ad9-130">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="94ad9-130">lastModifiedDateTime</span></span>|<span data-ttu-id="94ad9-131">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="94ad9-131">DateTimeOffset</span></span>|<span data-ttu-id="94ad9-132">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="94ad9-132">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="94ad9-133">displayName</span><span class="sxs-lookup"><span data-stu-id="94ad9-133">displayName</span></span>|<span data-ttu-id="94ad9-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="94ad9-134">String</span></span>|<span data-ttu-id="94ad9-135">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="94ad9-135">Admin provided name of the device configuration.</span></span>|
|<span data-ttu-id="94ad9-136">versión</span><span class="sxs-lookup"><span data-stu-id="94ad9-136">version</span></span>|<span data-ttu-id="94ad9-137">Int32</span><span class="sxs-lookup"><span data-stu-id="94ad9-137">Int32</span></span>|<span data-ttu-id="94ad9-138">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="94ad9-138">Version of the device configuration.</span></span>|

## <a name="relationships"></a><span data-ttu-id="94ad9-139">Relaciones</span><span class="sxs-lookup"><span data-stu-id="94ad9-139">Relationships</span></span>
|<span data-ttu-id="94ad9-140">Relación</span><span class="sxs-lookup"><span data-stu-id="94ad9-140">Relationship</span></span>|<span data-ttu-id="94ad9-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="94ad9-141">Type</span></span>|<span data-ttu-id="94ad9-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="94ad9-142">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="94ad9-143">assignments</span><span class="sxs-lookup"><span data-stu-id="94ad9-143">assignments</span></span>|<span data-ttu-id="94ad9-144">Colección [managedDeviceMobileAppConfigurationAssignment](../resources/intune_apps_manageddevicemobileappconfigurationassignment.md)</span><span class="sxs-lookup"><span data-stu-id="94ad9-144">[managedDeviceMobileAppConfigurationAssignment](../resources/intune_apps_manageddevicemobileappconfigurationassignment.md) collection</span></span>|<span data-ttu-id="94ad9-145">La lista de asignaciones de grupo para la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="94ad9-145">The list of group assignemenets for app configration.</span></span>|
|<span data-ttu-id="94ad9-146">deviceStatuses</span><span class="sxs-lookup"><span data-stu-id="94ad9-146">deviceStatuses</span></span>|<span data-ttu-id="94ad9-147">Colección de [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune_apps_manageddevicemobileappconfigurationdevicestatus.md)</span><span class="sxs-lookup"><span data-stu-id="94ad9-147">[managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune_apps_manageddevicemobileappconfigurationdevicestatus.md) collection</span></span>|<span data-ttu-id="94ad9-148">Lista de ManagedDeviceMobileAppConfigurationDeviceStatus.</span><span class="sxs-lookup"><span data-stu-id="94ad9-148">List of ManagedDeviceMobileAppConfigurationDeviceStatus.</span></span>|
|<span data-ttu-id="94ad9-149">userStatuses</span><span class="sxs-lookup"><span data-stu-id="94ad9-149">userStatuses</span></span>|<span data-ttu-id="94ad9-150">Colección [managedDeviceMobileAppConfigurationUserStatus](../resources/intune_apps_manageddevicemobileappconfigurationuserstatus.md)</span><span class="sxs-lookup"><span data-stu-id="94ad9-150">[managedDeviceMobileAppConfigurationUserStatus](../resources/intune_apps_manageddevicemobileappconfigurationuserstatus.md) collection</span></span>|<span data-ttu-id="94ad9-151">Lista de ManagedDeviceMobileAppConfigurationUserStatus.</span><span class="sxs-lookup"><span data-stu-id="94ad9-151">List of ManagedDeviceMobileAppConfigurationUserStatus.</span></span>|
|<span data-ttu-id="94ad9-152">deviceStatusSummary</span><span class="sxs-lookup"><span data-stu-id="94ad9-152">deviceStatusSummary</span></span>|[<span data-ttu-id="94ad9-153">managedDeviceMobileAppConfigurationDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="94ad9-153">managedDeviceMobileAppConfigurationDeviceSummary</span></span>](../resources/intune_apps_manageddevicemobileappconfigurationdevicesummary.md)|<span data-ttu-id="94ad9-154">Resumen del estado del dispositivo de la configuración de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="94ad9-154">App configuration device status summary.</span></span>|
|<span data-ttu-id="94ad9-155">userStatusSummary</span><span class="sxs-lookup"><span data-stu-id="94ad9-155">userStatusSummary</span></span>|[<span data-ttu-id="94ad9-156">managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="94ad9-156">managedDeviceMobileAppConfigurationUserSummary</span></span>](../resources/intune_apps_manageddevicemobileappconfigurationusersummary.md)|<span data-ttu-id="94ad9-157">Resumen del estado del usuario de la configuración de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="94ad9-157">App configuration user status summary.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="94ad9-158">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="94ad9-158">JSON Representation</span></span>
<span data-ttu-id="94ad9-159">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="94ad9-159">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedDeviceMobileAppConfiguration"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfiguration",
  "id": "String (identifier)",
  "targetedMobileApps": [
    "String"
  ],
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "version": 1024
}
```








