# <a name="create-androidcompliancepolicy"></a><span data-ttu-id="389a5-101">Crear androidCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="389a5-101">Create androidCompliancePolicy</span></span>

> <span data-ttu-id="389a5-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="389a5-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="389a5-103">Cree un objeto [androidCompliancePolicy](../resources/intune_deviceconfig_androidcompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="389a5-103">Create a new [androidCompliancePolicy](../resources/intune_deviceconfig_androidcompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="389a5-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="389a5-104">Prerequisites</span></span>
<span data-ttu-id="389a5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="389a5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="389a5-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="389a5-107">Permission type</span></span>|<span data-ttu-id="389a5-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="389a5-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="389a5-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="389a5-109">Delegated (work or school account)</span></span>|<span data-ttu-id="389a5-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="389a5-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="389a5-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="389a5-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="389a5-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="389a5-112">Not supported.</span></span>|
|<span data-ttu-id="389a5-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="389a5-113">Application</span></span>|<span data-ttu-id="389a5-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="389a5-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="389a5-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="389a5-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="389a5-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="389a5-116">Request headers</span></span>
|<span data-ttu-id="389a5-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="389a5-117">Header</span></span>|<span data-ttu-id="389a5-118">Valor</span><span class="sxs-lookup"><span data-stu-id="389a5-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="389a5-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="389a5-119">Authorization</span></span>|<span data-ttu-id="389a5-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="389a5-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="389a5-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="389a5-121">Accept</span></span>|<span data-ttu-id="389a5-122">application/json</span><span class="sxs-lookup"><span data-stu-id="389a5-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="389a5-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="389a5-123">Request body</span></span>
<span data-ttu-id="389a5-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto androidCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="389a5-124">In the request body, supply a JSON representation for the androidCompliancePolicy object.</span></span>

<span data-ttu-id="389a5-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto androidCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="389a5-125">The following table shows the properties that are required when you create the androidCompliancePolicy.</span></span>

|<span data-ttu-id="389a5-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="389a5-126">Property</span></span>|<span data-ttu-id="389a5-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="389a5-127">Type</span></span>|<span data-ttu-id="389a5-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="389a5-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="389a5-129">id</span><span class="sxs-lookup"><span data-stu-id="389a5-129">id</span></span>|<span data-ttu-id="389a5-130">String</span><span class="sxs-lookup"><span data-stu-id="389a5-130">String</span></span>|<span data-ttu-id="389a5-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="389a5-131">Key of the entity.</span></span> <span data-ttu-id="389a5-132">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="389a5-132">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="389a5-133">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="389a5-133">createdDateTime</span></span>|<span data-ttu-id="389a5-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="389a5-134">DateTimeOffset</span></span>|<span data-ttu-id="389a5-135">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="389a5-135">DateTime the object was created.</span></span> <span data-ttu-id="389a5-136">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="389a5-136">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="389a5-137">description</span><span class="sxs-lookup"><span data-stu-id="389a5-137">description</span></span>|<span data-ttu-id="389a5-138">String</span><span class="sxs-lookup"><span data-stu-id="389a5-138">String</span></span>|<span data-ttu-id="389a5-139">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="389a5-139">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="389a5-140">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="389a5-140">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="389a5-141">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="389a5-141">lastModifiedDateTime</span></span>|<span data-ttu-id="389a5-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="389a5-142">DateTimeOffset</span></span>|<span data-ttu-id="389a5-143">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="389a5-143">DateTime the object was last modified.</span></span> <span data-ttu-id="389a5-144">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="389a5-144">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="389a5-145">displayName</span><span class="sxs-lookup"><span data-stu-id="389a5-145">displayName</span></span>|<span data-ttu-id="389a5-146">String</span><span class="sxs-lookup"><span data-stu-id="389a5-146">String</span></span>|<span data-ttu-id="389a5-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="389a5-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="389a5-148">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="389a5-148">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="389a5-149">version</span><span class="sxs-lookup"><span data-stu-id="389a5-149">version</span></span>|<span data-ttu-id="389a5-150">Int32</span><span class="sxs-lookup"><span data-stu-id="389a5-150">Int32</span></span>|<span data-ttu-id="389a5-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="389a5-151">Version of the device configuration.</span></span> <span data-ttu-id="389a5-152">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="389a5-152">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="389a5-153">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="389a5-153">passwordRequired</span></span>|<span data-ttu-id="389a5-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="389a5-154">Boolean</span></span>|<span data-ttu-id="389a5-155">Exigir una contraseña para desbloquear el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="389a5-155">Require a password to unlock device.</span></span>|
|<span data-ttu-id="389a5-156">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="389a5-156">passwordMinimumLength</span></span>|<span data-ttu-id="389a5-157">Int32</span><span class="sxs-lookup"><span data-stu-id="389a5-157">Int32</span></span>|<span data-ttu-id="389a5-158">Longitud mínima de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="389a5-158">Minimum password length.</span></span> <span data-ttu-id="389a5-159">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="389a5-159">Valid values 4 to 16</span></span>|
|<span data-ttu-id="389a5-160">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="389a5-160">passwordRequiredType</span></span>|[<span data-ttu-id="389a5-161">androidRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="389a5-161">androidRequiredPasswordType</span></span>](../resources/intune_deviceconfig_androidrequiredpasswordtype.md)|<span data-ttu-id="389a5-162">Tipo de caracteres de contraseña.</span><span class="sxs-lookup"><span data-stu-id="389a5-162">Type of characters in password.</span></span> <span data-ttu-id="389a5-163">Los valores posibles son: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex` y `any`.</span><span class="sxs-lookup"><span data-stu-id="389a5-163">Possible values are: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex`, `any`.</span></span>|
|<span data-ttu-id="389a5-164">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="389a5-164">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="389a5-165">Int32</span><span class="sxs-lookup"><span data-stu-id="389a5-165">Int32</span></span>|<span data-ttu-id="389a5-166">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="389a5-166">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="389a5-167">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="389a5-167">passwordExpirationDays</span></span>|<span data-ttu-id="389a5-168">Int32</span><span class="sxs-lookup"><span data-stu-id="389a5-168">Int32</span></span>|<span data-ttu-id="389a5-169">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="389a5-169">Number of days before the password expires.</span></span> <span data-ttu-id="389a5-170">Valores válidos de 1 a 65535</span><span class="sxs-lookup"><span data-stu-id="389a5-170">Valid values 1 to 65535</span></span>|
|<span data-ttu-id="389a5-171">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="389a5-171">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="389a5-172">Int32</span><span class="sxs-lookup"><span data-stu-id="389a5-172">Int32</span></span>|<span data-ttu-id="389a5-173">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="389a5-173">Number of previous passwords to block.</span></span>|
|<span data-ttu-id="389a5-174">securityPreventInstallAppsFromUnknownSources</span><span class="sxs-lookup"><span data-stu-id="389a5-174">securityPreventInstallAppsFromUnknownSources</span></span>|<span data-ttu-id="389a5-175">Booleano</span><span class="sxs-lookup"><span data-stu-id="389a5-175">Boolean</span></span>|<span data-ttu-id="389a5-176">Exigir que los dispositivos impidan la instalación de aplicaciones de orígenes desconocidos.</span><span class="sxs-lookup"><span data-stu-id="389a5-176">Require that devices disallow installation of apps from unknown sources.</span></span>|
|<span data-ttu-id="389a5-177">securityDisableUsbDebugging</span><span class="sxs-lookup"><span data-stu-id="389a5-177">securityDisableUsbDebugging</span></span>|<span data-ttu-id="389a5-178">Booleano</span><span class="sxs-lookup"><span data-stu-id="389a5-178">Boolean</span></span>|<span data-ttu-id="389a5-179">Deshabilitar la depuración USB en dispositivos Android.</span><span class="sxs-lookup"><span data-stu-id="389a5-179">Disable USB debugging on Android devices.</span></span>|
|<span data-ttu-id="389a5-180">securityRequireVerifyApps</span><span class="sxs-lookup"><span data-stu-id="389a5-180">securityRequireVerifyApps</span></span>|<span data-ttu-id="389a5-181">Booleano</span><span class="sxs-lookup"><span data-stu-id="389a5-181">Boolean</span></span>|<span data-ttu-id="389a5-182">Exigir que la característica Verificar aplicaciones de Android esté activada.</span><span class="sxs-lookup"><span data-stu-id="389a5-182">Require the Android Verify apps feature is turned on.</span></span>|
|<span data-ttu-id="389a5-183">deviceThreatProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="389a5-183">deviceThreatProtectionEnabled</span></span>|<span data-ttu-id="389a5-184">Booleano</span><span class="sxs-lookup"><span data-stu-id="389a5-184">Boolean</span></span>|<span data-ttu-id="389a5-185">Exigir que los dispositivos hayan habilitado la protección contra amenazas de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="389a5-185">Require that devices have enabled device threat protection.</span></span>|
|<span data-ttu-id="389a5-186">deviceThreatProtectionRequiredSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="389a5-186">deviceThreatProtectionRequiredSecurityLevel</span></span>|[<span data-ttu-id="389a5-187">deviceThreatProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="389a5-187">deviceThreatProtectionLevel</span></span>](../resources/intune_deviceconfig_devicethreatprotectionlevel.md)|<span data-ttu-id="389a5-188">Exigir que el nivel de riesgo mínimo de Mobile Threat Protection informe del no cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="389a5-188">Require Mobile Threat Protection minimum risk level to report noncompliance.</span></span> <span data-ttu-id="389a5-189">Los valores posibles son: `unavailable`, `secured`, `low`, `medium`, `high` y `notSet`.</span><span class="sxs-lookup"><span data-stu-id="389a5-189">Possible values are: `unavailable`, `secured`, `low`, `medium`, `high`, `notSet`.</span></span>|
|<span data-ttu-id="389a5-190">securityBlockJailbrokenDevices</span><span class="sxs-lookup"><span data-stu-id="389a5-190">securityBlockJailbrokenDevices</span></span>|<span data-ttu-id="389a5-191">Booleano</span><span class="sxs-lookup"><span data-stu-id="389a5-191">Boolean</span></span>|<span data-ttu-id="389a5-192">No pueden usarse dispositivos con jailbreak o rooting.</span><span class="sxs-lookup"><span data-stu-id="389a5-192">Devices must not be jailbroken or rooted.</span></span>|
|<span data-ttu-id="389a5-193">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="389a5-193">osMinimumVersion</span></span>|<span data-ttu-id="389a5-194">String</span><span class="sxs-lookup"><span data-stu-id="389a5-194">String</span></span>|<span data-ttu-id="389a5-195">Versión mínima de Android.</span><span class="sxs-lookup"><span data-stu-id="389a5-195">Minimum Android version.</span></span>|
|<span data-ttu-id="389a5-196">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="389a5-196">osMaximumVersion</span></span>|<span data-ttu-id="389a5-197">String</span><span class="sxs-lookup"><span data-stu-id="389a5-197">String</span></span>|<span data-ttu-id="389a5-198">Versión máxima de Android.</span><span class="sxs-lookup"><span data-stu-id="389a5-198">Maximum Android version.</span></span>|
|<span data-ttu-id="389a5-199">minAndroidSecurityPatchLevel</span><span class="sxs-lookup"><span data-stu-id="389a5-199">minAndroidSecurityPatchLevel</span></span>|<span data-ttu-id="389a5-200">String</span><span class="sxs-lookup"><span data-stu-id="389a5-200">String</span></span>|<span data-ttu-id="389a5-201">Nivel de revisión de seguridad mínimo de Android.</span><span class="sxs-lookup"><span data-stu-id="389a5-201">Minimum Android security patch level.</span></span>|
|<span data-ttu-id="389a5-202">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="389a5-202">storageRequireEncryption</span></span>|<span data-ttu-id="389a5-203">Booleano</span><span class="sxs-lookup"><span data-stu-id="389a5-203">Boolean</span></span>|<span data-ttu-id="389a5-204">Exigir cifrado en dispositivos Android.</span><span class="sxs-lookup"><span data-stu-id="389a5-204">Require encryption on Android devices.</span></span>|
|<span data-ttu-id="389a5-205">securityRequireSafetyNetAttestationBasicIntegrity</span><span class="sxs-lookup"><span data-stu-id="389a5-205">securityRequireSafetyNetAttestationBasicIntegrity</span></span>|<span data-ttu-id="389a5-206">Booleano</span><span class="sxs-lookup"><span data-stu-id="389a5-206">Boolean</span></span>|<span data-ttu-id="389a5-207">Exigir que el dispositivo supere la comprobación de integridad básica de SafetyNet.</span><span class="sxs-lookup"><span data-stu-id="389a5-207">Require the device to pass the SafetyNet basic integrity check.</span></span>|
|<span data-ttu-id="389a5-208">securityRequireSafetyNetAttestationCertifiedDevice</span><span class="sxs-lookup"><span data-stu-id="389a5-208">securityRequireSafetyNetAttestationCertifiedDevice</span></span>|<span data-ttu-id="389a5-209">Booleano</span><span class="sxs-lookup"><span data-stu-id="389a5-209">Boolean</span></span>|<span data-ttu-id="389a5-210">Exigir que el dispositivo supere la comprobación de dispositivos certificados de SafetyNet.</span><span class="sxs-lookup"><span data-stu-id="389a5-210">Require the device to pass the SafetyNet certified device check.</span></span>|
|<span data-ttu-id="389a5-211">securityRequireGooglePlayServices</span><span class="sxs-lookup"><span data-stu-id="389a5-211">securityRequireGooglePlayServices</span></span>|<span data-ttu-id="389a5-212">Booleano</span><span class="sxs-lookup"><span data-stu-id="389a5-212">Boolean</span></span>|<span data-ttu-id="389a5-213">Exigir que Google Play Services esté instalado y habilitado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="389a5-213">Require Google Play Services to be installed and enabled on the device.</span></span>|
|<span data-ttu-id="389a5-214">securityRequireUpToDateSecurityProviders</span><span class="sxs-lookup"><span data-stu-id="389a5-214">securityRequireUpToDateSecurityProviders</span></span>|<span data-ttu-id="389a5-215">Booleano</span><span class="sxs-lookup"><span data-stu-id="389a5-215">Boolean</span></span>|<span data-ttu-id="389a5-216">Exigir que el dispositivo tenga los proveedores de seguridad actualizados.</span><span class="sxs-lookup"><span data-stu-id="389a5-216">Require the device to have up to date security providers.</span></span> <span data-ttu-id="389a5-217">El dispositivo requerirá que Google Play Services esté instalado y habilitado.</span><span class="sxs-lookup"><span data-stu-id="389a5-217">The device will require Google Play Services to be enabled and up to date.</span></span>|
|<span data-ttu-id="389a5-218">securityRequireCompanyPortalAppIntegrity</span><span class="sxs-lookup"><span data-stu-id="389a5-218">securityRequireCompanyPortalAppIntegrity</span></span>|<span data-ttu-id="389a5-219">Booleano</span><span class="sxs-lookup"><span data-stu-id="389a5-219">Boolean</span></span>|<span data-ttu-id="389a5-220">Exigir que el dispositivo supere la comprobación de integridad en tiempo de ejecución de la aplicación cliente del Portal de empresa.</span><span class="sxs-lookup"><span data-stu-id="389a5-220">Require the device to pass the Company Portal client app runtime integrity check.</span></span>|



## <a name="response"></a><span data-ttu-id="389a5-221">Respuesta</span><span class="sxs-lookup"><span data-stu-id="389a5-221">Response</span></span>
<span data-ttu-id="389a5-222">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [androidCompliancePolicy](../resources/intune_deviceconfig_androidcompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="389a5-222">If successful, this method returns a `201 Created` response code and a [androidCompliancePolicy](../resources/intune_deviceconfig_androidcompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="389a5-223">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="389a5-223">Example</span></span>
### <a name="request"></a><span data-ttu-id="389a5-224">Solicitud</span><span class="sxs-lookup"><span data-stu-id="389a5-224">Request</span></span>
<span data-ttu-id="389a5-225">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="389a5-225">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies
Content-type: application/json
Content-length: 1159

{
  "@odata.type": "#microsoft.graph.androidCompliancePolicy",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "passwordRequired": true,
  "passwordMinimumLength": 5,
  "passwordRequiredType": "alphabetic",
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordExpirationDays": 6,
  "passwordPreviousPasswordBlockCount": 2,
  "securityPreventInstallAppsFromUnknownSources": true,
  "securityDisableUsbDebugging": true,
  "securityRequireVerifyApps": true,
  "deviceThreatProtectionEnabled": true,
  "deviceThreatProtectionRequiredSecurityLevel": "secured",
  "securityBlockJailbrokenDevices": true,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "minAndroidSecurityPatchLevel": "Min Android Security Patch Level value",
  "storageRequireEncryption": true,
  "securityRequireSafetyNetAttestationBasicIntegrity": true,
  "securityRequireSafetyNetAttestationCertifiedDevice": true,
  "securityRequireGooglePlayServices": true,
  "securityRequireUpToDateSecurityProviders": true,
  "securityRequireCompanyPortalAppIntegrity": true
}
```

### <a name="response"></a><span data-ttu-id="389a5-226">Respuesta</span><span class="sxs-lookup"><span data-stu-id="389a5-226">Response</span></span>
<span data-ttu-id="389a5-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="389a5-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1331

{
  "@odata.type": "#microsoft.graph.androidCompliancePolicy",
  "id": "752c820f-820f-752c-0f82-2c750f822c75",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "passwordRequired": true,
  "passwordMinimumLength": 5,
  "passwordRequiredType": "alphabetic",
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordExpirationDays": 6,
  "passwordPreviousPasswordBlockCount": 2,
  "securityPreventInstallAppsFromUnknownSources": true,
  "securityDisableUsbDebugging": true,
  "securityRequireVerifyApps": true,
  "deviceThreatProtectionEnabled": true,
  "deviceThreatProtectionRequiredSecurityLevel": "secured",
  "securityBlockJailbrokenDevices": true,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "minAndroidSecurityPatchLevel": "Min Android Security Patch Level value",
  "storageRequireEncryption": true,
  "securityRequireSafetyNetAttestationBasicIntegrity": true,
  "securityRequireSafetyNetAttestationCertifiedDevice": true,
  "securityRequireGooglePlayServices": true,
  "securityRequireUpToDateSecurityProviders": true,
  "securityRequireCompanyPortalAppIntegrity": true
}
```



