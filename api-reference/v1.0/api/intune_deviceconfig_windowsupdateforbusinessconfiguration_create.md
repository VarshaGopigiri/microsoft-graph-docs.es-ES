# <a name="create-windowsupdateforbusinessconfiguration"></a><span data-ttu-id="80941-101">Crear windowsUpdateForBusinessConfiguration</span><span class="sxs-lookup"><span data-stu-id="80941-101">Create windowsUpdateForBusinessConfiguration</span></span>

> <span data-ttu-id="80941-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="80941-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="80941-103">Crear un objeto [windowsUpdateForBusinessConfiguration](../resources/intune_deviceconfig_windowsupdateforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="80941-103">Create a new [windowsUpdateForBusinessConfiguration](../resources/intune_deviceconfig_windowsupdateforbusinessconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="80941-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="80941-104">Prerequisites</span></span>
<span data-ttu-id="80941-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="80941-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="80941-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="80941-107">Permission type</span></span>|<span data-ttu-id="80941-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="80941-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="80941-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="80941-109">Delegated (work or school account)</span></span>|<span data-ttu-id="80941-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="80941-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="80941-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="80941-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="80941-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="80941-112">Not supported.</span></span>|
|<span data-ttu-id="80941-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="80941-113">Application</span></span>|<span data-ttu-id="80941-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="80941-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="80941-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="80941-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="80941-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="80941-116">Request headers</span></span>
|<span data-ttu-id="80941-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80941-117">Header</span></span>|<span data-ttu-id="80941-118">Valor</span><span class="sxs-lookup"><span data-stu-id="80941-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="80941-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="80941-119">Authorization</span></span>|<span data-ttu-id="80941-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="80941-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="80941-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="80941-121">Accept</span></span>|<span data-ttu-id="80941-122">aplicación/json</span><span class="sxs-lookup"><span data-stu-id="80941-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="80941-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="80941-123">Request body</span></span>
<span data-ttu-id="80941-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsUpdateForBusinessConfiguration.</span><span class="sxs-lookup"><span data-stu-id="80941-124">In the request body, supply a JSON representation for the windowsUpdateForBusinessConfiguration object.</span></span>

<span data-ttu-id="80941-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsUpdateForBusinessConfiguration.</span><span class="sxs-lookup"><span data-stu-id="80941-125">The following table shows the properties that are required when you create the windowsUpdateForBusinessConfiguration.</span></span>

|<span data-ttu-id="80941-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="80941-126">Property</span></span>|<span data-ttu-id="80941-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="80941-127">Type</span></span>|<span data-ttu-id="80941-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="80941-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="80941-129">id</span><span class="sxs-lookup"><span data-stu-id="80941-129">id</span></span>|<span data-ttu-id="80941-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="80941-130">String</span></span>|<span data-ttu-id="80941-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="80941-131">Key of the entity.</span></span> <span data-ttu-id="80941-132">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="80941-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="80941-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="80941-133">lastModifiedDateTime</span></span>|<span data-ttu-id="80941-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="80941-134">DateTimeOffset</span></span>|<span data-ttu-id="80941-135">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="80941-135">DateTime the object was last modified.</span></span> <span data-ttu-id="80941-136">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="80941-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="80941-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="80941-137">createdDateTime</span></span>|<span data-ttu-id="80941-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="80941-138">DateTimeOffset</span></span>|<span data-ttu-id="80941-139">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="80941-139">DateTime the object was created.</span></span> <span data-ttu-id="80941-140">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="80941-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="80941-141">descripción</span><span class="sxs-lookup"><span data-stu-id="80941-141">description</span></span>|<span data-ttu-id="80941-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="80941-142">String</span></span>|<span data-ttu-id="80941-143">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="80941-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="80941-144">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="80941-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="80941-145">displayName</span><span class="sxs-lookup"><span data-stu-id="80941-145">displayName</span></span>|<span data-ttu-id="80941-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="80941-146">String</span></span>|<span data-ttu-id="80941-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="80941-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="80941-148">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="80941-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="80941-149">version</span><span class="sxs-lookup"><span data-stu-id="80941-149">version</span></span>|<span data-ttu-id="80941-150">Int32</span><span class="sxs-lookup"><span data-stu-id="80941-150">Int32</span></span>|<span data-ttu-id="80941-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="80941-151">Version of the device configuration.</span></span> <span data-ttu-id="80941-152">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="80941-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="80941-153">deliveryOptimizationMode</span><span class="sxs-lookup"><span data-stu-id="80941-153">deliveryOptimizationMode</span></span>|[<span data-ttu-id="80941-154">windowsDeliveryOptimizationMode</span><span class="sxs-lookup"><span data-stu-id="80941-154">windowsDeliveryOptimizationMode</span></span>](../resources/intune_deviceconfig_windowsdeliveryoptimizationmode.md)|<span data-ttu-id="80941-p108">Modo de optimización de entrega. Los valores posibles son: `userDefined`, `httpOnly`, `httpWithPeeringNat`, `httpWithPeeringPrivateGroup`, `httpWithInternetPeering`, `simpleDownload` y `bypassMode`.</span><span class="sxs-lookup"><span data-stu-id="80941-p108">Delivery Optimization Mode Possible values are: `userDefined`, `httpOnly`, `httpWithPeeringNat`, `httpWithPeeringPrivateGroup`, `httpWithInternetPeering`, `simpleDownload`, `bypassMode`.</span></span>|
|<span data-ttu-id="80941-157">prereleaseFeatures</span><span class="sxs-lookup"><span data-stu-id="80941-157">prereleaseFeatures</span></span>|[<span data-ttu-id="80941-158">prereleaseFeatures</span><span class="sxs-lookup"><span data-stu-id="80941-158">prereleaseFeatures</span></span>](../resources/intune_deviceconfig_prereleasefeatures.md)|<span data-ttu-id="80941-p109">Las características de prelanzamiento. Los valores posibles son: `userDefined`, `settingsOnly`, `settingsAndExperimentations`, `notAllowed`..</span><span class="sxs-lookup"><span data-stu-id="80941-p109">The pre-release features. The possible values are: `userDefined`, `settingsOnly`, `settingsAndExperimentations`, `notAllowed`.</span></span>|
|<span data-ttu-id="80941-161">automaticUpdateMode</span><span class="sxs-lookup"><span data-stu-id="80941-161">automaticUpdateMode</span></span>|[<span data-ttu-id="80941-162">automaticUpdateMode</span><span class="sxs-lookup"><span data-stu-id="80941-162">automaticUpdateMode</span></span>](../resources/intune_deviceconfig_automaticupdatemode.md)|<span data-ttu-id="80941-p110">Modo de actualización automática. Los valores posibles son: `userDefined`, `notifyDownload`, `autoInstallAtMaintenanceTime`, `autoInstallAndRebootAtMaintenanceTime`, `autoInstallAndRebootAtScheduledTime`, `autoInstallAndRebootWithoutEndUserControl`.</span><span class="sxs-lookup"><span data-stu-id="80941-p110">Automatic update mode. The possible values are: `userDefined`, `notifyDownload`, `autoInstallAtMaintenanceTime`, `autoInstallAndRebootAtMaintenanceTime`, `autoInstallAndRebootAtScheduledTime`, `autoInstallAndRebootWithoutEndUserControl`.</span></span>|
|<span data-ttu-id="80941-165">microsoftUpdateServiceAllowed</span><span class="sxs-lookup"><span data-stu-id="80941-165">microsoftUpdateServiceAllowed</span></span>|<span data-ttu-id="80941-166">Booleano</span><span class="sxs-lookup"><span data-stu-id="80941-166">Boolean</span></span>|<span data-ttu-id="80941-167">Permitir el servicio de Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="80941-167">Allow Microsoft Update Service</span></span>|
|<span data-ttu-id="80941-168">driversExcluded</span><span class="sxs-lookup"><span data-stu-id="80941-168">driversExcluded</span></span>|<span data-ttu-id="80941-169">Booleano</span><span class="sxs-lookup"><span data-stu-id="80941-169">Boolean</span></span>|<span data-ttu-id="80941-170">Excluir controladores de Windows Update</span><span class="sxs-lookup"><span data-stu-id="80941-170">Exclude Windows update Drivers</span></span>|
|<span data-ttu-id="80941-171">installationSchedule</span><span class="sxs-lookup"><span data-stu-id="80941-171">installationSchedule</span></span>|[<span data-ttu-id="80941-172">windowsUpdateInstallScheduleType</span><span class="sxs-lookup"><span data-stu-id="80941-172">windowsUpdateInstallScheduleType</span></span>](../resources/intune_deviceconfig_windowsupdateinstallscheduletype.md)|<span data-ttu-id="80941-173">Programación de instalación</span><span class="sxs-lookup"><span data-stu-id="80941-173">Installation schedule</span></span>|
|<span data-ttu-id="80941-174">qualityUpdatesDeferralPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="80941-174">qualityUpdatesDeferralPeriodInDays</span></span>|<span data-ttu-id="80941-175">Int32</span><span class="sxs-lookup"><span data-stu-id="80941-175">Int32</span></span>|<span data-ttu-id="80941-176">Aplazar actualizaciones de calidad el siguiente número de días</span><span class="sxs-lookup"><span data-stu-id="80941-176">Defer Quality Updates by these many days</span></span>|
|<span data-ttu-id="80941-177">featureUpdatesDeferralPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="80941-177">featureUpdatesDeferralPeriodInDays</span></span>|<span data-ttu-id="80941-178">Int32</span><span class="sxs-lookup"><span data-stu-id="80941-178">Int32</span></span>|<span data-ttu-id="80941-179">Aplazar actualizaciones de características el siguiente número de días</span><span class="sxs-lookup"><span data-stu-id="80941-179">Defer Feature Updates by these many days</span></span>|
|<span data-ttu-id="80941-180">qualityUpdatesPaused</span><span class="sxs-lookup"><span data-stu-id="80941-180">qualityUpdatesPaused</span></span>|<span data-ttu-id="80941-181">Booleano</span><span class="sxs-lookup"><span data-stu-id="80941-181">Boolean</span></span>|<span data-ttu-id="80941-182">Pausar las actualizaciones de calidad</span><span class="sxs-lookup"><span data-stu-id="80941-182">Pause Quality Updates</span></span>|
|<span data-ttu-id="80941-183">featureUpdatesPaused</span><span class="sxs-lookup"><span data-stu-id="80941-183">featureUpdatesPaused</span></span>|<span data-ttu-id="80941-184">Booleano</span><span class="sxs-lookup"><span data-stu-id="80941-184">Boolean</span></span>|<span data-ttu-id="80941-185">Pausar las actualizaciones de características</span><span class="sxs-lookup"><span data-stu-id="80941-185">Pause Feature Updates</span></span>|
|<span data-ttu-id="80941-186">qualityUpdatesPauseExpiryDateTime</span><span class="sxs-lookup"><span data-stu-id="80941-186">qualityUpdatesPauseExpiryDateTime</span></span>|<span data-ttu-id="80941-187">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="80941-187">DateTimeOffset</span></span>|<span data-ttu-id="80941-188">Fecha y hora de expiración de la pausa en las actualizaciones de calidad</span><span class="sxs-lookup"><span data-stu-id="80941-188">Quality Updates Pause Expiry datetime</span></span>|
|<span data-ttu-id="80941-189">featureUpdatesPauseExpiryDateTime</span><span class="sxs-lookup"><span data-stu-id="80941-189">featureUpdatesPauseExpiryDateTime</span></span>|<span data-ttu-id="80941-190">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="80941-190">DateTimeOffset</span></span>|<span data-ttu-id="80941-191">Fecha y hora de expiración del pausado de actualizaciones de características</span><span class="sxs-lookup"><span data-stu-id="80941-191">Feature Updates Pause Expiry datetime</span></span>|
|<span data-ttu-id="80941-192">businessReadyUpdatesOnly</span><span class="sxs-lookup"><span data-stu-id="80941-192">businessReadyUpdatesOnly</span></span>|[<span data-ttu-id="80941-193">windowsUpdateType</span><span class="sxs-lookup"><span data-stu-id="80941-193">windowsUpdateType</span></span>](../resources/intune_deviceconfig_windowsupdatetype.md)|<span data-ttu-id="80941-p111">Determina de qué rama los dispositivos recibirán sus actualizaciones. Los valores posibles son: `userDefined`, `all`, `businessReadyOnly`, `windowsInsiderBuildFast`, `windowsInsiderBuildSlow`, `windowsInsiderBuildRelease`.</span><span class="sxs-lookup"><span data-stu-id="80941-p111">Determines which branch devices will receive their updates from. The possible values are: `userDefined`, `all`, `businessReadyOnly`, `windowsInsiderBuildFast`, `windowsInsiderBuildSlow`, `windowsInsiderBuildRelease`.</span></span>|



## <a name="response"></a><span data-ttu-id="80941-196">Respuesta</span><span class="sxs-lookup"><span data-stu-id="80941-196">Response</span></span>
<span data-ttu-id="80941-197">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsUpdateForBusinessConfiguration](../resources/intune_deviceconfig_windowsupdateforbusinessconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="80941-197">If successful, this method returns a `201 Created` response code and a [windowsUpdateForBusinessConfiguration](../resources/intune_deviceconfig_windowsupdateforbusinessconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="80941-198">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="80941-198">Example</span></span>
### <a name="request"></a><span data-ttu-id="80941-199">Solicitud</span><span class="sxs-lookup"><span data-stu-id="80941-199">Request</span></span>
<span data-ttu-id="80941-200">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="80941-200">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 974

{
  "@odata.type": "#microsoft.graph.windowsUpdateForBusinessConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "deliveryOptimizationMode": "httpOnly",
  "prereleaseFeatures": "settingsOnly",
  "automaticUpdateMode": "notifyDownload",
  "microsoftUpdateServiceAllowed": true,
  "driversExcluded": true,
  "installationSchedule": {
    "@odata.type": "microsoft.graph.windowsUpdateScheduledInstall",
    "scheduledInstallDay": "everyday",
    "scheduledInstallTime": "11:59:31.3170000"
  },
  "qualityUpdatesDeferralPeriodInDays": 2,
  "featureUpdatesDeferralPeriodInDays": 2,
  "qualityUpdatesPaused": true,
  "featureUpdatesPaused": true,
  "qualityUpdatesPauseExpiryDateTime": "2017-01-01T00:00:22.9594683-08:00",
  "featureUpdatesPauseExpiryDateTime": "2016-12-31T23:58:08.068669-08:00",
  "businessReadyUpdatesOnly": "all"
}
```

### <a name="response"></a><span data-ttu-id="80941-201">Respuesta</span><span class="sxs-lookup"><span data-stu-id="80941-201">Response</span></span>
<span data-ttu-id="80941-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="80941-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1082

{
  "@odata.type": "#microsoft.graph.windowsUpdateForBusinessConfiguration",
  "id": "4928dd6a-dd6a-4928-6add-28496add2849",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "deliveryOptimizationMode": "httpOnly",
  "prereleaseFeatures": "settingsOnly",
  "automaticUpdateMode": "notifyDownload",
  "microsoftUpdateServiceAllowed": true,
  "driversExcluded": true,
  "installationSchedule": {
    "@odata.type": "microsoft.graph.windowsUpdateScheduledInstall",
    "scheduledInstallDay": "everyday",
    "scheduledInstallTime": "11:59:31.3170000"
  },
  "qualityUpdatesDeferralPeriodInDays": 2,
  "featureUpdatesDeferralPeriodInDays": 2,
  "qualityUpdatesPaused": true,
  "featureUpdatesPaused": true,
  "qualityUpdatesPauseExpiryDateTime": "2017-01-01T00:00:22.9594683-08:00",
  "featureUpdatesPauseExpiryDateTime": "2016-12-31T23:58:08.068669-08:00",
  "businessReadyUpdatesOnly": "all"
}
```








