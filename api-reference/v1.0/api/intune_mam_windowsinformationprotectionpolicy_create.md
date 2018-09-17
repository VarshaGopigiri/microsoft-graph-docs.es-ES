# <a name="create-windowsinformationprotectionpolicy"></a><span data-ttu-id="39561-101">Crear windowsInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="39561-101">Create windowsInformationProtectionPolicy</span></span>

> <span data-ttu-id="39561-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="39561-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="39561-103">Crear un objeto [windowsInformationProtectionPolicy](../resources/intune_mam_windowsinformationprotectionpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="39561-103">Create a new [windowsInformationProtectionPolicy](../resources/intune_mam_windowsinformationprotectionpolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="39561-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="39561-104">Prerequisites</span></span>
<span data-ttu-id="39561-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="39561-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="39561-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="39561-107">Permission type</span></span>|<span data-ttu-id="39561-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="39561-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="39561-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="39561-109">Delegated (work or school account)</span></span>|<span data-ttu-id="39561-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="39561-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="39561-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="39561-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="39561-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="39561-112">Not supported.</span></span>|
|<span data-ttu-id="39561-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="39561-113">Application</span></span>|<span data-ttu-id="39561-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="39561-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="39561-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="39561-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/windowsInformationProtectionPolicies
```

## <a name="request-headers"></a><span data-ttu-id="39561-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="39561-116">Request headers</span></span>
|<span data-ttu-id="39561-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39561-117">Header</span></span>|<span data-ttu-id="39561-118">Valor</span><span class="sxs-lookup"><span data-stu-id="39561-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="39561-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="39561-119">Authorization</span></span>|<span data-ttu-id="39561-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="39561-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="39561-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="39561-121">Accept</span></span>|<span data-ttu-id="39561-122">application/json</span><span class="sxs-lookup"><span data-stu-id="39561-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="39561-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="39561-123">Request body</span></span>
<span data-ttu-id="39561-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsInformationProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="39561-124">In the request body, supply a JSON representation for the windowsInformationProtectionPolicy object.</span></span>

<span data-ttu-id="39561-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsInformationProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="39561-125">The following table shows the properties that are required when you create the windowsInformationProtectionPolicy.</span></span>

|<span data-ttu-id="39561-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="39561-126">Property</span></span>|<span data-ttu-id="39561-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="39561-127">Type</span></span>|<span data-ttu-id="39561-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="39561-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="39561-129">displayName</span><span class="sxs-lookup"><span data-stu-id="39561-129">displayName</span></span>|<span data-ttu-id="39561-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="39561-130">String</span></span>|<span data-ttu-id="39561-131">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="39561-131">Policy display name.</span></span> <span data-ttu-id="39561-132">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="39561-132">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="39561-133">descripción</span><span class="sxs-lookup"><span data-stu-id="39561-133">description</span></span>|<span data-ttu-id="39561-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="39561-134">String</span></span>|<span data-ttu-id="39561-135">Descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="39561-135">The policy's description.</span></span> <span data-ttu-id="39561-136">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="39561-136">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="39561-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="39561-137">createdDateTime</span></span>|<span data-ttu-id="39561-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="39561-138">DateTimeOffset</span></span>|<span data-ttu-id="39561-139">Fecha y hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="39561-139">The date and time the policy was created.</span></span> <span data-ttu-id="39561-140">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="39561-140">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="39561-141">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="39561-141">lastModifiedDateTime</span></span>|<span data-ttu-id="39561-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="39561-142">DateTimeOffset</span></span>|<span data-ttu-id="39561-143">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="39561-143">Last time the policy was modified.</span></span> <span data-ttu-id="39561-144">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="39561-144">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="39561-145">id.</span><span class="sxs-lookup"><span data-stu-id="39561-145">id</span></span>|<span data-ttu-id="39561-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="39561-146">String</span></span>|<span data-ttu-id="39561-147">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="39561-147">Key of the entity.</span></span> <span data-ttu-id="39561-148">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="39561-148">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="39561-149">versión</span><span class="sxs-lookup"><span data-stu-id="39561-149">version</span></span>|<span data-ttu-id="39561-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="39561-150">String</span></span>|<span data-ttu-id="39561-151">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="39561-151">Version of the entity.</span></span> <span data-ttu-id="39561-152">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="39561-152">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="39561-153">enforcementLevel</span><span class="sxs-lookup"><span data-stu-id="39561-153">enforcementLevel</span></span>|[<span data-ttu-id="39561-154">windowsInformationProtectionEnforcementLevel</span><span class="sxs-lookup"><span data-stu-id="39561-154">windowsInformationProtectionEnforcementLevel</span></span>](../resources/intune_mam_windowsinformationprotectionenforcementlevel.md)|<span data-ttu-id="39561-p108">Nivel de obligatoriedad del trabajo en curso. Vea la definición de enumeración para los valores compatibles. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md). Los valores posibles son: `noProtection`, `encryptAndAuditOnly`, `encryptAuditAndPrompt` y `encryptAuditAndBlock`.</span><span class="sxs-lookup"><span data-stu-id="39561-p108">WIP enforcement level.See the Enum definition for supported values Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) Possible values are: `noProtection`, `encryptAndAuditOnly`, `encryptAuditAndPrompt`, `encryptAuditAndBlock`.</span></span>|
|<span data-ttu-id="39561-157">enterpriseDomain</span><span class="sxs-lookup"><span data-stu-id="39561-157">enterpriseDomain</span></span>|<span data-ttu-id="39561-158">Cadena</span><span class="sxs-lookup"><span data-stu-id="39561-158">String</span></span>|<span data-ttu-id="39561-159">Dominio empresarial principal. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="39561-159">Primary enterprise domain Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="39561-160">enterpriseProtectedDomainNames</span><span class="sxs-lookup"><span data-stu-id="39561-160">enterpriseProtectedDomainNames</span></span>|<span data-ttu-id="39561-161">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="39561-161">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="39561-162">Lista de dominios de empresa que se van a proteger. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="39561-162">List of enterprise domains to be protected Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="39561-163">protectionUnderLockConfigRequired</span><span class="sxs-lookup"><span data-stu-id="39561-163">protectionUnderLockConfigRequired</span></span>|<span data-ttu-id="39561-164">Booleano</span><span class="sxs-lookup"><span data-stu-id="39561-164">Boolean</span></span>|<span data-ttu-id="39561-165">Especifica si es necesario configurar la protección en la característica de bloqueo (también conocida como cifrar con PIN). Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="39561-165">Specifies whether the protection under lock feature (also known as encrypt under pin) should be configured Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="39561-166">dataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="39561-166">dataRecoveryCertificate</span></span>|[<span data-ttu-id="39561-167">windowsInformationProtectionDataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="39561-167">windowsInformationProtectionDataRecoveryCertificate</span></span>](../resources/intune_mam_windowsinformationprotectiondatarecoverycertificate.md)|<span data-ttu-id="39561-168">Especifica un certificado de recuperación que se puede usar para recuperar datos de archivos cifrados.</span><span class="sxs-lookup"><span data-stu-id="39561-168">Specifies a recovery certificate that can be used for data recovery of encrypted files.</span></span> <span data-ttu-id="39561-169">Es igual al certificado del agente de recuperación de datos (DRA) para el sistema de cifrado de archivos (EFS). Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="39561-169">This is the same as the data recovery agent(DRA) certificate for encrypting file system(EFS) Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="39561-170">revokeOnUnenrollDisabled</span><span class="sxs-lookup"><span data-stu-id="39561-170">revokeOnUnenrollDisabled</span></span>|<span data-ttu-id="39561-171">Booleano</span><span class="sxs-lookup"><span data-stu-id="39561-171">Boolean</span></span>|<span data-ttu-id="39561-172">Esta directiva controla si se revocan las claves de trabajo en curso cuando se anula la inscripción de un dispositivo en el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="39561-172">This policy controls whether to revoke the WIP keys when a device unenrolls from the management service.</span></span> <span data-ttu-id="39561-173">Si se establece en 1 (no revocar las claves), no se revocarán las claves y el usuario seguirá teniendo acceso a archivos protegidos después de anular la inscripción.</span><span class="sxs-lookup"><span data-stu-id="39561-173">If set to 1 (Don't revoke keys), the keys will not be revoked and the user will continue to have access to protected files after unenrollment.</span></span> <span data-ttu-id="39561-174">Si no se revocan las claves, no habrá ninguna limpieza de archivos revocados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="39561-174">If the keys are not revoked, there will be no revoked file cleanup subsequently.</span></span> <span data-ttu-id="39561-175">Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="39561-175">Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="39561-176">rightsManagementServicesTemplateId</span><span class="sxs-lookup"><span data-stu-id="39561-176">rightsManagementServicesTemplateId</span></span>|<span data-ttu-id="39561-177">Guid</span><span class="sxs-lookup"><span data-stu-id="39561-177">Guid</span></span>|<span data-ttu-id="39561-178">GUID de TemplateID que se va a usar para el cifrado RMS.</span><span class="sxs-lookup"><span data-stu-id="39561-178">TemplateID GUID to use for RMS encryption.</span></span> <span data-ttu-id="39561-179">La plantilla de RMS permite que el administrador de TI configure los detalles sobre quién tiene acceso a los archivos protegidos por RMS y durante cuánto tiempo. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="39561-179">The RMS template allows the IT admin to configure the details about who has access to RMS-protected file and how long they have access Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="39561-180">azureRightsManagementServicesAllowed</span><span class="sxs-lookup"><span data-stu-id="39561-180">azureRightsManagementServicesAllowed</span></span>|<span data-ttu-id="39561-181">Booleano</span><span class="sxs-lookup"><span data-stu-id="39561-181">Boolean</span></span>|<span data-ttu-id="39561-182">Especifica si se permite el cifrado de Azure RMS para WIP. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="39561-182">Specifies whether to allow Azure RMS encryption for WIP Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="39561-183">iconsVisible</span><span class="sxs-lookup"><span data-stu-id="39561-183">iconsVisible</span></span>|<span data-ttu-id="39561-184">Booleano</span><span class="sxs-lookup"><span data-stu-id="39561-184">Boolean</span></span>|<span data-ttu-id="39561-185">Determina si se agregan las superposiciones a los iconos para los archivos protegidos mediante WIP en Explorer y en los iconos de aplicación solo de empresa en el menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="39561-185">Determines whether overlays are added to icons for WIP protected files in Explorer and enterprise only app tiles in the Start menu.</span></span> <span data-ttu-id="39561-186">A partir de Windows 10, versión 1703, estos ajustes también configuran la visibilidad del icono de WIP en la barra de título de una aplicación protegida mediante WIP. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="39561-186">Starting in Windows 10, version 1703 this setting also configures the visibility of the WIP icon in the title bar of a WIP-protected app Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="39561-187">protectedApps</span><span class="sxs-lookup"><span data-stu-id="39561-187">protectedApps</span></span>|<span data-ttu-id="39561-188">Colección [windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="39561-188">[windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md) collection</span></span>|<span data-ttu-id="39561-189">Las aplicaciones protegidas pueden tener acceso a datos empresariales y los datos controlados por dichas aplicaciones están protegidos mediante cifrado. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="39561-189">Protected applications can access enterprise data and the data handled by those applications are protected with encryption Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="39561-190">exemptApps</span><span class="sxs-lookup"><span data-stu-id="39561-190">exemptApps</span></span>|<span data-ttu-id="39561-191">Colección [windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="39561-191">[windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md) collection</span></span>|<span data-ttu-id="39561-192">Las aplicaciones exentas también pueden tener acceso a datos empresariales, pero los datos controlados por dichas aplicaciones no están protegidos.</span><span class="sxs-lookup"><span data-stu-id="39561-192">Exempt applications can also access enterprise data, but the data handled by those applications are not protected.</span></span> <span data-ttu-id="39561-193">Esto ocurre porque algunas aplicaciones empresariales críticas podrían tener problemas de compatibilidad con los datos cifrados.</span><span class="sxs-lookup"><span data-stu-id="39561-193">This is because some critical enterprise applications may have compatibility problems with encrypted data.</span></span> <span data-ttu-id="39561-194">Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="39561-194">Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="39561-195">enterpriseNetworkDomainNames</span><span class="sxs-lookup"><span data-stu-id="39561-195">enterpriseNetworkDomainNames</span></span>|<span data-ttu-id="39561-196">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="39561-196">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="39561-197">Esta es la lista de dominios que forman parte de los límites de la empresa.</span><span class="sxs-lookup"><span data-stu-id="39561-197">This is the list of domains that comprise the boundaries of the enterprise.</span></span> <span data-ttu-id="39561-198">Los datos de uno de estos dominios que se envíen a un dispositivo se considerarán datos empresariales y protegidos. Estas ubicaciones se consideran un destino seguro con el que compartir datos empresariales. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="39561-198">Data from one of these domains that is sent to a device will be considered enterprise data and protected These locations will be considered a safe destination for enterprise data to be shared to Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="39561-199">enterpriseProxiedDomains</span><span class="sxs-lookup"><span data-stu-id="39561-199">enterpriseProxiedDomains</span></span>|<span data-ttu-id="39561-200">Colección [windowsInformationProtectionProxiedDomainCollection](../resources/intune_mam_windowsinformationprotectionproxieddomaincollection.md)</span><span class="sxs-lookup"><span data-stu-id="39561-200">[windowsInformationProtectionProxiedDomainCollection](../resources/intune_mam_windowsinformationprotectionproxieddomaincollection.md) collection</span></span>|<span data-ttu-id="39561-201">Contiene una lista de dominios de recursos empresariales hospedados en la nube que necesitan protección.</span><span class="sxs-lookup"><span data-stu-id="39561-201">Contains a list of Enterprise resource domains hosted in the cloud that need to be protected.</span></span> <span data-ttu-id="39561-202">Las conexiones a estos recursos se consideran datos empresariales.</span><span class="sxs-lookup"><span data-stu-id="39561-202">Connections to these resources are considered enterprise data.</span></span> <span data-ttu-id="39561-203">Si un proxy se corresponde con un recurso de nube, el tráfico al recurso de la nube se dirigirá a través de la red empresarial mediante el servidor proxy indicado (en el puerto 80).</span><span class="sxs-lookup"><span data-stu-id="39561-203">If a proxy is paired with a cloud resource, traffic to the cloud resource will be routed through the enterprise network via the denoted proxy server (on Port 80).</span></span> <span data-ttu-id="39561-204">Un servidor proxy que se use con esta finalidad debe configurarse también mediante la directiva EnterpriseInternalProxyServers. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="39561-204">A proxy server used for this purpose must also be configured using the EnterpriseInternalProxyServers policy Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="39561-205">enterpriseIPRanges</span><span class="sxs-lookup"><span data-stu-id="39561-205">enterpriseIPRanges</span></span>|<span data-ttu-id="39561-206">Colección [windowsInformationProtectionIPRangeCollection](../resources/intune_mam_windowsinformationprotectioniprangecollection.md)</span><span class="sxs-lookup"><span data-stu-id="39561-206">[windowsInformationProtectionIPRangeCollection](../resources/intune_mam_windowsinformationprotectioniprangecollection.md) collection</span></span>|<span data-ttu-id="39561-207">Establece los intervalos IP empresariales que definen los equipos de la red empresarial.</span><span class="sxs-lookup"><span data-stu-id="39561-207">Sets the enterprise IP ranges that define the computers in the enterprise network.</span></span> <span data-ttu-id="39561-208">Los datos que provienen de dichos equipos se consideran parte de la empresa y están protegidos.</span><span class="sxs-lookup"><span data-stu-id="39561-208">Data that comes from those computers will be considered part of the enterprise and protected.</span></span> <span data-ttu-id="39561-209">Estas ubicaciones se consideran un destino seguro en el que compartir datos empresariales. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="39561-209">These locations will be considered a safe destination for enterprise data to be shared to Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="39561-210">enterpriseIPRangesAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="39561-210">enterpriseIPRangesAreAuthoritative</span></span>|<span data-ttu-id="39561-211">Booleano</span><span class="sxs-lookup"><span data-stu-id="39561-211">Boolean</span></span>|<span data-ttu-id="39561-212">Valor booleano que indica al cliente que acepte la lista configurada y que no use la heurística para intentar buscar otras subredes.</span><span class="sxs-lookup"><span data-stu-id="39561-212">Boolean value that tells the client to accept the configured list and not to use heuristics to attempt to find other subnets.</span></span> <span data-ttu-id="39561-213">El valor predeterminado es False. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="39561-213">Default is false Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="39561-214">enterpriseProxyServers</span><span class="sxs-lookup"><span data-stu-id="39561-214">enterpriseProxyServers</span></span>|<span data-ttu-id="39561-215">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="39561-215">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="39561-216">Esta es una lista de servidores proxy.</span><span class="sxs-lookup"><span data-stu-id="39561-216">This is a list of proxy servers.</span></span> <span data-ttu-id="39561-217">Cualquier servidor que no esté en esta lista se considera no empresarial. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="39561-217">Any server not on this list is considered non-enterprise Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="39561-218">enterpriseInternalProxyServers</span><span class="sxs-lookup"><span data-stu-id="39561-218">enterpriseInternalProxyServers</span></span>|<span data-ttu-id="39561-219">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="39561-219">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="39561-220">Se trata de la lista de valores separados por comas de servidores proxy internos.</span><span class="sxs-lookup"><span data-stu-id="39561-220">This is the comma-separated list of internal proxy servers.</span></span> <span data-ttu-id="39561-221">Por ejemplo, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span><span class="sxs-lookup"><span data-stu-id="39561-221">For example, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span></span> <span data-ttu-id="39561-222">El administrador ha configurado estos servidores proxy para que se conecten a los recursos específicos de Internet.</span><span class="sxs-lookup"><span data-stu-id="39561-222">These proxies have been configured by the admin to connect to specific resources on the Internet.</span></span> <span data-ttu-id="39561-223">Se consideran ubicaciones de red empresarial.</span><span class="sxs-lookup"><span data-stu-id="39561-223">They are considered to be enterprise network locations.</span></span> <span data-ttu-id="39561-224">Los servidores proxy solo se usan al configurar la directiva EnterpriseProxiedDomains para forzar el tráfico a los dominios coincidentes mediante estos proxy. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="39561-224">The proxies are only leveraged in configuring the EnterpriseProxiedDomains policy to force traffic to the matched domains through these proxies Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="39561-225">enterpriseProxyServersAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="39561-225">enterpriseProxyServersAreAuthoritative</span></span>|<span data-ttu-id="39561-226">Booleano</span><span class="sxs-lookup"><span data-stu-id="39561-226">Boolean</span></span>|<span data-ttu-id="39561-227">Valor booleano que indica al cliente que acepte la lista de configuración de servidores proxy y no intente detectar otros servidores proxy de trabajo.</span><span class="sxs-lookup"><span data-stu-id="39561-227">Boolean value that tells the client to accept the configured list of proxies and not try to detect other work proxies.</span></span> <span data-ttu-id="39561-228">El valor predeterminado es False. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="39561-228">Default is false Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="39561-229">neutralDomainResources</span><span class="sxs-lookup"><span data-stu-id="39561-229">neutralDomainResources</span></span>|<span data-ttu-id="39561-230">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="39561-230">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="39561-231">Lista de nombres de dominio que se pueden usar para el recurso de trabajo o personal. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="39561-231">List of domain names that can used for work or personal resource Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="39561-232">indexingEncryptedStoresOrItemsBlocked</span><span class="sxs-lookup"><span data-stu-id="39561-232">indexingEncryptedStoresOrItemsBlocked</span></span>|<span data-ttu-id="39561-233">Booleano</span><span class="sxs-lookup"><span data-stu-id="39561-233">Boolean</span></span>|<span data-ttu-id="39561-234">Este identificador es para que el indexador de Windows Search permita o impida la indexación de los elementos. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="39561-234">This switch is for the Windows Search Indexer, to allow or disallow indexing of items Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="39561-235">smbAutoEncryptedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="39561-235">smbAutoEncryptedFileExtensions</span></span>|<span data-ttu-id="39561-236">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="39561-236">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="39561-237">Especifica una lista de extensiones de archivo, para que los archivos con estas extensiones se cifren cuando se copian desde un recurso compartido de SMB dentro del límite de la empresa. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="39561-237">Specifies a list of file extensions, so that files with these extensions are encrypted when copying from an SMB share within the corporate boundary Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="39561-238">isAssigned</span><span class="sxs-lookup"><span data-stu-id="39561-238">isAssigned</span></span>|<span data-ttu-id="39561-239">Booleano</span><span class="sxs-lookup"><span data-stu-id="39561-239">Boolean</span></span>|<span data-ttu-id="39561-240">Indica si la directiva se implementará en los grupos de inclusión.</span><span class="sxs-lookup"><span data-stu-id="39561-240">Indicates if the policy is deployed to any inclusion groups or not.</span></span> <span data-ttu-id="39561-241">Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="39561-241">Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="39561-242">revokeOnMdmHandoffDisabled</span><span class="sxs-lookup"><span data-stu-id="39561-242">revokeOnMdmHandoffDisabled</span></span>|<span data-ttu-id="39561-243">Booleano</span><span class="sxs-lookup"><span data-stu-id="39561-243">Boolean</span></span>|<span data-ttu-id="39561-244">Nueva propiedad en RS2, pendiente de documentación.</span><span class="sxs-lookup"><span data-stu-id="39561-244">New property in RS2, pending documentation</span></span>|
|<span data-ttu-id="39561-245">mdmEnrollmentUrl</span><span class="sxs-lookup"><span data-stu-id="39561-245">mdmEnrollmentUrl</span></span>|<span data-ttu-id="39561-246">Cadena</span><span class="sxs-lookup"><span data-stu-id="39561-246">String</span></span>|<span data-ttu-id="39561-247">Dirección URL de la inscripción para MDM.</span><span class="sxs-lookup"><span data-stu-id="39561-247">Enrollment url for the MDM</span></span>|
|<span data-ttu-id="39561-248">windowsHelloForBusinessBlocked</span><span class="sxs-lookup"><span data-stu-id="39561-248">windowsHelloForBusinessBlocked</span></span>|<span data-ttu-id="39561-249">Booleano</span><span class="sxs-lookup"><span data-stu-id="39561-249">Boolean</span></span>|<span data-ttu-id="39561-250">Valor booleano que establece Windows Hello para empresas como método de inicio de sesión en Windows.</span><span class="sxs-lookup"><span data-stu-id="39561-250">Boolean value that sets Windows Hello for Business as a method for signing into Windows.</span></span>|
|<span data-ttu-id="39561-251">pinMinimumLength</span><span class="sxs-lookup"><span data-stu-id="39561-251">pinMinimumLength</span></span>|<span data-ttu-id="39561-252">Int32</span><span class="sxs-lookup"><span data-stu-id="39561-252">Int32</span></span>|<span data-ttu-id="39561-253">Valor entero que establece el número mínimo de caracteres necesarios para el PIN.</span><span class="sxs-lookup"><span data-stu-id="39561-253">Integer value that sets the minimum number of characters required for the PIN.</span></span> <span data-ttu-id="39561-254">El valor predeterminado es 4.</span><span class="sxs-lookup"><span data-stu-id="39561-254">Default value is 4.</span></span> <span data-ttu-id="39561-255">El número más bajo que se puede configurar para esta configuración de directiva es 4.</span><span class="sxs-lookup"><span data-stu-id="39561-255">The lowest number you can configure for this policy setting is 4.</span></span> <span data-ttu-id="39561-256">El número más alto que se puede configurar debe ser menor que el número establecido en la configuración de directiva de longitud máxima del PIN o el número 127, el que sea más bajo.</span><span class="sxs-lookup"><span data-stu-id="39561-256">The largest number you can configure must be less than the number configured in the Maximum PIN length policy setting or the number 127, whichever is the lowest.</span></span>|
|<span data-ttu-id="39561-257">pinUppercaseLetters</span><span class="sxs-lookup"><span data-stu-id="39561-257">pinUppercaseLetters</span></span>|[<span data-ttu-id="39561-258">windowsInformationProtectionPinCharacterRequirements</span><span class="sxs-lookup"><span data-stu-id="39561-258">windowsInformationProtectionPinCharacterRequirements</span></span>](../resources/intune_mam_windowsinformationprotectionpincharacterrequirements.md)|<span data-ttu-id="39561-p123">Valor entero que configura el uso de mayúsculas en el PIN de Windows Hello para empresas. El valor predeterminado es NotAllow. Los valores posibles son: `notAllow`, `requireAtLeastOne`, `allow`.</span><span class="sxs-lookup"><span data-stu-id="39561-p123">Integer value that configures the use of uppercase letters in the Windows Hello for Business PIN. Default is NotAllow. The possible values are: `notAllow`, `requireAtLeastOne`, `allow`.</span></span>|
|<span data-ttu-id="39561-262">pinLowercaseLetters</span><span class="sxs-lookup"><span data-stu-id="39561-262">pinLowercaseLetters</span></span>|[<span data-ttu-id="39561-263">windowsInformationProtectionPinCharacterRequirements</span><span class="sxs-lookup"><span data-stu-id="39561-263">windowsInformationProtectionPinCharacterRequirements</span></span>](../resources/intune_mam_windowsinformationprotectionpincharacterrequirements.md)|<span data-ttu-id="39561-p124">Valor entero que configura el uso de minúscula en el PIN de Windows Hello para empresas. El valor predeterminado es NotAllow. Los valores posibles son: `notAllow`, `requireAtLeastOne`, `allow`.</span><span class="sxs-lookup"><span data-stu-id="39561-p124">Integer value that configures the use of lowercase letters in the Windows Hello for Business PIN. Default is NotAllow. The possible values are: `notAllow`, `requireAtLeastOne`, `allow`.</span></span>|
|<span data-ttu-id="39561-267">pinSpecialCharacters</span><span class="sxs-lookup"><span data-stu-id="39561-267">pinSpecialCharacters</span></span>|[<span data-ttu-id="39561-268">windowsInformationProtectionPinCharacterRequirements</span><span class="sxs-lookup"><span data-stu-id="39561-268">windowsInformationProtectionPinCharacterRequirements</span></span>](../resources/intune_mam_windowsinformationprotectionpincharacterrequirements.md)|<span data-ttu-id="39561-269">Valor entero que configura el uso de caracteres especiales en el PIN de Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="39561-269">Integer value that configures the use of special characters in the Windows Hello for Business PIN.</span></span> <span data-ttu-id="39561-270">Los caracteres especiales válidos para el PIN de Windows Hello para empresas incluyen: !</span><span class="sxs-lookup"><span data-stu-id="39561-270">Valid special characters for Windows Hello for Business PIN gestures include: !</span></span> <span data-ttu-id="39561-271">" # $ % & ' ( ) \* + , - .</span><span class="sxs-lookup"><span data-stu-id="39561-271">" # $ % & ' ( ) \* + , - .</span></span> <span data-ttu-id="39561-272">/ : ; < = > ?</span><span class="sxs-lookup"><span data-stu-id="39561-272">/ : ; < = > ?</span></span><span data-ttu-id="39561-273"> @ \[ \ \] ^ _ \` {</span><span class="sxs-lookup"><span data-stu-id="39561-273"> @ \[ \ \] ^ _ \` {</span></span> | <span data-ttu-id="39561-p126">} ~. El valor predeterminado es NotAllow. Los valores posibles son: `notAllow`, `requireAtLeastOne`, `allow`.</span><span class="sxs-lookup"><span data-stu-id="39561-p126">} ~. Default is NotAllow. The possible values are: `notAllow`, `requireAtLeastOne`, `allow`.</span></span>|
|<span data-ttu-id="39561-277">pinExpirationDays</span><span class="sxs-lookup"><span data-stu-id="39561-277">pinExpirationDays</span></span>|<span data-ttu-id="39561-278">Int32</span><span class="sxs-lookup"><span data-stu-id="39561-278">Int32</span></span>|<span data-ttu-id="39561-279">Valor entero que especifica el período de tiempo (en días) que se puede usar un PIN antes de que el sistema solicite que el usuario lo cambie.</span><span class="sxs-lookup"><span data-stu-id="39561-279">Integer value specifies the period of time (in days) that a PIN can be used before the system requires the user to change it.</span></span> <span data-ttu-id="39561-280">El número más alto que puede configurar para esta configuración de directiva es 730.</span><span class="sxs-lookup"><span data-stu-id="39561-280">The largest number you can configure for this policy setting is 730.</span></span> <span data-ttu-id="39561-281">El número más bajo que puede configurar para esta configuración de directiva es 0.</span><span class="sxs-lookup"><span data-stu-id="39561-281">The lowest number you can configure for this policy setting is 0.</span></span> <span data-ttu-id="39561-282">Si esta directiva se establece en 0, el PIN del usuario nunca expirará.</span><span class="sxs-lookup"><span data-stu-id="39561-282">If this policy is set to 0, then the user's PIN will never expire.</span></span> <span data-ttu-id="39561-283">Este nodo se agregó en Windows 10, versión 1511.</span><span class="sxs-lookup"><span data-stu-id="39561-283">This node was added in Windows 10, version 1511.</span></span> <span data-ttu-id="39561-284">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="39561-284">Default is 0.</span></span>|
|<span data-ttu-id="39561-285">numberOfPastPinsRemembered</span><span class="sxs-lookup"><span data-stu-id="39561-285">numberOfPastPinsRemembered</span></span>|<span data-ttu-id="39561-286">Int32</span><span class="sxs-lookup"><span data-stu-id="39561-286">Int32</span></span>|<span data-ttu-id="39561-287">Valor entero que especifica el número de PIN anteriores que se pueden asociar a una cuenta de usuario que no se pueden volver a usar.</span><span class="sxs-lookup"><span data-stu-id="39561-287">Integer value that specifies the number of past PINs that can be associated to a user account that can't be reused.</span></span> <span data-ttu-id="39561-288">El número más alto que puede configurar para esta configuración de directiva es 50.</span><span class="sxs-lookup"><span data-stu-id="39561-288">The largest number you can configure for this policy setting is 50.</span></span> <span data-ttu-id="39561-289">El número más bajo que puede configurar para esta configuración de directiva es 0.</span><span class="sxs-lookup"><span data-stu-id="39561-289">The lowest number you can configure for this policy setting is 0.</span></span> <span data-ttu-id="39561-290">Si esta directiva se establece en 0, no es necesario almacenar los PIN antiguos.</span><span class="sxs-lookup"><span data-stu-id="39561-290">If this policy is set to 0, then storage of previous PINs is not required.</span></span> <span data-ttu-id="39561-291">Este nodo se agregó en Windows 10, versión 1511.</span><span class="sxs-lookup"><span data-stu-id="39561-291">This node was added in Windows 10, version 1511.</span></span> <span data-ttu-id="39561-292">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="39561-292">Default is 0.</span></span>|
|<span data-ttu-id="39561-293">passwordMaximumAttemptCount</span><span class="sxs-lookup"><span data-stu-id="39561-293">passwordMaximumAttemptCount</span></span>|<span data-ttu-id="39561-294">Int32</span><span class="sxs-lookup"><span data-stu-id="39561-294">Int32</span></span>|<span data-ttu-id="39561-295">Número de errores de autenticación permitidos antes de que se borre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="39561-295">The number of authentication failures allowed before the device will be wiped.</span></span> <span data-ttu-id="39561-296">Un valor de 0 deshabilita la funcionalidad de borrado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="39561-296">A value of 0 disables device wipe functionality.</span></span> <span data-ttu-id="39561-297">El intervalo es un entero X donde 4 < = X < = 16 para equipos de escritorio y 0 < = X < = 999 para dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="39561-297">Range is an integer X where 4 <= X <= 16 for desktop and 0 <= X <= 999 for mobile devices.</span></span>|
|<span data-ttu-id="39561-298">minutesOfInactivityBeforeDeviceLock</span><span class="sxs-lookup"><span data-stu-id="39561-298">minutesOfInactivityBeforeDeviceLock</span></span>|<span data-ttu-id="39561-299">Int32</span><span class="sxs-lookup"><span data-stu-id="39561-299">Int32</span></span>|<span data-ttu-id="39561-300">Especifica la cantidad máxima de tiempo (en minutos) permitida después de que el dispositivo esté inactivo que hará que el dispositivo esté bloqueado con PIN o contraseña.</span><span class="sxs-lookup"><span data-stu-id="39561-300">Specifies the maximum amount of time (in minutes) allowed after the device is idle that will cause the device to become PIN or password locked.</span></span>   <span data-ttu-id="39561-301">El intervalo es un entero X, donde 0 < = X < = 999.</span><span class="sxs-lookup"><span data-stu-id="39561-301">Range is an integer X where 0 <= X <= 999.</span></span>|
|<span data-ttu-id="39561-302">daysWithoutContactBeforeUnenroll</span><span class="sxs-lookup"><span data-stu-id="39561-302">daysWithoutContactBeforeUnenroll</span></span>|<span data-ttu-id="39561-303">Int32</span><span class="sxs-lookup"><span data-stu-id="39561-303">Int32</span></span>|<span data-ttu-id="39561-304">Intervalo sin conexión antes de que se borren los datos de la aplicación (días)</span><span class="sxs-lookup"><span data-stu-id="39561-304">Offline interval before app data is wiped (days)</span></span> |



## <a name="response"></a><span data-ttu-id="39561-305">Respuesta</span><span class="sxs-lookup"><span data-stu-id="39561-305">Response</span></span>
<span data-ttu-id="39561-306">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsInformationProtectionPolicy](../resources/intune_mam_windowsinformationprotectionpolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="39561-306">If successful, this method returns a `201 Created` response code and a [windowsInformationProtectionPolicy](../resources/intune_mam_windowsinformationprotectionpolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="39561-307">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="39561-307">Example</span></span>
### <a name="request"></a><span data-ttu-id="39561-308">Solicitud</span><span class="sxs-lookup"><span data-stu-id="39561-308">Request</span></span>
<span data-ttu-id="39561-309">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="39561-309">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/windowsInformationProtectionPolicies
Content-type: application/json
Content-length: 4466

{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionPolicy",
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
  "isAssigned": true,
  "revokeOnMdmHandoffDisabled": true,
  "mdmEnrollmentUrl": "https://example.com/mdmEnrollmentUrl/",
  "windowsHelloForBusinessBlocked": true,
  "pinMinimumLength": 0,
  "pinUppercaseLetters": "requireAtLeastOne",
  "pinLowercaseLetters": "requireAtLeastOne",
  "pinSpecialCharacters": "requireAtLeastOne",
  "pinExpirationDays": 1,
  "numberOfPastPinsRemembered": 10,
  "passwordMaximumAttemptCount": 11,
  "minutesOfInactivityBeforeDeviceLock": 3,
  "daysWithoutContactBeforeUnenroll": 0
}
```

### <a name="response"></a><span data-ttu-id="39561-310">Respuesta</span><span class="sxs-lookup"><span data-stu-id="39561-310">Response</span></span>
<span data-ttu-id="39561-p131">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="39561-p131">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 4574

{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionPolicy",
  "displayName": "Display Name value",
  "description": "Description value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "id": "6397be61-be61-6397-61be-976361be9763",
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
  "isAssigned": true,
  "revokeOnMdmHandoffDisabled": true,
  "mdmEnrollmentUrl": "https://example.com/mdmEnrollmentUrl/",
  "windowsHelloForBusinessBlocked": true,
  "pinMinimumLength": 0,
  "pinUppercaseLetters": "requireAtLeastOne",
  "pinLowercaseLetters": "requireAtLeastOne",
  "pinSpecialCharacters": "requireAtLeastOne",
  "pinExpirationDays": 1,
  "numberOfPastPinsRemembered": 10,
  "passwordMaximumAttemptCount": 11,
  "minutesOfInactivityBeforeDeviceLock": 3,
  "daysWithoutContactBeforeUnenroll": 0
}
```








