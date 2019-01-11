---
title: Actualizar windows10EndpointProtectionConfiguration
description: Actualice las propiedades de un objeto windows10EndpointProtectionConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: a4391676ad9620210f0cb80339ac986b5229e856
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27859384"
---
# <a name="update-windows10endpointprotectionconfiguration"></a><span data-ttu-id="16c07-103">Actualizar windows10EndpointProtectionConfiguration</span><span class="sxs-lookup"><span data-stu-id="16c07-103">Update windows10EndpointProtectionConfiguration</span></span>

> <span data-ttu-id="16c07-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="16c07-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="16c07-105">Actualice las propiedades de un objeto [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="16c07-105">Update the properties of a [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="16c07-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="16c07-106">Prerequisites</span></span>
<span data-ttu-id="16c07-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="16c07-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="16c07-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="16c07-109">Permission type</span></span>|<span data-ttu-id="16c07-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="16c07-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="16c07-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="16c07-111">Delegated (work or school account)</span></span>|<span data-ttu-id="16c07-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="16c07-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="16c07-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="16c07-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="16c07-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="16c07-114">Not supported.</span></span>|
|<span data-ttu-id="16c07-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="16c07-115">Application</span></span>|<span data-ttu-id="16c07-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="16c07-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="16c07-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="16c07-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="16c07-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="16c07-118">Request headers</span></span>
|<span data-ttu-id="16c07-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16c07-119">Header</span></span>|<span data-ttu-id="16c07-120">Valor</span><span class="sxs-lookup"><span data-stu-id="16c07-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="16c07-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="16c07-121">Authorization</span></span>|<span data-ttu-id="16c07-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="16c07-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="16c07-123">Accept</span><span class="sxs-lookup"><span data-stu-id="16c07-123">Accept</span></span>|<span data-ttu-id="16c07-124">application/json</span><span class="sxs-lookup"><span data-stu-id="16c07-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="16c07-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="16c07-125">Request body</span></span>
<span data-ttu-id="16c07-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="16c07-126">In the request body, supply a JSON representation for the [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md) object.</span></span>

<span data-ttu-id="16c07-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="16c07-127">The following table shows the properties that are required when you create the [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md).</span></span>

|<span data-ttu-id="16c07-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="16c07-128">Property</span></span>|<span data-ttu-id="16c07-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="16c07-129">Type</span></span>|<span data-ttu-id="16c07-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="16c07-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="16c07-131">id</span><span class="sxs-lookup"><span data-stu-id="16c07-131">id</span></span>|<span data-ttu-id="16c07-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="16c07-132">String</span></span>|<span data-ttu-id="16c07-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="16c07-133">Key of the entity.</span></span> <span data-ttu-id="16c07-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="16c07-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="16c07-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="16c07-135">lastModifiedDateTime</span></span>|<span data-ttu-id="16c07-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="16c07-136">DateTimeOffset</span></span>|<span data-ttu-id="16c07-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="16c07-137">DateTime the object was last modified.</span></span> <span data-ttu-id="16c07-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="16c07-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="16c07-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="16c07-139">createdDateTime</span></span>|<span data-ttu-id="16c07-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="16c07-140">DateTimeOffset</span></span>|<span data-ttu-id="16c07-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="16c07-141">DateTime the object was created.</span></span> <span data-ttu-id="16c07-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="16c07-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="16c07-143">descripción</span><span class="sxs-lookup"><span data-stu-id="16c07-143">description</span></span>|<span data-ttu-id="16c07-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="16c07-144">String</span></span>|<span data-ttu-id="16c07-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16c07-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="16c07-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="16c07-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="16c07-147">displayName</span><span class="sxs-lookup"><span data-stu-id="16c07-147">displayName</span></span>|<span data-ttu-id="16c07-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="16c07-148">String</span></span>|<span data-ttu-id="16c07-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16c07-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="16c07-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="16c07-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="16c07-151">version</span><span class="sxs-lookup"><span data-stu-id="16c07-151">version</span></span>|<span data-ttu-id="16c07-152">Int32</span><span class="sxs-lookup"><span data-stu-id="16c07-152">Int32</span></span>|<span data-ttu-id="16c07-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16c07-153">Version of the device configuration.</span></span> <span data-ttu-id="16c07-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="16c07-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="16c07-155">firewallBlockStatefulFTP</span><span class="sxs-lookup"><span data-stu-id="16c07-155">firewallBlockStatefulFTP</span></span>|<span data-ttu-id="16c07-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="16c07-156">Boolean</span></span>|<span data-ttu-id="16c07-157">Bloquea las conexiones FTP con estado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16c07-157">Blocks stateful FTP connections to the device</span></span>|
|<span data-ttu-id="16c07-158">firewallIdleTimeoutForSecurityAssociationInSeconds</span><span class="sxs-lookup"><span data-stu-id="16c07-158">firewallIdleTimeoutForSecurityAssociationInSeconds</span></span>|<span data-ttu-id="16c07-159">Int32</span><span class="sxs-lookup"><span data-stu-id="16c07-159">Int32</span></span>|<span data-ttu-id="16c07-160">Configura el tiempo de espera inactivo para asociaciones de seguridad, en segundos, de 300 a 3600 inclusive.</span><span class="sxs-lookup"><span data-stu-id="16c07-160">Configures the idle timeout for security associations, in seconds, from 300 to 3600 inclusive.</span></span> <span data-ttu-id="16c07-161">Se trata del período tras el cual expiran y se eliminan las asociaciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="16c07-161">This is the period after which security associations will expire and be deleted.</span></span> <span data-ttu-id="16c07-162">Valores válidos de 300 a 3600.</span><span class="sxs-lookup"><span data-stu-id="16c07-162">Valid values 300 to 3600</span></span>|
|<span data-ttu-id="16c07-163">firewallPreSharedKeyEncodingMethod</span><span class="sxs-lookup"><span data-stu-id="16c07-163">firewallPreSharedKeyEncodingMethod</span></span>|[<span data-ttu-id="16c07-164">firewallPreSharedKeyEncodingMethodType</span><span class="sxs-lookup"><span data-stu-id="16c07-164">firewallPreSharedKeyEncodingMethodType</span></span>](../resources/intune-deviceconfig-firewallpresharedkeyencodingmethodtype.md)|<span data-ttu-id="16c07-165">Seleccione la clave previamente compartida de codificación que se utilizará.</span><span class="sxs-lookup"><span data-stu-id="16c07-165">Select the preshared key encoding to be used.</span></span> <span data-ttu-id="16c07-166">Los valores posibles son: `deviceDefault`, `none` y `utF8`.</span><span class="sxs-lookup"><span data-stu-id="16c07-166">Possible values are: `deviceDefault`, `none`, `utF8`.</span></span>|
|<span data-ttu-id="16c07-167">firewallIPSecExemptionsAllowNeighborDiscovery</span><span class="sxs-lookup"><span data-stu-id="16c07-167">firewallIPSecExemptionsAllowNeighborDiscovery</span></span>|<span data-ttu-id="16c07-168">Booleano</span><span class="sxs-lookup"><span data-stu-id="16c07-168">Boolean</span></span>|<span data-ttu-id="16c07-169">Configura las exenciones IPSec para permitir los códigos de tipo ICMP de IPv6 de detección de vecinos.</span><span class="sxs-lookup"><span data-stu-id="16c07-169">Configures IPSec exemptions to allow neighbor discovery IPv6 ICMP type-codes</span></span>|
|<span data-ttu-id="16c07-170">firewallIPSecExemptionsAllowICMP</span><span class="sxs-lookup"><span data-stu-id="16c07-170">firewallIPSecExemptionsAllowICMP</span></span>|<span data-ttu-id="16c07-171">Booleano</span><span class="sxs-lookup"><span data-stu-id="16c07-171">Boolean</span></span>|<span data-ttu-id="16c07-172">Configura las exenciones IPSec para permitir ICMP.</span><span class="sxs-lookup"><span data-stu-id="16c07-172">Configures IPSec exemptions to allow ICMP</span></span>|
|<span data-ttu-id="16c07-173">firewallIPSecExemptionsAllowRouterDiscovery</span><span class="sxs-lookup"><span data-stu-id="16c07-173">firewallIPSecExemptionsAllowRouterDiscovery</span></span>|<span data-ttu-id="16c07-174">Booleano</span><span class="sxs-lookup"><span data-stu-id="16c07-174">Boolean</span></span>|<span data-ttu-id="16c07-175">Configura las exenciones IPSec para permitir los códigos de tipo ICMP de IPv6 de detección de enrutadores.</span><span class="sxs-lookup"><span data-stu-id="16c07-175">Configures IPSec exemptions to allow router discovery IPv6 ICMP type-codes</span></span>|
|<span data-ttu-id="16c07-176">firewallIPSecExemptionsAllowDHCP</span><span class="sxs-lookup"><span data-stu-id="16c07-176">firewallIPSecExemptionsAllowDHCP</span></span>|<span data-ttu-id="16c07-177">Booleano</span><span class="sxs-lookup"><span data-stu-id="16c07-177">Boolean</span></span>|<span data-ttu-id="16c07-178">Configura las exenciones IPSec para permitir el tráfico DHCP de IPv4 e IPv6.</span><span class="sxs-lookup"><span data-stu-id="16c07-178">Configures IPSec exemptions to allow both IPv4 and IPv6 DHCP traffic</span></span>|
|<span data-ttu-id="16c07-179">firewallCertificateRevocationListCheckMethod</span><span class="sxs-lookup"><span data-stu-id="16c07-179">firewallCertificateRevocationListCheckMethod</span></span>|[<span data-ttu-id="16c07-180">firewallCertificateRevocationListCheckMethodType</span><span class="sxs-lookup"><span data-stu-id="16c07-180">firewallCertificateRevocationListCheckMethodType</span></span>](../resources/intune-deviceconfig-firewallcertificaterevocationlistcheckmethodtype.md)|<span data-ttu-id="16c07-181">Especificar cómo se aplica la lista de revocación de certificados.</span><span class="sxs-lookup"><span data-stu-id="16c07-181">Specify how the certificate revocation list is to be enforced.</span></span> <span data-ttu-id="16c07-182">Los valores posibles son: `deviceDefault`, `none`, `attempt` y `require`.</span><span class="sxs-lookup"><span data-stu-id="16c07-182">Possible values are: `deviceDefault`, `none`, `attempt`, `require`.</span></span>|
|<span data-ttu-id="16c07-183">firewallMergeKeyingModuleSettings</span><span class="sxs-lookup"><span data-stu-id="16c07-183">firewallMergeKeyingModuleSettings</span></span>|<span data-ttu-id="16c07-184">Booleano</span><span class="sxs-lookup"><span data-stu-id="16c07-184">Boolean</span></span>|<span data-ttu-id="16c07-185">Si un conjunto de autenticación no es totalmente compatible con un módulo de generación de claves, dirija el módulo para que solo ignore los conjuntos de autenticación no admitidos, en lugar de todo el conjunto.</span><span class="sxs-lookup"><span data-stu-id="16c07-185">If an authentication set is not fully supported by a keying module, direct the module to ignore only unsupported authentication suites rather than the entire set</span></span>|
|<span data-ttu-id="16c07-186">firewallPacketQueueingMethod</span><span class="sxs-lookup"><span data-stu-id="16c07-186">firewallPacketQueueingMethod</span></span>|[<span data-ttu-id="16c07-187">firewallPacketQueueingMethodType</span><span class="sxs-lookup"><span data-stu-id="16c07-187">firewallPacketQueueingMethodType</span></span>](../resources/intune-deviceconfig-firewallpacketqueueingmethodtype.md)|<span data-ttu-id="16c07-188">Configura cómo debe aplicarse queueing de paquetes en el escenario de puerta de enlace de túnel.</span><span class="sxs-lookup"><span data-stu-id="16c07-188">Configures how packet queueing should be applied in the tunnel gateway scenario.</span></span> <span data-ttu-id="16c07-189">Los valores posibles son: `deviceDefault`, `disabled`, `queueInbound`, `queueOutbound` y `queueBoth`.</span><span class="sxs-lookup"><span data-stu-id="16c07-189">Possible values are: `deviceDefault`, `disabled`, `queueInbound`, `queueOutbound`, `queueBoth`.</span></span>|
|<span data-ttu-id="16c07-190">firewallProfileDomain</span><span class="sxs-lookup"><span data-stu-id="16c07-190">firewallProfileDomain</span></span>|[<span data-ttu-id="16c07-191">windowsFirewallNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="16c07-191">windowsFirewallNetworkProfile</span></span>](../resources/intune-deviceconfig-windowsfirewallnetworkprofile.md)|<span data-ttu-id="16c07-192">Configura las opciones del perfil de firewall para redes de dominio.</span><span class="sxs-lookup"><span data-stu-id="16c07-192">Configures the firewall profile settings for domain networks</span></span>|
|<span data-ttu-id="16c07-193">firewallProfilePublic</span><span class="sxs-lookup"><span data-stu-id="16c07-193">firewallProfilePublic</span></span>|[<span data-ttu-id="16c07-194">windowsFirewallNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="16c07-194">windowsFirewallNetworkProfile</span></span>](../resources/intune-deviceconfig-windowsfirewallnetworkprofile.md)|<span data-ttu-id="16c07-195">Configura las opciones del perfil de firewall para redes públicas.</span><span class="sxs-lookup"><span data-stu-id="16c07-195">Configures the firewall profile settings for public networks</span></span>|
|<span data-ttu-id="16c07-196">firewallProfilePrivate</span><span class="sxs-lookup"><span data-stu-id="16c07-196">firewallProfilePrivate</span></span>|[<span data-ttu-id="16c07-197">windowsFirewallNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="16c07-197">windowsFirewallNetworkProfile</span></span>](../resources/intune-deviceconfig-windowsfirewallnetworkprofile.md)|<span data-ttu-id="16c07-198">Configura las opciones del perfil de firewall para redes privadas.</span><span class="sxs-lookup"><span data-stu-id="16c07-198">Configures the firewall profile settings for private networks</span></span>|
|<span data-ttu-id="16c07-199">defenderAttackSurfaceReductionExcludedPaths</span><span class="sxs-lookup"><span data-stu-id="16c07-199">defenderAttackSurfaceReductionExcludedPaths</span></span>|<span data-ttu-id="16c07-200">Colección String</span><span class="sxs-lookup"><span data-stu-id="16c07-200">String collection</span></span>|<span data-ttu-id="16c07-201">Lista de archivos exe y carpetas que se deben excluir de las reglas de reducción de la superficie expuesta a ataques.</span><span class="sxs-lookup"><span data-stu-id="16c07-201">List of exe files and folders to be excluded from attack surface reduction rules</span></span>|
|<span data-ttu-id="16c07-202">defenderGuardedFoldersAllowedAppPaths</span><span class="sxs-lookup"><span data-stu-id="16c07-202">defenderGuardedFoldersAllowedAppPaths</span></span>|<span data-ttu-id="16c07-203">Colección String</span><span class="sxs-lookup"><span data-stu-id="16c07-203">String collection</span></span>|<span data-ttu-id="16c07-204">Lista de rutas de acceso a exe que pueden obtener acceso a carpetas protegidas.</span><span class="sxs-lookup"><span data-stu-id="16c07-204">List of paths to exe that are allowed to access protected folders</span></span>|
|<span data-ttu-id="16c07-205">defenderAdditionalGuardedFolders</span><span class="sxs-lookup"><span data-stu-id="16c07-205">defenderAdditionalGuardedFolders</span></span>|<span data-ttu-id="16c07-206">Colección String</span><span class="sxs-lookup"><span data-stu-id="16c07-206">String collection</span></span>|<span data-ttu-id="16c07-207">Lista de las rutas de acceso de carpeta que se van a agregar a la lista de carpetas protegidas.</span><span class="sxs-lookup"><span data-stu-id="16c07-207">List of folder paths to be added to the list of protected folders</span></span>|
|<span data-ttu-id="16c07-208">defenderExploitProtectionXml</span><span class="sxs-lookup"><span data-stu-id="16c07-208">defenderExploitProtectionXml</span></span>|<span data-ttu-id="16c07-209">Binario</span><span class="sxs-lookup"><span data-stu-id="16c07-209">Binary</span></span>|<span data-ttu-id="16c07-210">Contenido XML que contiene información sobre detalles de protección contra vulnerabilidades de seguridad.</span><span class="sxs-lookup"><span data-stu-id="16c07-210">Xml content containing information regarding exploit protection details.</span></span>|
|<span data-ttu-id="16c07-211">defenderExploitProtectionXmlFileName</span><span class="sxs-lookup"><span data-stu-id="16c07-211">defenderExploitProtectionXmlFileName</span></span>|<span data-ttu-id="16c07-212">Cadena</span><span class="sxs-lookup"><span data-stu-id="16c07-212">String</span></span>|<span data-ttu-id="16c07-213">Nombre del archivo del que se obtuvo DefenderExploitProtectionXml.</span><span class="sxs-lookup"><span data-stu-id="16c07-213">Name of the file from which DefenderExploitProtectionXml was obtained.</span></span>|
|<span data-ttu-id="16c07-214">defenderSecurityCenterBlockExploitProtectionOverride</span><span class="sxs-lookup"><span data-stu-id="16c07-214">defenderSecurityCenterBlockExploitProtectionOverride</span></span>|<span data-ttu-id="16c07-215">Booleano</span><span class="sxs-lookup"><span data-stu-id="16c07-215">Boolean</span></span>|<span data-ttu-id="16c07-216">Indica si se va a impedir que el usuario invalide la configuración de protección contra vulnerabilidades.</span><span class="sxs-lookup"><span data-stu-id="16c07-216">Indicates whether or not to block user from overriding Exploit Protection settings.</span></span>|
|<span data-ttu-id="16c07-217">appLockerApplicationControl</span><span class="sxs-lookup"><span data-stu-id="16c07-217">appLockerApplicationControl</span></span>|[<span data-ttu-id="16c07-218">appLockerApplicationControlType</span><span class="sxs-lookup"><span data-stu-id="16c07-218">appLockerApplicationControlType</span></span>](../resources/intune-deviceconfig-applockerapplicationcontroltype.md)|<span data-ttu-id="16c07-219">Permite que el administrador elija los tipos de aplicación que se permiten en los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="16c07-219">Enables the Admin to choose what types of app to allow on devices.</span></span> <span data-ttu-id="16c07-220">Los valores posibles son: `notConfigured`, `enforceComponentsAndStoreApps`, `auditComponentsAndStoreApps`, `enforceComponentsStoreAppsAndSmartlocker` y `auditComponentsStoreAppsAndSmartlocker`.</span><span class="sxs-lookup"><span data-stu-id="16c07-220">Possible values are: `notConfigured`, `enforceComponentsAndStoreApps`, `auditComponentsAndStoreApps`, `enforceComponentsStoreAppsAndSmartlocker`, `auditComponentsStoreAppsAndSmartlocker`.</span></span>|
|<span data-ttu-id="16c07-221">smartScreenEnableInShell</span><span class="sxs-lookup"><span data-stu-id="16c07-221">smartScreenEnableInShell</span></span>|<span data-ttu-id="16c07-222">Booleano</span><span class="sxs-lookup"><span data-stu-id="16c07-222">Boolean</span></span>|<span data-ttu-id="16c07-223">Permite que los administradores de TI configuren SmartScreen para Windows.</span><span class="sxs-lookup"><span data-stu-id="16c07-223">Allows IT Admins to configure SmartScreen for Windows.</span></span>|
|<span data-ttu-id="16c07-224">smartScreenBlockOverrideForFiles</span><span class="sxs-lookup"><span data-stu-id="16c07-224">smartScreenBlockOverrideForFiles</span></span>|<span data-ttu-id="16c07-225">Booleano</span><span class="sxs-lookup"><span data-stu-id="16c07-225">Boolean</span></span>|<span data-ttu-id="16c07-226">Permite que los administradores de TI controlen si los usuarios pueden omitir advertencias de SmartScreen y ejecutar archivos malintencionados.</span><span class="sxs-lookup"><span data-stu-id="16c07-226">Allows IT Admins to control whether users can can ignore SmartScreen warnings and run malicious files.</span></span>|
|<span data-ttu-id="16c07-227">applicationGuardEnabled</span><span class="sxs-lookup"><span data-stu-id="16c07-227">applicationGuardEnabled</span></span>|<span data-ttu-id="16c07-228">Booleano</span><span class="sxs-lookup"><span data-stu-id="16c07-228">Boolean</span></span>|<span data-ttu-id="16c07-229">Habilita la Protección de aplicaciones de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="16c07-229">Enable Windows Defender Application Guard</span></span>|
|<span data-ttu-id="16c07-230">applicationGuardBlockFileTransfer</span><span class="sxs-lookup"><span data-stu-id="16c07-230">applicationGuardBlockFileTransfer</span></span>|[<span data-ttu-id="16c07-231">applicationGuardBlockFileTransferType</span><span class="sxs-lookup"><span data-stu-id="16c07-231">applicationGuardBlockFileTransferType</span></span>](../resources/intune-deviceconfig-applicationguardblockfiletransfertype.md)|<span data-ttu-id="16c07-232">Portapapeles de bloqueo para el archivo de transferencia de imagen, archivo de texto o ninguno de ellos.</span><span class="sxs-lookup"><span data-stu-id="16c07-232">Block clipboard to transfer image file, text file or neither of them.</span></span> <span data-ttu-id="16c07-233">Los valores posibles son: `notConfigured`, `blockImageAndTextFile`, `blockImageFile`, `blockNone` y `blockTextFile`.</span><span class="sxs-lookup"><span data-stu-id="16c07-233">Possible values are: `notConfigured`, `blockImageAndTextFile`, `blockImageFile`, `blockNone`, `blockTextFile`.</span></span>|
|<span data-ttu-id="16c07-234">applicationGuardBlockNonEnterpriseContent</span><span class="sxs-lookup"><span data-stu-id="16c07-234">applicationGuardBlockNonEnterpriseContent</span></span>|<span data-ttu-id="16c07-235">Booleano</span><span class="sxs-lookup"><span data-stu-id="16c07-235">Boolean</span></span>|<span data-ttu-id="16c07-236">Impide que los sitios de la empresa carguen contenido no empresarial, como complementos de terceros.</span><span class="sxs-lookup"><span data-stu-id="16c07-236">Block enterprise sites to load non-enterprise content, such as third party plug-ins</span></span>|
|<span data-ttu-id="16c07-237">applicationGuardAllowPersistence</span><span class="sxs-lookup"><span data-stu-id="16c07-237">applicationGuardAllowPersistence</span></span>|<span data-ttu-id="16c07-238">Booleano</span><span class="sxs-lookup"><span data-stu-id="16c07-238">Boolean</span></span>|<span data-ttu-id="16c07-239">Permite el almacenamiento de los datos generados por el usuario en el contenedor de la protección de aplicaciones (favoritos, cookies, contraseñas web, etc.).</span><span class="sxs-lookup"><span data-stu-id="16c07-239">Allow persisting user generated data inside the App Guard Containter (favorites, cookies, web passwords, etc.)</span></span>|
|<span data-ttu-id="16c07-240">applicationGuardForceAuditing</span><span class="sxs-lookup"><span data-stu-id="16c07-240">applicationGuardForceAuditing</span></span>|<span data-ttu-id="16c07-241">Booleano</span><span class="sxs-lookup"><span data-stu-id="16c07-241">Boolean</span></span>|<span data-ttu-id="16c07-242">La auditoría forzada conservará los registros y eventos de Windows para cumplir con los criterios de seguridad y cumplimiento (algunos eventos de ejemplo son el inicio y cierre de sesión del usuario, el uso de derechos de privilegio, la instalación de software, los cambios del sistema, etc.).</span><span class="sxs-lookup"><span data-stu-id="16c07-242">Force auditing will persist Windows logs and events to meet security/compliance criteria (sample events are user login-logoff, use of privilege rights, software installation, system changes, etc.)</span></span>|
|<span data-ttu-id="16c07-243">applicationGuardBlockClipboardSharing</span><span class="sxs-lookup"><span data-stu-id="16c07-243">applicationGuardBlockClipboardSharing</span></span>|[<span data-ttu-id="16c07-244">applicationGuardBlockClipboardSharingType</span><span class="sxs-lookup"><span data-stu-id="16c07-244">applicationGuardBlockClipboardSharingType</span></span>](../resources/intune-deviceconfig-applicationguardblockclipboardsharingtype.md)|<span data-ttu-id="16c07-245">Impide que el Portapapeles comparta los datos del host al contenedor, del contenedor al host, en ambas direcciones o en ninguna.</span><span class="sxs-lookup"><span data-stu-id="16c07-245">Block clipboard to share data from Host to Container, or from Container to Host, or both ways, or neither ways.</span></span> <span data-ttu-id="16c07-246">Los valores posibles son: `notConfigured`, `blockBoth`, `blockHostToContainer`, `blockContainerToHost` y `blockNone`.</span><span class="sxs-lookup"><span data-stu-id="16c07-246">Possible values are: `notConfigured`, `blockBoth`, `blockHostToContainer`, `blockContainerToHost`, `blockNone`.</span></span>|
|<span data-ttu-id="16c07-247">applicationGuardAllowPrintToPDF</span><span class="sxs-lookup"><span data-stu-id="16c07-247">applicationGuardAllowPrintToPDF</span></span>|<span data-ttu-id="16c07-248">Booleano</span><span class="sxs-lookup"><span data-stu-id="16c07-248">Boolean</span></span>|<span data-ttu-id="16c07-249">Permite la impresión en PDF desde el contenedor.</span><span class="sxs-lookup"><span data-stu-id="16c07-249">Allow printing to PDF from Container</span></span>|
|<span data-ttu-id="16c07-250">applicationGuardAllowPrintToXPS</span><span class="sxs-lookup"><span data-stu-id="16c07-250">applicationGuardAllowPrintToXPS</span></span>|<span data-ttu-id="16c07-251">Booleano</span><span class="sxs-lookup"><span data-stu-id="16c07-251">Boolean</span></span>|<span data-ttu-id="16c07-252">Permite la impresión en XPS desde el contenedor.</span><span class="sxs-lookup"><span data-stu-id="16c07-252">Allow printing to XPS from Container</span></span>|
|<span data-ttu-id="16c07-253">applicationGuardAllowPrintToLocalPrinters</span><span class="sxs-lookup"><span data-stu-id="16c07-253">applicationGuardAllowPrintToLocalPrinters</span></span>|<span data-ttu-id="16c07-254">Booleano</span><span class="sxs-lookup"><span data-stu-id="16c07-254">Boolean</span></span>|<span data-ttu-id="16c07-255">Permite la impresión en impresoras locales desde el contenedor.</span><span class="sxs-lookup"><span data-stu-id="16c07-255">Allow printing to Local Printers from Container</span></span>|
|<span data-ttu-id="16c07-256">applicationGuardAllowPrintToNetworkPrinters</span><span class="sxs-lookup"><span data-stu-id="16c07-256">applicationGuardAllowPrintToNetworkPrinters</span></span>|<span data-ttu-id="16c07-257">Booleano</span><span class="sxs-lookup"><span data-stu-id="16c07-257">Boolean</span></span>|<span data-ttu-id="16c07-258">Permite la impresión en impresoras en red desde el contenedor.</span><span class="sxs-lookup"><span data-stu-id="16c07-258">Allow printing to Network Printers from Container</span></span>|
|<span data-ttu-id="16c07-259">bitLockerDisableWarningForOtherDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="16c07-259">bitLockerDisableWarningForOtherDiskEncryption</span></span>|<span data-ttu-id="16c07-260">Booleano</span><span class="sxs-lookup"><span data-stu-id="16c07-260">Boolean</span></span>|<span data-ttu-id="16c07-261">Permite que el administrador deshabilite el mensaje de advertencia para otro cifrado de disco en los equipos de usuario.</span><span class="sxs-lookup"><span data-stu-id="16c07-261">Allows the Admin to disable the warning prompt for other disk encryption on the user machines.</span></span>|
|<span data-ttu-id="16c07-262">bitLockerEnableStorageCardEncryptionOnMobile</span><span class="sxs-lookup"><span data-stu-id="16c07-262">bitLockerEnableStorageCardEncryptionOnMobile</span></span>|<span data-ttu-id="16c07-263">Booleano</span><span class="sxs-lookup"><span data-stu-id="16c07-263">Boolean</span></span>|<span data-ttu-id="16c07-264">Permite que el administrador exija que se active el cifrado con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="16c07-264">Allows the admin to require encryption to be turned on using BitLocker.</span></span> <span data-ttu-id="16c07-265">Esta directiva solo es válida para una SKU móvil.</span><span class="sxs-lookup"><span data-stu-id="16c07-265">This policy is valid only for a mobile SKU.</span></span>|
|<span data-ttu-id="16c07-266">bitLockerEncryptDevice</span><span class="sxs-lookup"><span data-stu-id="16c07-266">bitLockerEncryptDevice</span></span>|<span data-ttu-id="16c07-267">Booleano</span><span class="sxs-lookup"><span data-stu-id="16c07-267">Boolean</span></span>|<span data-ttu-id="16c07-268">Permite que el administrador exija que se active el cifrado con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="16c07-268">Allows the admin to require encryption to be turned on using BitLocker.</span></span>|
|<span data-ttu-id="16c07-269">bitLockerRemovableDrivePolicy</span><span class="sxs-lookup"><span data-stu-id="16c07-269">bitLockerRemovableDrivePolicy</span></span>|[<span data-ttu-id="16c07-270">bitLockerRemovableDrivePolicy</span><span class="sxs-lookup"><span data-stu-id="16c07-270">bitLockerRemovableDrivePolicy</span></span>](../resources/intune-deviceconfig-bitlockerremovabledrivepolicy.md)|<span data-ttu-id="16c07-271">Directiva de unidad extraíble de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="16c07-271">BitLocker Removable Drive Policy.</span></span>|



## <a name="response"></a><span data-ttu-id="16c07-272">Respuesta</span><span class="sxs-lookup"><span data-stu-id="16c07-272">Response</span></span>
<span data-ttu-id="16c07-273">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="16c07-273">If successful, this method returns a `200 OK` response code and an updated [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="16c07-274">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="16c07-274">Example</span></span>
### <a name="request"></a><span data-ttu-id="16c07-275">Solicitud</span><span class="sxs-lookup"><span data-stu-id="16c07-275">Request</span></span>
<span data-ttu-id="16c07-276">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="16c07-276">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 4245

{
  "@odata.type": "#microsoft.graph.windows10EndpointProtectionConfiguration",
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

### <a name="response"></a><span data-ttu-id="16c07-277">Respuesta</span><span class="sxs-lookup"><span data-stu-id="16c07-277">Response</span></span>
<span data-ttu-id="16c07-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="16c07-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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



