# <a name="create-manageddevice"></a><span data-ttu-id="3173e-101">Crear managedDevice</span><span class="sxs-lookup"><span data-stu-id="3173e-101">Create managedDevice</span></span>

> <span data-ttu-id="3173e-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3173e-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3173e-103">Crear un objeto [managedDevice](../resources/intune_devices_manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="3173e-103">Create a new [plannerBucket](../resources/intune_devices_manageddevice.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3173e-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3173e-104">Prerequisites</span></span>
<span data-ttu-id="3173e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="3173e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="3173e-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3173e-107">Permission type</span></span>|<span data-ttu-id="3173e-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3173e-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3173e-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3173e-109">Delegated (work or school account)</span></span>|<span data-ttu-id="3173e-110">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3173e-110">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="3173e-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3173e-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3173e-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3173e-112">Not supported.</span></span>|
|<span data-ttu-id="3173e-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3173e-113">Application</span></span>|<span data-ttu-id="3173e-114">No compatible.</span><span class="sxs-lookup"><span data-stu-id="3173e-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3173e-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3173e-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/managedDevices
POST /deviceManagement/managedDevices
POST /deviceManagement/detectedApps/{detectedAppId}/managedDevices
```

## <a name="request-headers"></a><span data-ttu-id="3173e-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3173e-116">Request headers</span></span>
|<span data-ttu-id="3173e-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3173e-117">Header</span></span>|<span data-ttu-id="3173e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3173e-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3173e-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="3173e-119">Authorization</span></span>|<span data-ttu-id="3173e-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3173e-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="3173e-121">Accept</span><span class="sxs-lookup"><span data-stu-id="3173e-121">Accept</span></span>|<span data-ttu-id="3173e-122">application/json</span><span class="sxs-lookup"><span data-stu-id="3173e-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3173e-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3173e-123">Request body</span></span>
<span data-ttu-id="3173e-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto managedDevice.</span><span class="sxs-lookup"><span data-stu-id="3173e-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="3173e-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto managedDevice.</span><span class="sxs-lookup"><span data-stu-id="3173e-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="3173e-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3173e-126">Property</span></span>|<span data-ttu-id="3173e-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="3173e-127">Type</span></span>|<span data-ttu-id="3173e-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="3173e-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3173e-129">id</span><span class="sxs-lookup"><span data-stu-id="3173e-129">id</span></span>|<span data-ttu-id="3173e-130">String</span><span class="sxs-lookup"><span data-stu-id="3173e-130">String</span></span>|<span data-ttu-id="3173e-131">Identificador único del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3173e-131">Unique Identifier for the device</span></span>|
|<span data-ttu-id="3173e-132">userId</span><span class="sxs-lookup"><span data-stu-id="3173e-132">userID</span></span>|<span data-ttu-id="3173e-133">String</span><span class="sxs-lookup"><span data-stu-id="3173e-133">String</span></span>|<span data-ttu-id="3173e-134">Identificador único del usuario asociado al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3173e-134">Unique Identifier for the user associated with the device</span></span>|
|<span data-ttu-id="3173e-135">deviceName</span><span class="sxs-lookup"><span data-stu-id="3173e-135">deviceName</span></span>|<span data-ttu-id="3173e-136">String</span><span class="sxs-lookup"><span data-stu-id="3173e-136">String</span></span>|<span data-ttu-id="3173e-137">Nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3173e-137">Name of the device</span></span>|
|<span data-ttu-id="3173e-138">deviceActionResults</span><span class="sxs-lookup"><span data-stu-id="3173e-138">deviceActionResults</span></span>|<span data-ttu-id="3173e-139">Colección [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="3173e-139">[deviceActionResult](../resources/intune_devices_deviceactionresult.md) collection</span></span>|<span data-ttu-id="3173e-140">Lista de objetos deviceActionResult ComplexType.</span><span class="sxs-lookup"><span data-stu-id="3173e-140">List of ComplexType deviceActionResult objects.</span></span>|
|<span data-ttu-id="3173e-141">enrolledDateTime</span><span class="sxs-lookup"><span data-stu-id="3173e-141">enrolledDateTime</span></span>|<span data-ttu-id="3173e-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3173e-142">DateTimeOffset</span></span>|<span data-ttu-id="3173e-143">Hora de inscripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3173e-143">Enrollment time of the device.</span></span>|
|<span data-ttu-id="3173e-144">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="3173e-144">lastSyncDateTime</span></span>|<span data-ttu-id="3173e-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3173e-145">DateTimeOffset</span></span>|<span data-ttu-id="3173e-146">Fecha y hora en que el dispositivo completó por última vez una sincronización correcta con Intune.</span><span class="sxs-lookup"><span data-stu-id="3173e-146">The date and time that the device last completed a successful sync with Intune.</span></span>|
|<span data-ttu-id="3173e-147">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="3173e-147">operatingSystem</span></span>|<span data-ttu-id="3173e-148">String</span><span class="sxs-lookup"><span data-stu-id="3173e-148">String</span></span>|<span data-ttu-id="3173e-149">Sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3173e-149">Operating system of the device.</span></span> <span data-ttu-id="3173e-150">Windows, iOS, etc.</span><span class="sxs-lookup"><span data-stu-id="3173e-150">Windows, iOS, etc.</span></span>|
|<span data-ttu-id="3173e-151">complianceState</span><span class="sxs-lookup"><span data-stu-id="3173e-151">complianceState</span></span>|<span data-ttu-id="3173e-152">String</span><span class="sxs-lookup"><span data-stu-id="3173e-152">String</span></span>|<span data-ttu-id="3173e-153">Estado de cumplimiento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3173e-153">Compliance state of the device.</span></span> <span data-ttu-id="3173e-154">Los valores posibles son: `unknown`, `compliant`, `noncompliant`, `conflict`, `error`, `inGracePeriod` y `configManager`.</span><span class="sxs-lookup"><span data-stu-id="3173e-154">Possible values are: `unknown`, `compliant`, `noncompliant`, `conflict`, `error`, `inGracePeriod`, `configManager`.</span></span>|
|<span data-ttu-id="3173e-155">jailBroken</span><span class="sxs-lookup"><span data-stu-id="3173e-155">jailBroken</span></span>|<span data-ttu-id="3173e-156">String</span><span class="sxs-lookup"><span data-stu-id="3173e-156">String</span></span>|<span data-ttu-id="3173e-157">Indica si se trata de un dispositivo con jailbreak o rooting.</span><span class="sxs-lookup"><span data-stu-id="3173e-157">whether the device is jail broken or rooted.</span></span>|
|<span data-ttu-id="3173e-158">managementAgent</span><span class="sxs-lookup"><span data-stu-id="3173e-158">managementAgent</span></span>|<span data-ttu-id="3173e-159">String</span><span class="sxs-lookup"><span data-stu-id="3173e-159">String</span></span>|<span data-ttu-id="3173e-160">Canal de administración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3173e-160">Management channel of the device.</span></span> <span data-ttu-id="3173e-161">Intune, EAS, etc. Los valores posibles son: `eas`, `mdm`, `easMdm`, `intuneClient`, `easIntuneClient`, `configurationManagerClient`, `configurationManagerClientMdm`, `configurationManagerClientMdmEas`, `unknown`, `jamf` y `googleCloudDevicePolicyController`.</span><span class="sxs-lookup"><span data-stu-id="3173e-161">Intune, EAS, etc. Possible values are: `eas`, `mdm`, `easMdm`, `intuneClient`, `easIntuneClient`, `configurationManagerClient`, `configurationManagerClientMdm`, `configurationManagerClientMdmEas`, `unknown`, `jamf`, `googleCloudDevicePolicyController`.</span></span>|
|<span data-ttu-id="3173e-162">osVersion</span><span class="sxs-lookup"><span data-stu-id="3173e-162">osVersion</span></span>|<span data-ttu-id="3173e-163">String</span><span class="sxs-lookup"><span data-stu-id="3173e-163">String</span></span>|<span data-ttu-id="3173e-164">Versión del sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3173e-164">Operating system version of the device.</span></span>|
|<span data-ttu-id="3173e-165">easActivated</span><span class="sxs-lookup"><span data-stu-id="3173e-165">easActivated</span></span>|<span data-ttu-id="3173e-166">Boolean</span><span class="sxs-lookup"><span data-stu-id="3173e-166">Boolean</span></span>|<span data-ttu-id="3173e-167">Indica si el dispositivo tiene Exchange ActiveSync activado.</span><span class="sxs-lookup"><span data-stu-id="3173e-167">Whether the device is Exchange ActiveSync activated.</span></span>|
|<span data-ttu-id="3173e-168">easDeviceId</span><span class="sxs-lookup"><span data-stu-id="3173e-168">easDeviceId</span></span>|<span data-ttu-id="3173e-169">String</span><span class="sxs-lookup"><span data-stu-id="3173e-169">String</span></span>|<span data-ttu-id="3173e-170">Identificador de Exchange ActiveSync del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3173e-170">Exchange ActiveSync Id of the device.</span></span>|
|<span data-ttu-id="3173e-171">easActivationDateTime</span><span class="sxs-lookup"><span data-stu-id="3173e-171">easActivationDateTime</span></span>|<span data-ttu-id="3173e-172">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3173e-172">DateTimeOffset</span></span>|<span data-ttu-id="3173e-173">Hora de activación de Exchange ActivationSync del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3173e-173">Exchange ActivationSync activation time of the device.</span></span>|
|<span data-ttu-id="3173e-174">azureADRegistered</span><span class="sxs-lookup"><span data-stu-id="3173e-174">azureADRegistered</span></span>|<span data-ttu-id="3173e-175">Boolean</span><span class="sxs-lookup"><span data-stu-id="3173e-175">Boolean</span></span>|<span data-ttu-id="3173e-176">Indica si el dispositivo está registrado en Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3173e-176">Whether the device is Azure Active Directory registered.</span></span>|
|<span data-ttu-id="3173e-177">deviceEnrollmentType</span><span class="sxs-lookup"><span data-stu-id="3173e-177">deviceEnrollmentType</span></span>|<span data-ttu-id="3173e-178">String</span><span class="sxs-lookup"><span data-stu-id="3173e-178">String</span></span>|<span data-ttu-id="3173e-179">Tipo de inscripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3173e-179">Enrollment type of the device.</span></span> <span data-ttu-id="3173e-180">Los valores posibles son: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin` y `windowsCoManagement`.</span><span class="sxs-lookup"><span data-stu-id="3173e-180">Possible values are: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin`, `windowsCoManagement`.</span></span>|
|<span data-ttu-id="3173e-181">activationLockBypassCode</span><span class="sxs-lookup"><span data-stu-id="3173e-181">activationLockBypassCode</span></span>|<span data-ttu-id="3173e-182">String</span><span class="sxs-lookup"><span data-stu-id="3173e-182">String</span></span>|<span data-ttu-id="3173e-183">Código que permite que se omita el bloqueo de activación en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3173e-183">Code that allows the Activation Lock on a device to be bypassed.</span></span>|
|<span data-ttu-id="3173e-184">emailAddress</span><span class="sxs-lookup"><span data-stu-id="3173e-184">emailAddress</span></span>|<span data-ttu-id="3173e-185">String</span><span class="sxs-lookup"><span data-stu-id="3173e-185">String</span></span>|<span data-ttu-id="3173e-186">Direcciones de correo electrónico del usuario asociado al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3173e-186">Email(s) for the user associated with the device</span></span>|
|<span data-ttu-id="3173e-187">azureADDeviceId</span><span class="sxs-lookup"><span data-stu-id="3173e-187">azureADDeviceId</span></span>|<span data-ttu-id="3173e-188">String</span><span class="sxs-lookup"><span data-stu-id="3173e-188">String</span></span>|<span data-ttu-id="3173e-189">Identificador único del dispositivo de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3173e-189">The unique identifier for the Azure Active Directory device.</span></span> <span data-ttu-id="3173e-190">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3173e-190">Read only.</span></span>|
|<span data-ttu-id="3173e-191">deviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="3173e-191">deviceRegistrationState</span></span>|<span data-ttu-id="3173e-192">String</span><span class="sxs-lookup"><span data-stu-id="3173e-192">String</span></span>|<span data-ttu-id="3173e-193">Estado de registro del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3173e-193">Device registration state.</span></span> <span data-ttu-id="3173e-194">Los valores posibles son: `notRegistered`, `registered`, `revoked`, `keyConflict`, `approvalPending`, `certificateReset`, `notRegisteredPendingEnrollment` y `unknown`.</span><span class="sxs-lookup"><span data-stu-id="3173e-194">Possible values are: `notRegistered`, `registered`, `revoked`, `keyConflict`, `approvalPending`, `certificateReset`, `notRegisteredPendingEnrollment`.</span></span>|
|<span data-ttu-id="3173e-195">deviceCategoryDisplayName</span><span class="sxs-lookup"><span data-stu-id="3173e-195">deviceCategoryDisplayName</span></span>|<span data-ttu-id="3173e-196">String</span><span class="sxs-lookup"><span data-stu-id="3173e-196">String</span></span>|<span data-ttu-id="3173e-197">Nombre para mostrar de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3173e-197">Device category display name</span></span>|
|<span data-ttu-id="3173e-198">isSupervised</span><span class="sxs-lookup"><span data-stu-id="3173e-198">isSupervised</span></span>|<span data-ttu-id="3173e-199">Boolean</span><span class="sxs-lookup"><span data-stu-id="3173e-199">Boolean</span></span>|<span data-ttu-id="3173e-200">Estado supervisado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3173e-200">Device supervised status</span></span>|
|<span data-ttu-id="3173e-201">exchangeLastSuccessfulSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="3173e-201">exchangeLastSuccessfulSyncDateTime</span></span>|<span data-ttu-id="3173e-202">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3173e-202">DateTimeOffset</span></span>|<span data-ttu-id="3173e-203">Última vez que el dispositivo contactó con Exchange.</span><span class="sxs-lookup"><span data-stu-id="3173e-203">Last time the device contacted Exchange.</span></span>|
|<span data-ttu-id="3173e-204">exchangeAccessState</span><span class="sxs-lookup"><span data-stu-id="3173e-204">exchangeAccessState</span></span>|<span data-ttu-id="3173e-205">String</span><span class="sxs-lookup"><span data-stu-id="3173e-205">String</span></span>|<span data-ttu-id="3173e-206">Estado de acceso del dispositivo en Exchange.</span><span class="sxs-lookup"><span data-stu-id="3173e-206">The Access State of the device in Exchange.</span></span> <span data-ttu-id="3173e-207">Los valores posibles son: `none`, `unknown`, `allowed`, `blocked` y `quarantined`.</span><span class="sxs-lookup"><span data-stu-id="3173e-207">Possible values are: `none`, `unknown`, `allowed`, `blocked`, `quarantined`.</span></span>|
|<span data-ttu-id="3173e-208">exchangeAccessStateReason</span><span class="sxs-lookup"><span data-stu-id="3173e-208">exchangeAccessStateReason</span></span>|<span data-ttu-id="3173e-209">String</span><span class="sxs-lookup"><span data-stu-id="3173e-209">String</span></span>|<span data-ttu-id="3173e-210">Motivo del estado de acceso del dispositivo en Exchange.</span><span class="sxs-lookup"><span data-stu-id="3173e-210">The reason for the device's access state in Exchange.</span></span> <span data-ttu-id="3173e-211">Los valores posibles son: `none`, `unknown`, `exchangeGlobalRule`, `exchangeIndividualRule`, `exchangeDeviceRule`, `exchangeUpgrade`, `exchangeMailboxPolicy`, `other`, `compliant`, `notCompliant`, `notEnrolled`, `unknownLocation`, `mfaRequired`, `azureADBlockDueToAccessPolicy`, `compromisedPassword` y `deviceNotKnownWithManagedApp`.</span><span class="sxs-lookup"><span data-stu-id="3173e-211">Possible values are: `none`, `unknown`, `exchangeGlobalRule`, `exchangeIndividualRule`, `exchangeDeviceRule`, `exchangeUpgrade`, `exchangeMailboxPolicy`, `other`, `compliant`, `notCompliant`, `notEnrolled`, `unknownLocation`, `mfaRequired`, `azureADBlockDueToAccessPolicy`, `compromisedPassword`, `deviceNotKnownWithManagedApp`.</span></span>|
|<span data-ttu-id="3173e-212">remoteAssistanceSessionUrl</span><span class="sxs-lookup"><span data-stu-id="3173e-212">remoteAssistanceSessionUrl</span></span>|<span data-ttu-id="3173e-213">String</span><span class="sxs-lookup"><span data-stu-id="3173e-213">String</span></span>|<span data-ttu-id="3173e-214">Dirección URL que permite que se establezca una sesión remota con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3173e-214">Url that allows a Remote Assistance session to be established with the device.</span></span>|
|<span data-ttu-id="3173e-215">remoteAssistanceSessionErrorDetails</span><span class="sxs-lookup"><span data-stu-id="3173e-215">remoteAssistanceSessionErrorDetails</span></span>|<span data-ttu-id="3173e-216">String</span><span class="sxs-lookup"><span data-stu-id="3173e-216">String</span></span>|<span data-ttu-id="3173e-217">Cadena de error que identifica los problemas al crear objetos de la sesión de asistencia remota.</span><span class="sxs-lookup"><span data-stu-id="3173e-217">An error string that identifies issues when creating Remote Assistance session objects.</span></span>|
|<span data-ttu-id="3173e-218">isEncrypted</span><span class="sxs-lookup"><span data-stu-id="3173e-218">isEncrypted</span></span>|<span data-ttu-id="3173e-219">Boolean</span><span class="sxs-lookup"><span data-stu-id="3173e-219">Boolean</span></span>|<span data-ttu-id="3173e-220">Estado del cifrado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3173e-220">Device encryption status</span></span>|
|<span data-ttu-id="3173e-221">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="3173e-221">userPrincipalName</span></span>|<span data-ttu-id="3173e-222">String</span><span class="sxs-lookup"><span data-stu-id="3173e-222">String</span></span>|<span data-ttu-id="3173e-223">Nombre principal de usuario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3173e-223">Device user principal name</span></span>|
|<span data-ttu-id="3173e-224">model</span><span class="sxs-lookup"><span data-stu-id="3173e-224">model</span></span>|<span data-ttu-id="3173e-225">String</span><span class="sxs-lookup"><span data-stu-id="3173e-225">String</span></span>|<span data-ttu-id="3173e-226">Modelo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3173e-226">Model of the device</span></span>|
|<span data-ttu-id="3173e-227">manufacturer</span><span class="sxs-lookup"><span data-stu-id="3173e-227">Camera manufacturer.</span></span>|<span data-ttu-id="3173e-228">String</span><span class="sxs-lookup"><span data-stu-id="3173e-228">String</span></span>|<span data-ttu-id="3173e-229">Fabricante del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3173e-229">Manufacturer of the device</span></span>|
|<span data-ttu-id="3173e-230">imei</span><span class="sxs-lookup"><span data-stu-id="3173e-230">imei</span></span>|<span data-ttu-id="3173e-231">String</span><span class="sxs-lookup"><span data-stu-id="3173e-231">String</span></span>|<span data-ttu-id="3173e-232">IMEI</span><span class="sxs-lookup"><span data-stu-id="3173e-232">IMEI</span></span>|
|<span data-ttu-id="3173e-233">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="3173e-233">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="3173e-234">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3173e-234">DateTimeOffset</span></span>|<span data-ttu-id="3173e-235">Fecha y hora en que expira el período de gracia de cumplimiento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3173e-235">The DateTime when device compliance grace period expires</span></span>|
|<span data-ttu-id="3173e-236">serialNumber</span><span class="sxs-lookup"><span data-stu-id="3173e-236">serialNumber</span></span>|<span data-ttu-id="3173e-237">String</span><span class="sxs-lookup"><span data-stu-id="3173e-237">String</span></span>|<span data-ttu-id="3173e-238">Número de serie.</span><span class="sxs-lookup"><span data-stu-id="3173e-238">SerialNumber Property</span></span>|
|<span data-ttu-id="3173e-239">phoneNumber</span><span class="sxs-lookup"><span data-stu-id="3173e-239">PhoneNumber</span></span>|<span data-ttu-id="3173e-240">String</span><span class="sxs-lookup"><span data-stu-id="3173e-240">String</span></span>|<span data-ttu-id="3173e-241">Número de teléfono del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3173e-241">Phone number of the device</span></span>|
|<span data-ttu-id="3173e-242">androidSecurityPatchLevel</span><span class="sxs-lookup"><span data-stu-id="3173e-242">androidSecurityPatchLevel</span></span>|<span data-ttu-id="3173e-243">String</span><span class="sxs-lookup"><span data-stu-id="3173e-243">String</span></span>|<span data-ttu-id="3173e-244">Nivel de revisión de seguridad de Android.</span><span class="sxs-lookup"><span data-stu-id="3173e-244">Android security patch level</span></span>|
|<span data-ttu-id="3173e-245">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="3173e-245">userDisplayName</span></span>|<span data-ttu-id="3173e-246">String</span><span class="sxs-lookup"><span data-stu-id="3173e-246">String</span></span>|<span data-ttu-id="3173e-247">Nombre para mostrar del usuario.</span><span class="sxs-lookup"><span data-stu-id="3173e-247">user display name</span></span>|
|<span data-ttu-id="3173e-248">configurationManagerClientEnabledFeatures</span><span class="sxs-lookup"><span data-stu-id="3173e-248">configurationManagerClientEnabledFeatures</span></span>|[<span data-ttu-id="3173e-249">configurationManagerClientEnabledFeatures</span><span class="sxs-lookup"><span data-stu-id="3173e-249">configurationManagerClientEnabledFeatures</span></span>](../resources/intune_devices_configurationmanagerclientenabledfeatures.md)|<span data-ttu-id="3173e-250">Características activadas del cliente ConfigrMgr.</span><span class="sxs-lookup"><span data-stu-id="3173e-250">ConfigrMgr client enabled features</span></span>|
|<span data-ttu-id="3173e-251">wiFiMacAddress</span><span class="sxs-lookup"><span data-stu-id="3173e-251">wiFiMacAddress</span></span>|<span data-ttu-id="3173e-252">String</span><span class="sxs-lookup"><span data-stu-id="3173e-252">String</span></span>|<span data-ttu-id="3173e-253">MAC de Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="3173e-253">Wi-Fi MAC</span></span>|
|<span data-ttu-id="3173e-254">deviceHealthAttestationState</span><span class="sxs-lookup"><span data-stu-id="3173e-254">deviceHealthAttestationState</span></span>|[<span data-ttu-id="3173e-255">deviceHealthAttestationState</span><span class="sxs-lookup"><span data-stu-id="3173e-255">deviceHealthAttestationState</span></span>](../resources/intune_devices_devicehealthattestationstate.md)|<span data-ttu-id="3173e-256">Estado de la atestación de estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3173e-256">The device health attestation state.</span></span>|
|<span data-ttu-id="3173e-257">subscriberCarrier</span><span class="sxs-lookup"><span data-stu-id="3173e-257">subscriberCarrier</span></span>|<span data-ttu-id="3173e-258">String</span><span class="sxs-lookup"><span data-stu-id="3173e-258">String</span></span>|<span data-ttu-id="3173e-259">Operador del suscriptor.</span><span class="sxs-lookup"><span data-stu-id="3173e-259">Subscriber Carrier</span></span>|
|<span data-ttu-id="3173e-260">meid</span><span class="sxs-lookup"><span data-stu-id="3173e-260">meid</span></span>|<span data-ttu-id="3173e-261">String</span><span class="sxs-lookup"><span data-stu-id="3173e-261">String</span></span>|<span data-ttu-id="3173e-262">MEID.</span><span class="sxs-lookup"><span data-stu-id="3173e-262">MEID</span></span>|
|<span data-ttu-id="3173e-263">totalStorageSpaceInBytes</span><span class="sxs-lookup"><span data-stu-id="3173e-263">totalStorageSpaceInBytes</span></span>|<span data-ttu-id="3173e-264">Int64</span><span class="sxs-lookup"><span data-stu-id="3173e-264">Int64</span></span>|<span data-ttu-id="3173e-265">Almacenamiento total en bytes.</span><span class="sxs-lookup"><span data-stu-id="3173e-265">Total Storage in Bytes</span></span>|
|<span data-ttu-id="3173e-266">freeStorageSpaceInBytes</span><span class="sxs-lookup"><span data-stu-id="3173e-266">freeStorageSpaceInBytes</span></span>|<span data-ttu-id="3173e-267">Int64</span><span class="sxs-lookup"><span data-stu-id="3173e-267">Int64</span></span>|<span data-ttu-id="3173e-268">Almacenamiento disponible en bytes.</span><span class="sxs-lookup"><span data-stu-id="3173e-268">Free Storage in Bytes</span></span>|
|<span data-ttu-id="3173e-269">managedDeviceName</span><span class="sxs-lookup"><span data-stu-id="3173e-269">managedDeviceName</span></span>|<span data-ttu-id="3173e-270">String</span><span class="sxs-lookup"><span data-stu-id="3173e-270">String</span></span>|<span data-ttu-id="3173e-271">Nombre generado automáticamente para identificar un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3173e-271">Automatically generated name to identify a device.</span></span> <span data-ttu-id="3173e-272">Se puede sobrescribir con un nombre descriptivo del usuario.</span><span class="sxs-lookup"><span data-stu-id="3173e-272">Can be overwritten to a user friendly name.</span></span>|
|<span data-ttu-id="3173e-273">partnerReportedThreatState</span><span class="sxs-lookup"><span data-stu-id="3173e-273">partnerReportedThreatState</span></span>|<span data-ttu-id="3173e-274">String</span><span class="sxs-lookup"><span data-stu-id="3173e-274">String</span></span>|<span data-ttu-id="3173e-275">Indica el estado de amenazas de un dispositivo cuando la cuenta y el dispositivo usan un partner de Mobile Threat Defense.</span><span class="sxs-lookup"><span data-stu-id="3173e-275">Indicates the threat state of a device when a Mobile Threat Defense partner is in use by the account and device.</span></span> <span data-ttu-id="3173e-276">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3173e-276">Read only.</span></span> <span data-ttu-id="3173e-277">Los valores posibles son: `unknown`, `activated`, `deactivated`, `secured`, `lowSeverity`, `mediumSeverity`, `highSeverity` y `unresponsive`.</span><span class="sxs-lookup"><span data-stu-id="3173e-277">Possible values are: `unknown`, `activated`, `deactivated`, `secured`, `lowSeverity`, `mediumSeverity`, `highSeverity`.</span></span>|



## <a name="response"></a><span data-ttu-id="3173e-278">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3173e-278">Response</span></span>
<span data-ttu-id="3173e-279">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [managedDevice](../resources/intune_devices_manageddevice.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3173e-279">If successful, this method returns a `201 Created` response code and a [ListItemVersion](../resources/intune_devices_manageddevice.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3173e-280">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3173e-280">Example</span></span>
### <a name="request"></a><span data-ttu-id="3173e-281">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3173e-281">Request</span></span>
<span data-ttu-id="3173e-282">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3173e-282">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/users/{usersId}/managedDevices
Content-type: application/json
Content-length: 4616

{
  "@odata.type": "#microsoft.graph.managedDevice",
  "userId": "User Id value",
  "deviceName": "Device Name value",
  "deviceActionResults": [
    {
      "@odata.type": "microsoft.graph.deviceActionResult",
      "actionName": "Action Name value",
      "actionState": "pending",
      "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
      "lastUpdatedDateTime": "2017-01-01T00:00:56.8321556-08:00"
    }
  ],
  "enrolledDateTime": "2016-12-31T23:59:43.797191-08:00",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "operatingSystem": "Operating System value",
  "complianceState": "compliant",
  "jailBroken": "Jail Broken value",
  "managementAgent": "mdm",
  "osVersion": "Os Version value",
  "easActivated": true,
  "easDeviceId": "Eas Device Id value",
  "easActivationDateTime": "2016-12-31T23:59:43.4878784-08:00",
  "azureADRegistered": true,
  "deviceEnrollmentType": "userEnrollment",
  "activationLockBypassCode": "Activation Lock Bypass Code value",
  "emailAddress": "Email Address value",
  "azureADDeviceId": "Azure ADDevice Id value",
  "deviceRegistrationState": "registered",
  "deviceCategoryDisplayName": "Device Category Display Name value",
  "isSupervised": true,
  "exchangeLastSuccessfulSyncDateTime": "2017-01-01T00:00:45.8803083-08:00",
  "exchangeAccessState": "unknown",
  "exchangeAccessStateReason": "unknown",
  "remoteAssistanceSessionUrl": "https://example.com/remoteAssistanceSessionUrl/",
  "remoteAssistanceSessionErrorDetails": "Remote Assistance Session Error Details value",
  "isEncrypted": true,
  "userPrincipalName": "User Principal Name value",
  "model": "Model value",
  "manufacturer": "Manufacturer value",
  "imei": "Imei value",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
  "serialNumber": "Serial Number value",
  "phoneNumber": "Phone Number value",
  "androidSecurityPatchLevel": "Android Security Patch Level value",
  "userDisplayName": "User Display Name value",
  "configurationManagerClientEnabledFeatures": {
    "@odata.type": "microsoft.graph.configurationManagerClientEnabledFeatures",
    "inventory": true,
    "modernApps": true,
    "resourceAccess": true,
    "deviceConfiguration": true,
    "compliancePolicy": true,
    "windowsUpdateForBusiness": true
  },
  "wiFiMacAddress": "Wi Fi Mac Address value",
  "deviceHealthAttestationState": {
    "@odata.type": "microsoft.graph.deviceHealthAttestationState",
    "lastUpdateDateTime": "Last Update Date Time value",
    "contentNamespaceUrl": "https://example.com/contentNamespaceUrl/",
    "deviceHealthAttestationStatus": "Device Health Attestation Status value",
    "contentVersion": "Content Version value",
    "issuedDateTime": "2016-12-31T23:58:22.1231038-08:00",
    "attestationIdentityKey": "Attestation Identity Key value",
    "resetCount": 10,
    "restartCount": 12,
    "dataExcutionPolicy": "Data Excution Policy value",
    "bitLockerStatus": "Bit Locker Status value",
    "bootManagerVersion": "Boot Manager Version value",
    "codeIntegrityCheckVersion": "Code Integrity Check Version value",
    "secureBoot": "Secure Boot value",
    "bootDebugging": "Boot Debugging value",
    "operatingSystemKernelDebugging": "Operating System Kernel Debugging value",
    "codeIntegrity": "Code Integrity value",
    "testSigning": "Test Signing value",
    "safeMode": "Safe Mode value",
    "windowsPE": "Windows PE value",
    "earlyLaunchAntiMalwareDriverProtection": "Early Launch Anti Malware Driver Protection value",
    "virtualSecureMode": "Virtual Secure Mode value",
    "pcrHashAlgorithm": "Pcr Hash Algorithm value",
    "bootAppSecurityVersion": "Boot App Security Version value",
    "bootManagerSecurityVersion": "Boot Manager Security Version value",
    "tpmVersion": "Tpm Version value",
    "pcr0": "Pcr0 value",
    "secureBootConfigurationPolicyFingerPrint": "Secure Boot Configuration Policy Finger Print value",
    "codeIntegrityPolicy": "Code Integrity Policy value",
    "bootRevisionListInfo": "Boot Revision List Info value",
    "operatingSystemRevListInfo": "Operating System Rev List Info value",
    "healthStatusMismatchInfo": "Health Status Mismatch Info value",
    "healthAttestationSupportedStatus": "Health Attestation Supported Status value"
  },
  "subscriberCarrier": "Subscriber Carrier value",
  "meid": "Meid value",
  "totalStorageSpaceInBytes": 8,
  "freeStorageSpaceInBytes": 7,
  "managedDeviceName": "Managed Device Name value",
  "partnerReportedThreatState": "activated"
}
```

### <a name="response"></a><span data-ttu-id="3173e-283">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3173e-283">Response</span></span>
<span data-ttu-id="3173e-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3173e-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 4665

{
  "@odata.type": "#microsoft.graph.managedDevice",
  "id": "705c034c-034c-705c-4c03-5c704c035c70",
  "userId": "User Id value",
  "deviceName": "Device Name value",
  "deviceActionResults": [
    {
      "@odata.type": "microsoft.graph.deviceActionResult",
      "actionName": "Action Name value",
      "actionState": "pending",
      "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
      "lastUpdatedDateTime": "2017-01-01T00:00:56.8321556-08:00"
    }
  ],
  "enrolledDateTime": "2016-12-31T23:59:43.797191-08:00",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "operatingSystem": "Operating System value",
  "complianceState": "compliant",
  "jailBroken": "Jail Broken value",
  "managementAgent": "mdm",
  "osVersion": "Os Version value",
  "easActivated": true,
  "easDeviceId": "Eas Device Id value",
  "easActivationDateTime": "2016-12-31T23:59:43.4878784-08:00",
  "azureADRegistered": true,
  "deviceEnrollmentType": "userEnrollment",
  "activationLockBypassCode": "Activation Lock Bypass Code value",
  "emailAddress": "Email Address value",
  "azureADDeviceId": "Azure ADDevice Id value",
  "deviceRegistrationState": "registered",
  "deviceCategoryDisplayName": "Device Category Display Name value",
  "isSupervised": true,
  "exchangeLastSuccessfulSyncDateTime": "2017-01-01T00:00:45.8803083-08:00",
  "exchangeAccessState": "unknown",
  "exchangeAccessStateReason": "unknown",
  "remoteAssistanceSessionUrl": "https://example.com/remoteAssistanceSessionUrl/",
  "remoteAssistanceSessionErrorDetails": "Remote Assistance Session Error Details value",
  "isEncrypted": true,
  "userPrincipalName": "User Principal Name value",
  "model": "Model value",
  "manufacturer": "Manufacturer value",
  "imei": "Imei value",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
  "serialNumber": "Serial Number value",
  "phoneNumber": "Phone Number value",
  "androidSecurityPatchLevel": "Android Security Patch Level value",
  "userDisplayName": "User Display Name value",
  "configurationManagerClientEnabledFeatures": {
    "@odata.type": "microsoft.graph.configurationManagerClientEnabledFeatures",
    "inventory": true,
    "modernApps": true,
    "resourceAccess": true,
    "deviceConfiguration": true,
    "compliancePolicy": true,
    "windowsUpdateForBusiness": true
  },
  "wiFiMacAddress": "Wi Fi Mac Address value",
  "deviceHealthAttestationState": {
    "@odata.type": "microsoft.graph.deviceHealthAttestationState",
    "lastUpdateDateTime": "Last Update Date Time value",
    "contentNamespaceUrl": "https://example.com/contentNamespaceUrl/",
    "deviceHealthAttestationStatus": "Device Health Attestation Status value",
    "contentVersion": "Content Version value",
    "issuedDateTime": "2016-12-31T23:58:22.1231038-08:00",
    "attestationIdentityKey": "Attestation Identity Key value",
    "resetCount": 10,
    "restartCount": 12,
    "dataExcutionPolicy": "Data Excution Policy value",
    "bitLockerStatus": "Bit Locker Status value",
    "bootManagerVersion": "Boot Manager Version value",
    "codeIntegrityCheckVersion": "Code Integrity Check Version value",
    "secureBoot": "Secure Boot value",
    "bootDebugging": "Boot Debugging value",
    "operatingSystemKernelDebugging": "Operating System Kernel Debugging value",
    "codeIntegrity": "Code Integrity value",
    "testSigning": "Test Signing value",
    "safeMode": "Safe Mode value",
    "windowsPE": "Windows PE value",
    "earlyLaunchAntiMalwareDriverProtection": "Early Launch Anti Malware Driver Protection value",
    "virtualSecureMode": "Virtual Secure Mode value",
    "pcrHashAlgorithm": "Pcr Hash Algorithm value",
    "bootAppSecurityVersion": "Boot App Security Version value",
    "bootManagerSecurityVersion": "Boot Manager Security Version value",
    "tpmVersion": "Tpm Version value",
    "pcr0": "Pcr0 value",
    "secureBootConfigurationPolicyFingerPrint": "Secure Boot Configuration Policy Finger Print value",
    "codeIntegrityPolicy": "Code Integrity Policy value",
    "bootRevisionListInfo": "Boot Revision List Info value",
    "operatingSystemRevListInfo": "Operating System Rev List Info value",
    "healthStatusMismatchInfo": "Health Status Mismatch Info value",
    "healthAttestationSupportedStatus": "Health Attestation Supported Status value"
  },
  "subscriberCarrier": "Subscriber Carrier value",
  "meid": "Meid value",
  "totalStorageSpaceInBytes": 8,
  "freeStorageSpaceInBytes": 7,
  "managedDeviceName": "Managed Device Name value",
  "partnerReportedThreatState": "activated"
}
```



