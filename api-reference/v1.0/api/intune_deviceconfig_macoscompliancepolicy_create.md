# <a name="create-macoscompliancepolicy"></a><span data-ttu-id="56774-101">Crear macOSCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="56774-101">Create macOSCompliancePolicy</span></span>

> <span data-ttu-id="56774-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="56774-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="56774-103">Cree un objeto [macOSCompliancePolicy](../resources/intune_deviceconfig_macoscompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="56774-103">Create a new [macOSCompliancePolicy](../resources/intune_deviceconfig_macoscompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="56774-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="56774-104">Prerequisites</span></span>
<span data-ttu-id="56774-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="56774-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="56774-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="56774-107">Permission type</span></span>|<span data-ttu-id="56774-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="56774-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="56774-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="56774-109">Delegated (work or school account)</span></span>|<span data-ttu-id="56774-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="56774-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="56774-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="56774-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="56774-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="56774-112">Not supported.</span></span>|
|<span data-ttu-id="56774-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="56774-113">Application</span></span>|<span data-ttu-id="56774-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="56774-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="56774-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="56774-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="56774-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="56774-116">Request headers</span></span>
|<span data-ttu-id="56774-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56774-117">Header</span></span>|<span data-ttu-id="56774-118">Valor</span><span class="sxs-lookup"><span data-stu-id="56774-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="56774-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="56774-119">Authorization</span></span>|<span data-ttu-id="56774-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="56774-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="56774-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="56774-121">Accept</span></span>|<span data-ttu-id="56774-122">application/json</span><span class="sxs-lookup"><span data-stu-id="56774-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="56774-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="56774-123">Request body</span></span>
<span data-ttu-id="56774-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto macOSCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="56774-124">In the request body, supply a JSON representation for the macOSCompliancePolicy object.</span></span>

<span data-ttu-id="56774-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto macOSCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="56774-125">The following table shows the properties that are required when you create the macOSCompliancePolicy.</span></span>

|<span data-ttu-id="56774-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="56774-126">Property</span></span>|<span data-ttu-id="56774-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="56774-127">Type</span></span>|<span data-ttu-id="56774-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="56774-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="56774-129">id</span><span class="sxs-lookup"><span data-stu-id="56774-129">id</span></span>|<span data-ttu-id="56774-130">String</span><span class="sxs-lookup"><span data-stu-id="56774-130">String</span></span>|<span data-ttu-id="56774-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="56774-131">Key of the entity.</span></span> <span data-ttu-id="56774-132">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="56774-132">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="56774-133">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="56774-133">createdDateTime</span></span>|<span data-ttu-id="56774-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="56774-134">DateTimeOffset</span></span>|<span data-ttu-id="56774-135">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="56774-135">DateTime the object was created.</span></span> <span data-ttu-id="56774-136">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="56774-136">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="56774-137">description</span><span class="sxs-lookup"><span data-stu-id="56774-137">description</span></span>|<span data-ttu-id="56774-138">String</span><span class="sxs-lookup"><span data-stu-id="56774-138">String</span></span>|<span data-ttu-id="56774-139">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56774-139">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="56774-140">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="56774-140">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="56774-141">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="56774-141">lastModifiedDateTime</span></span>|<span data-ttu-id="56774-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="56774-142">DateTimeOffset</span></span>|<span data-ttu-id="56774-143">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="56774-143">DateTime the object was last modified.</span></span> <span data-ttu-id="56774-144">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="56774-144">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="56774-145">displayName</span><span class="sxs-lookup"><span data-stu-id="56774-145">displayName</span></span>|<span data-ttu-id="56774-146">String</span><span class="sxs-lookup"><span data-stu-id="56774-146">String</span></span>|<span data-ttu-id="56774-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56774-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="56774-148">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="56774-148">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="56774-149">version</span><span class="sxs-lookup"><span data-stu-id="56774-149">version</span></span>|<span data-ttu-id="56774-150">Int32</span><span class="sxs-lookup"><span data-stu-id="56774-150">Int32</span></span>|<span data-ttu-id="56774-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56774-151">Version of the device configuration.</span></span> <span data-ttu-id="56774-152">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="56774-152">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="56774-153">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="56774-153">passwordRequired</span></span>|<span data-ttu-id="56774-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="56774-154">Boolean</span></span>|<span data-ttu-id="56774-155">Si quiere requerir o no una contraseña.</span><span class="sxs-lookup"><span data-stu-id="56774-155">Whether or not to require a password.</span></span>|
|<span data-ttu-id="56774-156">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="56774-156">passwordBlockSimple</span></span>|<span data-ttu-id="56774-157">Booleano</span><span class="sxs-lookup"><span data-stu-id="56774-157">Boolean</span></span>|<span data-ttu-id="56774-158">Indica si se van a bloquear las contraseñas simples.</span><span class="sxs-lookup"><span data-stu-id="56774-158">Indicates whether or not to block simple passwords.</span></span>|
|<span data-ttu-id="56774-159">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="56774-159">passwordExpirationDays</span></span>|<span data-ttu-id="56774-160">Int32</span><span class="sxs-lookup"><span data-stu-id="56774-160">Int32</span></span>|<span data-ttu-id="56774-161">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="56774-161">Number of days before the password expires.</span></span> <span data-ttu-id="56774-162">Valores válidos de 1 a 65535</span><span class="sxs-lookup"><span data-stu-id="56774-162">Valid values 1 to 65535</span></span>|
|<span data-ttu-id="56774-163">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="56774-163">passwordMinimumLength</span></span>|<span data-ttu-id="56774-164">Int32</span><span class="sxs-lookup"><span data-stu-id="56774-164">Int32</span></span>|<span data-ttu-id="56774-165">Longitud mínima de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="56774-165">Minimum length of password.</span></span> <span data-ttu-id="56774-166">Valores válidos de 4 a 14</span><span class="sxs-lookup"><span data-stu-id="56774-166">Valid values 4 to 14</span></span>|
|<span data-ttu-id="56774-167">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="56774-167">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="56774-168">Int32</span><span class="sxs-lookup"><span data-stu-id="56774-168">Int32</span></span>|<span data-ttu-id="56774-169">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="56774-169">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="56774-170">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="56774-170">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="56774-171">Int32</span><span class="sxs-lookup"><span data-stu-id="56774-171">Int32</span></span>|<span data-ttu-id="56774-172">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="56774-172">Number of previous passwords to block.</span></span> <span data-ttu-id="56774-173">Valores válidos de 1 a 24.</span><span class="sxs-lookup"><span data-stu-id="56774-173">Valid values 1 to 24</span></span>|
|<span data-ttu-id="56774-174">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="56774-174">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="56774-175">Int32</span><span class="sxs-lookup"><span data-stu-id="56774-175">Int32</span></span>|<span data-ttu-id="56774-176">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="56774-176">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="56774-177">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="56774-177">passwordRequiredType</span></span>|[<span data-ttu-id="56774-178">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="56774-178">requiredPasswordType</span></span>](../resources/intune_deviceconfig_requiredpasswordtype.md)|<span data-ttu-id="56774-179">Tipo de contraseña necesaria.</span><span class="sxs-lookup"><span data-stu-id="56774-179">The required password type.</span></span> <span data-ttu-id="56774-180">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="56774-180">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="56774-181">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="56774-181">osMinimumVersion</span></span>|<span data-ttu-id="56774-182">String</span><span class="sxs-lookup"><span data-stu-id="56774-182">String</span></span>|<span data-ttu-id="56774-183">Versión mínima de iOS.</span><span class="sxs-lookup"><span data-stu-id="56774-183">Minimum IOS version.</span></span>|
|<span data-ttu-id="56774-184">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="56774-184">osMaximumVersion</span></span>|<span data-ttu-id="56774-185">String</span><span class="sxs-lookup"><span data-stu-id="56774-185">String</span></span>|<span data-ttu-id="56774-186">Versión máxima de iOS.</span><span class="sxs-lookup"><span data-stu-id="56774-186">Maximum IOS version.</span></span>|
|<span data-ttu-id="56774-187">systemIntegrityProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="56774-187">systemIntegrityProtectionEnabled</span></span>|<span data-ttu-id="56774-188">Booleano</span><span class="sxs-lookup"><span data-stu-id="56774-188">Boolean</span></span>|<span data-ttu-id="56774-189">Requiere que los dispositivos hayan habilitado la protección de integridad del sistema.</span><span class="sxs-lookup"><span data-stu-id="56774-189">Require that devices have enabled system integrity protection.</span></span>|
|<span data-ttu-id="56774-190">deviceThreatProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="56774-190">deviceThreatProtectionEnabled</span></span>|<span data-ttu-id="56774-191">Booleano</span><span class="sxs-lookup"><span data-stu-id="56774-191">Boolean</span></span>|<span data-ttu-id="56774-192">Requiere que los dispositivos hayan habilitado la protección contra amenazas de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56774-192">Require that devices have enabled device threat protection .</span></span>|
|<span data-ttu-id="56774-193">deviceThreatProtectionRequiredSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="56774-193">deviceThreatProtectionRequiredSecurityLevel</span></span>|[<span data-ttu-id="56774-194">deviceThreatProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="56774-194">deviceThreatProtectionLevel</span></span>](../resources/intune_deviceconfig_devicethreatprotectionlevel.md)|<span data-ttu-id="56774-195">Exigir que el nivel de riesgo mínimo de Mobile Threat Protection informe del no cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="56774-195">Require Mobile Threat Protection minimum risk level to report noncompliance.</span></span> <span data-ttu-id="56774-196">Los valores posibles son: `unavailable`, `secured`, `low`, `medium`, `high` y `notSet`.</span><span class="sxs-lookup"><span data-stu-id="56774-196">Possible values are: `unavailable`, `secured`, `low`, `medium`, `high`, `notSet`.</span></span>|
|<span data-ttu-id="56774-197">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="56774-197">storageRequireEncryption</span></span>|<span data-ttu-id="56774-198">Booleano</span><span class="sxs-lookup"><span data-stu-id="56774-198">Boolean</span></span>|<span data-ttu-id="56774-199">Exige el cifrado en dispositivos Mac OS.</span><span class="sxs-lookup"><span data-stu-id="56774-199">Require encryption on Mac OS devices.</span></span>|
|<span data-ttu-id="56774-200">firewallEnabled</span><span class="sxs-lookup"><span data-stu-id="56774-200">firewallEnabled</span></span>|<span data-ttu-id="56774-201">Booleano</span><span class="sxs-lookup"><span data-stu-id="56774-201">Boolean</span></span>|<span data-ttu-id="56774-202">Si el firewall se debe habilitar o no.</span><span class="sxs-lookup"><span data-stu-id="56774-202">Whether the firewall should be enabled or not.</span></span>|
|<span data-ttu-id="56774-203">firewallBlockAllIncoming</span><span class="sxs-lookup"><span data-stu-id="56774-203">firewallBlockAllIncoming</span></span>|<span data-ttu-id="56774-204">Booleano</span><span class="sxs-lookup"><span data-stu-id="56774-204">Boolean</span></span>|<span data-ttu-id="56774-205">Corresponde a la opción "Bloquear todas las conexiones entrantes".</span><span class="sxs-lookup"><span data-stu-id="56774-205">Corresponds to the “Block all incoming connections” option.</span></span>|
|<span data-ttu-id="56774-206">firewallEnableStealthMode</span><span class="sxs-lookup"><span data-stu-id="56774-206">firewallEnableStealthMode</span></span>|<span data-ttu-id="56774-207">Booleano</span><span class="sxs-lookup"><span data-stu-id="56774-207">Boolean</span></span>|<span data-ttu-id="56774-208">Corresponde a "Habilitar modo silencioso".</span><span class="sxs-lookup"><span data-stu-id="56774-208">Corresponds to “Enable stealth mode.”</span></span>|



## <a name="response"></a><span data-ttu-id="56774-209">Respuesta</span><span class="sxs-lookup"><span data-stu-id="56774-209">Response</span></span>
<span data-ttu-id="56774-210">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [macOSCompliancePolicy](../resources/intune_deviceconfig_macoscompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="56774-210">If successful, this method returns a `201 Created` response code and a [macOSCompliancePolicy](../resources/intune_deviceconfig_macoscompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="56774-211">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="56774-211">Example</span></span>
### <a name="request"></a><span data-ttu-id="56774-212">Solicitud</span><span class="sxs-lookup"><span data-stu-id="56774-212">Request</span></span>
<span data-ttu-id="56774-213">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="56774-213">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies
Content-type: application/json
Content-length: 849

{
  "@odata.type": "#microsoft.graph.macOSCompliancePolicy",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "passwordRequired": true,
  "passwordBlockSimple": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordMinimumCharacterSetCount": 0,
  "passwordRequiredType": "alphanumeric",
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "systemIntegrityProtectionEnabled": true,
  "deviceThreatProtectionEnabled": true,
  "deviceThreatProtectionRequiredSecurityLevel": "secured",
  "storageRequireEncryption": true,
  "firewallEnabled": true,
  "firewallBlockAllIncoming": true,
  "firewallEnableStealthMode": true
}
```

### <a name="response"></a><span data-ttu-id="56774-214">Respuesta</span><span class="sxs-lookup"><span data-stu-id="56774-214">Response</span></span>
<span data-ttu-id="56774-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="56774-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1021

{
  "@odata.type": "#microsoft.graph.macOSCompliancePolicy",
  "id": "ddbadff3-dff3-ddba-f3df-baddf3dfbadd",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "passwordRequired": true,
  "passwordBlockSimple": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordMinimumCharacterSetCount": 0,
  "passwordRequiredType": "alphanumeric",
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "systemIntegrityProtectionEnabled": true,
  "deviceThreatProtectionEnabled": true,
  "deviceThreatProtectionRequiredSecurityLevel": "secured",
  "storageRequireEncryption": true,
  "firewallEnabled": true,
  "firewallBlockAllIncoming": true,
  "firewallEnableStealthMode": true
}
```



