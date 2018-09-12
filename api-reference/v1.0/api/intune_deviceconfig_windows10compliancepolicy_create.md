# <a name="create-windows10compliancepolicy"></a><span data-ttu-id="fa2b4-101">Crear windows10CompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="fa2b4-101">Create windows10CompliancePolicy</span></span>

> <span data-ttu-id="fa2b4-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fa2b4-103">Cree un objeto [windows10CompliancePolicy](../resources/intune_deviceconfig_windows10compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="fa2b4-103">Create a new [windows10CompliancePolicy](../resources/intune_deviceconfig_windows10compliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fa2b4-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fa2b4-104">Prerequisites</span></span>
<span data-ttu-id="fa2b4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="fa2b4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="fa2b4-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fa2b4-107">Permission type</span></span>|<span data-ttu-id="fa2b4-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fa2b4-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="fa2b4-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fa2b4-109">Delegated (work or school account)</span></span>|<span data-ttu-id="fa2b4-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fa2b4-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="fa2b4-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fa2b4-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="fa2b4-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-112">Not supported.</span></span>|
|<span data-ttu-id="fa2b4-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fa2b4-113">Application</span></span>|<span data-ttu-id="fa2b4-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="fa2b4-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fa2b4-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="fa2b4-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fa2b4-116">Request headers</span></span>
|<span data-ttu-id="fa2b4-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fa2b4-117">Header</span></span>|<span data-ttu-id="fa2b4-118">Valor</span><span class="sxs-lookup"><span data-stu-id="fa2b4-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="fa2b4-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="fa2b4-119">Authorization</span></span>|<span data-ttu-id="fa2b4-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="fa2b4-121">Accept</span><span class="sxs-lookup"><span data-stu-id="fa2b4-121">Accept</span></span>|<span data-ttu-id="fa2b4-122">application/json</span><span class="sxs-lookup"><span data-stu-id="fa2b4-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fa2b4-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fa2b4-123">Request body</span></span>
<span data-ttu-id="fa2b4-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto windows10CompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-124">In the request body, supply a JSON representation for the windows10CompliancePolicy object.</span></span>

<span data-ttu-id="fa2b4-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windows10CompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-125">The following table shows the properties that are required when you create the windows10CompliancePolicy.</span></span>

|<span data-ttu-id="fa2b4-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fa2b4-126">Property</span></span>|<span data-ttu-id="fa2b4-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="fa2b4-127">Type</span></span>|<span data-ttu-id="fa2b4-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa2b4-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fa2b4-129">id</span><span class="sxs-lookup"><span data-stu-id="fa2b4-129">id</span></span>|<span data-ttu-id="fa2b4-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="fa2b4-130">String</span></span>|<span data-ttu-id="fa2b4-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-131">Key of the entity.</span></span> <span data-ttu-id="fa2b4-132">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="fa2b4-132">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="fa2b4-133">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="fa2b4-133">createdDateTime</span></span>|<span data-ttu-id="fa2b4-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="fa2b4-134">DateTimeOffset</span></span>|<span data-ttu-id="fa2b4-135">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-135">DateTime the object was created.</span></span> <span data-ttu-id="fa2b4-136">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="fa2b4-136">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="fa2b4-137">description</span><span class="sxs-lookup"><span data-stu-id="fa2b4-137">description</span></span>|<span data-ttu-id="fa2b4-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="fa2b4-138">String</span></span>|<span data-ttu-id="fa2b4-139">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-139">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="fa2b4-140">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="fa2b4-140">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="fa2b4-141">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="fa2b4-141">lastModifiedDateTime</span></span>|<span data-ttu-id="fa2b4-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="fa2b4-142">DateTimeOffset</span></span>|<span data-ttu-id="fa2b4-143">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-143">DateTime the object was last modified.</span></span> <span data-ttu-id="fa2b4-144">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="fa2b4-144">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="fa2b4-145">displayName</span><span class="sxs-lookup"><span data-stu-id="fa2b4-145">displayName</span></span>|<span data-ttu-id="fa2b4-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="fa2b4-146">String</span></span>|<span data-ttu-id="fa2b4-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="fa2b4-148">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="fa2b4-148">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="fa2b4-149">version</span><span class="sxs-lookup"><span data-stu-id="fa2b4-149">version</span></span>|<span data-ttu-id="fa2b4-150">Int32</span><span class="sxs-lookup"><span data-stu-id="fa2b4-150">Int32</span></span>|<span data-ttu-id="fa2b4-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-151">Version of the device configuration.</span></span> <span data-ttu-id="fa2b4-152">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="fa2b4-152">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="fa2b4-153">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="fa2b4-153">passwordRequired</span></span>|<span data-ttu-id="fa2b4-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="fa2b4-154">Boolean</span></span>|<span data-ttu-id="fa2b4-155">Exige una contraseña para desbloquear el dispositivo Windows.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-155">Require a password to unlock Windows device.</span></span>|
|<span data-ttu-id="fa2b4-156">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="fa2b4-156">passwordBlockSimple</span></span>|<span data-ttu-id="fa2b4-157">Booleano</span><span class="sxs-lookup"><span data-stu-id="fa2b4-157">Boolean</span></span>|<span data-ttu-id="fa2b4-158">Indica si quiere bloquear o no la contraseña simple.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-158">Indicates whether or not to block simple password.</span></span>|
|<span data-ttu-id="fa2b4-159">passwordRequiredToUnlockFromIdle</span><span class="sxs-lookup"><span data-stu-id="fa2b4-159">passwordRequiredToUnlockFromIdle</span></span>|<span data-ttu-id="fa2b4-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="fa2b4-160">Boolean</span></span>|<span data-ttu-id="fa2b4-161">Exige una contraseña para desbloquear el dispositivo inactivo.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-161">Require a password to unlock an idle device.</span></span>|
|<span data-ttu-id="fa2b4-162">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="fa2b4-162">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="fa2b4-163">Int32</span><span class="sxs-lookup"><span data-stu-id="fa2b4-163">Int32</span></span>|<span data-ttu-id="fa2b4-164">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-164">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="fa2b4-165">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="fa2b4-165">passwordExpirationDays</span></span>|<span data-ttu-id="fa2b4-166">Int32</span><span class="sxs-lookup"><span data-stu-id="fa2b4-166">Int32</span></span>|<span data-ttu-id="fa2b4-167">La expiración de la contraseña en días.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-167">The password expiration in days.</span></span>|
|<span data-ttu-id="fa2b4-168">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="fa2b4-168">passwordMinimumLength</span></span>|<span data-ttu-id="fa2b4-169">Int32</span><span class="sxs-lookup"><span data-stu-id="fa2b4-169">Int32</span></span>|<span data-ttu-id="fa2b4-170">La longitud mínima de contraseña.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-170">The minimum password length.</span></span>|
|<span data-ttu-id="fa2b4-171">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="fa2b4-171">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="fa2b4-172">Int32</span><span class="sxs-lookup"><span data-stu-id="fa2b4-172">Int32</span></span>|<span data-ttu-id="fa2b4-173">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-173">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="fa2b4-174">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="fa2b4-174">passwordRequiredType</span></span>|[<span data-ttu-id="fa2b4-175">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="fa2b4-175">requiredPasswordType</span></span>](../resources/intune_deviceconfig_requiredpasswordtype.md)|<span data-ttu-id="fa2b4-p108">El tipo de contraseña requerida. Los valores posibles son: `deviceDefault`, `alphanumeric`, `numeric`.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-p108">The required password type. The possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="fa2b4-178">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="fa2b4-178">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="fa2b4-179">Int32</span><span class="sxs-lookup"><span data-stu-id="fa2b4-179">Int32</span></span>|<span data-ttu-id="fa2b4-180">Número de contraseñas anteriores que impide su reutilización.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-180">The number of previous passwords to prevent re-use of.</span></span>|
|<span data-ttu-id="fa2b4-181">requireHealthyDeviceReport</span><span class="sxs-lookup"><span data-stu-id="fa2b4-181">requireHealthyDeviceReport</span></span>|<span data-ttu-id="fa2b4-182">Booleano</span><span class="sxs-lookup"><span data-stu-id="fa2b4-182">Boolean</span></span>|<span data-ttu-id="fa2b4-183">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-183">Require devices to be reported as healthy by Windows Device Health Attestation.</span></span>|
|<span data-ttu-id="fa2b4-184">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="fa2b4-184">osMinimumVersion</span></span>|<span data-ttu-id="fa2b4-185">Cadena</span><span class="sxs-lookup"><span data-stu-id="fa2b4-185">String</span></span>|<span data-ttu-id="fa2b4-186">Versión mínima de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-186">Minimum Windows 10 version.</span></span>|
|<span data-ttu-id="fa2b4-187">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="fa2b4-187">osMaximumVersion</span></span>|<span data-ttu-id="fa2b4-188">Cadena</span><span class="sxs-lookup"><span data-stu-id="fa2b4-188">String</span></span>|<span data-ttu-id="fa2b4-189">Versión máxima de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-189">Maximum Windows 10 version.</span></span>|
|<span data-ttu-id="fa2b4-190">mobileOsMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="fa2b4-190">mobileOsMinimumVersion</span></span>|<span data-ttu-id="fa2b4-191">Cadena</span><span class="sxs-lookup"><span data-stu-id="fa2b4-191">String</span></span>|<span data-ttu-id="fa2b4-192">Versión mínima de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-192">Minimum Windows Phone version.</span></span>|
|<span data-ttu-id="fa2b4-193">mobileOsMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="fa2b4-193">mobileOsMaximumVersion</span></span>|<span data-ttu-id="fa2b4-194">Cadena</span><span class="sxs-lookup"><span data-stu-id="fa2b4-194">String</span></span>|<span data-ttu-id="fa2b4-195">Versión máxima de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-195">Maximum Windows Phone version.</span></span>|
|<span data-ttu-id="fa2b4-196">earlyLaunchAntiMalwareDriverEnabled</span><span class="sxs-lookup"><span data-stu-id="fa2b4-196">earlyLaunchAntiMalwareDriverEnabled</span></span>|<span data-ttu-id="fa2b4-197">Booleano</span><span class="sxs-lookup"><span data-stu-id="fa2b4-197">Boolean</span></span>|<span data-ttu-id="fa2b4-198">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; el controlador antimalware de inicio temprano está habilitado.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-198">Require devices to be reported as healthy by Windows Device Health Attestation - early launch antimalware driver is enabled.</span></span>|
|<span data-ttu-id="fa2b4-199">bitLockerEnabled</span><span class="sxs-lookup"><span data-stu-id="fa2b4-199">bitLockerEnabled</span></span>|<span data-ttu-id="fa2b4-200">Booleano</span><span class="sxs-lookup"><span data-stu-id="fa2b4-200">Boolean</span></span>|<span data-ttu-id="fa2b4-201">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; BitLocker está habilitado.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-201">Require devices to be reported healthy by Windows Device Health Attestation - bit locker is enabled</span></span>|
|<span data-ttu-id="fa2b4-202">secureBootEnabled</span><span class="sxs-lookup"><span data-stu-id="fa2b4-202">secureBootEnabled</span></span>|<span data-ttu-id="fa2b4-203">Booleano</span><span class="sxs-lookup"><span data-stu-id="fa2b4-203">Boolean</span></span>|<span data-ttu-id="fa2b4-204">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; el arranque seguro está habilitado.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-204">Require devices to be reported as healthy by Windows Device Health Attestation - secure boot is enabled.</span></span>|
|<span data-ttu-id="fa2b4-205">codeIntegrityEnabled</span><span class="sxs-lookup"><span data-stu-id="fa2b4-205">codeIntegrityEnabled</span></span>|<span data-ttu-id="fa2b4-206">Booleano</span><span class="sxs-lookup"><span data-stu-id="fa2b4-206">Boolean</span></span>|<span data-ttu-id="fa2b4-207">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-207">Require devices to be reported as healthy by Windows Device Health Attestation.</span></span>|
|<span data-ttu-id="fa2b4-208">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="fa2b4-208">storageRequireEncryption</span></span>|<span data-ttu-id="fa2b4-209">Booleano</span><span class="sxs-lookup"><span data-stu-id="fa2b4-209">Boolean</span></span>|<span data-ttu-id="fa2b4-210">Exige el cifrado en dispositivos Windows.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-210">Require encryption on windows devices.</span></span>|



## <a name="response"></a><span data-ttu-id="fa2b4-211">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fa2b4-211">Response</span></span>
<span data-ttu-id="fa2b4-212">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windows10CompliancePolicy](../resources/intune_deviceconfig_windows10compliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-212">If successful, this method returns a `201 Created` response code and a [windows10CompliancePolicy](../resources/intune_deviceconfig_windows10compliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fa2b4-213">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fa2b4-213">Example</span></span>
### <a name="request"></a><span data-ttu-id="fa2b4-214">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fa2b4-214">Request</span></span>
<span data-ttu-id="fa2b4-215">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-215">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies
Content-type: application/json
Content-length: 1018

{
  "@odata.type": "#microsoft.graph.windows10CompliancePolicy",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "passwordRequired": true,
  "passwordBlockSimple": true,
  "passwordRequiredToUnlockFromIdle": true,
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinimumCharacterSetCount": 0,
  "passwordRequiredType": "alphanumeric",
  "passwordPreviousPasswordBlockCount": 2,
  "requireHealthyDeviceReport": true,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "mobileOsMinimumVersion": "Mobile Os Minimum Version value",
  "mobileOsMaximumVersion": "Mobile Os Maximum Version value",
  "earlyLaunchAntiMalwareDriverEnabled": true,
  "bitLockerEnabled": true,
  "secureBootEnabled": true,
  "codeIntegrityEnabled": true,
  "storageRequireEncryption": true
}
```

### <a name="response"></a><span data-ttu-id="fa2b4-216">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fa2b4-216">Response</span></span>
<span data-ttu-id="fa2b4-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fa2b4-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1126

{
  "@odata.type": "#microsoft.graph.windows10CompliancePolicy",
  "id": "2919ae62-ae62-2919-62ae-192962ae1929",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "passwordRequired": true,
  "passwordBlockSimple": true,
  "passwordRequiredToUnlockFromIdle": true,
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinimumCharacterSetCount": 0,
  "passwordRequiredType": "alphanumeric",
  "passwordPreviousPasswordBlockCount": 2,
  "requireHealthyDeviceReport": true,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "mobileOsMinimumVersion": "Mobile Os Minimum Version value",
  "mobileOsMaximumVersion": "Mobile Os Maximum Version value",
  "earlyLaunchAntiMalwareDriverEnabled": true,
  "bitLockerEnabled": true,
  "secureBootEnabled": true,
  "codeIntegrityEnabled": true,
  "storageRequireEncryption": true
}
```








