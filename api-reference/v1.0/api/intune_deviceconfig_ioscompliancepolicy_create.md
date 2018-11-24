# <a name="create-ioscompliancepolicy"></a><span data-ttu-id="9c40b-101">Crear iosCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="9c40b-101">Create iosCompliancePolicy</span></span>

> <span data-ttu-id="9c40b-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9c40b-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9c40b-103">Crear un objeto [iosCompliancePolicy](../resources/intune_deviceconfig_ioscompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="9c40b-103">Create a new [iosCompliancePolicy](../resources/intune_deviceconfig_ioscompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9c40b-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9c40b-104">Prerequisites</span></span>
<span data-ttu-id="9c40b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9c40b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9c40b-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9c40b-107">Permission type</span></span>|<span data-ttu-id="9c40b-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9c40b-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9c40b-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9c40b-109">Delegated (work or school account)</span></span>|<span data-ttu-id="9c40b-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9c40b-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="9c40b-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9c40b-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9c40b-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9c40b-112">Not supported.</span></span>|
|<span data-ttu-id="9c40b-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9c40b-113">Application</span></span>|<span data-ttu-id="9c40b-114">No compatible.</span><span class="sxs-lookup"><span data-stu-id="9c40b-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9c40b-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9c40b-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="9c40b-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9c40b-116">Request headers</span></span>
|<span data-ttu-id="9c40b-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c40b-117">Header</span></span>|<span data-ttu-id="9c40b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="9c40b-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9c40b-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="9c40b-119">Authorization</span></span>|<span data-ttu-id="9c40b-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9c40b-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9c40b-121">Accept</span><span class="sxs-lookup"><span data-stu-id="9c40b-121">Accept</span></span>|<span data-ttu-id="9c40b-122">application/json</span><span class="sxs-lookup"><span data-stu-id="9c40b-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9c40b-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9c40b-123">Request body</span></span>
<span data-ttu-id="9c40b-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="9c40b-124">In the request body, supply a JSON representation for the iosCompliancePolicy object.</span></span>

<span data-ttu-id="9c40b-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="9c40b-125">The following table shows the properties that are required when you create the iosCompliancePolicy.</span></span>

|<span data-ttu-id="9c40b-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9c40b-126">Property</span></span>|<span data-ttu-id="9c40b-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="9c40b-127">Type</span></span>|<span data-ttu-id="9c40b-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c40b-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9c40b-129">id</span><span class="sxs-lookup"><span data-stu-id="9c40b-129">id</span></span>|<span data-ttu-id="9c40b-130">String</span><span class="sxs-lookup"><span data-stu-id="9c40b-130">String</span></span>|<span data-ttu-id="9c40b-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="9c40b-131">Key of the entity.</span></span> <span data-ttu-id="9c40b-132">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="9c40b-132">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="9c40b-133">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="9c40b-133">createdDateTime</span></span>|<span data-ttu-id="9c40b-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9c40b-134">DateTimeOffset</span></span>|<span data-ttu-id="9c40b-135">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="9c40b-135">DateTime the object was created.</span></span> <span data-ttu-id="9c40b-136">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="9c40b-136">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="9c40b-137">description</span><span class="sxs-lookup"><span data-stu-id="9c40b-137">description</span></span>|<span data-ttu-id="9c40b-138">String</span><span class="sxs-lookup"><span data-stu-id="9c40b-138">String</span></span>|<span data-ttu-id="9c40b-139">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c40b-139">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="9c40b-140">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="9c40b-140">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="9c40b-141">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="9c40b-141">lastModifiedDateTime</span></span>|<span data-ttu-id="9c40b-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9c40b-142">DateTimeOffset</span></span>|<span data-ttu-id="9c40b-143">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="9c40b-143">DateTime the object was last modified.</span></span> <span data-ttu-id="9c40b-144">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="9c40b-144">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="9c40b-145">displayName</span><span class="sxs-lookup"><span data-stu-id="9c40b-145">displayName</span></span>|<span data-ttu-id="9c40b-146">String</span><span class="sxs-lookup"><span data-stu-id="9c40b-146">String</span></span>|<span data-ttu-id="9c40b-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c40b-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="9c40b-148">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="9c40b-148">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="9c40b-149">version</span><span class="sxs-lookup"><span data-stu-id="9c40b-149">version</span></span>|<span data-ttu-id="9c40b-150">Int32</span><span class="sxs-lookup"><span data-stu-id="9c40b-150">Int32</span></span>|<span data-ttu-id="9c40b-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c40b-151">Version of the device configuration.</span></span> <span data-ttu-id="9c40b-152">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="9c40b-152">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="9c40b-153">passcodeBlockSimple</span><span class="sxs-lookup"><span data-stu-id="9c40b-153">passcodeBlockSimple</span></span>|<span data-ttu-id="9c40b-154">Boolean</span><span class="sxs-lookup"><span data-stu-id="9c40b-154">Boolean</span></span>|<span data-ttu-id="9c40b-155">Indica si se van a bloquear los códigos de acceso simples.</span><span class="sxs-lookup"><span data-stu-id="9c40b-155">Indicates whether or not to block simple passcodes.</span></span>|
|<span data-ttu-id="9c40b-156">passcodeExpirationDays</span><span class="sxs-lookup"><span data-stu-id="9c40b-156">passcodeExpirationDays</span></span>|<span data-ttu-id="9c40b-157">Int32</span><span class="sxs-lookup"><span data-stu-id="9c40b-157">Int32</span></span>|<span data-ttu-id="9c40b-158">Número de días antes de que expire el código de acceso.</span><span class="sxs-lookup"><span data-stu-id="9c40b-158">Number of days before the passcode expires.</span></span> <span data-ttu-id="9c40b-159">Valores válidos de 1 a 65535</span><span class="sxs-lookup"><span data-stu-id="9c40b-159">Valid values 1 to 65535</span></span>|
|<span data-ttu-id="9c40b-160">passcodeMinimumLength</span><span class="sxs-lookup"><span data-stu-id="9c40b-160">passcodeMinimumLength</span></span>|<span data-ttu-id="9c40b-161">Int32</span><span class="sxs-lookup"><span data-stu-id="9c40b-161">Int32</span></span>|<span data-ttu-id="9c40b-162">Longitud mínima de los códigos de acceso.</span><span class="sxs-lookup"><span data-stu-id="9c40b-162">Minimum length of passcode.</span></span> <span data-ttu-id="9c40b-163">Valores válidos de 4 a 14</span><span class="sxs-lookup"><span data-stu-id="9c40b-163">Valid values 4 to 14</span></span>|
|<span data-ttu-id="9c40b-164">passcodeMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="9c40b-164">passcodeMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="9c40b-165">Int32</span><span class="sxs-lookup"><span data-stu-id="9c40b-165">Int32</span></span>|<span data-ttu-id="9c40b-166">Minutos de inactividad antes de que sea necesario un código de acceso.</span><span class="sxs-lookup"><span data-stu-id="9c40b-166">Minutes of inactivity before a passcode is required.</span></span>|
|<span data-ttu-id="9c40b-167">passcodePreviousPasscodeBlockCount</span><span class="sxs-lookup"><span data-stu-id="9c40b-167">passcodePreviousPasscodeBlockCount</span></span>|<span data-ttu-id="9c40b-168">Int32</span><span class="sxs-lookup"><span data-stu-id="9c40b-168">Int32</span></span>|<span data-ttu-id="9c40b-169">Número de códigos de acceso anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="9c40b-169">Number of previous passcodes to block.</span></span> <span data-ttu-id="9c40b-170">Valores válidos de 1 a 24.</span><span class="sxs-lookup"><span data-stu-id="9c40b-170">Valid values 1 to 24</span></span>|
|<span data-ttu-id="9c40b-171">passcodeMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="9c40b-171">passcodeMinimumCharacterSetCount</span></span>|<span data-ttu-id="9c40b-172">Int32</span><span class="sxs-lookup"><span data-stu-id="9c40b-172">Int32</span></span>|<span data-ttu-id="9c40b-173">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="9c40b-173">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="9c40b-174">passcodeRequiredType</span><span class="sxs-lookup"><span data-stu-id="9c40b-174">passcodeRequiredType</span></span>|[<span data-ttu-id="9c40b-175">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="9c40b-175">requiredPasswordType</span></span>](../resources/intune_deviceconfig_requiredpasswordtype.md)|<span data-ttu-id="9c40b-176">Tipo de código de acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="9c40b-176">The required passcode type.</span></span> <span data-ttu-id="9c40b-177">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="9c40b-177">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="9c40b-178">passcodeRequired</span><span class="sxs-lookup"><span data-stu-id="9c40b-178">passcodeRequired</span></span>|<span data-ttu-id="9c40b-179">Boolean</span><span class="sxs-lookup"><span data-stu-id="9c40b-179">Boolean</span></span>|<span data-ttu-id="9c40b-180">Indica si se va a requerir un código de acceso.</span><span class="sxs-lookup"><span data-stu-id="9c40b-180">Indicates whether or not to require a passcode.</span></span>|
|<span data-ttu-id="9c40b-181">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="9c40b-181">osMinimumVersion</span></span>|<span data-ttu-id="9c40b-182">String</span><span class="sxs-lookup"><span data-stu-id="9c40b-182">String</span></span>|<span data-ttu-id="9c40b-183">Versión mínima de iOS.</span><span class="sxs-lookup"><span data-stu-id="9c40b-183">Minimum IOS version.</span></span>|
|<span data-ttu-id="9c40b-184">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="9c40b-184">osMaximumVersion</span></span>|<span data-ttu-id="9c40b-185">String</span><span class="sxs-lookup"><span data-stu-id="9c40b-185">String</span></span>|<span data-ttu-id="9c40b-186">Versión máxima de iOS.</span><span class="sxs-lookup"><span data-stu-id="9c40b-186">Maximum IOS version.</span></span>|
|<span data-ttu-id="9c40b-187">securityBlockJailbrokenDevices</span><span class="sxs-lookup"><span data-stu-id="9c40b-187">securityBlockJailbrokenDevices</span></span>|<span data-ttu-id="9c40b-188">Boolean</span><span class="sxs-lookup"><span data-stu-id="9c40b-188">Boolean</span></span>|<span data-ttu-id="9c40b-189">No pueden usarse dispositivos con jailbreak o rooting.</span><span class="sxs-lookup"><span data-stu-id="9c40b-189">Devices must not be jailbroken or rooted.</span></span>|
|<span data-ttu-id="9c40b-190">deviceThreatProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="9c40b-190">deviceThreatProtectionEnabled</span></span>|<span data-ttu-id="9c40b-191">Boolean</span><span class="sxs-lookup"><span data-stu-id="9c40b-191">Boolean</span></span>|<span data-ttu-id="9c40b-192">Requiere que los dispositivos hayan habilitado la protección contra amenazas de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c40b-192">Require that devices have enabled device threat protection .</span></span>|
|<span data-ttu-id="9c40b-193">deviceThreatProtectionRequiredSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="9c40b-193">deviceThreatProtectionRequiredSecurityLevel</span></span>|[<span data-ttu-id="9c40b-194">deviceThreatProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="9c40b-194">deviceThreatProtectionLevel</span></span>](../resources/intune_deviceconfig_devicethreatprotectionlevel.md)|<span data-ttu-id="9c40b-195">Exigir que el nivel de riesgo mínimo de Mobile Threat Protection informe del no cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="9c40b-195">Require Mobile Threat Protection minimum risk level to report noncompliance.</span></span> <span data-ttu-id="9c40b-196">Los valores posibles son: `unavailable`, `secured`, `low`, `medium`, `high` y `notSet`.</span><span class="sxs-lookup"><span data-stu-id="9c40b-196">Possible values are: `unavailable`, `secured`, `low`, `medium`, `high`, `notSet`.</span></span>|
|<span data-ttu-id="9c40b-197">managedEmailProfileRequired</span><span class="sxs-lookup"><span data-stu-id="9c40b-197">managedEmailProfileRequired</span></span>|<span data-ttu-id="9c40b-198">Boolean</span><span class="sxs-lookup"><span data-stu-id="9c40b-198">Boolean</span></span>|<span data-ttu-id="9c40b-199">Indica si se va a requerir un perfil de correo electrónico administrado.</span><span class="sxs-lookup"><span data-stu-id="9c40b-199">Indicates whether or not to require a managed email profile.</span></span>|



## <a name="response"></a><span data-ttu-id="9c40b-200">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9c40b-200">Response</span></span>
<span data-ttu-id="9c40b-201">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosCompliancePolicy](../resources/intune_deviceconfig_ioscompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9c40b-201">If successful, this method returns a `201 Created` response code and a [iosCompliancePolicy](../resources/intune_deviceconfig_ioscompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9c40b-202">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9c40b-202">Example</span></span>
### <a name="request"></a><span data-ttu-id="9c40b-203">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9c40b-203">Request</span></span>
<span data-ttu-id="9c40b-204">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9c40b-204">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies
Content-type: application/json
Content-length: 745

{
  "@odata.type": "#microsoft.graph.iosCompliancePolicy",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "passcodeBlockSimple": true,
  "passcodeExpirationDays": 6,
  "passcodeMinimumLength": 5,
  "passcodeMinutesOfInactivityBeforeLock": 5,
  "passcodePreviousPasscodeBlockCount": 2,
  "passcodeMinimumCharacterSetCount": 0,
  "passcodeRequiredType": "alphanumeric",
  "passcodeRequired": true,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "securityBlockJailbrokenDevices": true,
  "deviceThreatProtectionEnabled": true,
  "deviceThreatProtectionRequiredSecurityLevel": "secured",
  "managedEmailProfileRequired": true
}
```

### <a name="response"></a><span data-ttu-id="9c40b-205">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9c40b-205">Response</span></span>
<span data-ttu-id="9c40b-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9c40b-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 917

{
  "@odata.type": "#microsoft.graph.iosCompliancePolicy",
  "id": "4f501351-1351-4f50-5113-504f5113504f",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "passcodeBlockSimple": true,
  "passcodeExpirationDays": 6,
  "passcodeMinimumLength": 5,
  "passcodeMinutesOfInactivityBeforeLock": 5,
  "passcodePreviousPasscodeBlockCount": 2,
  "passcodeMinimumCharacterSetCount": 0,
  "passcodeRequiredType": "alphanumeric",
  "passcodeRequired": true,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "securityBlockJailbrokenDevices": true,
  "deviceThreatProtectionEnabled": true,
  "deviceThreatProtectionRequiredSecurityLevel": "secured",
  "managedEmailProfileRequired": true
}
```



