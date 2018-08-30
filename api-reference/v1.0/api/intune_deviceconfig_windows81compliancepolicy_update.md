# <a name="update-windows81compliancepolicy"></a><span data-ttu-id="59155-101">Actualizar windows81CompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="59155-101">Update windows81CompliancePolicy</span></span>

> <span data-ttu-id="59155-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="59155-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="59155-103">Actualice las propiedades de un objeto [windows81CompliancePolicy](../resources/intune_deviceconfig_windows81compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="59155-103">Update the properties of a [windows81CompliancePolicy](../resources/intune_deviceconfig_windows81compliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="59155-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="59155-104">Prerequisites</span></span>
<span data-ttu-id="59155-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="59155-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="59155-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="59155-107">Permission type</span></span>|<span data-ttu-id="59155-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="59155-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="59155-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="59155-109">Delegated (work or school account)</span></span>|<span data-ttu-id="59155-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="59155-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="59155-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="59155-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="59155-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="59155-112">Not supported.</span></span>|
|<span data-ttu-id="59155-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="59155-113">Application</span></span>|<span data-ttu-id="59155-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="59155-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="59155-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="59155-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="request-headers"></a><span data-ttu-id="59155-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="59155-116">Request headers</span></span>
|<span data-ttu-id="59155-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59155-117">Header</span></span>|<span data-ttu-id="59155-118">Valor</span><span class="sxs-lookup"><span data-stu-id="59155-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="59155-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="59155-119">Authorization</span></span>|<span data-ttu-id="59155-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="59155-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="59155-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="59155-121">Accept</span></span>|<span data-ttu-id="59155-122">application/json</span><span class="sxs-lookup"><span data-stu-id="59155-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="59155-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="59155-123">Request body</span></span>
<span data-ttu-id="59155-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windows81CompliancePolicy](../resources/intune_deviceconfig_windows81compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="59155-124">In the request body, supply a JSON representation for the [windows81CompliancePolicy](../resources/intune_deviceconfig_windows81compliancepolicy.md) object.</span></span>

<span data-ttu-id="59155-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windows81CompliancePolicy](../resources/intune_deviceconfig_windows81compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="59155-125">The following table shows the properties that are required when you create the [windows81CompliancePolicy](../resources/intune_deviceconfig_windows81compliancepolicy.md).</span></span>

|<span data-ttu-id="59155-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="59155-126">Property</span></span>|<span data-ttu-id="59155-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="59155-127">Type</span></span>|<span data-ttu-id="59155-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="59155-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="59155-129">id</span><span class="sxs-lookup"><span data-stu-id="59155-129">id</span></span>|<span data-ttu-id="59155-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="59155-130">String</span></span>|<span data-ttu-id="59155-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="59155-131">Key of the entity.</span></span> <span data-ttu-id="59155-132">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="59155-132">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="59155-133">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="59155-133">createdDateTime</span></span>|<span data-ttu-id="59155-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="59155-134">DateTimeOffset</span></span>|<span data-ttu-id="59155-135">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="59155-135">DateTime the object was created.</span></span> <span data-ttu-id="59155-136">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="59155-136">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="59155-137">descripción</span><span class="sxs-lookup"><span data-stu-id="59155-137">description</span></span>|<span data-ttu-id="59155-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="59155-138">String</span></span>|<span data-ttu-id="59155-139">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="59155-139">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="59155-140">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="59155-140">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="59155-141">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="59155-141">lastModifiedDateTime</span></span>|<span data-ttu-id="59155-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="59155-142">DateTimeOffset</span></span>|<span data-ttu-id="59155-143">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="59155-143">DateTime the object was last modified.</span></span> <span data-ttu-id="59155-144">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="59155-144">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="59155-145">displayName</span><span class="sxs-lookup"><span data-stu-id="59155-145">displayName</span></span>|<span data-ttu-id="59155-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="59155-146">String</span></span>|<span data-ttu-id="59155-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="59155-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="59155-148">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="59155-148">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="59155-149">version</span><span class="sxs-lookup"><span data-stu-id="59155-149">version</span></span>|<span data-ttu-id="59155-150">Int32</span><span class="sxs-lookup"><span data-stu-id="59155-150">Int32</span></span>|<span data-ttu-id="59155-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="59155-151">Version of the device configuration.</span></span> <span data-ttu-id="59155-152">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="59155-152">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="59155-153">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="59155-153">passwordRequired</span></span>|<span data-ttu-id="59155-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="59155-154">Boolean</span></span>|<span data-ttu-id="59155-155">Exige una contraseña para desbloquear el dispositivo Windows.</span><span class="sxs-lookup"><span data-stu-id="59155-155">Require a password to unlock Windows device.</span></span>|
|<span data-ttu-id="59155-156">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="59155-156">passwordBlockSimple</span></span>|<span data-ttu-id="59155-157">Booleano</span><span class="sxs-lookup"><span data-stu-id="59155-157">Boolean</span></span>|<span data-ttu-id="59155-158">Indica si quiere bloquear o no la contraseña simple.</span><span class="sxs-lookup"><span data-stu-id="59155-158">Indicates whether or not to block simple password.</span></span>|
|<span data-ttu-id="59155-159">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="59155-159">passwordExpirationDays</span></span>|<span data-ttu-id="59155-160">Int32</span><span class="sxs-lookup"><span data-stu-id="59155-160">Int32</span></span>|<span data-ttu-id="59155-161">Expiración de la contraseña en días.</span><span class="sxs-lookup"><span data-stu-id="59155-161">Password expiration in days.</span></span>|
|<span data-ttu-id="59155-162">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="59155-162">passwordMinimumLength</span></span>|<span data-ttu-id="59155-163">Int32</span><span class="sxs-lookup"><span data-stu-id="59155-163">Int32</span></span>|<span data-ttu-id="59155-164">La longitud mínima de contraseña.</span><span class="sxs-lookup"><span data-stu-id="59155-164">The minimum password length.</span></span>|
|<span data-ttu-id="59155-165">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="59155-165">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="59155-166">Int32</span><span class="sxs-lookup"><span data-stu-id="59155-166">Int32</span></span>|<span data-ttu-id="59155-167">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="59155-167">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="59155-168">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="59155-168">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="59155-169">Int32</span><span class="sxs-lookup"><span data-stu-id="59155-169">Int32</span></span>|<span data-ttu-id="59155-170">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="59155-170">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="59155-171">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="59155-171">passwordRequiredType</span></span>|[<span data-ttu-id="59155-172">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="59155-172">requiredPasswordType</span></span>](../resources/intune_deviceconfig_requiredpasswordtype.md)|<span data-ttu-id="59155-173">Tipo de contraseña necesaria.</span><span class="sxs-lookup"><span data-stu-id="59155-173">The required password type.</span></span> <span data-ttu-id="59155-174">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="59155-174">The possible values are `deviceDefault`, `alphanumeric`, `numeric`, , , , , , , , , or .</span></span>|
|<span data-ttu-id="59155-175">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="59155-175">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="59155-176">Int32</span><span class="sxs-lookup"><span data-stu-id="59155-176">Int32</span></span>|<span data-ttu-id="59155-177">Número de contraseñas anteriores que impide su reutilización.</span><span class="sxs-lookup"><span data-stu-id="59155-177">The number of previous passwords to prevent re-use of.</span></span> <span data-ttu-id="59155-178">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="59155-178">Valid values 0 to 24</span></span>|
|<span data-ttu-id="59155-179">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="59155-179">osMinimumVersion</span></span>|<span data-ttu-id="59155-180">Cadena</span><span class="sxs-lookup"><span data-stu-id="59155-180">String</span></span>|<span data-ttu-id="59155-181">Versión mínima de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="59155-181">Minimum Windows 8.1 version.</span></span>|
|<span data-ttu-id="59155-182">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="59155-182">osMaximumVersion</span></span>|<span data-ttu-id="59155-183">Cadena</span><span class="sxs-lookup"><span data-stu-id="59155-183">String</span></span>|<span data-ttu-id="59155-184">Versión máxima de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="59155-184">Maximum Windows 8.1 version.</span></span>|
|<span data-ttu-id="59155-185">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="59155-185">storageRequireEncryption</span></span>|<span data-ttu-id="59155-186">Booleano</span><span class="sxs-lookup"><span data-stu-id="59155-186">Boolean</span></span>|<span data-ttu-id="59155-187">Indica si quiere requerir o no el cifrado en un dispositivo Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="59155-187">Indicates whether or not to require encryption on a windows 8.1 device.</span></span>|



## <a name="response"></a><span data-ttu-id="59155-188">Respuesta</span><span class="sxs-lookup"><span data-stu-id="59155-188">Response</span></span>
<span data-ttu-id="59155-189">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows81CompliancePolicy](../resources/intune_deviceconfig_windows81compliancepolicy.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="59155-189">If successful, this method returns a `200 OK` response code and an updated [windows81CompliancePolicy](../resources/intune_deviceconfig_windows81compliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="59155-190">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="59155-190">Example</span></span>
### <a name="request"></a><span data-ttu-id="59155-191">Solicitud</span><span class="sxs-lookup"><span data-stu-id="59155-191">Request</span></span>
<span data-ttu-id="59155-192">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="59155-192">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
Content-type: application/json
Content-length: 602

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
  "passwordMinimumCharacterSetCount": 0,
  "passwordRequiredType": "alphanumeric",
  "passwordPreviousPasswordBlockCount": 2,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "storageRequireEncryption": true
}
```

### <a name="response"></a><span data-ttu-id="59155-193">Respuesta</span><span class="sxs-lookup"><span data-stu-id="59155-193">Response</span></span>
<span data-ttu-id="59155-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="59155-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 774

{
  "@odata.type": "#microsoft.graph.windows81CompliancePolicy",
  "id": "6bb4b7e0-b7e0-6bb4-e0b7-b46be0b7b46b",
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
  "passwordMinimumCharacterSetCount": 0,
  "passwordRequiredType": "alphanumeric",
  "passwordPreviousPasswordBlockCount": 2,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "storageRequireEncryption": true
}
```



