# <a name="create-manageddevice"></a><span data-ttu-id="e671f-101">Crear managedDevice</span><span class="sxs-lookup"><span data-stu-id="e671f-101">Create managedDevice</span></span>

> <span data-ttu-id="e671f-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e671f-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e671f-103">Crear un objeto [managedDevice](../resources/intune_devices_manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="e671f-103">Create a new [managedDevice](../resources/intune_devices_manageddevice.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e671f-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e671f-104">Prerequisites</span></span>
<span data-ttu-id="e671f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e671f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e671f-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e671f-107">Permission type</span></span>|<span data-ttu-id="e671f-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e671f-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e671f-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e671f-109">Delegated (work or school account)</span></span>|<span data-ttu-id="e671f-110">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e671f-110">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="e671f-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e671f-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e671f-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e671f-112">Not supported.</span></span>|
|<span data-ttu-id="e671f-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e671f-113">Application</span></span>|<span data-ttu-id="e671f-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e671f-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e671f-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e671f-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/managedDevices
POST /deviceManagement/managedDevices
POST /deviceManagement/detectedApps/{detectedAppId}/managedDevices
```

## <a name="request-headers"></a><span data-ttu-id="e671f-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e671f-116">Request headers</span></span>
|<span data-ttu-id="e671f-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e671f-117">Header</span></span>|<span data-ttu-id="e671f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e671f-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e671f-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="e671f-119">Authorization</span></span>|<span data-ttu-id="e671f-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e671f-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e671f-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e671f-121">Accept</span></span>|<span data-ttu-id="e671f-122">application/json</span><span class="sxs-lookup"><span data-stu-id="e671f-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e671f-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e671f-123">Request body</span></span>
<span data-ttu-id="e671f-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto managedDevice.</span><span class="sxs-lookup"><span data-stu-id="e671f-124">In the request body, supply a JSON representation for the managedDevice object.</span></span>

<span data-ttu-id="e671f-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto managedDevice.</span><span class="sxs-lookup"><span data-stu-id="e671f-125">The following table shows the properties that are required when you create the managedDevice.</span></span>

|<span data-ttu-id="e671f-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e671f-126">Property</span></span>|<span data-ttu-id="e671f-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="e671f-127">Type</span></span>|<span data-ttu-id="e671f-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="e671f-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e671f-129">id.</span><span class="sxs-lookup"><span data-stu-id="e671f-129">id</span></span>|<span data-ttu-id="e671f-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="e671f-130">String</span></span>|<span data-ttu-id="e671f-131">Identificador único del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e671f-131">Unique Identifier for the device</span></span>|
|<span data-ttu-id="e671f-132">userId</span><span class="sxs-lookup"><span data-stu-id="e671f-132">userId</span></span>|<span data-ttu-id="e671f-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="e671f-133">String</span></span>|<span data-ttu-id="e671f-134">Identificador único del usuario asociado al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e671f-134">Unique Identifier for the user associated with the device</span></span>|
|<span data-ttu-id="e671f-135">deviceName</span><span class="sxs-lookup"><span data-stu-id="e671f-135">deviceName</span></span>|<span data-ttu-id="e671f-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="e671f-136">String</span></span>|<span data-ttu-id="e671f-137">Nombre del dispositivo</span><span class="sxs-lookup"><span data-stu-id="e671f-137">Name of the device</span></span>|
|<span data-ttu-id="e671f-138">managedDeviceOwnerType</span><span class="sxs-lookup"><span data-stu-id="e671f-138">managedDeviceOwnerType</span></span>|[<span data-ttu-id="e671f-139">managedDeviceOwnerType</span><span class="sxs-lookup"><span data-stu-id="e671f-139">managedDeviceOwnerType</span></span>](../resources/intune_devices_manageddeviceownertype.md)|<span data-ttu-id="e671f-p102">Propietario del dispositivo. Puede ser 'compañía' o 'personal'. Los valores posibles son: `unknown`, `company`, `personal`.</span><span class="sxs-lookup"><span data-stu-id="e671f-p102">Ownership of the device. Can be 'company' or 'personal'. The possible values are: `unknown`, `company`, `personal`.</span></span>|
|<span data-ttu-id="e671f-143">deviceActionResults</span><span class="sxs-lookup"><span data-stu-id="e671f-143">deviceActionResults</span></span>|<span data-ttu-id="e671f-144">Colección [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="e671f-144">[deviceActionResult](../resources/intune_devices_deviceactionresult.md) collection</span></span>|<span data-ttu-id="e671f-145">Lista de objetos deviceActionResult ComplexType.</span><span class="sxs-lookup"><span data-stu-id="e671f-145">List of ComplexType deviceActionResult objects.</span></span>|
|<span data-ttu-id="e671f-146">enrolledDateTime</span><span class="sxs-lookup"><span data-stu-id="e671f-146">enrolledDateTime</span></span>|<span data-ttu-id="e671f-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e671f-147">DateTimeOffset</span></span>|<span data-ttu-id="e671f-148">Hora de inscripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e671f-148">Enrollment time of the device.</span></span>|
|<span data-ttu-id="e671f-149">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="e671f-149">lastSyncDateTime</span></span>|<span data-ttu-id="e671f-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e671f-150">DateTimeOffset</span></span>|<span data-ttu-id="e671f-151">Fecha y hora en que el dispositivo completó por última vez una sincronización correcta con Intune.</span><span class="sxs-lookup"><span data-stu-id="e671f-151">The date and time that the device last completed a successful sync with Intune.</span></span>|
|<span data-ttu-id="e671f-152">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="e671f-152">operatingSystem</span></span>|<span data-ttu-id="e671f-153">Cadena</span><span class="sxs-lookup"><span data-stu-id="e671f-153">String</span></span>|<span data-ttu-id="e671f-154">Sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e671f-154">Operating system of the device.</span></span> <span data-ttu-id="e671f-155">Windows, iOS, etc.</span><span class="sxs-lookup"><span data-stu-id="e671f-155">Windows, iOS, etc.</span></span>|
|<span data-ttu-id="e671f-156">complianceState</span><span class="sxs-lookup"><span data-stu-id="e671f-156">complianceState</span></span>|[<span data-ttu-id="e671f-157">complianceState</span><span class="sxs-lookup"><span data-stu-id="e671f-157">complianceState</span></span>](../resources/intune_devices_compliancestate.md)|<span data-ttu-id="e671f-p104">Estado de cumplimiento del dispositivo. Los valores posibles son: `unknown`, `compliant`, `noncompliant`, `conflict`, `error`, `inGracePeriod`, `configManager`.</span><span class="sxs-lookup"><span data-stu-id="e671f-p104">Compliance state of the device. The possible values are: `unknown`, `compliant`, `noncompliant`, `conflict`, `error`, `inGracePeriod`, `configManager`.</span></span>|
|<span data-ttu-id="e671f-160">jailBroken</span><span class="sxs-lookup"><span data-stu-id="e671f-160">jailBroken</span></span>|<span data-ttu-id="e671f-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="e671f-161">String</span></span>|<span data-ttu-id="e671f-162">Indica si se trata de un dispositivo liberado o con permisos elevados.</span><span class="sxs-lookup"><span data-stu-id="e671f-162">whether the device is jail broken or rooted.</span></span>|
|<span data-ttu-id="e671f-163">managementAgent</span><span class="sxs-lookup"><span data-stu-id="e671f-163">managementAgent</span></span>|[<span data-ttu-id="e671f-164">managementAgentType</span><span class="sxs-lookup"><span data-stu-id="e671f-164">managementAgentType</span></span>](../resources/intune_devices_managementagenttype.md)|<span data-ttu-id="e671f-p105">Canal de gestión del dispositivo. Intune, EAS, etc. Los valores posibles son: `eas`, `mdm`, `easMdm`, `intuneClient`, `easIntuneClient`, `configurationManagerClient`, `configurationManagerClientMdm`, `configurationManagerClientMdmEas`, `unknown`, `jamf`, `googleCloudDevicePolicyController`.</span><span class="sxs-lookup"><span data-stu-id="e671f-p105">Management channel of the device. Intune, EAS, etc. The possible values are: `eas`, `mdm`, `easMdm`, `intuneClient`, `easIntuneClient`, `configurationManagerClient`, `configurationManagerClientMdm`, `configurationManagerClientMdmEas`, `unknown`, `jamf`, `googleCloudDevicePolicyController`.</span></span>|
|<span data-ttu-id="e671f-167">osVersion</span><span class="sxs-lookup"><span data-stu-id="e671f-167">osVersion</span></span>|<span data-ttu-id="e671f-168">Cadena</span><span class="sxs-lookup"><span data-stu-id="e671f-168">String</span></span>|<span data-ttu-id="e671f-169">Versión del sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e671f-169">Operating system version of the device.</span></span>|
|<span data-ttu-id="e671f-170">easActivated</span><span class="sxs-lookup"><span data-stu-id="e671f-170">easActivated</span></span>|<span data-ttu-id="e671f-171">Booleano</span><span class="sxs-lookup"><span data-stu-id="e671f-171">Boolean</span></span>|<span data-ttu-id="e671f-172">Indica si el dispositivo tiene Exchange ActiveSync activado.</span><span class="sxs-lookup"><span data-stu-id="e671f-172">Whether the device is Exchange ActiveSync activated.</span></span>|
|<span data-ttu-id="e671f-173">easDeviceId</span><span class="sxs-lookup"><span data-stu-id="e671f-173">easDeviceId</span></span>|<span data-ttu-id="e671f-174">Cadena</span><span class="sxs-lookup"><span data-stu-id="e671f-174">String</span></span>|<span data-ttu-id="e671f-175">Identificador de Exchange ActiveSync del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e671f-175">Exchange ActiveSync Id of the device.</span></span>|
|<span data-ttu-id="e671f-176">easActivationDateTime</span><span class="sxs-lookup"><span data-stu-id="e671f-176">easActivationDateTime</span></span>|<span data-ttu-id="e671f-177">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e671f-177">DateTimeOffset</span></span>|<span data-ttu-id="e671f-178">Hora de activación de Exchange ActivationSync del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e671f-178">Exchange ActivationSync activation time of the device.</span></span>|
|<span data-ttu-id="e671f-179">azureADRegistered</span><span class="sxs-lookup"><span data-stu-id="e671f-179">azureADRegistered</span></span>|<span data-ttu-id="e671f-180">Booleano</span><span class="sxs-lookup"><span data-stu-id="e671f-180">Boolean</span></span>|<span data-ttu-id="e671f-181">Indica si el dispositivo está registrado en Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e671f-181">Whether the device is Azure Active Directory registered.</span></span>|
|<span data-ttu-id="e671f-182">deviceEnrollmentType</span><span class="sxs-lookup"><span data-stu-id="e671f-182">deviceEnrollmentType</span></span>|[<span data-ttu-id="e671f-183">deviceEnrollmentType</span><span class="sxs-lookup"><span data-stu-id="e671f-183">deviceEnrollmentType</span></span>](../resources/intune_shared_deviceenrollmenttype.md)|<span data-ttu-id="e671f-p106">Tipo de inscripción del dispositivo. Los valores posibles son: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin`, `windowsCoManagement`.</span><span class="sxs-lookup"><span data-stu-id="e671f-p106">Enrollment type of the device. The possible values are: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin`, `windowsCoManagement`.</span></span>|
|<span data-ttu-id="e671f-186">activationLockBypassCode</span><span class="sxs-lookup"><span data-stu-id="e671f-186">activationLockBypassCode</span></span>|<span data-ttu-id="e671f-187">Cadena</span><span class="sxs-lookup"><span data-stu-id="e671f-187">String</span></span>|<span data-ttu-id="e671f-188">Código que permite que se omita el bloqueo de activación en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e671f-188">Code that allows the Activation Lock on a device to be bypassed.</span></span>|
|<span data-ttu-id="e671f-189">emailAddress</span><span class="sxs-lookup"><span data-stu-id="e671f-189">emailAddress</span></span>|<span data-ttu-id="e671f-190">Cadena</span><span class="sxs-lookup"><span data-stu-id="e671f-190">String</span></span>|<span data-ttu-id="e671f-191">Direcciones de correo electrónico del usuario asociado al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e671f-191">Email(s) for the user associated with the device</span></span>|
|<span data-ttu-id="e671f-192">azureADDeviceId</span><span class="sxs-lookup"><span data-stu-id="e671f-192">azureADDeviceId</span></span>|<span data-ttu-id="e671f-193">Cadena</span><span class="sxs-lookup"><span data-stu-id="e671f-193">String</span></span>|<span data-ttu-id="e671f-194">Identificador único del dispositivo de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e671f-194">The unique identifier for the Azure Active Directory device.</span></span> <span data-ttu-id="e671f-195">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e671f-195">Read only.</span></span>|
|<span data-ttu-id="e671f-196">deviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="e671f-196">deviceRegistrationState</span></span>|[<span data-ttu-id="e671f-197">deviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="e671f-197">deviceRegistrationState</span></span>](../resources/intune_devices_deviceregistrationstate.md)|<span data-ttu-id="e671f-p108">Estado de registro de dispositivo. Los valores posibles son: `notRegistered`, `registered`, `revoked`, `keyConflict`, `approvalPending`, `certificateReset`, `notRegisteredPendingEnrollment`, `unknown`.</span><span class="sxs-lookup"><span data-stu-id="e671f-p108">Device registration state. The possible values are: `notRegistered`, `registered`, `revoked`, `keyConflict`, `approvalPending`, `certificateReset`, `notRegisteredPendingEnrollment`, `unknown`.</span></span>|
|<span data-ttu-id="e671f-200">deviceCategoryDisplayName</span><span class="sxs-lookup"><span data-stu-id="e671f-200">deviceCategoryDisplayName</span></span>|<span data-ttu-id="e671f-201">Cadena</span><span class="sxs-lookup"><span data-stu-id="e671f-201">String</span></span>|<span data-ttu-id="e671f-202">Nombre para mostrar de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e671f-202">Device category display name</span></span>|
|<span data-ttu-id="e671f-203">isSupervised</span><span class="sxs-lookup"><span data-stu-id="e671f-203">isSupervised</span></span>|<span data-ttu-id="e671f-204">Booleano</span><span class="sxs-lookup"><span data-stu-id="e671f-204">Boolean</span></span>|<span data-ttu-id="e671f-205">Estado supervisado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e671f-205">Device supervised status</span></span>|
|<span data-ttu-id="e671f-206">exchangeLastSuccessfulSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="e671f-206">exchangeLastSuccessfulSyncDateTime</span></span>|<span data-ttu-id="e671f-207">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e671f-207">DateTimeOffset</span></span>|<span data-ttu-id="e671f-208">Última vez que el dispositivo estableció contacto con Exchange.</span><span class="sxs-lookup"><span data-stu-id="e671f-208">Last time the device contacted Exchange.</span></span>|
|<span data-ttu-id="e671f-209">exchangeAccessState</span><span class="sxs-lookup"><span data-stu-id="e671f-209">exchangeAccessState</span></span>|[<span data-ttu-id="e671f-210">deviceManagementExchangeAccessState</span><span class="sxs-lookup"><span data-stu-id="e671f-210">deviceManagementExchangeAccessState</span></span>](../resources/intune_devices_devicemanagementexchangeaccessstate.md)|<span data-ttu-id="e671f-p109">El estado de acceso del dispositivo en Exchange. Los valores posibles son: `none`, `unknown`, `allowed`, `blocked`, `quarantined`.</span><span class="sxs-lookup"><span data-stu-id="e671f-p109">The Access State of the device in Exchange. The possible values are: `none`, `unknown`, `allowed`, `blocked`, `quarantined`.</span></span>|
|<span data-ttu-id="e671f-213">exchangeAccessStateReason</span><span class="sxs-lookup"><span data-stu-id="e671f-213">exchangeAccessStateReason</span></span>|[<span data-ttu-id="e671f-214">deviceManagementExchangeAccessStateReason</span><span class="sxs-lookup"><span data-stu-id="e671f-214">deviceManagementExchangeAccessStateReason</span></span>](../resources/intune_devices_devicemanagementexchangeaccessstatereason.md)|<span data-ttu-id="e671f-p110">El motivo para el estado de acceso del dispositivo en Exchange. Los valores posibles son: `none`, `unknown`, `exchangeGlobalRule`, `exchangeIndividualRule`, `exchangeDeviceRule`, `exchangeUpgrade`, `exchangeMailboxPolicy`, `other`, `compliant`, `notCompliant`, `notEnrolled`, `unknownLocation`, `mfaRequired`, `azureADBlockDueToAccessPolicy`, `compromisedPassword`, `deviceNotKnownWithManagedApp`.</span><span class="sxs-lookup"><span data-stu-id="e671f-p110">The reason for the device's access state in Exchange. The possible values are: `none`, `unknown`, `exchangeGlobalRule`, `exchangeIndividualRule`, `exchangeDeviceRule`, `exchangeUpgrade`, `exchangeMailboxPolicy`, `other`, `compliant`, `notCompliant`, `notEnrolled`, `unknownLocation`, `mfaRequired`, `azureADBlockDueToAccessPolicy`, `compromisedPassword`, `deviceNotKnownWithManagedApp`.</span></span>|
|<span data-ttu-id="e671f-217">remoteAssistanceSessionUrl</span><span class="sxs-lookup"><span data-stu-id="e671f-217">remoteAssistanceSessionUrl</span></span>|<span data-ttu-id="e671f-218">Cadena</span><span class="sxs-lookup"><span data-stu-id="e671f-218">String</span></span>|<span data-ttu-id="e671f-219">Dirección URL que permite que se establezca una sesión remota con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e671f-219">Url that allows a Remote Assistance session to be established with the device.</span></span>|
|<span data-ttu-id="e671f-220">remoteAssistanceSessionErrorDetails</span><span class="sxs-lookup"><span data-stu-id="e671f-220">remoteAssistanceSessionErrorDetails</span></span>|<span data-ttu-id="e671f-221">Cadena</span><span class="sxs-lookup"><span data-stu-id="e671f-221">String</span></span>|<span data-ttu-id="e671f-222">Cadena de error que identifica los problemas al crear objetos de la sesión de asistencia remota.</span><span class="sxs-lookup"><span data-stu-id="e671f-222">An error string that identifies issues when creating Remote Assistance session objects.</span></span>|
|<span data-ttu-id="e671f-223">isEncrypted</span><span class="sxs-lookup"><span data-stu-id="e671f-223">isEncrypted</span></span>|<span data-ttu-id="e671f-224">Booleano</span><span class="sxs-lookup"><span data-stu-id="e671f-224">Boolean</span></span>|<span data-ttu-id="e671f-225">Estado del cifrado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e671f-225">Device encryption status</span></span>|
|<span data-ttu-id="e671f-226">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="e671f-226">userPrincipalName</span></span>|<span data-ttu-id="e671f-227">Cadena</span><span class="sxs-lookup"><span data-stu-id="e671f-227">String</span></span>|<span data-ttu-id="e671f-228">Nombre principal de usuario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e671f-228">Device user principal name</span></span>|
|<span data-ttu-id="e671f-229">modelo</span><span class="sxs-lookup"><span data-stu-id="e671f-229">model</span></span>|<span data-ttu-id="e671f-230">Cadena</span><span class="sxs-lookup"><span data-stu-id="e671f-230">String</span></span>|<span data-ttu-id="e671f-231">Modelo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e671f-231">Model of the device</span></span>|
|<span data-ttu-id="e671f-232">fabricante</span><span class="sxs-lookup"><span data-stu-id="e671f-232">manufacturer</span></span>|<span data-ttu-id="e671f-233">Cadena</span><span class="sxs-lookup"><span data-stu-id="e671f-233">String</span></span>|<span data-ttu-id="e671f-234">Fabricante del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e671f-234">Manufacturer of the device</span></span>|
|<span data-ttu-id="e671f-235">imei</span><span class="sxs-lookup"><span data-stu-id="e671f-235">imei</span></span>|<span data-ttu-id="e671f-236">Cadena</span><span class="sxs-lookup"><span data-stu-id="e671f-236">String</span></span>|<span data-ttu-id="e671f-237">IMEI</span><span class="sxs-lookup"><span data-stu-id="e671f-237">IMEI</span></span>|
|<span data-ttu-id="e671f-238">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="e671f-238">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="e671f-239">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e671f-239">DateTimeOffset</span></span>|<span data-ttu-id="e671f-240">Fecha y hora en que expira el período de gracia de cumplimiento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e671f-240">The DateTime when device compliance grace period expires</span></span>|
|<span data-ttu-id="e671f-241">serialNumber</span><span class="sxs-lookup"><span data-stu-id="e671f-241">serialNumber</span></span>|<span data-ttu-id="e671f-242">Cadena</span><span class="sxs-lookup"><span data-stu-id="e671f-242">String</span></span>|<span data-ttu-id="e671f-243">Número de serie.</span><span class="sxs-lookup"><span data-stu-id="e671f-243">SerialNumber</span></span>|
|<span data-ttu-id="e671f-244">phoneNumber</span><span class="sxs-lookup"><span data-stu-id="e671f-244">phoneNumber</span></span>|<span data-ttu-id="e671f-245">Cadena</span><span class="sxs-lookup"><span data-stu-id="e671f-245">String</span></span>|<span data-ttu-id="e671f-246">Número de teléfono del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e671f-246">Phone number of the device</span></span>|
|<span data-ttu-id="e671f-247">androidSecurityPatchLevel</span><span class="sxs-lookup"><span data-stu-id="e671f-247">androidSecurityPatchLevel</span></span>|<span data-ttu-id="e671f-248">Cadena</span><span class="sxs-lookup"><span data-stu-id="e671f-248">String</span></span>|<span data-ttu-id="e671f-249">Nivel de revisión de seguridad de Android.</span><span class="sxs-lookup"><span data-stu-id="e671f-249">Android security patch level</span></span>|
|<span data-ttu-id="e671f-250">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="e671f-250">userDisplayName</span></span>|<span data-ttu-id="e671f-251">Cadena</span><span class="sxs-lookup"><span data-stu-id="e671f-251">String</span></span>|<span data-ttu-id="e671f-252">Nombre para mostrar del usuario.</span><span class="sxs-lookup"><span data-stu-id="e671f-252">User display name</span></span>|
|<span data-ttu-id="e671f-253">configurationManagerClientEnabledFeatures</span><span class="sxs-lookup"><span data-stu-id="e671f-253">configurationManagerClientEnabledFeatures</span></span>|[<span data-ttu-id="e671f-254">configurationManagerClientEnabledFeatures</span><span class="sxs-lookup"><span data-stu-id="e671f-254">configurationManagerClientEnabledFeatures</span></span>](../resources/intune_devices_configurationmanagerclientenabledfeatures.md)|<span data-ttu-id="e671f-255">Características activadas del cliente ConfigrMgr.</span><span class="sxs-lookup"><span data-stu-id="e671f-255">ConfigrMgr client enabled features</span></span>|
|<span data-ttu-id="e671f-256">wiFiMacAddress</span><span class="sxs-lookup"><span data-stu-id="e671f-256">wiFiMacAddress</span></span>|<span data-ttu-id="e671f-257">Cadena</span><span class="sxs-lookup"><span data-stu-id="e671f-257">String</span></span>|<span data-ttu-id="e671f-258">MAC de Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="e671f-258">Wi-Fi MAC</span></span>|
|<span data-ttu-id="e671f-259">deviceHealthAttestationState</span><span class="sxs-lookup"><span data-stu-id="e671f-259">deviceHealthAttestationState</span></span>|[<span data-ttu-id="e671f-260">deviceHealthAttestationState</span><span class="sxs-lookup"><span data-stu-id="e671f-260">deviceHealthAttestationState</span></span>](../resources/intune_devices_devicehealthattestationstate.md)|<span data-ttu-id="e671f-261">Estado de la atestación de estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e671f-261">The device health attestation state.</span></span>|
|<span data-ttu-id="e671f-262">subscriberCarrier</span><span class="sxs-lookup"><span data-stu-id="e671f-262">subscriberCarrier</span></span>|<span data-ttu-id="e671f-263">Cadena</span><span class="sxs-lookup"><span data-stu-id="e671f-263">String</span></span>|<span data-ttu-id="e671f-264">Operador del suscriptor.</span><span class="sxs-lookup"><span data-stu-id="e671f-264">Subscriber Carrier</span></span>|
|<span data-ttu-id="e671f-265">meid</span><span class="sxs-lookup"><span data-stu-id="e671f-265">meid</span></span>|<span data-ttu-id="e671f-266">Cadena</span><span class="sxs-lookup"><span data-stu-id="e671f-266">String</span></span>|<span data-ttu-id="e671f-267">MEID</span><span class="sxs-lookup"><span data-stu-id="e671f-267">MEID</span></span>|
|<span data-ttu-id="e671f-268">totalStorageSpaceInBytes</span><span class="sxs-lookup"><span data-stu-id="e671f-268">totalStorageSpaceInBytes</span></span>|<span data-ttu-id="e671f-269">Int64</span><span class="sxs-lookup"><span data-stu-id="e671f-269">Int64</span></span>|<span data-ttu-id="e671f-270">Almacenamiento total en bytes.</span><span class="sxs-lookup"><span data-stu-id="e671f-270">Total Storage in Bytes</span></span>|
|<span data-ttu-id="e671f-271">freeStorageSpaceInBytes</span><span class="sxs-lookup"><span data-stu-id="e671f-271">freeStorageSpaceInBytes</span></span>|<span data-ttu-id="e671f-272">Int64</span><span class="sxs-lookup"><span data-stu-id="e671f-272">Int64</span></span>|<span data-ttu-id="e671f-273">Almacenamiento disponible en bytes.</span><span class="sxs-lookup"><span data-stu-id="e671f-273">Free Storage in Bytes</span></span>|
|<span data-ttu-id="e671f-274">managedDeviceName</span><span class="sxs-lookup"><span data-stu-id="e671f-274">managedDeviceName</span></span>|<span data-ttu-id="e671f-275">Cadena</span><span class="sxs-lookup"><span data-stu-id="e671f-275">String</span></span>|<span data-ttu-id="e671f-276">Nombre generado automáticamente para identificar un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e671f-276">Automatically generated name to identify a device.</span></span> <span data-ttu-id="e671f-277">Se puede sobrescribir con un nombre descriptivo del usuario.</span><span class="sxs-lookup"><span data-stu-id="e671f-277">Can be overwritten to a user friendly name.</span></span>|
|<span data-ttu-id="e671f-278">partnerReportedThreatState</span><span class="sxs-lookup"><span data-stu-id="e671f-278">partnerReportedThreatState</span></span>|[<span data-ttu-id="e671f-279">managedDevicePartnerReportedHealthState</span><span class="sxs-lookup"><span data-stu-id="e671f-279">managedDevicePartnerReportedHealthState</span></span>](../resources/intune_devices_manageddevicepartnerreportedhealthstate.md)|<span data-ttu-id="e671f-p112">Indica el estado de amenaza de un dispositivo cuando el socio de defensa contra amenazas móvil se utiliza por la cuenta y el dispositivo. Solo de lectura. Los valores posibles son: `unknown`, `activated`, `deactivated`, `secured`, `lowSeverity`, `mediumSeverity`, `highSeverity`, `unresponsive`, `compromised`, `misconfigured`.</span><span class="sxs-lookup"><span data-stu-id="e671f-p112">Indicates the threat state of a device when a Mobile Threat Defense partner is in use by the account and device.</span></span>|



## <a name="response"></a><span data-ttu-id="e671f-283">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e671f-283">Response</span></span>
<span data-ttu-id="e671f-284">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [managedDevice](../resources/intune_devices_manageddevice.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e671f-284">If successful, this method returns a `201 Created` response code and a [managedDevice](../resources/intune_devices_manageddevice.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e671f-285">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e671f-285">Example</span></span>
### <a name="request"></a><span data-ttu-id="e671f-286">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e671f-286">Request</span></span>
<span data-ttu-id="e671f-287">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e671f-287">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/users/{usersId}/managedDevices
Content-type: application/json
Content-length: 4656

{
  "@odata.type": "#microsoft.graph.managedDevice",
  "userId": "User Id value",
  "deviceName": "Device Name value",
  "managedDeviceOwnerType": "company",
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

### <a name="response"></a><span data-ttu-id="e671f-288">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e671f-288">Response</span></span>
<span data-ttu-id="e671f-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e671f-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 4705

{
  "@odata.type": "#microsoft.graph.managedDevice",
  "id": "705c034c-034c-705c-4c03-5c704c035c70",
  "userId": "User Id value",
  "deviceName": "Device Name value",
  "managedDeviceOwnerType": "company",
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








