# <a name="update-windowsupdateforbusinessconfiguration"></a><span data-ttu-id="066d9-101">Actualizar windowsUpdateForBusinessConfiguration</span><span class="sxs-lookup"><span data-stu-id="066d9-101">Update windowsUpdateForBusinessConfiguration</span></span>

> <span data-ttu-id="066d9-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="066d9-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="066d9-103">Actualice las propiedades de un objeto [windowsUpdateForBusinessConfiguration](../resources/intune_deviceconfig_windowsupdateforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="066d9-103">Update the properties of a [calendar](../resources/intune_deviceconfig_windowsupdateforbusinessconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="066d9-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="066d9-104">Prerequisites</span></span>
<span data-ttu-id="066d9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="066d9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="066d9-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="066d9-107">Permission type</span></span>|<span data-ttu-id="066d9-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="066d9-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="066d9-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="066d9-109">Delegated (work or school account)</span></span>|<span data-ttu-id="066d9-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="066d9-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="066d9-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="066d9-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="066d9-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="066d9-112">Not supported.</span></span>|
|<span data-ttu-id="066d9-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="066d9-113">Application</span></span>|<span data-ttu-id="066d9-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="066d9-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="066d9-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="066d9-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="066d9-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="066d9-116">Request headers</span></span>
|<span data-ttu-id="066d9-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="066d9-117">Header</span></span>|<span data-ttu-id="066d9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="066d9-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="066d9-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="066d9-119">Authorization</span></span>|<span data-ttu-id="066d9-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="066d9-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="066d9-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="066d9-121">Accept</span></span>|<span data-ttu-id="066d9-122">application/json</span><span class="sxs-lookup"><span data-stu-id="066d9-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="066d9-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="066d9-123">Request body</span></span>
<span data-ttu-id="066d9-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsUpdateForBusinessConfiguration](../resources/intune_deviceconfig_windowsupdateforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="066d9-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_deviceconfig_windowsupdateforbusinessconfiguration.md) object.</span></span>

<span data-ttu-id="066d9-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsUpdateForBusinessConfiguration](../resources/intune_deviceconfig_windowsupdateforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="066d9-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="066d9-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="066d9-126">Property</span></span>|<span data-ttu-id="066d9-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="066d9-127">Type</span></span>|<span data-ttu-id="066d9-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="066d9-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="066d9-129">id</span><span class="sxs-lookup"><span data-stu-id="066d9-129">id</span></span>|<span data-ttu-id="066d9-130">String</span><span class="sxs-lookup"><span data-stu-id="066d9-130">String</span></span>|<span data-ttu-id="066d9-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="066d9-131">Key of the setting.</span></span> <span data-ttu-id="066d9-132">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="066d9-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="066d9-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="066d9-133">lastModifiedDateTime</span></span>|<span data-ttu-id="066d9-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="066d9-134">DateTimeOffset</span></span>|<span data-ttu-id="066d9-135">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="066d9-135">Indicates the date the object was last modified.</span></span> <span data-ttu-id="066d9-136">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="066d9-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="066d9-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="066d9-137">createdDateTime</span></span>|<span data-ttu-id="066d9-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="066d9-138">DateTimeOffset</span></span>|<span data-ttu-id="066d9-139">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="066d9-139">DateTime the object was created.</span></span> <span data-ttu-id="066d9-140">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="066d9-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="066d9-141">description</span><span class="sxs-lookup"><span data-stu-id="066d9-141">description</span></span>|<span data-ttu-id="066d9-142">String</span><span class="sxs-lookup"><span data-stu-id="066d9-142">String</span></span>|<span data-ttu-id="066d9-143">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="066d9-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="066d9-144">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="066d9-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="066d9-145">displayName</span><span class="sxs-lookup"><span data-stu-id="066d9-145">displayName</span></span>|<span data-ttu-id="066d9-146">String</span><span class="sxs-lookup"><span data-stu-id="066d9-146">String</span></span>|<span data-ttu-id="066d9-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="066d9-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="066d9-148">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="066d9-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="066d9-149">version</span><span class="sxs-lookup"><span data-stu-id="066d9-149">version</span></span>|<span data-ttu-id="066d9-150">Int32</span><span class="sxs-lookup"><span data-stu-id="066d9-150">Int32</span></span>|<span data-ttu-id="066d9-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="066d9-151">Version of the device configuration.</span></span> <span data-ttu-id="066d9-152">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="066d9-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="066d9-153">deliveryOptimizationMode</span><span class="sxs-lookup"><span data-stu-id="066d9-153">deliveryOptimizationMode</span></span>|<span data-ttu-id="066d9-154">String</span><span class="sxs-lookup"><span data-stu-id="066d9-154">String</span></span>|<span data-ttu-id="066d9-155">Modo de optimización de entrega. Los valores posibles son: `userDefined`, `httpOnly`, `httpWithPeeringNat`, `httpWithPeeringPrivateGroup`, `httpWithInternetPeering`, `simpleDownload` y `bypassMode`.</span><span class="sxs-lookup"><span data-stu-id="066d9-155">Delivery Optimization Mode Possible values are: `userDefined`, `httpOnly`, `httpWithPeeringNat`, `httpWithPeeringPrivateGroup`, `httpWithInternetPeering`, `simpleDownload`, `bypassMode`.</span></span>|
|<span data-ttu-id="066d9-156">prereleaseFeatures</span><span class="sxs-lookup"><span data-stu-id="066d9-156">prereleaseFeatures</span></span>|<span data-ttu-id="066d9-157">String</span><span class="sxs-lookup"><span data-stu-id="066d9-157">String</span></span>|<span data-ttu-id="066d9-158">Características de la versión preliminar.</span><span class="sxs-lookup"><span data-stu-id="066d9-158">The pre-release features.</span></span> <span data-ttu-id="066d9-159">Los valores posibles son: `userDefined`, `settingsOnly`, `settingsAndExperimentations` y `notAllowed`.</span><span class="sxs-lookup"><span data-stu-id="066d9-159">Possible values are: `userDefined`, `settingsOnly`, `settingsAndExperimentations`, `notAllowed`.</span></span>|
|<span data-ttu-id="066d9-160">automaticUpdateMode</span><span class="sxs-lookup"><span data-stu-id="066d9-160">automaticUpdateMode</span></span>|<span data-ttu-id="066d9-161">String</span><span class="sxs-lookup"><span data-stu-id="066d9-161">String</span></span>|<span data-ttu-id="066d9-162">Modo de actualización automático.</span><span class="sxs-lookup"><span data-stu-id="066d9-162">Automatic update mode.</span></span> <span data-ttu-id="066d9-163">Los valores posibles son: `userDefined`, `notifyDownload`, `autoInstallAtMaintenanceTime`, `autoInstallAndRebootAtMaintenanceTime`, `autoInstallAndRebootAtScheduledTime` y `autoInstallAndRebootWithoutEndUserControl`.</span><span class="sxs-lookup"><span data-stu-id="066d9-163">Possible values are: `userDefined`, `notifyDownload`, `autoInstallAtMaintenanceTime`, `autoInstallAndRebootAtMaintenanceTime`, `autoInstallAndRebootAtScheduledTime`, `autoInstallAndRebootWithoutEndUserControl`.</span></span>|
|<span data-ttu-id="066d9-164">microsoftUpdateServiceAllowed</span><span class="sxs-lookup"><span data-stu-id="066d9-164">microsoftUpdateServiceAllowed</span></span>|<span data-ttu-id="066d9-165">Boolean</span><span class="sxs-lookup"><span data-stu-id="066d9-165">Boolean</span></span>|<span data-ttu-id="066d9-166">Permitir el servicio de Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="066d9-166">Allow Microsoft Update Service</span></span>|
|<span data-ttu-id="066d9-167">driversExcluded</span><span class="sxs-lookup"><span data-stu-id="066d9-167">driversExcluded</span></span>|<span data-ttu-id="066d9-168">Boolean</span><span class="sxs-lookup"><span data-stu-id="066d9-168">Boolean</span></span>|<span data-ttu-id="066d9-169">Excluir controladores de Windows Update</span><span class="sxs-lookup"><span data-stu-id="066d9-169">Exclude Windows update Drivers</span></span>|
|<span data-ttu-id="066d9-170">installationSchedule</span><span class="sxs-lookup"><span data-stu-id="066d9-170">installationSchedule</span></span>|[<span data-ttu-id="066d9-171">windowsUpdateInstallScheduleType</span><span class="sxs-lookup"><span data-stu-id="066d9-171">windowsUpdateInstallScheduleType</span></span>](../resources/intune_deviceconfig_windowsupdateinstallscheduletype.md)|<span data-ttu-id="066d9-172">Programación de instalación</span><span class="sxs-lookup"><span data-stu-id="066d9-172">Installation schedule</span></span>|
|<span data-ttu-id="066d9-173">qualityUpdatesDeferralPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="066d9-173">qualityUpdatesDeferralPeriodInDays</span></span>|<span data-ttu-id="066d9-174">Int32</span><span class="sxs-lookup"><span data-stu-id="066d9-174">Int32</span></span>|<span data-ttu-id="066d9-175">Aplazar actualizaciones de calidad el siguiente número de días</span><span class="sxs-lookup"><span data-stu-id="066d9-175">Defer Quality Updates by these many days</span></span>|
|<span data-ttu-id="066d9-176">featureUpdatesDeferralPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="066d9-176">featureUpdatesDeferralPeriodInDays</span></span>|<span data-ttu-id="066d9-177">Int32</span><span class="sxs-lookup"><span data-stu-id="066d9-177">Int32</span></span>|<span data-ttu-id="066d9-178">Aplazar actualizaciones de características el siguiente número de días</span><span class="sxs-lookup"><span data-stu-id="066d9-178">Defer Feature Updates by these many days</span></span>|
|<span data-ttu-id="066d9-179">qualityUpdatesPaused</span><span class="sxs-lookup"><span data-stu-id="066d9-179">qualityUpdatesPaused</span></span>|<span data-ttu-id="066d9-180">Boolean</span><span class="sxs-lookup"><span data-stu-id="066d9-180">Boolean</span></span>|<span data-ttu-id="066d9-181">Pausar las actualizaciones de calidad</span><span class="sxs-lookup"><span data-stu-id="066d9-181">Pause Quality Updates</span></span>|
|<span data-ttu-id="066d9-182">featureUpdatesPaused</span><span class="sxs-lookup"><span data-stu-id="066d9-182">featureUpdatesPaused</span></span>|<span data-ttu-id="066d9-183">Boolean</span><span class="sxs-lookup"><span data-stu-id="066d9-183">Boolean</span></span>|<span data-ttu-id="066d9-184">Pausar las actualizaciones de características</span><span class="sxs-lookup"><span data-stu-id="066d9-184">Pause Feature Updates</span></span>|
|<span data-ttu-id="066d9-185">qualityUpdatesPauseExpiryDateTime</span><span class="sxs-lookup"><span data-stu-id="066d9-185">qualityUpdatesPauseExpiryDateTime</span></span>|<span data-ttu-id="066d9-186">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="066d9-186">DateTimeOffset</span></span>|<span data-ttu-id="066d9-187">Quality Updates Pause Expiry datetime</span><span class="sxs-lookup"><span data-stu-id="066d9-187">Quality Updates Pause Expiry datetime</span></span>|
|<span data-ttu-id="066d9-188">featureUpdatesPauseExpiryDateTime</span><span class="sxs-lookup"><span data-stu-id="066d9-188">featureUpdatesPauseExpiryDateTime</span></span>|<span data-ttu-id="066d9-189">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="066d9-189">DateTimeOffset</span></span>|<span data-ttu-id="066d9-190">Fecha y hora de expiración del pausado de actualizaciones de características</span><span class="sxs-lookup"><span data-stu-id="066d9-190">Feature Updates Pause Expiry datetime</span></span>|
|<span data-ttu-id="066d9-191">businessReadyUpdatesOnly</span><span class="sxs-lookup"><span data-stu-id="066d9-191">businessReadyUpdatesOnly</span></span>|<span data-ttu-id="066d9-192">String</span><span class="sxs-lookup"><span data-stu-id="066d9-192">String</span></span>|<span data-ttu-id="066d9-193">Determina la rama de dispositivos que recibirán las actualizaciones. Los valores posibles son: `userDefined`, `all` y `businessReadyOnly`.</span><span class="sxs-lookup"><span data-stu-id="066d9-193">Determines which branch devices will receive their updates from Possible values are: `userDefined`, `all`, `businessReadyOnly`.</span></span>|



## <a name="response"></a><span data-ttu-id="066d9-194">Respuesta</span><span class="sxs-lookup"><span data-stu-id="066d9-194">Response</span></span>
<span data-ttu-id="066d9-195">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsUpdateForBusinessConfiguration](../resources/intune_deviceconfig_windowsupdateforbusinessconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="066d9-195">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_deviceconfig_windowsupdateforbusinessconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="066d9-196">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="066d9-196">Example</span></span>
### <a name="request"></a><span data-ttu-id="066d9-197">Solicitud</span><span class="sxs-lookup"><span data-stu-id="066d9-197">Request</span></span>
<span data-ttu-id="066d9-198">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="066d9-198">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 898

{
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

### <a name="response"></a><span data-ttu-id="066d9-199">Respuesta</span><span class="sxs-lookup"><span data-stu-id="066d9-199">Response</span></span>
<span data-ttu-id="066d9-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="066d9-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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



