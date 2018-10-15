# <a name="create-mdmwindowsinformationprotectionpolicy"></a><span data-ttu-id="a26e7-101">Crear mdmWindowsInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a26e7-101">Create mdmWindowsInformationProtectionPolicy</span></span>

> <span data-ttu-id="a26e7-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a26e7-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a26e7-103">Crear un objeto [mdmWindowsInformationProtectionPolicy](../resources/intune_mam_mdmwindowsinformationprotectionpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="a26e7-103">Create a new [mdmWindowsInformationProtectionPolicy](../resources/intune_mam_mdmwindowsinformationprotectionpolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a26e7-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a26e7-104">Prerequisites</span></span>
<span data-ttu-id="a26e7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a26e7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a26e7-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a26e7-107">Permission type</span></span>|<span data-ttu-id="a26e7-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a26e7-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a26e7-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a26e7-109">Delegated (work or school account)</span></span>|<span data-ttu-id="a26e7-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a26e7-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="a26e7-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a26e7-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a26e7-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a26e7-112">Not supported.</span></span>|
|<span data-ttu-id="a26e7-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a26e7-113">Application</span></span>|<span data-ttu-id="a26e7-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a26e7-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a26e7-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a26e7-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mdmWindowsInformationProtectionPolicies
```

## <a name="request-headers"></a><span data-ttu-id="a26e7-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a26e7-116">Request headers</span></span>
|<span data-ttu-id="a26e7-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a26e7-117">Header</span></span>|<span data-ttu-id="a26e7-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a26e7-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a26e7-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="a26e7-119">Authorization</span></span>|<span data-ttu-id="a26e7-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a26e7-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a26e7-121">Accept</span><span class="sxs-lookup"><span data-stu-id="a26e7-121">Accept</span></span>|<span data-ttu-id="a26e7-122">application/json</span><span class="sxs-lookup"><span data-stu-id="a26e7-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a26e7-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a26e7-123">Request body</span></span>
<span data-ttu-id="a26e7-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto mdmWindowsInformationProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="a26e7-124">In the request body, supply a JSON representation for the mdmWindowsInformationProtectionPolicy object.</span></span>

<span data-ttu-id="a26e7-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto mdmWindowsInformationProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="a26e7-125">The following table shows the properties that are required when you create the mdmWindowsInformationProtectionPolicy.</span></span>

|<span data-ttu-id="a26e7-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a26e7-126">Property</span></span>|<span data-ttu-id="a26e7-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="a26e7-127">Type</span></span>|<span data-ttu-id="a26e7-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="a26e7-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a26e7-129">displayName</span><span class="sxs-lookup"><span data-stu-id="a26e7-129">displayName</span></span>|<span data-ttu-id="a26e7-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="a26e7-130">String</span></span>|<span data-ttu-id="a26e7-131">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="a26e7-131">Policy display name.</span></span> <span data-ttu-id="a26e7-132">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="a26e7-132">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="a26e7-133">description</span><span class="sxs-lookup"><span data-stu-id="a26e7-133">description</span></span>|<span data-ttu-id="a26e7-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="a26e7-134">String</span></span>|<span data-ttu-id="a26e7-135">Descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="a26e7-135">The policy's description.</span></span> <span data-ttu-id="a26e7-136">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="a26e7-136">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="a26e7-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="a26e7-137">createdDateTime</span></span>|<span data-ttu-id="a26e7-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a26e7-138">DateTimeOffset</span></span>|<span data-ttu-id="a26e7-139">Fecha y hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="a26e7-139">The date and time the policy was created.</span></span> <span data-ttu-id="a26e7-140">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="a26e7-140">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="a26e7-141">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="a26e7-141">lastModifiedDateTime</span></span>|<span data-ttu-id="a26e7-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a26e7-142">DateTimeOffset</span></span>|<span data-ttu-id="a26e7-143">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="a26e7-143">Last time the policy was modified.</span></span> <span data-ttu-id="a26e7-144">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="a26e7-144">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="a26e7-145">id</span><span class="sxs-lookup"><span data-stu-id="a26e7-145">id</span></span>|<span data-ttu-id="a26e7-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="a26e7-146">String</span></span>|<span data-ttu-id="a26e7-147">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a26e7-147">Key of the entity.</span></span> <span data-ttu-id="a26e7-148">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="a26e7-148">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="a26e7-149">version</span><span class="sxs-lookup"><span data-stu-id="a26e7-149">version</span></span>|<span data-ttu-id="a26e7-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="a26e7-150">String</span></span>|<span data-ttu-id="a26e7-151">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a26e7-151">Version of the entity.</span></span> <span data-ttu-id="a26e7-152">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="a26e7-152">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="a26e7-153">enforcementLevel</span><span class="sxs-lookup"><span data-stu-id="a26e7-153">enforcementLevel</span></span>|[<span data-ttu-id="a26e7-154">windowsInformationProtectionEnforcementLevel</span><span class="sxs-lookup"><span data-stu-id="a26e7-154">windowsInformationProtectionEnforcementLevel</span></span>](../resources/intune_mam_windowsinformationprotectionenforcementlevel.md)|<span data-ttu-id="a26e7-p108">Nivel de obligatoriedad del trabajo en curso. Vea la definición de enumeración para los valores compatibles. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md). Los valores posibles son: `noProtection`, `encryptAndAuditOnly`, `encryptAuditAndPrompt` y `encryptAuditAndBlock`.</span><span class="sxs-lookup"><span data-stu-id="a26e7-p108">WIP enforcement level.See the Enum definition for supported values Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) Possible values are: `noProtection`, `encryptAndAuditOnly`, `encryptAuditAndPrompt`, `encryptAuditAndBlock`.</span></span>|
|<span data-ttu-id="a26e7-157">enterpriseDomain</span><span class="sxs-lookup"><span data-stu-id="a26e7-157">enterpriseDomain</span></span>|<span data-ttu-id="a26e7-158">Cadena</span><span class="sxs-lookup"><span data-stu-id="a26e7-158">String</span></span>|<span data-ttu-id="a26e7-159">Dominio empresarial principal. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="a26e7-159">Primary enterprise domain Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="a26e7-160">enterpriseProtectedDomainNames</span><span class="sxs-lookup"><span data-stu-id="a26e7-160">enterpriseProtectedDomainNames</span></span>|<span data-ttu-id="a26e7-161">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="a26e7-161">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="a26e7-162">Lista de dominios de empresa que se van a proteger. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="a26e7-162">List of enterprise domains to be protected Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="a26e7-163">protectionUnderLockConfigRequired</span><span class="sxs-lookup"><span data-stu-id="a26e7-163">protectionUnderLockConfigRequired</span></span>|<span data-ttu-id="a26e7-164">Booleano</span><span class="sxs-lookup"><span data-stu-id="a26e7-164">Boolean</span></span>|<span data-ttu-id="a26e7-165">Especifica si es necesario configurar la protección en la característica de bloqueo (también conocida como cifrar con PIN). Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="a26e7-165">Specifies whether the protection under lock feature (also known as encrypt under pin) should be configured Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="a26e7-166">dataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="a26e7-166">dataRecoveryCertificate</span></span>|[<span data-ttu-id="a26e7-167">windowsInformationProtectionDataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="a26e7-167">windowsInformationProtectionDataRecoveryCertificate</span></span>](../resources/intune_mam_windowsinformationprotectiondatarecoverycertificate.md)|<span data-ttu-id="a26e7-168">Especifica un certificado de recuperación que se puede usar para recuperar datos de archivos cifrados.</span><span class="sxs-lookup"><span data-stu-id="a26e7-168">Specifies a recovery certificate that can be used for data recovery of encrypted files.</span></span> <span data-ttu-id="a26e7-169">Es igual al certificado del agente de recuperación de datos (DRA) para el sistema de cifrado de archivos (EFS). Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="a26e7-169">This is the same as the data recovery agent(DRA) certificate for encrypting file system(EFS) Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="a26e7-170">revokeOnUnenrollDisabled</span><span class="sxs-lookup"><span data-stu-id="a26e7-170">revokeOnUnenrollDisabled</span></span>|<span data-ttu-id="a26e7-171">Booleano</span><span class="sxs-lookup"><span data-stu-id="a26e7-171">Boolean</span></span>|<span data-ttu-id="a26e7-172">Esta directiva controla si se revocan las claves de trabajo en curso cuando se anula la inscripción de un dispositivo en el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="a26e7-172">This policy controls whether to revoke the WIP keys when a device unenrolls from the management service.</span></span> <span data-ttu-id="a26e7-173">Si se establece en 1 (no revocar las claves), no se revocarán las claves y el usuario seguirá teniendo acceso a archivos protegidos después de anular la inscripción.</span><span class="sxs-lookup"><span data-stu-id="a26e7-173">If set to 1 (Don't revoke keys), the keys will not be revoked and the user will continue to have access to protected files after unenrollment.</span></span> <span data-ttu-id="a26e7-174">Si no se revocan las claves, no habrá ninguna limpieza de archivos revocados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="a26e7-174">If the keys are not revoked, there will be no revoked file cleanup subsequently.</span></span> <span data-ttu-id="a26e7-175">Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="a26e7-175">Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="a26e7-176">rightsManagementServicesTemplateId</span><span class="sxs-lookup"><span data-stu-id="a26e7-176">rightsManagementServicesTemplateId</span></span>|<span data-ttu-id="a26e7-177">Guid</span><span class="sxs-lookup"><span data-stu-id="a26e7-177">Guid</span></span>|<span data-ttu-id="a26e7-178">GUID de TemplateID que se va a usar para el cifrado RMS.</span><span class="sxs-lookup"><span data-stu-id="a26e7-178">TemplateID GUID to use for RMS encryption.</span></span> <span data-ttu-id="a26e7-179">La plantilla de RMS permite que el administrador de TI configure los detalles sobre quién tiene acceso a los archivos protegidos por RMS y durante cuánto tiempo. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="a26e7-179">The RMS template allows the IT admin to configure the details about who has access to RMS-protected file and how long they have access Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="a26e7-180">azureRightsManagementServicesAllowed</span><span class="sxs-lookup"><span data-stu-id="a26e7-180">azureRightsManagementServicesAllowed</span></span>|<span data-ttu-id="a26e7-181">Booleano</span><span class="sxs-lookup"><span data-stu-id="a26e7-181">Boolean</span></span>|<span data-ttu-id="a26e7-182">Especifica si se permite el cifrado de Azure RMS para WIP. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="a26e7-182">Specifies whether to allow Azure RMS encryption for WIP Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="a26e7-183">iconsVisible</span><span class="sxs-lookup"><span data-stu-id="a26e7-183">iconsVisible</span></span>|<span data-ttu-id="a26e7-184">Booleano</span><span class="sxs-lookup"><span data-stu-id="a26e7-184">Boolean</span></span>|<span data-ttu-id="a26e7-185">Determina si se agregan las superposiciones a los iconos para los archivos protegidos mediante WIP en Explorer y en los iconos de aplicación solo de empresa en el menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="a26e7-185">Determines whether overlays are added to icons for WIP protected files in Explorer and enterprise only app tiles in the Start menu.</span></span> <span data-ttu-id="a26e7-186">A partir de Windows 10, versión 1703, estos ajustes también configuran la visibilidad del icono de WIP en la barra de título de una aplicación protegida mediante WIP. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="a26e7-186">Starting in Windows 10, version 1703 this setting also configures the visibility of the WIP icon in the title bar of a WIP-protected app Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="a26e7-187">protectedApps</span><span class="sxs-lookup"><span data-stu-id="a26e7-187">protectedApps</span></span>|<span data-ttu-id="a26e7-188">Colección [windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="a26e7-188">[windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md) collection</span></span>|<span data-ttu-id="a26e7-189">Las aplicaciones protegidas pueden tener acceso a datos empresariales y los datos controlados por dichas aplicaciones están protegidos mediante cifrado. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="a26e7-189">Protected applications can access enterprise data and the data handled by those applications are protected with encryption Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="a26e7-190">exemptApps</span><span class="sxs-lookup"><span data-stu-id="a26e7-190">exemptApps</span></span>|<span data-ttu-id="a26e7-191">Colección [windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="a26e7-191">[windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md) collection</span></span>|<span data-ttu-id="a26e7-192">Las aplicaciones exentas también pueden tener acceso a datos empresariales, pero los datos controlados por dichas aplicaciones no están protegidos.</span><span class="sxs-lookup"><span data-stu-id="a26e7-192">Exempt applications can also access enterprise data, but the data handled by those applications are not protected.</span></span> <span data-ttu-id="a26e7-193">Esto ocurre porque algunas aplicaciones empresariales críticas podrían tener problemas de compatibilidad con los datos cifrados.</span><span class="sxs-lookup"><span data-stu-id="a26e7-193">This is because some critical enterprise applications may have compatibility problems with encrypted data.</span></span> <span data-ttu-id="a26e7-194">Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="a26e7-194">Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="a26e7-195">enterpriseNetworkDomainNames</span><span class="sxs-lookup"><span data-stu-id="a26e7-195">enterpriseNetworkDomainNames</span></span>|<span data-ttu-id="a26e7-196">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="a26e7-196">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="a26e7-197">Esta es la lista de dominios que forman parte de los límites de la empresa.</span><span class="sxs-lookup"><span data-stu-id="a26e7-197">This is the list of domains that comprise the boundaries of the enterprise.</span></span> <span data-ttu-id="a26e7-198">Los datos de uno de estos dominios que se envíen a un dispositivo se considerarán datos empresariales y protegidos. Estas ubicaciones se consideran un destino seguro con el que compartir datos empresariales. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="a26e7-198">Data from one of these domains that is sent to a device will be considered enterprise data and protected These locations will be considered a safe destination for enterprise data to be shared to Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="a26e7-199">enterpriseProxiedDomains</span><span class="sxs-lookup"><span data-stu-id="a26e7-199">enterpriseProxiedDomains</span></span>|<span data-ttu-id="a26e7-200">Colección [windowsInformationProtectionProxiedDomainCollection](../resources/intune_mam_windowsinformationprotectionproxieddomaincollection.md)</span><span class="sxs-lookup"><span data-stu-id="a26e7-200">[windowsInformationProtectionProxiedDomainCollection](../resources/intune_mam_windowsinformationprotectionproxieddomaincollection.md) collection</span></span>|<span data-ttu-id="a26e7-201">Contiene una lista de dominios de recursos empresariales hospedados en la nube que necesitan protección.</span><span class="sxs-lookup"><span data-stu-id="a26e7-201">Contains a list of Enterprise resource domains hosted in the cloud that need to be protected.</span></span> <span data-ttu-id="a26e7-202">Las conexiones a estos recursos se consideran datos empresariales.</span><span class="sxs-lookup"><span data-stu-id="a26e7-202">Connections to these resources are considered enterprise data.</span></span> <span data-ttu-id="a26e7-203">Si un proxy se corresponde con un recurso de nube, el tráfico al recurso de la nube se dirigirá a través de la red empresarial mediante el servidor proxy indicado (en el puerto 80).</span><span class="sxs-lookup"><span data-stu-id="a26e7-203">If a proxy is paired with a cloud resource, traffic to the cloud resource will be routed through the enterprise network via the denoted proxy server (on Port 80).</span></span> <span data-ttu-id="a26e7-204">Un servidor proxy que se use con esta finalidad debe configurarse también mediante la directiva EnterpriseInternalProxyServers. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="a26e7-204">A proxy server used for this purpose must also be configured using the EnterpriseInternalProxyServers policy Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="a26e7-205">enterpriseIPRanges</span><span class="sxs-lookup"><span data-stu-id="a26e7-205">enterpriseIPRanges</span></span>|<span data-ttu-id="a26e7-206">Colección [windowsInformationProtectionIPRangeCollection](../resources/intune_mam_windowsinformationprotectioniprangecollection.md)</span><span class="sxs-lookup"><span data-stu-id="a26e7-206">[windowsInformationProtectionIPRangeCollection](../resources/intune_mam_windowsinformationprotectioniprangecollection.md) collection</span></span>|<span data-ttu-id="a26e7-207">Establece los intervalos IP empresariales que definen los equipos de la red empresarial.</span><span class="sxs-lookup"><span data-stu-id="a26e7-207">Sets the enterprise IP ranges that define the computers in the enterprise network.</span></span> <span data-ttu-id="a26e7-208">Los datos que provienen de dichos equipos se consideran parte de la empresa y están protegidos.</span><span class="sxs-lookup"><span data-stu-id="a26e7-208">Data that comes from those computers will be considered part of the enterprise and protected.</span></span> <span data-ttu-id="a26e7-209">Estas ubicaciones se consideran un destino seguro en el que compartir datos empresariales. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="a26e7-209">These locations will be considered a safe destination for enterprise data to be shared to Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="a26e7-210">enterpriseIPRangesAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="a26e7-210">enterpriseIPRangesAreAuthoritative</span></span>|<span data-ttu-id="a26e7-211">Booleano</span><span class="sxs-lookup"><span data-stu-id="a26e7-211">Boolean</span></span>|<span data-ttu-id="a26e7-212">Valor booleano que indica al cliente que acepte la lista configurada y que no use la heurística para intentar buscar otras subredes.</span><span class="sxs-lookup"><span data-stu-id="a26e7-212">Boolean value that tells the client to accept the configured list and not to use heuristics to attempt to find other subnets.</span></span> <span data-ttu-id="a26e7-213">El valor predeterminado es False. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="a26e7-213">Default is false Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="a26e7-214">enterpriseProxyServers</span><span class="sxs-lookup"><span data-stu-id="a26e7-214">enterpriseProxyServers</span></span>|<span data-ttu-id="a26e7-215">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="a26e7-215">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="a26e7-216">Esta es una lista de servidores proxy.</span><span class="sxs-lookup"><span data-stu-id="a26e7-216">This is a list of proxy servers.</span></span> <span data-ttu-id="a26e7-217">Cualquier servidor que no esté en esta lista se considera no empresarial. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="a26e7-217">Any server not on this list is considered non-enterprise Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="a26e7-218">enterpriseInternalProxyServers</span><span class="sxs-lookup"><span data-stu-id="a26e7-218">enterpriseInternalProxyServers</span></span>|<span data-ttu-id="a26e7-219">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="a26e7-219">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="a26e7-220">Se trata de la lista de valores separados por comas de servidores proxy internos.</span><span class="sxs-lookup"><span data-stu-id="a26e7-220">This is the comma-separated list of internal proxy servers.</span></span> <span data-ttu-id="a26e7-221">Por ejemplo, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span><span class="sxs-lookup"><span data-stu-id="a26e7-221">For example, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span></span> <span data-ttu-id="a26e7-222">El administrador ha configurado estos servidores proxy para que se conecten a los recursos específicos de Internet.</span><span class="sxs-lookup"><span data-stu-id="a26e7-222">These proxies have been configured by the admin to connect to specific resources on the Internet.</span></span> <span data-ttu-id="a26e7-223">Se consideran ubicaciones de red empresarial.</span><span class="sxs-lookup"><span data-stu-id="a26e7-223">They are considered to be enterprise network locations.</span></span> <span data-ttu-id="a26e7-224">Los servidores proxy solo se usan al configurar la directiva EnterpriseProxiedDomains para forzar el tráfico a los dominios coincidentes mediante estos proxy. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="a26e7-224">The proxies are only leveraged in configuring the EnterpriseProxiedDomains policy to force traffic to the matched domains through these proxies Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="a26e7-225">enterpriseProxyServersAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="a26e7-225">enterpriseProxyServersAreAuthoritative</span></span>|<span data-ttu-id="a26e7-226">Booleano</span><span class="sxs-lookup"><span data-stu-id="a26e7-226">Boolean</span></span>|<span data-ttu-id="a26e7-227">Valor booleano que indica al cliente que acepte la lista de configuración de servidores proxy y no intente detectar otros servidores proxy de trabajo.</span><span class="sxs-lookup"><span data-stu-id="a26e7-227">Boolean value that tells the client to accept the configured list of proxies and not try to detect other work proxies.</span></span> <span data-ttu-id="a26e7-228">El valor predeterminado es False. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="a26e7-228">Default is false Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="a26e7-229">neutralDomainResources</span><span class="sxs-lookup"><span data-stu-id="a26e7-229">neutralDomainResources</span></span>|<span data-ttu-id="a26e7-230">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="a26e7-230">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="a26e7-231">Lista de nombres de dominio que se pueden usar para el recurso de trabajo o personal. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="a26e7-231">List of domain names that can used for work or personal resource Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="a26e7-232">indexingEncryptedStoresOrItemsBlocked</span><span class="sxs-lookup"><span data-stu-id="a26e7-232">indexingEncryptedStoresOrItemsBlocked</span></span>|<span data-ttu-id="a26e7-233">Booleano</span><span class="sxs-lookup"><span data-stu-id="a26e7-233">Boolean</span></span>|<span data-ttu-id="a26e7-234">Este identificador es para que el indexador de Windows Search permita o impida la indexación de los elementos. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="a26e7-234">This switch is for the Windows Search Indexer, to allow or disallow indexing of items Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="a26e7-235">smbAutoEncryptedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="a26e7-235">smbAutoEncryptedFileExtensions</span></span>|<span data-ttu-id="a26e7-236">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="a26e7-236">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="a26e7-237">Especifica una lista de extensiones de archivo, para que los archivos con estas extensiones se cifren cuando se copian desde un recurso compartido de SMB dentro del límite de la empresa. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="a26e7-237">Specifies a list of file extensions, so that files with these extensions are encrypted when copying from an SMB share within the corporate boundary Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="a26e7-238">isAssigned</span><span class="sxs-lookup"><span data-stu-id="a26e7-238">isAssigned</span></span>|<span data-ttu-id="a26e7-239">Booleano</span><span class="sxs-lookup"><span data-stu-id="a26e7-239">Boolean</span></span>|<span data-ttu-id="a26e7-240">Indica si la directiva se implementará en los grupos de inclusión.</span><span class="sxs-lookup"><span data-stu-id="a26e7-240">Indicates if the policy is deployed to any inclusion groups or not.</span></span> <span data-ttu-id="a26e7-241">Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="a26e7-241">Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|



## <a name="response"></a><span data-ttu-id="a26e7-242">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a26e7-242">Response</span></span>
<span data-ttu-id="a26e7-243">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [mdmWindowsInformationProtectionPolicy](../resources/intune_mam_mdmwindowsinformationprotectionpolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a26e7-243">If successful, this method returns a `201 Created` response code and a [mdmWindowsInformationProtectionPolicy](../resources/intune_mam_mdmwindowsinformationprotectionpolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a26e7-244">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a26e7-244">Example</span></span>
### <a name="request"></a><span data-ttu-id="a26e7-245">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a26e7-245">Request</span></span>
<span data-ttu-id="a26e7-246">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a26e7-246">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mdmWindowsInformationProtectionPolicies
Content-type: application/json
Content-length: 3966

{
  "@odata.type": "#microsoft.intune_mam_graph.windowsInformationProtectionPolicy",
  "displayName": "Display Name value",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "version": "Version value",
  "enforcementLevel": "encryptAndAuditOnly",
  "enterpriseDomain": "Enterprise Domain value",
  "enterpriseProtectedDomainNames": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "protectionUnderLockConfigRequired": true,
  "dataRecoveryCertificate": {
    "@odata.type": "microsoft.graph.windowsInformationProtectionDataRecoveryCertificate",
    "subjectName": "Subject Name value",
    "description": "Description value",
    "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
    "certificate": "Y2VydGlmaWNhdGU="
  },
  "revokeOnUnenrollDisabled": true,
  "rightsManagementServicesTemplateId": "<Unknown Primitive Type Edm.Guid>",
  "azureRightsManagementServicesAllowed": true,
  "iconsVisible": true,
  "protectedApps": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp",
      "displayName": "Display Name value",
      "description": "Description value",
      "publisherName": "Publisher Name value",
      "productName": "Product Name value",
      "denied": true
    }
  ],
  "exemptApps": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp",
      "displayName": "Display Name value",
      "description": "Description value",
      "publisherName": "Publisher Name value",
      "productName": "Product Name value",
      "denied": true
    }
  ],
  "enterpriseNetworkDomainNames": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "enterpriseProxiedDomains": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionProxiedDomainCollection",
      "displayName": "Display Name value",
      "proxiedDomains": [
        {
          "@odata.type": "microsoft.graph.proxiedDomain",
          "ipAddressOrFQDN": "Ip Address Or FQDN value",
          "proxy": "Proxy value"
        }
      ]
    }
  ],
  "enterpriseIPRanges": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionIPRangeCollection",
      "displayName": "Display Name value",
      "ranges": [
        {
          "@odata.type": "microsoft.graph.iPv6Range",
          "lowerAddress": "Lower Address value",
          "upperAddress": "Upper Address value"
        }
      ]
    }
  ],
  "enterpriseIPRangesAreAuthoritative": true,
  "enterpriseProxyServers": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "enterpriseInternalProxyServers": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "enterpriseProxyServersAreAuthoritative": true,
  "neutralDomainResources": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "indexingEncryptedStoresOrItemsBlocked": true,
  "smbAutoEncryptedFileExtensions": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "isAssigned": true
}
```

### <a name="response"></a><span data-ttu-id="a26e7-247">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a26e7-247">Response</span></span>
<span data-ttu-id="a26e7-p122">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a26e7-p122">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 4074

{
  "@odata.type": "#microsoft.intune_mam_graph.windowsInformationProtectionPolicy",
  "displayName": "Display Name value",
  "description": "Description value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "id": "8efb0c35-0c35-8efb-350c-fb8e350cfb8e",
  "version": "Version value",
  "enforcementLevel": "encryptAndAuditOnly",
  "enterpriseDomain": "Enterprise Domain value",
  "enterpriseProtectedDomainNames": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "protectionUnderLockConfigRequired": true,
  "dataRecoveryCertificate": {
    "@odata.type": "microsoft.graph.windowsInformationProtectionDataRecoveryCertificate",
    "subjectName": "Subject Name value",
    "description": "Description value",
    "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
    "certificate": "Y2VydGlmaWNhdGU="
  },
  "revokeOnUnenrollDisabled": true,
  "rightsManagementServicesTemplateId": "<Unknown Primitive Type Edm.Guid>",
  "azureRightsManagementServicesAllowed": true,
  "iconsVisible": true,
  "protectedApps": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp",
      "displayName": "Display Name value",
      "description": "Description value",
      "publisherName": "Publisher Name value",
      "productName": "Product Name value",
      "denied": true
    }
  ],
  "exemptApps": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp",
      "displayName": "Display Name value",
      "description": "Description value",
      "publisherName": "Publisher Name value",
      "productName": "Product Name value",
      "denied": true
    }
  ],
  "enterpriseNetworkDomainNames": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "enterpriseProxiedDomains": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionProxiedDomainCollection",
      "displayName": "Display Name value",
      "proxiedDomains": [
        {
          "@odata.type": "microsoft.graph.proxiedDomain",
          "ipAddressOrFQDN": "Ip Address Or FQDN value",
          "proxy": "Proxy value"
        }
      ]
    }
  ],
  "enterpriseIPRanges": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionIPRangeCollection",
      "displayName": "Display Name value",
      "ranges": [
        {
          "@odata.type": "microsoft.graph.iPv6Range",
          "lowerAddress": "Lower Address value",
          "upperAddress": "Upper Address value"
        }
      ]
    }
  ],
  "enterpriseIPRangesAreAuthoritative": true,
  "enterpriseProxyServers": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "enterpriseInternalProxyServers": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "enterpriseProxyServersAreAuthoritative": true,
  "neutralDomainResources": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "indexingEncryptedStoresOrItemsBlocked": true,
  "smbAutoEncryptedFileExtensions": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "isAssigned": true
}
```








