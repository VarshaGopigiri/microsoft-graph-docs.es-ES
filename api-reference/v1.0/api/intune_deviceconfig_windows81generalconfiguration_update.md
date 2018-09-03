# <a name="update-windows81generalconfiguration"></a><span data-ttu-id="c8424-101">Actualizar windows81GeneralConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8424-101">Update windows81GeneralConfiguration</span></span>

> <span data-ttu-id="c8424-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c8424-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c8424-103">Actualice las propiedades de un objeto [windows81GeneralConfiguration](../resources/intune_deviceconfig_windows81generalconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="c8424-103">Update the properties of a [windows81GeneralConfiguration](../resources/intune_deviceconfig_windows81generalconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c8424-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c8424-104">Prerequisites</span></span>
<span data-ttu-id="c8424-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c8424-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c8424-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c8424-107">Permission type</span></span>|<span data-ttu-id="c8424-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c8424-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c8424-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c8424-109">Delegated (work or school account)</span></span>|<span data-ttu-id="c8424-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c8424-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="c8424-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c8424-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c8424-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c8424-112">Not supported.</span></span>|
|<span data-ttu-id="c8424-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c8424-113">Application</span></span>|<span data-ttu-id="c8424-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c8424-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c8424-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c8424-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="c8424-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c8424-116">Request headers</span></span>
|<span data-ttu-id="c8424-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8424-117">Header</span></span>|<span data-ttu-id="c8424-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c8424-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c8424-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="c8424-119">Authorization</span></span>|<span data-ttu-id="c8424-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c8424-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c8424-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c8424-121">Accept</span></span>|<span data-ttu-id="c8424-122">application/json</span><span class="sxs-lookup"><span data-stu-id="c8424-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c8424-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c8424-123">Request body</span></span>
<span data-ttu-id="c8424-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windows81GeneralConfiguration](../resources/intune_deviceconfig_windows81generalconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="c8424-124">In the request body, supply a JSON representation for the [windows81GeneralConfiguration](../resources/intune_deviceconfig_windows81generalconfiguration.md) object.</span></span>

<span data-ttu-id="c8424-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windows81GeneralConfiguration](../resources/intune_deviceconfig_windows81generalconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="c8424-125">The following table shows the properties that are required when you create the [windows81GeneralConfiguration](../resources/intune_deviceconfig_windows81generalconfiguration.md).</span></span>

|<span data-ttu-id="c8424-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c8424-126">Property</span></span>|<span data-ttu-id="c8424-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="c8424-127">Type</span></span>|<span data-ttu-id="c8424-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8424-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c8424-129">id</span><span class="sxs-lookup"><span data-stu-id="c8424-129">id</span></span>|<span data-ttu-id="c8424-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="c8424-130">String</span></span>|<span data-ttu-id="c8424-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="c8424-131">Key of the entity.</span></span> <span data-ttu-id="c8424-132">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="c8424-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="c8424-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="c8424-133">lastModifiedDateTime</span></span>|<span data-ttu-id="c8424-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c8424-134">DateTimeOffset</span></span>|<span data-ttu-id="c8424-135">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="c8424-135">DateTime the object was last modified.</span></span> <span data-ttu-id="c8424-136">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="c8424-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="c8424-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="c8424-137">createdDateTime</span></span>|<span data-ttu-id="c8424-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c8424-138">DateTimeOffset</span></span>|<span data-ttu-id="c8424-139">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="c8424-139">DateTime the object was created.</span></span> <span data-ttu-id="c8424-140">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="c8424-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="c8424-141">descripción</span><span class="sxs-lookup"><span data-stu-id="c8424-141">description</span></span>|<span data-ttu-id="c8424-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="c8424-142">String</span></span>|<span data-ttu-id="c8424-143">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c8424-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="c8424-144">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="c8424-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="c8424-145">displayName</span><span class="sxs-lookup"><span data-stu-id="c8424-145">displayName</span></span>|<span data-ttu-id="c8424-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="c8424-146">String</span></span>|<span data-ttu-id="c8424-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c8424-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="c8424-148">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="c8424-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="c8424-149">version</span><span class="sxs-lookup"><span data-stu-id="c8424-149">version</span></span>|<span data-ttu-id="c8424-150">Int32</span><span class="sxs-lookup"><span data-stu-id="c8424-150">Int32</span></span>|<span data-ttu-id="c8424-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c8424-151">Version of the device configuration.</span></span> <span data-ttu-id="c8424-152">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="c8424-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="c8424-153">accountsBlockAddingNonMicrosoftAccountEmail</span><span class="sxs-lookup"><span data-stu-id="c8424-153">accountsBlockAddingNonMicrosoftAccountEmail</span></span>|<span data-ttu-id="c8424-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="c8424-154">Boolean</span></span>|<span data-ttu-id="c8424-155">Indica si se va a impedir que el usuario agregue cuentas de correo electrónico en el dispositivo que no están asociadas a una cuenta de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c8424-155">Indicates whether or not to Block the user from adding email accounts to the device that are not associated with a Microsoft account.</span></span>|
|<span data-ttu-id="c8424-156">applyOnlyToWindows81</span><span class="sxs-lookup"><span data-stu-id="c8424-156">applyOnlyToWindows81</span></span>|<span data-ttu-id="c8424-157">Booleano</span><span class="sxs-lookup"><span data-stu-id="c8424-157">Boolean</span></span>|<span data-ttu-id="c8424-158">Valor que indica si esta directiva se aplica solo a Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="c8424-158">Value indicating whether this policy only applies to Windows 8.1.</span></span> <span data-ttu-id="c8424-159">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c8424-159">This property is read-only.</span></span>|
|<span data-ttu-id="c8424-160">browserBlockAutofill</span><span class="sxs-lookup"><span data-stu-id="c8424-160">browserBlockAutofill</span></span>|<span data-ttu-id="c8424-161">Booleano</span><span class="sxs-lookup"><span data-stu-id="c8424-161">Boolean</span></span>|<span data-ttu-id="c8424-162">Indica si se va a bloquear el autorrelleno.</span><span class="sxs-lookup"><span data-stu-id="c8424-162">Indicates whether or not to block auto fill.</span></span>|
|<span data-ttu-id="c8424-163">browserBlockAutomaticDetectionOfIntranetSites</span><span class="sxs-lookup"><span data-stu-id="c8424-163">browserBlockAutomaticDetectionOfIntranetSites</span></span>|<span data-ttu-id="c8424-164">Booleano</span><span class="sxs-lookup"><span data-stu-id="c8424-164">Boolean</span></span>|<span data-ttu-id="c8424-165">Indica si se va a bloquear la detección automática de sitios de intranet.</span><span class="sxs-lookup"><span data-stu-id="c8424-165">Indicates whether or not to block automatic detection of Intranet sites.</span></span>|
|<span data-ttu-id="c8424-166">browserBlockEnterpriseModeAccess</span><span class="sxs-lookup"><span data-stu-id="c8424-166">browserBlockEnterpriseModeAccess</span></span>|<span data-ttu-id="c8424-167">Booleano</span><span class="sxs-lookup"><span data-stu-id="c8424-167">Boolean</span></span>|<span data-ttu-id="c8424-168">Indica si se va a bloquear el acceso al modo de empresa.</span><span class="sxs-lookup"><span data-stu-id="c8424-168">Indicates whether or not to block enterprise mode access.</span></span>|
|<span data-ttu-id="c8424-169">browserBlockJavaScript</span><span class="sxs-lookup"><span data-stu-id="c8424-169">browserBlockJavaScript</span></span>|<span data-ttu-id="c8424-170">Booleano</span><span class="sxs-lookup"><span data-stu-id="c8424-170">Boolean</span></span>|<span data-ttu-id="c8424-171">Indica si se va a impedir que el usuario utilice JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c8424-171">Indicates whether or not to Block the user from using JavaScript.</span></span>|
|<span data-ttu-id="c8424-172">browserBlockPlugins</span><span class="sxs-lookup"><span data-stu-id="c8424-172">browserBlockPlugins</span></span>|<span data-ttu-id="c8424-173">Booleano</span><span class="sxs-lookup"><span data-stu-id="c8424-173">Boolean</span></span>|<span data-ttu-id="c8424-174">Indica si se van a bloquear los complementos.</span><span class="sxs-lookup"><span data-stu-id="c8424-174">Indicates whether or not to block plug-ins.</span></span>|
|<span data-ttu-id="c8424-175">browserBlockPopups</span><span class="sxs-lookup"><span data-stu-id="c8424-175">browserBlockPopups</span></span>|<span data-ttu-id="c8424-176">Booleano</span><span class="sxs-lookup"><span data-stu-id="c8424-176">Boolean</span></span>|<span data-ttu-id="c8424-177">Indica si se van a bloquear los elementos emergentes.</span><span class="sxs-lookup"><span data-stu-id="c8424-177">Indicates whether or not to block popups.</span></span>|
|<span data-ttu-id="c8424-178">browserBlockSendingDoNotTrackHeader</span><span class="sxs-lookup"><span data-stu-id="c8424-178">browserBlockSendingDoNotTrackHeader</span></span>|<span data-ttu-id="c8424-179">Booleano</span><span class="sxs-lookup"><span data-stu-id="c8424-179">Boolean</span></span>|<span data-ttu-id="c8424-180">Indica si se va a impedir que el usuario envíe el encabezado Do Not Track.</span><span class="sxs-lookup"><span data-stu-id="c8424-180">Indicates whether or not to Block the user from sending the do not track header.</span></span>|
|<span data-ttu-id="c8424-181">browserBlockSingleWordEntryOnIntranetSites</span><span class="sxs-lookup"><span data-stu-id="c8424-181">browserBlockSingleWordEntryOnIntranetSites</span></span>|<span data-ttu-id="c8424-182">Booleano</span><span class="sxs-lookup"><span data-stu-id="c8424-182">Boolean</span></span>|<span data-ttu-id="c8424-183">Indica si se va a bloquear la entrada de palabra única en sitios de intranet.</span><span class="sxs-lookup"><span data-stu-id="c8424-183">Indicates whether or not to block a single word entry on Intranet sites.</span></span>|
|<span data-ttu-id="c8424-184">browserRequireSmartScreen</span><span class="sxs-lookup"><span data-stu-id="c8424-184">browserRequireSmartScreen</span></span>|<span data-ttu-id="c8424-185">Booleano</span><span class="sxs-lookup"><span data-stu-id="c8424-185">Boolean</span></span>|<span data-ttu-id="c8424-186">Indica si se va a requerir que el usuario use el filtro de pantalla inteligente.</span><span class="sxs-lookup"><span data-stu-id="c8424-186">Indicates whether or not to require the user to use the smart screen filter.</span></span>|
|<span data-ttu-id="c8424-187">browserEnterpriseModeSiteListLocation</span><span class="sxs-lookup"><span data-stu-id="c8424-187">browserEnterpriseModeSiteListLocation</span></span>|<span data-ttu-id="c8424-188">Cadena</span><span class="sxs-lookup"><span data-stu-id="c8424-188">String</span></span>|<span data-ttu-id="c8424-189">Ubicación de la lista de sitios del modo de empresa.</span><span class="sxs-lookup"><span data-stu-id="c8424-189">The enterprise mode site list location.</span></span> <span data-ttu-id="c8424-190">Puede ser un archivo local, la red local o la ubicación http.</span><span class="sxs-lookup"><span data-stu-id="c8424-190">Could be a local file, local network or http location.</span></span>|
|<span data-ttu-id="c8424-191">browserInternetSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="c8424-191">browserInternetSecurityLevel</span></span>|[<span data-ttu-id="c8424-192">internetSiteSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="c8424-192">internetSiteSecurityLevel</span></span>](../resources/intune_deviceconfig_internetsitesecuritylevel.md)|<span data-ttu-id="c8424-193">Nivel de seguridad de Internet.</span><span class="sxs-lookup"><span data-stu-id="c8424-193">The internet security level.</span></span> <span data-ttu-id="c8424-194">Los valores posibles son: `userDefined`, `medium`, `mediumHigh` y `high`.</span><span class="sxs-lookup"><span data-stu-id="c8424-194">The possible values are `userDefined`, `medium`, `mediumHigh`, `high`, , , , , , , , or .</span></span>|
|<span data-ttu-id="c8424-195">browserIntranetSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="c8424-195">browserIntranetSecurityLevel</span></span>|[<span data-ttu-id="c8424-196">siteSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="c8424-196">siteSecurityLevel</span></span>](../resources/intune_deviceconfig_sitesecuritylevel.md)|<span data-ttu-id="c8424-197">Nivel de seguridad de la intranet.</span><span class="sxs-lookup"><span data-stu-id="c8424-197">The Intranet security level.</span></span> <span data-ttu-id="c8424-198">Los valores posibles son `userDefined`, `low`, `mediumLow`, `medium`, `mediumHigh` y `high`.</span><span class="sxs-lookup"><span data-stu-id="c8424-198">The possible values are `userDefined`, `low`, `mediumLow`, `medium`, `mediumHigh`, `high`, , , , , , or .</span></span>|
|<span data-ttu-id="c8424-199">browserLoggingReportLocation</span><span class="sxs-lookup"><span data-stu-id="c8424-199">browserLoggingReportLocation</span></span>|<span data-ttu-id="c8424-200">Cadena</span><span class="sxs-lookup"><span data-stu-id="c8424-200">String</span></span>|<span data-ttu-id="c8424-201">Ubicación del informe de registro.</span><span class="sxs-lookup"><span data-stu-id="c8424-201">The logging report location.</span></span>|
|<span data-ttu-id="c8424-202">browserRequireHighSecurityForRestrictedSites</span><span class="sxs-lookup"><span data-stu-id="c8424-202">browserRequireHighSecurityForRestrictedSites</span></span>|<span data-ttu-id="c8424-203">Booleano</span><span class="sxs-lookup"><span data-stu-id="c8424-203">Boolean</span></span>|<span data-ttu-id="c8424-204">Indica si se va a requerir alta seguridad para los sitios restringidos.</span><span class="sxs-lookup"><span data-stu-id="c8424-204">Indicates whether or not to require high security for restricted sites.</span></span>|
|<span data-ttu-id="c8424-205">browserRequireFirewall</span><span class="sxs-lookup"><span data-stu-id="c8424-205">browserRequireFirewall</span></span>|<span data-ttu-id="c8424-206">Booleano</span><span class="sxs-lookup"><span data-stu-id="c8424-206">Boolean</span></span>|<span data-ttu-id="c8424-207">Indica si se va a requerir un firewall.</span><span class="sxs-lookup"><span data-stu-id="c8424-207">Indicates whether or not to require a firewall.</span></span>|
|<span data-ttu-id="c8424-208">browserRequireFraudWarning</span><span class="sxs-lookup"><span data-stu-id="c8424-208">browserRequireFraudWarning</span></span>|<span data-ttu-id="c8424-209">Booleano</span><span class="sxs-lookup"><span data-stu-id="c8424-209">Boolean</span></span>|<span data-ttu-id="c8424-210">Indica si se va a requerir una advertencia de fraude.</span><span class="sxs-lookup"><span data-stu-id="c8424-210">Indicates whether or not to require fraud warning.</span></span>|
|<span data-ttu-id="c8424-211">browserTrustedSitesSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="c8424-211">browserTrustedSitesSecurityLevel</span></span>|[<span data-ttu-id="c8424-212">siteSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="c8424-212">siteSecurityLevel</span></span>](../resources/intune_deviceconfig_sitesecuritylevel.md)|<span data-ttu-id="c8424-213">Nivel de seguridad de los sitios de confianza.</span><span class="sxs-lookup"><span data-stu-id="c8424-213">The trusted sites security level.</span></span> <span data-ttu-id="c8424-214">Los valores posibles son `userDefined`, `low`, `mediumLow`, `medium`, `mediumHigh` y `high`.</span><span class="sxs-lookup"><span data-stu-id="c8424-214">The possible values are `userDefined`, `low`, `mediumLow`, `medium`, `mediumHigh`, `high`, , , , , , or .</span></span>|
|<span data-ttu-id="c8424-215">cellularBlockDataRoaming</span><span class="sxs-lookup"><span data-stu-id="c8424-215">cellularBlockDataRoaming</span></span>|<span data-ttu-id="c8424-216">Booleano</span><span class="sxs-lookup"><span data-stu-id="c8424-216">Boolean</span></span>|<span data-ttu-id="c8424-217">Indica si se va a bloquear la itinerancia de datos.</span><span class="sxs-lookup"><span data-stu-id="c8424-217">Indicates whether or not to block data roaming.</span></span>|
|<span data-ttu-id="c8424-218">diagnosticsBlockDataSubmission</span><span class="sxs-lookup"><span data-stu-id="c8424-218">diagnosticsBlockDataSubmission</span></span>|<span data-ttu-id="c8424-219">Booleano</span><span class="sxs-lookup"><span data-stu-id="c8424-219">Boolean</span></span>|<span data-ttu-id="c8424-220">Indica si se va a bloquear el envío de datos de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="c8424-220">Indicates whether or not to block diagnostic data submission.</span></span>|
|<span data-ttu-id="c8424-221">passwordBlockPicturePasswordAndPin</span><span class="sxs-lookup"><span data-stu-id="c8424-221">passwordBlockPicturePasswordAndPin</span></span>|<span data-ttu-id="c8424-222">Booleano</span><span class="sxs-lookup"><span data-stu-id="c8424-222">Boolean</span></span>|<span data-ttu-id="c8424-223">Indica si se va a impedir que el usuario utilice una contraseña de imágenes y un PIN.</span><span class="sxs-lookup"><span data-stu-id="c8424-223">Indicates whether or not to Block the user from using a pictures password and pin.</span></span>|
|<span data-ttu-id="c8424-224">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="c8424-224">passwordExpirationDays</span></span>|<span data-ttu-id="c8424-225">Int32</span><span class="sxs-lookup"><span data-stu-id="c8424-225">Int32</span></span>|<span data-ttu-id="c8424-226">Expiración de la contraseña en días.</span><span class="sxs-lookup"><span data-stu-id="c8424-226">Password expiration in days.</span></span>|
|<span data-ttu-id="c8424-227">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="c8424-227">passwordMinimumLength</span></span>|<span data-ttu-id="c8424-228">Int32</span><span class="sxs-lookup"><span data-stu-id="c8424-228">Int32</span></span>|<span data-ttu-id="c8424-229">La longitud mínima de contraseña.</span><span class="sxs-lookup"><span data-stu-id="c8424-229">The minimum password length.</span></span>|
|<span data-ttu-id="c8424-230">passwordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="c8424-230">passwordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="c8424-231">Int32</span><span class="sxs-lookup"><span data-stu-id="c8424-231">Int32</span></span>|<span data-ttu-id="c8424-232">Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="c8424-232">The minutes of inactivity before the screen times out.</span></span>|
|<span data-ttu-id="c8424-233">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="c8424-233">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="c8424-234">Int32</span><span class="sxs-lookup"><span data-stu-id="c8424-234">Int32</span></span>|<span data-ttu-id="c8424-235">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="c8424-235">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="c8424-236">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="c8424-236">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="c8424-237">Int32</span><span class="sxs-lookup"><span data-stu-id="c8424-237">Int32</span></span>|<span data-ttu-id="c8424-238">Número de contraseñas anteriores que impide su reutilización.</span><span class="sxs-lookup"><span data-stu-id="c8424-238">The number of previous passwords to prevent re-use of.</span></span> <span data-ttu-id="c8424-239">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="c8424-239">Valid values 0 to 24</span></span>|
|<span data-ttu-id="c8424-240">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="c8424-240">passwordRequiredType</span></span>|[<span data-ttu-id="c8424-241">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="c8424-241">requiredPasswordType</span></span>](../resources/intune_deviceconfig_requiredpasswordtype.md)|<span data-ttu-id="c8424-242">Tipo de contraseña necesaria.</span><span class="sxs-lookup"><span data-stu-id="c8424-242">The required password type.</span></span> <span data-ttu-id="c8424-243">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="c8424-243">The possible values are `deviceDefault`, `alphanumeric`, `numeric`, , , , , , , , , or .</span></span>|
|<span data-ttu-id="c8424-244">passwordSignInFailureCountBeforeFactoryReset</span><span class="sxs-lookup"><span data-stu-id="c8424-244">passwordSignInFailureCountBeforeFactoryReset</span></span>|<span data-ttu-id="c8424-245">Int32</span><span class="sxs-lookup"><span data-stu-id="c8424-245">Int32</span></span>|<span data-ttu-id="c8424-246">Número de errores de inicio de sesión permitidos antes del restablecimiento de fábrica.</span><span class="sxs-lookup"><span data-stu-id="c8424-246">The number of sign in failures before factory reset.</span></span>|
|<span data-ttu-id="c8424-247">storageRequireDeviceEncryption</span><span class="sxs-lookup"><span data-stu-id="c8424-247">storageRequireDeviceEncryption</span></span>|<span data-ttu-id="c8424-248">Booleano</span><span class="sxs-lookup"><span data-stu-id="c8424-248">Boolean</span></span>|<span data-ttu-id="c8424-249">Indica si se va a requerir el cifrado en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="c8424-249">Indicates whether or not to require encryption on a mobile device.</span></span>|
|<span data-ttu-id="c8424-250">updatesRequireAutomaticUpdates</span><span class="sxs-lookup"><span data-stu-id="c8424-250">updatesRequireAutomaticUpdates</span></span>|<span data-ttu-id="c8424-251">Booleano</span><span class="sxs-lookup"><span data-stu-id="c8424-251">Boolean</span></span>|<span data-ttu-id="c8424-252">Indica si se van a requerir las actualizaciones automáticas.</span><span class="sxs-lookup"><span data-stu-id="c8424-252">Indicates whether or not to require automatic updates.</span></span>|
|<span data-ttu-id="c8424-253">userAccountControlSettings</span><span class="sxs-lookup"><span data-stu-id="c8424-253">userAccountControlSettings</span></span>|[<span data-ttu-id="c8424-254">windowsUserAccountControlSettings</span><span class="sxs-lookup"><span data-stu-id="c8424-254">windowsUserAccountControlSettings</span></span>](../resources/intune_deviceconfig_windowsuseraccountcontrolsettings.md)|<span data-ttu-id="c8424-255">Configuración del control de cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="c8424-255">The user account control settings.</span></span> <span data-ttu-id="c8424-256">Los valores posibles son: `userDefined`, `alwaysNotify`, `notifyOnAppChanges`, `notifyOnAppChangesWithoutDimming` y `neverNotify`.</span><span class="sxs-lookup"><span data-stu-id="c8424-256">The possible values are `userDefined`, `alwaysNotify`, `notifyOnAppChanges`, `notifyOnAppChangesWithoutDimming`, `neverNotify`, , , , , , , or .</span></span>|
|<span data-ttu-id="c8424-257">workFoldersUrl</span><span class="sxs-lookup"><span data-stu-id="c8424-257">workFoldersUrl</span></span>|<span data-ttu-id="c8424-258">Cadena</span><span class="sxs-lookup"><span data-stu-id="c8424-258">String</span></span>|<span data-ttu-id="c8424-259">Dirección URL de las carpetas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="c8424-259">The work folders url.</span></span>|



## <a name="response"></a><span data-ttu-id="c8424-260">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c8424-260">Response</span></span>
<span data-ttu-id="c8424-261">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows81GeneralConfiguration](../resources/intune_deviceconfig_windows81generalconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c8424-261">If successful, this method returns a `200 OK` response code and an updated [windows81GeneralConfiguration](../resources/intune_deviceconfig_windows81generalconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c8424-262">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c8424-262">Example</span></span>
### <a name="request"></a><span data-ttu-id="c8424-263">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c8424-263">Request</span></span>
<span data-ttu-id="c8424-264">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c8424-264">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 1689

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "accountsBlockAddingNonMicrosoftAccountEmail": true,
  "applyOnlyToWindows81": true,
  "browserBlockAutofill": true,
  "browserBlockAutomaticDetectionOfIntranetSites": true,
  "browserBlockEnterpriseModeAccess": true,
  "browserBlockJavaScript": true,
  "browserBlockPlugins": true,
  "browserBlockPopups": true,
  "browserBlockSendingDoNotTrackHeader": true,
  "browserBlockSingleWordEntryOnIntranetSites": true,
  "browserRequireSmartScreen": true,
  "browserEnterpriseModeSiteListLocation": "Browser Enterprise Mode Site List Location value",
  "browserInternetSecurityLevel": "medium",
  "browserIntranetSecurityLevel": "low",
  "browserLoggingReportLocation": "Browser Logging Report Location value",
  "browserRequireHighSecurityForRestrictedSites": true,
  "browserRequireFirewall": true,
  "browserRequireFraudWarning": true,
  "browserTrustedSitesSecurityLevel": "low",
  "cellularBlockDataRoaming": true,
  "diagnosticsBlockDataSubmission": true,
  "passwordBlockPicturePasswordAndPin": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordMinimumCharacterSetCount": 0,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordRequiredType": "alphanumeric",
  "passwordSignInFailureCountBeforeFactoryReset": 12,
  "storageRequireDeviceEncryption": true,
  "updatesRequireAutomaticUpdates": true,
  "userAccountControlSettings": "alwaysNotify",
  "workFoldersUrl": "https://example.com/workFoldersUrl/"
}
```

### <a name="response"></a><span data-ttu-id="c8424-265">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c8424-265">Response</span></span>
<span data-ttu-id="c8424-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c8424-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1865

{
  "@odata.type": "#microsoft.graph.windows81GeneralConfiguration",
  "id": "0e9285b5-85b5-0e92-b585-920eb585920e",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "accountsBlockAddingNonMicrosoftAccountEmail": true,
  "applyOnlyToWindows81": true,
  "browserBlockAutofill": true,
  "browserBlockAutomaticDetectionOfIntranetSites": true,
  "browserBlockEnterpriseModeAccess": true,
  "browserBlockJavaScript": true,
  "browserBlockPlugins": true,
  "browserBlockPopups": true,
  "browserBlockSendingDoNotTrackHeader": true,
  "browserBlockSingleWordEntryOnIntranetSites": true,
  "browserRequireSmartScreen": true,
  "browserEnterpriseModeSiteListLocation": "Browser Enterprise Mode Site List Location value",
  "browserInternetSecurityLevel": "medium",
  "browserIntranetSecurityLevel": "low",
  "browserLoggingReportLocation": "Browser Logging Report Location value",
  "browserRequireHighSecurityForRestrictedSites": true,
  "browserRequireFirewall": true,
  "browserRequireFraudWarning": true,
  "browserTrustedSitesSecurityLevel": "low",
  "cellularBlockDataRoaming": true,
  "diagnosticsBlockDataSubmission": true,
  "passwordBlockPicturePasswordAndPin": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordMinimumCharacterSetCount": 0,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordRequiredType": "alphanumeric",
  "passwordSignInFailureCountBeforeFactoryReset": 12,
  "storageRequireDeviceEncryption": true,
  "updatesRequireAutomaticUpdates": true,
  "userAccountControlSettings": "alwaysNotify",
  "workFoldersUrl": "https://example.com/workFoldersUrl/"
}
```



