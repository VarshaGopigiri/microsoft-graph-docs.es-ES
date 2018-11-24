# <a name="update-devicemanagement"></a><span data-ttu-id="ed493-101">Actualizar deviceManagement</span><span class="sxs-lookup"><span data-stu-id="ed493-101">Update deviceManagement</span></span>

> <span data-ttu-id="ed493-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ed493-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ed493-103">Actualice las propiedades de un objeto [deviceManagement](../resources/intune_shared_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="ed493-103">Update the properties of a [deviceManagement](../resources/intune_shared_devicemanagement.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ed493-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ed493-104">Prerequisites</span></span>
<span data-ttu-id="ed493-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ed493-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="ed493-107">Permisos&nbsp;tipo&nbsp;(por&nbsp;flujo de trabajo)</span><span class="sxs-lookup"><span data-stu-id="ed493-107">Permission&nbsp;type&nbsp;(by&nbsp;workflow)</span></span> | <span data-ttu-id="ed493-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ed493-108">Permissions (from most to least privileged)</span></span> |
|:---|:---|
| <span data-ttu-id="ed493-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ed493-109">Delegated (work or school account)</span></span> |
| <span data-ttu-id="ed493-110">&nbsp;&nbsp; Auditoría</span><span class="sxs-lookup"><span data-stu-id="ed493-110">&nbsp; &nbsp; Auditing</span></span> | <span data-ttu-id="ed493-111">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed493-111">DeviceManagementApps.ReadWrite.All</span></span> |
| <span data-ttu-id="ed493-112">&nbsp;&nbsp; Los términos de la empresa</span><span class="sxs-lookup"><span data-stu-id="ed493-112">&nbsp; &nbsp; Company terms</span></span> | <span data-ttu-id="ed493-113">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed493-113">DeviceManagementServiceConfig.ReadWrite.All</span></span> |
| <span data-ttu-id="ed493-114">&nbsp;&nbsp; Inscripción corporativa</span><span class="sxs-lookup"><span data-stu-id="ed493-114">&nbsp; &nbsp; Corporate enrollment</span></span> | <span data-ttu-id="ed493-115">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed493-115">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
| <span data-ttu-id="ed493-116">&nbsp;&nbsp; Configuración de dispositivo</span><span class="sxs-lookup"><span data-stu-id="ed493-116">&nbsp; &nbsp; Device configuration</span></span> | <span data-ttu-id="ed493-117">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed493-117">DeviceManagementConfiguration.ReadWrite.All</span></span> |
| <span data-ttu-id="ed493-118">&nbsp;&nbsp; Administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="ed493-118">&nbsp; &nbsp; Device management</span></span> | <span data-ttu-id="ed493-119">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed493-119">DeviceManagementManagedDevices.ReadWrite.All</span></span> |
| <span data-ttu-id="ed493-120">&nbsp;&nbsp; Protección de extremo</span><span class="sxs-lookup"><span data-stu-id="ed493-120">&nbsp; &nbsp; Endpoint protection</span></span> | <span data-ttu-id="ed493-121">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed493-121">DeviceManagementManagedDevices.ReadWrite.All</span></span> |
| <span data-ttu-id="ed493-122">&nbsp;&nbsp; Notificación</span><span class="sxs-lookup"><span data-stu-id="ed493-122">&nbsp; &nbsp; Notification</span></span> | <span data-ttu-id="ed493-123">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed493-123">DeviceManagementServiceConfig.ReadWrite.All</span></span> |
| <span data-ttu-id="ed493-124">&nbsp;&nbsp; Incorporación</span><span class="sxs-lookup"><span data-stu-id="ed493-124">&nbsp; &nbsp; Onboarding</span></span> | <span data-ttu-id="ed493-125">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed493-125">DeviceManagementServiceConfig.ReadWrite.All</span></span> |
| <span data-ttu-id="ed493-126">&nbsp;&nbsp; Control de acceso basado en roles</span><span class="sxs-lookup"><span data-stu-id="ed493-126">&nbsp; &nbsp; Role-based access control</span></span> | <span data-ttu-id="ed493-127">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed493-127">DeviceManagementRBAC.ReadWrite.All</span></span> |
| <span data-ttu-id="ed493-128">&nbsp;&nbsp; Asistencia remota</span><span class="sxs-lookup"><span data-stu-id="ed493-128">&nbsp; &nbsp; Remote assistance</span></span> | <span data-ttu-id="ed493-129">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed493-129">DeviceManagementServiceConfig.ReadWrite.All</span></span> |
| <span data-ttu-id="ed493-130">&nbsp;&nbsp; Gestión de gastos de telecomunicaciones</span><span class="sxs-lookup"><span data-stu-id="ed493-130">&nbsp; &nbsp; Telecom expense management</span></span> | <span data-ttu-id="ed493-131">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed493-131">DeviceManagementServiceConfig.ReadWrite.All</span></span> |
| <span data-ttu-id="ed493-132">&nbsp;&nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="ed493-132">&nbsp; &nbsp; Troubleshooting</span></span> | <span data-ttu-id="ed493-133">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed493-133">DeviceManagementManagedDevices.ReadWrite.All</span></span> |
| <span data-ttu-id="ed493-134">&nbsp;&nbsp; Protección de la información de Windows</span><span class="sxs-lookup"><span data-stu-id="ed493-134">&nbsp; &nbsp; Windows Information Protection</span></span> | <span data-ttu-id="ed493-135">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed493-135">DeviceManagementApps.ReadWrite.All</span></span> |
| <span data-ttu-id="ed493-136">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ed493-136">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ed493-137">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ed493-137">Not supported.</span></span>|
| <span data-ttu-id="ed493-138">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ed493-138">Application</span></span> | <span data-ttu-id="ed493-139">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ed493-139">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="ed493-140">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ed493-140">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement
```

## <a name="request-headers"></a><span data-ttu-id="ed493-141">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ed493-141">Request headers</span></span>
|<span data-ttu-id="ed493-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed493-142">Header</span></span>|<span data-ttu-id="ed493-143">Valor</span><span class="sxs-lookup"><span data-stu-id="ed493-143">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ed493-144">Authorization</span><span class="sxs-lookup"><span data-stu-id="ed493-144">Authorization</span></span>|<span data-ttu-id="ed493-145">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ed493-145">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ed493-146">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ed493-146">Accept</span></span>|<span data-ttu-id="ed493-147">application/json</span><span class="sxs-lookup"><span data-stu-id="ed493-147">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ed493-148">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ed493-148">Request body</span></span>
<span data-ttu-id="ed493-149">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceManagement](../resources/intune_shared_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="ed493-149">In the request body, supply a JSON representation for the [deviceManagement](../resources/intune_shared_devicemanagement.md) object.</span></span>

<span data-ttu-id="ed493-150">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceManagement](../resources/intune_shared_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="ed493-150">The following table shows the properties that are required when you create the [deviceManagement](../resources/intune_shared_devicemanagement.md).</span></span>

|<span data-ttu-id="ed493-151">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ed493-151">Property</span></span>|<span data-ttu-id="ed493-152">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed493-152">Type</span></span>|<span data-ttu-id="ed493-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed493-153">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ed493-154">id</span><span class="sxs-lookup"><span data-stu-id="ed493-154">id</span></span>|<span data-ttu-id="ed493-155">String</span><span class="sxs-lookup"><span data-stu-id="ed493-155">String</span></span>|<span data-ttu-id="ed493-156">Identificador único del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ed493-156">Unique Identifier for the device</span></span>|
|<span data-ttu-id="ed493-157">**Configuración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="ed493-157">**Device configuration**</span></span>|
|<span data-ttu-id="ed493-158">configuración</span><span class="sxs-lookup"><span data-stu-id="ed493-158">settings</span></span>|[<span data-ttu-id="ed493-159">deviceManagementSettings</span><span class="sxs-lookup"><span data-stu-id="ed493-159">deviceManagementSettings</span></span>](../resources/intune_deviceconfig_devicemanagementsettings.md)|<span data-ttu-id="ed493-160">Configuración de niveles de cuenta.</span><span class="sxs-lookup"><span data-stu-id="ed493-160">Account level settings.</span></span>|
|<span data-ttu-id="ed493-161">**Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="ed493-161">**Device management**</span></span>|
|<span data-ttu-id="ed493-162">subscriptionState</span><span class="sxs-lookup"><span data-stu-id="ed493-162">subscriptionState</span></span>|[<span data-ttu-id="ed493-163">deviceManagementSubscriptionState</span><span class="sxs-lookup"><span data-stu-id="ed493-163">deviceManagementSubscriptionState</span></span>](../resources/intune_devices_devicemanagementsubscriptionstate.md)|<span data-ttu-id="ed493-164">Estado de suscripción de administración de dispositivos móviles del espacio empresarial.</span><span class="sxs-lookup"><span data-stu-id="ed493-164">Tenant mobile device management subscription state.</span></span> <span data-ttu-id="ed493-165">Los valores posibles son: `pending`, `active`, `warning`, `disabled`, `deleted`, `blocked`, `lockedOut`.</span><span class="sxs-lookup"><span data-stu-id="ed493-165">The possible values are: `pending`, `active`, `warning`, `disabled`, `deleted`, `blocked`, `lockedOut`.</span></span>|
|<span data-ttu-id="ed493-166">**Incorporación de redes**</span><span class="sxs-lookup"><span data-stu-id="ed493-166">**Onboarding**</span></span>|
|<span data-ttu-id="ed493-167">intuneBrand</span><span class="sxs-lookup"><span data-stu-id="ed493-167">intuneBrand</span></span>|[<span data-ttu-id="ed493-168">intuneBrand</span><span class="sxs-lookup"><span data-stu-id="ed493-168">intuneBrand</span></span>](../resources/intune_onboarding_intunebrand.md)|<span data-ttu-id="ed493-169">intuneBrand contiene datos que se usan para personalizar las aplicaciones del Portal de empresa, así como el portal web del usuario final.</span><span class="sxs-lookup"><span data-stu-id="ed493-169">intuneBrand contains data which is used in customizing the appearance of the Company Portal applications as well as the end user web portal.</span></span>|

<span data-ttu-id="ed493-170">Compatibilidad con propiedades de cuerpo de solicitud varía según el flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="ed493-170">Request body property support varies according to workflow.</span></span>

## <a name="response"></a><span data-ttu-id="ed493-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ed493-171">Response</span></span>
<span data-ttu-id="ed493-172">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceManagement](../resources/intune_shared_devicemanagement.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ed493-172">If successful, this method returns a `200 OK` response code and an updated [deviceManagement](../resources/intune_shared_devicemanagement.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ed493-173">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ed493-173">Example</span></span>

### <a name="request"></a><span data-ttu-id="ed493-174">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ed493-174">Request</span></span>
<span data-ttu-id="ed493-175">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ed493-175">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement
Content-type: application/json
Content-length: 751

{
  "subscriptionState": "active",
  "subscriptions": "intune",
  "adminConsent": {
    "@odata.type": "microsoft.graph.adminConsent",
    "shareAPNSData": "granted"
  },
  "deviceProtectionOverview": {
    "@odata.type": "microsoft.graph.deviceProtectionOverview",
    "totalReportedDeviceCount": 8,
    "inactiveThreatAgentDeviceCount": 14,
    "unknownStateThreatAgentDeviceCount": 2,
    "pendingSignatureUpdateDeviceCount": 1,
    "cleanDeviceCount": 0,
    "pendingFullScanDeviceCount": 10,
    "pendingRestartDeviceCount": 9,
    "pendingManualStepsDeviceCount": 13,
    "pendingOfflineScanDeviceCount": 13,
    "criticalFailuresDeviceCount": 11
  },
  "accountMoveCompletionDateTime": "2017-01-01T00:01:17.9006709-08:00"
}
```

### <a name="response"></a><span data-ttu-id="ed493-176">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ed493-176">Response</span></span>

<span data-ttu-id="ed493-177">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ed493-177">Here is an example of the response.</span></span> <span data-ttu-id="ed493-178">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="ed493-178">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="ed493-179">Propiedades devueltas varían según el flujo de trabajo y el contexto.</span><span class="sxs-lookup"><span data-stu-id="ed493-179">Returned properties vary according to workflow and context.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 855

{
  "@odata.type": "#microsoft.graph.deviceManagement",
  "id": "0b283420-3420-0b28-2034-280b2034280b",
  "subscriptionState": "active",
  "subscriptions": "intune",
  "adminConsent": {
    "@odata.type": "microsoft.graph.adminConsent",
    "shareAPNSData": "granted"
  },
  "deviceProtectionOverview": {
    "@odata.type": "microsoft.graph.deviceProtectionOverview",
    "totalReportedDeviceCount": 8,
    "inactiveThreatAgentDeviceCount": 14,
    "unknownStateThreatAgentDeviceCount": 2,
    "pendingSignatureUpdateDeviceCount": 1,
    "cleanDeviceCount": 0,
    "pendingFullScanDeviceCount": 10,
    "pendingRestartDeviceCount": 9,
    "pendingManualStepsDeviceCount": 13,
    "pendingOfflineScanDeviceCount": 13,
    "criticalFailuresDeviceCount": 11
  },
  "accountMoveCompletionDateTime": "2017-01-01T00:01:17.9006709-08:00"
}
```



