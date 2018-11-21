# <a name="create-androidworkprofilecompliancepolicy"></a><span data-ttu-id="2239a-101">Crear androidWorkProfileCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="2239a-101">Create androidWorkProfileCompliancePolicy</span></span>

> <span data-ttu-id="2239a-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2239a-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2239a-103">Crear un nuevo objeto [androidWorkProfileCompliancePolicy](../resources/intune_deviceconfig_androidworkprofilecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2239a-103">Create a new [editionUpgradeConfiguration](../resources/intune_deviceconfig_androidworkprofilecompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2239a-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2239a-104">Prerequisites</span></span>
<span data-ttu-id="2239a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="2239a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="2239a-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2239a-107">Permission type</span></span>|<span data-ttu-id="2239a-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2239a-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2239a-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2239a-109">Delegated (work or school account)</span></span>|<span data-ttu-id="2239a-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2239a-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="2239a-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2239a-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2239a-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2239a-112">Not supported.</span></span>|
|<span data-ttu-id="2239a-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2239a-113">Application</span></span>|<span data-ttu-id="2239a-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2239a-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2239a-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2239a-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="2239a-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2239a-116">Request headers</span></span>
|<span data-ttu-id="2239a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2239a-117">Header</span></span>|<span data-ttu-id="2239a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2239a-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2239a-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="2239a-119">Authorization</span></span>|<span data-ttu-id="2239a-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2239a-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2239a-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="2239a-121">Accept</span></span>|<span data-ttu-id="2239a-122">application/json</span><span class="sxs-lookup"><span data-stu-id="2239a-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2239a-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2239a-123">Request body</span></span>
<span data-ttu-id="2239a-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto androidWorkProfileCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="2239a-124">In the request body, supply a JSON representation for the mobileAppContentFile object.</span></span>

<span data-ttu-id="2239a-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto androidWorkProfileCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="2239a-125">The following table shows the properties that are required when you create the deviceComplianceUserOverview.</span></span>

|<span data-ttu-id="2239a-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2239a-126">Property</span></span>|<span data-ttu-id="2239a-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="2239a-127">Type</span></span>|<span data-ttu-id="2239a-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="2239a-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2239a-129">id.</span><span class="sxs-lookup"><span data-stu-id="2239a-129">id</span></span>|<span data-ttu-id="2239a-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="2239a-130">String</span></span>|<span data-ttu-id="2239a-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="2239a-131">Key of the entity.</span></span> <span data-ttu-id="2239a-132">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2239a-132">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="2239a-133">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="2239a-133">createdDateTime</span></span>|<span data-ttu-id="2239a-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2239a-134">DateTimeOffset</span></span>|<span data-ttu-id="2239a-135">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="2239a-135">DateTime the object was created.</span></span> <span data-ttu-id="2239a-136">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2239a-136">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="2239a-137">descripción</span><span class="sxs-lookup"><span data-stu-id="2239a-137">description</span></span>|<span data-ttu-id="2239a-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="2239a-138">String</span></span>|<span data-ttu-id="2239a-139">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2239a-139">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="2239a-140">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2239a-140">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="2239a-141">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="2239a-141">lastModifiedDateTime</span></span>|<span data-ttu-id="2239a-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2239a-142">DateTimeOffset</span></span>|<span data-ttu-id="2239a-143">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="2239a-143">DateTime the object was last modified.</span></span> <span data-ttu-id="2239a-144">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2239a-144">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="2239a-145">displayName</span><span class="sxs-lookup"><span data-stu-id="2239a-145">displayName</span></span>|<span data-ttu-id="2239a-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="2239a-146">String</span></span>|<span data-ttu-id="2239a-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2239a-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="2239a-148">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2239a-148">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="2239a-149">versión</span><span class="sxs-lookup"><span data-stu-id="2239a-149">version</span></span>|<span data-ttu-id="2239a-150">Int32</span><span class="sxs-lookup"><span data-stu-id="2239a-150">Int32</span></span>|<span data-ttu-id="2239a-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2239a-151">Version of the device configuration.</span></span> <span data-ttu-id="2239a-152">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2239a-152">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="2239a-153">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="2239a-153">passwordRequired</span></span>|<span data-ttu-id="2239a-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="2239a-154">Boolean</span></span>|<span data-ttu-id="2239a-155">Exigir una contraseña para desbloquear el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2239a-155">Require a password to unlock device.</span></span>|
|<span data-ttu-id="2239a-156">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="2239a-156">passwordMinimumLength</span></span>|<span data-ttu-id="2239a-157">Int32</span><span class="sxs-lookup"><span data-stu-id="2239a-157">Int32</span></span>|<span data-ttu-id="2239a-158">Longitud mínima de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="2239a-158">Minimum password length.</span></span> <span data-ttu-id="2239a-159">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="2239a-159">Valid values 4 to 16</span></span>|
|<span data-ttu-id="2239a-160">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="2239a-160">passwordRequiredType</span></span>|[<span data-ttu-id="2239a-161">androidRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="2239a-161">androidRequiredPasswordType</span></span>](../resources/intune_deviceconfig_androidrequiredpasswordtype.md)|<span data-ttu-id="2239a-162">Tipo de caracteres en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="2239a-162">Type of characters in password Possible values are: , , , , , , , .</span></span> <span data-ttu-id="2239a-163">Los valores posibles son: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex` y `any`.</span><span class="sxs-lookup"><span data-stu-id="2239a-163">Possible values are: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex`, `any`.</span></span>|
|<span data-ttu-id="2239a-164">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="2239a-164">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="2239a-165">Int32</span><span class="sxs-lookup"><span data-stu-id="2239a-165">Int32</span></span>|<span data-ttu-id="2239a-166">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="2239a-166">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="2239a-167">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="2239a-167">passwordExpirationDays</span></span>|<span data-ttu-id="2239a-168">Int32</span><span class="sxs-lookup"><span data-stu-id="2239a-168">Int32</span></span>|<span data-ttu-id="2239a-169">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="2239a-169">Number of days before the password expires.</span></span> <span data-ttu-id="2239a-170">Valores válidos de 1 a 365</span><span class="sxs-lookup"><span data-stu-id="2239a-170">Valid values 1 to 365</span></span>|
|<span data-ttu-id="2239a-171">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="2239a-171">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="2239a-172">Int32</span><span class="sxs-lookup"><span data-stu-id="2239a-172">Int32</span></span>|<span data-ttu-id="2239a-173">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="2239a-173">Number of previous passwords to block.</span></span>|
|<span data-ttu-id="2239a-174">securityPreventInstallAppsFromUnknownSources</span><span class="sxs-lookup"><span data-stu-id="2239a-174">securityPreventInstallAppsFromUnknownSources</span></span>|<span data-ttu-id="2239a-175">Booleano</span><span class="sxs-lookup"><span data-stu-id="2239a-175">Boolean</span></span>|<span data-ttu-id="2239a-176">Exigir que los dispositivos impidan la instalación de aplicaciones de orígenes desconocidos.</span><span class="sxs-lookup"><span data-stu-id="2239a-176">Require that devices disallow installation of apps from unknown sources.</span></span>|
|<span data-ttu-id="2239a-177">securityDisableUsbDebugging</span><span class="sxs-lookup"><span data-stu-id="2239a-177">securityDisableUsbDebugging</span></span>|<span data-ttu-id="2239a-178">Booleano</span><span class="sxs-lookup"><span data-stu-id="2239a-178">Boolean</span></span>|<span data-ttu-id="2239a-179">Deshabilitar la depuración USB en dispositivos Android.</span><span class="sxs-lookup"><span data-stu-id="2239a-179">Disable USB debugging on Android devices.</span></span>|
|<span data-ttu-id="2239a-180">securityRequireVerifyApps</span><span class="sxs-lookup"><span data-stu-id="2239a-180">securityRequireVerifyApps</span></span>|<span data-ttu-id="2239a-181">Booleano</span><span class="sxs-lookup"><span data-stu-id="2239a-181">Boolean</span></span>|<span data-ttu-id="2239a-182">Exigir que la característica Verificar aplicaciones de Android esté activada.</span><span class="sxs-lookup"><span data-stu-id="2239a-182">Require the Android Verify apps feature is turned on.</span></span>|
|<span data-ttu-id="2239a-183">deviceThreatProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="2239a-183">deviceThreatProtectionEnabled</span></span>|<span data-ttu-id="2239a-184">Booleano</span><span class="sxs-lookup"><span data-stu-id="2239a-184">Boolean</span></span>|<span data-ttu-id="2239a-185">Exigir que los dispositivos hayan habilitado la protección contra amenazas de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2239a-185">Require that devices have enabled device threat protection.</span></span>|
|<span data-ttu-id="2239a-186">deviceThreatProtectionRequiredSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="2239a-186">deviceThreatProtectionRequiredSecurityLevel</span></span>|[<span data-ttu-id="2239a-187">deviceThreatProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="2239a-187">deviceThreatProtectionLevel</span></span>](../resources/intune_deviceconfig_devicethreatprotectionlevel.md)|<span data-ttu-id="2239a-188">Exigir que el nivel de riesgo mínimo de Mobile Threat Protection informe del no cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="2239a-188">Require Mobile Threat Protection minimum risk level to report noncompliance.</span></span> <span data-ttu-id="2239a-189">Los valores posibles son: `unavailable`, `secured`, `low`, `medium`, `high` y `notSet`.</span><span class="sxs-lookup"><span data-stu-id="2239a-189">Possible values are: `unavailable`, `secured`, `low`, `medium`, `high`, `notSet`.</span></span>|
|<span data-ttu-id="2239a-190">securityBlockJailbrokenDevices</span><span class="sxs-lookup"><span data-stu-id="2239a-190">securityBlockJailbrokenDevices</span></span>|<span data-ttu-id="2239a-191">Booleano</span><span class="sxs-lookup"><span data-stu-id="2239a-191">Boolean</span></span>|<span data-ttu-id="2239a-192">No pueden usarse dispositivos con jailbreak o rooting.</span><span class="sxs-lookup"><span data-stu-id="2239a-192">Devices must not be jailbroken or rooted.</span></span>|
|<span data-ttu-id="2239a-193">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="2239a-193">osMinimumVersion</span></span>|<span data-ttu-id="2239a-194">Cadena</span><span class="sxs-lookup"><span data-stu-id="2239a-194">String</span></span>|<span data-ttu-id="2239a-195">Versión mínima de Android.</span><span class="sxs-lookup"><span data-stu-id="2239a-195">Minimum Android version.</span></span>|
|<span data-ttu-id="2239a-196">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="2239a-196">osMaximumVersion</span></span>|<span data-ttu-id="2239a-197">Cadena</span><span class="sxs-lookup"><span data-stu-id="2239a-197">String</span></span>|<span data-ttu-id="2239a-198">Versión máxima de Android.</span><span class="sxs-lookup"><span data-stu-id="2239a-198">Maximum Android version.</span></span>|
|<span data-ttu-id="2239a-199">minAndroidSecurityPatchLevel</span><span class="sxs-lookup"><span data-stu-id="2239a-199">minAndroidSecurityPatchLevel</span></span>|<span data-ttu-id="2239a-200">Cadena</span><span class="sxs-lookup"><span data-stu-id="2239a-200">String</span></span>|<span data-ttu-id="2239a-201">Nivel de revisión de seguridad mínimo de Android.</span><span class="sxs-lookup"><span data-stu-id="2239a-201">Minimum Android security patch level.</span></span>|
|<span data-ttu-id="2239a-202">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="2239a-202">storageRequireEncryption</span></span>|<span data-ttu-id="2239a-203">Booleano</span><span class="sxs-lookup"><span data-stu-id="2239a-203">Boolean</span></span>|<span data-ttu-id="2239a-204">Exigir cifrado en dispositivos Android.</span><span class="sxs-lookup"><span data-stu-id="2239a-204">Require encryption on Android devices.</span></span>|
|<span data-ttu-id="2239a-205">securityRequireSafetyNetAttestationBasicIntegrity</span><span class="sxs-lookup"><span data-stu-id="2239a-205">securityRequireSafetyNetAttestationBasicIntegrity</span></span>|<span data-ttu-id="2239a-206">Booleano</span><span class="sxs-lookup"><span data-stu-id="2239a-206">Boolean</span></span>|<span data-ttu-id="2239a-207">Exigir que el dispositivo supere la comprobación de integridad básica de SafetyNet.</span><span class="sxs-lookup"><span data-stu-id="2239a-207">Require the device to pass the SafetyNet basic integrity check.</span></span>|
|<span data-ttu-id="2239a-208">securityRequireSafetyNetAttestationCertifiedDevice</span><span class="sxs-lookup"><span data-stu-id="2239a-208">securityRequireSafetyNetAttestationCertifiedDevice</span></span>|<span data-ttu-id="2239a-209">Booleano</span><span class="sxs-lookup"><span data-stu-id="2239a-209">Boolean</span></span>|<span data-ttu-id="2239a-210">Exigir que el dispositivo supere la comprobación de dispositivos certificados de SafetyNet.</span><span class="sxs-lookup"><span data-stu-id="2239a-210">Require the device to pass the SafetyNet certified device check.</span></span>|
|<span data-ttu-id="2239a-211">securityRequireGooglePlayServices</span><span class="sxs-lookup"><span data-stu-id="2239a-211">securityRequireGooglePlayServices</span></span>|<span data-ttu-id="2239a-212">Booleano</span><span class="sxs-lookup"><span data-stu-id="2239a-212">Boolean</span></span>|<span data-ttu-id="2239a-213">Exigir que Google Play Services esté instalado y habilitado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2239a-213">Require Google Play Services to be installed and enabled on the device.</span></span>|
|<span data-ttu-id="2239a-214">securityRequireUpToDateSecurityProviders</span><span class="sxs-lookup"><span data-stu-id="2239a-214">securityRequireUpToDateSecurityProviders</span></span>|<span data-ttu-id="2239a-215">Booleano</span><span class="sxs-lookup"><span data-stu-id="2239a-215">Boolean</span></span>|<span data-ttu-id="2239a-216">Exigir que el dispositivo tenga los proveedores de seguridad actualizados.</span><span class="sxs-lookup"><span data-stu-id="2239a-216">Require the device to have up to date security providers.</span></span> <span data-ttu-id="2239a-217">El dispositivo requerirá que Google Play Services esté instalado y habilitado.</span><span class="sxs-lookup"><span data-stu-id="2239a-217">The device will require Google Play Services to be enabled and up to date.</span></span>|
|<span data-ttu-id="2239a-218">securityRequireCompanyPortalAppIntegrity</span><span class="sxs-lookup"><span data-stu-id="2239a-218">securityRequireCompanyPortalAppIntegrity</span></span>|<span data-ttu-id="2239a-219">Booleano</span><span class="sxs-lookup"><span data-stu-id="2239a-219">Boolean</span></span>|<span data-ttu-id="2239a-220">Exigir que el dispositivo supere la comprobación de integridad en tiempo de ejecución de la aplicación cliente del Portal de empresa.</span><span class="sxs-lookup"><span data-stu-id="2239a-220">Require the device to pass the Company Portal client app runtime integrity check.</span></span>|



## <a name="response"></a><span data-ttu-id="2239a-221">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2239a-221">Response</span></span>
<span data-ttu-id="2239a-222">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [androidWorkProfileCompliancePolicy](../resources/intune_deviceconfig_androidworkprofilecompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2239a-222">If successful, this method returns a `201 Created` response code and a [deviceConfigurationDeviceStatus](../resources/intune_deviceconfig_androidworkprofilecompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2239a-223">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2239a-223">Example</span></span>
### <a name="request"></a><span data-ttu-id="2239a-224">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2239a-224">Request</span></span>
<span data-ttu-id="2239a-225">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2239a-225">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies
Content-type: application/json
Content-length: 1234

{
  "@odata.type": "#microsoft.graph.androidWorkProfileCompliancePolicy",
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

### <a name="response"></a><span data-ttu-id="2239a-226">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2239a-226">Response</span></span>
<span data-ttu-id="2239a-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2239a-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1342

{
  "@odata.type": "#microsoft.graph.androidWorkProfileCompliancePolicy",
  "id": "4e385271-5271-4e38-7152-384e7152384e",
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







