# <a name="windowsinformationprotection-resource-type"></a><span data-ttu-id="f4915-101">Tipo de recurso windowsInformationProtection</span><span class="sxs-lookup"><span data-stu-id="f4915-101">windowsInformationProtection resource type</span></span>

> <span data-ttu-id="f4915-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f4915-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f4915-103">Directiva de Windows Information Protection para configurar las opciones de administración detalladas</span><span class="sxs-lookup"><span data-stu-id="f4915-103">Policy for Windows information protection to configure detailed management settings</span></span>

<span data-ttu-id="f4915-104">Hereda de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="f4915-104">Inherits from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>

## <a name="methods"></a><span data-ttu-id="f4915-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="f4915-105">Methods</span></span>
|<span data-ttu-id="f4915-106">Método</span><span class="sxs-lookup"><span data-stu-id="f4915-106">Method</span></span>|<span data-ttu-id="f4915-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f4915-107">Return Type</span></span>|<span data-ttu-id="f4915-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4915-108">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="f4915-109">Enumerar windowsInformationProtections</span><span class="sxs-lookup"><span data-stu-id="f4915-109">List windowsInformationProtections</span></span>](../api/intune_mam_windowsinformationprotection_list.md)|<span data-ttu-id="f4915-110">Colección [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="f4915-110">[windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) collection</span></span>|<span data-ttu-id="f4915-111">Enumere las propiedades y las relaciones de los objetos [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="f4915-111">List properties and relationships of the [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) objects.</span></span>|
|[<span data-ttu-id="f4915-112">Obtener windowsInformationProtection</span><span class="sxs-lookup"><span data-stu-id="f4915-112">Get windowsInformationProtection</span></span>](../api/intune_mam_windowsinformationprotection_get.md)|[<span data-ttu-id="f4915-113">windowsInformationProtection</span><span class="sxs-lookup"><span data-stu-id="f4915-113">windowsInformationProtection</span></span>](../resources/intune_mam_windowsinformationprotection.md)|<span data-ttu-id="f4915-114">Lea las propiedades y las relaciones del objeto [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="f4915-114">Read properties and relationships of the [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) object.</span></span>|
|[<span data-ttu-id="f4915-115">Acción assign</span><span class="sxs-lookup"><span data-stu-id="f4915-115">assign action</span></span>](../api/intune_mam_windowsinformationprotection_assign.md)|<span data-ttu-id="f4915-116">Ninguno</span><span class="sxs-lookup"><span data-stu-id="f4915-116">None</span></span>|<span data-ttu-id="f4915-117">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="f4915-117">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="f4915-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f4915-118">Properties</span></span>
|<span data-ttu-id="f4915-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f4915-119">Property</span></span>|<span data-ttu-id="f4915-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="f4915-120">Type</span></span>|<span data-ttu-id="f4915-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4915-121">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f4915-122">displayName</span><span class="sxs-lookup"><span data-stu-id="f4915-122">displayName</span></span>|<span data-ttu-id="f4915-123">String</span><span class="sxs-lookup"><span data-stu-id="f4915-123">String</span></span>|<span data-ttu-id="f4915-124">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="f4915-124">Policy display name.</span></span> <span data-ttu-id="f4915-125">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f4915-125">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="f4915-126">description</span><span class="sxs-lookup"><span data-stu-id="f4915-126">description</span></span>|<span data-ttu-id="f4915-127">String</span><span class="sxs-lookup"><span data-stu-id="f4915-127">String</span></span>|<span data-ttu-id="f4915-128">Descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="f4915-128">The policy's description.</span></span> <span data-ttu-id="f4915-129">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f4915-129">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="f4915-130">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="f4915-130">createdDateTime</span></span>|<span data-ttu-id="f4915-131">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f4915-131">DateTimeOffset</span></span>|<span data-ttu-id="f4915-132">Fecha y hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="f4915-132">The date and time the policy was created.</span></span> <span data-ttu-id="f4915-133">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f4915-133">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="f4915-134">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="f4915-134">lastModifiedDateTime</span></span>|<span data-ttu-id="f4915-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f4915-135">DateTimeOffset</span></span>|<span data-ttu-id="f4915-136">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="f4915-136">Last time the policy was modified.</span></span> <span data-ttu-id="f4915-137">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f4915-137">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="f4915-138">id</span><span class="sxs-lookup"><span data-stu-id="f4915-138">id</span></span>|<span data-ttu-id="f4915-139">String</span><span class="sxs-lookup"><span data-stu-id="f4915-139">String</span></span>|<span data-ttu-id="f4915-140">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f4915-140">Key of the entity.</span></span> <span data-ttu-id="f4915-141">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f4915-141">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="f4915-142">version</span><span class="sxs-lookup"><span data-stu-id="f4915-142">version</span></span>|<span data-ttu-id="f4915-143">String</span><span class="sxs-lookup"><span data-stu-id="f4915-143">String</span></span>|<span data-ttu-id="f4915-144">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f4915-144">Version of the entity.</span></span> <span data-ttu-id="f4915-145">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f4915-145">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="f4915-146">enforcementLevel</span><span class="sxs-lookup"><span data-stu-id="f4915-146">enforcementLevel</span></span>|[<span data-ttu-id="f4915-147">windowsInformationProtectionEnforcementLevel</span><span class="sxs-lookup"><span data-stu-id="f4915-147">windowsInformationProtectionEnforcementLevel</span></span>](../resources/intune_mam_windowsinformationprotectionenforcementlevel.md)|<span data-ttu-id="f4915-148">Nivel de aplicación de trabajo en curso. Vea la definición de enumeración para los valores admitidos.</span><span class="sxs-lookup"><span data-stu-id="f4915-148">WIP enforcement level.See the Enum definition for supported values.</span></span> <span data-ttu-id="f4915-149">Los valores posibles son: `noProtection`, `encryptAndAuditOnly`, `encryptAuditAndPrompt` y `encryptAuditAndBlock`.</span><span class="sxs-lookup"><span data-stu-id="f4915-149">Possible values are: `noProtection`, `encryptAndAuditOnly`, `encryptAuditAndPrompt`, `encryptAuditAndBlock`.</span></span>|
|<span data-ttu-id="f4915-150">enterpriseDomain</span><span class="sxs-lookup"><span data-stu-id="f4915-150">enterpriseDomain</span></span>|<span data-ttu-id="f4915-151">Cadena</span><span class="sxs-lookup"><span data-stu-id="f4915-151">String</span></span>|<span data-ttu-id="f4915-152">Dominio empresarial principal</span><span class="sxs-lookup"><span data-stu-id="f4915-152">Primary enterprise domain</span></span>|
|<span data-ttu-id="f4915-153">enterpriseProtectedDomainNames</span><span class="sxs-lookup"><span data-stu-id="f4915-153">enterpriseProtectedDomainNames</span></span>|<span data-ttu-id="f4915-154">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="f4915-154">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="f4915-155">Lista de dominios empresariales que quiere proteger</span><span class="sxs-lookup"><span data-stu-id="f4915-155">List of enterprise domains to be protected</span></span>|
|<span data-ttu-id="f4915-156">protectionUnderLockConfigRequired</span><span class="sxs-lookup"><span data-stu-id="f4915-156">protectionUnderLockConfigRequired</span></span>|<span data-ttu-id="f4915-157">Booleano</span><span class="sxs-lookup"><span data-stu-id="f4915-157">Boolean</span></span>|<span data-ttu-id="f4915-158">Especifica si es necesario configurar la protección en la característica de bloqueo (también conocida como cifrar con PIN)</span><span class="sxs-lookup"><span data-stu-id="f4915-158">Specifies whether the protection under lock feature (also known as encrypt under pin) should be configured</span></span>|
|<span data-ttu-id="f4915-159">dataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="f4915-159">dataRecoveryCertificate</span></span>|[<span data-ttu-id="f4915-160">windowsInformationProtectionDataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="f4915-160">windowsInformationProtectionDataRecoveryCertificate</span></span>](../resources/intune_mam_windowsinformationprotectiondatarecoverycertificate.md)|<span data-ttu-id="f4915-161">Especifica un certificado de recuperación que se puede usar para recuperar datos de archivos cifrados.</span><span class="sxs-lookup"><span data-stu-id="f4915-161">Specifies a recovery certificate that can be used for data recovery of encrypted files.</span></span> <span data-ttu-id="f4915-162">Esto es lo mismo que el certificado del agente de recuperación de datos (DRA) para el sistema de cifrado de archivos (EFS)</span><span class="sxs-lookup"><span data-stu-id="f4915-162">This is the same as the data recovery agent(DRA) certificate for encrypting file system(EFS)</span></span>|
|<span data-ttu-id="f4915-163">revokeOnUnenrollDisabled</span><span class="sxs-lookup"><span data-stu-id="f4915-163">revokeOnUnenrollDisabled</span></span>|<span data-ttu-id="f4915-164">Booleano</span><span class="sxs-lookup"><span data-stu-id="f4915-164">Boolean</span></span>|<span data-ttu-id="f4915-165">Esta directiva controla si se revocan las claves de trabajo en curso cuando se anula la inscripción de un dispositivo en el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="f4915-165">This policy controls whether to revoke the WIP keys when a device unenrolls from the management service.</span></span> <span data-ttu-id="f4915-166">Si se establece en 1 (no revocar las claves), no se revocarán las claves y el usuario seguirá teniendo acceso a archivos protegidos después de anular la inscripción.</span><span class="sxs-lookup"><span data-stu-id="f4915-166">If set to 1 (Don't revoke keys), the keys will not be revoked and the user will continue to have access to protected files after unenrollment.</span></span> <span data-ttu-id="f4915-167">Si no se revocan las claves, no habrá ninguna limpieza de archivos revocados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="f4915-167">If the keys are not revoked, there will be no revoked file cleanup subsequently.</span></span>|
|<span data-ttu-id="f4915-168">rightsManagementServicesTemplateId</span><span class="sxs-lookup"><span data-stu-id="f4915-168">rightsManagementServicesTemplateId</span></span>|<span data-ttu-id="f4915-169">Guid</span><span class="sxs-lookup"><span data-stu-id="f4915-169">Guid</span></span>|<span data-ttu-id="f4915-170">GUID de TemplateID que se va a usar para el cifrado RMS.</span><span class="sxs-lookup"><span data-stu-id="f4915-170">TemplateID GUID to use for RMS encryption.</span></span> <span data-ttu-id="f4915-171">La plantilla de RMS permite que el administrador de TI configure los detalles sobre quién tiene acceso a los archivos protegidos por RMS y durante cuánto tiempo tienen acceso</span><span class="sxs-lookup"><span data-stu-id="f4915-171">The RMS template allows the IT admin to configure the details about who has access to RMS-protected file and how long they have access</span></span>|
|<span data-ttu-id="f4915-172">azureRightsManagementServicesAllowed</span><span class="sxs-lookup"><span data-stu-id="f4915-172">azureRightsManagementServicesAllowed</span></span>|<span data-ttu-id="f4915-173">Booleano</span><span class="sxs-lookup"><span data-stu-id="f4915-173">Boolean</span></span>|<span data-ttu-id="f4915-174">Especifica si se permite el cifrado de Azure RMS para WIP.</span><span class="sxs-lookup"><span data-stu-id="f4915-174">Specifies whether to allow Azure RMS encryption for WIP</span></span>|
|<span data-ttu-id="f4915-175">iconsVisible</span><span class="sxs-lookup"><span data-stu-id="f4915-175">iconsVisible</span></span>|<span data-ttu-id="f4915-176">Booleano</span><span class="sxs-lookup"><span data-stu-id="f4915-176">Boolean</span></span>|<span data-ttu-id="f4915-177">Determina si se agregan las superposiciones a los iconos para los archivos protegidos mediante WIP en Explorer y en los iconos de aplicación solo de empresa en el menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="f4915-177">Determines whether overlays are added to icons for WIP protected files in Explorer and enterprise only app tiles in the Start menu.</span></span> <span data-ttu-id="f4915-178">A partir de Windows 10, versión 1703, estos ajustes también configuran la visibilidad del icono de WIP en la barra de título de una aplicación protegida mediante WIP</span><span class="sxs-lookup"><span data-stu-id="f4915-178">Starting in Windows 10, version 1703 this setting also configures the visibility of the WIP icon in the title bar of a WIP-protected app</span></span>|
|<span data-ttu-id="f4915-179">protectedApps</span><span class="sxs-lookup"><span data-stu-id="f4915-179">protectedApps</span></span>|<span data-ttu-id="f4915-180">Colección [windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="f4915-180">[windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md) collection</span></span>|<span data-ttu-id="f4915-181">Las aplicaciones protegidas pueden tener acceso a datos empresariales y los datos controlados por dichas aplicaciones están protegidos mediante cifrado</span><span class="sxs-lookup"><span data-stu-id="f4915-181">Protected applications can access enterprise data and the data handled by those applications are protected with encryption</span></span>|
|<span data-ttu-id="f4915-182">exemptApps</span><span class="sxs-lookup"><span data-stu-id="f4915-182">exemptApps</span></span>|<span data-ttu-id="f4915-183">Colección [windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="f4915-183">[windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md) collection</span></span>|<span data-ttu-id="f4915-184">Las aplicaciones exentas también pueden tener acceso a datos empresariales, pero los datos controlados por dichas aplicaciones no están protegidos.</span><span class="sxs-lookup"><span data-stu-id="f4915-184">Exempt applications can also access enterprise data, but the data handled by those applications are not protected.</span></span> <span data-ttu-id="f4915-185">Esto ocurre porque algunas aplicaciones empresariales críticas podrían tener problemas de compatibilidad con los datos cifrados.</span><span class="sxs-lookup"><span data-stu-id="f4915-185">This is because some critical enterprise applications may have compatibility problems with encrypted data.</span></span>|
|<span data-ttu-id="f4915-186">enterpriseNetworkDomainNames</span><span class="sxs-lookup"><span data-stu-id="f4915-186">enterpriseNetworkDomainNames</span></span>|<span data-ttu-id="f4915-187">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="f4915-187">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="f4915-188">Esta es la lista de dominios que forman parte de los límites de la empresa.</span><span class="sxs-lookup"><span data-stu-id="f4915-188">This is the list of domains that comprise the boundaries of the enterprise.</span></span> <span data-ttu-id="f4915-189">Los datos de uno de estos dominios que se envíen a un dispositivo se considerarán datos empresariales y protegidos. Estas ubicaciones se consideran un destino seguro con el que compartir datos empresariales</span><span class="sxs-lookup"><span data-stu-id="f4915-189">Data from one of these domains that is sent to a device will be considered enterprise data and protected These locations will be considered a safe destination for enterprise data to be shared to</span></span>|
|<span data-ttu-id="f4915-190">enterpriseProxiedDomains</span><span class="sxs-lookup"><span data-stu-id="f4915-190">enterpriseProxiedDomains</span></span>|<span data-ttu-id="f4915-191">Colección [windowsInformationProtectionProxiedDomainCollection](../resources/intune_mam_windowsinformationprotectionproxieddomaincollection.md)</span><span class="sxs-lookup"><span data-stu-id="f4915-191">[windowsInformationProtectionProxiedDomainCollection](../resources/intune_mam_windowsinformationprotectionproxieddomaincollection.md) collection</span></span>|<span data-ttu-id="f4915-192">Contiene una lista de dominios de recursos empresariales hospedados en la nube que necesitan protección.</span><span class="sxs-lookup"><span data-stu-id="f4915-192">Contains a list of Enterprise resource domains hosted in the cloud that need to be protected.</span></span> <span data-ttu-id="f4915-193">Las conexiones a estos recursos se consideran datos empresariales.</span><span class="sxs-lookup"><span data-stu-id="f4915-193">Connections to these resources are considered enterprise data.</span></span> <span data-ttu-id="f4915-194">Si un proxy se corresponde con un recurso de nube, el tráfico al recurso de la nube se dirigirá a través de la red empresarial mediante el servidor proxy indicado (en el puerto 80).</span><span class="sxs-lookup"><span data-stu-id="f4915-194">If a proxy is paired with a cloud resource, traffic to the cloud resource will be routed through the enterprise network via the denoted proxy server (on Port 80).</span></span> <span data-ttu-id="f4915-195">Un servidor proxy que se use para este propósito también debe configurarse mediante la directiva EnterpriseInternalProxyServers</span><span class="sxs-lookup"><span data-stu-id="f4915-195">A proxy server used for this purpose must also be configured using the EnterpriseInternalProxyServers policy</span></span>|
|<span data-ttu-id="f4915-196">enterpriseIPRanges</span><span class="sxs-lookup"><span data-stu-id="f4915-196">enterpriseIPRanges</span></span>|<span data-ttu-id="f4915-197">Colección [windowsInformationProtectionIPRangeCollection](../resources/intune_mam_windowsinformationprotectioniprangecollection.md)</span><span class="sxs-lookup"><span data-stu-id="f4915-197">[windowsInformationProtectionIPRangeCollection](../resources/intune_mam_windowsinformationprotectioniprangecollection.md) collection</span></span>|<span data-ttu-id="f4915-198">Establece los intervalos IP empresariales que definen los equipos de la red empresarial.</span><span class="sxs-lookup"><span data-stu-id="f4915-198">Sets the enterprise IP ranges that define the computers in the enterprise network.</span></span> <span data-ttu-id="f4915-199">Los datos que provienen de dichos equipos se consideran parte de la empresa y están protegidos.</span><span class="sxs-lookup"><span data-stu-id="f4915-199">Data that comes from those computers will be considered part of the enterprise and protected.</span></span> <span data-ttu-id="f4915-200">Estas ubicaciones se consideran un destino seguro en el que compartir datos empresariales</span><span class="sxs-lookup"><span data-stu-id="f4915-200">These locations will be considered a safe destination for enterprise data to be shared to</span></span>|
|<span data-ttu-id="f4915-201">enterpriseIPRangesAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="f4915-201">enterpriseIPRangesAreAuthoritative</span></span>|<span data-ttu-id="f4915-202">Booleano</span><span class="sxs-lookup"><span data-stu-id="f4915-202">Boolean</span></span>|<span data-ttu-id="f4915-203">Valor booleano que indica al cliente que acepte la lista configurada y que no use la heurística para intentar buscar otras subredes.</span><span class="sxs-lookup"><span data-stu-id="f4915-203">Boolean value that tells the client to accept the configured list and not to use heuristics to attempt to find other subnets.</span></span> <span data-ttu-id="f4915-204">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="f4915-204">Default is false</span></span>|
|<span data-ttu-id="f4915-205">enterpriseProxyServers</span><span class="sxs-lookup"><span data-stu-id="f4915-205">enterpriseProxyServers</span></span>|<span data-ttu-id="f4915-206">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="f4915-206">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="f4915-207">Esta es una lista de servidores proxy.</span><span class="sxs-lookup"><span data-stu-id="f4915-207">This is a list of proxy servers.</span></span> <span data-ttu-id="f4915-208">Cualquier servidor que no esté en esta lista se considera no empresarial</span><span class="sxs-lookup"><span data-stu-id="f4915-208">Any server not on this list is considered non-enterprise</span></span>|
|<span data-ttu-id="f4915-209">enterpriseInternalProxyServers</span><span class="sxs-lookup"><span data-stu-id="f4915-209">enterpriseInternalProxyServers</span></span>|<span data-ttu-id="f4915-210">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="f4915-210">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="f4915-211">Se trata de la lista de valores separados por comas de servidores proxy internos.</span><span class="sxs-lookup"><span data-stu-id="f4915-211">This is the comma-separated list of internal proxy servers.</span></span> <span data-ttu-id="f4915-212">Por ejemplo, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span><span class="sxs-lookup"><span data-stu-id="f4915-212">For example, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span></span> <span data-ttu-id="f4915-213">El administrador ha configurado estos servidores proxy para que se conecten a los recursos específicos de Internet.</span><span class="sxs-lookup"><span data-stu-id="f4915-213">These proxies have been configured by the admin to connect to specific resources on the Internet.</span></span> <span data-ttu-id="f4915-214">Se consideran ubicaciones de red empresarial.</span><span class="sxs-lookup"><span data-stu-id="f4915-214">They are considered to be enterprise network locations.</span></span> <span data-ttu-id="f4915-215">Los servidores proxy solo se usan para configurar la directiva EnterpriseProxiedDomains para forzar el tráfico a los dominios coincidentes mediante estos proxy</span><span class="sxs-lookup"><span data-stu-id="f4915-215">The proxies are only leveraged in configuring the EnterpriseProxiedDomains policy to force traffic to the matched domains through these proxies</span></span>|
|<span data-ttu-id="f4915-216">enterpriseProxyServersAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="f4915-216">enterpriseProxyServersAreAuthoritative</span></span>|<span data-ttu-id="f4915-217">Booleano</span><span class="sxs-lookup"><span data-stu-id="f4915-217">Boolean</span></span>|<span data-ttu-id="f4915-218">Valor booleano que indica al cliente que acepte la lista de configuración de servidores proxy y no intente detectar otros servidores proxy de trabajo.</span><span class="sxs-lookup"><span data-stu-id="f4915-218">Boolean value that tells the client to accept the configured list of proxies and not try to detect other work proxies.</span></span> <span data-ttu-id="f4915-219">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="f4915-219">Default is false</span></span>|
|<span data-ttu-id="f4915-220">neutralDomainResources</span><span class="sxs-lookup"><span data-stu-id="f4915-220">neutralDomainResources</span></span>|<span data-ttu-id="f4915-221">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="f4915-221">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="f4915-222">Lista de nombres de dominio que se pueden usar para el recurso de trabajo o personal</span><span class="sxs-lookup"><span data-stu-id="f4915-222">List of domain names that can used for work or personal resource</span></span>|
|<span data-ttu-id="f4915-223">indexingEncryptedStoresOrItemsBlocked</span><span class="sxs-lookup"><span data-stu-id="f4915-223">indexingEncryptedStoresOrItemsBlocked</span></span>|<span data-ttu-id="f4915-224">Booleano</span><span class="sxs-lookup"><span data-stu-id="f4915-224">Boolean</span></span>|<span data-ttu-id="f4915-225">Esta opción es para que el indexador de Windows Search permita o impida la indexación de los elementos</span><span class="sxs-lookup"><span data-stu-id="f4915-225">This switch is for the Windows Search Indexer, to allow or disallow indexing of items</span></span>|
|<span data-ttu-id="f4915-226">smbAutoEncryptedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="f4915-226">smbAutoEncryptedFileExtensions</span></span>|<span data-ttu-id="f4915-227">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="f4915-227">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="f4915-228">Especifica una lista de extensiones de archivo, para que los archivos con estas extensiones se cifren cuando se copian desde un recurso compartido de SMB dentro del límite de la empresa</span><span class="sxs-lookup"><span data-stu-id="f4915-228">Specifies a list of file extensions, so that files with these extensions are encrypted when copying from an SMB share within the corporate boundary</span></span>|
|<span data-ttu-id="f4915-229">isAssigned</span><span class="sxs-lookup"><span data-stu-id="f4915-229">isAssigned</span></span>|<span data-ttu-id="f4915-230">Booleano</span><span class="sxs-lookup"><span data-stu-id="f4915-230">Boolean</span></span>|<span data-ttu-id="f4915-231">Indica si la directiva se implementará en los grupos de inclusión o no.</span><span class="sxs-lookup"><span data-stu-id="f4915-231">Indicates if the policy is deployed to any inclusion groups or not.</span></span>|

## <a name="relationships"></a><span data-ttu-id="f4915-232">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f4915-232">Relationships</span></span>
|<span data-ttu-id="f4915-233">Relación</span><span class="sxs-lookup"><span data-stu-id="f4915-233">Relationship</span></span>|<span data-ttu-id="f4915-234">Tipo</span><span class="sxs-lookup"><span data-stu-id="f4915-234">Type</span></span>|<span data-ttu-id="f4915-235">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4915-235">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f4915-236">protectedAppLockerFiles</span><span class="sxs-lookup"><span data-stu-id="f4915-236">protectedAppLockerFiles</span></span>|<span data-ttu-id="f4915-237">Colección [windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md)</span><span class="sxs-lookup"><span data-stu-id="f4915-237">[windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md) collection</span></span>|<span data-ttu-id="f4915-238">Otra forma de introducir aplicaciones protegidas mediante archivos XML</span><span class="sxs-lookup"><span data-stu-id="f4915-238">Another way to input protected apps through xml files</span></span>|
|<span data-ttu-id="f4915-239">exemptAppLockerFiles</span><span class="sxs-lookup"><span data-stu-id="f4915-239">exemptAppLockerFiles</span></span>|<span data-ttu-id="f4915-240">Colección [windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md)</span><span class="sxs-lookup"><span data-stu-id="f4915-240">[windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md) collection</span></span>|<span data-ttu-id="f4915-241">Otra forma de introducir aplicaciones exentas mediante archivos XML</span><span class="sxs-lookup"><span data-stu-id="f4915-241">Another way to input exempt apps through xml files</span></span>|
|<span data-ttu-id="f4915-242">asignaciones</span><span class="sxs-lookup"><span data-stu-id="f4915-242">assignments</span></span>|<span data-ttu-id="f4915-243">Colección [targetedManagedAppPolicyAssignment](../resources/intune_mam_targetedmanagedapppolicyassignment.md)</span><span class="sxs-lookup"><span data-stu-id="f4915-243">[targetedManagedAppPolicyAssignment](../resources/intune_mam_targetedmanagedapppolicyassignment.md) collection</span></span>|<span data-ttu-id="f4915-244">Propiedad de navegación a la lista de grupos de seguridad destinados a la directiva.</span><span class="sxs-lookup"><span data-stu-id="f4915-244">Navigation property to list of security groups targeted for policy.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="f4915-245">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f4915-245">JSON Representation</span></span>
<span data-ttu-id="f4915-246">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f4915-246">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsInformationProtection"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtection",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "version": "String",
  "enforcementLevel": "String",
  "enterpriseDomain": "String",
  "enterpriseProtectedDomainNames": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "String",
      "resources": [
        "String"
      ]
    }
  ],
  "protectionUnderLockConfigRequired": true,
  "dataRecoveryCertificate": {
    "@odata.type": "microsoft.graph.windowsInformationProtectionDataRecoveryCertificate",
    "subjectName": "String",
    "description": "String",
    "expirationDateTime": "String (timestamp)",
    "certificate": "binary"
  },
  "revokeOnUnenrollDisabled": true,
  "rightsManagementServicesTemplateId": "Guid",
  "azureRightsManagementServicesAllowed": true,
  "iconsVisible": true,
  "protectedApps": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionApp",
      "displayName": "String",
      "description": "String",
      "publisherName": "String",
      "productName": "String",
      "denied": true
    }
  ],
  "exemptApps": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionApp",
      "displayName": "String",
      "description": "String",
      "publisherName": "String",
      "productName": "String",
      "denied": true
    }
  ],
  "enterpriseNetworkDomainNames": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "String",
      "resources": [
        "String"
      ]
    }
  ],
  "enterpriseProxiedDomains": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionProxiedDomainCollection",
      "displayName": "String",
      "proxiedDomains": [
        {
          "@odata.type": "microsoft.graph.proxiedDomain",
          "ipAddressOrFQDN": "String",
          "proxy": "String"
        }
      ]
    }
  ],
  "enterpriseIPRanges": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionIPRangeCollection",
      "displayName": "String",
      "ranges": [
        {
          "@odata.type": "microsoft.graph.iPv6Range",
          "lowerAddress": "String",
          "upperAddress": "String"
        }
      ]
    }
  ],
  "enterpriseIPRangesAreAuthoritative": true,
  "enterpriseProxyServers": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "String",
      "resources": [
        "String"
      ]
    }
  ],
  "enterpriseInternalProxyServers": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "String",
      "resources": [
        "String"
      ]
    }
  ],
  "enterpriseProxyServersAreAuthoritative": true,
  "neutralDomainResources": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "String",
      "resources": [
        "String"
      ]
    }
  ],
  "indexingEncryptedStoresOrItemsBlocked": true,
  "smbAutoEncryptedFileExtensions": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "String",
      "resources": [
        "String"
      ]
    }
  ],
  "isAssigned": true
}
```



