# <a name="create-windows81compliancepolicy"></a><span data-ttu-id="e244c-101">Crear windows81CompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="e244c-101">Create windows81CompliancePolicy</span></span>

> <span data-ttu-id="e244c-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e244c-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e244c-103">Cree un objeto [windows81CompliancePolicy](../resources/intune_deviceconfig_windows81compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="e244c-103">Create a new [plannerBucket](../resources/intune_deviceconfig_windows81compliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e244c-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e244c-104">Prerequisites</span></span>
<span data-ttu-id="e244c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e244c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e244c-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e244c-107">Permission type</span></span>|<span data-ttu-id="e244c-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e244c-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e244c-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e244c-109">Delegated (work or school account)</span></span>|<span data-ttu-id="e244c-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e244c-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="e244c-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e244c-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e244c-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e244c-112">Not supported.</span></span>|
|<span data-ttu-id="e244c-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e244c-113">Application</span></span>|<span data-ttu-id="e244c-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e244c-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e244c-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e244c-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="e244c-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e244c-116">Request headers</span></span>
|<span data-ttu-id="e244c-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e244c-117">Header</span></span>|<span data-ttu-id="e244c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e244c-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e244c-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="e244c-119">Authorization</span></span>|<span data-ttu-id="e244c-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e244c-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="e244c-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e244c-121">Accept</span></span>|<span data-ttu-id="e244c-122">application/json</span><span class="sxs-lookup"><span data-stu-id="e244c-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e244c-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e244c-123">Request body</span></span>
<span data-ttu-id="e244c-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto windows81CompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="e244c-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="e244c-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windows81CompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="e244c-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="e244c-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e244c-126">Property</span></span>|<span data-ttu-id="e244c-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="e244c-127">Type</span></span>|<span data-ttu-id="e244c-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="e244c-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e244c-129">id</span><span class="sxs-lookup"><span data-stu-id="e244c-129">id</span></span>|<span data-ttu-id="e244c-130">String</span><span class="sxs-lookup"><span data-stu-id="e244c-130">String</span></span>|<span data-ttu-id="e244c-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e244c-131">Key of the setting.</span></span> <span data-ttu-id="e244c-132">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="e244c-132">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="e244c-133">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="e244c-133">createdDateTime</span></span>|<span data-ttu-id="e244c-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e244c-134">DateTimeOffset</span></span>|<span data-ttu-id="e244c-135">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="e244c-135">DateTime the object was created.</span></span> <span data-ttu-id="e244c-136">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="e244c-136">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="e244c-137">description</span><span class="sxs-lookup"><span data-stu-id="e244c-137">description</span></span>|<span data-ttu-id="e244c-138">String</span><span class="sxs-lookup"><span data-stu-id="e244c-138">String</span></span>|<span data-ttu-id="e244c-139">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e244c-139">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="e244c-140">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="e244c-140">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="e244c-141">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="e244c-141">lastModifiedDateTime</span></span>|<span data-ttu-id="e244c-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e244c-142">DateTimeOffset</span></span>|<span data-ttu-id="e244c-143">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="e244c-143">Indicates the date the object was last modified.</span></span> <span data-ttu-id="e244c-144">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="e244c-144">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="e244c-145">displayName</span><span class="sxs-lookup"><span data-stu-id="e244c-145">displayName</span></span>|<span data-ttu-id="e244c-146">String</span><span class="sxs-lookup"><span data-stu-id="e244c-146">String</span></span>|<span data-ttu-id="e244c-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e244c-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="e244c-148">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="e244c-148">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="e244c-149">version</span><span class="sxs-lookup"><span data-stu-id="e244c-149">version</span></span>|<span data-ttu-id="e244c-150">Int32</span><span class="sxs-lookup"><span data-stu-id="e244c-150">Int32</span></span>|<span data-ttu-id="e244c-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e244c-151">Version of the device configuration.</span></span> <span data-ttu-id="e244c-152">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="e244c-152">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="e244c-153">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="e244c-153">passwordRequired</span></span>|<span data-ttu-id="e244c-154">Boolean</span><span class="sxs-lookup"><span data-stu-id="e244c-154">Boolean</span></span>|<span data-ttu-id="e244c-155">Exige una contraseña para desbloquear el dispositivo Windows.</span><span class="sxs-lookup"><span data-stu-id="e244c-155">Require a password to unlock Windows device.</span></span>|
|<span data-ttu-id="e244c-156">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="e244c-156">passwordBlockSimple</span></span>|<span data-ttu-id="e244c-157">Boolean</span><span class="sxs-lookup"><span data-stu-id="e244c-157">Boolean</span></span>|<span data-ttu-id="e244c-158">Indica si quiere bloquear o no la contraseña simple.</span><span class="sxs-lookup"><span data-stu-id="e244c-158">Indicates whether or not to block simple password.</span></span>|
|<span data-ttu-id="e244c-159">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="e244c-159">passwordExpirationDays</span></span>|<span data-ttu-id="e244c-160">Int32</span><span class="sxs-lookup"><span data-stu-id="e244c-160">Int32</span></span>|<span data-ttu-id="e244c-161">Expiración de la contraseña en días.</span><span class="sxs-lookup"><span data-stu-id="e244c-161">Password expiration in days.</span></span>|
|<span data-ttu-id="e244c-162">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="e244c-162">passwordMinimumLength</span></span>|<span data-ttu-id="e244c-163">Int32</span><span class="sxs-lookup"><span data-stu-id="e244c-163">Int32</span></span>|<span data-ttu-id="e244c-164">La longitud mínima de contraseña.</span><span class="sxs-lookup"><span data-stu-id="e244c-164">The minimum password length.</span></span>|
|<span data-ttu-id="e244c-165">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="e244c-165">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="e244c-166">Int32</span><span class="sxs-lookup"><span data-stu-id="e244c-166">Int32</span></span>|<span data-ttu-id="e244c-167">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="e244c-167">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="e244c-168">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="e244c-168">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="e244c-169">Int32</span><span class="sxs-lookup"><span data-stu-id="e244c-169">Int32</span></span>|<span data-ttu-id="e244c-170">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="e244c-170">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="e244c-171">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="e244c-171">passwordRequiredType</span></span>|<span data-ttu-id="e244c-172">String</span><span class="sxs-lookup"><span data-stu-id="e244c-172">String</span></span>|<span data-ttu-id="e244c-173">Tipo de contraseña necesaria.</span><span class="sxs-lookup"><span data-stu-id="e244c-173">The required password type.</span></span> <span data-ttu-id="e244c-174">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="e244c-174">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="e244c-175">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="e244c-175">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="e244c-176">Int32</span><span class="sxs-lookup"><span data-stu-id="e244c-176">Int32</span></span>|<span data-ttu-id="e244c-177">Número de contraseñas anteriores que impide su reutilización.</span><span class="sxs-lookup"><span data-stu-id="e244c-177">The number of previous passwords to prevent re-use of.</span></span> <span data-ttu-id="e244c-178">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="e244c-178">Valid values 0 to 24</span></span>|
|<span data-ttu-id="e244c-179">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="e244c-179">osMinimumVersion</span></span>|<span data-ttu-id="e244c-180">String</span><span class="sxs-lookup"><span data-stu-id="e244c-180">String</span></span>|<span data-ttu-id="e244c-181">Versión mínima de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="e244c-181">Minimum Windows 8.1 version.</span></span>|
|<span data-ttu-id="e244c-182">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="e244c-182">osMaximumVersion</span></span>|<span data-ttu-id="e244c-183">String</span><span class="sxs-lookup"><span data-stu-id="e244c-183">String</span></span>|<span data-ttu-id="e244c-184">Versión máxima de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="e244c-184">Maximum Windows 8.1 version.</span></span>|
|<span data-ttu-id="e244c-185">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="e244c-185">storageRequireEncryption</span></span>|<span data-ttu-id="e244c-186">Boolean</span><span class="sxs-lookup"><span data-stu-id="e244c-186">Boolean</span></span>|<span data-ttu-id="e244c-187">Indica si quiere requerir o no el cifrado en un dispositivo Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="e244c-187">Indicates whether or not to require encryption on a windows 8.1 device.</span></span>|



## <a name="response"></a><span data-ttu-id="e244c-188">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e244c-188">Response</span></span>
<span data-ttu-id="e244c-189">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windows81CompliancePolicy](../resources/intune_deviceconfig_windows81compliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e244c-189">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_deviceconfig_windows81compliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e244c-190">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e244c-190">Example</span></span>
### <a name="request"></a><span data-ttu-id="e244c-191">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e244c-191">Request</span></span>
<span data-ttu-id="e244c-192">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e244c-192">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies
Content-type: application/json
Content-length: 666

{
  "@odata.type": "#microsoft.graph.windows81CompliancePolicy",
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

### <a name="response"></a><span data-ttu-id="e244c-193">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e244c-193">Response</span></span>
<span data-ttu-id="e244c-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e244c-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



