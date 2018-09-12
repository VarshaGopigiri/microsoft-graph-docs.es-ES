# <a name="update-windows10compliancepolicy"></a><span data-ttu-id="391ab-101">Actualizar windows10CompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="391ab-101">Update windows10CompliancePolicy</span></span>

> <span data-ttu-id="391ab-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="391ab-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="391ab-103">Actualice las propiedades de un objeto [windows10CompliancePolicy](../resources/intune_deviceconfig_windows10compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="391ab-103">Update the properties of a [windows10CompliancePolicy](../resources/intune_deviceconfig_windows10compliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="391ab-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="391ab-104">Prerequisites</span></span>
<span data-ttu-id="391ab-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="391ab-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="391ab-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="391ab-107">Permission type</span></span>|<span data-ttu-id="391ab-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="391ab-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="391ab-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="391ab-109">Delegated (work or school account)</span></span>|<span data-ttu-id="391ab-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="391ab-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="391ab-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="391ab-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="391ab-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="391ab-112">Not supported.</span></span>|
|<span data-ttu-id="391ab-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="391ab-113">Application</span></span>|<span data-ttu-id="391ab-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="391ab-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="391ab-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="391ab-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="request-headers"></a><span data-ttu-id="391ab-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="391ab-116">Request headers</span></span>
|<span data-ttu-id="391ab-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="391ab-117">Header</span></span>|<span data-ttu-id="391ab-118">Valor</span><span class="sxs-lookup"><span data-stu-id="391ab-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="391ab-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="391ab-119">Authorization</span></span>|<span data-ttu-id="391ab-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="391ab-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="391ab-121">Accept</span><span class="sxs-lookup"><span data-stu-id="391ab-121">Accept</span></span>|<span data-ttu-id="391ab-122">application/json</span><span class="sxs-lookup"><span data-stu-id="391ab-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="391ab-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="391ab-123">Request body</span></span>
<span data-ttu-id="391ab-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windows10CompliancePolicy](../resources/intune_deviceconfig_windows10compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="391ab-124">In the request body, supply a JSON representation for the [windows10CompliancePolicy](../resources/intune_deviceconfig_windows10compliancepolicy.md) object.</span></span>

<span data-ttu-id="391ab-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windows10CompliancePolicy](../resources/intune_deviceconfig_windows10compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="391ab-125">The following table shows the properties that are required when you create the [windows10CompliancePolicy](../resources/intune_deviceconfig_windows10compliancepolicy.md).</span></span>

|<span data-ttu-id="391ab-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="391ab-126">Property</span></span>|<span data-ttu-id="391ab-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="391ab-127">Type</span></span>|<span data-ttu-id="391ab-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="391ab-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="391ab-129">id</span><span class="sxs-lookup"><span data-stu-id="391ab-129">id</span></span>|<span data-ttu-id="391ab-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="391ab-130">String</span></span>|<span data-ttu-id="391ab-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="391ab-131">Key of the entity.</span></span> <span data-ttu-id="391ab-132">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="391ab-132">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="391ab-133">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="391ab-133">createdDateTime</span></span>|<span data-ttu-id="391ab-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="391ab-134">DateTimeOffset</span></span>|<span data-ttu-id="391ab-135">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="391ab-135">DateTime the object was created.</span></span> <span data-ttu-id="391ab-136">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="391ab-136">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="391ab-137">description</span><span class="sxs-lookup"><span data-stu-id="391ab-137">description</span></span>|<span data-ttu-id="391ab-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="391ab-138">String</span></span>|<span data-ttu-id="391ab-139">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="391ab-139">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="391ab-140">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="391ab-140">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="391ab-141">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="391ab-141">lastModifiedDateTime</span></span>|<span data-ttu-id="391ab-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="391ab-142">DateTimeOffset</span></span>|<span data-ttu-id="391ab-143">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="391ab-143">DateTime the object was last modified.</span></span> <span data-ttu-id="391ab-144">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="391ab-144">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="391ab-145">displayName</span><span class="sxs-lookup"><span data-stu-id="391ab-145">displayName</span></span>|<span data-ttu-id="391ab-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="391ab-146">String</span></span>|<span data-ttu-id="391ab-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="391ab-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="391ab-148">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="391ab-148">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="391ab-149">version</span><span class="sxs-lookup"><span data-stu-id="391ab-149">version</span></span>|<span data-ttu-id="391ab-150">Int32</span><span class="sxs-lookup"><span data-stu-id="391ab-150">Int32</span></span>|<span data-ttu-id="391ab-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="391ab-151">Version of the device configuration.</span></span> <span data-ttu-id="391ab-152">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="391ab-152">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="391ab-153">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="391ab-153">passwordRequired</span></span>|<span data-ttu-id="391ab-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="391ab-154">Boolean</span></span>|<span data-ttu-id="391ab-155">Exige una contraseña para desbloquear el dispositivo Windows.</span><span class="sxs-lookup"><span data-stu-id="391ab-155">Require a password to unlock Windows device.</span></span>|
|<span data-ttu-id="391ab-156">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="391ab-156">passwordBlockSimple</span></span>|<span data-ttu-id="391ab-157">Booleano</span><span class="sxs-lookup"><span data-stu-id="391ab-157">Boolean</span></span>|<span data-ttu-id="391ab-158">Indica si quiere bloquear o no la contraseña simple.</span><span class="sxs-lookup"><span data-stu-id="391ab-158">Indicates whether or not to block simple password.</span></span>|
|<span data-ttu-id="391ab-159">passwordRequiredToUnlockFromIdle</span><span class="sxs-lookup"><span data-stu-id="391ab-159">passwordRequiredToUnlockFromIdle</span></span>|<span data-ttu-id="391ab-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="391ab-160">Boolean</span></span>|<span data-ttu-id="391ab-161">Exige una contraseña para desbloquear el dispositivo inactivo.</span><span class="sxs-lookup"><span data-stu-id="391ab-161">Require a password to unlock an idle device.</span></span>|
|<span data-ttu-id="391ab-162">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="391ab-162">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="391ab-163">Int32</span><span class="sxs-lookup"><span data-stu-id="391ab-163">Int32</span></span>|<span data-ttu-id="391ab-164">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="391ab-164">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="391ab-165">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="391ab-165">passwordExpirationDays</span></span>|<span data-ttu-id="391ab-166">Int32</span><span class="sxs-lookup"><span data-stu-id="391ab-166">Int32</span></span>|<span data-ttu-id="391ab-167">La expiración de la contraseña en días.</span><span class="sxs-lookup"><span data-stu-id="391ab-167">The password expiration in days.</span></span>|
|<span data-ttu-id="391ab-168">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="391ab-168">passwordMinimumLength</span></span>|<span data-ttu-id="391ab-169">Int32</span><span class="sxs-lookup"><span data-stu-id="391ab-169">Int32</span></span>|<span data-ttu-id="391ab-170">La longitud mínima de contraseña.</span><span class="sxs-lookup"><span data-stu-id="391ab-170">The minimum password length.</span></span>|
|<span data-ttu-id="391ab-171">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="391ab-171">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="391ab-172">Int32</span><span class="sxs-lookup"><span data-stu-id="391ab-172">Int32</span></span>|<span data-ttu-id="391ab-173">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="391ab-173">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="391ab-174">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="391ab-174">passwordRequiredType</span></span>|[<span data-ttu-id="391ab-175">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="391ab-175">requiredPasswordType</span></span>](../resources/intune_deviceconfig_requiredpasswordtype.md)|<span data-ttu-id="391ab-p108">El tipo de contraseña requerida. Los valores posibles son: `deviceDefault`, `alphanumeric`, `numeric`.</span><span class="sxs-lookup"><span data-stu-id="391ab-p108">The required password type. The possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="391ab-178">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="391ab-178">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="391ab-179">Int32</span><span class="sxs-lookup"><span data-stu-id="391ab-179">Int32</span></span>|<span data-ttu-id="391ab-180">Número de contraseñas anteriores que impide su reutilización.</span><span class="sxs-lookup"><span data-stu-id="391ab-180">The number of previous passwords to prevent re-use of.</span></span>|
|<span data-ttu-id="391ab-181">requireHealthyDeviceReport</span><span class="sxs-lookup"><span data-stu-id="391ab-181">requireHealthyDeviceReport</span></span>|<span data-ttu-id="391ab-182">Booleano</span><span class="sxs-lookup"><span data-stu-id="391ab-182">Boolean</span></span>|<span data-ttu-id="391ab-183">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos.</span><span class="sxs-lookup"><span data-stu-id="391ab-183">Require devices to be reported as healthy by Windows Device Health Attestation.</span></span>|
|<span data-ttu-id="391ab-184">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="391ab-184">osMinimumVersion</span></span>|<span data-ttu-id="391ab-185">Cadena</span><span class="sxs-lookup"><span data-stu-id="391ab-185">String</span></span>|<span data-ttu-id="391ab-186">Versión mínima de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="391ab-186">Minimum Windows 10 version.</span></span>|
|<span data-ttu-id="391ab-187">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="391ab-187">osMaximumVersion</span></span>|<span data-ttu-id="391ab-188">Cadena</span><span class="sxs-lookup"><span data-stu-id="391ab-188">String</span></span>|<span data-ttu-id="391ab-189">Versión máxima de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="391ab-189">Maximum Windows 10 version.</span></span>|
|<span data-ttu-id="391ab-190">mobileOsMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="391ab-190">mobileOsMinimumVersion</span></span>|<span data-ttu-id="391ab-191">Cadena</span><span class="sxs-lookup"><span data-stu-id="391ab-191">String</span></span>|<span data-ttu-id="391ab-192">Versión mínima de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="391ab-192">Minimum Windows Phone version.</span></span>|
|<span data-ttu-id="391ab-193">mobileOsMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="391ab-193">mobileOsMaximumVersion</span></span>|<span data-ttu-id="391ab-194">Cadena</span><span class="sxs-lookup"><span data-stu-id="391ab-194">String</span></span>|<span data-ttu-id="391ab-195">Versión máxima de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="391ab-195">Maximum Windows Phone version.</span></span>|
|<span data-ttu-id="391ab-196">earlyLaunchAntiMalwareDriverEnabled</span><span class="sxs-lookup"><span data-stu-id="391ab-196">earlyLaunchAntiMalwareDriverEnabled</span></span>|<span data-ttu-id="391ab-197">Booleano</span><span class="sxs-lookup"><span data-stu-id="391ab-197">Boolean</span></span>|<span data-ttu-id="391ab-198">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; el controlador antimalware de inicio temprano está habilitado.</span><span class="sxs-lookup"><span data-stu-id="391ab-198">Require devices to be reported as healthy by Windows Device Health Attestation - early launch antimalware driver is enabled.</span></span>|
|<span data-ttu-id="391ab-199">bitLockerEnabled</span><span class="sxs-lookup"><span data-stu-id="391ab-199">bitLockerEnabled</span></span>|<span data-ttu-id="391ab-200">Booleano</span><span class="sxs-lookup"><span data-stu-id="391ab-200">Boolean</span></span>|<span data-ttu-id="391ab-201">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; BitLocker está habilitado.</span><span class="sxs-lookup"><span data-stu-id="391ab-201">Require devices to be reported healthy by Windows Device Health Attestation - bit locker is enabled</span></span>|
|<span data-ttu-id="391ab-202">secureBootEnabled</span><span class="sxs-lookup"><span data-stu-id="391ab-202">secureBootEnabled</span></span>|<span data-ttu-id="391ab-203">Booleano</span><span class="sxs-lookup"><span data-stu-id="391ab-203">Boolean</span></span>|<span data-ttu-id="391ab-204">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; el arranque seguro está habilitado.</span><span class="sxs-lookup"><span data-stu-id="391ab-204">Require devices to be reported as healthy by Windows Device Health Attestation - secure boot is enabled.</span></span>|
|<span data-ttu-id="391ab-205">codeIntegrityEnabled</span><span class="sxs-lookup"><span data-stu-id="391ab-205">codeIntegrityEnabled</span></span>|<span data-ttu-id="391ab-206">Booleano</span><span class="sxs-lookup"><span data-stu-id="391ab-206">Boolean</span></span>|<span data-ttu-id="391ab-207">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos.</span><span class="sxs-lookup"><span data-stu-id="391ab-207">Require devices to be reported as healthy by Windows Device Health Attestation.</span></span>|
|<span data-ttu-id="391ab-208">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="391ab-208">storageRequireEncryption</span></span>|<span data-ttu-id="391ab-209">Booleano</span><span class="sxs-lookup"><span data-stu-id="391ab-209">Boolean</span></span>|<span data-ttu-id="391ab-210">Exige el cifrado en dispositivos Windows.</span><span class="sxs-lookup"><span data-stu-id="391ab-210">Require encryption on windows devices.</span></span>|



## <a name="response"></a><span data-ttu-id="391ab-211">Respuesta</span><span class="sxs-lookup"><span data-stu-id="391ab-211">Response</span></span>
<span data-ttu-id="391ab-212">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows10CompliancePolicy](../resources/intune_deviceconfig_windows10compliancepolicy.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="391ab-212">If successful, this method returns a `200 OK` response code and an updated [windows10CompliancePolicy](../resources/intune_deviceconfig_windows10compliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="391ab-213">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="391ab-213">Example</span></span>
### <a name="request"></a><span data-ttu-id="391ab-214">Solicitud</span><span class="sxs-lookup"><span data-stu-id="391ab-214">Request</span></span>
<span data-ttu-id="391ab-215">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="391ab-215">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
Content-type: application/json
Content-length: 954

{
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

### <a name="response"></a><span data-ttu-id="391ab-216">Respuesta</span><span class="sxs-lookup"><span data-stu-id="391ab-216">Response</span></span>
<span data-ttu-id="391ab-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="391ab-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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








