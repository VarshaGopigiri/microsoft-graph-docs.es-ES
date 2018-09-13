# <a name="create-androidworkprofilegeneraldeviceconfiguration"></a><span data-ttu-id="ea4fd-101">Crear androidWorkProfileGeneralDeviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea4fd-101">Create androidWorkProfileGeneralDeviceConfiguration</span></span>

> <span data-ttu-id="ea4fd-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ea4fd-103">Crear un nuevo objeto [androidWorkProfileGeneralDeviceConfiguration](../resources/intune_deviceconfig_androidworkprofilegeneraldeviceconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="ea4fd-103">Create a new [microsoftStoreForBusinessApp](../resources/intune_deviceconfig_androidworkprofilegeneraldeviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ea4fd-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ea4fd-104">Prerequisites</span></span>
<span data-ttu-id="ea4fd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ea4fd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ea4fd-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ea4fd-107">Permission type</span></span>|<span data-ttu-id="ea4fd-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ea4fd-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ea4fd-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ea4fd-109">Delegated (work or school account)</span></span>|<span data-ttu-id="ea4fd-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ea4fd-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="ea4fd-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ea4fd-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ea4fd-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-112">Not supported.</span></span>|
|<span data-ttu-id="ea4fd-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ea4fd-113">Application</span></span>|<span data-ttu-id="ea4fd-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ea4fd-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ea4fd-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="ea4fd-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ea4fd-116">Request headers</span></span>
|<span data-ttu-id="ea4fd-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea4fd-117">Header</span></span>|<span data-ttu-id="ea4fd-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ea4fd-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ea4fd-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="ea4fd-119">Authorization</span></span>|<span data-ttu-id="ea4fd-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ea4fd-121">Accept</span><span class="sxs-lookup"><span data-stu-id="ea4fd-121">Accept</span></span>|<span data-ttu-id="ea4fd-122">application/json</span><span class="sxs-lookup"><span data-stu-id="ea4fd-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ea4fd-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ea4fd-123">Request body</span></span>
<span data-ttu-id="ea4fd-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto androidWorkProfileGeneralDeviceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-124">In the request body, supply a JSON representation for the deviceManagement object.</span></span>

<span data-ttu-id="ea4fd-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto androidWorkProfileGeneralDeviceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-125">The following table shows the properties that are required when you create the deviceConfigurationUserStatus.</span></span>

|<span data-ttu-id="ea4fd-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ea4fd-126">Property</span></span>|<span data-ttu-id="ea4fd-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="ea4fd-127">Type</span></span>|<span data-ttu-id="ea4fd-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea4fd-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ea4fd-129">id</span><span class="sxs-lookup"><span data-stu-id="ea4fd-129">id</span></span>|<span data-ttu-id="ea4fd-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="ea4fd-130">String</span></span>|<span data-ttu-id="ea4fd-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-131">Key of the entity.</span></span> <span data-ttu-id="ea4fd-132">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea4fd-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ea4fd-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="ea4fd-133">lastModifiedDateTime</span></span>|<span data-ttu-id="ea4fd-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ea4fd-134">DateTimeOffset</span></span>|<span data-ttu-id="ea4fd-135">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-135">DateTime the object was last modified.</span></span> <span data-ttu-id="ea4fd-136">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea4fd-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ea4fd-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="ea4fd-137">createdDateTime</span></span>|<span data-ttu-id="ea4fd-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ea4fd-138">DateTimeOffset</span></span>|<span data-ttu-id="ea4fd-139">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-139">DateTime the object was created.</span></span> <span data-ttu-id="ea4fd-140">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea4fd-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ea4fd-141">description</span><span class="sxs-lookup"><span data-stu-id="ea4fd-141">description</span></span>|<span data-ttu-id="ea4fd-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="ea4fd-142">String</span></span>|<span data-ttu-id="ea4fd-143">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="ea4fd-144">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea4fd-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ea4fd-145">displayName</span><span class="sxs-lookup"><span data-stu-id="ea4fd-145">displayName</span></span>|<span data-ttu-id="ea4fd-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="ea4fd-146">String</span></span>|<span data-ttu-id="ea4fd-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="ea4fd-148">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea4fd-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ea4fd-149">version</span><span class="sxs-lookup"><span data-stu-id="ea4fd-149">version</span></span>|<span data-ttu-id="ea4fd-150">Int32</span><span class="sxs-lookup"><span data-stu-id="ea4fd-150">Int32</span></span>|<span data-ttu-id="ea4fd-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-151">Version of the device configuration.</span></span> <span data-ttu-id="ea4fd-152">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea4fd-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ea4fd-153">passwordBlockFingerprintUnlock</span><span class="sxs-lookup"><span data-stu-id="ea4fd-153">passwordBlockFingerprintUnlock</span></span>|<span data-ttu-id="ea4fd-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="ea4fd-154">Boolean</span></span>|<span data-ttu-id="ea4fd-155">Indica si se va a impedir el desbloqueo por huella dactilar.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-155">Indicates whether or not to block fingerprint unlock.</span></span>|
|<span data-ttu-id="ea4fd-156">passwordBlockTrustAgents</span><span class="sxs-lookup"><span data-stu-id="ea4fd-156">passwordBlockTrustAgents</span></span>|<span data-ttu-id="ea4fd-157">Booleano</span><span class="sxs-lookup"><span data-stu-id="ea4fd-157">Boolean</span></span>|<span data-ttu-id="ea4fd-158">Indica si se van a bloquear Smart Lock y otros agentes de confianza.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-158">Indicates whether or not to block Smart Lock and other trust agents.</span></span>|
|<span data-ttu-id="ea4fd-159">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="ea4fd-159">passwordExpirationDays</span></span>|<span data-ttu-id="ea4fd-160">Int32</span><span class="sxs-lookup"><span data-stu-id="ea4fd-160">Int32</span></span>|<span data-ttu-id="ea4fd-161">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-161">Number of days before the password expires.</span></span> <span data-ttu-id="ea4fd-162">Valores válidos de 1 a 365</span><span class="sxs-lookup"><span data-stu-id="ea4fd-162">Valid values 1 to 365</span></span>|
|<span data-ttu-id="ea4fd-163">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="ea4fd-163">passwordMinimumLength</span></span>|<span data-ttu-id="ea4fd-164">Int32</span><span class="sxs-lookup"><span data-stu-id="ea4fd-164">Int32</span></span>|<span data-ttu-id="ea4fd-165">Longitud mínima de las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-165">Minimum length of passwords.</span></span> <span data-ttu-id="ea4fd-166">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="ea4fd-166">Valid values 4 to 16</span></span>|
|<span data-ttu-id="ea4fd-167">passwordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="ea4fd-167">passwordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="ea4fd-168">Int32</span><span class="sxs-lookup"><span data-stu-id="ea4fd-168">Int32</span></span>|<span data-ttu-id="ea4fd-169">Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-169">Minutes of inactivity before the screen times out.</span></span>|
|<span data-ttu-id="ea4fd-170">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="ea4fd-170">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="ea4fd-171">Int32</span><span class="sxs-lookup"><span data-stu-id="ea4fd-171">Int32</span></span>|<span data-ttu-id="ea4fd-172">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-172">Number of previous passwords to block.</span></span> <span data-ttu-id="ea4fd-173">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="ea4fd-173">Valid values 0 to 24</span></span>|
|<span data-ttu-id="ea4fd-174">passwordSignInFailureCountBeforeFactoryReset</span><span class="sxs-lookup"><span data-stu-id="ea4fd-174">passwordSignInFailureCountBeforeFactoryReset</span></span>|<span data-ttu-id="ea4fd-175">Int32</span><span class="sxs-lookup"><span data-stu-id="ea4fd-175">Int32</span></span>|<span data-ttu-id="ea4fd-176">Número de errores de inicio de sesión permitidos antes del restablecimiento de fábrica.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-176">Number of sign in failures allowed before factory reset.</span></span> <span data-ttu-id="ea4fd-177">Valores válidos de 4 a 11</span><span class="sxs-lookup"><span data-stu-id="ea4fd-177">Valid values 4 to 11</span></span>|
|<span data-ttu-id="ea4fd-178">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="ea4fd-178">passwordRequiredType</span></span>|[<span data-ttu-id="ea4fd-179">androidWorkProfileRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="ea4fd-179">androidWorkProfileRequiredPasswordType</span></span>](../resources/intune_deviceconfig_androidworkprofilerequiredpasswordtype.md)|<span data-ttu-id="ea4fd-180">Tipo de contraseña que es necesario.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-180">Type of password that is required.</span></span> <span data-ttu-id="ea4fd-181">Los valores posibles son: `deviceDefault`, `lowSecurityBiometric`, `required`, `atLeastNumeric`, `numericComplex`, `atLeastAlphabetic`, `atLeastAlphanumeric` y `alphanumericWithSymbols`.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-181">Possible values are: `deviceDefault`, `lowSecurityBiometric`, `required`, `atLeastNumeric`, `numericComplex`, `atLeastAlphabetic`, `atLeastAlphanumeric`, `alphanumericWithSymbols`.</span></span>|
|<span data-ttu-id="ea4fd-182">workProfileDataSharingType</span><span class="sxs-lookup"><span data-stu-id="ea4fd-182">workProfileDataSharingType</span></span>|[<span data-ttu-id="ea4fd-183">androidWorkProfileCrossProfileDataSharingType</span><span class="sxs-lookup"><span data-stu-id="ea4fd-183">androidWorkProfileCrossProfileDataSharingType</span></span>](../resources/intune_deviceconfig_androidworkprofilecrossprofiledatasharingtype.md)|<span data-ttu-id="ea4fd-184">Tipo de datos de uso compartido que está permitido.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-184">Type of data sharing that is allowed.</span></span> <span data-ttu-id="ea4fd-185">Los valores posibles son: `deviceDefault`, `preventAny`, `allowPersonalToWork` y `noRestrictions`.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-185">Possible values are: `deviceDefault`, `preventAny`, `allowPersonalToWork`, `noRestrictions`.</span></span>|
|<span data-ttu-id="ea4fd-186">workProfileBlockNotificationsWhileDeviceLocked</span><span class="sxs-lookup"><span data-stu-id="ea4fd-186">workProfileBlockNotificationsWhileDeviceLocked</span></span>|<span data-ttu-id="ea4fd-187">Booleano</span><span class="sxs-lookup"><span data-stu-id="ea4fd-187">Boolean</span></span>|<span data-ttu-id="ea4fd-188">Indica si se deben bloquear las notificaciones al dispositivo bloqueado.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-188">Indicates whether or not to block notifications while device locked.</span></span>|
|<span data-ttu-id="ea4fd-189">workProfileBlockAddingAccounts</span><span class="sxs-lookup"><span data-stu-id="ea4fd-189">workProfileBlockAddingAccounts</span></span>|<span data-ttu-id="ea4fd-190">Booleano</span><span class="sxs-lookup"><span data-stu-id="ea4fd-190">Boolean</span></span>|<span data-ttu-id="ea4fd-191">Impedir a los usuarios agregar o quitar cuentas en el perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-191">Block users from adding/removing accounts in work profile.</span></span>|
|<span data-ttu-id="ea4fd-192">workProfileBluetoothEnableContactSharing</span><span class="sxs-lookup"><span data-stu-id="ea4fd-192">workProfileBluetoothEnableContactSharing</span></span>|<span data-ttu-id="ea4fd-193">Booleano</span><span class="sxs-lookup"><span data-stu-id="ea4fd-193">Boolean</span></span>|<span data-ttu-id="ea4fd-194">Permitir a los dispositivos bluetooth tener acceso a los contactos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-194">Allow bluetooth devices to access enterprise contacts.</span></span>|
|<span data-ttu-id="ea4fd-195">workProfileBlockScreenCapture</span><span class="sxs-lookup"><span data-stu-id="ea4fd-195">workProfileBlockScreenCapture</span></span>|<span data-ttu-id="ea4fd-196">Booleano</span><span class="sxs-lookup"><span data-stu-id="ea4fd-196">Boolean</span></span>|<span data-ttu-id="ea4fd-197">Bloquear captura de pantalla en el perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-197">Block screen capture in work profile.</span></span>|
|<span data-ttu-id="ea4fd-198">workProfileBlockCrossProfileCallerId</span><span class="sxs-lookup"><span data-stu-id="ea4fd-198">workProfileBlockCrossProfileCallerId</span></span>|<span data-ttu-id="ea4fd-199">Booleano</span><span class="sxs-lookup"><span data-stu-id="ea4fd-199">Boolean</span></span>|<span data-ttu-id="ea4fd-200">Bloquear mostrar el identificador de autor de la llamada de perfil de trabajo en un perfil personal.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-200">Block display work profile caller ID in personal profile.</span></span>|
|<span data-ttu-id="ea4fd-201">workProfileBlockCamera</span><span class="sxs-lookup"><span data-stu-id="ea4fd-201">workProfileBlockCamera</span></span>|<span data-ttu-id="ea4fd-202">Booleano</span><span class="sxs-lookup"><span data-stu-id="ea4fd-202">Boolean</span></span>|<span data-ttu-id="ea4fd-203">Bloquear la cámara en el perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-203">Block work profile camera.</span></span>|
|<span data-ttu-id="ea4fd-204">workProfileBlockCrossProfileContactsSearch</span><span class="sxs-lookup"><span data-stu-id="ea4fd-204">workProfileBlockCrossProfileContactsSearch</span></span>|<span data-ttu-id="ea4fd-205">Booleano</span><span class="sxs-lookup"><span data-stu-id="ea4fd-205">Boolean</span></span>|<span data-ttu-id="ea4fd-206">Bloquear disponibilidad de los contactos del perfil de trabajo en perfil personal.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-206">Block work profile contacts availability in personal profile.</span></span>|
|<span data-ttu-id="ea4fd-207">workProfileBlockCrossProfileCopyPaste</span><span class="sxs-lookup"><span data-stu-id="ea4fd-207">workProfileBlockCrossProfileCopyPaste</span></span>|<span data-ttu-id="ea4fd-208">Booleano</span><span class="sxs-lookup"><span data-stu-id="ea4fd-208">Boolean</span></span>|<span data-ttu-id="ea4fd-209">Valor booleano que indica si está habilitada la opción de no permitir el copiado y pegado entre perfiles.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-209">Boolean that indicates if the setting disallow cross profile copy/paste is enabled.</span></span>|
|<span data-ttu-id="ea4fd-210">workProfileDefaultAppPermissionPolicy</span><span class="sxs-lookup"><span data-stu-id="ea4fd-210">workProfileDefaultAppPermissionPolicy</span></span>|[<span data-ttu-id="ea4fd-211">androidWorkProfileDefaultAppPermissionPolicyType</span><span class="sxs-lookup"><span data-stu-id="ea4fd-211">androidWorkProfileDefaultAppPermissionPolicyType</span></span>](../resources/intune_deviceconfig_androidworkprofiledefaultapppermissionpolicytype.md)|<span data-ttu-id="ea4fd-212">Tipo de contraseña que es necesario.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-212">Type of password that is required.</span></span> <span data-ttu-id="ea4fd-213">Los valores posibles son: `deviceDefault`, `prompt`, `autoGrant` y `autoDeny`.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-213">Possible values are: `deviceDefault`, `prompt`, `autoGrant`, `autoDeny`.</span></span>|
|<span data-ttu-id="ea4fd-214">workProfilePasswordBlockFingerprintUnlock</span><span class="sxs-lookup"><span data-stu-id="ea4fd-214">workProfilePasswordBlockFingerprintUnlock</span></span>|<span data-ttu-id="ea4fd-215">Booleano</span><span class="sxs-lookup"><span data-stu-id="ea4fd-215">Boolean</span></span>|<span data-ttu-id="ea4fd-216">Indica si se va a impedir el desbloqueo por huella dactilar en el perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-216">Indicates whether or not to block fingerprint unlock.</span></span>|
|<span data-ttu-id="ea4fd-217">workProfilePasswordBlockTrustAgents</span><span class="sxs-lookup"><span data-stu-id="ea4fd-217">workProfilePasswordBlockTrustAgents</span></span>|<span data-ttu-id="ea4fd-218">Booleano</span><span class="sxs-lookup"><span data-stu-id="ea4fd-218">Boolean</span></span>|<span data-ttu-id="ea4fd-219">Indica si se van a bloquear Smart Lock y otros agentes de confianza en el perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-219">Indicates whether or not to block Smart Lock and other trust agents.</span></span>|
|<span data-ttu-id="ea4fd-220">workProfilePasswordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="ea4fd-220">workProfilePasswordExpirationDays</span></span>|<span data-ttu-id="ea4fd-221">Int32</span><span class="sxs-lookup"><span data-stu-id="ea4fd-221">Int32</span></span>|<span data-ttu-id="ea4fd-222">Número de días antes de que expire la contraseña en el perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-222">Number of days before the password expires.</span></span> <span data-ttu-id="ea4fd-223">Valores válidos de 1 a 365</span><span class="sxs-lookup"><span data-stu-id="ea4fd-223">Valid values 1 to 365</span></span>|
|<span data-ttu-id="ea4fd-224">workProfilePasswordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="ea4fd-224">workProfilePasswordMinimumLength</span></span>|<span data-ttu-id="ea4fd-225">Int32</span><span class="sxs-lookup"><span data-stu-id="ea4fd-225">Int32</span></span>|<span data-ttu-id="ea4fd-226">Longitud mínima de contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-226">Minimum length of work profile password.</span></span> <span data-ttu-id="ea4fd-227">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="ea4fd-227">Valid values 4 to 16</span></span>|
|<span data-ttu-id="ea4fd-228">workProfilePasswordMinNumericCharacters</span><span class="sxs-lookup"><span data-stu-id="ea4fd-228">workProfilePasswordMinNumericCharacters</span></span>|<span data-ttu-id="ea4fd-229">Int32</span><span class="sxs-lookup"><span data-stu-id="ea4fd-229">Int32</span></span>|<span data-ttu-id="ea4fd-230">N.º mínimo de caracteres numéricos requeridos en la contraseña del perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-230">Minimum # of numeric characters required in work profile password.</span></span> <span data-ttu-id="ea4fd-231">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="ea4fd-231">Valid values 1 to 65535</span></span>|
|<span data-ttu-id="ea4fd-232">workProfilePasswordMinNonLetterCharacters</span><span class="sxs-lookup"><span data-stu-id="ea4fd-232">workProfilePasswordMinNonLetterCharacters</span></span>|<span data-ttu-id="ea4fd-233">Int32</span><span class="sxs-lookup"><span data-stu-id="ea4fd-233">Int32</span></span>|<span data-ttu-id="ea4fd-234">N.º mínimo de caracteres que no sean una letra requeridos en la contraseña del perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-234">Minimum # of non-letter characters required in work profile password.</span></span> <span data-ttu-id="ea4fd-235">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="ea4fd-235">Valid values 1 to 65535</span></span>|
|<span data-ttu-id="ea4fd-236">workProfilePasswordMinLetterCharacters</span><span class="sxs-lookup"><span data-stu-id="ea4fd-236">workProfilePasswordMinLetterCharacters</span></span>|<span data-ttu-id="ea4fd-237">Int32</span><span class="sxs-lookup"><span data-stu-id="ea4fd-237">Int32</span></span>|<span data-ttu-id="ea4fd-238">N.º mínimo de caracteres que sean una letra requeridos en la contraseña del perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-238">Minimum # of letter characters required in work profile password.</span></span> <span data-ttu-id="ea4fd-239">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="ea4fd-239">Valid values 1 to 65535</span></span>|
|<span data-ttu-id="ea4fd-240">workProfilePasswordMinLowerCaseCharacters</span><span class="sxs-lookup"><span data-stu-id="ea4fd-240">workProfilePasswordMinLowerCaseCharacters</span></span>|<span data-ttu-id="ea4fd-241">Int32</span><span class="sxs-lookup"><span data-stu-id="ea4fd-241">Int32</span></span>|<span data-ttu-id="ea4fd-242">N.º mínimo de caracteres en minúsculas requeridos en la contraseña del perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-242">Minimum # of lower-case characters required in work profile password.</span></span> <span data-ttu-id="ea4fd-243">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="ea4fd-243">Valid values 1 to 65535</span></span>|
|<span data-ttu-id="ea4fd-244">workProfilePasswordMinUpperCaseCharacters</span><span class="sxs-lookup"><span data-stu-id="ea4fd-244">workProfilePasswordMinUpperCaseCharacters</span></span>|<span data-ttu-id="ea4fd-245">Int32</span><span class="sxs-lookup"><span data-stu-id="ea4fd-245">Int32</span></span>|<span data-ttu-id="ea4fd-246">N.º mínimo de caracteres en mayúsculas requeridos en la contraseña del perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-246">Minimum # of upper-case characters required in work profile password.</span></span> <span data-ttu-id="ea4fd-247">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="ea4fd-247">Valid values 1 to 65535</span></span>|
|<span data-ttu-id="ea4fd-248">workProfilePasswordMinSymbolCharacters</span><span class="sxs-lookup"><span data-stu-id="ea4fd-248">workProfilePasswordMinSymbolCharacters</span></span>|<span data-ttu-id="ea4fd-249">Int32</span><span class="sxs-lookup"><span data-stu-id="ea4fd-249">Int32</span></span>|<span data-ttu-id="ea4fd-250">N.º mínimo de símbolos requeridos en la contraseña del perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-250">Minimum # of symbols required in work profile password.</span></span> <span data-ttu-id="ea4fd-251">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="ea4fd-251">Valid values 1 to 65535</span></span>|
|<span data-ttu-id="ea4fd-252">workProfilePasswordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="ea4fd-252">workProfilePasswordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="ea4fd-253">Int32</span><span class="sxs-lookup"><span data-stu-id="ea4fd-253">Int32</span></span>|<span data-ttu-id="ea4fd-254">Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-254">Minutes of inactivity before the screen times out.</span></span>|
|<span data-ttu-id="ea4fd-255">workProfilePasswordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="ea4fd-255">workProfilePasswordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="ea4fd-256">Int32</span><span class="sxs-lookup"><span data-stu-id="ea4fd-256">Int32</span></span>|<span data-ttu-id="ea4fd-257">Número de contraseñas previas para bloquear en el perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-257">Number of previous passwords to block.</span></span> <span data-ttu-id="ea4fd-258">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="ea4fd-258">Valid values 0 to 24</span></span>|
|<span data-ttu-id="ea4fd-259">workProfilePasswordSignInFailureCountBeforeFactoryReset</span><span class="sxs-lookup"><span data-stu-id="ea4fd-259">workProfilePasswordSignInFailureCountBeforeFactoryReset</span></span>|<span data-ttu-id="ea4fd-260">Int32</span><span class="sxs-lookup"><span data-stu-id="ea4fd-260">Int32</span></span>|<span data-ttu-id="ea4fd-261">Número de errores de inicio de sesión permitidos antes de que se quite el perfil de trabajo y todos los datos corporativos sean eliminados.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-261">Number of sign in failures allowed before work profile is removed and all corporate data deleted.</span></span> <span data-ttu-id="ea4fd-262">Valores válidos de 4 a 11</span><span class="sxs-lookup"><span data-stu-id="ea4fd-262">Valid values 4 to 11</span></span>|
|<span data-ttu-id="ea4fd-263">workProfilePasswordRequiredType</span><span class="sxs-lookup"><span data-stu-id="ea4fd-263">workProfilePasswordRequiredType</span></span>|[<span data-ttu-id="ea4fd-264">androidWorkProfileRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="ea4fd-264">androidWorkProfileRequiredPasswordType</span></span>](../resources/intune_deviceconfig_androidworkprofilerequiredpasswordtype.md)|<span data-ttu-id="ea4fd-265">Tipo de contraseña del perfil de trabajo que se requiere.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-265">Type of password that is required.</span></span> <span data-ttu-id="ea4fd-266">Los valores posibles son: `deviceDefault`, `lowSecurityBiometric`, `required`, `atLeastNumeric`, `numericComplex`, `atLeastAlphabetic`, `atLeastAlphanumeric` y `alphanumericWithSymbols`.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-266">Possible values are: `deviceDefault`, `lowSecurityBiometric`, `required`, `atLeastNumeric`, `numericComplex`, `atLeastAlphabetic`, `atLeastAlphanumeric`, `alphanumericWithSymbols`.</span></span>|
|<span data-ttu-id="ea4fd-267">workProfileRequirePassword</span><span class="sxs-lookup"><span data-stu-id="ea4fd-267">workProfileRequirePassword</span></span>|<span data-ttu-id="ea4fd-268">Booleano</span><span class="sxs-lookup"><span data-stu-id="ea4fd-268">Boolean</span></span>|<span data-ttu-id="ea4fd-269">Se requiere contraseña o no para el perfil de trabajo</span><span class="sxs-lookup"><span data-stu-id="ea4fd-269">Password is required or not for work profile</span></span>|
|<span data-ttu-id="ea4fd-270">securityRequireVerifyApps</span><span class="sxs-lookup"><span data-stu-id="ea4fd-270">securityRequireVerifyApps</span></span>|<span data-ttu-id="ea4fd-271">Booleano</span><span class="sxs-lookup"><span data-stu-id="ea4fd-271">Boolean</span></span>|<span data-ttu-id="ea4fd-272">Requerir que la característica Verificar aplicaciones de Android esté activada.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-272">Require the Android Verify apps feature is turned on.</span></span>|



## <a name="response"></a><span data-ttu-id="ea4fd-273">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea4fd-273">Response</span></span>
<span data-ttu-id="ea4fd-274">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [androidWorkProfileGeneralDeviceConfiguration](../resources/intune_deviceconfig_androidworkprofilegeneraldeviceconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-274">If successful, this method returns a `201 Created` response code and a [windowsPhone81CompliancePolicy](../resources/intune_deviceconfig_androidworkprofilegeneraldeviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ea4fd-275">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ea4fd-275">Example</span></span>
### <a name="request"></a><span data-ttu-id="ea4fd-276">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ea4fd-276">Request</span></span>
<span data-ttu-id="ea4fd-277">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-277">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 1895

{
  "@odata.type": "#microsoft.graph.androidWorkProfileGeneralDeviceConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "passwordBlockFingerprintUnlock": true,
  "passwordBlockTrustAgents": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordSignInFailureCountBeforeFactoryReset": 12,
  "passwordRequiredType": "lowSecurityBiometric",
  "workProfileDataSharingType": "preventAny",
  "workProfileBlockNotificationsWhileDeviceLocked": true,
  "workProfileBlockAddingAccounts": true,
  "workProfileBluetoothEnableContactSharing": true,
  "workProfileBlockScreenCapture": true,
  "workProfileBlockCrossProfileCallerId": true,
  "workProfileBlockCamera": true,
  "workProfileBlockCrossProfileContactsSearch": true,
  "workProfileBlockCrossProfileCopyPaste": true,
  "workProfileDefaultAppPermissionPolicy": "prompt",
  "workProfilePasswordBlockFingerprintUnlock": true,
  "workProfilePasswordBlockTrustAgents": true,
  "workProfilePasswordExpirationDays": 1,
  "workProfilePasswordMinimumLength": 0,
  "workProfilePasswordMinNumericCharacters": 7,
  "workProfilePasswordMinNonLetterCharacters": 9,
  "workProfilePasswordMinLetterCharacters": 6,
  "workProfilePasswordMinLowerCaseCharacters": 9,
  "workProfilePasswordMinUpperCaseCharacters": 9,
  "workProfilePasswordMinSymbolCharacters": 6,
  "workProfilePasswordMinutesOfInactivityBeforeScreenTimeout": 9,
  "workProfilePasswordPreviousPasswordBlockCount": 13,
  "workProfilePasswordSignInFailureCountBeforeFactoryReset": 7,
  "workProfilePasswordRequiredType": "lowSecurityBiometric",
  "workProfileRequirePassword": true,
  "securityRequireVerifyApps": true
}
```

### <a name="response"></a><span data-ttu-id="ea4fd-278">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea4fd-278">Response</span></span>
<span data-ttu-id="ea4fd-p126">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-p126">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 2003

{
  "@odata.type": "#microsoft.graph.androidWorkProfileGeneralDeviceConfiguration",
  "id": "6decda7e-da7e-6dec-7eda-ec6d7edaec6d",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "passwordBlockFingerprintUnlock": true,
  "passwordBlockTrustAgents": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordSignInFailureCountBeforeFactoryReset": 12,
  "passwordRequiredType": "lowSecurityBiometric",
  "workProfileDataSharingType": "preventAny",
  "workProfileBlockNotificationsWhileDeviceLocked": true,
  "workProfileBlockAddingAccounts": true,
  "workProfileBluetoothEnableContactSharing": true,
  "workProfileBlockScreenCapture": true,
  "workProfileBlockCrossProfileCallerId": true,
  "workProfileBlockCamera": true,
  "workProfileBlockCrossProfileContactsSearch": true,
  "workProfileBlockCrossProfileCopyPaste": true,
  "workProfileDefaultAppPermissionPolicy": "prompt",
  "workProfilePasswordBlockFingerprintUnlock": true,
  "workProfilePasswordBlockTrustAgents": true,
  "workProfilePasswordExpirationDays": 1,
  "workProfilePasswordMinimumLength": 0,
  "workProfilePasswordMinNumericCharacters": 7,
  "workProfilePasswordMinNonLetterCharacters": 9,
  "workProfilePasswordMinLetterCharacters": 6,
  "workProfilePasswordMinLowerCaseCharacters": 9,
  "workProfilePasswordMinUpperCaseCharacters": 9,
  "workProfilePasswordMinSymbolCharacters": 6,
  "workProfilePasswordMinutesOfInactivityBeforeScreenTimeout": 9,
  "workProfilePasswordPreviousPasswordBlockCount": 13,
  "workProfilePasswordSignInFailureCountBeforeFactoryReset": 7,
  "workProfilePasswordRequiredType": "lowSecurityBiometric",
  "workProfileRequirePassword": true,
  "securityRequireVerifyApps": true
}
```








