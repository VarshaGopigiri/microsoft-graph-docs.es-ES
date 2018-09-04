# <a name="create-windows10endpointprotectionconfiguration"></a><span data-ttu-id="99090-101">Crear windows10EndpointProtectionConfiguration</span><span class="sxs-lookup"><span data-stu-id="99090-101">Create windows10EndpointProtectionConfiguration</span></span>

> <span data-ttu-id="99090-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="99090-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="99090-103">Crea un objeto [windows10EndpointProtectionConfiguration](../resources/intune_deviceconfig_windows10endpointprotectionconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="99090-103">Create a new [windows10EndpointProtectionConfiguration](../resources/intune_deviceconfig_windows10endpointprotectionconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="99090-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="99090-104">Prerequisites</span></span>
<span data-ttu-id="99090-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="99090-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="99090-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="99090-107">Permission type</span></span>|<span data-ttu-id="99090-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="99090-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="99090-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="99090-109">Delegated (work or school account)</span></span>|<span data-ttu-id="99090-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="99090-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="99090-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="99090-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="99090-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="99090-112">Not supported.</span></span>|
|<span data-ttu-id="99090-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="99090-113">Application</span></span>|<span data-ttu-id="99090-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="99090-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="99090-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="99090-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="99090-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="99090-116">Request headers</span></span>
|<span data-ttu-id="99090-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="99090-117">Header</span></span>|<span data-ttu-id="99090-118">Valor</span><span class="sxs-lookup"><span data-stu-id="99090-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="99090-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="99090-119">Authorization</span></span>|<span data-ttu-id="99090-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="99090-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="99090-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="99090-121">Accept</span></span>|<span data-ttu-id="99090-122">application/json</span><span class="sxs-lookup"><span data-stu-id="99090-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="99090-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="99090-123">Request body</span></span>
<span data-ttu-id="99090-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto windows10EndpointProtectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="99090-124">In the request body, supply a JSON representation for the windows10EndpointProtectionConfiguration object.</span></span>

<span data-ttu-id="99090-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windows10EndpointProtectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="99090-125">The following table shows the properties that are required when you create the windows10EndpointProtectionConfiguration.</span></span>

|<span data-ttu-id="99090-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="99090-126">Property</span></span>|<span data-ttu-id="99090-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="99090-127">Type</span></span>|<span data-ttu-id="99090-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="99090-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="99090-129">id</span><span class="sxs-lookup"><span data-stu-id="99090-129">id</span></span>|<span data-ttu-id="99090-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="99090-130">String</span></span>|<span data-ttu-id="99090-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="99090-131">Key of the entity.</span></span> <span data-ttu-id="99090-132">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="99090-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="99090-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="99090-133">lastModifiedDateTime</span></span>|<span data-ttu-id="99090-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="99090-134">DateTimeOffset</span></span>|<span data-ttu-id="99090-135">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="99090-135">DateTime the object was last modified.</span></span> <span data-ttu-id="99090-136">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="99090-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="99090-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="99090-137">createdDateTime</span></span>|<span data-ttu-id="99090-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="99090-138">DateTimeOffset</span></span>|<span data-ttu-id="99090-139">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="99090-139">DateTime the object was created.</span></span> <span data-ttu-id="99090-140">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="99090-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="99090-141">descripción</span><span class="sxs-lookup"><span data-stu-id="99090-141">description</span></span>|<span data-ttu-id="99090-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="99090-142">String</span></span>|<span data-ttu-id="99090-143">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="99090-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="99090-144">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="99090-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="99090-145">displayName</span><span class="sxs-lookup"><span data-stu-id="99090-145">displayName</span></span>|<span data-ttu-id="99090-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="99090-146">String</span></span>|<span data-ttu-id="99090-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="99090-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="99090-148">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="99090-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="99090-149">version</span><span class="sxs-lookup"><span data-stu-id="99090-149">version</span></span>|<span data-ttu-id="99090-150">Int32</span><span class="sxs-lookup"><span data-stu-id="99090-150">Int32</span></span>|<span data-ttu-id="99090-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="99090-151">Version of the device configuration.</span></span> <span data-ttu-id="99090-152">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="99090-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="99090-153">firewallBlockStatefulFTP</span><span class="sxs-lookup"><span data-stu-id="99090-153">firewallBlockStatefulFTP</span></span>|<span data-ttu-id="99090-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="99090-154">Boolean</span></span>|<span data-ttu-id="99090-155">Bloquea las conexiones FTP con estado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="99090-155">Blocks stateful FTP connections to the device</span></span>|
|<span data-ttu-id="99090-156">firewallIdleTimeoutForSecurityAssociationInSeconds</span><span class="sxs-lookup"><span data-stu-id="99090-156">firewallIdleTimeoutForSecurityAssociationInSeconds</span></span>|<span data-ttu-id="99090-157">Int32</span><span class="sxs-lookup"><span data-stu-id="99090-157">Int32</span></span>|<span data-ttu-id="99090-158">Configura el tiempo de espera inactivo para asociaciones de seguridad, en segundos, de 300 a 3600 inclusive.</span><span class="sxs-lookup"><span data-stu-id="99090-158">Configures the idle timeout for security associations, in seconds, from 300 to 3600 inclusive.</span></span> <span data-ttu-id="99090-159">Se trata del período tras el cual expiran y se eliminan las asociaciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="99090-159">This is the period after which security associations will expire and be deleted.</span></span> <span data-ttu-id="99090-160">Valores válidos de 300 a 3600.</span><span class="sxs-lookup"><span data-stu-id="99090-160">Valid values 300 to 3600</span></span>|
|<span data-ttu-id="99090-161">firewallPreSharedKeyEncodingMethod</span><span class="sxs-lookup"><span data-stu-id="99090-161">firewallPreSharedKeyEncodingMethod</span></span>|[<span data-ttu-id="99090-162">firewallPreSharedKeyEncodingMethodType</span><span class="sxs-lookup"><span data-stu-id="99090-162">firewallPreSharedKeyEncodingMethodType</span></span>](../resources/intune_deviceconfig_firewallpresharedkeyencodingmethodtype.md)|<span data-ttu-id="99090-163">Selecciona la clave de codificación previamente compartida que se utilizará.</span><span class="sxs-lookup"><span data-stu-id="99090-163">Select the preshared key encoding to be used Possible values are: , , .</span></span> <span data-ttu-id="99090-164">Los valores posibles son: `deviceDefault`, `none` y `utF8`.</span><span class="sxs-lookup"><span data-stu-id="99090-164">The possible values are `deviceDefault`, `none`, `utF8`, , , , , , , , , or .</span></span>|
|<span data-ttu-id="99090-165">firewallIPSecExemptionsAllowNeighborDiscovery</span><span class="sxs-lookup"><span data-stu-id="99090-165">firewallIPSecExemptionsAllowNeighborDiscovery</span></span>|<span data-ttu-id="99090-166">Booleano</span><span class="sxs-lookup"><span data-stu-id="99090-166">Boolean</span></span>|<span data-ttu-id="99090-167">Configura las exenciones IPSec para permitir los códigos de tipo ICMP de IPv6 de detección de vecinos.</span><span class="sxs-lookup"><span data-stu-id="99090-167">Configures IPSec exemptions to allow neighbor discovery IPv6 ICMP type-codes</span></span>|
|<span data-ttu-id="99090-168">firewallIPSecExemptionsAllowICMP</span><span class="sxs-lookup"><span data-stu-id="99090-168">firewallIPSecExemptionsAllowICMP</span></span>|<span data-ttu-id="99090-169">Booleano</span><span class="sxs-lookup"><span data-stu-id="99090-169">Boolean</span></span>|<span data-ttu-id="99090-170">Configura las exenciones IPSec para permitir ICMP.</span><span class="sxs-lookup"><span data-stu-id="99090-170">Configures IPSec exemptions to allow ICMP</span></span>|
|<span data-ttu-id="99090-171">firewallIPSecExemptionsAllowRouterDiscovery</span><span class="sxs-lookup"><span data-stu-id="99090-171">firewallIPSecExemptionsAllowRouterDiscovery</span></span>|<span data-ttu-id="99090-172">Booleano</span><span class="sxs-lookup"><span data-stu-id="99090-172">Boolean</span></span>|<span data-ttu-id="99090-173">Configura las exenciones IPSec para permitir los códigos de tipo ICMP de IPv6 de detección de enrutadores.</span><span class="sxs-lookup"><span data-stu-id="99090-173">Configures IPSec exemptions to allow router discovery IPv6 ICMP type-codes</span></span>|
|<span data-ttu-id="99090-174">firewallIPSecExemptionsAllowDHCP</span><span class="sxs-lookup"><span data-stu-id="99090-174">firewallIPSecExemptionsAllowDHCP</span></span>|<span data-ttu-id="99090-175">Booleano</span><span class="sxs-lookup"><span data-stu-id="99090-175">Boolean</span></span>|<span data-ttu-id="99090-176">Configura las exenciones IPSec para permitir el tráfico DHCP de IPv4 e IPv6.</span><span class="sxs-lookup"><span data-stu-id="99090-176">Configures IPSec exemptions to allow both IPv4 and IPv6 DHCP traffic</span></span>|
|<span data-ttu-id="99090-177">firewallCertificateRevocationListCheckMethod</span><span class="sxs-lookup"><span data-stu-id="99090-177">firewallCertificateRevocationListCheckMethod</span></span>|[<span data-ttu-id="99090-178">firewallCertificateRevocationListCheckMethodType</span><span class="sxs-lookup"><span data-stu-id="99090-178">firewallCertificateRevocationListCheckMethodType</span></span>](../resources/intune_deviceconfig_firewallcertificaterevocationlistcheckmethodtype.md)|<span data-ttu-id="99090-179">Especifica cómo se aplica la lista de revocación de certificados.</span><span class="sxs-lookup"><span data-stu-id="99090-179">Specify how the certificate revocation list is to be enforced Possible values are: , , , .</span></span> <span data-ttu-id="99090-180">Los valores posibles son: `deviceDefault`, `none`, `attempt` y `require`.</span><span class="sxs-lookup"><span data-stu-id="99090-180">The possible values are `deviceDefault`, `none`, `attempt`, `require`, , , , , , , , or .</span></span>|
|<span data-ttu-id="99090-181">firewallMergeKeyingModuleSettings</span><span class="sxs-lookup"><span data-stu-id="99090-181">firewallMergeKeyingModuleSettings</span></span>|<span data-ttu-id="99090-182">Booleano</span><span class="sxs-lookup"><span data-stu-id="99090-182">Boolean</span></span>|<span data-ttu-id="99090-183">Si un conjunto de autenticación no es totalmente compatible con un módulo de generación de claves, dirija el módulo para que solo ignore los conjuntos de autenticación no admitidos, en lugar de todo el conjunto.</span><span class="sxs-lookup"><span data-stu-id="99090-183">If an authentication set is not fully supported by a keying module, direct the module to ignore only unsupported authentication suites rather than the entire set</span></span>|
|<span data-ttu-id="99090-184">firewallPacketQueueingMethod</span><span class="sxs-lookup"><span data-stu-id="99090-184">firewallPacketQueueingMethod</span></span>|[<span data-ttu-id="99090-185">firewallPacketQueueingMethodType</span><span class="sxs-lookup"><span data-stu-id="99090-185">firewallPacketQueueingMethodType</span></span>](../resources/intune_deviceconfig_firewallpacketqueueingmethodtype.md)|<span data-ttu-id="99090-186">Configura cómo debe aplicarse el encolado de paquetes en el escenario de puerta de enlace de túnel.</span><span class="sxs-lookup"><span data-stu-id="99090-186">Configures how packet queueing should be applied in the tunnel gateway scenario Possible values are: , , , , .</span></span> <span data-ttu-id="99090-187">Los valores posibles son: `deviceDefault`, `disabled`, `queueInbound`, `queueOutbound` y`queueBoth`.</span><span class="sxs-lookup"><span data-stu-id="99090-187">The possible values are `deviceDefault`, `disabled`, `queueInbound`, `queueOutbound`, `queueBoth`, , , , , , , or .</span></span>|
|<span data-ttu-id="99090-188">firewallProfileDomain</span><span class="sxs-lookup"><span data-stu-id="99090-188">firewallProfileDomain</span></span>|[<span data-ttu-id="99090-189">windowsFirewallNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="99090-189">windowsFirewallNetworkProfile</span></span>](../resources/intune_deviceconfig_windowsfirewallnetworkprofile.md)|<span data-ttu-id="99090-190">Configura las opciones del perfil de firewall para redes de dominio.</span><span class="sxs-lookup"><span data-stu-id="99090-190">Configures the firewall profile settings for domain networks</span></span>|
|<span data-ttu-id="99090-191">firewallProfilePublic</span><span class="sxs-lookup"><span data-stu-id="99090-191">firewallProfilePublic</span></span>|[<span data-ttu-id="99090-192">windowsFirewallNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="99090-192">windowsFirewallNetworkProfile</span></span>](../resources/intune_deviceconfig_windowsfirewallnetworkprofile.md)|<span data-ttu-id="99090-193">Configura las opciones del perfil de firewall para redes públicas.</span><span class="sxs-lookup"><span data-stu-id="99090-193">Configures the firewall profile settings for public networks</span></span>|
|<span data-ttu-id="99090-194">firewallProfilePrivate</span><span class="sxs-lookup"><span data-stu-id="99090-194">firewallProfilePrivate</span></span>|[<span data-ttu-id="99090-195">windowsFirewallNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="99090-195">windowsFirewallNetworkProfile</span></span>](../resources/intune_deviceconfig_windowsfirewallnetworkprofile.md)|<span data-ttu-id="99090-196">Configura las opciones del perfil de firewall para redes privadas.</span><span class="sxs-lookup"><span data-stu-id="99090-196">Configures the firewall profile settings for private networks</span></span>|
|<span data-ttu-id="99090-197">defenderAttackSurfaceReductionExcludedPaths</span><span class="sxs-lookup"><span data-stu-id="99090-197">defenderAttackSurfaceReductionExcludedPaths</span></span>|<span data-ttu-id="99090-198">Colección String</span><span class="sxs-lookup"><span data-stu-id="99090-198">String collection</span></span>|<span data-ttu-id="99090-199">Lista de archivos exe y carpetas que se deben excluir de las reglas de reducción de la superficie expuesta a ataques.</span><span class="sxs-lookup"><span data-stu-id="99090-199">List of exe files and folders to be excluded from attack surface reduction rules</span></span>|
|<span data-ttu-id="99090-200">defenderGuardedFoldersAllowedAppPaths</span><span class="sxs-lookup"><span data-stu-id="99090-200">defenderGuardedFoldersAllowedAppPaths</span></span>|<span data-ttu-id="99090-201">Colección String</span><span class="sxs-lookup"><span data-stu-id="99090-201">String collection</span></span>|<span data-ttu-id="99090-202">Lista de rutas de acceso a exe que pueden obtener acceso a carpetas protegidas.</span><span class="sxs-lookup"><span data-stu-id="99090-202">List of paths to exe that are allowed to access protected folders</span></span>|
|<span data-ttu-id="99090-203">defenderAdditionalGuardedFolders</span><span class="sxs-lookup"><span data-stu-id="99090-203">defenderAdditionalGuardedFolders</span></span>|<span data-ttu-id="99090-204">Colección String</span><span class="sxs-lookup"><span data-stu-id="99090-204">String collection</span></span>|<span data-ttu-id="99090-205">Lista de las rutas de acceso de carpeta que se van a agregar a la lista de carpetas protegidas.</span><span class="sxs-lookup"><span data-stu-id="99090-205">List of folder paths to be added to the list of protected folders</span></span>|
|<span data-ttu-id="99090-206">defenderExploitProtectionXml</span><span class="sxs-lookup"><span data-stu-id="99090-206">defenderExploitProtectionXml</span></span>|<span data-ttu-id="99090-207">Binario</span><span class="sxs-lookup"><span data-stu-id="99090-207">Binary</span></span>|<span data-ttu-id="99090-208">Contenido XML que contiene información sobre detalles de protección contra vulnerabilidades de seguridad.</span><span class="sxs-lookup"><span data-stu-id="99090-208">Xml content containing information regarding exploit protection details.</span></span>|
|<span data-ttu-id="99090-209">defenderExploitProtectionXmlFileName</span><span class="sxs-lookup"><span data-stu-id="99090-209">defenderExploitProtectionXmlFileName</span></span>|<span data-ttu-id="99090-210">Cadena</span><span class="sxs-lookup"><span data-stu-id="99090-210">String</span></span>|<span data-ttu-id="99090-211">Nombre del archivo del que se obtuvo DefenderExploitProtectionXml.</span><span class="sxs-lookup"><span data-stu-id="99090-211">Name of the file from which DefenderExploitProtectionXml was obtained.</span></span>|
|<span data-ttu-id="99090-212">defenderSecurityCenterBlockExploitProtectionOverride</span><span class="sxs-lookup"><span data-stu-id="99090-212">defenderSecurityCenterBlockExploitProtectionOverride</span></span>|<span data-ttu-id="99090-213">Booleano</span><span class="sxs-lookup"><span data-stu-id="99090-213">Boolean</span></span>|<span data-ttu-id="99090-214">Indica si se va a impedir que el usuario invalide la configuración de protección contra vulnerabilidades.</span><span class="sxs-lookup"><span data-stu-id="99090-214">Indicates whether or not to block user from overriding Exploit Protection settings.</span></span>|
|<span data-ttu-id="99090-215">appLockerApplicationControl</span><span class="sxs-lookup"><span data-stu-id="99090-215">appLockerApplicationControl</span></span>|[<span data-ttu-id="99090-216">appLockerApplicationControlType</span><span class="sxs-lookup"><span data-stu-id="99090-216">appLockerApplicationControlType</span></span>](../resources/intune_deviceconfig_applockerapplicationcontroltype.md)|<span data-ttu-id="99090-217">Permite que el administrador elija los tipos de aplicación que se permiten en los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="99090-217">Enables the Admin to choose what types of app to allow on devices.</span></span> <span data-ttu-id="99090-218">Los valores posibles son: `notConfigured`, `enforceComponentsAndStoreApps`, `auditComponentsAndStoreApps`, `enforceComponentsStoreAppsAndSmartlocker` y`auditComponentsStoreAppsAndSmartlocker`.</span><span class="sxs-lookup"><span data-stu-id="99090-218">The possible values are `notConfigured`, `enforceComponentsAndStoreApps`, `auditComponentsAndStoreApps`, `enforceComponentsStoreAppsAndSmartlocker`, `auditComponentsStoreAppsAndSmartlocker`, , , , , , , or .</span></span>|
|<span data-ttu-id="99090-219">smartScreenEnableInShell</span><span class="sxs-lookup"><span data-stu-id="99090-219">smartScreenEnableInShell</span></span>|<span data-ttu-id="99090-220">Booleano</span><span class="sxs-lookup"><span data-stu-id="99090-220">Boolean</span></span>|<span data-ttu-id="99090-221">Permite que los administradores de TI configuren SmartScreen para Windows.</span><span class="sxs-lookup"><span data-stu-id="99090-221">Allows IT Admins to configure SmartScreen for Windows.</span></span>|
|<span data-ttu-id="99090-222">smartScreenBlockOverrideForFiles</span><span class="sxs-lookup"><span data-stu-id="99090-222">smartScreenBlockOverrideForFiles</span></span>|<span data-ttu-id="99090-223">Booleano</span><span class="sxs-lookup"><span data-stu-id="99090-223">Boolean</span></span>|<span data-ttu-id="99090-224">Permite que los administradores de TI controlen si los usuarios pueden omitir advertencias de SmartScreen y ejecutar archivos malintencionados.</span><span class="sxs-lookup"><span data-stu-id="99090-224">Allows IT Admins to control whether users can can ignore SmartScreen warnings and run malicious files.</span></span>|
|<span data-ttu-id="99090-225">applicationGuardEnabled</span><span class="sxs-lookup"><span data-stu-id="99090-225">applicationGuardEnabled</span></span>|<span data-ttu-id="99090-226">Booleano</span><span class="sxs-lookup"><span data-stu-id="99090-226">Boolean</span></span>|<span data-ttu-id="99090-227">Habilita la Protección de aplicaciones de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="99090-227">Enable Windows Defender Application Guard</span></span>|
|<span data-ttu-id="99090-228">applicationGuardBlockFileTransfer</span><span class="sxs-lookup"><span data-stu-id="99090-228">applicationGuardBlockFileTransfer</span></span>|[<span data-ttu-id="99090-229">applicationGuardBlockFileTransferType</span><span class="sxs-lookup"><span data-stu-id="99090-229">applicationGuardBlockFileTransferType</span></span>](../resources/intune_deviceconfig_applicationguardblockfiletransfertype.md)|<span data-ttu-id="99090-230">Impide que el Portapapeles transfiera archivos de imagen, de texto o ambos.</span><span class="sxs-lookup"><span data-stu-id="99090-230">Block clipboard to transfer image file, text file or neither of them Possible values are: , , , , .</span></span> <span data-ttu-id="99090-231">Los valores posibles son: `notConfigured`, `blockImageAndTextFile`, `blockImageFile`, `blockNone` y`blockTextFile`.</span><span class="sxs-lookup"><span data-stu-id="99090-231">The possible values are `notConfigured`, `blockImageAndTextFile`, `blockImageFile`, `blockNone`, `blockTextFile`, , , , , , , or .</span></span>|
|<span data-ttu-id="99090-232">applicationGuardBlockNonEnterpriseContent</span><span class="sxs-lookup"><span data-stu-id="99090-232">applicationGuardBlockNonEnterpriseContent</span></span>|<span data-ttu-id="99090-233">Booleano</span><span class="sxs-lookup"><span data-stu-id="99090-233">Boolean</span></span>|<span data-ttu-id="99090-234">Impide que los sitios de la empresa carguen contenido no empresarial, como complementos de terceros.</span><span class="sxs-lookup"><span data-stu-id="99090-234">Block enterprise sites to load non-enterprise content, such as third party plug-ins</span></span>|
|<span data-ttu-id="99090-235">applicationGuardAllowPersistence</span><span class="sxs-lookup"><span data-stu-id="99090-235">applicationGuardAllowPersistence</span></span>|<span data-ttu-id="99090-236">Booleano</span><span class="sxs-lookup"><span data-stu-id="99090-236">Boolean</span></span>|<span data-ttu-id="99090-237">Permite el almacenamiento de los datos generados por el usuario en el contenedor de la protección de aplicaciones (favoritos, cookies, contraseñas web, etc.).</span><span class="sxs-lookup"><span data-stu-id="99090-237">Allow persisting user generated data inside the App Guard Containter (favorites, cookies, web passwords, etc.)</span></span>|
|<span data-ttu-id="99090-238">applicationGuardForceAuditing</span><span class="sxs-lookup"><span data-stu-id="99090-238">applicationGuardForceAuditing</span></span>|<span data-ttu-id="99090-239">Booleano</span><span class="sxs-lookup"><span data-stu-id="99090-239">Boolean</span></span>|<span data-ttu-id="99090-240">La auditoría forzada conservará los registros y eventos de Windows para cumplir con los criterios de seguridad y cumplimiento (algunos eventos de ejemplo son el inicio y cierre de sesión del usuario, el uso de derechos de privilegio, la instalación de software, los cambios del sistema, etc.).</span><span class="sxs-lookup"><span data-stu-id="99090-240">Force auditing will persist Windows logs and events to meet security/compliance criteria (sample events are user login-logoff, use of privilege rights, software installation, system changes, etc.)</span></span>|
|<span data-ttu-id="99090-241">applicationGuardBlockClipboardSharing</span><span class="sxs-lookup"><span data-stu-id="99090-241">applicationGuardBlockClipboardSharing</span></span>|[<span data-ttu-id="99090-242">applicationGuardBlockClipboardSharingType</span><span class="sxs-lookup"><span data-stu-id="99090-242">applicationGuardBlockClipboardSharingType</span></span>](../resources/intune_deviceconfig_applicationguardblockclipboardsharingtype.md)|<span data-ttu-id="99090-243">Impide que el Portapapeles comparta datos del host al contenedor, del contenedor al host, en ambas direcciones o en ninguna.</span><span class="sxs-lookup"><span data-stu-id="99090-243">Block clipboard to share data from Host to Container, or from Container to Host, or both ways, or neither ways.</span></span> <span data-ttu-id="99090-244">Los valores posibles son: `notConfigured`, `blockBoth`, `blockHostToContainer`, `blockContainerToHost` y`blockNone`.</span><span class="sxs-lookup"><span data-stu-id="99090-244">The possible values are `notConfigured`, `blockBoth`, `blockHostToContainer`, `blockContainerToHost`, `blockNone`, , , , , , , or .</span></span>|
|<span data-ttu-id="99090-245">applicationGuardAllowPrintToPDF</span><span class="sxs-lookup"><span data-stu-id="99090-245">applicationGuardAllowPrintToPDF</span></span>|<span data-ttu-id="99090-246">Booleano</span><span class="sxs-lookup"><span data-stu-id="99090-246">Boolean</span></span>|<span data-ttu-id="99090-247">Permite la impresión en PDF desde el contenedor.</span><span class="sxs-lookup"><span data-stu-id="99090-247">Allow printing to PDF from Container</span></span>|
|<span data-ttu-id="99090-248">applicationGuardAllowPrintToXPS</span><span class="sxs-lookup"><span data-stu-id="99090-248">applicationGuardAllowPrintToXPS</span></span>|<span data-ttu-id="99090-249">Booleano</span><span class="sxs-lookup"><span data-stu-id="99090-249">Boolean</span></span>|<span data-ttu-id="99090-250">Permite la impresión en XPS desde el contenedor.</span><span class="sxs-lookup"><span data-stu-id="99090-250">Allow printing to XPS from Container</span></span>|
|<span data-ttu-id="99090-251">applicationGuardAllowPrintToLocalPrinters</span><span class="sxs-lookup"><span data-stu-id="99090-251">applicationGuardAllowPrintToLocalPrinters</span></span>|<span data-ttu-id="99090-252">Booleano</span><span class="sxs-lookup"><span data-stu-id="99090-252">Boolean</span></span>|<span data-ttu-id="99090-253">Permite la impresión en impresoras locales desde el contenedor.</span><span class="sxs-lookup"><span data-stu-id="99090-253">Allow printing to Local Printers from Container</span></span>|
|<span data-ttu-id="99090-254">applicationGuardAllowPrintToNetworkPrinters</span><span class="sxs-lookup"><span data-stu-id="99090-254">applicationGuardAllowPrintToNetworkPrinters</span></span>|<span data-ttu-id="99090-255">Booleano</span><span class="sxs-lookup"><span data-stu-id="99090-255">Boolean</span></span>|<span data-ttu-id="99090-256">Permite la impresión en impresoras en red desde el contenedor.</span><span class="sxs-lookup"><span data-stu-id="99090-256">Allow printing to Network Printers from Container</span></span>|
|<span data-ttu-id="99090-257">bitLockerDisableWarningForOtherDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="99090-257">bitLockerDisableWarningForOtherDiskEncryption</span></span>|<span data-ttu-id="99090-258">Booleano</span><span class="sxs-lookup"><span data-stu-id="99090-258">Boolean</span></span>|<span data-ttu-id="99090-259">Permite que el administrador deshabilite el mensaje de advertencia para otro cifrado de disco en los equipos de usuario.</span><span class="sxs-lookup"><span data-stu-id="99090-259">Allows the Admin to disable the warning prompt for other disk encryption on the user machines.</span></span>|
|<span data-ttu-id="99090-260">bitLockerEnableStorageCardEncryptionOnMobile</span><span class="sxs-lookup"><span data-stu-id="99090-260">bitLockerEnableStorageCardEncryptionOnMobile</span></span>|<span data-ttu-id="99090-261">Booleano</span><span class="sxs-lookup"><span data-stu-id="99090-261">Boolean</span></span>|<span data-ttu-id="99090-262">Permite que el administrador exija que se active el cifrado con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="99090-262">Allows the admin to require encryption to be turned on using BitLocker.</span></span> <span data-ttu-id="99090-263">Esta directiva solo es válida para una SKU móvil.</span><span class="sxs-lookup"><span data-stu-id="99090-263">This policy is valid only for a mobile SKU.</span></span>|
|<span data-ttu-id="99090-264">bitLockerEncryptDevice</span><span class="sxs-lookup"><span data-stu-id="99090-264">bitLockerEncryptDevice</span></span>|<span data-ttu-id="99090-265">Booleano</span><span class="sxs-lookup"><span data-stu-id="99090-265">Boolean</span></span>|<span data-ttu-id="99090-266">Permite que el administrador exija que se active el cifrado con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="99090-266">Allows the admin to require encryption to be turned on using BitLocker.</span></span>|
|<span data-ttu-id="99090-267">bitLockerRemovableDrivePolicy</span><span class="sxs-lookup"><span data-stu-id="99090-267">bitLockerRemovableDrivePolicy</span></span>|[<span data-ttu-id="99090-268">bitLockerRemovableDrivePolicy</span><span class="sxs-lookup"><span data-stu-id="99090-268">bitLockerRemovableDrivePolicy</span></span>](../resources/intune_deviceconfig_bitlockerremovabledrivepolicy.md)|<span data-ttu-id="99090-269">Directiva de unidad extraíble de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="99090-269">BitLocker Removable Drive Policy.</span></span>|



## <a name="response"></a><span data-ttu-id="99090-270">Respuesta</span><span class="sxs-lookup"><span data-stu-id="99090-270">Response</span></span>
<span data-ttu-id="99090-271">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windows10EndpointProtectionConfiguration](../resources/intune_deviceconfig_windows10endpointprotectionconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="99090-271">If successful, this method returns a `201 Created` response code and a [windows10EndpointProtectionConfiguration](../resources/intune_deviceconfig_windows10endpointprotectionconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="99090-272">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="99090-272">Example</span></span>
### <a name="request"></a><span data-ttu-id="99090-273">Solicitud</span><span class="sxs-lookup"><span data-stu-id="99090-273">Request</span></span>
<span data-ttu-id="99090-274">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="99090-274">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="99090-275">Respuesta</span><span class="sxs-lookup"><span data-stu-id="99090-275">Response</span></span>
<span data-ttu-id="99090-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="99090-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



