# <a name="create-macoscompliancepolicy"></a><span data-ttu-id="56fbe-101">Crear macOSCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="56fbe-101">Create macOSCompliancePolicy</span></span>

> <span data-ttu-id="56fbe-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="56fbe-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="56fbe-103">Cree un objeto [macOSCompliancePolicy](../resources/intune_deviceconfig_macoscompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="56fbe-103">Create a new [plannerBucket](../resources/intune_deviceconfig_macoscompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="56fbe-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="56fbe-104">Prerequisites</span></span>
<span data-ttu-id="56fbe-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="56fbe-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="56fbe-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="56fbe-107">Permission type</span></span>|<span data-ttu-id="56fbe-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="56fbe-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="56fbe-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="56fbe-109">Delegated (work or school account)</span></span>|<span data-ttu-id="56fbe-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="56fbe-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="56fbe-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="56fbe-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="56fbe-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="56fbe-112">Not supported.</span></span>|
|<span data-ttu-id="56fbe-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="56fbe-113">Application</span></span>|<span data-ttu-id="56fbe-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="56fbe-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="56fbe-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="56fbe-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="56fbe-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="56fbe-116">Request headers</span></span>
|<span data-ttu-id="56fbe-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56fbe-117">Header</span></span>|<span data-ttu-id="56fbe-118">Valor</span><span class="sxs-lookup"><span data-stu-id="56fbe-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="56fbe-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="56fbe-119">Authorization</span></span>|<span data-ttu-id="56fbe-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="56fbe-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="56fbe-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="56fbe-121">Accept</span></span>|<span data-ttu-id="56fbe-122">application/json</span><span class="sxs-lookup"><span data-stu-id="56fbe-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="56fbe-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="56fbe-123">Request body</span></span>
<span data-ttu-id="56fbe-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto macOSCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="56fbe-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="56fbe-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto macOSCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="56fbe-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="56fbe-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="56fbe-126">Property</span></span>|<span data-ttu-id="56fbe-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="56fbe-127">Type</span></span>|<span data-ttu-id="56fbe-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="56fbe-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="56fbe-129">id</span><span class="sxs-lookup"><span data-stu-id="56fbe-129">id</span></span>|<span data-ttu-id="56fbe-130">String</span><span class="sxs-lookup"><span data-stu-id="56fbe-130">String</span></span>|<span data-ttu-id="56fbe-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="56fbe-131">Key of the setting.</span></span> <span data-ttu-id="56fbe-132">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="56fbe-132">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="56fbe-133">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="56fbe-133">createdDateTime</span></span>|<span data-ttu-id="56fbe-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="56fbe-134">DateTimeOffset</span></span>|<span data-ttu-id="56fbe-135">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="56fbe-135">DateTime the object was created.</span></span> <span data-ttu-id="56fbe-136">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="56fbe-136">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="56fbe-137">description</span><span class="sxs-lookup"><span data-stu-id="56fbe-137">description</span></span>|<span data-ttu-id="56fbe-138">String</span><span class="sxs-lookup"><span data-stu-id="56fbe-138">String</span></span>|<span data-ttu-id="56fbe-139">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56fbe-139">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="56fbe-140">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="56fbe-140">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="56fbe-141">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="56fbe-141">lastModifiedDateTime</span></span>|<span data-ttu-id="56fbe-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="56fbe-142">DateTimeOffset</span></span>|<span data-ttu-id="56fbe-143">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="56fbe-143">Indicates the date the object was last modified.</span></span> <span data-ttu-id="56fbe-144">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="56fbe-144">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="56fbe-145">displayName</span><span class="sxs-lookup"><span data-stu-id="56fbe-145">displayName</span></span>|<span data-ttu-id="56fbe-146">String</span><span class="sxs-lookup"><span data-stu-id="56fbe-146">String</span></span>|<span data-ttu-id="56fbe-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56fbe-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="56fbe-148">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="56fbe-148">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="56fbe-149">version</span><span class="sxs-lookup"><span data-stu-id="56fbe-149">version</span></span>|<span data-ttu-id="56fbe-150">Int32</span><span class="sxs-lookup"><span data-stu-id="56fbe-150">Int32</span></span>|<span data-ttu-id="56fbe-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56fbe-151">Version of the device configuration.</span></span> <span data-ttu-id="56fbe-152">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="56fbe-152">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="56fbe-153">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="56fbe-153">passwordRequired</span></span>|<span data-ttu-id="56fbe-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="56fbe-154">Boolean</span></span>|<span data-ttu-id="56fbe-155">Si quiere requerir o no una contraseña.</span><span class="sxs-lookup"><span data-stu-id="56fbe-155">Whether or not to require a password.</span></span>|
|<span data-ttu-id="56fbe-156">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="56fbe-156">passwordBlockSimple</span></span>|<span data-ttu-id="56fbe-157">Booleano</span><span class="sxs-lookup"><span data-stu-id="56fbe-157">Boolean</span></span>|<span data-ttu-id="56fbe-158">Indica si se van a bloquear las contraseñas simples.</span><span class="sxs-lookup"><span data-stu-id="56fbe-158">Indicates whether or not to block simple passwords.</span></span>|
|<span data-ttu-id="56fbe-159">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="56fbe-159">passwordExpirationDays</span></span>|<span data-ttu-id="56fbe-160">Int32</span><span class="sxs-lookup"><span data-stu-id="56fbe-160">Int32</span></span>|<span data-ttu-id="56fbe-161">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="56fbe-161">Number of days before the password expires.</span></span> <span data-ttu-id="56fbe-162">Valores válidos de 1 a 65535</span><span class="sxs-lookup"><span data-stu-id="56fbe-162">Valid values 1 to 65535</span></span>|
|<span data-ttu-id="56fbe-163">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="56fbe-163">passwordMinimumLength</span></span>|<span data-ttu-id="56fbe-164">Int32</span><span class="sxs-lookup"><span data-stu-id="56fbe-164">Int32</span></span>|<span data-ttu-id="56fbe-165">Longitud mínima de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="56fbe-165">Minimum length of password.</span></span> <span data-ttu-id="56fbe-166">Valores válidos de 4 a 14</span><span class="sxs-lookup"><span data-stu-id="56fbe-166">Valid values 4 to 14</span></span>|
|<span data-ttu-id="56fbe-167">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="56fbe-167">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="56fbe-168">Int32</span><span class="sxs-lookup"><span data-stu-id="56fbe-168">Int32</span></span>|<span data-ttu-id="56fbe-169">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="56fbe-169">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="56fbe-170">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="56fbe-170">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="56fbe-171">Int32</span><span class="sxs-lookup"><span data-stu-id="56fbe-171">Int32</span></span>|<span data-ttu-id="56fbe-172">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="56fbe-172">Number of previous passwords to block.</span></span> <span data-ttu-id="56fbe-173">Valores válidos de 1 a 24.</span><span class="sxs-lookup"><span data-stu-id="56fbe-173">Valid values 1 to 24</span></span>|
|<span data-ttu-id="56fbe-174">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="56fbe-174">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="56fbe-175">Int32</span><span class="sxs-lookup"><span data-stu-id="56fbe-175">Int32</span></span>|<span data-ttu-id="56fbe-176">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="56fbe-176">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="56fbe-177">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="56fbe-177">passwordRequiredType</span></span>|<span data-ttu-id="56fbe-178">String</span><span class="sxs-lookup"><span data-stu-id="56fbe-178">String</span></span>|<span data-ttu-id="56fbe-179">Tipo de contraseña necesaria.</span><span class="sxs-lookup"><span data-stu-id="56fbe-179">The required password type.</span></span> <span data-ttu-id="56fbe-180">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="56fbe-180">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="56fbe-181">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="56fbe-181">osMinimumVersion</span></span>|<span data-ttu-id="56fbe-182">String</span><span class="sxs-lookup"><span data-stu-id="56fbe-182">String</span></span>|<span data-ttu-id="56fbe-183">Versión mínima de iOS.</span><span class="sxs-lookup"><span data-stu-id="56fbe-183">Minimum IOS version.</span></span>|
|<span data-ttu-id="56fbe-184">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="56fbe-184">osMaximumVersion</span></span>|<span data-ttu-id="56fbe-185">String</span><span class="sxs-lookup"><span data-stu-id="56fbe-185">String</span></span>|<span data-ttu-id="56fbe-186">Versión máxima de iOS.</span><span class="sxs-lookup"><span data-stu-id="56fbe-186">Maximum IOS version.</span></span>|
|<span data-ttu-id="56fbe-187">systemIntegrityProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="56fbe-187">systemIntegrityProtectionEnabled</span></span>|<span data-ttu-id="56fbe-188">Booleano</span><span class="sxs-lookup"><span data-stu-id="56fbe-188">Boolean</span></span>|<span data-ttu-id="56fbe-189">Requiere que los dispositivos hayan habilitado la protección de integridad del sistema.</span><span class="sxs-lookup"><span data-stu-id="56fbe-189">Require that devices have enabled system integrity protection.</span></span>|
|<span data-ttu-id="56fbe-190">deviceThreatProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="56fbe-190">deviceThreatProtectionEnabled</span></span>|<span data-ttu-id="56fbe-191">Booleano</span><span class="sxs-lookup"><span data-stu-id="56fbe-191">Boolean</span></span>|<span data-ttu-id="56fbe-192">Requiere que los dispositivos hayan habilitado la protección contra amenazas de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56fbe-192">Require that devices have enabled device threat protection .</span></span>|
|<span data-ttu-id="56fbe-193">deviceThreatProtectionRequiredSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="56fbe-193">deviceThreatProtectionRequiredSecurityLevel</span></span>|<span data-ttu-id="56fbe-194">String</span><span class="sxs-lookup"><span data-stu-id="56fbe-194">String</span></span>|<span data-ttu-id="56fbe-195">Exigir que el nivel de riesgo mínimo de Mobile Threat Protection informe del no cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="56fbe-195">Require Mobile Threat Protection minimum risk level to report noncompliance.</span></span> <span data-ttu-id="56fbe-196">Los valores posibles son: `unavailable`, `secured`, `low`, `medium`, `high` y `notSet`.</span><span class="sxs-lookup"><span data-stu-id="56fbe-196">Possible values are: `unavailable`, `secured`, `low`, `medium`, `high`, `notSet`.</span></span>|
|<span data-ttu-id="56fbe-197">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="56fbe-197">storageRequireEncryption</span></span>|<span data-ttu-id="56fbe-198">Booleano</span><span class="sxs-lookup"><span data-stu-id="56fbe-198">Boolean</span></span>|<span data-ttu-id="56fbe-199">Exige el cifrado en dispositivos Mac OS.</span><span class="sxs-lookup"><span data-stu-id="56fbe-199">Require encryption on Mac OS devices.</span></span>|



## <a name="response"></a><span data-ttu-id="56fbe-200">Respuesta</span><span class="sxs-lookup"><span data-stu-id="56fbe-200">Response</span></span>
<span data-ttu-id="56fbe-201">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [macOSCompliancePolicy](../resources/intune_deviceconfig_macoscompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="56fbe-201">If successful, this method returns a `201 Created` response code and a [DriveItemVersion](../resources/intune_deviceconfig_macoscompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="56fbe-202">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="56fbe-202">Example</span></span>
### <a name="request"></a><span data-ttu-id="56fbe-203">Solicitud</span><span class="sxs-lookup"><span data-stu-id="56fbe-203">Request</span></span>
<span data-ttu-id="56fbe-204">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="56fbe-204">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies
Content-type: application/json
Content-length: 810

{
  "@odata.type": "#microsoft.graph.macOSCompliancePolicy",
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
  "storageRequireEncryption": true
}
```

### <a name="response"></a><span data-ttu-id="56fbe-205">Respuesta</span><span class="sxs-lookup"><span data-stu-id="56fbe-205">Response</span></span>
<span data-ttu-id="56fbe-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="56fbe-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 918

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
  "storageRequireEncryption": true
}
```



