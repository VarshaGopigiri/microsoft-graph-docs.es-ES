# <a name="create-ioscompliancepolicy"></a><span data-ttu-id="5bf33-101">Crear iosCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="5bf33-101">Create iosCompliancePolicy</span></span>

> <span data-ttu-id="5bf33-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5bf33-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5bf33-103">Crear un objeto [iosCompliancePolicy](../resources/intune_deviceconfig_ioscompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5bf33-103">Create a new [plannerBucket](../resources/intune_deviceconfig_ioscompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5bf33-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5bf33-104">Prerequisites</span></span>
<span data-ttu-id="5bf33-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="5bf33-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="5bf33-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5bf33-107">Permission type</span></span>|<span data-ttu-id="5bf33-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5bf33-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5bf33-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5bf33-109">Delegated (work or school account)</span></span>|<span data-ttu-id="5bf33-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5bf33-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="5bf33-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5bf33-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5bf33-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5bf33-112">Not supported.</span></span>|
|<span data-ttu-id="5bf33-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5bf33-113">Application</span></span>|<span data-ttu-id="5bf33-114">No compatible.</span><span class="sxs-lookup"><span data-stu-id="5bf33-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5bf33-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5bf33-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="5bf33-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5bf33-116">Request headers</span></span>
|<span data-ttu-id="5bf33-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5bf33-117">Header</span></span>|<span data-ttu-id="5bf33-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5bf33-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5bf33-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="5bf33-119">Authorization</span></span>|<span data-ttu-id="5bf33-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5bf33-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="5bf33-121">Accept</span><span class="sxs-lookup"><span data-stu-id="5bf33-121">Accept</span></span>|<span data-ttu-id="5bf33-122">application/json</span><span class="sxs-lookup"><span data-stu-id="5bf33-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5bf33-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5bf33-123">Request body</span></span>
<span data-ttu-id="5bf33-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="5bf33-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="5bf33-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="5bf33-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="5bf33-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5bf33-126">Property</span></span>|<span data-ttu-id="5bf33-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="5bf33-127">Type</span></span>|<span data-ttu-id="5bf33-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="5bf33-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5bf33-129">id</span><span class="sxs-lookup"><span data-stu-id="5bf33-129">id</span></span>|<span data-ttu-id="5bf33-130">String</span><span class="sxs-lookup"><span data-stu-id="5bf33-130">String</span></span>|<span data-ttu-id="5bf33-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="5bf33-131">Key of the setting.</span></span> <span data-ttu-id="5bf33-132">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5bf33-132">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="5bf33-133">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="5bf33-133">createdDateTime</span></span>|<span data-ttu-id="5bf33-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5bf33-134">DateTimeOffset</span></span>|<span data-ttu-id="5bf33-135">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="5bf33-135">DateTime the object was created.</span></span> <span data-ttu-id="5bf33-136">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5bf33-136">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="5bf33-137">description</span><span class="sxs-lookup"><span data-stu-id="5bf33-137">description</span></span>|<span data-ttu-id="5bf33-138">String</span><span class="sxs-lookup"><span data-stu-id="5bf33-138">String</span></span>|<span data-ttu-id="5bf33-139">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5bf33-139">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="5bf33-140">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5bf33-140">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="5bf33-141">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="5bf33-141">lastModifiedDateTime</span></span>|<span data-ttu-id="5bf33-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5bf33-142">DateTimeOffset</span></span>|<span data-ttu-id="5bf33-143">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="5bf33-143">Indicates the date the object was last modified.</span></span> <span data-ttu-id="5bf33-144">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5bf33-144">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="5bf33-145">displayName</span><span class="sxs-lookup"><span data-stu-id="5bf33-145">displayName</span></span>|<span data-ttu-id="5bf33-146">String</span><span class="sxs-lookup"><span data-stu-id="5bf33-146">String</span></span>|<span data-ttu-id="5bf33-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5bf33-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="5bf33-148">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5bf33-148">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="5bf33-149">version</span><span class="sxs-lookup"><span data-stu-id="5bf33-149">version</span></span>|<span data-ttu-id="5bf33-150">Int32</span><span class="sxs-lookup"><span data-stu-id="5bf33-150">Int32</span></span>|<span data-ttu-id="5bf33-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5bf33-151">Version of the device configuration.</span></span> <span data-ttu-id="5bf33-152">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5bf33-152">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="5bf33-153">passcodeBlockSimple</span><span class="sxs-lookup"><span data-stu-id="5bf33-153">passcodeBlockSimple</span></span>|<span data-ttu-id="5bf33-154">Boolean</span><span class="sxs-lookup"><span data-stu-id="5bf33-154">Boolean</span></span>|<span data-ttu-id="5bf33-155">Indica si se van a bloquear los códigos de acceso simples.</span><span class="sxs-lookup"><span data-stu-id="5bf33-155">Indicates whether or not to block simple passcodes.</span></span>|
|<span data-ttu-id="5bf33-156">passcodeExpirationDays</span><span class="sxs-lookup"><span data-stu-id="5bf33-156">passcodeExpirationDays</span></span>|<span data-ttu-id="5bf33-157">Int32</span><span class="sxs-lookup"><span data-stu-id="5bf33-157">Int32</span></span>|<span data-ttu-id="5bf33-158">Número de días antes de que expire el código de acceso.</span><span class="sxs-lookup"><span data-stu-id="5bf33-158">Number of days before the passcode expires.</span></span> <span data-ttu-id="5bf33-159">Valores válidos de 1 a 65 535.</span><span class="sxs-lookup"><span data-stu-id="5bf33-159">Valid values 1 to 65535</span></span>|
|<span data-ttu-id="5bf33-160">passcodeMinimumLength</span><span class="sxs-lookup"><span data-stu-id="5bf33-160">passcodeMinimumLength</span></span>|<span data-ttu-id="5bf33-161">Int32</span><span class="sxs-lookup"><span data-stu-id="5bf33-161">Int32</span></span>|<span data-ttu-id="5bf33-162">Longitud mínima del código de acceso.</span><span class="sxs-lookup"><span data-stu-id="5bf33-162">Minimum length of passcode.</span></span> <span data-ttu-id="5bf33-163">Valores válidos de 4 a 14.</span><span class="sxs-lookup"><span data-stu-id="5bf33-163">Valid values 4 to 14</span></span>|
|<span data-ttu-id="5bf33-164">passcodeMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="5bf33-164">passcodeMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="5bf33-165">Int32</span><span class="sxs-lookup"><span data-stu-id="5bf33-165">Int32</span></span>|<span data-ttu-id="5bf33-166">Minutos de inactividad antes de que sea necesario un código de acceso.</span><span class="sxs-lookup"><span data-stu-id="5bf33-166">Minutes of inactivity before a passcode is required.</span></span>|
|<span data-ttu-id="5bf33-167">passcodePreviousPasscodeBlockCount</span><span class="sxs-lookup"><span data-stu-id="5bf33-167">passcodePreviousPasscodeBlockCount</span></span>|<span data-ttu-id="5bf33-168">Int32</span><span class="sxs-lookup"><span data-stu-id="5bf33-168">Int32</span></span>|<span data-ttu-id="5bf33-169">Número de códigos de acceso anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="5bf33-169">Number of previous passcodes to block.</span></span> <span data-ttu-id="5bf33-170">Valores válidos de 1 a 24.</span><span class="sxs-lookup"><span data-stu-id="5bf33-170">Valid values 1 to 24</span></span>|
|<span data-ttu-id="5bf33-171">passcodeMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="5bf33-171">passcodeMinimumCharacterSetCount</span></span>|<span data-ttu-id="5bf33-172">Int32</span><span class="sxs-lookup"><span data-stu-id="5bf33-172">Int32</span></span>|<span data-ttu-id="5bf33-173">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="5bf33-173">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="5bf33-174">passcodeRequiredType</span><span class="sxs-lookup"><span data-stu-id="5bf33-174">passcodeRequiredType</span></span>|<span data-ttu-id="5bf33-175">String</span><span class="sxs-lookup"><span data-stu-id="5bf33-175">String</span></span>|<span data-ttu-id="5bf33-176">Tipo de código de acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="5bf33-176">The required passcode type.</span></span> <span data-ttu-id="5bf33-177">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="5bf33-177">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="5bf33-178">passcodeRequired</span><span class="sxs-lookup"><span data-stu-id="5bf33-178">passcodeRequired</span></span>|<span data-ttu-id="5bf33-179">Boolean</span><span class="sxs-lookup"><span data-stu-id="5bf33-179">Boolean</span></span>|<span data-ttu-id="5bf33-180">Indica si se va a requerir un código de acceso.</span><span class="sxs-lookup"><span data-stu-id="5bf33-180">Indicates whether or not to require a passcode.</span></span>|
|<span data-ttu-id="5bf33-181">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="5bf33-181">osMinimumVersion</span></span>|<span data-ttu-id="5bf33-182">String</span><span class="sxs-lookup"><span data-stu-id="5bf33-182">String</span></span>|<span data-ttu-id="5bf33-183">Versión mínima de iOS.</span><span class="sxs-lookup"><span data-stu-id="5bf33-183">Minimum IOS version.</span></span>|
|<span data-ttu-id="5bf33-184">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="5bf33-184">osMaximumVersion</span></span>|<span data-ttu-id="5bf33-185">String</span><span class="sxs-lookup"><span data-stu-id="5bf33-185">String</span></span>|<span data-ttu-id="5bf33-186">Versión máxima de iOS.</span><span class="sxs-lookup"><span data-stu-id="5bf33-186">Maximum IOS version.</span></span>|
|<span data-ttu-id="5bf33-187">securityBlockJailbrokenDevices</span><span class="sxs-lookup"><span data-stu-id="5bf33-187">securityBlockJailbrokenDevices</span></span>|<span data-ttu-id="5bf33-188">Boolean</span><span class="sxs-lookup"><span data-stu-id="5bf33-188">Boolean</span></span>|<span data-ttu-id="5bf33-189">No pueden usarse dispositivos con jailbreak o rooting.</span><span class="sxs-lookup"><span data-stu-id="5bf33-189">Devices must not be jailbroken or rooted.</span></span>|
|<span data-ttu-id="5bf33-190">deviceThreatProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="5bf33-190">deviceThreatProtectionEnabled</span></span>|<span data-ttu-id="5bf33-191">Boolean</span><span class="sxs-lookup"><span data-stu-id="5bf33-191">Boolean</span></span>|<span data-ttu-id="5bf33-192">Requiere que los dispositivos hayan habilitado la protección contra amenazas de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5bf33-192">Require that devices have enabled device threat protection .</span></span>|
|<span data-ttu-id="5bf33-193">deviceThreatProtectionRequiredSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="5bf33-193">deviceThreatProtectionRequiredSecurityLevel</span></span>|<span data-ttu-id="5bf33-194">String</span><span class="sxs-lookup"><span data-stu-id="5bf33-194">String</span></span>|<span data-ttu-id="5bf33-195">Requiere que el nivel de riesgo mínimo de Mobile Threat Protection informe del no cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="5bf33-195">Require Mobile Threat Protection minimum risk level to report noncompliance.</span></span> <span data-ttu-id="5bf33-196">Los valores posibles son: `unavailable`, `secured`, `low`, `medium`, `high` y `notSet`.</span><span class="sxs-lookup"><span data-stu-id="5bf33-196">Possible values are: `unavailable`, `secured`, `low`, `medium`, `high`, `notSet`.</span></span>|
|<span data-ttu-id="5bf33-197">managedEmailProfileRequired</span><span class="sxs-lookup"><span data-stu-id="5bf33-197">managedEmailProfileRequired</span></span>|<span data-ttu-id="5bf33-198">Boolean</span><span class="sxs-lookup"><span data-stu-id="5bf33-198">Boolean</span></span>|<span data-ttu-id="5bf33-199">Indica si se va a requerir un perfil de correo electrónico administrado.</span><span class="sxs-lookup"><span data-stu-id="5bf33-199">Indicates whether or not to require a managed email profile.</span></span>|



## <a name="response"></a><span data-ttu-id="5bf33-200">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5bf33-200">Response</span></span>
<span data-ttu-id="5bf33-201">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosCompliancePolicy](../resources/intune_deviceconfig_ioscompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5bf33-201">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_deviceconfig_ioscompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5bf33-202">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5bf33-202">Example</span></span>
### <a name="request"></a><span data-ttu-id="5bf33-203">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5bf33-203">Request</span></span>
<span data-ttu-id="5bf33-204">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5bf33-204">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies
Content-type: application/json
Content-length: 809

{
  "@odata.type": "#microsoft.graph.iosCompliancePolicy",
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

### <a name="response"></a><span data-ttu-id="5bf33-205">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5bf33-205">Response</span></span>
<span data-ttu-id="5bf33-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5bf33-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



