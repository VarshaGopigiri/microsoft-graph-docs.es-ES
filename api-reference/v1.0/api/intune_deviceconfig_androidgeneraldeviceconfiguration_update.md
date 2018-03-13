# <a name="update-androidgeneraldeviceconfiguration"></a><span data-ttu-id="85427-101">Actualizar androidGeneralDeviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="85427-101">Update androidGeneralDeviceConfiguration</span></span>

> <span data-ttu-id="85427-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="85427-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="85427-103">Actualice las propiedades de un objeto [androidGeneralDeviceConfiguration](../resources/intune_deviceconfig_androidgeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="85427-103">Update the properties of a [calendar](../resources/intune_deviceconfig_androidgeneraldeviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="85427-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="85427-104">Prerequisites</span></span>
<span data-ttu-id="85427-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="85427-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="85427-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="85427-107">Permission type</span></span>|<span data-ttu-id="85427-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="85427-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="85427-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="85427-109">Delegated (work or school account)</span></span>|<span data-ttu-id="85427-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="85427-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="85427-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="85427-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="85427-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="85427-112">Not supported.</span></span>|
|<span data-ttu-id="85427-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="85427-113">Application</span></span>|<span data-ttu-id="85427-114">No compatible.</span><span class="sxs-lookup"><span data-stu-id="85427-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="85427-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="85427-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="85427-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="85427-116">Request headers</span></span>
|<span data-ttu-id="85427-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85427-117">Header</span></span>|<span data-ttu-id="85427-118">Valor</span><span class="sxs-lookup"><span data-stu-id="85427-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="85427-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="85427-119">Authorization</span></span>|<span data-ttu-id="85427-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="85427-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="85427-121">Accept</span><span class="sxs-lookup"><span data-stu-id="85427-121">Accept</span></span>|<span data-ttu-id="85427-122">application/json</span><span class="sxs-lookup"><span data-stu-id="85427-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="85427-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="85427-123">Request body</span></span>
<span data-ttu-id="85427-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [androidGeneralDeviceConfiguration](../resources/intune_deviceconfig_androidgeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="85427-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_deviceconfig_androidgeneraldeviceconfiguration.md) object.</span></span>

<span data-ttu-id="85427-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [androidGeneralDeviceConfiguration](../resources/intune_deviceconfig_androidgeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="85427-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="85427-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="85427-126">Property</span></span>|<span data-ttu-id="85427-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="85427-127">Type</span></span>|<span data-ttu-id="85427-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="85427-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="85427-129">id</span><span class="sxs-lookup"><span data-stu-id="85427-129">id</span></span>|<span data-ttu-id="85427-130">String</span><span class="sxs-lookup"><span data-stu-id="85427-130">String</span></span>|<span data-ttu-id="85427-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="85427-131">Key of the setting.</span></span> <span data-ttu-id="85427-132">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="85427-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="85427-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="85427-133">lastModifiedDateTime</span></span>|<span data-ttu-id="85427-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="85427-134">DateTimeOffset</span></span>|<span data-ttu-id="85427-135">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="85427-135">Indicates the date the object was last modified.</span></span> <span data-ttu-id="85427-136">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="85427-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="85427-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="85427-137">createdDateTime</span></span>|<span data-ttu-id="85427-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="85427-138">DateTimeOffset</span></span>|<span data-ttu-id="85427-139">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="85427-139">DateTime the object was created.</span></span> <span data-ttu-id="85427-140">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="85427-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="85427-141">description</span><span class="sxs-lookup"><span data-stu-id="85427-141">description</span></span>|<span data-ttu-id="85427-142">String</span><span class="sxs-lookup"><span data-stu-id="85427-142">String</span></span>|<span data-ttu-id="85427-143">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="85427-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="85427-144">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="85427-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="85427-145">displayName</span><span class="sxs-lookup"><span data-stu-id="85427-145">displayName</span></span>|<span data-ttu-id="85427-146">String</span><span class="sxs-lookup"><span data-stu-id="85427-146">String</span></span>|<span data-ttu-id="85427-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="85427-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="85427-148">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="85427-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="85427-149">version</span><span class="sxs-lookup"><span data-stu-id="85427-149">version</span></span>|<span data-ttu-id="85427-150">Int32</span><span class="sxs-lookup"><span data-stu-id="85427-150">Int32</span></span>|<span data-ttu-id="85427-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="85427-151">Version of the device configuration.</span></span> <span data-ttu-id="85427-152">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="85427-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="85427-153">appsBlockClipboardSharing</span><span class="sxs-lookup"><span data-stu-id="85427-153">appsBlockClipboardSharing</span></span>|<span data-ttu-id="85427-154">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-154">Boolean</span></span>|<span data-ttu-id="85427-155">Indica si se va a bloquear el uso compartido del Portapapeles para copiar y pegar entre aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="85427-155">Indicates whether or not to block clipboard sharing to copy and paste between applications.</span></span>|
|<span data-ttu-id="85427-156">appsBlockCopyPaste</span><span class="sxs-lookup"><span data-stu-id="85427-156">appsBlockCopyPaste</span></span>|<span data-ttu-id="85427-157">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-157">Boolean</span></span>|<span data-ttu-id="85427-158">Indica si se va a impedir copiar y pegar en las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="85427-158">Indicates whether or not to block copy and paste within applications.</span></span>|
|<span data-ttu-id="85427-159">appsBlockYouTube</span><span class="sxs-lookup"><span data-stu-id="85427-159">appsBlockYouTube</span></span>|<span data-ttu-id="85427-160">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-160">Boolean</span></span>|<span data-ttu-id="85427-161">Indica si se va a bloquear la aplicación YouTube.</span><span class="sxs-lookup"><span data-stu-id="85427-161">Indicates whether or not to block the YouTube app.</span></span>|
|<span data-ttu-id="85427-162">bluetoothBlocked</span><span class="sxs-lookup"><span data-stu-id="85427-162">bluetoothBlocked</span></span>|<span data-ttu-id="85427-163">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-163">Boolean</span></span>|<span data-ttu-id="85427-164">Indica si se va a bloquear Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="85427-164">Indicates whether or not to block Bluetooth.</span></span>|
|<span data-ttu-id="85427-165">cameraBlocked</span><span class="sxs-lookup"><span data-stu-id="85427-165">cameraBlocked</span></span>|<span data-ttu-id="85427-166">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-166">Boolean</span></span>|<span data-ttu-id="85427-167">Indica si se va a bloquear el uso de la cámara.</span><span class="sxs-lookup"><span data-stu-id="85427-167">Indicates whether or not to block the use of the camera.</span></span>|
|<span data-ttu-id="85427-168">cellularBlockDataRoaming</span><span class="sxs-lookup"><span data-stu-id="85427-168">cellularBlockDataRoaming</span></span>|<span data-ttu-id="85427-169">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-169">Boolean</span></span>|<span data-ttu-id="85427-170">Indica si se va a bloquear la itinerancia de datos.</span><span class="sxs-lookup"><span data-stu-id="85427-170">Indicates whether or not to block data roaming.</span></span>|
|<span data-ttu-id="85427-171">cellularBlockMessaging</span><span class="sxs-lookup"><span data-stu-id="85427-171">cellularBlockMessaging</span></span>|<span data-ttu-id="85427-172">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-172">Boolean</span></span>|<span data-ttu-id="85427-173">Indica si se va a bloquear la mensajería SMS/MMS.</span><span class="sxs-lookup"><span data-stu-id="85427-173">Indicates whether or not to block SMS/MMS messaging.</span></span>|
|<span data-ttu-id="85427-174">cellularBlockVoiceRoaming</span><span class="sxs-lookup"><span data-stu-id="85427-174">cellularBlockVoiceRoaming</span></span>|<span data-ttu-id="85427-175">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-175">Boolean</span></span>|<span data-ttu-id="85427-176">Indica si se va a bloquear la itinerancia de voz.</span><span class="sxs-lookup"><span data-stu-id="85427-176">Indicates whether or not to block voice roaming.</span></span>|
|<span data-ttu-id="85427-177">cellularBlockWiFiTethering</span><span class="sxs-lookup"><span data-stu-id="85427-177">cellularBlockWiFiTethering</span></span>|<span data-ttu-id="85427-178">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-178">Boolean</span></span>|<span data-ttu-id="85427-179">Indica si se va a bloquear la sincronización de tethering Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="85427-179">Indicates whether or not to block syncing Wi-Fi tethering.</span></span>|
|<span data-ttu-id="85427-180">compliantAppsList</span><span class="sxs-lookup"><span data-stu-id="85427-180">compliantAppsList</span></span>|<span data-ttu-id="85427-181">Colección [appListItem](../resources/intune_deviceconfig_applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="85427-181">[appListItem](../resources/intune_deviceconfig_applistitem.md) collection</span></span>|<span data-ttu-id="85427-182">Lista de aplicaciones en el cumplimiento (sea lista de permitidos o de bloqueados, controlado por CompliantAppListType).</span><span class="sxs-lookup"><span data-stu-id="85427-182">List of apps in the compliance (either allow list or block list, controlled by CompliantAppListType).</span></span> <span data-ttu-id="85427-183">Esta colección puede contener un máximo de 10 000 elementos.</span><span class="sxs-lookup"><span data-stu-id="85427-183">This collection can contain a maximum of 10000 elements.</span></span>|
|<span data-ttu-id="85427-184">compliantAppListType</span><span class="sxs-lookup"><span data-stu-id="85427-184">compliantAppListType</span></span>|<span data-ttu-id="85427-185">String</span><span class="sxs-lookup"><span data-stu-id="85427-185">String</span></span>|<span data-ttu-id="85427-186">Tipo de lista que se encuentra en la CompliantAppsList.</span><span class="sxs-lookup"><span data-stu-id="85427-186">Type of list that is in the CompliantAppsList.</span></span> <span data-ttu-id="85427-187">Los valores posibles son: `none`, `appsInListCompliant` y `appsNotInListCompliant`.</span><span class="sxs-lookup"><span data-stu-id="85427-187">Possible values are: `none`, `appsInListCompliant`, `appsNotInListCompliant`.</span></span>|
|<span data-ttu-id="85427-188">diagnosticDataBlockSubmission</span><span class="sxs-lookup"><span data-stu-id="85427-188">diagnosticDataBlockSubmission</span></span>|<span data-ttu-id="85427-189">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-189">Boolean</span></span>|<span data-ttu-id="85427-190">Indica si se va a bloquear el envío de datos de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="85427-190">Indicates whether or not to block diagnostic data submission.</span></span>|
|<span data-ttu-id="85427-191">locationServicesBlocked</span><span class="sxs-lookup"><span data-stu-id="85427-191">locationServicesBlocked</span></span>|<span data-ttu-id="85427-192">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-192">Boolean</span></span>|<span data-ttu-id="85427-193">Indica si se van a bloquear los servicios de ubicación.</span><span class="sxs-lookup"><span data-stu-id="85427-193">Indicates whether or not to block location services.</span></span>|
|<span data-ttu-id="85427-194">googleAccountBlockAutoSync</span><span class="sxs-lookup"><span data-stu-id="85427-194">googleAccountBlockAutoSync</span></span>|<span data-ttu-id="85427-195">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-195">Boolean</span></span>|<span data-ttu-id="85427-196">Indica si se va a bloquear la sincronización automática de cuentas de Google.</span><span class="sxs-lookup"><span data-stu-id="85427-196">Indicates whether or not to block Google account auto sync.</span></span>|
|<span data-ttu-id="85427-197">googlePlayStoreBlocked</span><span class="sxs-lookup"><span data-stu-id="85427-197">googlePlayStoreBlocked</span></span>|<span data-ttu-id="85427-198">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-198">Boolean</span></span>|<span data-ttu-id="85427-199">Indica si se va a bloquear la aplicación Google Play Store.</span><span class="sxs-lookup"><span data-stu-id="85427-199">Indicates whether or not to block the Google Play store.</span></span>|
|<span data-ttu-id="85427-200">kioskModeBlockSleepButton</span><span class="sxs-lookup"><span data-stu-id="85427-200">kioskModeBlockSleepButton</span></span>|<span data-ttu-id="85427-201">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-201">Boolean</span></span>|<span data-ttu-id="85427-202">Indica si se va a bloquear el botón de suspensión de pantalla durante el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="85427-202">Indicates whether or not to block the screen sleep button while in Kiosk Mode.</span></span>|
|<span data-ttu-id="85427-203">kioskModeBlockVolumeButtons</span><span class="sxs-lookup"><span data-stu-id="85427-203">kioskModeBlockVolumeButtons</span></span>|<span data-ttu-id="85427-204">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-204">Boolean</span></span>|<span data-ttu-id="85427-205">Indica si se van a bloquear los botones de volumen durante el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="85427-205">Indicates whether or not to block the volume buttons while in Kiosk Mode.</span></span>|
|<span data-ttu-id="85427-206">kioskModeApps</span><span class="sxs-lookup"><span data-stu-id="85427-206">kioskModeApps</span></span>|<span data-ttu-id="85427-207">Colección [appListItem](../resources/intune_deviceconfig_applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="85427-207">[appListItem](../resources/intune_deviceconfig_applistitem.md) collection</span></span>|<span data-ttu-id="85427-208">Lista de aplicaciones que se podrán ejecutar cuando el dispositivo esté en modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="85427-208">A list of apps that will be allowed to run when the device is in Kiosk Mode.</span></span> <span data-ttu-id="85427-209">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="85427-209">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="85427-210">nfcBlocked</span><span class="sxs-lookup"><span data-stu-id="85427-210">nfcBlocked</span></span>|<span data-ttu-id="85427-211">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-211">Boolean</span></span>|<span data-ttu-id="85427-212">Indica si se va a bloquear la transmisión de datos en proximidad.</span><span class="sxs-lookup"><span data-stu-id="85427-212">Indicates whether or not to block Near-Field Communication.</span></span>|
|<span data-ttu-id="85427-213">passwordBlockFingerprintUnlock</span><span class="sxs-lookup"><span data-stu-id="85427-213">passwordBlockFingerprintUnlock</span></span>|<span data-ttu-id="85427-214">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-214">Boolean</span></span>|<span data-ttu-id="85427-215">Indica si se va a impedir el desbloqueo por huella digital.</span><span class="sxs-lookup"><span data-stu-id="85427-215">Indicates whether or not to block fingerprint unlock.</span></span>|
|<span data-ttu-id="85427-216">passwordBlockTrustAgents</span><span class="sxs-lookup"><span data-stu-id="85427-216">passwordBlockTrustAgents</span></span>|<span data-ttu-id="85427-217">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-217">Boolean</span></span>|<span data-ttu-id="85427-218">Indica si se van a bloquear Smart Lock y otros agentes de confianza.</span><span class="sxs-lookup"><span data-stu-id="85427-218">Indicates whether or not to block Smart Lock and other trust agents.</span></span>|
|<span data-ttu-id="85427-219">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="85427-219">passwordExpirationDays</span></span>|<span data-ttu-id="85427-220">Int32</span><span class="sxs-lookup"><span data-stu-id="85427-220">Int32</span></span>|<span data-ttu-id="85427-221">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="85427-221">Number of days before the password expires.</span></span> <span data-ttu-id="85427-222">Valores válidos de 1 a 365.</span><span class="sxs-lookup"><span data-stu-id="85427-222">Valid values 1 to 365</span></span>|
|<span data-ttu-id="85427-223">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="85427-223">passwordMinimumLength</span></span>|<span data-ttu-id="85427-224">Int32</span><span class="sxs-lookup"><span data-stu-id="85427-224">Int32</span></span>|<span data-ttu-id="85427-225">Longitud mínima de las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="85427-225">Minimum length of passwords.</span></span> <span data-ttu-id="85427-226">Valores válidos de 4 a 16.</span><span class="sxs-lookup"><span data-stu-id="85427-226">Valid values 4 to 16</span></span>|
|<span data-ttu-id="85427-227">passwordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="85427-227">passwordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="85427-228">Int32</span><span class="sxs-lookup"><span data-stu-id="85427-228">Int32</span></span>|<span data-ttu-id="85427-229">Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="85427-229">Minutes of inactivity before the screen times out.</span></span>|
|<span data-ttu-id="85427-230">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="85427-230">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="85427-231">Int32</span><span class="sxs-lookup"><span data-stu-id="85427-231">Int32</span></span>|<span data-ttu-id="85427-232">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="85427-232">Number of previous passwords to block.</span></span> <span data-ttu-id="85427-233">Valores válidos de 0 a 24.</span><span class="sxs-lookup"><span data-stu-id="85427-233">Valid values 0 to 24</span></span>|
|<span data-ttu-id="85427-234">passwordSignInFailureCountBeforeFactoryReset</span><span class="sxs-lookup"><span data-stu-id="85427-234">passwordSignInFailureCountBeforeFactoryReset</span></span>|<span data-ttu-id="85427-235">Int32</span><span class="sxs-lookup"><span data-stu-id="85427-235">Int32</span></span>|<span data-ttu-id="85427-236">Número de errores de inicio de sesión permitidos antes del restablecimiento de fábrica.</span><span class="sxs-lookup"><span data-stu-id="85427-236">Number of sign in failures allowed before factory reset.</span></span> <span data-ttu-id="85427-237">Valores válidos de 4 a 11.</span><span class="sxs-lookup"><span data-stu-id="85427-237">Valid values 4 to 11</span></span>|
|<span data-ttu-id="85427-238">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="85427-238">passwordRequiredType</span></span>|<span data-ttu-id="85427-239">String</span><span class="sxs-lookup"><span data-stu-id="85427-239">String</span></span>|<span data-ttu-id="85427-240">Tipo de contraseña que es necesario.</span><span class="sxs-lookup"><span data-stu-id="85427-240">Type of password that is required.</span></span> <span data-ttu-id="85427-241">Los valores posibles son: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex` y `any`.</span><span class="sxs-lookup"><span data-stu-id="85427-241">Possible values are: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex`.</span></span>|
|<span data-ttu-id="85427-242">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="85427-242">passwordRequired</span></span>|<span data-ttu-id="85427-243">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-243">Boolean</span></span>|<span data-ttu-id="85427-244">Indica si se va a requerir una contraseña.</span><span class="sxs-lookup"><span data-stu-id="85427-244">Indicates whether or not to require a password.</span></span>|
|<span data-ttu-id="85427-245">powerOffBlocked</span><span class="sxs-lookup"><span data-stu-id="85427-245">powerOffBlocked</span></span>|<span data-ttu-id="85427-246">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-246">Boolean</span></span>|<span data-ttu-id="85427-247">Indica si se va a bloquear el apagado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="85427-247">Indicates whether or not to block powering off the device.</span></span>|
|<span data-ttu-id="85427-248">factoryResetBlocked</span><span class="sxs-lookup"><span data-stu-id="85427-248">factoryResetBlocked</span></span>|<span data-ttu-id="85427-249">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-249">Boolean</span></span>|<span data-ttu-id="85427-250">Indica si se va a impedir que el usuario realice un restablecimiento de fábrica.</span><span class="sxs-lookup"><span data-stu-id="85427-250">Indicates whether or not to block user performing a factory reset.</span></span>|
|<span data-ttu-id="85427-251">screenCaptureBlocked</span><span class="sxs-lookup"><span data-stu-id="85427-251">screenCaptureBlocked</span></span>|<span data-ttu-id="85427-252">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-252">Boolean</span></span>|<span data-ttu-id="85427-253">Indica si se van a impedir las capturas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="85427-253">Indicates whether or not to block screenshots.</span></span>|
|<span data-ttu-id="85427-254">deviceSharingAllowed</span><span class="sxs-lookup"><span data-stu-id="85427-254">deviceSharingAllowed</span></span>|<span data-ttu-id="85427-255">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-255">Boolean</span></span>|<span data-ttu-id="85427-256">Indica si se va a permitir el modo de uso compartido del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="85427-256">Indicates whether or not to allow device sharing mode.</span></span>|
|<span data-ttu-id="85427-257">storageBlockGoogleBackup</span><span class="sxs-lookup"><span data-stu-id="85427-257">storageBlockGoogleBackup</span></span>|<span data-ttu-id="85427-258">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-258">Boolean</span></span>|<span data-ttu-id="85427-259">Indica si se va a bloquear Google Backup.</span><span class="sxs-lookup"><span data-stu-id="85427-259">Indicates whether or not to block Google Backup.</span></span>|
|<span data-ttu-id="85427-260">storageBlockRemovableStorage</span><span class="sxs-lookup"><span data-stu-id="85427-260">storageBlockRemovableStorage</span></span>|<span data-ttu-id="85427-261">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-261">Boolean</span></span>|<span data-ttu-id="85427-262">Indica si se va a bloquear el uso de almacenamiento extraíble.</span><span class="sxs-lookup"><span data-stu-id="85427-262">Indicates whether or not to block removable storage usage.</span></span>|
|<span data-ttu-id="85427-263">storageRequireDeviceEncryption</span><span class="sxs-lookup"><span data-stu-id="85427-263">storageRequireDeviceEncryption</span></span>|<span data-ttu-id="85427-264">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-264">Boolean</span></span>|<span data-ttu-id="85427-265">Indica si se va a requerir cifrado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="85427-265">Indicates whether or not to require device encryption.</span></span>|
|<span data-ttu-id="85427-266">storageRequireRemovableStorageEncryption</span><span class="sxs-lookup"><span data-stu-id="85427-266">storageRequireRemovableStorageEncryption</span></span>|<span data-ttu-id="85427-267">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-267">Boolean</span></span>|<span data-ttu-id="85427-268">Indica si se va a requerir cifrado del almacenamiento extraíble.</span><span class="sxs-lookup"><span data-stu-id="85427-268">Indicates whether or not to require removable storage encryption.</span></span>|
|<span data-ttu-id="85427-269">voiceAssistantBlocked</span><span class="sxs-lookup"><span data-stu-id="85427-269">voiceAssistantBlocked</span></span>|<span data-ttu-id="85427-270">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-270">Boolean</span></span>|<span data-ttu-id="85427-271">Indica si se va a bloquear el uso del asistente de voz.</span><span class="sxs-lookup"><span data-stu-id="85427-271">Indicates whether or not to block the use of the Voice Assistant.</span></span>|
|<span data-ttu-id="85427-272">voiceDialingBlocked</span><span class="sxs-lookup"><span data-stu-id="85427-272">voiceDialingBlocked</span></span>|<span data-ttu-id="85427-273">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-273">Boolean</span></span>|<span data-ttu-id="85427-274">Indica si se va a bloquear la marcación por voz.</span><span class="sxs-lookup"><span data-stu-id="85427-274">Indicates whether or not to block voice dialing.</span></span>|
|<span data-ttu-id="85427-275">webBrowserBlockPopups</span><span class="sxs-lookup"><span data-stu-id="85427-275">webBrowserBlockPopups</span></span>|<span data-ttu-id="85427-276">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-276">Boolean</span></span>|<span data-ttu-id="85427-277">Indica si se van a bloquear los elementos emergentes en el explorador web.</span><span class="sxs-lookup"><span data-stu-id="85427-277">Indicates whether or not to block popups within the web browser.</span></span>|
|<span data-ttu-id="85427-278">webBrowserBlockAutofill</span><span class="sxs-lookup"><span data-stu-id="85427-278">webBrowserBlockAutofill</span></span>|<span data-ttu-id="85427-279">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-279">Boolean</span></span>|<span data-ttu-id="85427-280">Indica si se va a bloquear la característica de autorrellenado del explorador web.</span><span class="sxs-lookup"><span data-stu-id="85427-280">Indicates whether or not to block the web browser's auto fill feature.</span></span>|
|<span data-ttu-id="85427-281">webBrowserBlockJavaScript</span><span class="sxs-lookup"><span data-stu-id="85427-281">webBrowserBlockJavaScript</span></span>|<span data-ttu-id="85427-282">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-282">Boolean</span></span>|<span data-ttu-id="85427-283">Indica si se va a bloquear JavaScript en el explorador web.</span><span class="sxs-lookup"><span data-stu-id="85427-283">Indicates whether or not to block JavaScript within the web browser.</span></span>|
|<span data-ttu-id="85427-284">webBrowserBlocked</span><span class="sxs-lookup"><span data-stu-id="85427-284">webBrowserBlocked</span></span>|<span data-ttu-id="85427-285">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-285">Boolean</span></span>|<span data-ttu-id="85427-286">Indica si se va a bloquear el explorador web.</span><span class="sxs-lookup"><span data-stu-id="85427-286">Indicates whether or not to block the web browser.</span></span>|
|<span data-ttu-id="85427-287">webBrowserCookieSettings</span><span class="sxs-lookup"><span data-stu-id="85427-287">webBrowserCookieSettings</span></span>|<span data-ttu-id="85427-288">String</span><span class="sxs-lookup"><span data-stu-id="85427-288">String</span></span>|<span data-ttu-id="85427-289">Configuración de cookies en el explorador web.</span><span class="sxs-lookup"><span data-stu-id="85427-289">Cookie settings within the web browser.</span></span> <span data-ttu-id="85427-290">Los valores posibles son: `browserDefault`, `blockAlways`, `allowCurrentWebSite`, `allowFromWebsitesVisited` y `allowAlways`.</span><span class="sxs-lookup"><span data-stu-id="85427-290">Possible values are: `browserDefault`, `blockAlways`, `allowCurrentWebSite`, `allowFromWebsitesVisited`, `allowAlways`.</span></span>|
|<span data-ttu-id="85427-291">wiFiBlocked</span><span class="sxs-lookup"><span data-stu-id="85427-291">wiFiBlocked</span></span>|<span data-ttu-id="85427-292">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-292">Boolean</span></span>|<span data-ttu-id="85427-293">Indica si se va a bloquear la sincronización de Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="85427-293">Indicates whether or not to block syncing Wi-Fi.</span></span>|
|<span data-ttu-id="85427-294">appsInstallAllowList</span><span class="sxs-lookup"><span data-stu-id="85427-294">appsInstallAllowList</span></span>|<span data-ttu-id="85427-295">Colección [appListItem](../resources/intune_deviceconfig_applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="85427-295">[appListItem](../resources/intune_deviceconfig_applistitem.md) collection</span></span>|<span data-ttu-id="85427-296">Lista de aplicaciones que se pueden instalar en el dispositivo KNOX.</span><span class="sxs-lookup"><span data-stu-id="85427-296">List of apps which can be installed on the KNOX device.</span></span> <span data-ttu-id="85427-297">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="85427-297">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="85427-298">appsLaunchBlockList</span><span class="sxs-lookup"><span data-stu-id="85427-298">appsLaunchBlockList</span></span>|<span data-ttu-id="85427-299">Colección [appListItem](../resources/intune_deviceconfig_applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="85427-299">[appListItem](../resources/intune_deviceconfig_applistitem.md) collection</span></span>|<span data-ttu-id="85427-300">Lista de aplicaciones cuyo inicio en el dispositivo KNOX está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="85427-300">List of apps which are blocked from being launched on the KNOX device.</span></span> <span data-ttu-id="85427-301">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="85427-301">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="85427-302">appsHideList</span><span class="sxs-lookup"><span data-stu-id="85427-302">appsHideList</span></span>|<span data-ttu-id="85427-303">Colección [appListItem](../resources/intune_deviceconfig_applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="85427-303">[appListItem](../resources/intune_deviceconfig_applistitem.md) collection</span></span>|<span data-ttu-id="85427-304">Lista de aplicaciones que se ocultarán en el dispositivo KNOX.</span><span class="sxs-lookup"><span data-stu-id="85427-304">List of apps to be hidden on the KNOX device.</span></span> <span data-ttu-id="85427-305">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="85427-305">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="85427-306">securityRequireVerifyApps</span><span class="sxs-lookup"><span data-stu-id="85427-306">securityRequireVerifyApps</span></span>|<span data-ttu-id="85427-307">Boolean</span><span class="sxs-lookup"><span data-stu-id="85427-307">Boolean</span></span>|<span data-ttu-id="85427-308">Requerir que la característica Verificar aplicaciones de Android esté activada.</span><span class="sxs-lookup"><span data-stu-id="85427-308">Require the Android Verify apps feature is turned on.</span></span>|



## <a name="response"></a><span data-ttu-id="85427-309">Respuesta</span><span class="sxs-lookup"><span data-stu-id="85427-309">Response</span></span>
<span data-ttu-id="85427-310">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidGeneralDeviceConfiguration](../resources/intune_deviceconfig_androidgeneraldeviceconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="85427-310">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_deviceconfig_androidgeneraldeviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="85427-311">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="85427-311">Example</span></span>
### <a name="request"></a><span data-ttu-id="85427-312">Solicitud</span><span class="sxs-lookup"><span data-stu-id="85427-312">Request</span></span>
<span data-ttu-id="85427-313">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="85427-313">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 3025

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "appsBlockClipboardSharing": true,
  "appsBlockCopyPaste": true,
  "appsBlockYouTube": true,
  "bluetoothBlocked": true,
  "cameraBlocked": true,
  "cellularBlockDataRoaming": true,
  "cellularBlockMessaging": true,
  "cellularBlockVoiceRoaming": true,
  "cellularBlockWiFiTethering": true,
  "compliantAppsList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "compliantAppListType": "appsInListCompliant",
  "diagnosticDataBlockSubmission": true,
  "locationServicesBlocked": true,
  "googleAccountBlockAutoSync": true,
  "googlePlayStoreBlocked": true,
  "kioskModeBlockSleepButton": true,
  "kioskModeBlockVolumeButtons": true,
  "kioskModeApps": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "nfcBlocked": true,
  "passwordBlockFingerprintUnlock": true,
  "passwordBlockTrustAgents": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordSignInFailureCountBeforeFactoryReset": 12,
  "passwordRequiredType": "alphabetic",
  "passwordRequired": true,
  "powerOffBlocked": true,
  "factoryResetBlocked": true,
  "screenCaptureBlocked": true,
  "deviceSharingAllowed": true,
  "storageBlockGoogleBackup": true,
  "storageBlockRemovableStorage": true,
  "storageRequireDeviceEncryption": true,
  "storageRequireRemovableStorageEncryption": true,
  "voiceAssistantBlocked": true,
  "voiceDialingBlocked": true,
  "webBrowserBlockPopups": true,
  "webBrowserBlockAutofill": true,
  "webBrowserBlockJavaScript": true,
  "webBrowserBlocked": true,
  "webBrowserCookieSettings": "blockAlways",
  "wiFiBlocked": true,
  "appsInstallAllowList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "appsLaunchBlockList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "appsHideList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "securityRequireVerifyApps": true
}
```

### <a name="response"></a><span data-ttu-id="85427-314">Respuesta</span><span class="sxs-lookup"><span data-stu-id="85427-314">Response</span></span>
<span data-ttu-id="85427-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="85427-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 3205

{
  "@odata.type": "#microsoft.graph.androidGeneralDeviceConfiguration",
  "id": "9e00d534-d534-9e00-34d5-009e34d5009e",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "appsBlockClipboardSharing": true,
  "appsBlockCopyPaste": true,
  "appsBlockYouTube": true,
  "bluetoothBlocked": true,
  "cameraBlocked": true,
  "cellularBlockDataRoaming": true,
  "cellularBlockMessaging": true,
  "cellularBlockVoiceRoaming": true,
  "cellularBlockWiFiTethering": true,
  "compliantAppsList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "compliantAppListType": "appsInListCompliant",
  "diagnosticDataBlockSubmission": true,
  "locationServicesBlocked": true,
  "googleAccountBlockAutoSync": true,
  "googlePlayStoreBlocked": true,
  "kioskModeBlockSleepButton": true,
  "kioskModeBlockVolumeButtons": true,
  "kioskModeApps": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "nfcBlocked": true,
  "passwordBlockFingerprintUnlock": true,
  "passwordBlockTrustAgents": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordSignInFailureCountBeforeFactoryReset": 12,
  "passwordRequiredType": "alphabetic",
  "passwordRequired": true,
  "powerOffBlocked": true,
  "factoryResetBlocked": true,
  "screenCaptureBlocked": true,
  "deviceSharingAllowed": true,
  "storageBlockGoogleBackup": true,
  "storageBlockRemovableStorage": true,
  "storageRequireDeviceEncryption": true,
  "storageRequireRemovableStorageEncryption": true,
  "voiceAssistantBlocked": true,
  "voiceDialingBlocked": true,
  "webBrowserBlockPopups": true,
  "webBrowserBlockAutofill": true,
  "webBrowserBlockJavaScript": true,
  "webBrowserBlocked": true,
  "webBrowserCookieSettings": "blockAlways",
  "wiFiBlocked": true,
  "appsInstallAllowList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "appsLaunchBlockList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "appsHideList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "securityRequireVerifyApps": true
}
```



