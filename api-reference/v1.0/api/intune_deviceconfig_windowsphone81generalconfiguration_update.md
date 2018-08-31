# <a name="update-windowsphone81generalconfiguration"></a><span data-ttu-id="19aa4-101">Actualizar windowsPhone81GeneralConfiguration</span><span class="sxs-lookup"><span data-stu-id="19aa4-101">Update windowsPhone81GeneralConfiguration</span></span>

> <span data-ttu-id="19aa4-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="19aa4-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="19aa4-103">Actualice las propiedades de un objeto [windowsPhone81GeneralConfiguration](../resources/intune_deviceconfig_windowsphone81generalconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="19aa4-103">Update the properties of a [windowsPhone81GeneralConfiguration](../resources/intune_deviceconfig_windowsphone81generalconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="19aa4-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="19aa4-104">Prerequisites</span></span>
<span data-ttu-id="19aa4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="19aa4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="19aa4-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="19aa4-107">Permission type</span></span>|<span data-ttu-id="19aa4-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="19aa4-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="19aa4-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="19aa4-109">Delegated (work or school account)</span></span>|<span data-ttu-id="19aa4-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="19aa4-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="19aa4-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="19aa4-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="19aa4-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="19aa4-112">Not supported.</span></span>|
|<span data-ttu-id="19aa4-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="19aa4-113">Application</span></span>|<span data-ttu-id="19aa4-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="19aa4-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="19aa4-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="19aa4-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="19aa4-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="19aa4-116">Request headers</span></span>
|<span data-ttu-id="19aa4-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="19aa4-117">Header</span></span>|<span data-ttu-id="19aa4-118">Valor</span><span class="sxs-lookup"><span data-stu-id="19aa4-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="19aa4-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="19aa4-119">Authorization</span></span>|<span data-ttu-id="19aa4-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="19aa4-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="19aa4-121">Accept</span><span class="sxs-lookup"><span data-stu-id="19aa4-121">Accept</span></span>|<span data-ttu-id="19aa4-122">application/json</span><span class="sxs-lookup"><span data-stu-id="19aa4-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="19aa4-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="19aa4-123">Request body</span></span>
<span data-ttu-id="19aa4-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsPhone81GeneralConfiguration](../resources/intune_deviceconfig_windowsphone81generalconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="19aa4-124">In the request body, supply a JSON representation for the [windowsPhone81GeneralConfiguration](../resources/intune_deviceconfig_windowsphone81generalconfiguration.md) object.</span></span>

<span data-ttu-id="19aa4-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsPhone81GeneralConfiguration](../resources/intune_deviceconfig_windowsphone81generalconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="19aa4-125">The following table shows the properties that are required when you create the [windowsPhone81GeneralConfiguration](../resources/intune_deviceconfig_windowsphone81generalconfiguration.md).</span></span>

|<span data-ttu-id="19aa4-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="19aa4-126">Property</span></span>|<span data-ttu-id="19aa4-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="19aa4-127">Type</span></span>|<span data-ttu-id="19aa4-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="19aa4-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="19aa4-129">id</span><span class="sxs-lookup"><span data-stu-id="19aa4-129">id</span></span>|<span data-ttu-id="19aa4-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="19aa4-130">String</span></span>|<span data-ttu-id="19aa4-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="19aa4-131">Key of the entity.</span></span> <span data-ttu-id="19aa4-132">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="19aa4-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="19aa4-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="19aa4-133">lastModifiedDateTime</span></span>|<span data-ttu-id="19aa4-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="19aa4-134">DateTimeOffset</span></span>|<span data-ttu-id="19aa4-135">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="19aa4-135">DateTime the object was last modified.</span></span> <span data-ttu-id="19aa4-136">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="19aa4-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="19aa4-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="19aa4-137">createdDateTime</span></span>|<span data-ttu-id="19aa4-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="19aa4-138">DateTimeOffset</span></span>|<span data-ttu-id="19aa4-139">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="19aa4-139">DateTime the object was created.</span></span> <span data-ttu-id="19aa4-140">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="19aa4-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="19aa4-141">description</span><span class="sxs-lookup"><span data-stu-id="19aa4-141">description</span></span>|<span data-ttu-id="19aa4-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="19aa4-142">String</span></span>|<span data-ttu-id="19aa4-143">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19aa4-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="19aa4-144">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="19aa4-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="19aa4-145">displayName</span><span class="sxs-lookup"><span data-stu-id="19aa4-145">displayName</span></span>|<span data-ttu-id="19aa4-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="19aa4-146">String</span></span>|<span data-ttu-id="19aa4-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19aa4-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="19aa4-148">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="19aa4-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="19aa4-149">version</span><span class="sxs-lookup"><span data-stu-id="19aa4-149">version</span></span>|<span data-ttu-id="19aa4-150">Int32</span><span class="sxs-lookup"><span data-stu-id="19aa4-150">Int32</span></span>|<span data-ttu-id="19aa4-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19aa4-151">Version of the device configuration.</span></span> <span data-ttu-id="19aa4-152">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="19aa4-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="19aa4-153">applyOnlyToWindowsPhone81</span><span class="sxs-lookup"><span data-stu-id="19aa4-153">applyOnlyToWindowsPhone81</span></span>|<span data-ttu-id="19aa4-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="19aa4-154">Boolean</span></span>|<span data-ttu-id="19aa4-155">Valor que indica si esta directiva se aplica solo a Windows Phone 8.1.</span><span class="sxs-lookup"><span data-stu-id="19aa4-155">Value indicating whether this policy only applies to Windows Phone 8.1.</span></span> <span data-ttu-id="19aa4-156">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="19aa4-156">This property is read-only.</span></span>|
|<span data-ttu-id="19aa4-157">appsBlockCopyPaste</span><span class="sxs-lookup"><span data-stu-id="19aa4-157">appsBlockCopyPaste</span></span>|<span data-ttu-id="19aa4-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="19aa4-158">Boolean</span></span>|<span data-ttu-id="19aa4-159">Indica si se va a impedir cortar y pegar.</span><span class="sxs-lookup"><span data-stu-id="19aa4-159">Indicates whether or not to block copy paste.</span></span>|
|<span data-ttu-id="19aa4-160">bluetoothBlocked</span><span class="sxs-lookup"><span data-stu-id="19aa4-160">bluetoothBlocked</span></span>|<span data-ttu-id="19aa4-161">Booleano</span><span class="sxs-lookup"><span data-stu-id="19aa4-161">Boolean</span></span>|<span data-ttu-id="19aa4-162">Indica si se va a bloquear Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="19aa4-162">Indicates whether or not to block bluetooth.</span></span>|
|<span data-ttu-id="19aa4-163">cameraBlocked</span><span class="sxs-lookup"><span data-stu-id="19aa4-163">cameraBlocked</span></span>|<span data-ttu-id="19aa4-164">Booleano</span><span class="sxs-lookup"><span data-stu-id="19aa4-164">Boolean</span></span>|<span data-ttu-id="19aa4-165">Indica si se va a bloquear la cámara.</span><span class="sxs-lookup"><span data-stu-id="19aa4-165">Indicates whether or not to block camera.</span></span>|
|<span data-ttu-id="19aa4-166">cellularBlockWifiTethering</span><span class="sxs-lookup"><span data-stu-id="19aa4-166">cellularBlockWifiTethering</span></span>|<span data-ttu-id="19aa4-167">Booleano</span><span class="sxs-lookup"><span data-stu-id="19aa4-167">Boolean</span></span>|<span data-ttu-id="19aa4-168">Indica si se va a bloquear el tethering Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="19aa4-168">Indicates whether or not to block Wi-Fi tethering.</span></span> <span data-ttu-id="19aa4-169">No tiene impacto si se bloquea el Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="19aa4-169">Has no impact if Wi-Fi is blocked.</span></span>|
|<span data-ttu-id="19aa4-170">compliantAppsList</span><span class="sxs-lookup"><span data-stu-id="19aa4-170">compliantAppsList</span></span>|<span data-ttu-id="19aa4-171">Colección [appListItem](../resources/intune_deviceconfig_applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="19aa4-171">[appListItem](../resources/intune_deviceconfig_applistitem.md) collection</span></span>|<span data-ttu-id="19aa4-172">Lista de aplicaciones en el cumplimiento (sea lista de permitidos o de bloqueados, controlado por CompliantAppListType).</span><span class="sxs-lookup"><span data-stu-id="19aa4-172">List of apps in the compliance (either allow list or block list, controlled by CompliantAppListType).</span></span> <span data-ttu-id="19aa4-173">Esta colección puede contener un máximo de 10 000 elementos.</span><span class="sxs-lookup"><span data-stu-id="19aa4-173">This collection can contain a maximum of 10000 elements.</span></span>|
|<span data-ttu-id="19aa4-174">compliantAppListType</span><span class="sxs-lookup"><span data-stu-id="19aa4-174">compliantAppListType</span></span>|[<span data-ttu-id="19aa4-175">appListType</span><span class="sxs-lookup"><span data-stu-id="19aa4-175">appListType</span></span>](../resources/intune_deviceconfig_applisttype.md)|<span data-ttu-id="19aa4-176">Lista que se encuentra en la AppComplianceList.</span><span class="sxs-lookup"><span data-stu-id="19aa4-176">List that is in the AppComplianceList.</span></span> <span data-ttu-id="19aa4-177">Los valores posibles son: `none`, `appsInListCompliant` y `appsNotInListCompliant`.</span><span class="sxs-lookup"><span data-stu-id="19aa4-177">The possible values are `none`, `appsInListCompliant`, `appsNotInListCompliant`, , , , , , , , , or .</span></span>|
|<span data-ttu-id="19aa4-178">diagnosticDataBlockSubmission</span><span class="sxs-lookup"><span data-stu-id="19aa4-178">diagnosticDataBlockSubmission</span></span>|<span data-ttu-id="19aa4-179">Booleano</span><span class="sxs-lookup"><span data-stu-id="19aa4-179">Boolean</span></span>|<span data-ttu-id="19aa4-180">Indica si se va a bloquear el envío de datos de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="19aa4-180">Indicates whether or not to block diagnostic data submission.</span></span>|
|<span data-ttu-id="19aa4-181">emailBlockAddingAccounts</span><span class="sxs-lookup"><span data-stu-id="19aa4-181">emailBlockAddingAccounts</span></span>|<span data-ttu-id="19aa4-182">Booleano</span><span class="sxs-lookup"><span data-stu-id="19aa4-182">Boolean</span></span>|<span data-ttu-id="19aa4-183">Indica si se van a bloquear las cuentas de correo electrónico personalizadas.</span><span class="sxs-lookup"><span data-stu-id="19aa4-183">Indicates whether or not to block custom email accounts.</span></span>|
|<span data-ttu-id="19aa4-184">locationServicesBlocked</span><span class="sxs-lookup"><span data-stu-id="19aa4-184">locationServicesBlocked</span></span>|<span data-ttu-id="19aa4-185">Booleano</span><span class="sxs-lookup"><span data-stu-id="19aa4-185">Boolean</span></span>|<span data-ttu-id="19aa4-186">Indica si se van a bloquear los servicios de ubicación.</span><span class="sxs-lookup"><span data-stu-id="19aa4-186">Indicates whether or not to block location services.</span></span>|
|<span data-ttu-id="19aa4-187">microsoftAccountBlocked</span><span class="sxs-lookup"><span data-stu-id="19aa4-187">microsoftAccountBlocked</span></span>|<span data-ttu-id="19aa4-188">Booleano</span><span class="sxs-lookup"><span data-stu-id="19aa4-188">Boolean</span></span>|<span data-ttu-id="19aa4-189">Indica si se va a bloquear el uso de una cuenta de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="19aa4-189">Indicates whether or not to block using a Microsoft Account.</span></span>|
|<span data-ttu-id="19aa4-190">nfcBlocked</span><span class="sxs-lookup"><span data-stu-id="19aa4-190">nfcBlocked</span></span>|<span data-ttu-id="19aa4-191">Booleano</span><span class="sxs-lookup"><span data-stu-id="19aa4-191">Boolean</span></span>|<span data-ttu-id="19aa4-192">Indica si se va a bloquear la transmisión de datos en proximidad.</span><span class="sxs-lookup"><span data-stu-id="19aa4-192">Indicates whether or not to block Near-Field Communication.</span></span>|
|<span data-ttu-id="19aa4-193">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="19aa4-193">passwordBlockSimple</span></span>|<span data-ttu-id="19aa4-194">Booleano</span><span class="sxs-lookup"><span data-stu-id="19aa4-194">Boolean</span></span>|<span data-ttu-id="19aa4-195">Indica si se va a bloquear la sincronización del calendario.</span><span class="sxs-lookup"><span data-stu-id="19aa4-195">Indicates whether or not to block syncing the calendar.</span></span>|
|<span data-ttu-id="19aa4-196">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="19aa4-196">passwordExpirationDays</span></span>|<span data-ttu-id="19aa4-197">Int32</span><span class="sxs-lookup"><span data-stu-id="19aa4-197">Int32</span></span>|<span data-ttu-id="19aa4-198">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="19aa4-198">Number of days before the password expires.</span></span>|
|<span data-ttu-id="19aa4-199">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="19aa4-199">passwordMinimumLength</span></span>|<span data-ttu-id="19aa4-200">Int32</span><span class="sxs-lookup"><span data-stu-id="19aa4-200">Int32</span></span>|<span data-ttu-id="19aa4-201">Longitud mínima de las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="19aa4-201">Minimum length of passwords.</span></span>|
|<span data-ttu-id="19aa4-202">passwordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="19aa4-202">passwordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="19aa4-203">Int32</span><span class="sxs-lookup"><span data-stu-id="19aa4-203">Int32</span></span>|<span data-ttu-id="19aa4-204">Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="19aa4-204">Minutes of inactivity before screen timeout.</span></span>|
|<span data-ttu-id="19aa4-205">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="19aa4-205">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="19aa4-206">Int32</span><span class="sxs-lookup"><span data-stu-id="19aa4-206">Int32</span></span>|<span data-ttu-id="19aa4-207">Número de juegos de caracteres que debe contener una contraseña.</span><span class="sxs-lookup"><span data-stu-id="19aa4-207">Number of character sets a password must contain.</span></span>|
|<span data-ttu-id="19aa4-208">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="19aa4-208">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="19aa4-209">Int32</span><span class="sxs-lookup"><span data-stu-id="19aa4-209">Int32</span></span>|<span data-ttu-id="19aa4-210">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="19aa4-210">Number of previous passwords to block.</span></span> <span data-ttu-id="19aa4-211">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="19aa4-211">Valid values 0 to 24</span></span>|
|<span data-ttu-id="19aa4-212">passwordSignInFailureCountBeforeFactoryReset</span><span class="sxs-lookup"><span data-stu-id="19aa4-212">passwordSignInFailureCountBeforeFactoryReset</span></span>|<span data-ttu-id="19aa4-213">Int32</span><span class="sxs-lookup"><span data-stu-id="19aa4-213">Int32</span></span>|<span data-ttu-id="19aa4-214">Número de errores de inicio de sesión permitidos antes del restablecimiento de fábrica.</span><span class="sxs-lookup"><span data-stu-id="19aa4-214">Number of sign in failures allowed before factory reset.</span></span>|
|<span data-ttu-id="19aa4-215">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="19aa4-215">passwordRequiredType</span></span>|[<span data-ttu-id="19aa4-216">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="19aa4-216">requiredPasswordType</span></span>](../resources/intune_deviceconfig_requiredpasswordtype.md)|<span data-ttu-id="19aa4-217">Tipo de contraseña que es necesario.</span><span class="sxs-lookup"><span data-stu-id="19aa4-217">Password type that is required.</span></span> <span data-ttu-id="19aa4-218">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="19aa4-218">The possible values are `deviceDefault`, `alphanumeric`, `numeric`, , , , , , , , , or .</span></span>|
|<span data-ttu-id="19aa4-219">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="19aa4-219">passwordRequired</span></span>|<span data-ttu-id="19aa4-220">Booleano</span><span class="sxs-lookup"><span data-stu-id="19aa4-220">Boolean</span></span>|<span data-ttu-id="19aa4-221">Indica si se va a requerir una contraseña.</span><span class="sxs-lookup"><span data-stu-id="19aa4-221">Indicates whether or not to require a password.</span></span>|
|<span data-ttu-id="19aa4-222">screenCaptureBlocked</span><span class="sxs-lookup"><span data-stu-id="19aa4-222">screenCaptureBlocked</span></span>|<span data-ttu-id="19aa4-223">Booleano</span><span class="sxs-lookup"><span data-stu-id="19aa4-223">Boolean</span></span>|<span data-ttu-id="19aa4-224">Indica si se van a impedir las capturas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="19aa4-224">Indicates whether or not to block screenshots.</span></span>|
|<span data-ttu-id="19aa4-225">storageBlockRemovableStorage</span><span class="sxs-lookup"><span data-stu-id="19aa4-225">storageBlockRemovableStorage</span></span>|<span data-ttu-id="19aa4-226">Booleano</span><span class="sxs-lookup"><span data-stu-id="19aa4-226">Boolean</span></span>|<span data-ttu-id="19aa4-227">Indica si se va a impedir el almacenamiento extraíble.</span><span class="sxs-lookup"><span data-stu-id="19aa4-227">Indicates whether or not to block removable storage.</span></span>|
|<span data-ttu-id="19aa4-228">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="19aa4-228">storageRequireEncryption</span></span>|<span data-ttu-id="19aa4-229">Booleano</span><span class="sxs-lookup"><span data-stu-id="19aa4-229">Boolean</span></span>|<span data-ttu-id="19aa4-230">Indica si se va a requerir cifrado.</span><span class="sxs-lookup"><span data-stu-id="19aa4-230">Indicates whether or not to require encryption.</span></span>|
|<span data-ttu-id="19aa4-231">webBrowserBlocked</span><span class="sxs-lookup"><span data-stu-id="19aa4-231">webBrowserBlocked</span></span>|<span data-ttu-id="19aa4-232">Booleano</span><span class="sxs-lookup"><span data-stu-id="19aa4-232">Boolean</span></span>|<span data-ttu-id="19aa4-233">Indica si se va a bloquear el explorador web.</span><span class="sxs-lookup"><span data-stu-id="19aa4-233">Indicates whether or not to block the web browser.</span></span>|
|<span data-ttu-id="19aa4-234">wifiBlocked</span><span class="sxs-lookup"><span data-stu-id="19aa4-234">wifiBlocked</span></span>|<span data-ttu-id="19aa4-235">Booleano</span><span class="sxs-lookup"><span data-stu-id="19aa4-235">Boolean</span></span>|<span data-ttu-id="19aa4-236">Indica si se va a bloquear el uso de Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="19aa4-236">Indicates whether or not to block Wi-Fi.</span></span>|
|<span data-ttu-id="19aa4-237">wifiBlockAutomaticConnectHotspots</span><span class="sxs-lookup"><span data-stu-id="19aa4-237">wifiBlockAutomaticConnectHotspots</span></span>|<span data-ttu-id="19aa4-238">Booleano</span><span class="sxs-lookup"><span data-stu-id="19aa4-238">Boolean</span></span>|<span data-ttu-id="19aa4-239">Indica si se va a bloquear automáticamente la conexión a zonas Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="19aa4-239">Indicates whether or not to block automatically connecting to Wi-Fi hotspots.</span></span> <span data-ttu-id="19aa4-240">No tiene impacto si se bloquea el Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="19aa4-240">Has no impact if Wi-Fi is blocked.</span></span>|
|<span data-ttu-id="19aa4-241">wifiBlockHotspotReporting</span><span class="sxs-lookup"><span data-stu-id="19aa4-241">wifiBlockHotspotReporting</span></span>|<span data-ttu-id="19aa4-242">Booleano</span><span class="sxs-lookup"><span data-stu-id="19aa4-242">Boolean</span></span>|<span data-ttu-id="19aa4-243">Indica si se van a bloquear los informes de zona Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="19aa4-243">Indicates whether or not to block Wi-Fi hotspot reporting.</span></span> <span data-ttu-id="19aa4-244">No tiene impacto si se bloquea el Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="19aa4-244">Has no impact if Wi-Fi is blocked.</span></span>|
|<span data-ttu-id="19aa4-245">windowsStoreBlocked</span><span class="sxs-lookup"><span data-stu-id="19aa4-245">windowsStoreBlocked</span></span>|<span data-ttu-id="19aa4-246">Booleano</span><span class="sxs-lookup"><span data-stu-id="19aa4-246">Boolean</span></span>|<span data-ttu-id="19aa4-247">Indica si se va a bloquear la Tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="19aa4-247">Indicates whether or not to block the Windows Store.</span></span>|



## <a name="response"></a><span data-ttu-id="19aa4-248">Respuesta</span><span class="sxs-lookup"><span data-stu-id="19aa4-248">Response</span></span>
<span data-ttu-id="19aa4-249">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsPhone81GeneralConfiguration](../resources/intune_deviceconfig_windowsphone81generalconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="19aa4-249">If successful, this method returns a `200 OK` response code and an updated [windowsPhone81GeneralConfiguration](../resources/intune_deviceconfig_windowsphone81generalconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="19aa4-250">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="19aa4-250">Example</span></span>
### <a name="request"></a><span data-ttu-id="19aa4-251">Solicitud</span><span class="sxs-lookup"><span data-stu-id="19aa4-251">Request</span></span>
<span data-ttu-id="19aa4-252">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="19aa4-252">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 1452

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "applyOnlyToWindowsPhone81": true,
  "appsBlockCopyPaste": true,
  "bluetoothBlocked": true,
  "cameraBlocked": true,
  "cellularBlockWifiTethering": true,
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
  "emailBlockAddingAccounts": true,
  "locationServicesBlocked": true,
  "microsoftAccountBlocked": true,
  "nfcBlocked": true,
  "passwordBlockSimple": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordMinimumCharacterSetCount": 0,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordSignInFailureCountBeforeFactoryReset": 12,
  "passwordRequiredType": "alphanumeric",
  "passwordRequired": true,
  "screenCaptureBlocked": true,
  "storageBlockRemovableStorage": true,
  "storageRequireEncryption": true,
  "webBrowserBlocked": true,
  "wifiBlocked": true,
  "wifiBlockAutomaticConnectHotspots": true,
  "wifiBlockHotspotReporting": true,
  "windowsStoreBlocked": true
}
```

### <a name="response"></a><span data-ttu-id="19aa4-253">Respuesta</span><span class="sxs-lookup"><span data-stu-id="19aa4-253">Response</span></span>
<span data-ttu-id="19aa4-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="19aa4-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1633

{
  "@odata.type": "#microsoft.graph.windowsPhone81GeneralConfiguration",
  "id": "f5e0e34d-e34d-f5e0-4de3-e0f54de3e0f5",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "applyOnlyToWindowsPhone81": true,
  "appsBlockCopyPaste": true,
  "bluetoothBlocked": true,
  "cameraBlocked": true,
  "cellularBlockWifiTethering": true,
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
  "emailBlockAddingAccounts": true,
  "locationServicesBlocked": true,
  "microsoftAccountBlocked": true,
  "nfcBlocked": true,
  "passwordBlockSimple": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordMinimumCharacterSetCount": 0,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordSignInFailureCountBeforeFactoryReset": 12,
  "passwordRequiredType": "alphanumeric",
  "passwordRequired": true,
  "screenCaptureBlocked": true,
  "storageBlockRemovableStorage": true,
  "storageRequireEncryption": true,
  "webBrowserBlocked": true,
  "wifiBlocked": true,
  "wifiBlockAutomaticConnectHotspots": true,
  "wifiBlockHotspotReporting": true,
  "windowsStoreBlocked": true
}
```



