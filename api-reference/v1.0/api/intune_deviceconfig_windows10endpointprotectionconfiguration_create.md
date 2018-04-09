# <a name="create-windows10endpointprotectionconfiguration"></a><span data-ttu-id="a4043-101">Crear windows10EndpointProtectionConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4043-101">Create windows10EndpointProtectionConfiguration</span></span>

> <span data-ttu-id="a4043-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a4043-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a4043-103">Crea un objeto [windows10EndpointProtectionConfiguration](../resources/intune_deviceconfig_windows10endpointprotectionconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="a4043-103">Create a new [plannerBucket](../resources/intune_deviceconfig_windows10endpointprotectionconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a4043-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a4043-104">Prerequisites</span></span>
<span data-ttu-id="a4043-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, que incluye cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a4043-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a4043-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a4043-107">Permission type</span></span>|<span data-ttu-id="a4043-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a4043-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a4043-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a4043-109">Delegated (work or school account)</span></span>|<span data-ttu-id="a4043-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a4043-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="a4043-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a4043-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a4043-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a4043-112">Not supported.</span></span>|
|<span data-ttu-id="a4043-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a4043-113">Application</span></span>|<span data-ttu-id="a4043-114">No admitido.</span><span class="sxs-lookup"><span data-stu-id="a4043-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a4043-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a4043-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="a4043-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a4043-116">Request headers</span></span>
|<span data-ttu-id="a4043-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4043-117">Header</span></span>|<span data-ttu-id="a4043-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a4043-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a4043-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="a4043-119">Authorization</span></span>|<span data-ttu-id="a4043-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a4043-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="a4043-121">Accept</span><span class="sxs-lookup"><span data-stu-id="a4043-121">Accept</span></span>|<span data-ttu-id="a4043-122">application/json</span><span class="sxs-lookup"><span data-stu-id="a4043-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a4043-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a4043-123">Request body</span></span>
<span data-ttu-id="a4043-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto windows10EndpointProtectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a4043-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="a4043-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windows10EndpointProtectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a4043-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="a4043-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a4043-126">Property</span></span>|<span data-ttu-id="a4043-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="a4043-127">Type</span></span>|<span data-ttu-id="a4043-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4043-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a4043-129">id</span><span class="sxs-lookup"><span data-stu-id="a4043-129">id</span></span>|<span data-ttu-id="a4043-130">String</span><span class="sxs-lookup"><span data-stu-id="a4043-130">String</span></span>|<span data-ttu-id="a4043-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a4043-131">Key of the setting.</span></span> <span data-ttu-id="a4043-132">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="a4043-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a4043-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="a4043-133">lastModifiedDateTime</span></span>|<span data-ttu-id="a4043-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a4043-134">DateTimeOffset</span></span>|<span data-ttu-id="a4043-135">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="a4043-135">Indicates the date the object was last modified.</span></span> <span data-ttu-id="a4043-136">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="a4043-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a4043-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="a4043-137">createdDateTime</span></span>|<span data-ttu-id="a4043-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a4043-138">DateTimeOffset</span></span>|<span data-ttu-id="a4043-139">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="a4043-139">DateTime the object was created.</span></span> <span data-ttu-id="a4043-140">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="a4043-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a4043-141">description</span><span class="sxs-lookup"><span data-stu-id="a4043-141">description</span></span>|<span data-ttu-id="a4043-142">String</span><span class="sxs-lookup"><span data-stu-id="a4043-142">String</span></span>|<span data-ttu-id="a4043-143">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4043-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="a4043-144">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="a4043-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a4043-145">displayName</span><span class="sxs-lookup"><span data-stu-id="a4043-145">displayName</span></span>|<span data-ttu-id="a4043-146">String</span><span class="sxs-lookup"><span data-stu-id="a4043-146">String</span></span>|<span data-ttu-id="a4043-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4043-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="a4043-148">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="a4043-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a4043-149">version</span><span class="sxs-lookup"><span data-stu-id="a4043-149">version</span></span>|<span data-ttu-id="a4043-150">Int32</span><span class="sxs-lookup"><span data-stu-id="a4043-150">Int32</span></span>|<span data-ttu-id="a4043-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4043-151">Version of the device configuration.</span></span> <span data-ttu-id="a4043-152">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="a4043-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a4043-153">firewallBlockStatefulFTP</span><span class="sxs-lookup"><span data-stu-id="a4043-153">firewallBlockStatefulFTP</span></span>|<span data-ttu-id="a4043-154">Boolean</span><span class="sxs-lookup"><span data-stu-id="a4043-154">Boolean</span></span>|<span data-ttu-id="a4043-155">Bloquea las conexiones FTP con estado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4043-155">Blocks stateful FTP connections to the device</span></span>|
|<span data-ttu-id="a4043-156">firewallIdleTimeoutForSecurityAssociationInSeconds</span><span class="sxs-lookup"><span data-stu-id="a4043-156">firewallIdleTimeoutForSecurityAssociationInSeconds</span></span>|<span data-ttu-id="a4043-157">Int32</span><span class="sxs-lookup"><span data-stu-id="a4043-157">Int32</span></span>|<span data-ttu-id="a4043-158">Configura el tiempo de espera inactivo para asociaciones de seguridad, en segundos, de 300 a 3600 inclusive.</span><span class="sxs-lookup"><span data-stu-id="a4043-158">Configures the idle timeout for security associations, in seconds, from 300 to 3600 inclusive.</span></span> <span data-ttu-id="a4043-159">Se trata del período tras el cual expiran y se eliminan las asociaciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a4043-159">This is the period after which security associations will expire and be deleted.</span></span> <span data-ttu-id="a4043-160">Valores válidos de 300 a 3600.</span><span class="sxs-lookup"><span data-stu-id="a4043-160">Valid values 300 to 3600</span></span>|
|<span data-ttu-id="a4043-161">firewallPreSharedKeyEncodingMethod</span><span class="sxs-lookup"><span data-stu-id="a4043-161">firewallPreSharedKeyEncodingMethod</span></span>|<span data-ttu-id="a4043-162">String</span><span class="sxs-lookup"><span data-stu-id="a4043-162">String</span></span>|<span data-ttu-id="a4043-163">Selecciona la codificación de clave previamente compartida que se debe usar. Los valores posibles son: `deviceDefault`, `none` y `utF8`.</span><span class="sxs-lookup"><span data-stu-id="a4043-163">Select the preshared key encoding to be used Possible values are: `deviceDefault`, `none`, `utF8`.</span></span>|
|<span data-ttu-id="a4043-164">firewallIPSecExemptionsAllowNeighborDiscovery</span><span class="sxs-lookup"><span data-stu-id="a4043-164">firewallIPSecExemptionsAllowNeighborDiscovery</span></span>|<span data-ttu-id="a4043-165">Boolean</span><span class="sxs-lookup"><span data-stu-id="a4043-165">Boolean</span></span>|<span data-ttu-id="a4043-166">Configura las exenciones IPSec para permitir los códigos de tipo ICMP de IPv6 de detección de vecinos.</span><span class="sxs-lookup"><span data-stu-id="a4043-166">Configures IPSec exemptions to allow neighbor discovery IPv6 ICMP type-codes</span></span>|
|<span data-ttu-id="a4043-167">firewallIPSecExemptionsAllowICMP</span><span class="sxs-lookup"><span data-stu-id="a4043-167">firewallIPSecExemptionsAllowICMP</span></span>|<span data-ttu-id="a4043-168">Boolean</span><span class="sxs-lookup"><span data-stu-id="a4043-168">Boolean</span></span>|<span data-ttu-id="a4043-169">Configura las exenciones IPSec para permitir ICMP.</span><span class="sxs-lookup"><span data-stu-id="a4043-169">Configures IPSec exemptions to allow ICMP</span></span>|
|<span data-ttu-id="a4043-170">firewallIPSecExemptionsAllowRouterDiscovery</span><span class="sxs-lookup"><span data-stu-id="a4043-170">firewallIPSecExemptionsAllowRouterDiscovery</span></span>|<span data-ttu-id="a4043-171">Boolean</span><span class="sxs-lookup"><span data-stu-id="a4043-171">Boolean</span></span>|<span data-ttu-id="a4043-172">Configura las exenciones IPSec para permitir los códigos de tipo ICMP de IPv6 de detección de enrutadores.</span><span class="sxs-lookup"><span data-stu-id="a4043-172">Configures IPSec exemptions to allow router discovery IPv6 ICMP type-codes</span></span>|
|<span data-ttu-id="a4043-173">firewallIPSecExemptionsAllowDHCP</span><span class="sxs-lookup"><span data-stu-id="a4043-173">firewallIPSecExemptionsAllowDHCP</span></span>|<span data-ttu-id="a4043-174">Boolean</span><span class="sxs-lookup"><span data-stu-id="a4043-174">Boolean</span></span>|<span data-ttu-id="a4043-175">Configura las exenciones IPSec para permitir el tráfico DHCP de IPv4 e IPv6.</span><span class="sxs-lookup"><span data-stu-id="a4043-175">Configures IPSec exemptions to allow both IPv4 and IPv6 DHCP traffic</span></span>|
|<span data-ttu-id="a4043-176">firewallCertificateRevocationListCheckMethod</span><span class="sxs-lookup"><span data-stu-id="a4043-176">firewallCertificateRevocationListCheckMethod</span></span>|<span data-ttu-id="a4043-177">String</span><span class="sxs-lookup"><span data-stu-id="a4043-177">String</span></span>|<span data-ttu-id="a4043-178">Especifica cómo se aplica la lista de revocación de certificados. Los valores posibles son: `deviceDefault`, `none`, `attempt` y `require`.</span><span class="sxs-lookup"><span data-stu-id="a4043-178">Specify how the certificate revocation list is to be enforced Possible values are: `deviceDefault`, `none`, `attempt`, `require`.</span></span>|
|<span data-ttu-id="a4043-179">firewallMergeKeyingModuleSettings</span><span class="sxs-lookup"><span data-stu-id="a4043-179">firewallMergeKeyingModuleSettings</span></span>|<span data-ttu-id="a4043-180">Boolean</span><span class="sxs-lookup"><span data-stu-id="a4043-180">Boolean</span></span>|<span data-ttu-id="a4043-181">Si un conjunto de autenticación no es totalmente compatible con un módulo de generación de claves, dirija el módulo para que solo ignore los conjuntos de autenticación no admitidos, en lugar de todo el conjunto.</span><span class="sxs-lookup"><span data-stu-id="a4043-181">If an authentication set is not fully supported by a keying module, direct the module to ignore only unsupported authentication suites rather than the entire set</span></span>|
|<span data-ttu-id="a4043-182">firewallPacketQueueingMethod</span><span class="sxs-lookup"><span data-stu-id="a4043-182">firewallPacketQueueingMethod</span></span>|<span data-ttu-id="a4043-183">String</span><span class="sxs-lookup"><span data-stu-id="a4043-183">String</span></span>|<span data-ttu-id="a4043-184">Configura cómo debe aplicarse la cola de paquetes en el escenario de puerta de enlace de túnel. Los valores posibles son: `deviceDefault`, `disabled`, `queueInbound`, `queueOutbound` y `queueBoth`.</span><span class="sxs-lookup"><span data-stu-id="a4043-184">Configures how packet queueing should be applied in the tunnel gateway scenario Possible values are: `deviceDefault`, `disabled`, `queueInbound`, `queueOutbound`, `queueBoth`.</span></span>|
|<span data-ttu-id="a4043-185">firewallProfileDomain</span><span class="sxs-lookup"><span data-stu-id="a4043-185">firewallProfileDomain</span></span>|[<span data-ttu-id="a4043-186">windowsFirewallNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a4043-186">windowsFirewallNetworkProfile</span></span>](../resources/intune_deviceconfig_windowsfirewallnetworkprofile.md)|<span data-ttu-id="a4043-187">Configura las opciones del perfil de firewall para redes de dominio.</span><span class="sxs-lookup"><span data-stu-id="a4043-187">Configures the firewall profile settings for domain networks</span></span>|
|<span data-ttu-id="a4043-188">firewallProfilePublic</span><span class="sxs-lookup"><span data-stu-id="a4043-188">firewallProfilePublic</span></span>|[<span data-ttu-id="a4043-189">windowsFirewallNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a4043-189">windowsFirewallNetworkProfile</span></span>](../resources/intune_deviceconfig_windowsfirewallnetworkprofile.md)|<span data-ttu-id="a4043-190">Configura las opciones del perfil de firewall para redes públicas.</span><span class="sxs-lookup"><span data-stu-id="a4043-190">Configures the firewall profile settings for public networks</span></span>|
|<span data-ttu-id="a4043-191">firewallProfilePrivate</span><span class="sxs-lookup"><span data-stu-id="a4043-191">firewallProfilePrivate</span></span>|[<span data-ttu-id="a4043-192">windowsFirewallNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a4043-192">windowsFirewallNetworkProfile</span></span>](../resources/intune_deviceconfig_windowsfirewallnetworkprofile.md)|<span data-ttu-id="a4043-193">Configura las opciones del perfil de firewall para redes privadas.</span><span class="sxs-lookup"><span data-stu-id="a4043-193">Configures the firewall profile settings for private networks</span></span>|
|<span data-ttu-id="a4043-194">defenderAttackSurfaceReductionExcludedPaths</span><span class="sxs-lookup"><span data-stu-id="a4043-194">defenderAttackSurfaceReductionExcludedPaths</span></span>|<span data-ttu-id="a4043-195">Colección String</span><span class="sxs-lookup"><span data-stu-id="a4043-195">String collection</span></span>|<span data-ttu-id="a4043-196">Lista de archivos exe y carpetas que se deben excluir de las reglas de reducción de la superficie expuesta a ataques.</span><span class="sxs-lookup"><span data-stu-id="a4043-196">List of exe files and folders to be excluded from attack surface reduction rules</span></span>|
|<span data-ttu-id="a4043-197">defenderGuardedFoldersAllowedAppPaths</span><span class="sxs-lookup"><span data-stu-id="a4043-197">defenderGuardedFoldersAllowedAppPaths</span></span>|<span data-ttu-id="a4043-198">Colección String</span><span class="sxs-lookup"><span data-stu-id="a4043-198">String collection</span></span>|<span data-ttu-id="a4043-199">Lista de rutas de acceso a exe que pueden obtener acceso a carpetas protegidas.</span><span class="sxs-lookup"><span data-stu-id="a4043-199">List of paths to exe that are allowed to access protected folders</span></span>|
|<span data-ttu-id="a4043-200">defenderAdditionalGuardedFolders</span><span class="sxs-lookup"><span data-stu-id="a4043-200">defenderAdditionalGuardedFolders</span></span>|<span data-ttu-id="a4043-201">Colección String</span><span class="sxs-lookup"><span data-stu-id="a4043-201">String collection</span></span>|<span data-ttu-id="a4043-202">Lista de las rutas de acceso de carpeta que se van a agregar a la lista de carpetas protegidas.</span><span class="sxs-lookup"><span data-stu-id="a4043-202">List of folder paths to be added to the list of protected folders</span></span>|
|<span data-ttu-id="a4043-203">defenderExploitProtectionXml</span><span class="sxs-lookup"><span data-stu-id="a4043-203">defenderExploitProtectionXml</span></span>|<span data-ttu-id="a4043-204">Binary</span><span class="sxs-lookup"><span data-stu-id="a4043-204">Binary</span></span>|<span data-ttu-id="a4043-205">Contenido XML que contiene información sobre detalles de protección contra vulnerabilidades de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a4043-205">Xml content containing information regarding exploit protection details.</span></span>|
|<span data-ttu-id="a4043-206">defenderExploitProtectionXmlFileName</span><span class="sxs-lookup"><span data-stu-id="a4043-206">defenderExploitProtectionXmlFileName</span></span>|<span data-ttu-id="a4043-207">String</span><span class="sxs-lookup"><span data-stu-id="a4043-207">String</span></span>|<span data-ttu-id="a4043-208">Nombre del archivo del que se obtuvo DefenderExploitProtectionXml.</span><span class="sxs-lookup"><span data-stu-id="a4043-208">Name of the file from which DefenderExploitProtectionXml was obtained.</span></span>|
|<span data-ttu-id="a4043-209">defenderSecurityCenterBlockExploitProtectionOverride</span><span class="sxs-lookup"><span data-stu-id="a4043-209">defenderSecurityCenterBlockExploitProtectionOverride</span></span>|<span data-ttu-id="a4043-210">Boolean</span><span class="sxs-lookup"><span data-stu-id="a4043-210">Boolean</span></span>|<span data-ttu-id="a4043-211">Indica si se va a impedir que el usuario invalide la configuración de protección contra vulnerabilidades.</span><span class="sxs-lookup"><span data-stu-id="a4043-211">Indicates whether or not to block user from overriding Exploit Protection settings.</span></span>|
|<span data-ttu-id="a4043-212">appLockerApplicationControl</span><span class="sxs-lookup"><span data-stu-id="a4043-212">appLockerApplicationControl</span></span>|<span data-ttu-id="a4043-213">String</span><span class="sxs-lookup"><span data-stu-id="a4043-213">String</span></span>|<span data-ttu-id="a4043-214">Permite que el administrador elija los tipos de aplicación que se permiten en los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a4043-214">Enables the Admin to choose what types of app to allow on devices.</span></span> <span data-ttu-id="a4043-215">Los valores posibles son: `notConfigured`, `enforceComponentsAndStoreApps`, `auditComponentsAndStoreApps`, `enforceComponentsStoreAppsAndSmartlocker` y `auditComponentsStoreAppsAndSmartlocker`.</span><span class="sxs-lookup"><span data-stu-id="a4043-215">Possible values are: `notConfigured`, `enforceComponentsAndStoreApps`, `auditComponentsAndStoreApps`, `enforceComponentsStoreAppsAndSmartlocker`, `auditComponentsStoreAppsAndSmartlocker`.</span></span>|
|<span data-ttu-id="a4043-216">smartScreenEnableInShell</span><span class="sxs-lookup"><span data-stu-id="a4043-216">smartScreenEnableInShell</span></span>|<span data-ttu-id="a4043-217">Boolean</span><span class="sxs-lookup"><span data-stu-id="a4043-217">Boolean</span></span>|<span data-ttu-id="a4043-218">Permite que los administradores de TI configuren SmartScreen para Windows.</span><span class="sxs-lookup"><span data-stu-id="a4043-218">Allows IT Admins to configure SmartScreen for Windows.</span></span>|
|<span data-ttu-id="a4043-219">smartScreenBlockOverrideForFiles</span><span class="sxs-lookup"><span data-stu-id="a4043-219">smartScreenBlockOverrideForFiles</span></span>|<span data-ttu-id="a4043-220">Boolean</span><span class="sxs-lookup"><span data-stu-id="a4043-220">Boolean</span></span>|<span data-ttu-id="a4043-221">Permite que los administradores de TI controlen si los usuarios pueden omitir advertencias de SmartScreen y ejecutar archivos malintencionados.</span><span class="sxs-lookup"><span data-stu-id="a4043-221">Allows IT Admins to control whether users can can ignore SmartScreen warnings and run malicious files.</span></span>|
|<span data-ttu-id="a4043-222">applicationGuardEnabled</span><span class="sxs-lookup"><span data-stu-id="a4043-222">applicationGuardEnabled</span></span>|<span data-ttu-id="a4043-223">Boolean</span><span class="sxs-lookup"><span data-stu-id="a4043-223">Boolean</span></span>|<span data-ttu-id="a4043-224">Habilita la Protección de aplicaciones de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="a4043-224">Enable Windows Defender Application Guard</span></span>|
|<span data-ttu-id="a4043-225">applicationGuardBlockFileTransfer</span><span class="sxs-lookup"><span data-stu-id="a4043-225">applicationGuardBlockFileTransfer</span></span>|<span data-ttu-id="a4043-226">String</span><span class="sxs-lookup"><span data-stu-id="a4043-226">String</span></span>|<span data-ttu-id="a4043-227">Impide que el Portapapeles transfiera archivos de imagen, de texto o ambos. Los valores posibles son: `notConfigured`, `blockImageAndTextFile`, `blockImageFile`, `blockNone` y `blockTextFile`.</span><span class="sxs-lookup"><span data-stu-id="a4043-227">Block clipboard to transfer image file, text file or neither of them Possible values are: `notConfigured`, `blockImageAndTextFile`, `blockImageFile`, `blockNone`, `blockTextFile`.</span></span>|
|<span data-ttu-id="a4043-228">applicationGuardBlockNonEnterpriseContent</span><span class="sxs-lookup"><span data-stu-id="a4043-228">applicationGuardBlockNonEnterpriseContent</span></span>|<span data-ttu-id="a4043-229">Boolean</span><span class="sxs-lookup"><span data-stu-id="a4043-229">Boolean</span></span>|<span data-ttu-id="a4043-230">Impide que los sitios de la empresa carguen contenido no empresarial, como complementos de terceros.</span><span class="sxs-lookup"><span data-stu-id="a4043-230">Block enterprise sites to load non-enterprise content, such as third party plug-ins</span></span>|
|<span data-ttu-id="a4043-231">applicationGuardAllowPersistence</span><span class="sxs-lookup"><span data-stu-id="a4043-231">applicationGuardAllowPersistence</span></span>|<span data-ttu-id="a4043-232">Boolean</span><span class="sxs-lookup"><span data-stu-id="a4043-232">Boolean</span></span>|<span data-ttu-id="a4043-233">Permite el almacenamiento de los datos generados por el usuario en el contenedor de la protección de aplicaciones (favoritos, cookies, contraseñas web, etc.).</span><span class="sxs-lookup"><span data-stu-id="a4043-233">Allow persisting user generated data inside the App Guard Containter (favorites, cookies, web passwords, etc.)</span></span>|
|<span data-ttu-id="a4043-234">applicationGuardForceAuditing</span><span class="sxs-lookup"><span data-stu-id="a4043-234">applicationGuardForceAuditing</span></span>|<span data-ttu-id="a4043-235">Boolean</span><span class="sxs-lookup"><span data-stu-id="a4043-235">Boolean</span></span>|<span data-ttu-id="a4043-236">La auditoría forzada conservará los registros y eventos de Windows para cumplir con los criterios de seguridad y cumplimiento (algunos eventos de ejemplo son el inicio y cierre de sesión del usuario, el uso de derechos de privilegio, la instalación de software, los cambios del sistema, etc.).</span><span class="sxs-lookup"><span data-stu-id="a4043-236">Force auditing will persist Windows logs and events to meet security/compliance criteria (sample events are user login-logoff, use of privilege rights, software installation, system changes, etc.)</span></span>|
|<span data-ttu-id="a4043-237">applicationGuardBlockClipboardSharing</span><span class="sxs-lookup"><span data-stu-id="a4043-237">applicationGuardBlockClipboardSharing</span></span>|<span data-ttu-id="a4043-238">String</span><span class="sxs-lookup"><span data-stu-id="a4043-238">String</span></span>|<span data-ttu-id="a4043-239">Impide que el Portapapeles comparta los datos del host al contenedor, del contenedor al host, en ambas direcciones o en ninguna.</span><span class="sxs-lookup"><span data-stu-id="a4043-239">Block clipboard to share data from Host to Container, or from Container to Host, or both ways, or neither ways.</span></span> <span data-ttu-id="a4043-240">Los valores posibles son: `notConfigured`, `blockBoth`, `blockHostToContainer`, `blockContainerToHost` y `blockNone`.</span><span class="sxs-lookup"><span data-stu-id="a4043-240">Possible values are: `notConfigured`, `blockBoth`, `blockHostToContainer`, `blockContainerToHost`, `blockNone`.</span></span>|
|<span data-ttu-id="a4043-241">applicationGuardAllowPrintToPDF</span><span class="sxs-lookup"><span data-stu-id="a4043-241">applicationGuardAllowPrintToPDF</span></span>|<span data-ttu-id="a4043-242">Boolean</span><span class="sxs-lookup"><span data-stu-id="a4043-242">Boolean</span></span>|<span data-ttu-id="a4043-243">Permite la impresión en PDF desde el contenedor.</span><span class="sxs-lookup"><span data-stu-id="a4043-243">Allow printing to PDF from Container</span></span>|
|<span data-ttu-id="a4043-244">applicationGuardAllowPrintToXPS</span><span class="sxs-lookup"><span data-stu-id="a4043-244">applicationGuardAllowPrintToXPS</span></span>|<span data-ttu-id="a4043-245">Boolean</span><span class="sxs-lookup"><span data-stu-id="a4043-245">Boolean</span></span>|<span data-ttu-id="a4043-246">Permite la impresión en XPS desde el contenedor.</span><span class="sxs-lookup"><span data-stu-id="a4043-246">Allow printing to XPS from Container</span></span>|
|<span data-ttu-id="a4043-247">applicationGuardAllowPrintToLocalPrinters</span><span class="sxs-lookup"><span data-stu-id="a4043-247">applicationGuardAllowPrintToLocalPrinters</span></span>|<span data-ttu-id="a4043-248">Boolean</span><span class="sxs-lookup"><span data-stu-id="a4043-248">Boolean</span></span>|<span data-ttu-id="a4043-249">Permite la impresión en impresoras locales desde el contenedor.</span><span class="sxs-lookup"><span data-stu-id="a4043-249">Allow printing to Local Printers from Container</span></span>|
|<span data-ttu-id="a4043-250">applicationGuardAllowPrintToNetworkPrinters</span><span class="sxs-lookup"><span data-stu-id="a4043-250">applicationGuardAllowPrintToNetworkPrinters</span></span>|<span data-ttu-id="a4043-251">Boolean</span><span class="sxs-lookup"><span data-stu-id="a4043-251">Boolean</span></span>|<span data-ttu-id="a4043-252">Permite la impresión en impresoras en red desde el contenedor.</span><span class="sxs-lookup"><span data-stu-id="a4043-252">Allow printing to Network Printers from Container</span></span>|
|<span data-ttu-id="a4043-253">bitLockerDisableWarningForOtherDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="a4043-253">bitLockerDisableWarningForOtherDiskEncryption</span></span>|<span data-ttu-id="a4043-254">Boolean</span><span class="sxs-lookup"><span data-stu-id="a4043-254">Boolean</span></span>|<span data-ttu-id="a4043-255">Permite que el administrador deshabilite el mensaje de advertencia para otro cifrado de disco en los equipos de usuario.</span><span class="sxs-lookup"><span data-stu-id="a4043-255">Allows the Admin to disable the warning prompt for other disk encryption on the user machines.</span></span>|
|<span data-ttu-id="a4043-256">bitLockerEnableStorageCardEncryptionOnMobile</span><span class="sxs-lookup"><span data-stu-id="a4043-256">bitLockerEnableStorageCardEncryptionOnMobile</span></span>|<span data-ttu-id="a4043-257">Boolean</span><span class="sxs-lookup"><span data-stu-id="a4043-257">Boolean</span></span>|<span data-ttu-id="a4043-258">Permite que el administrador exija que se active el cifrado con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a4043-258">Allows the admin to require encryption to be turned on using BitLocker.</span></span> <span data-ttu-id="a4043-259">Esta directiva solo es válida para una SKU móvil.</span><span class="sxs-lookup"><span data-stu-id="a4043-259">This policy is valid only for a mobile SKU.</span></span>|
|<span data-ttu-id="a4043-260">bitLockerEncryptDevice</span><span class="sxs-lookup"><span data-stu-id="a4043-260">bitLockerEncryptDevice</span></span>|<span data-ttu-id="a4043-261">Boolean</span><span class="sxs-lookup"><span data-stu-id="a4043-261">Boolean</span></span>|<span data-ttu-id="a4043-262">Permite que el administrador exija que se active el cifrado con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a4043-262">Allows the admin to require encryption to be turned on using BitLocker.</span></span>|
|<span data-ttu-id="a4043-263">bitLockerRemovableDrivePolicy</span><span class="sxs-lookup"><span data-stu-id="a4043-263">bitLockerRemovableDrivePolicy</span></span>|[<span data-ttu-id="a4043-264">bitLockerRemovableDrivePolicy</span><span class="sxs-lookup"><span data-stu-id="a4043-264">bitLockerRemovableDrivePolicy</span></span>](../resources/intune_deviceconfig_bitlockerremovabledrivepolicy.md)|<span data-ttu-id="a4043-265">Directiva de unidad extraíble de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a4043-265">BitLocker Removable Drive Policy.</span></span>|



## <a name="response"></a><span data-ttu-id="a4043-266">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a4043-266">Response</span></span>
<span data-ttu-id="a4043-267">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windows10EndpointProtectionConfiguration](../resources/intune_deviceconfig_windows10endpointprotectionconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a4043-267">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_deviceconfig_windows10endpointprotectionconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a4043-268">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a4043-268">Example</span></span>
### <a name="request"></a><span data-ttu-id="a4043-269">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a4043-269">Request</span></span>
<span data-ttu-id="a4043-270">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a4043-270">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 4309

{
  "@odata.type": "#microsoft.graph.windows10EndpointProtectionConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "firewallBlockStatefulFTP": true,
  "firewallIdleTimeoutForSecurityAssociationInSeconds": 2,
  "firewallPreSharedKeyEncodingMethod": "none",
  "firewallIPSecExemptionsAllowNeighborDiscovery": true,
  "firewallIPSecExemptionsAllowICMP": true,
  "firewallIPSecExemptionsAllowRouterDiscovery": true,
  "firewallIPSecExemptionsAllowDHCP": true,
  "firewallCertificateRevocationListCheckMethod": "none",
  "firewallMergeKeyingModuleSettings": true,
  "firewallPacketQueueingMethod": "disabled",
  "firewallProfileDomain": {
    "@odata.type": "microsoft.graph.windowsFirewallNetworkProfile",
    "firewallEnabled": "blocked",
    "stealthModeBlocked": true,
    "incomingTrafficBlocked": true,
    "unicastResponsesToMulticastBroadcastsBlocked": true,
    "inboundNotificationsBlocked": true,
    "authorizedApplicationRulesFromGroupPolicyMerged": true,
    "globalPortRulesFromGroupPolicyMerged": true,
    "connectionSecurityRulesFromGroupPolicyMerged": true,
    "outboundConnectionsBlocked": true,
    "inboundConnectionsBlocked": true,
    "securedPacketExemptionAllowed": true,
    "policyRulesFromGroupPolicyMerged": true
  },
  "firewallProfilePublic": {
    "@odata.type": "microsoft.graph.windowsFirewallNetworkProfile",
    "firewallEnabled": "blocked",
    "stealthModeBlocked": true,
    "incomingTrafficBlocked": true,
    "unicastResponsesToMulticastBroadcastsBlocked": true,
    "inboundNotificationsBlocked": true,
    "authorizedApplicationRulesFromGroupPolicyMerged": true,
    "globalPortRulesFromGroupPolicyMerged": true,
    "connectionSecurityRulesFromGroupPolicyMerged": true,
    "outboundConnectionsBlocked": true,
    "inboundConnectionsBlocked": true,
    "securedPacketExemptionAllowed": true,
    "policyRulesFromGroupPolicyMerged": true
  },
  "firewallProfilePrivate": {
    "@odata.type": "microsoft.graph.windowsFirewallNetworkProfile",
    "firewallEnabled": "blocked",
    "stealthModeBlocked": true,
    "incomingTrafficBlocked": true,
    "unicastResponsesToMulticastBroadcastsBlocked": true,
    "inboundNotificationsBlocked": true,
    "authorizedApplicationRulesFromGroupPolicyMerged": true,
    "globalPortRulesFromGroupPolicyMerged": true,
    "connectionSecurityRulesFromGroupPolicyMerged": true,
    "outboundConnectionsBlocked": true,
    "inboundConnectionsBlocked": true,
    "securedPacketExemptionAllowed": true,
    "policyRulesFromGroupPolicyMerged": true
  },
  "defenderAttackSurfaceReductionExcludedPaths": [
    "Defender Attack Surface Reduction Excluded Paths value"
  ],
  "defenderGuardedFoldersAllowedAppPaths": [
    "Defender Guarded Folders Allowed App Paths value"
  ],
  "defenderAdditionalGuardedFolders": [
    "Defender Additional Guarded Folders value"
  ],
  "defenderExploitProtectionXml": "ZGVmZW5kZXJFeHBsb2l0UHJvdGVjdGlvblhtbA==",
  "defenderExploitProtectionXmlFileName": "Defender Exploit Protection Xml File Name value",
  "defenderSecurityCenterBlockExploitProtectionOverride": true,
  "appLockerApplicationControl": "enforceComponentsAndStoreApps",
  "smartScreenEnableInShell": true,
  "smartScreenBlockOverrideForFiles": true,
  "applicationGuardEnabled": true,
  "applicationGuardBlockFileTransfer": "blockImageAndTextFile",
  "applicationGuardBlockNonEnterpriseContent": true,
  "applicationGuardAllowPersistence": true,
  "applicationGuardForceAuditing": true,
  "applicationGuardBlockClipboardSharing": "blockBoth",
  "applicationGuardAllowPrintToPDF": true,
  "applicationGuardAllowPrintToXPS": true,
  "applicationGuardAllowPrintToLocalPrinters": true,
  "applicationGuardAllowPrintToNetworkPrinters": true,
  "bitLockerDisableWarningForOtherDiskEncryption": true,
  "bitLockerEnableStorageCardEncryptionOnMobile": true,
  "bitLockerEncryptDevice": true,
  "bitLockerRemovableDrivePolicy": {
    "@odata.type": "microsoft.graph.bitLockerRemovableDrivePolicy",
    "encryptionMethod": "aesCbc256",
    "requireEncryptionForWriteAccess": true,
    "blockCrossOrganizationWriteAccess": true
  }
}
```

### <a name="response"></a><span data-ttu-id="a4043-271">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a4043-271">Response</span></span>
<span data-ttu-id="a4043-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a4043-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 4417

{
  "@odata.type": "#microsoft.graph.windows10EndpointProtectionConfiguration",
  "id": "09709403-9403-0970-0394-700903947009",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "firewallBlockStatefulFTP": true,
  "firewallIdleTimeoutForSecurityAssociationInSeconds": 2,
  "firewallPreSharedKeyEncodingMethod": "none",
  "firewallIPSecExemptionsAllowNeighborDiscovery": true,
  "firewallIPSecExemptionsAllowICMP": true,
  "firewallIPSecExemptionsAllowRouterDiscovery": true,
  "firewallIPSecExemptionsAllowDHCP": true,
  "firewallCertificateRevocationListCheckMethod": "none",
  "firewallMergeKeyingModuleSettings": true,
  "firewallPacketQueueingMethod": "disabled",
  "firewallProfileDomain": {
    "@odata.type": "microsoft.graph.windowsFirewallNetworkProfile",
    "firewallEnabled": "blocked",
    "stealthModeBlocked": true,
    "incomingTrafficBlocked": true,
    "unicastResponsesToMulticastBroadcastsBlocked": true,
    "inboundNotificationsBlocked": true,
    "authorizedApplicationRulesFromGroupPolicyMerged": true,
    "globalPortRulesFromGroupPolicyMerged": true,
    "connectionSecurityRulesFromGroupPolicyMerged": true,
    "outboundConnectionsBlocked": true,
    "inboundConnectionsBlocked": true,
    "securedPacketExemptionAllowed": true,
    "policyRulesFromGroupPolicyMerged": true
  },
  "firewallProfilePublic": {
    "@odata.type": "microsoft.graph.windowsFirewallNetworkProfile",
    "firewallEnabled": "blocked",
    "stealthModeBlocked": true,
    "incomingTrafficBlocked": true,
    "unicastResponsesToMulticastBroadcastsBlocked": true,
    "inboundNotificationsBlocked": true,
    "authorizedApplicationRulesFromGroupPolicyMerged": true,
    "globalPortRulesFromGroupPolicyMerged": true,
    "connectionSecurityRulesFromGroupPolicyMerged": true,
    "outboundConnectionsBlocked": true,
    "inboundConnectionsBlocked": true,
    "securedPacketExemptionAllowed": true,
    "policyRulesFromGroupPolicyMerged": true
  },
  "firewallProfilePrivate": {
    "@odata.type": "microsoft.graph.windowsFirewallNetworkProfile",
    "firewallEnabled": "blocked",
    "stealthModeBlocked": true,
    "incomingTrafficBlocked": true,
    "unicastResponsesToMulticastBroadcastsBlocked": true,
    "inboundNotificationsBlocked": true,
    "authorizedApplicationRulesFromGroupPolicyMerged": true,
    "globalPortRulesFromGroupPolicyMerged": true,
    "connectionSecurityRulesFromGroupPolicyMerged": true,
    "outboundConnectionsBlocked": true,
    "inboundConnectionsBlocked": true,
    "securedPacketExemptionAllowed": true,
    "policyRulesFromGroupPolicyMerged": true
  },
  "defenderAttackSurfaceReductionExcludedPaths": [
    "Defender Attack Surface Reduction Excluded Paths value"
  ],
  "defenderGuardedFoldersAllowedAppPaths": [
    "Defender Guarded Folders Allowed App Paths value"
  ],
  "defenderAdditionalGuardedFolders": [
    "Defender Additional Guarded Folders value"
  ],
  "defenderExploitProtectionXml": "ZGVmZW5kZXJFeHBsb2l0UHJvdGVjdGlvblhtbA==",
  "defenderExploitProtectionXmlFileName": "Defender Exploit Protection Xml File Name value",
  "defenderSecurityCenterBlockExploitProtectionOverride": true,
  "appLockerApplicationControl": "enforceComponentsAndStoreApps",
  "smartScreenEnableInShell": true,
  "smartScreenBlockOverrideForFiles": true,
  "applicationGuardEnabled": true,
  "applicationGuardBlockFileTransfer": "blockImageAndTextFile",
  "applicationGuardBlockNonEnterpriseContent": true,
  "applicationGuardAllowPersistence": true,
  "applicationGuardForceAuditing": true,
  "applicationGuardBlockClipboardSharing": "blockBoth",
  "applicationGuardAllowPrintToPDF": true,
  "applicationGuardAllowPrintToXPS": true,
  "applicationGuardAllowPrintToLocalPrinters": true,
  "applicationGuardAllowPrintToNetworkPrinters": true,
  "bitLockerDisableWarningForOtherDiskEncryption": true,
  "bitLockerEnableStorageCardEncryptionOnMobile": true,
  "bitLockerEncryptDevice": true,
  "bitLockerRemovableDrivePolicy": {
    "@odata.type": "microsoft.graph.bitLockerRemovableDrivePolicy",
    "encryptionMethod": "aesCbc256",
    "requireEncryptionForWriteAccess": true,
    "blockCrossOrganizationWriteAccess": true
  }
}
```



