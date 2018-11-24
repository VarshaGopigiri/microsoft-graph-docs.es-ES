# <a name="create-sharedpcconfiguration"></a><span data-ttu-id="80525-101">Crear sharedPCConfiguration</span><span class="sxs-lookup"><span data-stu-id="80525-101">Create sharedPCConfiguration</span></span>

> <span data-ttu-id="80525-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="80525-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="80525-103">Crear un objeto [sharedPCConfiguration](../resources/intune_deviceconfig_sharedpcconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="80525-103">Create a new [sharedPCConfiguration](../resources/intune_deviceconfig_sharedpcconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="80525-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="80525-104">Prerequisites</span></span>
<span data-ttu-id="80525-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="80525-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="80525-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="80525-107">Permission type</span></span>|<span data-ttu-id="80525-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="80525-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="80525-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="80525-109">Delegated (work or school account)</span></span>|<span data-ttu-id="80525-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="80525-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="80525-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="80525-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="80525-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="80525-112">Not supported.</span></span>|
|<span data-ttu-id="80525-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="80525-113">Application</span></span>|<span data-ttu-id="80525-114">No compatible.</span><span class="sxs-lookup"><span data-stu-id="80525-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="80525-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="80525-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="80525-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="80525-116">Request headers</span></span>
|<span data-ttu-id="80525-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80525-117">Header</span></span>|<span data-ttu-id="80525-118">Valor</span><span class="sxs-lookup"><span data-stu-id="80525-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="80525-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="80525-119">Authorization</span></span>|<span data-ttu-id="80525-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="80525-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="80525-121">Accept</span><span class="sxs-lookup"><span data-stu-id="80525-121">Accept</span></span>|<span data-ttu-id="80525-122">application/json</span><span class="sxs-lookup"><span data-stu-id="80525-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="80525-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="80525-123">Request body</span></span>
<span data-ttu-id="80525-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto sharedPCConfiguration.</span><span class="sxs-lookup"><span data-stu-id="80525-124">In the request body, supply a JSON representation for the sharedPCConfiguration object.</span></span>

<span data-ttu-id="80525-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto sharedPCConfiguration.</span><span class="sxs-lookup"><span data-stu-id="80525-125">The following table shows the properties that are required when you create the sharedPCConfiguration.</span></span>

|<span data-ttu-id="80525-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="80525-126">Property</span></span>|<span data-ttu-id="80525-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="80525-127">Type</span></span>|<span data-ttu-id="80525-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="80525-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="80525-129">id</span><span class="sxs-lookup"><span data-stu-id="80525-129">id</span></span>|<span data-ttu-id="80525-130">String</span><span class="sxs-lookup"><span data-stu-id="80525-130">String</span></span>|<span data-ttu-id="80525-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="80525-131">Key of the entity.</span></span> <span data-ttu-id="80525-132">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="80525-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="80525-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="80525-133">lastModifiedDateTime</span></span>|<span data-ttu-id="80525-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="80525-134">DateTimeOffset</span></span>|<span data-ttu-id="80525-135">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="80525-135">DateTime the object was last modified.</span></span> <span data-ttu-id="80525-136">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="80525-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="80525-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="80525-137">createdDateTime</span></span>|<span data-ttu-id="80525-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="80525-138">DateTimeOffset</span></span>|<span data-ttu-id="80525-139">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="80525-139">DateTime the object was created.</span></span> <span data-ttu-id="80525-140">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="80525-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="80525-141">description</span><span class="sxs-lookup"><span data-stu-id="80525-141">description</span></span>|<span data-ttu-id="80525-142">String</span><span class="sxs-lookup"><span data-stu-id="80525-142">String</span></span>|<span data-ttu-id="80525-143">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="80525-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="80525-144">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="80525-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="80525-145">displayName</span><span class="sxs-lookup"><span data-stu-id="80525-145">displayName</span></span>|<span data-ttu-id="80525-146">String</span><span class="sxs-lookup"><span data-stu-id="80525-146">String</span></span>|<span data-ttu-id="80525-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="80525-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="80525-148">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="80525-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="80525-149">version</span><span class="sxs-lookup"><span data-stu-id="80525-149">version</span></span>|<span data-ttu-id="80525-150">Int32</span><span class="sxs-lookup"><span data-stu-id="80525-150">Int32</span></span>|<span data-ttu-id="80525-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="80525-151">Version of the device configuration.</span></span> <span data-ttu-id="80525-152">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="80525-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="80525-153">accountManagerPolicy</span><span class="sxs-lookup"><span data-stu-id="80525-153">accountManagerPolicy</span></span>|[<span data-ttu-id="80525-154">sharedPCAccountManagerPolicy</span><span class="sxs-lookup"><span data-stu-id="80525-154">sharedPCAccountManagerPolicy</span></span>](../resources/intune_deviceconfig_sharedpcaccountmanagerpolicy.md)|<span data-ttu-id="80525-155">Especifica cómo se administran las cuentas en un equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="80525-155">Specifies how accounts are managed on a shared PC.</span></span> <span data-ttu-id="80525-156">Solo se aplica cuando disableAccountManager es False.</span><span class="sxs-lookup"><span data-stu-id="80525-156">Only applies when disableAccountManager is false.</span></span>|
|<span data-ttu-id="80525-157">allowedAccounts</span><span class="sxs-lookup"><span data-stu-id="80525-157">allowedAccounts</span></span>|[<span data-ttu-id="80525-158">sharedPCAllowedAccountType</span><span class="sxs-lookup"><span data-stu-id="80525-158">sharedPCAllowedAccountType</span></span>](../resources/intune_deviceconfig_sharedpcallowedaccounttype.md)|<span data-ttu-id="80525-159">Indica el tipo de cuentas que se pueden usar en un equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="80525-159">Indicates which type of accounts are allowed to use on a shared PC.</span></span> <span data-ttu-id="80525-160">Los valores posibles son: `guest` y `domain`.</span><span class="sxs-lookup"><span data-stu-id="80525-160">Possible values are: `guest`, `domain`.</span></span>|
|<span data-ttu-id="80525-161">allowLocalStorage</span><span class="sxs-lookup"><span data-stu-id="80525-161">allowLocalStorage</span></span>|<span data-ttu-id="80525-162">Boolean</span><span class="sxs-lookup"><span data-stu-id="80525-162">Boolean</span></span>|<span data-ttu-id="80525-163">Especifica si se permite el almacenamiento local en un equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="80525-163">Specifies whether local storage is allowed on a shared PC.</span></span>|
|<span data-ttu-id="80525-164">disableAccountManager</span><span class="sxs-lookup"><span data-stu-id="80525-164">disableAccountManager</span></span>|<span data-ttu-id="80525-165">Boolean</span><span class="sxs-lookup"><span data-stu-id="80525-165">Boolean</span></span>|<span data-ttu-id="80525-166">Deshabilita al administrador de cuentas para el modo de equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="80525-166">Disables the account manager for shared PC mode.</span></span>|
|<span data-ttu-id="80525-167">disableEduPolicies</span><span class="sxs-lookup"><span data-stu-id="80525-167">disableEduPolicies</span></span>|<span data-ttu-id="80525-168">Boolean</span><span class="sxs-lookup"><span data-stu-id="80525-168">Boolean</span></span>|<span data-ttu-id="80525-169">Especifica si se deben deshabilitar las directivas predeterminadas de entorno educativo de equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="80525-169">Specifies whether the default shared PC education environment policies should be disabled.</span></span> <span data-ttu-id="80525-170">Para Windows 10 RS2 y versiones posteriores, se aplicará esta directiva sin establecer Habilitado en true.</span><span class="sxs-lookup"><span data-stu-id="80525-170">For Windows 10 RS2 and later, this policy will be applied without setting Enabled to true.</span></span>|
|<span data-ttu-id="80525-171">disablePowerPolicies</span><span class="sxs-lookup"><span data-stu-id="80525-171">disablePowerPolicies</span></span>|<span data-ttu-id="80525-172">Boolean</span><span class="sxs-lookup"><span data-stu-id="80525-172">Boolean</span></span>|<span data-ttu-id="80525-173">Especifica si se deben deshabilitar las directivas predeterminadas de energía de equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="80525-173">Specifies whether the default shared PC power policies should be disabled.</span></span>|
|<span data-ttu-id="80525-174">disableSignInOnResume</span><span class="sxs-lookup"><span data-stu-id="80525-174">disableSignInOnResume</span></span>|<span data-ttu-id="80525-175">Boolean</span><span class="sxs-lookup"><span data-stu-id="80525-175">Boolean</span></span>|<span data-ttu-id="80525-176">Deshabilita el requisito de iniciar sesión siempre que el dispositivo salga del modo de suspensión.</span><span class="sxs-lookup"><span data-stu-id="80525-176">Disables the requirement to sign in whenever the device wakes up from sleep mode.</span></span>|
|<span data-ttu-id="80525-177">enabled</span><span class="sxs-lookup"><span data-stu-id="80525-177">enabled</span></span>|<span data-ttu-id="80525-178">Boolean</span><span class="sxs-lookup"><span data-stu-id="80525-178">Boolean</span></span>|<span data-ttu-id="80525-179">Habilita el modo de equipo compartido y se aplica a las directivas de equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="80525-179">Enables shared PC mode and applies the shared pc policies.</span></span>|
|<span data-ttu-id="80525-180">idleTimeBeforeSleepInSeconds</span><span class="sxs-lookup"><span data-stu-id="80525-180">idleTimeBeforeSleepInSeconds</span></span>|<span data-ttu-id="80525-181">Int32</span><span class="sxs-lookup"><span data-stu-id="80525-181">Int32</span></span>|<span data-ttu-id="80525-182">Especifica el tiempo en segundos que un dispositivo debe permanecer inactivo antes de que el equipo pase al estado de suspensión.</span><span class="sxs-lookup"><span data-stu-id="80525-182">Specifies the time in seconds that a device must sit idle before the PC goes to sleep.</span></span> <span data-ttu-id="80525-183">Si este valor se establece en 0 impide que se produzca el tiempo de espera en suspensión.</span><span class="sxs-lookup"><span data-stu-id="80525-183">Setting this value to 0 prevents the sleep timeout from occurring.</span></span>|
|<span data-ttu-id="80525-184">kioskAppDisplayName</span><span class="sxs-lookup"><span data-stu-id="80525-184">kioskAppDisplayName</span></span>|<span data-ttu-id="80525-185">String</span><span class="sxs-lookup"><span data-stu-id="80525-185">String</span></span>|<span data-ttu-id="80525-186">Especifica el texto para mostrar de la cuenta que se muestra en la pantalla de inicio de sesión que inicia la aplicación especificada por SetKioskAppUserModelId.</span><span class="sxs-lookup"><span data-stu-id="80525-186">Specifies the display text for the account shown on the sign-in screen which launches the app specified by SetKioskAppUserModelId.</span></span> <span data-ttu-id="80525-187">Solo se aplica cuando se establece KioskAppUserModelId.</span><span class="sxs-lookup"><span data-stu-id="80525-187">Only applies when KioskAppUserModelId is set.</span></span>|
|<span data-ttu-id="80525-188">kioskAppUserModelId</span><span class="sxs-lookup"><span data-stu-id="80525-188">kioskAppUserModelId</span></span>|<span data-ttu-id="80525-189">String</span><span class="sxs-lookup"><span data-stu-id="80525-189">String</span></span>|<span data-ttu-id="80525-190">Especifica el identificador del modelo de usuario de la aplicación correspondiente a la aplicación para que se use con el acceso asignado.</span><span class="sxs-lookup"><span data-stu-id="80525-190">Specifies the application user model ID of the app to use with assigned access.</span></span>|
|<span data-ttu-id="80525-191">maintenanceStartTime</span><span class="sxs-lookup"><span data-stu-id="80525-191">maintenanceStartTime</span></span>|<span data-ttu-id="80525-192">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="80525-192">TimeOfDay</span></span>|<span data-ttu-id="80525-193">Especifica la hora de inicio diaria de la hora de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="80525-193">Specifies the daily start time of maintenance hour.</span></span>|



## <a name="response"></a><span data-ttu-id="80525-194">Respuesta</span><span class="sxs-lookup"><span data-stu-id="80525-194">Response</span></span>
<span data-ttu-id="80525-195">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [sharedPCConfiguration](../resources/intune_deviceconfig_sharedpcconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="80525-195">If successful, this method returns a `201 Created` response code and a [sharedPCConfiguration](../resources/intune_deviceconfig_sharedpcconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="80525-196">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="80525-196">Example</span></span>
### <a name="request"></a><span data-ttu-id="80525-197">Solicitud</span><span class="sxs-lookup"><span data-stu-id="80525-197">Request</span></span>
<span data-ttu-id="80525-198">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="80525-198">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 860

{
  "@odata.type": "#microsoft.graph.sharedPCConfiguration",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "accountManagerPolicy": {
    "@odata.type": "microsoft.graph.sharedPCAccountManagerPolicy",
    "accountDeletionPolicy": "diskSpaceThreshold",
    "cacheAccountsAboveDiskFreePercentage": 4,
    "inactiveThresholdDays": 5,
    "removeAccountsBelowDiskFreePercentage": 5
  },
  "allowedAccounts": "domain",
  "allowLocalStorage": true,
  "disableAccountManager": true,
  "disableEduPolicies": true,
  "disablePowerPolicies": true,
  "disableSignInOnResume": true,
  "enabled": true,
  "idleTimeBeforeSleepInSeconds": 12,
  "kioskAppDisplayName": "Kiosk App Display Name value",
  "kioskAppUserModelId": "Kiosk App User Model Id value",
  "maintenanceStartTime": "11:59:24.7240000"
}
```

### <a name="response"></a><span data-ttu-id="80525-199">Respuesta</span><span class="sxs-lookup"><span data-stu-id="80525-199">Response</span></span>
<span data-ttu-id="80525-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="80525-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1032

{
  "@odata.type": "#microsoft.graph.sharedPCConfiguration",
  "id": "5206be3b-be3b-5206-3bbe-06523bbe0652",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "accountManagerPolicy": {
    "@odata.type": "microsoft.graph.sharedPCAccountManagerPolicy",
    "accountDeletionPolicy": "diskSpaceThreshold",
    "cacheAccountsAboveDiskFreePercentage": 4,
    "inactiveThresholdDays": 5,
    "removeAccountsBelowDiskFreePercentage": 5
  },
  "allowedAccounts": "domain",
  "allowLocalStorage": true,
  "disableAccountManager": true,
  "disableEduPolicies": true,
  "disablePowerPolicies": true,
  "disableSignInOnResume": true,
  "enabled": true,
  "idleTimeBeforeSleepInSeconds": 12,
  "kioskAppDisplayName": "Kiosk App Display Name value",
  "kioskAppUserModelId": "Kiosk App User Model Id value",
  "maintenanceStartTime": "11:59:24.7240000"
}
```



