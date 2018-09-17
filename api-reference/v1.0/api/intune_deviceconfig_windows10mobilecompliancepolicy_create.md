# <a name="create-windows10mobilecompliancepolicy"></a><span data-ttu-id="f1f0d-101">Crear windows10MobileCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="f1f0d-101">Create windows10MobileCompliancePolicy</span></span>

> <span data-ttu-id="f1f0d-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f1f0d-103">Crear un objeto [windows10MobileCompliancePolicy](../resources/intune_deviceconfig_windows10mobilecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f1f0d-103">Create a new [windows10MobileCompliancePolicy](../resources/intune_deviceconfig_windows10mobilecompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f1f0d-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f1f0d-104">Prerequisites</span></span>
<span data-ttu-id="f1f0d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f1f0d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f1f0d-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f1f0d-107">Permission type</span></span>|<span data-ttu-id="f1f0d-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f1f0d-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f1f0d-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f1f0d-109">Delegated (work or school account)</span></span>|<span data-ttu-id="f1f0d-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f1f0d-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="f1f0d-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f1f0d-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f1f0d-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-112">Not supported.</span></span>|
|<span data-ttu-id="f1f0d-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f1f0d-113">Application</span></span>|<span data-ttu-id="f1f0d-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f1f0d-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f1f0d-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="f1f0d-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f1f0d-116">Request headers</span></span>
|<span data-ttu-id="f1f0d-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1f0d-117">Header</span></span>|<span data-ttu-id="f1f0d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f1f0d-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f1f0d-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="f1f0d-119">Authorization</span></span>|<span data-ttu-id="f1f0d-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f1f0d-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f1f0d-121">Accept</span></span>|<span data-ttu-id="f1f0d-122">application/json</span><span class="sxs-lookup"><span data-stu-id="f1f0d-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f1f0d-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f1f0d-123">Request body</span></span>
<span data-ttu-id="f1f0d-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto windows10MobileCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-124">In the request body, supply a JSON representation for the windows10MobileCompliancePolicy object.</span></span>

<span data-ttu-id="f1f0d-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windows10MobileCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-125">The following table shows the properties that are required when you create the windows10MobileCompliancePolicy.</span></span>

|<span data-ttu-id="f1f0d-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f1f0d-126">Property</span></span>|<span data-ttu-id="f1f0d-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="f1f0d-127">Type</span></span>|<span data-ttu-id="f1f0d-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="f1f0d-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f1f0d-129">id.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-129">id</span></span>|<span data-ttu-id="f1f0d-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="f1f0d-130">String</span></span>|<span data-ttu-id="f1f0d-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-131">Key of the entity.</span></span> <span data-ttu-id="f1f0d-132">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f1f0d-132">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="f1f0d-133">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="f1f0d-133">createdDateTime</span></span>|<span data-ttu-id="f1f0d-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f1f0d-134">DateTimeOffset</span></span>|<span data-ttu-id="f1f0d-135">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-135">DateTime the object was created.</span></span> <span data-ttu-id="f1f0d-136">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f1f0d-136">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="f1f0d-137">descripción</span><span class="sxs-lookup"><span data-stu-id="f1f0d-137">description</span></span>|<span data-ttu-id="f1f0d-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="f1f0d-138">String</span></span>|<span data-ttu-id="f1f0d-139">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-139">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="f1f0d-140">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f1f0d-140">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="f1f0d-141">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="f1f0d-141">lastModifiedDateTime</span></span>|<span data-ttu-id="f1f0d-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f1f0d-142">DateTimeOffset</span></span>|<span data-ttu-id="f1f0d-143">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-143">DateTime the object was last modified.</span></span> <span data-ttu-id="f1f0d-144">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f1f0d-144">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="f1f0d-145">displayName</span><span class="sxs-lookup"><span data-stu-id="f1f0d-145">displayName</span></span>|<span data-ttu-id="f1f0d-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="f1f0d-146">String</span></span>|<span data-ttu-id="f1f0d-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="f1f0d-148">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f1f0d-148">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="f1f0d-149">versión</span><span class="sxs-lookup"><span data-stu-id="f1f0d-149">version</span></span>|<span data-ttu-id="f1f0d-150">Int32</span><span class="sxs-lookup"><span data-stu-id="f1f0d-150">Int32</span></span>|<span data-ttu-id="f1f0d-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-151">Version of the device configuration.</span></span> <span data-ttu-id="f1f0d-152">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f1f0d-152">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="f1f0d-153">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="f1f0d-153">passwordRequired</span></span>|<span data-ttu-id="f1f0d-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="f1f0d-154">Boolean</span></span>|<span data-ttu-id="f1f0d-155">Exigir una contraseña para desbloquear el dispositivo de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-155">Require a password to unlock Windows Phone device.</span></span>|
|<span data-ttu-id="f1f0d-156">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="f1f0d-156">passwordBlockSimple</span></span>|<span data-ttu-id="f1f0d-157">Booleano</span><span class="sxs-lookup"><span data-stu-id="f1f0d-157">Boolean</span></span>|<span data-ttu-id="f1f0d-158">Si quiere bloquear o no la sincronización del calendario.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-158">Whether or not to block syncing the calendar.</span></span>|
|<span data-ttu-id="f1f0d-159">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="f1f0d-159">passwordMinimumLength</span></span>|<span data-ttu-id="f1f0d-160">Int32</span><span class="sxs-lookup"><span data-stu-id="f1f0d-160">Int32</span></span>|<span data-ttu-id="f1f0d-161">Longitud mínima de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-161">Minimum password length.</span></span> <span data-ttu-id="f1f0d-162">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="f1f0d-162">Valid values 4 to 16</span></span>|
|<span data-ttu-id="f1f0d-163">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="f1f0d-163">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="f1f0d-164">Int32</span><span class="sxs-lookup"><span data-stu-id="f1f0d-164">Int32</span></span>|<span data-ttu-id="f1f0d-165">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-165">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="f1f0d-166">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="f1f0d-166">passwordRequiredType</span></span>|[<span data-ttu-id="f1f0d-167">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="f1f0d-167">requiredPasswordType</span></span>](../resources/intune_deviceconfig_requiredpasswordtype.md)|<span data-ttu-id="f1f0d-168">Tipo de contraseña necesaria.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-168">The required password type.</span></span> <span data-ttu-id="f1f0d-169">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-169">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="f1f0d-170">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="f1f0d-170">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="f1f0d-171">Int32</span><span class="sxs-lookup"><span data-stu-id="f1f0d-171">Int32</span></span>|<span data-ttu-id="f1f0d-172">Número de contraseñas anteriores que impide su reutilización.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-172">The number of previous passwords to prevent re-use of.</span></span>|
|<span data-ttu-id="f1f0d-173">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="f1f0d-173">passwordExpirationDays</span></span>|<span data-ttu-id="f1f0d-174">Int32</span><span class="sxs-lookup"><span data-stu-id="f1f0d-174">Int32</span></span>|<span data-ttu-id="f1f0d-175">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-175">Number of days before password expiration.</span></span> <span data-ttu-id="f1f0d-176">Valores válidos de 1 a 255</span><span class="sxs-lookup"><span data-stu-id="f1f0d-176">Valid values 1 to 255</span></span>|
|<span data-ttu-id="f1f0d-177">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="f1f0d-177">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="f1f0d-178">Int32</span><span class="sxs-lookup"><span data-stu-id="f1f0d-178">Int32</span></span>|<span data-ttu-id="f1f0d-179">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-179">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="f1f0d-180">passwordRequireToUnlockFromIdle</span><span class="sxs-lookup"><span data-stu-id="f1f0d-180">passwordRequireToUnlockFromIdle</span></span>|<span data-ttu-id="f1f0d-181">Booleano</span><span class="sxs-lookup"><span data-stu-id="f1f0d-181">Boolean</span></span>|<span data-ttu-id="f1f0d-182">Exige una contraseña para desbloquear el dispositivo inactivo.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-182">Require a password to unlock an idle device.</span></span>|
|<span data-ttu-id="f1f0d-183">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="f1f0d-183">osMinimumVersion</span></span>|<span data-ttu-id="f1f0d-184">Cadena</span><span class="sxs-lookup"><span data-stu-id="f1f0d-184">String</span></span>|<span data-ttu-id="f1f0d-185">Versión mínima de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-185">Minimum Windows Phone version.</span></span>|
|<span data-ttu-id="f1f0d-186">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="f1f0d-186">osMaximumVersion</span></span>|<span data-ttu-id="f1f0d-187">Cadena</span><span class="sxs-lookup"><span data-stu-id="f1f0d-187">String</span></span>|<span data-ttu-id="f1f0d-188">Versión máxima de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-188">Maximum Windows Phone version.</span></span>|
|<span data-ttu-id="f1f0d-189">earlyLaunchAntiMalwareDriverEnabled</span><span class="sxs-lookup"><span data-stu-id="f1f0d-189">earlyLaunchAntiMalwareDriverEnabled</span></span>|<span data-ttu-id="f1f0d-190">Booleano</span><span class="sxs-lookup"><span data-stu-id="f1f0d-190">Boolean</span></span>|<span data-ttu-id="f1f0d-191">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; el controlador antimalware de inicio temprano está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-191">Require devices to be reported as healthy by Windows Device Health Attestation - early launch antimalware driver is enabled.</span></span>|
|<span data-ttu-id="f1f0d-192">bitLockerEnabled</span><span class="sxs-lookup"><span data-stu-id="f1f0d-192">bitLockerEnabled</span></span>|<span data-ttu-id="f1f0d-193">Booleano</span><span class="sxs-lookup"><span data-stu-id="f1f0d-193">Boolean</span></span>|<span data-ttu-id="f1f0d-194">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; BitLocker está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-194">Require devices to be reported healthy by Windows Device Health Attestation - bit locker is enabled</span></span>|
|<span data-ttu-id="f1f0d-195">secureBootEnabled</span><span class="sxs-lookup"><span data-stu-id="f1f0d-195">secureBootEnabled</span></span>|<span data-ttu-id="f1f0d-196">Booleano</span><span class="sxs-lookup"><span data-stu-id="f1f0d-196">Boolean</span></span>|<span data-ttu-id="f1f0d-197">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; el arranque seguro está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-197">Require devices to be reported as healthy by Windows Device Health Attestation - secure boot is enabled.</span></span>|
|<span data-ttu-id="f1f0d-198">codeIntegrityEnabled</span><span class="sxs-lookup"><span data-stu-id="f1f0d-198">codeIntegrityEnabled</span></span>|<span data-ttu-id="f1f0d-199">Booleano</span><span class="sxs-lookup"><span data-stu-id="f1f0d-199">Boolean</span></span>|<span data-ttu-id="f1f0d-200">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-200">Require devices to be reported as healthy by Windows Device Health Attestation.</span></span>|
|<span data-ttu-id="f1f0d-201">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="f1f0d-201">storageRequireEncryption</span></span>|<span data-ttu-id="f1f0d-202">Booleano</span><span class="sxs-lookup"><span data-stu-id="f1f0d-202">Boolean</span></span>|<span data-ttu-id="f1f0d-203">Exige el cifrado en dispositivos Windows.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-203">Require encryption on windows devices.</span></span>|



## <a name="response"></a><span data-ttu-id="f1f0d-204">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f1f0d-204">Response</span></span>
<span data-ttu-id="f1f0d-205">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windows10MobileCompliancePolicy](../resources/intune_deviceconfig_windows10mobilecompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-205">If successful, this method returns a `201 Created` response code and a [windows10MobileCompliancePolicy](../resources/intune_deviceconfig_windows10mobilecompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f1f0d-206">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f1f0d-206">Example</span></span>
### <a name="request"></a><span data-ttu-id="f1f0d-207">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f1f0d-207">Request</span></span>
<span data-ttu-id="f1f0d-208">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-208">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies
Content-type: application/json
Content-length: 856

{
  "@odata.type": "#microsoft.graph.windows10MobileCompliancePolicy",
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

### <a name="response"></a><span data-ttu-id="f1f0d-209">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f1f0d-209">Response</span></span>
<span data-ttu-id="f1f0d-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f1f0d-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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








