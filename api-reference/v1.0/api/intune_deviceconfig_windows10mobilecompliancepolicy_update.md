# <a name="update-windows10mobilecompliancepolicy"></a><span data-ttu-id="66ba1-101">Actualizar windows10MobileCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="66ba1-101">Update windows10MobileCompliancePolicy</span></span>

> <span data-ttu-id="66ba1-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="66ba1-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="66ba1-103">Actualice las propiedades de un objeto [windows10MobileCompliancePolicy](../resources/intune_deviceconfig_windows10mobilecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="66ba1-103">Update the properties of a [calendar](../resources/intune_deviceconfig_windows10mobilecompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="66ba1-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="66ba1-104">Prerequisites</span></span>
<span data-ttu-id="66ba1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="66ba1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="66ba1-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="66ba1-107">Permission type</span></span>|<span data-ttu-id="66ba1-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="66ba1-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="66ba1-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="66ba1-109">Delegated (work or school account)</span></span>|<span data-ttu-id="66ba1-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="66ba1-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="66ba1-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="66ba1-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="66ba1-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="66ba1-112">Not supported.</span></span>|
|<span data-ttu-id="66ba1-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="66ba1-113">Application</span></span>|<span data-ttu-id="66ba1-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="66ba1-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="66ba1-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="66ba1-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="request-headers"></a><span data-ttu-id="66ba1-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="66ba1-116">Request headers</span></span>
|<span data-ttu-id="66ba1-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66ba1-117">Header</span></span>|<span data-ttu-id="66ba1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="66ba1-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="66ba1-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="66ba1-119">Authorization</span></span>|<span data-ttu-id="66ba1-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="66ba1-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="66ba1-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="66ba1-121">Accept</span></span>|<span data-ttu-id="66ba1-122">application/json</span><span class="sxs-lookup"><span data-stu-id="66ba1-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="66ba1-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="66ba1-123">Request body</span></span>
<span data-ttu-id="66ba1-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windows10MobileCompliancePolicy](../resources/intune_deviceconfig_windows10mobilecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="66ba1-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_deviceconfig_windows10mobilecompliancepolicy.md) object.</span></span>

<span data-ttu-id="66ba1-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windows10MobileCompliancePolicy](../resources/intune_deviceconfig_windows10mobilecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="66ba1-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="66ba1-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="66ba1-126">Property</span></span>|<span data-ttu-id="66ba1-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="66ba1-127">Type</span></span>|<span data-ttu-id="66ba1-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="66ba1-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="66ba1-129">id</span><span class="sxs-lookup"><span data-stu-id="66ba1-129">id</span></span>|<span data-ttu-id="66ba1-130">String</span><span class="sxs-lookup"><span data-stu-id="66ba1-130">String</span></span>|<span data-ttu-id="66ba1-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="66ba1-131">Key of the setting.</span></span> <span data-ttu-id="66ba1-132">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="66ba1-132">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="66ba1-133">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="66ba1-133">createdDateTime</span></span>|<span data-ttu-id="66ba1-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="66ba1-134">DateTimeOffset</span></span>|<span data-ttu-id="66ba1-135">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="66ba1-135">DateTime the object was created.</span></span> <span data-ttu-id="66ba1-136">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="66ba1-136">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="66ba1-137">description</span><span class="sxs-lookup"><span data-stu-id="66ba1-137">description</span></span>|<span data-ttu-id="66ba1-138">String</span><span class="sxs-lookup"><span data-stu-id="66ba1-138">String</span></span>|<span data-ttu-id="66ba1-139">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66ba1-139">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="66ba1-140">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="66ba1-140">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="66ba1-141">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="66ba1-141">lastModifiedDateTime</span></span>|<span data-ttu-id="66ba1-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="66ba1-142">DateTimeOffset</span></span>|<span data-ttu-id="66ba1-143">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="66ba1-143">Indicates the date the object was last modified.</span></span> <span data-ttu-id="66ba1-144">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="66ba1-144">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="66ba1-145">displayName</span><span class="sxs-lookup"><span data-stu-id="66ba1-145">displayName</span></span>|<span data-ttu-id="66ba1-146">String</span><span class="sxs-lookup"><span data-stu-id="66ba1-146">String</span></span>|<span data-ttu-id="66ba1-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66ba1-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="66ba1-148">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="66ba1-148">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="66ba1-149">version</span><span class="sxs-lookup"><span data-stu-id="66ba1-149">version</span></span>|<span data-ttu-id="66ba1-150">Int32</span><span class="sxs-lookup"><span data-stu-id="66ba1-150">Int32</span></span>|<span data-ttu-id="66ba1-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66ba1-151">Version of the device configuration.</span></span> <span data-ttu-id="66ba1-152">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="66ba1-152">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="66ba1-153">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="66ba1-153">passwordRequired</span></span>|<span data-ttu-id="66ba1-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="66ba1-154">Boolean</span></span>|<span data-ttu-id="66ba1-155">Exigir una contraseña para desbloquear el dispositivo de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="66ba1-155">Require a password to unlock Windows Phone device.</span></span>|
|<span data-ttu-id="66ba1-156">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="66ba1-156">passwordBlockSimple</span></span>|<span data-ttu-id="66ba1-157">Booleano</span><span class="sxs-lookup"><span data-stu-id="66ba1-157">Boolean</span></span>|<span data-ttu-id="66ba1-158">Si quiere bloquear o no la sincronización del calendario.</span><span class="sxs-lookup"><span data-stu-id="66ba1-158">Whether or not to block syncing the calendar.</span></span>|
|<span data-ttu-id="66ba1-159">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="66ba1-159">passwordMinimumLength</span></span>|<span data-ttu-id="66ba1-160">Int32</span><span class="sxs-lookup"><span data-stu-id="66ba1-160">Int32</span></span>|<span data-ttu-id="66ba1-161">Longitud mínima de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="66ba1-161">Minimum password length.</span></span> <span data-ttu-id="66ba1-162">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="66ba1-162">Valid values 4 to 16</span></span>|
|<span data-ttu-id="66ba1-163">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="66ba1-163">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="66ba1-164">Int32</span><span class="sxs-lookup"><span data-stu-id="66ba1-164">Int32</span></span>|<span data-ttu-id="66ba1-165">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="66ba1-165">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="66ba1-166">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="66ba1-166">passwordRequiredType</span></span>|<span data-ttu-id="66ba1-167">String</span><span class="sxs-lookup"><span data-stu-id="66ba1-167">String</span></span>|<span data-ttu-id="66ba1-168">Tipo de contraseña necesaria.</span><span class="sxs-lookup"><span data-stu-id="66ba1-168">The required password type.</span></span> <span data-ttu-id="66ba1-169">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="66ba1-169">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="66ba1-170">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="66ba1-170">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="66ba1-171">Int32</span><span class="sxs-lookup"><span data-stu-id="66ba1-171">Int32</span></span>|<span data-ttu-id="66ba1-172">Número de contraseñas anteriores que impide su reutilización.</span><span class="sxs-lookup"><span data-stu-id="66ba1-172">The number of previous passwords to prevent re-use of.</span></span>|
|<span data-ttu-id="66ba1-173">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="66ba1-173">passwordExpirationDays</span></span>|<span data-ttu-id="66ba1-174">Int32</span><span class="sxs-lookup"><span data-stu-id="66ba1-174">Int32</span></span>|<span data-ttu-id="66ba1-175">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="66ba1-175">Number of days before password expiration.</span></span> <span data-ttu-id="66ba1-176">Valores válidos de 1 a 255</span><span class="sxs-lookup"><span data-stu-id="66ba1-176">Valid values 1 to 255</span></span>|
|<span data-ttu-id="66ba1-177">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="66ba1-177">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="66ba1-178">Int32</span><span class="sxs-lookup"><span data-stu-id="66ba1-178">Int32</span></span>|<span data-ttu-id="66ba1-179">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="66ba1-179">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="66ba1-180">passwordRequireToUnlockFromIdle</span><span class="sxs-lookup"><span data-stu-id="66ba1-180">passwordRequireToUnlockFromIdle</span></span>|<span data-ttu-id="66ba1-181">Booleano</span><span class="sxs-lookup"><span data-stu-id="66ba1-181">Boolean</span></span>|<span data-ttu-id="66ba1-182">Exige una contraseña para desbloquear el dispositivo inactivo.</span><span class="sxs-lookup"><span data-stu-id="66ba1-182">Require a password to unlock an idle device.</span></span>|
|<span data-ttu-id="66ba1-183">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="66ba1-183">osMinimumVersion</span></span>|<span data-ttu-id="66ba1-184">String</span><span class="sxs-lookup"><span data-stu-id="66ba1-184">String</span></span>|<span data-ttu-id="66ba1-185">Versión mínima de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="66ba1-185">Minimum Windows Phone version.</span></span>|
|<span data-ttu-id="66ba1-186">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="66ba1-186">osMaximumVersion</span></span>|<span data-ttu-id="66ba1-187">String</span><span class="sxs-lookup"><span data-stu-id="66ba1-187">String</span></span>|<span data-ttu-id="66ba1-188">Versión máxima de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="66ba1-188">Maximum Windows Phone version.</span></span>|
|<span data-ttu-id="66ba1-189">earlyLaunchAntiMalwareDriverEnabled</span><span class="sxs-lookup"><span data-stu-id="66ba1-189">earlyLaunchAntiMalwareDriverEnabled</span></span>|<span data-ttu-id="66ba1-190">Booleano</span><span class="sxs-lookup"><span data-stu-id="66ba1-190">Boolean</span></span>|<span data-ttu-id="66ba1-191">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; el controlador antimalware de inicio temprano está habilitado.</span><span class="sxs-lookup"><span data-stu-id="66ba1-191">Require devices to be reported as healthy by Windows Device Health Attestation - early launch antimalware driver is enabled.</span></span>|
|<span data-ttu-id="66ba1-192">bitLockerEnabled</span><span class="sxs-lookup"><span data-stu-id="66ba1-192">bitLockerEnabled</span></span>|<span data-ttu-id="66ba1-193">Booleano</span><span class="sxs-lookup"><span data-stu-id="66ba1-193">Boolean</span></span>|<span data-ttu-id="66ba1-194">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; BitLocker está habilitado.</span><span class="sxs-lookup"><span data-stu-id="66ba1-194">Require devices to be reported healthy by Windows Device Health Attestation - bit locker is enabled</span></span>|
|<span data-ttu-id="66ba1-195">secureBootEnabled</span><span class="sxs-lookup"><span data-stu-id="66ba1-195">secureBootEnabled</span></span>|<span data-ttu-id="66ba1-196">Booleano</span><span class="sxs-lookup"><span data-stu-id="66ba1-196">Boolean</span></span>|<span data-ttu-id="66ba1-197">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; el arranque seguro está habilitado.</span><span class="sxs-lookup"><span data-stu-id="66ba1-197">Require devices to be reported as healthy by Windows Device Health Attestation - secure boot is enabled.</span></span>|
|<span data-ttu-id="66ba1-198">codeIntegrityEnabled</span><span class="sxs-lookup"><span data-stu-id="66ba1-198">codeIntegrityEnabled</span></span>|<span data-ttu-id="66ba1-199">Booleano</span><span class="sxs-lookup"><span data-stu-id="66ba1-199">Boolean</span></span>|<span data-ttu-id="66ba1-200">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos.</span><span class="sxs-lookup"><span data-stu-id="66ba1-200">Require devices to be reported as healthy by Windows Device Health Attestation.</span></span>|
|<span data-ttu-id="66ba1-201">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="66ba1-201">storageRequireEncryption</span></span>|<span data-ttu-id="66ba1-202">Booleano</span><span class="sxs-lookup"><span data-stu-id="66ba1-202">Boolean</span></span>|<span data-ttu-id="66ba1-203">Exige el cifrado en dispositivos Windows.</span><span class="sxs-lookup"><span data-stu-id="66ba1-203">Require encryption on windows devices.</span></span>|



## <a name="response"></a><span data-ttu-id="66ba1-204">Respuesta</span><span class="sxs-lookup"><span data-stu-id="66ba1-204">Response</span></span>
<span data-ttu-id="66ba1-205">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows10MobileCompliancePolicy](../resources/intune_deviceconfig_windows10mobilecompliancepolicy.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="66ba1-205">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_deviceconfig_windows10mobilecompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="66ba1-206">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="66ba1-206">Example</span></span>
### <a name="request"></a><span data-ttu-id="66ba1-207">Solicitud</span><span class="sxs-lookup"><span data-stu-id="66ba1-207">Request</span></span>
<span data-ttu-id="66ba1-208">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="66ba1-208">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
Content-type: application/json
Content-length: 786

{
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "passwordRequired": true,
  "passwordBlockSimple": true,
  "passwordMinimumLength": 5,
  "passwordMinimumCharacterSetCount": 0,
  "passwordRequiredType": "alphanumeric",
  "passwordPreviousPasswordBlockCount": 2,
  "passwordExpirationDays": 6,
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordRequireToUnlockFromIdle": true,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "earlyLaunchAntiMalwareDriverEnabled": true,
  "bitLockerEnabled": true,
  "secureBootEnabled": true,
  "codeIntegrityEnabled": true,
  "storageRequireEncryption": true
}
```

### <a name="response"></a><span data-ttu-id="66ba1-209">Respuesta</span><span class="sxs-lookup"><span data-stu-id="66ba1-209">Response</span></span>
<span data-ttu-id="66ba1-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="66ba1-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 964

{
  "@odata.type": "#microsoft.graph.windows10MobileCompliancePolicy",
  "id": "3d4237b0-37b0-3d42-b037-423db037423d",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "passwordRequired": true,
  "passwordBlockSimple": true,
  "passwordMinimumLength": 5,
  "passwordMinimumCharacterSetCount": 0,
  "passwordRequiredType": "alphanumeric",
  "passwordPreviousPasswordBlockCount": 2,
  "passwordExpirationDays": 6,
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordRequireToUnlockFromIdle": true,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "earlyLaunchAntiMalwareDriverEnabled": true,
  "bitLockerEnabled": true,
  "secureBootEnabled": true,
  "codeIntegrityEnabled": true,
  "storageRequireEncryption": true
}
```



