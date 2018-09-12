# <a name="create-macosgeneraldeviceconfiguration"></a><span data-ttu-id="270fe-101">Crear macOSGeneralDeviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="270fe-101">Create macOSGeneralDeviceConfiguration</span></span>

> <span data-ttu-id="270fe-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="270fe-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="270fe-103">Crear un objeto [macOSGeneralDeviceConfiguration](../resources/intune_deviceconfig_macosgeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="270fe-103">Create a new [macOSGeneralDeviceConfiguration](../resources/intune_deviceconfig_macosgeneraldeviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="270fe-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="270fe-104">Prerequisites</span></span>
<span data-ttu-id="270fe-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="270fe-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="270fe-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="270fe-107">Permission type</span></span>|<span data-ttu-id="270fe-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="270fe-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="270fe-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="270fe-109">Delegated (work or school account)</span></span>|<span data-ttu-id="270fe-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="270fe-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="270fe-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="270fe-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="270fe-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="270fe-112">Not supported.</span></span>|
|<span data-ttu-id="270fe-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="270fe-113">Application</span></span>|<span data-ttu-id="270fe-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="270fe-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="270fe-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="270fe-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="270fe-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="270fe-116">Request headers</span></span>
|<span data-ttu-id="270fe-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="270fe-117">Header</span></span>|<span data-ttu-id="270fe-118">Valor</span><span class="sxs-lookup"><span data-stu-id="270fe-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="270fe-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="270fe-119">Authorization</span></span>|<span data-ttu-id="270fe-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="270fe-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="270fe-121">Accept</span><span class="sxs-lookup"><span data-stu-id="270fe-121">Accept</span></span>|<span data-ttu-id="270fe-122">application/json</span><span class="sxs-lookup"><span data-stu-id="270fe-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="270fe-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="270fe-123">Request body</span></span>
<span data-ttu-id="270fe-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto macOSGeneralDeviceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="270fe-124">In the request body, supply a JSON representation for the macOSGeneralDeviceConfiguration object.</span></span>

<span data-ttu-id="270fe-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto macOSGeneralDeviceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="270fe-125">The following table shows the properties that are required when you create the macOSGeneralDeviceConfiguration.</span></span>

|<span data-ttu-id="270fe-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="270fe-126">Property</span></span>|<span data-ttu-id="270fe-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="270fe-127">Type</span></span>|<span data-ttu-id="270fe-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="270fe-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="270fe-129">id</span><span class="sxs-lookup"><span data-stu-id="270fe-129">id</span></span>|<span data-ttu-id="270fe-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="270fe-130">String</span></span>|<span data-ttu-id="270fe-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="270fe-131">Key of the entity.</span></span> <span data-ttu-id="270fe-132">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="270fe-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="270fe-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="270fe-133">lastModifiedDateTime</span></span>|<span data-ttu-id="270fe-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="270fe-134">DateTimeOffset</span></span>|<span data-ttu-id="270fe-135">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="270fe-135">DateTime the object was last modified.</span></span> <span data-ttu-id="270fe-136">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="270fe-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="270fe-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="270fe-137">createdDateTime</span></span>|<span data-ttu-id="270fe-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="270fe-138">DateTimeOffset</span></span>|<span data-ttu-id="270fe-139">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="270fe-139">DateTime the object was created.</span></span> <span data-ttu-id="270fe-140">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="270fe-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="270fe-141">description</span><span class="sxs-lookup"><span data-stu-id="270fe-141">description</span></span>|<span data-ttu-id="270fe-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="270fe-142">String</span></span>|<span data-ttu-id="270fe-143">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="270fe-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="270fe-144">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="270fe-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="270fe-145">displayName</span><span class="sxs-lookup"><span data-stu-id="270fe-145">displayName</span></span>|<span data-ttu-id="270fe-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="270fe-146">String</span></span>|<span data-ttu-id="270fe-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="270fe-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="270fe-148">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="270fe-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="270fe-149">version</span><span class="sxs-lookup"><span data-stu-id="270fe-149">version</span></span>|<span data-ttu-id="270fe-150">Int32</span><span class="sxs-lookup"><span data-stu-id="270fe-150">Int32</span></span>|<span data-ttu-id="270fe-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="270fe-151">Version of the device configuration.</span></span> <span data-ttu-id="270fe-152">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="270fe-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="270fe-153">compliantAppsList</span><span class="sxs-lookup"><span data-stu-id="270fe-153">compliantAppsList</span></span>|<span data-ttu-id="270fe-154">Colección [appListItem](../resources/intune_deviceconfig_applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="270fe-154">[appListItem](../resources/intune_deviceconfig_applistitem.md) collection</span></span>|<span data-ttu-id="270fe-155">Lista de aplicaciones en el cumplimiento (sea lista de permitidos o de bloqueados, controlado por CompliantAppListType).</span><span class="sxs-lookup"><span data-stu-id="270fe-155">List of apps in the compliance (either allow list or block list, controlled by CompliantAppListType).</span></span> <span data-ttu-id="270fe-156">Esta colección puede contener un máximo de 10 000 elementos.</span><span class="sxs-lookup"><span data-stu-id="270fe-156">This collection can contain a maximum of 10000 elements.</span></span>|
|<span data-ttu-id="270fe-157">compliantAppListType</span><span class="sxs-lookup"><span data-stu-id="270fe-157">compliantAppListType</span></span>|[<span data-ttu-id="270fe-158">appListType</span><span class="sxs-lookup"><span data-stu-id="270fe-158">appListType</span></span>](../resources/intune_deviceconfig_applisttype.md)|<span data-ttu-id="270fe-159">Lista que se encuentra en la CompliantAppsList.</span><span class="sxs-lookup"><span data-stu-id="270fe-159">List that is in the CompliantAppsList.</span></span> <span data-ttu-id="270fe-160">Los valores posibles son: `none`, `appsInListCompliant` y `appsNotInListCompliant`.</span><span class="sxs-lookup"><span data-stu-id="270fe-160">Possible values are: `none`, `appsInListCompliant`, `appsNotInListCompliant`.</span></span>|
|<span data-ttu-id="270fe-161">emailInDomainSuffixes</span><span class="sxs-lookup"><span data-stu-id="270fe-161">emailInDomainSuffixes</span></span>|<span data-ttu-id="270fe-162">Colección String</span><span class="sxs-lookup"><span data-stu-id="270fe-162">String collection</span></span>|<span data-ttu-id="270fe-163">Una dirección de correo electrónico que carezca de un sufijo que coincida con cualquiera de estas cadenas se considerará fuera de dominio.</span><span class="sxs-lookup"><span data-stu-id="270fe-163">An email address lacking a suffix that matches any of these strings will be considered out-of-domain.</span></span>|
|<span data-ttu-id="270fe-164">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="270fe-164">passwordBlockSimple</span></span>|<span data-ttu-id="270fe-165">Booleano</span><span class="sxs-lookup"><span data-stu-id="270fe-165">Boolean</span></span>|<span data-ttu-id="270fe-166">Bloquear contraseñas sencillas.</span><span class="sxs-lookup"><span data-stu-id="270fe-166">Block simple passwords.</span></span>|
|<span data-ttu-id="270fe-167">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="270fe-167">passwordExpirationDays</span></span>|<span data-ttu-id="270fe-168">Int32</span><span class="sxs-lookup"><span data-stu-id="270fe-168">Int32</span></span>|<span data-ttu-id="270fe-169">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="270fe-169">Number of days before the password expires.</span></span>|
|<span data-ttu-id="270fe-170">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="270fe-170">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="270fe-171">Int32</span><span class="sxs-lookup"><span data-stu-id="270fe-171">Int32</span></span>|<span data-ttu-id="270fe-172">Número de juegos de caracteres que debe contener una contraseña.</span><span class="sxs-lookup"><span data-stu-id="270fe-172">Number of character sets a password must contain.</span></span> <span data-ttu-id="270fe-173">Valores válidos de 0 a 4.</span><span class="sxs-lookup"><span data-stu-id="270fe-173">Valid values 0 to 4</span></span>|
|<span data-ttu-id="270fe-174">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="270fe-174">passwordMinimumLength</span></span>|<span data-ttu-id="270fe-175">Int32</span><span class="sxs-lookup"><span data-stu-id="270fe-175">Int32</span></span>|<span data-ttu-id="270fe-176">Longitud mínima de las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="270fe-176">Minimum length of passwords.</span></span>|
|<span data-ttu-id="270fe-177">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="270fe-177">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="270fe-178">Int32</span><span class="sxs-lookup"><span data-stu-id="270fe-178">Int32</span></span>|<span data-ttu-id="270fe-179">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="270fe-179">Minutes of inactivity required before a password is required.</span></span>|
|<span data-ttu-id="270fe-180">passwordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="270fe-180">passwordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="270fe-181">Int32</span><span class="sxs-lookup"><span data-stu-id="270fe-181">Int32</span></span>|<span data-ttu-id="270fe-182">Minutos de inactividad que se requieren antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="270fe-182">Minutes of inactivity required before the screen times out.</span></span>|
|<span data-ttu-id="270fe-183">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="270fe-183">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="270fe-184">Int32</span><span class="sxs-lookup"><span data-stu-id="270fe-184">Int32</span></span>|<span data-ttu-id="270fe-185">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="270fe-185">Number of previous passwords to block.</span></span>|
|<span data-ttu-id="270fe-186">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="270fe-186">passwordRequiredType</span></span>|[<span data-ttu-id="270fe-187">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="270fe-187">requiredPasswordType</span></span>](../resources/intune_deviceconfig_requiredpasswordtype.md)|<span data-ttu-id="270fe-188">Tipo de contraseña que es necesario.</span><span class="sxs-lookup"><span data-stu-id="270fe-188">Type of password that is required.</span></span> <span data-ttu-id="270fe-189">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="270fe-189">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="270fe-190">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="270fe-190">passwordRequired</span></span>|<span data-ttu-id="270fe-191">Booleano</span><span class="sxs-lookup"><span data-stu-id="270fe-191">Boolean</span></span>|<span data-ttu-id="270fe-192">Si quiere requerir o no una contraseña.</span><span class="sxs-lookup"><span data-stu-id="270fe-192">Whether or not to require a password.</span></span>|



## <a name="response"></a><span data-ttu-id="270fe-193">Respuesta</span><span class="sxs-lookup"><span data-stu-id="270fe-193">Response</span></span>
<span data-ttu-id="270fe-194">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [macOSGeneralDeviceConfiguration](../resources/intune_deviceconfig_macosgeneraldeviceconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="270fe-194">If successful, this method returns a `201 Created` response code and a [macOSGeneralDeviceConfiguration](../resources/intune_deviceconfig_macosgeneraldeviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="270fe-195">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="270fe-195">Example</span></span>
### <a name="request"></a><span data-ttu-id="270fe-196">Solicitud</span><span class="sxs-lookup"><span data-stu-id="270fe-196">Request</span></span>
<span data-ttu-id="270fe-197">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="270fe-197">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 970

{
  "@odata.type": "#microsoft.graph.macOSGeneralDeviceConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "compliantAppsList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "compliantAppListType": "appsInListCompliant",
  "emailInDomainSuffixes": [
    "Email In Domain Suffixes value"
  ],
  "passwordBlockSimple": true,
  "passwordExpirationDays": 6,
  "passwordMinimumCharacterSetCount": 0,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordRequiredType": "alphanumeric",
  "passwordRequired": true
}
```

### <a name="response"></a><span data-ttu-id="270fe-198">Respuesta</span><span class="sxs-lookup"><span data-stu-id="270fe-198">Response</span></span>
<span data-ttu-id="270fe-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="270fe-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1078

{
  "@odata.type": "#microsoft.graph.macOSGeneralDeviceConfiguration",
  "id": "dc356aee-6aee-dc35-ee6a-35dcee6a35dc",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "compliantAppsList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "compliantAppListType": "appsInListCompliant",
  "emailInDomainSuffixes": [
    "Email In Domain Suffixes value"
  ],
  "passwordBlockSimple": true,
  "passwordExpirationDays": 6,
  "passwordMinimumCharacterSetCount": 0,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordRequiredType": "alphanumeric",
  "passwordRequired": true
}
```








