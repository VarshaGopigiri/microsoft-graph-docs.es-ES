# <a name="create-windowsupdateforbusinessconfiguration"></a><span data-ttu-id="0aa6e-101">Crear windowsUpdateForBusinessConfiguration</span><span class="sxs-lookup"><span data-stu-id="0aa6e-101">Create windowsUpdateForBusinessConfiguration</span></span>

> <span data-ttu-id="0aa6e-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0aa6e-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0aa6e-103">Crear un objeto [windowsUpdateForBusinessConfiguration](../resources/intune_deviceconfig_windowsupdateforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="0aa6e-103">Create a new [plannerBucket](../resources/intune_deviceconfig_windowsupdateforbusinessconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0aa6e-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0aa6e-104">Prerequisites</span></span>
<span data-ttu-id="0aa6e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="0aa6e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="0aa6e-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0aa6e-107">Permission type</span></span>|<span data-ttu-id="0aa6e-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0aa6e-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0aa6e-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0aa6e-109">Delegated (work or school account)</span></span>|<span data-ttu-id="0aa6e-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0aa6e-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="0aa6e-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0aa6e-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0aa6e-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0aa6e-112">Not supported.</span></span>|
|<span data-ttu-id="0aa6e-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0aa6e-113">Application</span></span>|<span data-ttu-id="0aa6e-114">No compatible.</span><span class="sxs-lookup"><span data-stu-id="0aa6e-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0aa6e-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0aa6e-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="0aa6e-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0aa6e-116">Request headers</span></span>
|<span data-ttu-id="0aa6e-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0aa6e-117">Header</span></span>|<span data-ttu-id="0aa6e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0aa6e-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0aa6e-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="0aa6e-119">Authorization</span></span>|<span data-ttu-id="0aa6e-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0aa6e-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="0aa6e-121">Accept</span><span class="sxs-lookup"><span data-stu-id="0aa6e-121">Accept</span></span>|<span data-ttu-id="0aa6e-122">application/json</span><span class="sxs-lookup"><span data-stu-id="0aa6e-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0aa6e-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0aa6e-123">Request body</span></span>
<span data-ttu-id="0aa6e-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsUpdateForBusinessConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0aa6e-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="0aa6e-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsUpdateForBusinessConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0aa6e-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="0aa6e-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0aa6e-126">Property</span></span>|<span data-ttu-id="0aa6e-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="0aa6e-127">Type</span></span>|<span data-ttu-id="0aa6e-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="0aa6e-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0aa6e-129">id</span><span class="sxs-lookup"><span data-stu-id="0aa6e-129">id</span></span>|<span data-ttu-id="0aa6e-130">String</span><span class="sxs-lookup"><span data-stu-id="0aa6e-130">String</span></span>|<span data-ttu-id="0aa6e-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="0aa6e-131">Key of the setting.</span></span> <span data-ttu-id="0aa6e-132">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="0aa6e-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0aa6e-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="0aa6e-133">lastModifiedDateTime</span></span>|<span data-ttu-id="0aa6e-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0aa6e-134">DateTimeOffset</span></span>|<span data-ttu-id="0aa6e-135">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="0aa6e-135">Indicates the date the object was last modified.</span></span> <span data-ttu-id="0aa6e-136">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="0aa6e-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0aa6e-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="0aa6e-137">createdDateTime</span></span>|<span data-ttu-id="0aa6e-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0aa6e-138">DateTimeOffset</span></span>|<span data-ttu-id="0aa6e-139">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="0aa6e-139">DateTime the object was created.</span></span> <span data-ttu-id="0aa6e-140">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="0aa6e-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0aa6e-141">description</span><span class="sxs-lookup"><span data-stu-id="0aa6e-141">description</span></span>|<span data-ttu-id="0aa6e-142">String</span><span class="sxs-lookup"><span data-stu-id="0aa6e-142">String</span></span>|<span data-ttu-id="0aa6e-143">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0aa6e-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="0aa6e-144">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="0aa6e-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0aa6e-145">displayName</span><span class="sxs-lookup"><span data-stu-id="0aa6e-145">displayName</span></span>|<span data-ttu-id="0aa6e-146">String</span><span class="sxs-lookup"><span data-stu-id="0aa6e-146">String</span></span>|<span data-ttu-id="0aa6e-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0aa6e-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="0aa6e-148">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="0aa6e-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0aa6e-149">version</span><span class="sxs-lookup"><span data-stu-id="0aa6e-149">version</span></span>|<span data-ttu-id="0aa6e-150">Int32</span><span class="sxs-lookup"><span data-stu-id="0aa6e-150">Int32</span></span>|<span data-ttu-id="0aa6e-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0aa6e-151">Version of the device configuration.</span></span> <span data-ttu-id="0aa6e-152">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="0aa6e-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0aa6e-153">deliveryOptimizationMode</span><span class="sxs-lookup"><span data-stu-id="0aa6e-153">deliveryOptimizationMode</span></span>|<span data-ttu-id="0aa6e-154">String</span><span class="sxs-lookup"><span data-stu-id="0aa6e-154">String</span></span>|<span data-ttu-id="0aa6e-155">Modo de optimización de entrega. Los valores posibles son: `userDefined`, `httpOnly`, `httpWithPeeringNat`, `httpWithPeeringPrivateGroup`, `httpWithInternetPeering`, `simpleDownload` y `bypassMode`.</span><span class="sxs-lookup"><span data-stu-id="0aa6e-155">Delivery Optimization Mode Possible values are: `userDefined`, `httpOnly`, `httpWithPeeringNat`, `httpWithPeeringPrivateGroup`, `httpWithInternetPeering`, `simpleDownload`, `bypassMode`.</span></span>|
|<span data-ttu-id="0aa6e-156">prereleaseFeatures</span><span class="sxs-lookup"><span data-stu-id="0aa6e-156">prereleaseFeatures</span></span>|<span data-ttu-id="0aa6e-157">String</span><span class="sxs-lookup"><span data-stu-id="0aa6e-157">String</span></span>|<span data-ttu-id="0aa6e-158">Características de la versión preliminar.</span><span class="sxs-lookup"><span data-stu-id="0aa6e-158">The pre-release features.</span></span> <span data-ttu-id="0aa6e-159">Los valores posibles son: `userDefined`, `settingsOnly`, `settingsAndExperimentations` y `notAllowed`.</span><span class="sxs-lookup"><span data-stu-id="0aa6e-159">Possible values are: `userDefined`, `settingsOnly`, `settingsAndExperimentations`, `notAllowed`.</span></span>|
|<span data-ttu-id="0aa6e-160">automaticUpdateMode</span><span class="sxs-lookup"><span data-stu-id="0aa6e-160">automaticUpdateMode</span></span>|<span data-ttu-id="0aa6e-161">String</span><span class="sxs-lookup"><span data-stu-id="0aa6e-161">String</span></span>|<span data-ttu-id="0aa6e-162">Modo de actualización automático.</span><span class="sxs-lookup"><span data-stu-id="0aa6e-162">Automatic update mode.</span></span> <span data-ttu-id="0aa6e-163">Los valores posibles son: `userDefined`, `notifyDownload`, `autoInstallAtMaintenanceTime`, `autoInstallAndRebootAtMaintenanceTime`, `autoInstallAndRebootAtScheduledTime` y `autoInstallAndRebootWithoutEndUserControl`.</span><span class="sxs-lookup"><span data-stu-id="0aa6e-163">Possible values are: `userDefined`, `notifyDownload`, `autoInstallAtMaintenanceTime`, `autoInstallAndRebootAtMaintenanceTime`, `autoInstallAndRebootAtScheduledTime`, `autoInstallAndRebootWithoutEndUserControl`.</span></span>|
|<span data-ttu-id="0aa6e-164">microsoftUpdateServiceAllowed</span><span class="sxs-lookup"><span data-stu-id="0aa6e-164">microsoftUpdateServiceAllowed</span></span>|<span data-ttu-id="0aa6e-165">Boolean</span><span class="sxs-lookup"><span data-stu-id="0aa6e-165">Boolean</span></span>|<span data-ttu-id="0aa6e-166">Permitir el servicio de Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="0aa6e-166">Allow Microsoft Update Service</span></span>|
|<span data-ttu-id="0aa6e-167">driversExcluded</span><span class="sxs-lookup"><span data-stu-id="0aa6e-167">driversExcluded</span></span>|<span data-ttu-id="0aa6e-168">Boolean</span><span class="sxs-lookup"><span data-stu-id="0aa6e-168">Boolean</span></span>|<span data-ttu-id="0aa6e-169">Excluir controladores de Windows Update</span><span class="sxs-lookup"><span data-stu-id="0aa6e-169">Exclude Windows update Drivers</span></span>|
|<span data-ttu-id="0aa6e-170">installationSchedule</span><span class="sxs-lookup"><span data-stu-id="0aa6e-170">installationSchedule</span></span>|[<span data-ttu-id="0aa6e-171">windowsUpdateInstallScheduleType</span><span class="sxs-lookup"><span data-stu-id="0aa6e-171">windowsUpdateInstallScheduleType</span></span>](../resources/intune_deviceconfig_windowsupdateinstallscheduletype.md)|<span data-ttu-id="0aa6e-172">Programación de instalación</span><span class="sxs-lookup"><span data-stu-id="0aa6e-172">Installation schedule</span></span>|
|<span data-ttu-id="0aa6e-173">qualityUpdatesDeferralPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="0aa6e-173">qualityUpdatesDeferralPeriodInDays</span></span>|<span data-ttu-id="0aa6e-174">Int32</span><span class="sxs-lookup"><span data-stu-id="0aa6e-174">Int32</span></span>|<span data-ttu-id="0aa6e-175">Aplazar actualizaciones de calidad el siguiente número de días</span><span class="sxs-lookup"><span data-stu-id="0aa6e-175">Defer Quality Updates by these many days</span></span>|
|<span data-ttu-id="0aa6e-176">featureUpdatesDeferralPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="0aa6e-176">featureUpdatesDeferralPeriodInDays</span></span>|<span data-ttu-id="0aa6e-177">Int32</span><span class="sxs-lookup"><span data-stu-id="0aa6e-177">Int32</span></span>|<span data-ttu-id="0aa6e-178">Aplazar actualizaciones de características el siguiente número de días</span><span class="sxs-lookup"><span data-stu-id="0aa6e-178">Defer Feature Updates by these many days</span></span>|
|<span data-ttu-id="0aa6e-179">qualityUpdatesPaused</span><span class="sxs-lookup"><span data-stu-id="0aa6e-179">qualityUpdatesPaused</span></span>|<span data-ttu-id="0aa6e-180">Boolean</span><span class="sxs-lookup"><span data-stu-id="0aa6e-180">Boolean</span></span>|<span data-ttu-id="0aa6e-181">Pausar las actualizaciones de calidad</span><span class="sxs-lookup"><span data-stu-id="0aa6e-181">Pause Quality Updates</span></span>|
|<span data-ttu-id="0aa6e-182">featureUpdatesPaused</span><span class="sxs-lookup"><span data-stu-id="0aa6e-182">featureUpdatesPaused</span></span>|<span data-ttu-id="0aa6e-183">Boolean</span><span class="sxs-lookup"><span data-stu-id="0aa6e-183">Boolean</span></span>|<span data-ttu-id="0aa6e-184">Pausar las actualizaciones de características</span><span class="sxs-lookup"><span data-stu-id="0aa6e-184">Pause Feature Updates</span></span>|
|<span data-ttu-id="0aa6e-185">qualityUpdatesPauseExpiryDateTime</span><span class="sxs-lookup"><span data-stu-id="0aa6e-185">qualityUpdatesPauseExpiryDateTime</span></span>|<span data-ttu-id="0aa6e-186">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0aa6e-186">DateTimeOffset</span></span>|<span data-ttu-id="0aa6e-187">Quality Updates Pause Expiry datetime</span><span class="sxs-lookup"><span data-stu-id="0aa6e-187">Quality Updates Pause Expiry datetime</span></span>|
|<span data-ttu-id="0aa6e-188">featureUpdatesPauseExpiryDateTime</span><span class="sxs-lookup"><span data-stu-id="0aa6e-188">featureUpdatesPauseExpiryDateTime</span></span>|<span data-ttu-id="0aa6e-189">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0aa6e-189">DateTimeOffset</span></span>|<span data-ttu-id="0aa6e-190">Fecha y hora de expiración del pausado de actualizaciones de características</span><span class="sxs-lookup"><span data-stu-id="0aa6e-190">Feature Updates Pause Expiry datetime</span></span>|
|<span data-ttu-id="0aa6e-191">businessReadyUpdatesOnly</span><span class="sxs-lookup"><span data-stu-id="0aa6e-191">businessReadyUpdatesOnly</span></span>|<span data-ttu-id="0aa6e-192">String</span><span class="sxs-lookup"><span data-stu-id="0aa6e-192">String</span></span>|<span data-ttu-id="0aa6e-193">Determina la rama de dispositivos que recibirán las actualizaciones. Los valores posibles son: `userDefined`, `all` y `businessReadyOnly`.</span><span class="sxs-lookup"><span data-stu-id="0aa6e-193">Determines which branch devices will receive their updates from Possible values are: `userDefined`, `all`, `businessReadyOnly`.</span></span>|



## <a name="response"></a><span data-ttu-id="0aa6e-194">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0aa6e-194">Response</span></span>
<span data-ttu-id="0aa6e-195">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsUpdateForBusinessConfiguration](../resources/intune_deviceconfig_windowsupdateforbusinessconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0aa6e-195">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_deviceconfig_windowsupdateforbusinessconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0aa6e-196">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0aa6e-196">Example</span></span>
### <a name="request"></a><span data-ttu-id="0aa6e-197">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0aa6e-197">Request</span></span>
<span data-ttu-id="0aa6e-198">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0aa6e-198">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="0aa6e-199">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0aa6e-199">Response</span></span>
<span data-ttu-id="0aa6e-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0aa6e-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



