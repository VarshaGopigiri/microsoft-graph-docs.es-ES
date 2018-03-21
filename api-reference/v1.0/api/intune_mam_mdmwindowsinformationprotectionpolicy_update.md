# <a name="update-mdmwindowsinformationprotectionpolicy"></a><span data-ttu-id="1271c-101">Actualizar mdmWindowsInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1271c-101">Update mdmWindowsInformationProtectionPolicy</span></span>

> <span data-ttu-id="1271c-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1271c-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1271c-103">Actualice las propiedades de un objeto [mdmWindowsInformationProtectionPolicy](../resources/intune_mam_mdmwindowsinformationprotectionpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="1271c-103">Update the properties of a [calendar](../resources/intune_mam_mdmwindowsinformationprotectionpolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1271c-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1271c-104">Prerequisites</span></span>
<span data-ttu-id="1271c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="1271c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="1271c-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1271c-107">Permission type</span></span>|<span data-ttu-id="1271c-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1271c-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1271c-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1271c-109">Delegated (work or school account)</span></span>|<span data-ttu-id="1271c-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1271c-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="1271c-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1271c-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1271c-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1271c-112">Not supported.</span></span>|
|<span data-ttu-id="1271c-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1271c-113">Application</span></span>|<span data-ttu-id="1271c-114">No compatible.</span><span class="sxs-lookup"><span data-stu-id="1271c-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1271c-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1271c-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mdmWindowsInformationProtectionPolicies/{mdmWindowsInformationProtectionPolicyId}
```

## <a name="request-headers"></a><span data-ttu-id="1271c-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1271c-116">Request headers</span></span>
|<span data-ttu-id="1271c-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1271c-117">Header</span></span>|<span data-ttu-id="1271c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1271c-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1271c-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="1271c-119">Authorization</span></span>|<span data-ttu-id="1271c-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1271c-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="1271c-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1271c-121">Accept</span></span>|<span data-ttu-id="1271c-122">application/json</span><span class="sxs-lookup"><span data-stu-id="1271c-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1271c-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1271c-123">Request body</span></span>
<span data-ttu-id="1271c-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [mdmWindowsInformationProtectionPolicy](../resources/intune_mam_mdmwindowsinformationprotectionpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="1271c-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_mam_mdmwindowsinformationprotectionpolicy.md) object.</span></span>

<span data-ttu-id="1271c-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [mdmWindowsInformationProtectionPolicy](../resources/intune_mam_mdmwindowsinformationprotectionpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="1271c-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="1271c-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1271c-126">Property</span></span>|<span data-ttu-id="1271c-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="1271c-127">Type</span></span>|<span data-ttu-id="1271c-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="1271c-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1271c-129">displayName</span><span class="sxs-lookup"><span data-stu-id="1271c-129">displayName</span></span>|<span data-ttu-id="1271c-130">String</span><span class="sxs-lookup"><span data-stu-id="1271c-130">String</span></span>|<span data-ttu-id="1271c-131">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="1271c-131">Policy display name.</span></span> <span data-ttu-id="1271c-132">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-132">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="1271c-133">description</span><span class="sxs-lookup"><span data-stu-id="1271c-133">description</span></span>|<span data-ttu-id="1271c-134">String</span><span class="sxs-lookup"><span data-stu-id="1271c-134">String</span></span>|<span data-ttu-id="1271c-135">Descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="1271c-135">The policy's description.</span></span> <span data-ttu-id="1271c-136">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-136">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="1271c-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="1271c-137">createdDateTime</span></span>|<span data-ttu-id="1271c-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1271c-138">DateTimeOffset</span></span>|<span data-ttu-id="1271c-139">Fecha y hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="1271c-139">The date and time when the page was created.</span></span> <span data-ttu-id="1271c-140">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-140">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="1271c-141">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="1271c-141">lastModifiedDateTime</span></span>|<span data-ttu-id="1271c-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1271c-142">DateTimeOffset</span></span>|<span data-ttu-id="1271c-143">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="1271c-143">Last time the policy was modified.</span></span> <span data-ttu-id="1271c-144">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-144">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="1271c-145">id</span><span class="sxs-lookup"><span data-stu-id="1271c-145">id</span></span>|<span data-ttu-id="1271c-146">String</span><span class="sxs-lookup"><span data-stu-id="1271c-146">String</span></span>|<span data-ttu-id="1271c-147">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="1271c-147">Key of the setting.</span></span> <span data-ttu-id="1271c-148">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-148">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="1271c-149">version</span><span class="sxs-lookup"><span data-stu-id="1271c-149">version</span></span>|<span data-ttu-id="1271c-150">String</span><span class="sxs-lookup"><span data-stu-id="1271c-150">String</span></span>|<span data-ttu-id="1271c-151">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="1271c-151">Version of the entity.</span></span> <span data-ttu-id="1271c-152">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-152">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="1271c-153">enforcementLevel</span><span class="sxs-lookup"><span data-stu-id="1271c-153">enforcementLevel</span></span>|<span data-ttu-id="1271c-154">String</span><span class="sxs-lookup"><span data-stu-id="1271c-154">String</span></span>|<span data-ttu-id="1271c-155">Nivel de obligatoriedad del trabajo en curso. Vea la definición de enumeración para los valores compatibles. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md). Los valores posibles son: `noProtection`, `encryptAndAuditOnly`, `encryptAuditAndPrompt` y `encryptAuditAndBlock`.</span><span class="sxs-lookup"><span data-stu-id="1271c-155">WIP enforcement level.See the Enum definition for supported values Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) Possible values are: `noProtection`, `encryptAndAuditOnly`, `encryptAuditAndPrompt`, `encryptAuditAndBlock`.</span></span>|
|<span data-ttu-id="1271c-156">enterpriseDomain</span><span class="sxs-lookup"><span data-stu-id="1271c-156">enterpriseDomain</span></span>|<span data-ttu-id="1271c-157">String</span><span class="sxs-lookup"><span data-stu-id="1271c-157">String</span></span>|<span data-ttu-id="1271c-158">Dominio empresarial principal. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-158">Primary enterprise domain Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="1271c-159">enterpriseProtectedDomainNames</span><span class="sxs-lookup"><span data-stu-id="1271c-159">enterpriseProtectedDomainNames</span></span>|<span data-ttu-id="1271c-160">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-160">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="1271c-161">Lista de dominios de empresa que se van a proteger. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-161">List of enterprise domains to be protected Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="1271c-162">protectionUnderLockConfigRequired</span><span class="sxs-lookup"><span data-stu-id="1271c-162">protectionUnderLockConfigRequired</span></span>|<span data-ttu-id="1271c-163">Boolean</span><span class="sxs-lookup"><span data-stu-id="1271c-163">Boolean</span></span>|<span data-ttu-id="1271c-164">Especifica si es necesario configurar la protección en la característica de bloqueo (también conocida como cifrar con PIN). Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-164">Specifies whether the protection under lock feature (also known as encrypt under pin) should be configured Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="1271c-165">dataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="1271c-165">dataRecoveryCertificate</span></span>|[<span data-ttu-id="1271c-166">windowsInformationProtectionDataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="1271c-166">windowsInformationProtectionDataRecoveryCertificate</span></span>](../resources/intune_mam_windowsinformationprotectiondatarecoverycertificate.md)|<span data-ttu-id="1271c-167">Especifica un certificado de recuperación que se puede usar para recuperar datos de archivos cifrados.</span><span class="sxs-lookup"><span data-stu-id="1271c-167">Specifies a recovery certificate that can be used for data recovery of encrypted files.</span></span> <span data-ttu-id="1271c-168">Es igual al certificado del agente de recuperación de datos (DRA) para el sistema de cifrado de archivos (EFS). Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-168">This is the same as the data recovery agent(DRA) certificate for encrypting file system(EFS) Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="1271c-169">revokeOnUnenrollDisabled</span><span class="sxs-lookup"><span data-stu-id="1271c-169">revokeOnUnenrollDisabled</span></span>|<span data-ttu-id="1271c-170">Boolean</span><span class="sxs-lookup"><span data-stu-id="1271c-170">Boolean</span></span>|<span data-ttu-id="1271c-171">Esta directiva controla si se revocan las claves de trabajo en curso cuando se anula la inscripción de un dispositivo en el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="1271c-171">This policy controls whether to revoke the WIP keys when a device unenrolls from the management service.</span></span> <span data-ttu-id="1271c-172">Si se establece en 1 (no revocar las claves), no se revocarán las claves y el usuario seguirá teniendo acceso a archivos protegidos después de anular la inscripción.</span><span class="sxs-lookup"><span data-stu-id="1271c-172">If set to 1 (Don't revoke keys), the keys will not be revoked and the user will continue to have access to protected files after unenrollment.</span></span> <span data-ttu-id="1271c-173">Si no se revocan las claves, no habrá ninguna limpieza de archivos revocados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="1271c-173">If the keys are not revoked, there will be no revoked file cleanup subsequently.</span></span> <span data-ttu-id="1271c-174">Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-174">Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="1271c-175">rightsManagementServicesTemplateId</span><span class="sxs-lookup"><span data-stu-id="1271c-175">rightsManagementServicesTemplateId</span></span>|<span data-ttu-id="1271c-176">Guid</span><span class="sxs-lookup"><span data-stu-id="1271c-176">Guid</span></span>|<span data-ttu-id="1271c-177">GUID de TemplateID que se va a usar para el cifrado RMS.</span><span class="sxs-lookup"><span data-stu-id="1271c-177">TemplateID GUID to use for RMS encryption.</span></span> <span data-ttu-id="1271c-178">La plantilla de RMS permite que el administrador de TI configure los detalles sobre quién tiene acceso a los archivos protegidos por RMS y durante cuánto tiempo. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-178">The RMS template allows the IT admin to configure the details about who has access to RMS-protected file and how long they have access Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="1271c-179">azureRightsManagementServicesAllowed</span><span class="sxs-lookup"><span data-stu-id="1271c-179">azureRightsManagementServicesAllowed</span></span>|<span data-ttu-id="1271c-180">Boolean</span><span class="sxs-lookup"><span data-stu-id="1271c-180">Boolean</span></span>|<span data-ttu-id="1271c-181">Especifica si se permite el cifrado de Azure RMS para WIP. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-181">Specifies whether to allow Azure RMS encryption for WIP Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="1271c-182">iconsVisible</span><span class="sxs-lookup"><span data-stu-id="1271c-182">iconsVisible</span></span>|<span data-ttu-id="1271c-183">Boolean</span><span class="sxs-lookup"><span data-stu-id="1271c-183">Boolean</span></span>|<span data-ttu-id="1271c-184">Determina si se agregan superposiciones a los iconos para los archivos protegidos mediante WIP en Explorer y en los iconos de aplicación solo de empresa en el menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="1271c-184">Determines whether overlays are added to icons for WIP protected files in Explorer and enterprise only app tiles in the Start menu.</span></span> <span data-ttu-id="1271c-185">A partir de Windows 10, versión 1703, estos ajustes también configuran la visibilidad del icono de WIP en la barra de título de una aplicación protegida mediante WIP. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-185">Starting in Windows 10, version 1703 this setting also configures the visibility of the WIP icon in the title bar of a WIP-protected app Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="1271c-186">protectedApps</span><span class="sxs-lookup"><span data-stu-id="1271c-186">protectedApps</span></span>|<span data-ttu-id="1271c-187">Colección [windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-187">[windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md) collection</span></span>|<span data-ttu-id="1271c-188">Las aplicaciones protegidas pueden tener acceso a datos empresariales y los datos controlados por dichas aplicaciones están protegidos mediante cifrado. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-188">Protected applications can access enterprise data and the data handled by those applications are protected with encryption Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="1271c-189">exemptApps</span><span class="sxs-lookup"><span data-stu-id="1271c-189">exemptApps</span></span>|<span data-ttu-id="1271c-190">Colección [windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-190">[windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md) collection</span></span>|<span data-ttu-id="1271c-191">Las aplicaciones exentas también pueden tener acceso a datos empresariales, pero los datos controlados por dichas aplicaciones no están protegidos.</span><span class="sxs-lookup"><span data-stu-id="1271c-191">Exempt applications can also access enterprise data, but the data handled by those applications are not protected.</span></span> <span data-ttu-id="1271c-192">Esto se debe a que es posible que algunas aplicaciones empresariales críticas tengan problemas de compatibilidad con los datos cifrados.</span><span class="sxs-lookup"><span data-stu-id="1271c-192">This is because some critical enterprise applications may have compatibility problems with encrypted data.</span></span> <span data-ttu-id="1271c-193">Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-193">Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="1271c-194">enterpriseNetworkDomainNames</span><span class="sxs-lookup"><span data-stu-id="1271c-194">enterpriseNetworkDomainNames</span></span>|<span data-ttu-id="1271c-195">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-195">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="1271c-196">Se trata de la lista de dominios que forman parte de los límites de la empresa.</span><span class="sxs-lookup"><span data-stu-id="1271c-196">This is the list of domains that comprise the boundaries of the enterprise.</span></span> <span data-ttu-id="1271c-197">Los datos de uno de estos dominios que se envíen a un dispositivo se considerarán datos empresariales y protegidos. Estas ubicaciones se consideran un destino seguro con el que compartir datos empresariales. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-197">Data from one of these domains that is sent to a device will be considered enterprise data and protected These locations will be considered a safe destination for enterprise data to be shared to Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="1271c-198">enterpriseProxiedDomains</span><span class="sxs-lookup"><span data-stu-id="1271c-198">enterpriseProxiedDomains</span></span>|<span data-ttu-id="1271c-199">Colección [windowsInformationProtectionProxiedDomainCollection](../resources/intune_mam_windowsinformationprotectionproxieddomaincollection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-199">[windowsInformationProtectionProxiedDomainCollection](../resources/intune_mam_windowsinformationprotectionproxieddomaincollection.md) collection</span></span>|<span data-ttu-id="1271c-200">Contiene una lista de dominios de recursos empresariales hospedados en la nube que necesitan protección.</span><span class="sxs-lookup"><span data-stu-id="1271c-200">Contains a list of Enterprise resource domains hosted in the cloud that need to be protected.</span></span> <span data-ttu-id="1271c-201">Las conexiones a estos recursos se consideran datos empresariales.</span><span class="sxs-lookup"><span data-stu-id="1271c-201">Connections to these resources are considered enterprise data.</span></span> <span data-ttu-id="1271c-202">Si un proxy se corresponde con un recurso de nube, el tráfico al recurso de nube se dirigirá a través de la red empresarial mediante el servidor proxy indicado (en el puerto 80).</span><span class="sxs-lookup"><span data-stu-id="1271c-202">If a proxy is paired with a cloud resource, traffic to the cloud resource will be routed through the enterprise network via the denoted proxy server (on Port 80).</span></span> <span data-ttu-id="1271c-203">Un servidor proxy que se use con esta finalidad debe configurarse también mediante la directiva EnterpriseInternalProxyServers. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-203">A proxy server used for this purpose must also be configured using the EnterpriseInternalProxyServers policy Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="1271c-204">enterpriseIPRanges</span><span class="sxs-lookup"><span data-stu-id="1271c-204">enterpriseIPRanges</span></span>|<span data-ttu-id="1271c-205">Colección [windowsInformationProtectionIPRangeCollection](../resources/intune_mam_windowsinformationprotectioniprangecollection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-205">[windowsInformationProtectionIPRangeCollection](../resources/intune_mam_windowsinformationprotectioniprangecollection.md) collection</span></span>|<span data-ttu-id="1271c-206">Establece los intervalos IP empresariales que definen los equipos de la red empresarial.</span><span class="sxs-lookup"><span data-stu-id="1271c-206">Sets the enterprise IP ranges that define the computers in the enterprise network.</span></span> <span data-ttu-id="1271c-207">Los datos que provienen de dichos equipos se consideran parte de la empresa y están protegidos.</span><span class="sxs-lookup"><span data-stu-id="1271c-207">Data that comes from those computers will be considered part of the enterprise and protected.</span></span> <span data-ttu-id="1271c-208">Estas ubicaciones se consideran un destino seguro en el que compartir datos empresariales. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-208">These locations will be considered a safe destination for enterprise data to be shared to Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="1271c-209">enterpriseIPRangesAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="1271c-209">enterpriseIPRangesAreAuthoritative</span></span>|<span data-ttu-id="1271c-210">Boolean</span><span class="sxs-lookup"><span data-stu-id="1271c-210">Boolean</span></span>|<span data-ttu-id="1271c-211">Valor booleano que indica al cliente que acepte la lista configurada y que no use la heurística para intentar buscar otras subredes.</span><span class="sxs-lookup"><span data-stu-id="1271c-211">Boolean value that tells the client to accept the configured list and not to use heuristics to attempt to find other subnets.</span></span> <span data-ttu-id="1271c-212">El valor predeterminado es False. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-212">Default is false Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="1271c-213">enterpriseProxyServers</span><span class="sxs-lookup"><span data-stu-id="1271c-213">enterpriseProxyServers</span></span>|<span data-ttu-id="1271c-214">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-214">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="1271c-215">Se trata de una lista de servidores proxy.</span><span class="sxs-lookup"><span data-stu-id="1271c-215">This is a list of proxy servers.</span></span> <span data-ttu-id="1271c-216">Cualquier servidor que no esté en esta lista se considera no empresarial. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-216">Any server not on this list is considered non-enterprise Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="1271c-217">enterpriseInternalProxyServers</span><span class="sxs-lookup"><span data-stu-id="1271c-217">enterpriseInternalProxyServers</span></span>|<span data-ttu-id="1271c-218">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-218">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="1271c-219">Se trata de la lista de valores separados por comas de servidores proxy internos.</span><span class="sxs-lookup"><span data-stu-id="1271c-219">This is the comma-separated list of internal proxy servers.</span></span> <span data-ttu-id="1271c-220">Por ejemplo, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span><span class="sxs-lookup"><span data-stu-id="1271c-220">For example, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span></span> <span data-ttu-id="1271c-221">El administrador ha configurado estos servidores proxy para que se conecten a los recursos específicos de Internet.</span><span class="sxs-lookup"><span data-stu-id="1271c-221">These proxies have been configured by the admin to connect to specific resources on the Internet.</span></span> <span data-ttu-id="1271c-222">Se consideran ubicaciones de red empresarial.</span><span class="sxs-lookup"><span data-stu-id="1271c-222">They are considered to be enterprise network locations.</span></span> <span data-ttu-id="1271c-223">Los servidores proxy solo se usan al configurar la directiva EnterpriseProxiedDomains para forzar el tráfico a los dominios coincidentes mediante estos proxy. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-223">The proxies are only leveraged in configuring the EnterpriseProxiedDomains policy to force traffic to the matched domains through these proxies Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="1271c-224">enterpriseProxyServersAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="1271c-224">enterpriseProxyServersAreAuthoritative</span></span>|<span data-ttu-id="1271c-225">Boolean</span><span class="sxs-lookup"><span data-stu-id="1271c-225">Boolean</span></span>|<span data-ttu-id="1271c-226">Valor booleano que indica al cliente que acepte la lista configurada de servidores proxy y no intente detectar otros servidores proxy de trabajo.</span><span class="sxs-lookup"><span data-stu-id="1271c-226">Boolean value that tells the client to accept the configured list of proxies and not try to detect other work proxies.</span></span> <span data-ttu-id="1271c-227">El valor predeterminado es False. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-227">Default is false Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="1271c-228">neutralDomainResources</span><span class="sxs-lookup"><span data-stu-id="1271c-228">neutralDomainResources</span></span>|<span data-ttu-id="1271c-229">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-229">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="1271c-230">Lista de nombres de dominio que se pueden usar para el recurso de trabajo o personal. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-230">List of domain names that can used for work or personal resource Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="1271c-231">indexingEncryptedStoresOrItemsBlocked</span><span class="sxs-lookup"><span data-stu-id="1271c-231">indexingEncryptedStoresOrItemsBlocked</span></span>|<span data-ttu-id="1271c-232">Boolean</span><span class="sxs-lookup"><span data-stu-id="1271c-232">Boolean</span></span>|<span data-ttu-id="1271c-233">Este identificador es para que el indexador de Windows Search permita o impida la indexación de los elementos. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-233">This switch is for the Windows Search Indexer, to allow or disallow indexing of items Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="1271c-234">smbAutoEncryptedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="1271c-234">smbAutoEncryptedFileExtensions</span></span>|<span data-ttu-id="1271c-235">Colección [windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-235">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="1271c-236">Especifica una lista de extensiones de archivo, para que los archivos con estas extensiones se cifren cuando se copian desde un recurso compartido de SMB dentro del límite de la empresa. Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-236">Specifies a list of file extensions, so that files with these extensions are encrypted when copying from an SMB share within the corporate boundary Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="1271c-237">isAssigned</span><span class="sxs-lookup"><span data-stu-id="1271c-237">isAssigned</span></span>|<span data-ttu-id="1271c-238">Boolean</span><span class="sxs-lookup"><span data-stu-id="1271c-238">Boolean</span></span>|<span data-ttu-id="1271c-239">Indica si la directiva se implementará en los grupos de inclusión o no.</span><span class="sxs-lookup"><span data-stu-id="1271c-239">Indicates if the policy is deployed to any inclusion groups or not.</span></span> <span data-ttu-id="1271c-240">Heredado de [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="1271c-240">Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|



## <a name="response"></a><span data-ttu-id="1271c-241">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1271c-241">Response</span></span>
<span data-ttu-id="1271c-242">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [mdmWindowsInformationProtectionPolicy](../resources/intune_mam_mdmwindowsinformationprotectionpolicy.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1271c-242">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_mam_mdmwindowsinformationprotectionpolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1271c-243">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1271c-243">Example</span></span>
### <a name="request"></a><span data-ttu-id="1271c-244">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1271c-244">Request</span></span>
<span data-ttu-id="1271c-245">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1271c-245">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mdmWindowsInformationProtectionPolicies/{mdmWindowsInformationProtectionPolicyId}
Content-type: application/json
Content-length: 3890

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
  "isAssigned": true
}
```

### <a name="response"></a><span data-ttu-id="1271c-246">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1271c-246">Response</span></span>
<span data-ttu-id="1271c-p121">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1271c-p121">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 4074

{
  "@odata.type": "#microsoft.intune_mam_graph.mdmWindowsInformationProtectionPolicy",
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



