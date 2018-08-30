# <a name="user-resource-type"></a><span data-ttu-id="75147-101">Tipo de recurso del usuario</span><span class="sxs-lookup"><span data-stu-id="75147-101">user resource type</span></span>

> <span data-ttu-id="75147-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="75147-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="75147-103">Representa un objeto de usuario de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="75147-103">Represents an Azure Active Directory user object.</span></span>

## <a name="methods"></a><span data-ttu-id="75147-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="75147-104">Methods</span></span>
|<span data-ttu-id="75147-105">Método</span><span class="sxs-lookup"><span data-stu-id="75147-105">Method</span></span>|<span data-ttu-id="75147-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75147-106">Return Type</span></span>|<span data-ttu-id="75147-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="75147-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="75147-108">Objetos [List users](../api/intune_shared_user_list.md).</span><span class="sxs-lookup"><span data-stu-id="75147-108">[List users](../api/intune_shared_user_list.md) objects.</span></span>|
|<span data-ttu-id="75147-109">Objeto [Get user](../api/intune_shared_user_get.md).</span><span class="sxs-lookup"><span data-stu-id="75147-109">[Get user](../api/intune_shared_user_get.md) object.</span></span>|
|<span data-ttu-id="75147-110">Objeto [Create user](../api/intune_shared_user_create.md).</span><span class="sxs-lookup"><span data-stu-id="75147-110">Create a new [user](../api/intune_shared_user_create.md) object.</span></span>|
|<span data-ttu-id="75147-111">[Delete user](../api/intune_shared_user_delete.md).</span><span class="sxs-lookup"><span data-stu-id="75147-111">Delete user</span></span>|
|<span data-ttu-id="75147-112">Objeto [Update user](../api/intune_shared_user_update.md).</span><span class="sxs-lookup"><span data-stu-id="75147-112">Update user object.</span></span>|
|<span data-ttu-id="75147-113">**Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="75147-113">**Device management**</span></span>|
|[<span data-ttu-id="75147-114">Acción removeAllDevicesFromManagement</span><span class="sxs-lookup"><span data-stu-id="75147-114">removeAllDevicesFromManagement action</span></span>](../api/intune_shared_user_removealldevicesfrommanagement.md)|<span data-ttu-id="75147-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="75147-115">None</span></span>|<span data-ttu-id="75147-116">Retirar todos los dispositivos de la administración para este usuario</span><span class="sxs-lookup"><span data-stu-id="75147-116">Retire all devices from management for this user</span></span>|
|<span data-ttu-id="75147-117">**Administración de aplicaciones móviles (MAM)**</span><span class="sxs-lookup"><span data-stu-id="75147-117">**Mobile app management (MAM)**</span></span>|
|[<span data-ttu-id="75147-118">Función getManagedAppDiagnosticStatuses</span><span class="sxs-lookup"><span data-stu-id="75147-118">getManagedAppDiagnosticStatuses function</span></span>](../api/intune_shared_user_getmanagedappdiagnosticstatuses.md)|<span data-ttu-id="75147-119">Colección [getManagedAppDiagnosticStatus](../resources/intune_mam_managedappdiagnosticstatus.md)</span><span class="sxs-lookup"><span data-stu-id="75147-119">[managedAppDiagnosticStatus](../resources/intune_mam_managedappdiagnosticstatus.md) collection</span></span>|<span data-ttu-id="75147-120">Obtiene estados de validación de diagnósticos de un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="75147-120">Gets diagnostics validation status for a given user.</span></span>|
|[<span data-ttu-id="75147-121">Función getManagedAppPolicies</span><span class="sxs-lookup"><span data-stu-id="75147-121">getManagedAppPolicies function</span></span>](../api/intune_shared_user_getmanagedapppolicies.md)|<span data-ttu-id="75147-122">Colección [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="75147-122">[managedAppPolicy](../resources/intune_mam_managedapppolicy.md) collection</span></span>|<span data-ttu-id="75147-123">Obtiene las restricciones de aplicaciones de un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="75147-123">Gets app restrictions for a given user.</span></span>|
|[<span data-ttu-id="75147-124">Acción wipeManagedAppRegistrationsByDeviceTag</span><span class="sxs-lookup"><span data-stu-id="75147-124">wipeManagedAppRegistrationsByDeviceTag action</span></span>](../api/intune_shared_user_wipemanagedappregistrationsbydevicetag.md)|<span data-ttu-id="75147-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="75147-125">None</span></span>|<span data-ttu-id="75147-126">Emite una operación de borrado en un registro de la aplicación con la etiqueta del dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="75147-126">Issues a wipe operation on an app registration with specified device tag.</span></span>|

## <a name="properties"></a><span data-ttu-id="75147-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="75147-127">Properties</span></span>
|<span data-ttu-id="75147-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="75147-128">Property</span></span>|<span data-ttu-id="75147-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="75147-129">Type</span></span>|<span data-ttu-id="75147-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="75147-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="75147-131">id</span><span class="sxs-lookup"><span data-stu-id="75147-131">id</span></span>|<span data-ttu-id="75147-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="75147-132">String</span></span>|<span data-ttu-id="75147-133">Identificador único del usuario.</span><span class="sxs-lookup"><span data-stu-id="75147-133">Unique identifier of the user.</span></span>|
|<span data-ttu-id="75147-134">**Incorporación**</span><span class="sxs-lookup"><span data-stu-id="75147-134">**On-boarding**</span></span>|
|<span data-ttu-id="75147-135">deviceEnrollmentLimit</span><span class="sxs-lookup"><span data-stu-id="75147-135">deviceEnrollmentLimit</span></span>|<span data-ttu-id="75147-136">Int32</span><span class="sxs-lookup"><span data-stu-id="75147-136">Int32</span></span>|<span data-ttu-id="75147-137">El límite del número máximo de dispositivos que el usuario puede inscribir.</span><span class="sxs-lookup"><span data-stu-id="75147-137">The limit on the maximum number of devices that the user is permitted to enroll.</span></span> <span data-ttu-id="75147-138">Los valores permitidos son 5 o 1000.</span><span class="sxs-lookup"><span data-stu-id="75147-138">Allowed values are 5 or 1000.</span></span>|


## <a name="relationships"></a><span data-ttu-id="75147-139">Relaciones</span><span class="sxs-lookup"><span data-stu-id="75147-139">Relationships</span></span>
|<span data-ttu-id="75147-140">Relación</span><span class="sxs-lookup"><span data-stu-id="75147-140">Relationship</span></span>|<span data-ttu-id="75147-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="75147-141">Type</span></span>|<span data-ttu-id="75147-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="75147-142">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="75147-143">**Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="75147-143">**Device management**</span></span>|
|<span data-ttu-id="75147-144">managedDevices</span><span class="sxs-lookup"><span data-stu-id="75147-144">managedDevices</span></span>|<span data-ttu-id="75147-145">Colección [managedDevice](../resources/intune_devices_manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="75147-145">[managedDevice](../resources/intune_devices_manageddevice.md) collection</span></span>|<span data-ttu-id="75147-146">Los dispositivos administrados asociados al usuario.</span><span class="sxs-lookup"><span data-stu-id="75147-146">The managed devices associated with the user.</span></span>|
|<span data-ttu-id="75147-147">**Administración de aplicaciones móviles (MAM)**</span><span class="sxs-lookup"><span data-stu-id="75147-147">**Mobile app management (MAM)**</span></span>|
|<span data-ttu-id="75147-148">managedAppRegistrations</span><span class="sxs-lookup"><span data-stu-id="75147-148">managedAppRegistrations</span></span>|<span data-ttu-id="75147-149">Colección [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="75147-149">[managedAppRegistration](../resources/intune_mam_managedappregistration.md) collection</span></span>|<span data-ttu-id="75147-150">Cero o más registros de administración de aplicaciones administradas que pertenecen al usuario.</span><span class="sxs-lookup"><span data-stu-id="75147-150">Zero or more managed app registrations that belong to the user.</span></span>|
|<span data-ttu-id="75147-151">**Solución de problemas**</span><span class="sxs-lookup"><span data-stu-id="75147-151">**Troubleshooting**</span></span>|
|<span data-ttu-id="75147-152">deviceManagementTroubleshootingEvents</span><span class="sxs-lookup"><span data-stu-id="75147-152">deviceManagementTroubleshootingEvents</span></span>|<span data-ttu-id="75147-153">Colección [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="75147-153">[deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md) collection</span></span>|<span data-ttu-id="75147-154">La lista de eventos de solución de problemas para este usuario.</span><span class="sxs-lookup"><span data-stu-id="75147-154">The list of troubleshooting events for this user.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="75147-155">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="75147-155">JSON Representation</span></span>
<span data-ttu-id="75147-156">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="75147-156">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.directoryObject",
  "openType": true,
  "@odata.type": "microsoft.graph.user"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.user",
  "id": "String (identifier)",
  "deviceEnrollmentLimit": 5
}
```

<!-- {
  "type": "#page.annotation",
  "suppressions": [
    "Warning: Resource microsoft.graph.user is defined in multiple files: /api-reference/v1.0/resources/intune_shared_user.md, /api-reference/v1.0/resources/user.md",
  ]
}-->
