# <a name="create-androidcompliancepolicy"></a><span data-ttu-id="524a1-101">Crear androidCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="524a1-101">Create androidCompliancePolicy</span></span>

> <span data-ttu-id="524a1-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="524a1-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="524a1-103">Cree un objeto [androidCompliancePolicy](../resources/intune_deviceconfig_androidcompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="524a1-103">Create a new [plannerBucket](../resources/intune_deviceconfig_androidcompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="524a1-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="524a1-104">Prerequisites</span></span>
<span data-ttu-id="524a1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="524a1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="524a1-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="524a1-107">Permission type</span></span>|<span data-ttu-id="524a1-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="524a1-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="524a1-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="524a1-109">Delegated (work or school account)</span></span>|<span data-ttu-id="524a1-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="524a1-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="524a1-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="524a1-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="524a1-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="524a1-112">Not supported.</span></span>|
|<span data-ttu-id="524a1-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="524a1-113">Application</span></span>|<span data-ttu-id="524a1-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="524a1-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="524a1-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="524a1-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="524a1-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="524a1-116">Request headers</span></span>
|<span data-ttu-id="524a1-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="524a1-117">Header</span></span>|<span data-ttu-id="524a1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="524a1-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="524a1-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="524a1-119">Authorization</span></span>|<span data-ttu-id="524a1-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="524a1-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="524a1-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="524a1-121">Accept</span></span>|<span data-ttu-id="524a1-122">application/json</span><span class="sxs-lookup"><span data-stu-id="524a1-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="524a1-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="524a1-123">Request body</span></span>
<span data-ttu-id="524a1-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto androidCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="524a1-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="524a1-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto androidCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="524a1-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="524a1-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="524a1-126">Property</span></span>|<span data-ttu-id="524a1-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="524a1-127">Type</span></span>|<span data-ttu-id="524a1-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="524a1-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="524a1-129">id</span><span class="sxs-lookup"><span data-stu-id="524a1-129">id</span></span>|<span data-ttu-id="524a1-130">String</span><span class="sxs-lookup"><span data-stu-id="524a1-130">String</span></span>|<span data-ttu-id="524a1-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="524a1-131">Key of the setting.</span></span> <span data-ttu-id="524a1-132">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="524a1-132">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="524a1-133">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="524a1-133">createdDateTime</span></span>|<span data-ttu-id="524a1-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="524a1-134">DateTimeOffset</span></span>|<span data-ttu-id="524a1-135">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="524a1-135">DateTime the object was created.</span></span> <span data-ttu-id="524a1-136">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="524a1-136">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="524a1-137">description</span><span class="sxs-lookup"><span data-stu-id="524a1-137">description</span></span>|<span data-ttu-id="524a1-138">String</span><span class="sxs-lookup"><span data-stu-id="524a1-138">String</span></span>|<span data-ttu-id="524a1-139">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="524a1-139">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="524a1-140">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="524a1-140">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="524a1-141">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="524a1-141">lastModifiedDateTime</span></span>|<span data-ttu-id="524a1-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="524a1-142">DateTimeOffset</span></span>|<span data-ttu-id="524a1-143">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="524a1-143">Indicates the date the object was last modified.</span></span> <span data-ttu-id="524a1-144">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="524a1-144">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="524a1-145">displayName</span><span class="sxs-lookup"><span data-stu-id="524a1-145">displayName</span></span>|<span data-ttu-id="524a1-146">String</span><span class="sxs-lookup"><span data-stu-id="524a1-146">String</span></span>|<span data-ttu-id="524a1-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="524a1-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="524a1-148">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="524a1-148">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="524a1-149">version</span><span class="sxs-lookup"><span data-stu-id="524a1-149">version</span></span>|<span data-ttu-id="524a1-150">Int32</span><span class="sxs-lookup"><span data-stu-id="524a1-150">Int32</span></span>|<span data-ttu-id="524a1-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="524a1-151">Version of the device configuration.</span></span> <span data-ttu-id="524a1-152">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="524a1-152">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="524a1-153">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="524a1-153">passwordRequired</span></span>|<span data-ttu-id="524a1-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="524a1-154">Boolean</span></span>|<span data-ttu-id="524a1-155">Exigir una contraseña para desbloquear el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="524a1-155">Require a password to unlock device.</span></span>|
|<span data-ttu-id="524a1-156">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="524a1-156">passwordMinimumLength</span></span>|<span data-ttu-id="524a1-157">Int32</span><span class="sxs-lookup"><span data-stu-id="524a1-157">Int32</span></span>|<span data-ttu-id="524a1-158">Longitud mínima de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="524a1-158">Minimum password length.</span></span> <span data-ttu-id="524a1-159">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="524a1-159">Valid values 4 to 16</span></span>|
|<span data-ttu-id="524a1-160">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="524a1-160">passwordRequiredType</span></span>|<span data-ttu-id="524a1-161">String</span><span class="sxs-lookup"><span data-stu-id="524a1-161">String</span></span>|<span data-ttu-id="524a1-162">Tipo de caracteres en la contraseña. Los valores posibles son: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex` y `any`.</span><span class="sxs-lookup"><span data-stu-id="524a1-162">Type of characters in password Possible values are: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex`, `any`.</span></span>|
|<span data-ttu-id="524a1-163">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="524a1-163">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="524a1-164">Int32</span><span class="sxs-lookup"><span data-stu-id="524a1-164">Int32</span></span>|<span data-ttu-id="524a1-165">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="524a1-165">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="524a1-166">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="524a1-166">passwordExpirationDays</span></span>|<span data-ttu-id="524a1-167">Int32</span><span class="sxs-lookup"><span data-stu-id="524a1-167">Int32</span></span>|<span data-ttu-id="524a1-168">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="524a1-168">Number of days before the password expires.</span></span> <span data-ttu-id="524a1-169">Valores válidos de 1 a 365</span><span class="sxs-lookup"><span data-stu-id="524a1-169">Valid values 1 to 365</span></span>|
|<span data-ttu-id="524a1-170">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="524a1-170">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="524a1-171">Int32</span><span class="sxs-lookup"><span data-stu-id="524a1-171">Int32</span></span>|<span data-ttu-id="524a1-172">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="524a1-172">Number of previous passwords to block.</span></span>|
|<span data-ttu-id="524a1-173">securityPreventInstallAppsFromUnknownSources</span><span class="sxs-lookup"><span data-stu-id="524a1-173">securityPreventInstallAppsFromUnknownSources</span></span>|<span data-ttu-id="524a1-174">Booleano</span><span class="sxs-lookup"><span data-stu-id="524a1-174">Boolean</span></span>|<span data-ttu-id="524a1-175">Exigir que los dispositivos impidan la instalación de aplicaciones de orígenes desconocidos.</span><span class="sxs-lookup"><span data-stu-id="524a1-175">Require that devices disallow installation of apps from unknown sources.</span></span>|
|<span data-ttu-id="524a1-176">securityDisableUsbDebugging</span><span class="sxs-lookup"><span data-stu-id="524a1-176">securityDisableUsbDebugging</span></span>|<span data-ttu-id="524a1-177">Booleano</span><span class="sxs-lookup"><span data-stu-id="524a1-177">Boolean</span></span>|<span data-ttu-id="524a1-178">Deshabilitar la depuración USB en dispositivos Android.</span><span class="sxs-lookup"><span data-stu-id="524a1-178">Disable USB debugging on Android devices.</span></span>|
|<span data-ttu-id="524a1-179">securityRequireVerifyApps</span><span class="sxs-lookup"><span data-stu-id="524a1-179">securityRequireVerifyApps</span></span>|<span data-ttu-id="524a1-180">Booleano</span><span class="sxs-lookup"><span data-stu-id="524a1-180">Boolean</span></span>|<span data-ttu-id="524a1-181">Exigir que la característica Verificar aplicaciones de Android esté activada.</span><span class="sxs-lookup"><span data-stu-id="524a1-181">Require the Android Verify apps feature is turned on.</span></span>|
|<span data-ttu-id="524a1-182">deviceThreatProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="524a1-182">deviceThreatProtectionEnabled</span></span>|<span data-ttu-id="524a1-183">Booleano</span><span class="sxs-lookup"><span data-stu-id="524a1-183">Boolean</span></span>|<span data-ttu-id="524a1-184">Exigir que los dispositivos hayan habilitado la protección contra amenazas de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="524a1-184">Require that devices have enabled device threat protection.</span></span>|
|<span data-ttu-id="524a1-185">deviceThreatProtectionRequiredSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="524a1-185">deviceThreatProtectionRequiredSecurityLevel</span></span>|<span data-ttu-id="524a1-186">String</span><span class="sxs-lookup"><span data-stu-id="524a1-186">String</span></span>|<span data-ttu-id="524a1-187">Exigir que el nivel de riesgo mínimo de Mobile Threat Protection informe del no cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="524a1-187">Require Mobile Threat Protection minimum risk level to report noncompliance.</span></span> <span data-ttu-id="524a1-188">Los valores posibles son: `unavailable`, `secured`, `low`, `medium`, `high` y `notSet`.</span><span class="sxs-lookup"><span data-stu-id="524a1-188">Possible values are: `unavailable`, `secured`, `low`, `medium`, `high`, `notSet`.</span></span>|
|<span data-ttu-id="524a1-189">securityBlockJailbrokenDevices</span><span class="sxs-lookup"><span data-stu-id="524a1-189">securityBlockJailbrokenDevices</span></span>|<span data-ttu-id="524a1-190">Booleano</span><span class="sxs-lookup"><span data-stu-id="524a1-190">Boolean</span></span>|<span data-ttu-id="524a1-191">No pueden usarse dispositivos con jailbreak o rooting.</span><span class="sxs-lookup"><span data-stu-id="524a1-191">Devices must not be jailbroken or rooted.</span></span>|
|<span data-ttu-id="524a1-192">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="524a1-192">osMinimumVersion</span></span>|<span data-ttu-id="524a1-193">String</span><span class="sxs-lookup"><span data-stu-id="524a1-193">String</span></span>|<span data-ttu-id="524a1-194">Versión mínima de Android.</span><span class="sxs-lookup"><span data-stu-id="524a1-194">Minimum Android version.</span></span>|
|<span data-ttu-id="524a1-195">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="524a1-195">osMaximumVersion</span></span>|<span data-ttu-id="524a1-196">String</span><span class="sxs-lookup"><span data-stu-id="524a1-196">String</span></span>|<span data-ttu-id="524a1-197">Versión máxima de Android.</span><span class="sxs-lookup"><span data-stu-id="524a1-197">Maximum Android version.</span></span>|
|<span data-ttu-id="524a1-198">minAndroidSecurityPatchLevel</span><span class="sxs-lookup"><span data-stu-id="524a1-198">minAndroidSecurityPatchLevel</span></span>|<span data-ttu-id="524a1-199">String</span><span class="sxs-lookup"><span data-stu-id="524a1-199">String</span></span>|<span data-ttu-id="524a1-200">Nivel de revisión de seguridad mínimo de Android.</span><span class="sxs-lookup"><span data-stu-id="524a1-200">Minimum Android security patch level.</span></span>|
|<span data-ttu-id="524a1-201">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="524a1-201">storageRequireEncryption</span></span>|<span data-ttu-id="524a1-202">Booleano</span><span class="sxs-lookup"><span data-stu-id="524a1-202">Boolean</span></span>|<span data-ttu-id="524a1-203">Exigir cifrado en dispositivos Android.</span><span class="sxs-lookup"><span data-stu-id="524a1-203">Require encryption on Android devices.</span></span>|
|<span data-ttu-id="524a1-204">securityRequireSafetyNetAttestationBasicIntegrity</span><span class="sxs-lookup"><span data-stu-id="524a1-204">securityRequireSafetyNetAttestationBasicIntegrity</span></span>|<span data-ttu-id="524a1-205">Booleano</span><span class="sxs-lookup"><span data-stu-id="524a1-205">Boolean</span></span>|<span data-ttu-id="524a1-206">Exigir que el dispositivo supere la comprobación de integridad básica de SafetyNet.</span><span class="sxs-lookup"><span data-stu-id="524a1-206">Require the device to pass the SafetyNet basic integrity check.</span></span>|
|<span data-ttu-id="524a1-207">securityRequireSafetyNetAttestationCertifiedDevice</span><span class="sxs-lookup"><span data-stu-id="524a1-207">securityRequireSafetyNetAttestationCertifiedDevice</span></span>|<span data-ttu-id="524a1-208">Booleano</span><span class="sxs-lookup"><span data-stu-id="524a1-208">Boolean</span></span>|<span data-ttu-id="524a1-209">Exigir que el dispositivo supere la comprobación de dispositivos certificados de SafetyNet.</span><span class="sxs-lookup"><span data-stu-id="524a1-209">Require the device to pass the SafetyNet certified device check.</span></span>|
|<span data-ttu-id="524a1-210">securityRequireGooglePlayServices</span><span class="sxs-lookup"><span data-stu-id="524a1-210">securityRequireGooglePlayServices</span></span>|<span data-ttu-id="524a1-211">Booleano</span><span class="sxs-lookup"><span data-stu-id="524a1-211">Boolean</span></span>|<span data-ttu-id="524a1-212">Exigir que Google Play Services esté instalado y habilitado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="524a1-212">Require Google Play Services to be installed and enabled on the device.</span></span>|
|<span data-ttu-id="524a1-213">securityRequireUpToDateSecurityProviders</span><span class="sxs-lookup"><span data-stu-id="524a1-213">securityRequireUpToDateSecurityProviders</span></span>|<span data-ttu-id="524a1-214">Booleano</span><span class="sxs-lookup"><span data-stu-id="524a1-214">Boolean</span></span>|<span data-ttu-id="524a1-215">Exigir que el dispositivo tenga los proveedores de seguridad actualizados.</span><span class="sxs-lookup"><span data-stu-id="524a1-215">Require the device to have up to date security providers.</span></span> <span data-ttu-id="524a1-216">El dispositivo requerirá que Google Play Services esté instalado y habilitado.</span><span class="sxs-lookup"><span data-stu-id="524a1-216">The device will require Google Play Services to be enabled and up to date.</span></span>|
|<span data-ttu-id="524a1-217">securityRequireCompanyPortalAppIntegrity</span><span class="sxs-lookup"><span data-stu-id="524a1-217">securityRequireCompanyPortalAppIntegrity</span></span>|<span data-ttu-id="524a1-218">Booleano</span><span class="sxs-lookup"><span data-stu-id="524a1-218">Boolean</span></span>|<span data-ttu-id="524a1-219">Exigir que el dispositivo supere la comprobación de integridad en tiempo de ejecución de la aplicación cliente del Portal de empresa.</span><span class="sxs-lookup"><span data-stu-id="524a1-219">Require the device to pass the Company Portal client app runtime integrity check.</span></span>|



## <a name="response"></a><span data-ttu-id="524a1-220">Respuesta</span><span class="sxs-lookup"><span data-stu-id="524a1-220">Response</span></span>
<span data-ttu-id="524a1-221">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [androidCompliancePolicy](../resources/intune_deviceconfig_androidcompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="524a1-221">If successful, this method returns a `201 Created` response code and a [DriveItemVersion](../resources/intune_deviceconfig_androidcompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="524a1-222">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="524a1-222">Example</span></span>
### <a name="request"></a><span data-ttu-id="524a1-223">Solicitud</span><span class="sxs-lookup"><span data-stu-id="524a1-223">Request</span></span>
<span data-ttu-id="524a1-224">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="524a1-224">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies
Content-type: application/json
Content-length: 1223

{
  "@odata.type": "#microsoft.graph.androidCompliancePolicy",
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

### <a name="response"></a><span data-ttu-id="524a1-225">Respuesta</span><span class="sxs-lookup"><span data-stu-id="524a1-225">Response</span></span>
<span data-ttu-id="524a1-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="524a1-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



