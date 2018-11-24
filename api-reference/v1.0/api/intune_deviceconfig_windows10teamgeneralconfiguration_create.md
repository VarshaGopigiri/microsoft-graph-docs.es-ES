# <a name="create-windows10teamgeneralconfiguration"></a><span data-ttu-id="ef05b-101">Crear windows10TeamGeneralConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef05b-101">Create windows10TeamGeneralConfiguration</span></span>

> <span data-ttu-id="ef05b-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ef05b-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ef05b-103">Cree un objeto [windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="ef05b-103">Create a new [windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ef05b-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ef05b-104">Prerequisites</span></span>
<span data-ttu-id="ef05b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ef05b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ef05b-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ef05b-107">Permission type</span></span>|<span data-ttu-id="ef05b-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ef05b-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ef05b-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ef05b-109">Delegated (work or school account)</span></span>|<span data-ttu-id="ef05b-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ef05b-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="ef05b-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ef05b-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ef05b-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ef05b-112">Not supported.</span></span>|
|<span data-ttu-id="ef05b-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ef05b-113">Application</span></span>|<span data-ttu-id="ef05b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ef05b-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ef05b-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ef05b-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="ef05b-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ef05b-116">Request headers</span></span>
|<span data-ttu-id="ef05b-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef05b-117">Header</span></span>|<span data-ttu-id="ef05b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ef05b-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ef05b-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="ef05b-119">Authorization</span></span>|<span data-ttu-id="ef05b-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ef05b-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ef05b-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ef05b-121">Accept</span></span>|<span data-ttu-id="ef05b-122">application/json</span><span class="sxs-lookup"><span data-stu-id="ef05b-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ef05b-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ef05b-123">Request body</span></span>
<span data-ttu-id="ef05b-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto windows10TeamGeneralConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ef05b-124">In the request body, supply a JSON representation for the windows10TeamGeneralConfiguration object.</span></span>

<span data-ttu-id="ef05b-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windows10TeamGeneralConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ef05b-125">The following table shows the properties that are required when you create the windows10TeamGeneralConfiguration.</span></span>

|<span data-ttu-id="ef05b-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ef05b-126">Property</span></span>|<span data-ttu-id="ef05b-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="ef05b-127">Type</span></span>|<span data-ttu-id="ef05b-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef05b-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ef05b-129">id</span><span class="sxs-lookup"><span data-stu-id="ef05b-129">id</span></span>|<span data-ttu-id="ef05b-130">String</span><span class="sxs-lookup"><span data-stu-id="ef05b-130">String</span></span>|<span data-ttu-id="ef05b-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ef05b-131">Key of the entity.</span></span> <span data-ttu-id="ef05b-132">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ef05b-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ef05b-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="ef05b-133">lastModifiedDateTime</span></span>|<span data-ttu-id="ef05b-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ef05b-134">DateTimeOffset</span></span>|<span data-ttu-id="ef05b-135">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="ef05b-135">DateTime the object was last modified.</span></span> <span data-ttu-id="ef05b-136">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ef05b-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ef05b-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="ef05b-137">createdDateTime</span></span>|<span data-ttu-id="ef05b-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ef05b-138">DateTimeOffset</span></span>|<span data-ttu-id="ef05b-139">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="ef05b-139">DateTime the object was created.</span></span> <span data-ttu-id="ef05b-140">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ef05b-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ef05b-141">description</span><span class="sxs-lookup"><span data-stu-id="ef05b-141">description</span></span>|<span data-ttu-id="ef05b-142">String</span><span class="sxs-lookup"><span data-stu-id="ef05b-142">String</span></span>|<span data-ttu-id="ef05b-143">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ef05b-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="ef05b-144">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ef05b-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ef05b-145">displayName</span><span class="sxs-lookup"><span data-stu-id="ef05b-145">displayName</span></span>|<span data-ttu-id="ef05b-146">String</span><span class="sxs-lookup"><span data-stu-id="ef05b-146">String</span></span>|<span data-ttu-id="ef05b-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ef05b-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="ef05b-148">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ef05b-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ef05b-149">version</span><span class="sxs-lookup"><span data-stu-id="ef05b-149">version</span></span>|<span data-ttu-id="ef05b-150">Int32</span><span class="sxs-lookup"><span data-stu-id="ef05b-150">Int32</span></span>|<span data-ttu-id="ef05b-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ef05b-151">Version of the device configuration.</span></span> <span data-ttu-id="ef05b-152">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ef05b-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ef05b-153">azureOperationalInsightsBlockTelemetry</span><span class="sxs-lookup"><span data-stu-id="ef05b-153">azureOperationalInsightsBlockTelemetry</span></span>|<span data-ttu-id="ef05b-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="ef05b-154">Boolean</span></span>|<span data-ttu-id="ef05b-155">Indica si se va a bloquear Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="ef05b-155">Indicates whether or not to Block Azure Operational Insights.</span></span>|
|<span data-ttu-id="ef05b-156">azureOperationalInsightsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="ef05b-156">azureOperationalInsightsWorkspaceId</span></span>|<span data-ttu-id="ef05b-157">String</span><span class="sxs-lookup"><span data-stu-id="ef05b-157">String</span></span>|<span data-ttu-id="ef05b-158">Identificador del área de trabajo de Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="ef05b-158">The Azure Operational Insights workspace id.</span></span>|
|<span data-ttu-id="ef05b-159">azureOperationalInsightsWorkspaceKey</span><span class="sxs-lookup"><span data-stu-id="ef05b-159">azureOperationalInsightsWorkspaceKey</span></span>|<span data-ttu-id="ef05b-160">String</span><span class="sxs-lookup"><span data-stu-id="ef05b-160">String</span></span>|<span data-ttu-id="ef05b-161">Clave del área de trabajo de Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="ef05b-161">The Azure Operational Insights Workspace key.</span></span>|
|<span data-ttu-id="ef05b-162">connectAppBlockAutoLaunch</span><span class="sxs-lookup"><span data-stu-id="ef05b-162">connectAppBlockAutoLaunch</span></span>|<span data-ttu-id="ef05b-163">Booleano</span><span class="sxs-lookup"><span data-stu-id="ef05b-163">Boolean</span></span>|<span data-ttu-id="ef05b-164">Especifica si se iniciará automáticamente la aplicación Conectar cada vez que se inicie un proyecto.</span><span class="sxs-lookup"><span data-stu-id="ef05b-164">Specifies whether to automatically launch the Connect app whenever a projection is initiated.</span></span>|
|<span data-ttu-id="ef05b-165">maintenanceWindowBlocked</span><span class="sxs-lookup"><span data-stu-id="ef05b-165">maintenanceWindowBlocked</span></span>|<span data-ttu-id="ef05b-166">Booleano</span><span class="sxs-lookup"><span data-stu-id="ef05b-166">Boolean</span></span>|<span data-ttu-id="ef05b-167">Indica si se va a bloquear la configuración de un período de mantenimiento para las actualizaciones del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ef05b-167">Indicates whether or not to Block setting a maintenance window for device updates.</span></span>|
|<span data-ttu-id="ef05b-168">maintenanceWindowDurationInHours</span><span class="sxs-lookup"><span data-stu-id="ef05b-168">maintenanceWindowDurationInHours</span></span>|<span data-ttu-id="ef05b-169">Int32</span><span class="sxs-lookup"><span data-stu-id="ef05b-169">Int32</span></span>|<span data-ttu-id="ef05b-170">Duración del período de mantenimiento para las actualizaciones del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ef05b-170">Maintenance window duration for device updates.</span></span> <span data-ttu-id="ef05b-171">Valores válidos de 0 a 5</span><span class="sxs-lookup"><span data-stu-id="ef05b-171">Valid values 0 to 5</span></span>|
|<span data-ttu-id="ef05b-172">maintenanceWindowStartTime</span><span class="sxs-lookup"><span data-stu-id="ef05b-172">maintenanceWindowStartTime</span></span>|<span data-ttu-id="ef05b-173">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="ef05b-173">TimeOfDay</span></span>|<span data-ttu-id="ef05b-174">Hora de inicio del periodo de mantenimiento para las actualizaciones del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ef05b-174">Maintenance window start time for device updates.</span></span>|
|<span data-ttu-id="ef05b-175">miracastChannel</span><span class="sxs-lookup"><span data-stu-id="ef05b-175">miracastChannel</span></span>|[<span data-ttu-id="ef05b-176">miracastChannel</span><span class="sxs-lookup"><span data-stu-id="ef05b-176">miracastChannel</span></span>](../resources/intune_deviceconfig_miracastchannel.md)|<span data-ttu-id="ef05b-177">Canal.</span><span class="sxs-lookup"><span data-stu-id="ef05b-177">The channel.</span></span> <span data-ttu-id="ef05b-178">Los valores posibles son: `userDefined`, `one`, `two`, `three`, `four`, `five`, `six`, `seven`, `eight`, `nine`, `ten`, `eleven`, `thirtySix`, `forty`, `fortyFour`, `fortyEight`, `oneHundredFortyNine`, `oneHundredFiftyThree`, `oneHundredFiftySeven`, `oneHundredSixtyOne` y `oneHundredSixtyFive`.</span><span class="sxs-lookup"><span data-stu-id="ef05b-178">Possible values are: `userDefined`, `one`, `two`, `three`, `four`, `five`, `six`, `seven`, `eight`, `nine`, `ten`, `eleven`, `thirtySix`, `forty`, `fortyFour`, `fortyEight`, `oneHundredFortyNine`, `oneHundredFiftyThree`, `oneHundredFiftySeven`, `oneHundredSixtyOne`, `oneHundredSixtyFive`.</span></span>|
|<span data-ttu-id="ef05b-179">miracastBlocked</span><span class="sxs-lookup"><span data-stu-id="ef05b-179">miracastBlocked</span></span>|<span data-ttu-id="ef05b-180">Booleano</span><span class="sxs-lookup"><span data-stu-id="ef05b-180">Boolean</span></span>|<span data-ttu-id="ef05b-181">Indica si se van a bloquear las proyecciones inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="ef05b-181">Indicates whether or not to Block wireless projection.</span></span>|
|<span data-ttu-id="ef05b-182">miracastRequirePin</span><span class="sxs-lookup"><span data-stu-id="ef05b-182">miracastRequirePin</span></span>|<span data-ttu-id="ef05b-183">Booleano</span><span class="sxs-lookup"><span data-stu-id="ef05b-183">Boolean</span></span>|<span data-ttu-id="ef05b-184">Indica si se va a requerir un PIN para las proyecciones inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="ef05b-184">Indicates whether or not to require a pin for wireless projection.</span></span>|
|<span data-ttu-id="ef05b-185">settingsBlockMyMeetingsAndFiles</span><span class="sxs-lookup"><span data-stu-id="ef05b-185">settingsBlockMyMeetingsAndFiles</span></span>|<span data-ttu-id="ef05b-186">Booleano</span><span class="sxs-lookup"><span data-stu-id="ef05b-186">Boolean</span></span>|<span data-ttu-id="ef05b-187">Especifica si se deshabilita la característica "Mis reuniones y archivos" en el menú Inicio, que muestra las reuniones y los archivos del usuario que ha iniciado sesión en Office 365.</span><span class="sxs-lookup"><span data-stu-id="ef05b-187">Specifies whether to disable the "My meetings and files" feature in the Start menu, which shows the signed-in user's meetings and files from Office 365.</span></span>|
|<span data-ttu-id="ef05b-188">settingsBlockSessionResume</span><span class="sxs-lookup"><span data-stu-id="ef05b-188">settingsBlockSessionResume</span></span>|<span data-ttu-id="ef05b-189">Booleano</span><span class="sxs-lookup"><span data-stu-id="ef05b-189">Boolean</span></span>|<span data-ttu-id="ef05b-190">Especifica si se permite la posibilidad de reanudar una sesión cuando se agota el tiempo de espera de la sesión.</span><span class="sxs-lookup"><span data-stu-id="ef05b-190">Specifies whether to allow the ability to resume a session when the session times out.</span></span>|
|<span data-ttu-id="ef05b-191">settingsBlockSigninSuggestions</span><span class="sxs-lookup"><span data-stu-id="ef05b-191">settingsBlockSigninSuggestions</span></span>|<span data-ttu-id="ef05b-192">Booleano</span><span class="sxs-lookup"><span data-stu-id="ef05b-192">Boolean</span></span>|<span data-ttu-id="ef05b-193">Especifica si se deshabilita la opción de rellenar automáticamente el cuadro de diálogo de inicio de sesión con invitados de reuniones programadas.</span><span class="sxs-lookup"><span data-stu-id="ef05b-193">Specifies whether to disable auto-populating of the sign-in dialog with invitees from scheduled meetings.</span></span>|
|<span data-ttu-id="ef05b-194">settingsDefaultVolume</span><span class="sxs-lookup"><span data-stu-id="ef05b-194">settingsDefaultVolume</span></span>|<span data-ttu-id="ef05b-195">Int32</span><span class="sxs-lookup"><span data-stu-id="ef05b-195">Int32</span></span>|<span data-ttu-id="ef05b-196">Especifica el valor de volumen predeterminado para una nueva sesión.</span><span class="sxs-lookup"><span data-stu-id="ef05b-196">Specifies the default volume value for a new session.</span></span> <span data-ttu-id="ef05b-197">Los valores permitidos son de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="ef05b-197">Permitted values are 0-100.</span></span> <span data-ttu-id="ef05b-198">El valor predeterminado es 45.</span><span class="sxs-lookup"><span data-stu-id="ef05b-198">The default is 45.</span></span> <span data-ttu-id="ef05b-199">Valores válidos de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="ef05b-199">Valid values 0 to 100</span></span>|
|<span data-ttu-id="ef05b-200">settingsScreenTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ef05b-200">settingsScreenTimeoutInMinutes</span></span>|<span data-ttu-id="ef05b-201">Int32</span><span class="sxs-lookup"><span data-stu-id="ef05b-201">Int32</span></span>|<span data-ttu-id="ef05b-202">Especifica el número de minutos hasta que se desconecta la pantalla Concentrador.</span><span class="sxs-lookup"><span data-stu-id="ef05b-202">Specifies the number of minutes until the Hub screen turns off.</span></span>|
|<span data-ttu-id="ef05b-203">settingsSessionTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ef05b-203">settingsSessionTimeoutInMinutes</span></span>|<span data-ttu-id="ef05b-204">Int32</span><span class="sxs-lookup"><span data-stu-id="ef05b-204">Int32</span></span>|<span data-ttu-id="ef05b-205">Especifica el número de minutos hasta que se agota el tiempo de espera de la sesión.</span><span class="sxs-lookup"><span data-stu-id="ef05b-205">Specifies the number of minutes until the session times out.</span></span>|
|<span data-ttu-id="ef05b-206">settingsSleepTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ef05b-206">settingsSleepTimeoutInMinutes</span></span>|<span data-ttu-id="ef05b-207">Int32</span><span class="sxs-lookup"><span data-stu-id="ef05b-207">Int32</span></span>|<span data-ttu-id="ef05b-208">Especifica el número de minutos hasta que el concentrador entra en modo de suspensión.</span><span class="sxs-lookup"><span data-stu-id="ef05b-208">Specifies the number of minutes until the Hub enters sleep mode.</span></span>|
|<span data-ttu-id="ef05b-209">welcomeScreenBlockAutomaticWakeUp</span><span class="sxs-lookup"><span data-stu-id="ef05b-209">welcomeScreenBlockAutomaticWakeUp</span></span>|<span data-ttu-id="ef05b-210">Booleano</span><span class="sxs-lookup"><span data-stu-id="ef05b-210">Boolean</span></span>|<span data-ttu-id="ef05b-211">Indica si se va a impedir que la pantalla de inicio de sesión se reactive automáticamente cuando alguien entre en la sala.</span><span class="sxs-lookup"><span data-stu-id="ef05b-211">Indicates whether or not to Block the welcome screen from waking up automatically when someone enters the room.</span></span>|
|<span data-ttu-id="ef05b-212">welcomeScreenBackgroundImageUrl</span><span class="sxs-lookup"><span data-stu-id="ef05b-212">welcomeScreenBackgroundImageUrl</span></span>|<span data-ttu-id="ef05b-213">String</span><span class="sxs-lookup"><span data-stu-id="ef05b-213">String</span></span>|<span data-ttu-id="ef05b-214">Dirección URL de la imagen de fondo de la pantalla de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="ef05b-214">The welcome screen background image URL.</span></span> <span data-ttu-id="ef05b-215">La dirección URL debe utilizar el protocolo HTTPS y devolver una imagen PNG.</span><span class="sxs-lookup"><span data-stu-id="ef05b-215">The URL must use the HTTPS protocol and return a PNG image.</span></span>|
|<span data-ttu-id="ef05b-216">welcomeScreenMeetingInformation</span><span class="sxs-lookup"><span data-stu-id="ef05b-216">welcomeScreenMeetingInformation</span></span>|[<span data-ttu-id="ef05b-217">welcomeScreenMeetingInformation</span><span class="sxs-lookup"><span data-stu-id="ef05b-217">welcomeScreenMeetingInformation</span></span>](../resources/intune_deviceconfig_welcomescreenmeetinginformation.md)|<span data-ttu-id="ef05b-218">Información de la reunión que se muestra en la pantalla de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="ef05b-218">The welcome screen meeting information shown.</span></span> <span data-ttu-id="ef05b-219">Los valores posibles son: `userDefined`, `showOrganizerAndTimeOnly` y `showOrganizerAndTimeAndSubject`.</span><span class="sxs-lookup"><span data-stu-id="ef05b-219">Possible values are: `userDefined`, `showOrganizerAndTimeOnly`, `showOrganizerAndTimeAndSubject`.</span></span>|



## <a name="response"></a><span data-ttu-id="ef05b-220">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ef05b-220">Response</span></span>
<span data-ttu-id="ef05b-221">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ef05b-221">If successful, this method returns a `201 Created` response code and a [windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ef05b-222">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ef05b-222">Example</span></span>
### <a name="request"></a><span data-ttu-id="ef05b-223">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ef05b-223">Request</span></span>
<span data-ttu-id="ef05b-224">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ef05b-224">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 1150

{
  "@odata.type": "#microsoft.graph.windows10TeamGeneralConfiguration",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "azureOperationalInsightsBlockTelemetry": true,
  "azureOperationalInsightsWorkspaceId": "Azure Operational Insights Workspace Id value",
  "azureOperationalInsightsWorkspaceKey": "Azure Operational Insights Workspace Key value",
  "connectAppBlockAutoLaunch": true,
  "maintenanceWindowBlocked": true,
  "maintenanceWindowDurationInHours": 0,
  "maintenanceWindowStartTime": "11:59:09.3130000",
  "miracastChannel": "one",
  "miracastBlocked": true,
  "miracastRequirePin": true,
  "settingsBlockMyMeetingsAndFiles": true,
  "settingsBlockSessionResume": true,
  "settingsBlockSigninSuggestions": true,
  "settingsDefaultVolume": 5,
  "settingsScreenTimeoutInMinutes": 14,
  "settingsSessionTimeoutInMinutes": 15,
  "settingsSleepTimeoutInMinutes": 13,
  "welcomeScreenBlockAutomaticWakeUp": true,
  "welcomeScreenBackgroundImageUrl": "https://example.com/welcomeScreenBackgroundImageUrl/",
  "welcomeScreenMeetingInformation": "showOrganizerAndTimeOnly"
}
```

### <a name="response"></a><span data-ttu-id="ef05b-225">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ef05b-225">Response</span></span>
<span data-ttu-id="ef05b-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ef05b-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1322

{
  "@odata.type": "#microsoft.graph.windows10TeamGeneralConfiguration",
  "id": "0c94aa20-aa20-0c94-20aa-940c20aa940c",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "azureOperationalInsightsBlockTelemetry": true,
  "azureOperationalInsightsWorkspaceId": "Azure Operational Insights Workspace Id value",
  "azureOperationalInsightsWorkspaceKey": "Azure Operational Insights Workspace Key value",
  "connectAppBlockAutoLaunch": true,
  "maintenanceWindowBlocked": true,
  "maintenanceWindowDurationInHours": 0,
  "maintenanceWindowStartTime": "11:59:09.3130000",
  "miracastChannel": "one",
  "miracastBlocked": true,
  "miracastRequirePin": true,
  "settingsBlockMyMeetingsAndFiles": true,
  "settingsBlockSessionResume": true,
  "settingsBlockSigninSuggestions": true,
  "settingsDefaultVolume": 5,
  "settingsScreenTimeoutInMinutes": 14,
  "settingsSessionTimeoutInMinutes": 15,
  "settingsSleepTimeoutInMinutes": 13,
  "welcomeScreenBlockAutomaticWakeUp": true,
  "welcomeScreenBackgroundImageUrl": "https://example.com/welcomeScreenBackgroundImageUrl/",
  "welcomeScreenMeetingInformation": "showOrganizerAndTimeOnly"
}
```



