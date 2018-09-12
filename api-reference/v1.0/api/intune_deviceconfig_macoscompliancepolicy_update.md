# <a name="update-macoscompliancepolicy"></a><span data-ttu-id="f81bf-101">Actualizar macOSCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="f81bf-101">Update macOSCompliancePolicy</span></span>

> <span data-ttu-id="f81bf-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f81bf-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f81bf-103">Actualice las propiedades de un objeto [macOSCompliancePolicy](../resources/intune_deviceconfig_macoscompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f81bf-103">Update the properties of a [macOSCompliancePolicy](../resources/intune_deviceconfig_macoscompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f81bf-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f81bf-104">Prerequisites</span></span>
<span data-ttu-id="f81bf-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f81bf-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f81bf-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f81bf-107">Permission type</span></span>|<span data-ttu-id="f81bf-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f81bf-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f81bf-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f81bf-109">Delegated (work or school account)</span></span>|<span data-ttu-id="f81bf-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f81bf-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="f81bf-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f81bf-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f81bf-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f81bf-112">Not supported.</span></span>|
|<span data-ttu-id="f81bf-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f81bf-113">Application</span></span>|<span data-ttu-id="f81bf-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f81bf-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f81bf-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f81bf-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="request-headers"></a><span data-ttu-id="f81bf-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f81bf-116">Request headers</span></span>
|<span data-ttu-id="f81bf-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f81bf-117">Header</span></span>|<span data-ttu-id="f81bf-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f81bf-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f81bf-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="f81bf-119">Authorization</span></span>|<span data-ttu-id="f81bf-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f81bf-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f81bf-121">Accept</span><span class="sxs-lookup"><span data-stu-id="f81bf-121">Accept</span></span>|<span data-ttu-id="f81bf-122">application/json</span><span class="sxs-lookup"><span data-stu-id="f81bf-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f81bf-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f81bf-123">Request body</span></span>
<span data-ttu-id="f81bf-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [macOSCompliancePolicy](../resources/intune_deviceconfig_macoscompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f81bf-124">In the request body, supply a JSON representation for the [macOSCompliancePolicy](../resources/intune_deviceconfig_macoscompliancepolicy.md) object.</span></span>

<span data-ttu-id="f81bf-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [macOSCompliancePolicy](../resources/intune_deviceconfig_macoscompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f81bf-125">The following table shows the properties that are required when you create the [macOSCompliancePolicy](../resources/intune_deviceconfig_macoscompliancepolicy.md).</span></span>

|<span data-ttu-id="f81bf-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f81bf-126">Property</span></span>|<span data-ttu-id="f81bf-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="f81bf-127">Type</span></span>|<span data-ttu-id="f81bf-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="f81bf-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f81bf-129">id</span><span class="sxs-lookup"><span data-stu-id="f81bf-129">id</span></span>|<span data-ttu-id="f81bf-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="f81bf-130">String</span></span>|<span data-ttu-id="f81bf-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f81bf-131">Key of the entity.</span></span> <span data-ttu-id="f81bf-132">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f81bf-132">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="f81bf-133">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="f81bf-133">createdDateTime</span></span>|<span data-ttu-id="f81bf-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f81bf-134">DateTimeOffset</span></span>|<span data-ttu-id="f81bf-135">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="f81bf-135">DateTime the object was created.</span></span> <span data-ttu-id="f81bf-136">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f81bf-136">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="f81bf-137">descripción</span><span class="sxs-lookup"><span data-stu-id="f81bf-137">description</span></span>|<span data-ttu-id="f81bf-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="f81bf-138">String</span></span>|<span data-ttu-id="f81bf-139">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f81bf-139">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="f81bf-140">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f81bf-140">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="f81bf-141">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="f81bf-141">lastModifiedDateTime</span></span>|<span data-ttu-id="f81bf-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f81bf-142">DateTimeOffset</span></span>|<span data-ttu-id="f81bf-143">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="f81bf-143">DateTime the object was last modified.</span></span> <span data-ttu-id="f81bf-144">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f81bf-144">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="f81bf-145">displayName</span><span class="sxs-lookup"><span data-stu-id="f81bf-145">displayName</span></span>|<span data-ttu-id="f81bf-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="f81bf-146">String</span></span>|<span data-ttu-id="f81bf-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f81bf-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="f81bf-148">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f81bf-148">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="f81bf-149">Cadena</span><span class="sxs-lookup"><span data-stu-id="f81bf-149">version</span></span>|<span data-ttu-id="f81bf-150">Int32</span><span class="sxs-lookup"><span data-stu-id="f81bf-150">Int32</span></span>|<span data-ttu-id="f81bf-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f81bf-151">Version of the device configuration.</span></span> <span data-ttu-id="f81bf-152">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f81bf-152">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="f81bf-153">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="f81bf-153">passwordRequired</span></span>|<span data-ttu-id="f81bf-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="f81bf-154">Boolean</span></span>|<span data-ttu-id="f81bf-155">Si quiere requerir o no una contraseña.</span><span class="sxs-lookup"><span data-stu-id="f81bf-155">Whether or not to require a password.</span></span>|
|<span data-ttu-id="f81bf-156">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="f81bf-156">passwordBlockSimple</span></span>|<span data-ttu-id="f81bf-157">Booleano</span><span class="sxs-lookup"><span data-stu-id="f81bf-157">Boolean</span></span>|<span data-ttu-id="f81bf-158">Indica si se van a bloquear las contraseñas simples.</span><span class="sxs-lookup"><span data-stu-id="f81bf-158">Indicates whether or not to block simple passwords.</span></span>|
|<span data-ttu-id="f81bf-159">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="f81bf-159">passwordExpirationDays</span></span>|<span data-ttu-id="f81bf-160">Int32</span><span class="sxs-lookup"><span data-stu-id="f81bf-160">Int32</span></span>|<span data-ttu-id="f81bf-161">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="f81bf-161">Number of days before the password expires.</span></span> <span data-ttu-id="f81bf-162">Valores válidos de 1 a 65535</span><span class="sxs-lookup"><span data-stu-id="f81bf-162">Valid values 1 to 65535</span></span>|
|<span data-ttu-id="f81bf-163">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="f81bf-163">passwordMinimumLength</span></span>|<span data-ttu-id="f81bf-164">Int32</span><span class="sxs-lookup"><span data-stu-id="f81bf-164">Int32</span></span>|<span data-ttu-id="f81bf-165">Longitud mínima de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="f81bf-165">Minimum length of password.</span></span> <span data-ttu-id="f81bf-166">Valores válidos de 4 a 14</span><span class="sxs-lookup"><span data-stu-id="f81bf-166">Valid values 4 to 14</span></span>|
|<span data-ttu-id="f81bf-167">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="f81bf-167">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="f81bf-168">Int32</span><span class="sxs-lookup"><span data-stu-id="f81bf-168">Int32</span></span>|<span data-ttu-id="f81bf-169">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="f81bf-169">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="f81bf-170">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="f81bf-170">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="f81bf-171">Int32</span><span class="sxs-lookup"><span data-stu-id="f81bf-171">Int32</span></span>|<span data-ttu-id="f81bf-172">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="f81bf-172">Number of previous passwords to block.</span></span> <span data-ttu-id="f81bf-173">Valores válidos de 1 a 24.</span><span class="sxs-lookup"><span data-stu-id="f81bf-173">Valid values 1 to 24</span></span>|
|<span data-ttu-id="f81bf-174">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="f81bf-174">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="f81bf-175">Int32</span><span class="sxs-lookup"><span data-stu-id="f81bf-175">Int32</span></span>|<span data-ttu-id="f81bf-176">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="f81bf-176">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="f81bf-177">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="f81bf-177">passwordRequiredType</span></span>|[<span data-ttu-id="f81bf-178">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="f81bf-178">requiredPasswordType</span></span>](../resources/intune_deviceconfig_requiredpasswordtype.md)|<span data-ttu-id="f81bf-p111">El tipo de contraseña requerida. Los valores posibles son: `deviceDefault`, `alphanumeric`, `numeric`.</span><span class="sxs-lookup"><span data-stu-id="f81bf-p111">The required password type. The possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="f81bf-181">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="f81bf-181">osMinimumVersion</span></span>|<span data-ttu-id="f81bf-182">Cadena</span><span class="sxs-lookup"><span data-stu-id="f81bf-182">String</span></span>|<span data-ttu-id="f81bf-183">Versión mínima de iOS.</span><span class="sxs-lookup"><span data-stu-id="f81bf-183">Minimum IOS version.</span></span>|
|<span data-ttu-id="f81bf-184">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="f81bf-184">osMaximumVersion</span></span>|<span data-ttu-id="f81bf-185">Cadena</span><span class="sxs-lookup"><span data-stu-id="f81bf-185">String</span></span>|<span data-ttu-id="f81bf-186">Versión máxima de iOS.</span><span class="sxs-lookup"><span data-stu-id="f81bf-186">Maximum IOS version.</span></span>|
|<span data-ttu-id="f81bf-187">systemIntegrityProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="f81bf-187">systemIntegrityProtectionEnabled</span></span>|<span data-ttu-id="f81bf-188">Booleano</span><span class="sxs-lookup"><span data-stu-id="f81bf-188">Boolean</span></span>|<span data-ttu-id="f81bf-189">Requiere que los dispositivos hayan habilitado la protección de integridad del sistema.</span><span class="sxs-lookup"><span data-stu-id="f81bf-189">Require that devices have enabled system integrity protection.</span></span>|
|<span data-ttu-id="f81bf-190">deviceThreatProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="f81bf-190">deviceThreatProtectionEnabled</span></span>|<span data-ttu-id="f81bf-191">Booleano</span><span class="sxs-lookup"><span data-stu-id="f81bf-191">Boolean</span></span>|<span data-ttu-id="f81bf-192">Requiere que los dispositivos hayan habilitado la protección contra amenazas de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f81bf-192">Require that devices have enabled device threat protection .</span></span>|
|<span data-ttu-id="f81bf-193">deviceThreatProtectionRequiredSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="f81bf-193">deviceThreatProtectionRequiredSecurityLevel</span></span>|[<span data-ttu-id="f81bf-194">deviceThreatProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="f81bf-194">deviceThreatProtectionLevel</span></span>](../resources/intune_deviceconfig_devicethreatprotectionlevel.md)|<span data-ttu-id="f81bf-p112">Requerir que el nivel de riesgo mínimo de la Protección contra amenazas móviles informe de un incumplimiento. Los valores posibles son: `unavailable`, `secured`, `low`, `medium`, `high`, `notSet`.</span><span class="sxs-lookup"><span data-stu-id="f81bf-p112">Require Mobile Threat Protection minimum risk level to report noncompliance. The possible values are: `unavailable`, `secured`, `low`, `medium`, `high`, `notSet`.</span></span>|
|<span data-ttu-id="f81bf-197">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="f81bf-197">storageRequireEncryption</span></span>|<span data-ttu-id="f81bf-198">Booleano</span><span class="sxs-lookup"><span data-stu-id="f81bf-198">Boolean</span></span>|<span data-ttu-id="f81bf-199">Exige el cifrado en dispositivos Mac OS.</span><span class="sxs-lookup"><span data-stu-id="f81bf-199">Require encryption on Mac OS devices.</span></span>|
|<span data-ttu-id="f81bf-200">firewallEnabled</span><span class="sxs-lookup"><span data-stu-id="f81bf-200">firewallEnabled</span></span>|<span data-ttu-id="f81bf-201">Booleano</span><span class="sxs-lookup"><span data-stu-id="f81bf-201">Boolean</span></span>|<span data-ttu-id="f81bf-202">Si el firewall se debe habilitar o no.</span><span class="sxs-lookup"><span data-stu-id="f81bf-202">Whether the firewall should be enabled or not.</span></span>|
|<span data-ttu-id="f81bf-203">firewallBlockAllIncoming</span><span class="sxs-lookup"><span data-stu-id="f81bf-203">firewallBlockAllIncoming</span></span>|<span data-ttu-id="f81bf-204">Booleano</span><span class="sxs-lookup"><span data-stu-id="f81bf-204">Boolean</span></span>|<span data-ttu-id="f81bf-205">Corresponde a la opción "Bloquear todas las conexiones entrantes".</span><span class="sxs-lookup"><span data-stu-id="f81bf-205">Corresponds to the “Block all incoming connections” option.</span></span>|
|<span data-ttu-id="f81bf-206">firewallEnableStealthMode</span><span class="sxs-lookup"><span data-stu-id="f81bf-206">firewallEnableStealthMode</span></span>|<span data-ttu-id="f81bf-207">Booleano</span><span class="sxs-lookup"><span data-stu-id="f81bf-207">Boolean</span></span>|<span data-ttu-id="f81bf-208">Corresponde a "Habilitar el modo sigiloso".</span><span class="sxs-lookup"><span data-stu-id="f81bf-208">Corresponds to “Enable stealth mode.”</span></span>|



## <a name="response"></a><span data-ttu-id="f81bf-209">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f81bf-209">Response</span></span>
<span data-ttu-id="f81bf-210">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [macOSCompliancePolicy](../resources/intune_deviceconfig_macoscompliancepolicy.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f81bf-210">If successful, this method returns a `200 OK` response code and an updated [macOSCompliancePolicy](../resources/intune_deviceconfig_macoscompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f81bf-211">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f81bf-211">Example</span></span>
### <a name="request"></a><span data-ttu-id="f81bf-212">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f81bf-212">Request</span></span>
<span data-ttu-id="f81bf-213">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f81bf-213">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
Content-type: application/json
Content-length: 853

{
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

### <a name="response"></a><span data-ttu-id="f81bf-214">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f81bf-214">Response</span></span>
<span data-ttu-id="f81bf-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f81bf-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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








