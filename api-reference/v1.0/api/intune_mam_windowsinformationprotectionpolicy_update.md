# <a name="update-windowsinformationprotectionpolicy"></a><span data-ttu-id="ee486-101">Actualizar windowsInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ee486-101">Update windowsInformationProtectionPolicy</span></span>

> <span data-ttu-id="ee486-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ee486-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ee486-103">Actualice las propiedades de un objeto [windowsInformationProtectionPolicy](../resources/intune_mam_windowsinformationprotectionpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-103">Update the properties of a [calendar](../resources/intune_mam_windowsinformationprotectionpolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ee486-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ee486-104">Prerequisites</span></span>
<span data-ttu-id="ee486-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ee486-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ee486-107">Permission type</span></span>|<span data-ttu-id="ee486-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ee486-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ee486-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ee486-109">Delegated (work or school account)</span></span>|<span data-ttu-id="ee486-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ee486-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="ee486-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ee486-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ee486-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ee486-112">Not supported.</span></span>|
|<span data-ttu-id="ee486-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ee486-113">Application</span></span>|<span data-ttu-id="ee486-114">No compatible.</span><span class="sxs-lookup"><span data-stu-id="ee486-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ee486-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ee486-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/windowsInformationProtectionPolicies/{windowsInformationProtectionPolicyId}
```

## <a name="request-headers"></a><span data-ttu-id="ee486-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ee486-116">Request headers</span></span>
|<span data-ttu-id="ee486-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee486-117">Header</span></span>|<span data-ttu-id="ee486-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ee486-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ee486-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="ee486-119">Authorization</span></span>|<span data-ttu-id="ee486-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ee486-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="ee486-121">Accept</span><span class="sxs-lookup"><span data-stu-id="ee486-121">Accept</span></span>|<span data-ttu-id="ee486-122">application/json</span><span class="sxs-lookup"><span data-stu-id="ee486-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ee486-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ee486-123">Request body</span></span>
<span data-ttu-id="ee486-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsInformationProtectionPolicy](../resources/intune_mam_windowsinformationprotectionpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_mam_windowsinformationprotectionpolicy.md) object.</span></span>

<span data-ttu-id="ee486-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsInformationProtectionPolicy](../resources/intune_mam_windowsinformationprotectionpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="ee486-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ee486-126">Property</span></span>|<span data-ttu-id="ee486-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="ee486-127">Type</span></span>|<span data-ttu-id="ee486-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee486-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ee486-129">displayName</span><span class="sxs-lookup"><span data-stu-id="ee486-129">displayName</span></span>|<span data-ttu-id="ee486-130">String</span><span class="sxs-lookup"><span data-stu-id="ee486-130">String</span></span>|<span data-ttu-id="ee486-131">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="ee486-131">Policy display name.</span></span> <span data-ttu-id="ee486-132">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-132">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="ee486-133">description</span><span class="sxs-lookup"><span data-stu-id="ee486-133">description</span></span>|<span data-ttu-id="ee486-134">String</span><span class="sxs-lookup"><span data-stu-id="ee486-134">String</span></span>|<span data-ttu-id="ee486-135">Descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="ee486-135">The policy's description.</span></span> <span data-ttu-id="ee486-136">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-136">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="ee486-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="ee486-137">createdDateTime</span></span>|<span data-ttu-id="ee486-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ee486-138">DateTimeOffset</span></span>|<span data-ttu-id="ee486-139">Fecha y hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="ee486-139">The date and time when the page was created.</span></span> <span data-ttu-id="ee486-140">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-140">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="ee486-141">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="ee486-141">lastModifiedDateTime</span></span>|<span data-ttu-id="ee486-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ee486-142">DateTimeOffset</span></span>|<span data-ttu-id="ee486-143">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="ee486-143">Last time the policy was modified.</span></span> <span data-ttu-id="ee486-144">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-144">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="ee486-145">id</span><span class="sxs-lookup"><span data-stu-id="ee486-145">id</span></span>|<span data-ttu-id="ee486-146">String</span><span class="sxs-lookup"><span data-stu-id="ee486-146">String</span></span>|<span data-ttu-id="ee486-147">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ee486-147">Key of the setting.</span></span> <span data-ttu-id="ee486-148">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-148">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="ee486-149">version</span><span class="sxs-lookup"><span data-stu-id="ee486-149">version</span></span>|<span data-ttu-id="ee486-150">String</span><span class="sxs-lookup"><span data-stu-id="ee486-150">String</span></span>|<span data-ttu-id="ee486-151">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ee486-151">Version of the entity.</span></span> <span data-ttu-id="ee486-152">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-152">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="ee486-153">enforcementLevel</span><span class="sxs-lookup"><span data-stu-id="ee486-153">enforcementLevel</span></span>|<span data-ttu-id="ee486-154">String</span><span class="sxs-lookup"><span data-stu-id="ee486-154">String</span></span>|<span data-ttu-id="ee486-155">Nivel de obligatoriedad del trabajo en curso. Vea la definición de enumeración para los valores compatibles. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md). Los valores posibles son: `noProtection`, `encryptAndAuditOnly`, `encryptAuditAndPrompt` y `encryptAuditAndBlock`.</span><span class="sxs-lookup"><span data-stu-id="ee486-155">WIP enforcement level.See the Enum definition for supported values Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) Possible values are: `noProtection`, `encryptAndAuditOnly`, `encryptAuditAndPrompt`, `encryptAuditAndBlock`.</span></span>|
|<span data-ttu-id="ee486-156">enterpriseDomain</span><span class="sxs-lookup"><span data-stu-id="ee486-156">enterpriseDomain</span></span>|<span data-ttu-id="ee486-157">String</span><span class="sxs-lookup"><span data-stu-id="ee486-157">String</span></span>|<span data-ttu-id="ee486-158">Dominio empresarial principal. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-158">Primary enterprise domain Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="ee486-159">enterpriseProtectedDomainNames</span><span class="sxs-lookup"><span data-stu-id="ee486-159">enterpriseProtectedDomainNames</span></span>|<span data-ttu-id="ee486-160">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="ee486-160">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="ee486-161">Lista de dominios de empresa que se van a proteger. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-161">List of enterprise domains to be protected Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="ee486-162">protectionUnderLockConfigRequired</span><span class="sxs-lookup"><span data-stu-id="ee486-162">protectionUnderLockConfigRequired</span></span>|<span data-ttu-id="ee486-163">Boolean</span><span class="sxs-lookup"><span data-stu-id="ee486-163">Boolean</span></span>|<span data-ttu-id="ee486-164">Especifica si es necesario configurar la protección en la característica de bloqueo (también conocida como cifrar con PIN). Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-164">Specifies whether the protection under lock feature (also known as encrypt under pin) should be configured Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="ee486-165">dataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="ee486-165">dataRecoveryCertificate</span></span>|[<span data-ttu-id="ee486-166">windowsInformationProtectionDataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="ee486-166">windowsInformationProtectionDataRecoveryCertificate</span></span>](../resources/intune_mam_windowsinformationprotectiondatarecoverycertificate.md)|<span data-ttu-id="ee486-167">Especifica un certificado de recuperación que se puede usar para recuperar datos de archivos cifrados.</span><span class="sxs-lookup"><span data-stu-id="ee486-167">Specifies a recovery certificate that can be used for data recovery of encrypted files.</span></span> <span data-ttu-id="ee486-168">Es lo mismo que el certificado del agente de recuperación de datos (DRA) para el sistema de cifrado de archivos (EFS). Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-168">This is the same as the data recovery agent(DRA) certificate for encrypting file system(EFS) Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="ee486-169">revokeOnUnenrollDisabled</span><span class="sxs-lookup"><span data-stu-id="ee486-169">revokeOnUnenrollDisabled</span></span>|<span data-ttu-id="ee486-170">Boolean</span><span class="sxs-lookup"><span data-stu-id="ee486-170">Boolean</span></span>|<span data-ttu-id="ee486-171">Esta directiva controla si se revocan las claves de trabajo en curso cuando se anula la inscripción de un dispositivo en el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="ee486-171">This policy controls whether to revoke the WIP keys when a device unenrolls from the management service.</span></span> <span data-ttu-id="ee486-172">Si se establece en 1 (No revocar las claves), no se revocarán las claves y el usuario seguirá teniendo acceso a archivos protegidos después de anular la inscripción.</span><span class="sxs-lookup"><span data-stu-id="ee486-172">If set to 1 (Don't revoke keys), the keys will not be revoked and the user will continue to have access to protected files after unenrollment.</span></span> <span data-ttu-id="ee486-173">Si no se revocan las claves, no habrá ninguna limpieza de archivos revocados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="ee486-173">If the keys are not revoked, there will be no revoked file cleanup subsequently.</span></span> <span data-ttu-id="ee486-174">Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-174">Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="ee486-175">rightsManagementServicesTemplateId</span><span class="sxs-lookup"><span data-stu-id="ee486-175">rightsManagementServicesTemplateId</span></span>|<span data-ttu-id="ee486-176">Guid</span><span class="sxs-lookup"><span data-stu-id="ee486-176">Guid</span></span>|<span data-ttu-id="ee486-177">GUID de TemplateID que se va a usar para el cifrado RMS.</span><span class="sxs-lookup"><span data-stu-id="ee486-177">TemplateID GUID to use for RMS encryption.</span></span> <span data-ttu-id="ee486-178">La plantilla de RMS permite que el administrador de TI configure los detalles sobre quién tiene acceso a los archivos protegidos por RMS y durante cuánto tiempo. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-178">The RMS template allows the IT admin to configure the details about who has access to RMS-protected file and how long they have access Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="ee486-179">azureRightsManagementServicesAllowed</span><span class="sxs-lookup"><span data-stu-id="ee486-179">azureRightsManagementServicesAllowed</span></span>|<span data-ttu-id="ee486-180">Boolean</span><span class="sxs-lookup"><span data-stu-id="ee486-180">Boolean</span></span>|<span data-ttu-id="ee486-181">Especifica si se permite el cifrado de Azure RMS para WIP. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-181">Specifies whether to allow Azure RMS encryption for WIP Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="ee486-182">iconsVisible</span><span class="sxs-lookup"><span data-stu-id="ee486-182">iconsVisible</span></span>|<span data-ttu-id="ee486-183">Boolean</span><span class="sxs-lookup"><span data-stu-id="ee486-183">Boolean</span></span>|<span data-ttu-id="ee486-184">Determina si se agregan superposiciones a los iconos para los archivos protegidos mediante WIP en Explorer y en los iconos de aplicación solo de empresa en el menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="ee486-184">Determines whether overlays are added to icons for WIP protected files in Explorer and enterprise only app tiles in the Start menu.</span></span> <span data-ttu-id="ee486-185">A partir de Windows 10, versión 1703, estos ajustes también configuran la visibilidad del icono de WIP en la barra de título de una aplicación protegida mediante WIP. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-185">Starting in Windows 10, version 1703 this setting also configures the visibility of the WIP icon in the title bar of a WIP-protected app Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="ee486-186">protectedApps</span><span class="sxs-lookup"><span data-stu-id="ee486-186">protectedApps</span></span>|<span data-ttu-id="ee486-187">Colección [windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="ee486-187">[windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md) collection</span></span>|<span data-ttu-id="ee486-188">Las aplicaciones protegidas pueden tener acceso a datos empresariales y los datos controlados por dichas aplicaciones están protegidos mediante cifrado. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-188">Protected applications can access enterprise data and the data handled by those applications are protected with encryption Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="ee486-189">exemptApps</span><span class="sxs-lookup"><span data-stu-id="ee486-189">exemptApps</span></span>|<span data-ttu-id="ee486-190">Colección [windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="ee486-190">[windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md) collection</span></span>|<span data-ttu-id="ee486-191">Las aplicaciones exentas también pueden tener acceso a datos empresariales, pero los datos controlados por dichas aplicaciones no están protegidos.</span><span class="sxs-lookup"><span data-stu-id="ee486-191">Exempt applications can also access enterprise data, but the data handled by those applications are not protected.</span></span> <span data-ttu-id="ee486-192">Esto se debe a que es posible que algunas aplicaciones empresariales críticas tengan problemas de compatibilidad con los datos cifrados.</span><span class="sxs-lookup"><span data-stu-id="ee486-192">This is because some critical enterprise applications may have compatibility problems with encrypted data.</span></span> <span data-ttu-id="ee486-193">Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-193">Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="ee486-194">enterpriseNetworkDomainNames</span><span class="sxs-lookup"><span data-stu-id="ee486-194">enterpriseNetworkDomainNames</span></span>|<span data-ttu-id="ee486-195">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="ee486-195">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="ee486-196">Se trata de la lista de dominios que forman parte de los límites de la empresa.</span><span class="sxs-lookup"><span data-stu-id="ee486-196">This is the list of domains that comprise the boundaries of the enterprise.</span></span> <span data-ttu-id="ee486-197">Los datos de uno de estos dominios que se envíen a un dispositivo se considerarán datos empresariales y protegidos. Estas ubicaciones se consideran un destino seguro con el que compartir datos empresariales. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-197">Data from one of these domains that is sent to a device will be considered enterprise data and protected These locations will be considered a safe destination for enterprise data to be shared to Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="ee486-198">enterpriseProxiedDomains</span><span class="sxs-lookup"><span data-stu-id="ee486-198">enterpriseProxiedDomains</span></span>|<span data-ttu-id="ee486-199">Colección [windowsInformationProtectionProxiedDomainCollection](../resources/intune_mam_windowsinformationprotectionproxieddomaincollection.md)</span><span class="sxs-lookup"><span data-stu-id="ee486-199">[windowsInformationProtectionProxiedDomainCollection](../resources/intune_mam_windowsinformationprotectionproxieddomaincollection.md) collection</span></span>|<span data-ttu-id="ee486-200">Contiene una lista de dominios de recursos empresariales hospedados en la nube que necesitan protección.</span><span class="sxs-lookup"><span data-stu-id="ee486-200">Contains a list of Enterprise resource domains hosted in the cloud that need to be protected.</span></span> <span data-ttu-id="ee486-201">Las conexiones a estos recursos se consideran datos empresariales.</span><span class="sxs-lookup"><span data-stu-id="ee486-201">Connections to these resources are considered enterprise data.</span></span> <span data-ttu-id="ee486-202">Si un proxy se corresponde con un recurso de nube, el tráfico al recurso de nube se dirigirá a través de la red empresarial mediante el servidor proxy indicado (en el puerto 80).</span><span class="sxs-lookup"><span data-stu-id="ee486-202">If a proxy is paired with a cloud resource, traffic to the cloud resource will be routed through the enterprise network via the denoted proxy server (on Port 80).</span></span> <span data-ttu-id="ee486-203">Un servidor proxy que se use con esta finalidad debe configurarse también mediante la directiva EnterpriseInternalProxyServers. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-203">A proxy server used for this purpose must also be configured using the EnterpriseInternalProxyServers policy Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="ee486-204">enterpriseIPRanges</span><span class="sxs-lookup"><span data-stu-id="ee486-204">enterpriseIPRanges</span></span>|<span data-ttu-id="ee486-205">Colección [windowsInformationProtectionIPRangeCollection](../resources/intune_mam_windowsinformationprotectioniprangecollection.md)</span><span class="sxs-lookup"><span data-stu-id="ee486-205">[windowsInformationProtectionIPRangeCollection](../resources/intune_mam_windowsinformationprotectioniprangecollection.md) collection</span></span>|<span data-ttu-id="ee486-206">Establece los intervalos IP empresariales que definen los equipos de la red empresarial.</span><span class="sxs-lookup"><span data-stu-id="ee486-206">Sets the enterprise IP ranges that define the computers in the enterprise network.</span></span> <span data-ttu-id="ee486-207">Los datos que provienen de dichos equipos se consideran parte de la empresa y están protegidos.</span><span class="sxs-lookup"><span data-stu-id="ee486-207">Data that comes from those computers will be considered part of the enterprise and protected.</span></span> <span data-ttu-id="ee486-208">Estas ubicaciones se consideran un destino seguro en el que compartir datos empresariales. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-208">These locations will be considered a safe destination for enterprise data to be shared to Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="ee486-209">enterpriseIPRangesAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="ee486-209">enterpriseIPRangesAreAuthoritative</span></span>|<span data-ttu-id="ee486-210">Boolean</span><span class="sxs-lookup"><span data-stu-id="ee486-210">Boolean</span></span>|<span data-ttu-id="ee486-211">Valor booleano que indica al cliente que acepte la lista configurada y que no use la heurística para intentar buscar otras subredes.</span><span class="sxs-lookup"><span data-stu-id="ee486-211">Boolean value that tells the client to accept the configured list and not to use heuristics to attempt to find other subnets.</span></span> <span data-ttu-id="ee486-212">El valor predeterminado es False. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-212">Default is false Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="ee486-213">enterpriseProxyServers</span><span class="sxs-lookup"><span data-stu-id="ee486-213">enterpriseProxyServers</span></span>|<span data-ttu-id="ee486-214">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="ee486-214">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="ee486-215">Se trata de una lista de servidores proxy.</span><span class="sxs-lookup"><span data-stu-id="ee486-215">This is a list of proxy servers.</span></span> <span data-ttu-id="ee486-216">Cualquier servidor que no esté en esta lista se considera no empresarial. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-216">Any server not on this list is considered non-enterprise Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="ee486-217">enterpriseInternalProxyServers</span><span class="sxs-lookup"><span data-stu-id="ee486-217">enterpriseInternalProxyServers</span></span>|<span data-ttu-id="ee486-218">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="ee486-218">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="ee486-219">Se trata de la lista de valores separados por comas de servidores proxy internos.</span><span class="sxs-lookup"><span data-stu-id="ee486-219">This is the comma-separated list of internal proxy servers.</span></span> <span data-ttu-id="ee486-220">Por ejemplo, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span><span class="sxs-lookup"><span data-stu-id="ee486-220">For example, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span></span> <span data-ttu-id="ee486-221">El administrador ha configurado estos servidores proxy para que se conecten a los recursos específicos de Internet.</span><span class="sxs-lookup"><span data-stu-id="ee486-221">These proxies have been configured by the admin to connect to specific resources on the Internet.</span></span> <span data-ttu-id="ee486-222">Se consideran ubicaciones de red empresarial.</span><span class="sxs-lookup"><span data-stu-id="ee486-222">They are considered to be enterprise network locations.</span></span> <span data-ttu-id="ee486-223">Los servidores proxy solo se usan al configurar la directiva EnterpriseProxiedDomains para forzar el tráfico a los dominios coincidentes mediante estos proxy. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-223">The proxies are only leveraged in configuring the EnterpriseProxiedDomains policy to force traffic to the matched domains through these proxies Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="ee486-224">enterpriseProxyServersAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="ee486-224">enterpriseProxyServersAreAuthoritative</span></span>|<span data-ttu-id="ee486-225">Boolean</span><span class="sxs-lookup"><span data-stu-id="ee486-225">Boolean</span></span>|<span data-ttu-id="ee486-226">Valor booleano que indica al cliente que acepte la lista configurada de servidores proxy y no intente detectar otros servidores proxy de trabajo.</span><span class="sxs-lookup"><span data-stu-id="ee486-226">Boolean value that tells the client to accept the configured list of proxies and not try to detect other work proxies.</span></span> <span data-ttu-id="ee486-227">El valor predeterminado es False. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-227">Default is false Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="ee486-228">neutralDomainResources</span><span class="sxs-lookup"><span data-stu-id="ee486-228">neutralDomainResources</span></span>|<span data-ttu-id="ee486-229">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="ee486-229">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="ee486-230">Lista de nombres de dominio que se pueden usar para el recurso de trabajo o personal. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-230">List of domain names that can used for work or personal resource Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="ee486-231">indexingEncryptedStoresOrItemsBlocked</span><span class="sxs-lookup"><span data-stu-id="ee486-231">indexingEncryptedStoresOrItemsBlocked</span></span>|<span data-ttu-id="ee486-232">Boolean</span><span class="sxs-lookup"><span data-stu-id="ee486-232">Boolean</span></span>|<span data-ttu-id="ee486-233">Este identificador es para que el indexador de Windows Search permita o impida la indexación de los elementos. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-233">This switch is for the Windows Search Indexer, to allow or disallow indexing of items Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="ee486-234">smbAutoEncryptedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="ee486-234">smbAutoEncryptedFileExtensions</span></span>|<span data-ttu-id="ee486-235">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="ee486-235">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="ee486-236">Especifica una lista de extensiones de archivo, para que los archivos con estas extensiones se cifren cuando se copian desde un recurso compartido de SMB dentro del límite de la empresa. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-236">Specifies a list of file extensions, so that files with these extensions are encrypted when copying from an SMB share within the corporate boundary Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="ee486-237">isAssigned</span><span class="sxs-lookup"><span data-stu-id="ee486-237">isAssigned</span></span>|<span data-ttu-id="ee486-238">Boolean</span><span class="sxs-lookup"><span data-stu-id="ee486-238">Boolean</span></span>|<span data-ttu-id="ee486-239">Indica si la directiva se implementará en los grupos de inclusión.</span><span class="sxs-lookup"><span data-stu-id="ee486-239">Indicates if the policy is deployed to any inclusion groups or not.</span></span> <span data-ttu-id="ee486-240">Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-240">Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="ee486-241">revokeOnMdmHandoffDisabled</span><span class="sxs-lookup"><span data-stu-id="ee486-241">revokeOnMdmHandoffDisabled</span></span>|<span data-ttu-id="ee486-242">Boolean</span><span class="sxs-lookup"><span data-stu-id="ee486-242">Boolean</span></span>|<span data-ttu-id="ee486-243">Nueva propiedad en RS2, pendiente de documentación.</span><span class="sxs-lookup"><span data-stu-id="ee486-243">New property in RS2, pending documentation</span></span>|
|<span data-ttu-id="ee486-244">mdmEnrollmentUrl</span><span class="sxs-lookup"><span data-stu-id="ee486-244">mdmEnrollmentUrl</span></span>|<span data-ttu-id="ee486-245">String</span><span class="sxs-lookup"><span data-stu-id="ee486-245">String</span></span>|<span data-ttu-id="ee486-246">Dirección URL de la inscripción para MDM.</span><span class="sxs-lookup"><span data-stu-id="ee486-246">Enrollment url for the MDM</span></span>|
|<span data-ttu-id="ee486-247">windowsHelloForBusinessBlocked</span><span class="sxs-lookup"><span data-stu-id="ee486-247">windowsHelloForBusinessBlocked</span></span>|<span data-ttu-id="ee486-248">Boolean</span><span class="sxs-lookup"><span data-stu-id="ee486-248">Boolean</span></span>|<span data-ttu-id="ee486-249">Valor booleano que establece Windows Hello para empresas como método de inicio de sesión en Windows.</span><span class="sxs-lookup"><span data-stu-id="ee486-249">Boolean value that sets Windows Hello for Business as a method for signing into Windows.</span></span>|
|<span data-ttu-id="ee486-250">pinMinimumLength</span><span class="sxs-lookup"><span data-stu-id="ee486-250">pinMinimumLength</span></span>|<span data-ttu-id="ee486-251">Int32</span><span class="sxs-lookup"><span data-stu-id="ee486-251">Int32</span></span>|<span data-ttu-id="ee486-252">Valor entero que establece el número mínimo de caracteres necesarios para el PIN.</span><span class="sxs-lookup"><span data-stu-id="ee486-252">Integer value that sets the minimum number of characters required for the PIN.</span></span> <span data-ttu-id="ee486-253">El valor predeterminado es 4.</span><span class="sxs-lookup"><span data-stu-id="ee486-253">Default value is 4.</span></span> <span data-ttu-id="ee486-254">El número más bajo que se puede configurar para esta configuración de directiva es 4.</span><span class="sxs-lookup"><span data-stu-id="ee486-254">The lowest number you can configure for this policy setting is 4.</span></span> <span data-ttu-id="ee486-255">El número más alto que se puede configurar debe ser menor que el número establecido en la configuración de directiva de longitud máxima del PIN o el número 127, el que sea más bajo.</span><span class="sxs-lookup"><span data-stu-id="ee486-255">The largest number you can configure must be less than the number configured in the Maximum PIN length policy setting or the number 127, whichever is the lowest.</span></span>|
|<span data-ttu-id="ee486-256">pinUppercaseLetters</span><span class="sxs-lookup"><span data-stu-id="ee486-256">pinUppercaseLetters</span></span>|<span data-ttu-id="ee486-257">String</span><span class="sxs-lookup"><span data-stu-id="ee486-257">String</span></span>|<span data-ttu-id="ee486-258">Valor entero que configura el uso de mayúsculas en el PIN de Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="ee486-258">Integer value that configures the use of uppercase letters in the Windows Hello for Business PIN.</span></span> <span data-ttu-id="ee486-259">El valor predeterminado es NotAllow.</span><span class="sxs-lookup"><span data-stu-id="ee486-259">Default is NotAllow.</span></span> <span data-ttu-id="ee486-260">Los valores posibles son: `notAllow`, `requireAtLeastOne` y `allow`.</span><span class="sxs-lookup"><span data-stu-id="ee486-260">Possible values are: `notAllow`, `requireAtLeastOne`, `allow`.</span></span>|
|<span data-ttu-id="ee486-261">pinLowercaseLetters</span><span class="sxs-lookup"><span data-stu-id="ee486-261">pinLowercaseLetters</span></span>|<span data-ttu-id="ee486-262">String</span><span class="sxs-lookup"><span data-stu-id="ee486-262">String</span></span>|<span data-ttu-id="ee486-263">Valor entero que configura el uso de minúsculas en el PIN de Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="ee486-263">Integer value that configures the use of lowercase letters in the Windows Hello for Business PIN.</span></span> <span data-ttu-id="ee486-264">El valor predeterminado es NotAllow.</span><span class="sxs-lookup"><span data-stu-id="ee486-264">Default is NotAllow.</span></span> <span data-ttu-id="ee486-265">Los valores posibles son: `notAllow`, `requireAtLeastOne` y `allow`.</span><span class="sxs-lookup"><span data-stu-id="ee486-265">Possible values are: `notAllow`, `requireAtLeastOne`, `allow`.</span></span>|
|<span data-ttu-id="ee486-266">pinSpecialCharacters</span><span class="sxs-lookup"><span data-stu-id="ee486-266">pinSpecialCharacters</span></span>|<span data-ttu-id="ee486-267">String</span><span class="sxs-lookup"><span data-stu-id="ee486-267">String</span></span>|<span data-ttu-id="ee486-268">Valor entero que configura el uso de caracteres especiales en el PIN de Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="ee486-268">Integer value that configures the use of special characters in the Windows Hello for Business PIN.</span></span> <span data-ttu-id="ee486-269">Los caracteres especiales válidos para el PIN de Windows Hello para empresas incluyen: !</span><span class="sxs-lookup"><span data-stu-id="ee486-269">Valid special characters for Windows Hello for Business PIN gestures include: !</span></span> <span data-ttu-id="ee486-270">" # $ % & ' ( ) \* + , - .</span><span class="sxs-lookup"><span data-stu-id="ee486-270">" # $ % & ' ( ) \* + , - .</span></span> <span data-ttu-id="ee486-271">/ : ; < = > ?</span><span class="sxs-lookup"><span data-stu-id="ee486-271">/ : ; < = > ?</span></span><span data-ttu-id="ee486-272"> @ \[ \ \] ^ _ \` {</span><span class="sxs-lookup"><span data-stu-id="ee486-272"> @ \[ \ \] ^ _ \` {</span></span> | <span data-ttu-id="ee486-273">} ~.</span><span class="sxs-lookup"><span data-stu-id="ee486-273">=, ==</span></span> <span data-ttu-id="ee486-274">El valor predeterminado es NotAllow.</span><span class="sxs-lookup"><span data-stu-id="ee486-274">Default is NotAllow.</span></span> <span data-ttu-id="ee486-275">Los valores posibles son: `notAllow`, `requireAtLeastOne` y `allow`.</span><span class="sxs-lookup"><span data-stu-id="ee486-275">Possible values are: `notAllow`, `requireAtLeastOne`, `allow`.</span></span>|
|<span data-ttu-id="ee486-276">pinExpirationDays</span><span class="sxs-lookup"><span data-stu-id="ee486-276">pinExpirationDays</span></span>|<span data-ttu-id="ee486-277">Int32</span><span class="sxs-lookup"><span data-stu-id="ee486-277">Int32</span></span>|<span data-ttu-id="ee486-278">Valor entero que especifica el período de tiempo (en días) que se puede usar un PIN antes de que el sistema solicite que el usuario lo cambie.</span><span class="sxs-lookup"><span data-stu-id="ee486-278">Integer value specifies the period of time (in days) that a PIN can be used before the system requires the user to change it.</span></span> <span data-ttu-id="ee486-279">El número más alto que puede configurar para esta configuración de directiva es 730.</span><span class="sxs-lookup"><span data-stu-id="ee486-279">The largest number you can configure for this policy setting is 730.</span></span> <span data-ttu-id="ee486-280">El número más bajo que puede configurar para esta configuración de directiva es 0.</span><span class="sxs-lookup"><span data-stu-id="ee486-280">The lowest number you can configure for this policy setting is 0.</span></span> <span data-ttu-id="ee486-281">Si esta directiva se establece en 0, el PIN del usuario nunca expirará.</span><span class="sxs-lookup"><span data-stu-id="ee486-281">If this policy is set to 0, then the user's PIN will never expire.</span></span> <span data-ttu-id="ee486-282">Este nodo se agregó en Windows 10, versión 1511.</span><span class="sxs-lookup"><span data-stu-id="ee486-282">This node was added in Windows 10, version 1511.</span></span> <span data-ttu-id="ee486-283">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="ee486-283">Default is 0.</span></span>|
|<span data-ttu-id="ee486-284">numberOfPastPinsRemembered</span><span class="sxs-lookup"><span data-stu-id="ee486-284">numberOfPastPinsRemembered</span></span>|<span data-ttu-id="ee486-285">Int32</span><span class="sxs-lookup"><span data-stu-id="ee486-285">Int32</span></span>|<span data-ttu-id="ee486-286">Valor entero que especifica el número de PIN anteriores que se pueden asociar a una cuenta de usuario que no se pueden volver a usar.</span><span class="sxs-lookup"><span data-stu-id="ee486-286">Integer value that specifies the number of past PINs that can be associated to a user account that can't be reused.</span></span> <span data-ttu-id="ee486-287">El número más alto que puede configurar para esta configuración de directiva es 50.</span><span class="sxs-lookup"><span data-stu-id="ee486-287">The largest number you can configure for this policy setting is 50.</span></span> <span data-ttu-id="ee486-288">El número más bajo que puede configurar para esta configuración de directiva es 0.</span><span class="sxs-lookup"><span data-stu-id="ee486-288">The lowest number you can configure for this policy setting is 0.</span></span> <span data-ttu-id="ee486-289">Si esta directiva se establece en 0, no es necesario almacenar los PIN antiguos.</span><span class="sxs-lookup"><span data-stu-id="ee486-289">If this policy is set to 0, then storage of previous PINs is not required.</span></span> <span data-ttu-id="ee486-290">Este nodo se agregó en Windows 10, versión 1511.</span><span class="sxs-lookup"><span data-stu-id="ee486-290">This node was added in Windows 10, version 1511.</span></span> <span data-ttu-id="ee486-291">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="ee486-291">Default is 0.</span></span>|
|<span data-ttu-id="ee486-292">passwordMaximumAttemptCount</span><span class="sxs-lookup"><span data-stu-id="ee486-292">passwordMaximumAttemptCount</span></span>|<span data-ttu-id="ee486-293">Int32</span><span class="sxs-lookup"><span data-stu-id="ee486-293">Int32</span></span>|<span data-ttu-id="ee486-294">Número de errores de autenticación permitidos antes de que se borre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ee486-294">The number of authentication failures allowed before the device will be wiped.</span></span> <span data-ttu-id="ee486-295">Un valor de 0 deshabilita la funcionalidad de borrado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ee486-295">A value of 0 disables device wipe functionality.</span></span> <span data-ttu-id="ee486-296">El intervalo es un entero X donde 4 < = X < = 16 para equipos de escritorio y 0 < = X < = 999 para dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="ee486-296">Range is an integer X where 4 <= X <= 16 for desktop and 0 <= X <= 999 for mobile devices.</span></span>|
|<span data-ttu-id="ee486-297">minutesOfInactivityBeforeDeviceLock</span><span class="sxs-lookup"><span data-stu-id="ee486-297">minutesOfInactivityBeforeDeviceLock</span></span>|<span data-ttu-id="ee486-298">Int32</span><span class="sxs-lookup"><span data-stu-id="ee486-298">Int32</span></span>|<span data-ttu-id="ee486-299">Especifica la cantidad máxima de tiempo (en minutos) permitida después de que el dispositivo esté inactivo que hará que el dispositivo esté bloqueado con PIN o contraseña.</span><span class="sxs-lookup"><span data-stu-id="ee486-299">Specifies the maximum amount of time (in minutes) allowed after the device is idle that will cause the device to become PIN or password locked.</span></span>   <span data-ttu-id="ee486-300">El intervalo es un entero X, donde 0 < = X < = 999.</span><span class="sxs-lookup"><span data-stu-id="ee486-300">Range is an integer X where 0 <= X <= 999.</span></span>|
|<span data-ttu-id="ee486-301">daysWithoutContactBeforeUnenroll</span><span class="sxs-lookup"><span data-stu-id="ee486-301">daysWithoutContactBeforeUnenroll</span></span>|<span data-ttu-id="ee486-302">Int32</span><span class="sxs-lookup"><span data-stu-id="ee486-302">Int32</span></span>|<span data-ttu-id="ee486-303">Intervalo sin conexión antes de que se borren los datos de la aplicación (días)</span><span class="sxs-lookup"><span data-stu-id="ee486-303">Offline interval before app data is wiped (days)</span></span> |



## <a name="response"></a><span data-ttu-id="ee486-304">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ee486-304">Response</span></span>
<span data-ttu-id="ee486-305">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsInformationProtectionPolicy](../resources/intune_mam_windowsinformationprotectionpolicy.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ee486-305">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_mam_windowsinformationprotectionpolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ee486-306">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ee486-306">Example</span></span>
### <a name="request"></a><span data-ttu-id="ee486-307">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ee486-307">Request</span></span>
<span data-ttu-id="ee486-308">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ee486-308">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/windowsInformationProtectionPolicies/{windowsInformationProtectionPolicyId}
Content-type: application/json
Content-length: 4393

{
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

### <a name="response"></a><span data-ttu-id="ee486-309">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ee486-309">Response</span></span>
<span data-ttu-id="ee486-p130">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ee486-p130">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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



