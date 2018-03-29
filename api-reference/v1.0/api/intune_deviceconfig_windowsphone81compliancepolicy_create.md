# <a name="create-windowsphone81compliancepolicy"></a><span data-ttu-id="d70e8-101">Crear windowsPhone81CompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="d70e8-101">Create windowsPhone81CompliancePolicy</span></span>

> <span data-ttu-id="d70e8-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d70e8-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d70e8-103">Cree un objeto [windowsPhone81CompliancePolicy](../resources/intune_deviceconfig_windowsphone81compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="d70e8-103">Create a new [plannerBucket](../resources/intune_deviceconfig_windowsphone81compliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d70e8-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d70e8-104">Prerequisites</span></span>
<span data-ttu-id="d70e8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d70e8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d70e8-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d70e8-107">Permission type</span></span>|<span data-ttu-id="d70e8-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d70e8-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d70e8-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d70e8-109">Delegated (work or school account)</span></span>|<span data-ttu-id="d70e8-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d70e8-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="d70e8-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d70e8-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d70e8-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d70e8-112">Not supported.</span></span>|
|<span data-ttu-id="d70e8-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d70e8-113">Application</span></span>|<span data-ttu-id="d70e8-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d70e8-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d70e8-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d70e8-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="d70e8-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d70e8-116">Request headers</span></span>
|<span data-ttu-id="d70e8-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d70e8-117">Header</span></span>|<span data-ttu-id="d70e8-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d70e8-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d70e8-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="d70e8-119">Authorization</span></span>|<span data-ttu-id="d70e8-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d70e8-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="d70e8-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d70e8-121">Accept</span></span>|<span data-ttu-id="d70e8-122">application/json</span><span class="sxs-lookup"><span data-stu-id="d70e8-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d70e8-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d70e8-123">Request body</span></span>
<span data-ttu-id="d70e8-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsPhone81CompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="d70e8-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="d70e8-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsPhone81CompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="d70e8-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="d70e8-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d70e8-126">Property</span></span>|<span data-ttu-id="d70e8-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="d70e8-127">Type</span></span>|<span data-ttu-id="d70e8-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="d70e8-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d70e8-129">id</span><span class="sxs-lookup"><span data-stu-id="d70e8-129">id</span></span>|<span data-ttu-id="d70e8-130">String</span><span class="sxs-lookup"><span data-stu-id="d70e8-130">String</span></span>|<span data-ttu-id="d70e8-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d70e8-131">Key of the setting.</span></span> <span data-ttu-id="d70e8-132">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="d70e8-132">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="d70e8-133">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="d70e8-133">createdDateTime</span></span>|<span data-ttu-id="d70e8-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d70e8-134">DateTimeOffset</span></span>|<span data-ttu-id="d70e8-135">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="d70e8-135">DateTime the object was created.</span></span> <span data-ttu-id="d70e8-136">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="d70e8-136">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="d70e8-137">description</span><span class="sxs-lookup"><span data-stu-id="d70e8-137">description</span></span>|<span data-ttu-id="d70e8-138">String</span><span class="sxs-lookup"><span data-stu-id="d70e8-138">String</span></span>|<span data-ttu-id="d70e8-139">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d70e8-139">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="d70e8-140">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="d70e8-140">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="d70e8-141">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="d70e8-141">lastModifiedDateTime</span></span>|<span data-ttu-id="d70e8-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d70e8-142">DateTimeOffset</span></span>|<span data-ttu-id="d70e8-143">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="d70e8-143">Indicates the date the object was last modified.</span></span> <span data-ttu-id="d70e8-144">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="d70e8-144">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="d70e8-145">displayName</span><span class="sxs-lookup"><span data-stu-id="d70e8-145">displayName</span></span>|<span data-ttu-id="d70e8-146">String</span><span class="sxs-lookup"><span data-stu-id="d70e8-146">String</span></span>|<span data-ttu-id="d70e8-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d70e8-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="d70e8-148">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="d70e8-148">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="d70e8-149">version</span><span class="sxs-lookup"><span data-stu-id="d70e8-149">version</span></span>|<span data-ttu-id="d70e8-150">Int32</span><span class="sxs-lookup"><span data-stu-id="d70e8-150">Int32</span></span>|<span data-ttu-id="d70e8-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d70e8-151">Version of the device configuration.</span></span> <span data-ttu-id="d70e8-152">Heredado de [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="d70e8-152">Inherited from [deviceCompliancePolicy](../resources/intune_deviceconfig_devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="d70e8-153">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="d70e8-153">passwordBlockSimple</span></span>|<span data-ttu-id="d70e8-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="d70e8-154">Boolean</span></span>|<span data-ttu-id="d70e8-155">Si quiere bloquear o no la sincronización del calendario.</span><span class="sxs-lookup"><span data-stu-id="d70e8-155">Whether or not to block syncing the calendar.</span></span>|
|<span data-ttu-id="d70e8-156">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="d70e8-156">passwordExpirationDays</span></span>|<span data-ttu-id="d70e8-157">Int32</span><span class="sxs-lookup"><span data-stu-id="d70e8-157">Int32</span></span>|<span data-ttu-id="d70e8-158">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="d70e8-158">Number of days before the password expires.</span></span>|
|<span data-ttu-id="d70e8-159">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="d70e8-159">passwordMinimumLength</span></span>|<span data-ttu-id="d70e8-160">Int32</span><span class="sxs-lookup"><span data-stu-id="d70e8-160">Int32</span></span>|<span data-ttu-id="d70e8-161">Longitud mínima de las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="d70e8-161">Minimum length of passwords.</span></span>|
|<span data-ttu-id="d70e8-162">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="d70e8-162">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="d70e8-163">Int32</span><span class="sxs-lookup"><span data-stu-id="d70e8-163">Int32</span></span>|<span data-ttu-id="d70e8-164">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="d70e8-164">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="d70e8-165">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="d70e8-165">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="d70e8-166">Int32</span><span class="sxs-lookup"><span data-stu-id="d70e8-166">Int32</span></span>|<span data-ttu-id="d70e8-167">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="d70e8-167">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="d70e8-168">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="d70e8-168">passwordRequiredType</span></span>|<span data-ttu-id="d70e8-169">String</span><span class="sxs-lookup"><span data-stu-id="d70e8-169">String</span></span>|<span data-ttu-id="d70e8-170">Tipo de contraseña necesaria.</span><span class="sxs-lookup"><span data-stu-id="d70e8-170">The required password type.</span></span> <span data-ttu-id="d70e8-171">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="d70e8-171">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="d70e8-172">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="d70e8-172">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="d70e8-173">Int32</span><span class="sxs-lookup"><span data-stu-id="d70e8-173">Int32</span></span>|<span data-ttu-id="d70e8-174">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="d70e8-174">Number of previous passwords to block.</span></span> <span data-ttu-id="d70e8-175">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="d70e8-175">Valid values 0 to 24</span></span>|
|<span data-ttu-id="d70e8-176">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="d70e8-176">passwordRequired</span></span>|<span data-ttu-id="d70e8-177">Booleano</span><span class="sxs-lookup"><span data-stu-id="d70e8-177">Boolean</span></span>|<span data-ttu-id="d70e8-178">Si quiere requerir o no una contraseña.</span><span class="sxs-lookup"><span data-stu-id="d70e8-178">Whether or not to require a password.</span></span>|
|<span data-ttu-id="d70e8-179">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="d70e8-179">osMinimumVersion</span></span>|<span data-ttu-id="d70e8-180">String</span><span class="sxs-lookup"><span data-stu-id="d70e8-180">String</span></span>|<span data-ttu-id="d70e8-181">Versión mínima de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="d70e8-181">Minimum Windows Phone version.</span></span>|
|<span data-ttu-id="d70e8-182">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="d70e8-182">osMaximumVersion</span></span>|<span data-ttu-id="d70e8-183">String</span><span class="sxs-lookup"><span data-stu-id="d70e8-183">String</span></span>|<span data-ttu-id="d70e8-184">Versión máxima de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="d70e8-184">Maximum Windows Phone version.</span></span>|
|<span data-ttu-id="d70e8-185">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="d70e8-185">storageRequireEncryption</span></span>|<span data-ttu-id="d70e8-186">Booleano</span><span class="sxs-lookup"><span data-stu-id="d70e8-186">Boolean</span></span>|<span data-ttu-id="d70e8-187">Requerir el cifrado en dispositivos de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="d70e8-187">Require encryption on windows phone devices.</span></span>|



## <a name="response"></a><span data-ttu-id="d70e8-188">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d70e8-188">Response</span></span>
<span data-ttu-id="d70e8-189">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsPhone81CompliancePolicy](../resources/intune_deviceconfig_windowsphone81compliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d70e8-189">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_deviceconfig_windowsphone81compliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d70e8-190">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d70e8-190">Example</span></span>
### <a name="request"></a><span data-ttu-id="d70e8-191">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d70e8-191">Request</span></span>
<span data-ttu-id="d70e8-192">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d70e8-192">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies
Content-type: application/json
Content-length: 671

{
  "@odata.type": "#microsoft.graph.windowsPhone81CompliancePolicy",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "passwordBlockSimple": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordMinimumCharacterSetCount": 0,
  "passwordRequiredType": "alphanumeric",
  "passwordPreviousPasswordBlockCount": 2,
  "passwordRequired": true,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "storageRequireEncryption": true
}
```

### <a name="response"></a><span data-ttu-id="d70e8-193">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d70e8-193">Response</span></span>
<span data-ttu-id="d70e8-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d70e8-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 779

{
  "@odata.type": "#microsoft.graph.windowsPhone81CompliancePolicy",
  "id": "e6021ad4-1ad4-e602-d41a-02e6d41a02e6",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "passwordBlockSimple": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordMinimumCharacterSetCount": 0,
  "passwordRequiredType": "alphanumeric",
  "passwordPreviousPasswordBlockCount": 2,
  "passwordRequired": true,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "storageRequireEncryption": true
}
```



