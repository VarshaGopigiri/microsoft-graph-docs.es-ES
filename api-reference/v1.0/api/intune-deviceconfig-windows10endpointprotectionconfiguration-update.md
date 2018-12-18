---
title: Actualizar windows10EndpointProtectionConfiguration
description: Actualice las propiedades de un objeto windows10EndpointProtectionConfiguration.
author: tfitzmac
ms.openlocfilehash: 7116f7a6eef8c3ae26d5588191eec471a53373b7
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27313982"
---
# <a name="update-windows10endpointprotectionconfiguration"></a><span data-ttu-id="d4f9c-103">Actualizar windows10EndpointProtectionConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4f9c-103">Update windows10EndpointProtectionConfiguration</span></span>

> <span data-ttu-id="d4f9c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d4f9c-105">Actualice las propiedades de un objeto [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="d4f9c-105">Update the properties of a [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d4f9c-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d4f9c-106">Prerequisites</span></span>
<span data-ttu-id="d4f9c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d4f9c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d4f9c-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d4f9c-109">Permission type</span></span>|<span data-ttu-id="d4f9c-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d4f9c-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d4f9c-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d4f9c-111">Delegated (work or school account)</span></span>|<span data-ttu-id="d4f9c-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d4f9c-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="d4f9c-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d4f9c-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d4f9c-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-114">Not supported.</span></span>|
|<span data-ttu-id="d4f9c-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d4f9c-115">Application</span></span>|<span data-ttu-id="d4f9c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d4f9c-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d4f9c-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="d4f9c-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d4f9c-118">Request headers</span></span>
|<span data-ttu-id="d4f9c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4f9c-119">Header</span></span>|<span data-ttu-id="d4f9c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d4f9c-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d4f9c-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="d4f9c-121">Authorization</span></span>|<span data-ttu-id="d4f9c-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d4f9c-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d4f9c-123">Accept</span></span>|<span data-ttu-id="d4f9c-124">application/json</span><span class="sxs-lookup"><span data-stu-id="d4f9c-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d4f9c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d4f9c-125">Request body</span></span>
<span data-ttu-id="d4f9c-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="d4f9c-126">In the request body, supply a JSON representation for the [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md) object.</span></span>

<span data-ttu-id="d4f9c-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="d4f9c-127">The following table shows the properties that are required when you create the [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md).</span></span>

|<span data-ttu-id="d4f9c-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d4f9c-128">Property</span></span>|<span data-ttu-id="d4f9c-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="d4f9c-129">Type</span></span>|<span data-ttu-id="d4f9c-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4f9c-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d4f9c-131">id</span><span class="sxs-lookup"><span data-stu-id="d4f9c-131">id</span></span>|<span data-ttu-id="d4f9c-132">String</span><span class="sxs-lookup"><span data-stu-id="d4f9c-132">String</span></span>|<span data-ttu-id="d4f9c-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-133">Key of the entity.</span></span> <span data-ttu-id="d4f9c-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d4f9c-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d4f9c-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="d4f9c-135">lastModifiedDateTime</span></span>|<span data-ttu-id="d4f9c-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d4f9c-136">DateTimeOffset</span></span>|<span data-ttu-id="d4f9c-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-137">DateTime the object was last modified.</span></span> <span data-ttu-id="d4f9c-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d4f9c-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d4f9c-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="d4f9c-139">createdDateTime</span></span>|<span data-ttu-id="d4f9c-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d4f9c-140">DateTimeOffset</span></span>|<span data-ttu-id="d4f9c-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-141">DateTime the object was created.</span></span> <span data-ttu-id="d4f9c-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d4f9c-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d4f9c-143">descripción</span><span class="sxs-lookup"><span data-stu-id="d4f9c-143">description</span></span>|<span data-ttu-id="d4f9c-144">String</span><span class="sxs-lookup"><span data-stu-id="d4f9c-144">String</span></span>|<span data-ttu-id="d4f9c-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="d4f9c-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d4f9c-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d4f9c-147">displayName</span><span class="sxs-lookup"><span data-stu-id="d4f9c-147">displayName</span></span>|<span data-ttu-id="d4f9c-148">String</span><span class="sxs-lookup"><span data-stu-id="d4f9c-148">String</span></span>|<span data-ttu-id="d4f9c-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="d4f9c-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d4f9c-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d4f9c-151">version</span><span class="sxs-lookup"><span data-stu-id="d4f9c-151">version</span></span>|<span data-ttu-id="d4f9c-152">Int32</span><span class="sxs-lookup"><span data-stu-id="d4f9c-152">Int32</span></span>|<span data-ttu-id="d4f9c-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-153">Version of the device configuration.</span></span> <span data-ttu-id="d4f9c-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d4f9c-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d4f9c-155">firewallBlockStatefulFTP</span><span class="sxs-lookup"><span data-stu-id="d4f9c-155">firewallBlockStatefulFTP</span></span>|<span data-ttu-id="d4f9c-156">Boolean</span><span class="sxs-lookup"><span data-stu-id="d4f9c-156">Boolean</span></span>|<span data-ttu-id="d4f9c-157">Bloquea las conexiones FTP con estado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-157">Blocks stateful FTP connections to the device</span></span>|
|<span data-ttu-id="d4f9c-158">firewallIdleTimeoutForSecurityAssociationInSeconds</span><span class="sxs-lookup"><span data-stu-id="d4f9c-158">firewallIdleTimeoutForSecurityAssociationInSeconds</span></span>|<span data-ttu-id="d4f9c-159">Int32</span><span class="sxs-lookup"><span data-stu-id="d4f9c-159">Int32</span></span>|<span data-ttu-id="d4f9c-160">Configura el tiempo de espera inactivo para asociaciones de seguridad, en segundos, de 300 a 3600 inclusive.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-160">Configures the idle timeout for security associations, in seconds, from 300 to 3600 inclusive.</span></span> <span data-ttu-id="d4f9c-161">Se trata del período tras el cual expiran y se eliminan las asociaciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-161">This is the period after which security associations will expire and be deleted.</span></span> <span data-ttu-id="d4f9c-162">Valores válidos de 300 a 3600.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-162">Valid values 300 to 3600</span></span>|
|<span data-ttu-id="d4f9c-163">firewallPreSharedKeyEncodingMethod</span><span class="sxs-lookup"><span data-stu-id="d4f9c-163">firewallPreSharedKeyEncodingMethod</span></span>|[<span data-ttu-id="d4f9c-164">firewallPreSharedKeyEncodingMethodType</span><span class="sxs-lookup"><span data-stu-id="d4f9c-164">firewallPreSharedKeyEncodingMethodType</span></span>](../resources/intune-deviceconfig-firewallpresharedkeyencodingmethodtype.md)|<span data-ttu-id="d4f9c-165">Seleccione la clave previamente compartida de codificación que se utilizará.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-165">Select the preshared key encoding to be used.</span></span> <span data-ttu-id="d4f9c-166">Los valores posibles son: `deviceDefault`, `none` y `utF8`.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-166">Possible values are: `deviceDefault`, `none`, `utF8`.</span></span>|
|<span data-ttu-id="d4f9c-167">firewallIPSecExemptionsAllowNeighborDiscovery</span><span class="sxs-lookup"><span data-stu-id="d4f9c-167">firewallIPSecExemptionsAllowNeighborDiscovery</span></span>|<span data-ttu-id="d4f9c-168">Boolean</span><span class="sxs-lookup"><span data-stu-id="d4f9c-168">Boolean</span></span>|<span data-ttu-id="d4f9c-169">Configura las exenciones IPSec para permitir los códigos de tipo ICMP de IPv6 de detección de vecinos.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-169">Configures IPSec exemptions to allow neighbor discovery IPv6 ICMP type-codes</span></span>|
|<span data-ttu-id="d4f9c-170">firewallIPSecExemptionsAllowICMP</span><span class="sxs-lookup"><span data-stu-id="d4f9c-170">firewallIPSecExemptionsAllowICMP</span></span>|<span data-ttu-id="d4f9c-171">Boolean</span><span class="sxs-lookup"><span data-stu-id="d4f9c-171">Boolean</span></span>|<span data-ttu-id="d4f9c-172">Configura las exenciones IPSec para permitir ICMP.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-172">Configures IPSec exemptions to allow ICMP</span></span>|
|<span data-ttu-id="d4f9c-173">firewallIPSecExemptionsAllowRouterDiscovery</span><span class="sxs-lookup"><span data-stu-id="d4f9c-173">firewallIPSecExemptionsAllowRouterDiscovery</span></span>|<span data-ttu-id="d4f9c-174">Boolean</span><span class="sxs-lookup"><span data-stu-id="d4f9c-174">Boolean</span></span>|<span data-ttu-id="d4f9c-175">Configura las exenciones IPSec para permitir los códigos de tipo ICMP de IPv6 de detección de enrutadores.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-175">Configures IPSec exemptions to allow router discovery IPv6 ICMP type-codes</span></span>|
|<span data-ttu-id="d4f9c-176">firewallIPSecExemptionsAllowDHCP</span><span class="sxs-lookup"><span data-stu-id="d4f9c-176">firewallIPSecExemptionsAllowDHCP</span></span>|<span data-ttu-id="d4f9c-177">Boolean</span><span class="sxs-lookup"><span data-stu-id="d4f9c-177">Boolean</span></span>|<span data-ttu-id="d4f9c-178">Configura las exenciones IPSec para permitir el tráfico DHCP de IPv4 e IPv6.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-178">Configures IPSec exemptions to allow both IPv4 and IPv6 DHCP traffic</span></span>|
|<span data-ttu-id="d4f9c-179">firewallCertificateRevocationListCheckMethod</span><span class="sxs-lookup"><span data-stu-id="d4f9c-179">firewallCertificateRevocationListCheckMethod</span></span>|[<span data-ttu-id="d4f9c-180">firewallCertificateRevocationListCheckMethodType</span><span class="sxs-lookup"><span data-stu-id="d4f9c-180">firewallCertificateRevocationListCheckMethodType</span></span>](../resources/intune-deviceconfig-firewallcertificaterevocationlistcheckmethodtype.md)|<span data-ttu-id="d4f9c-181">Especificar cómo se aplica la lista de revocación de certificados.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-181">Specify how the certificate revocation list is to be enforced.</span></span> <span data-ttu-id="d4f9c-182">Los valores posibles son: `deviceDefault`, `none`, `attempt` y `require`.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-182">Possible values are: `deviceDefault`, `none`, `attempt`, `require`.</span></span>|
|<span data-ttu-id="d4f9c-183">firewallMergeKeyingModuleSettings</span><span class="sxs-lookup"><span data-stu-id="d4f9c-183">firewallMergeKeyingModuleSettings</span></span>|<span data-ttu-id="d4f9c-184">Booleano</span><span class="sxs-lookup"><span data-stu-id="d4f9c-184">Boolean</span></span>|<span data-ttu-id="d4f9c-185">Si un conjunto de autenticación no es totalmente compatible con un módulo de generación de claves, dirija el módulo para que solo ignore los conjuntos de autenticación no admitidos, en lugar de todo el conjunto.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-185">If an authentication set is not fully supported by a keying module, direct the module to ignore only unsupported authentication suites rather than the entire set</span></span>|
|<span data-ttu-id="d4f9c-186">firewallPacketQueueingMethod</span><span class="sxs-lookup"><span data-stu-id="d4f9c-186">firewallPacketQueueingMethod</span></span>|[<span data-ttu-id="d4f9c-187">firewallPacketQueueingMethodType</span><span class="sxs-lookup"><span data-stu-id="d4f9c-187">firewallPacketQueueingMethodType</span></span>](../resources/intune-deviceconfig-firewallpacketqueueingmethodtype.md)|<span data-ttu-id="d4f9c-188">Configura cómo debe aplicarse queueing de paquetes en el escenario de puerta de enlace de túnel.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-188">Configures how packet queueing should be applied in the tunnel gateway scenario.</span></span> <span data-ttu-id="d4f9c-189">Los valores posibles son: `deviceDefault`, `disabled`, `queueInbound`, `queueOutbound` y `queueBoth`.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-189">Possible values are: `deviceDefault`, `disabled`, `queueInbound`, `queueOutbound`, `queueBoth`.</span></span>|
|<span data-ttu-id="d4f9c-190">firewallProfileDomain</span><span class="sxs-lookup"><span data-stu-id="d4f9c-190">firewallProfileDomain</span></span>|[<span data-ttu-id="d4f9c-191">windowsFirewallNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d4f9c-191">windowsFirewallNetworkProfile</span></span>](../resources/intune-deviceconfig-windowsfirewallnetworkprofile.md)|<span data-ttu-id="d4f9c-192">Configura las opciones del perfil de firewall para redes de dominio.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-192">Configures the firewall profile settings for domain networks</span></span>|
|<span data-ttu-id="d4f9c-193">firewallProfilePublic</span><span class="sxs-lookup"><span data-stu-id="d4f9c-193">firewallProfilePublic</span></span>|[<span data-ttu-id="d4f9c-194">windowsFirewallNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d4f9c-194">windowsFirewallNetworkProfile</span></span>](../resources/intune-deviceconfig-windowsfirewallnetworkprofile.md)|<span data-ttu-id="d4f9c-195">Configura las opciones del perfil de firewall para redes públicas.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-195">Configures the firewall profile settings for public networks</span></span>|
|<span data-ttu-id="d4f9c-196">firewallProfilePrivate</span><span class="sxs-lookup"><span data-stu-id="d4f9c-196">firewallProfilePrivate</span></span>|[<span data-ttu-id="d4f9c-197">windowsFirewallNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d4f9c-197">windowsFirewallNetworkProfile</span></span>](../resources/intune-deviceconfig-windowsfirewallnetworkprofile.md)|<span data-ttu-id="d4f9c-198">Configura las opciones del perfil de firewall para redes privadas.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-198">Configures the firewall profile settings for private networks</span></span>|
|<span data-ttu-id="d4f9c-199">defenderAttackSurfaceReductionExcludedPaths</span><span class="sxs-lookup"><span data-stu-id="d4f9c-199">defenderAttackSurfaceReductionExcludedPaths</span></span>|<span data-ttu-id="d4f9c-200">Colección String</span><span class="sxs-lookup"><span data-stu-id="d4f9c-200">String collection</span></span>|<span data-ttu-id="d4f9c-201">Lista de archivos exe y carpetas que se deben excluir de las reglas de reducción de la superficie expuesta a ataques.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-201">List of exe files and folders to be excluded from attack surface reduction rules</span></span>|
|<span data-ttu-id="d4f9c-202">defenderGuardedFoldersAllowedAppPaths</span><span class="sxs-lookup"><span data-stu-id="d4f9c-202">defenderGuardedFoldersAllowedAppPaths</span></span>|<span data-ttu-id="d4f9c-203">Colección String</span><span class="sxs-lookup"><span data-stu-id="d4f9c-203">String collection</span></span>|<span data-ttu-id="d4f9c-204">Lista de rutas de acceso a exe que pueden obtener acceso a carpetas protegidas.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-204">List of paths to exe that are allowed to access protected folders</span></span>|
|<span data-ttu-id="d4f9c-205">defenderAdditionalGuardedFolders</span><span class="sxs-lookup"><span data-stu-id="d4f9c-205">defenderAdditionalGuardedFolders</span></span>|<span data-ttu-id="d4f9c-206">Colección String</span><span class="sxs-lookup"><span data-stu-id="d4f9c-206">String collection</span></span>|<span data-ttu-id="d4f9c-207">Lista de las rutas de acceso de carpeta que se van a agregar a la lista de carpetas protegidas.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-207">List of folder paths to be added to the list of protected folders</span></span>|
|<span data-ttu-id="d4f9c-208">defenderExploitProtectionXml</span><span class="sxs-lookup"><span data-stu-id="d4f9c-208">defenderExploitProtectionXml</span></span>|<span data-ttu-id="d4f9c-209">Binario</span><span class="sxs-lookup"><span data-stu-id="d4f9c-209">Binary</span></span>|<span data-ttu-id="d4f9c-210">Contenido XML que contiene información sobre detalles de protección contra vulnerabilidades de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-210">Xml content containing information regarding exploit protection details.</span></span>|
|<span data-ttu-id="d4f9c-211">defenderExploitProtectionXmlFileName</span><span class="sxs-lookup"><span data-stu-id="d4f9c-211">defenderExploitProtectionXmlFileName</span></span>|<span data-ttu-id="d4f9c-212">String</span><span class="sxs-lookup"><span data-stu-id="d4f9c-212">String</span></span>|<span data-ttu-id="d4f9c-213">Nombre del archivo del que se obtuvo DefenderExploitProtectionXml.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-213">Name of the file from which DefenderExploitProtectionXml was obtained.</span></span>|
|<span data-ttu-id="d4f9c-214">defenderSecurityCenterBlockExploitProtectionOverride</span><span class="sxs-lookup"><span data-stu-id="d4f9c-214">defenderSecurityCenterBlockExploitProtectionOverride</span></span>|<span data-ttu-id="d4f9c-215">Boolean</span><span class="sxs-lookup"><span data-stu-id="d4f9c-215">Boolean</span></span>|<span data-ttu-id="d4f9c-216">Indica si se va a impedir que el usuario invalide la configuración de protección contra vulnerabilidades.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-216">Indicates whether or not to block user from overriding Exploit Protection settings.</span></span>|
|<span data-ttu-id="d4f9c-217">appLockerApplicationControl</span><span class="sxs-lookup"><span data-stu-id="d4f9c-217">appLockerApplicationControl</span></span>|[<span data-ttu-id="d4f9c-218">appLockerApplicationControlType</span><span class="sxs-lookup"><span data-stu-id="d4f9c-218">appLockerApplicationControlType</span></span>](../resources/intune-deviceconfig-applockerapplicationcontroltype.md)|<span data-ttu-id="d4f9c-219">Permite que el administrador elija los tipos de aplicación que se permiten en los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-219">Enables the Admin to choose what types of app to allow on devices.</span></span> <span data-ttu-id="d4f9c-220">Los valores posibles son: `notConfigured`, `enforceComponentsAndStoreApps`, `auditComponentsAndStoreApps`, `enforceComponentsStoreAppsAndSmartlocker` y `auditComponentsStoreAppsAndSmartlocker`.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-220">Possible values are: `notConfigured`, `enforceComponentsAndStoreApps`, `auditComponentsAndStoreApps`, `enforceComponentsStoreAppsAndSmartlocker`, `auditComponentsStoreAppsAndSmartlocker`.</span></span>|
|<span data-ttu-id="d4f9c-221">smartScreenEnableInShell</span><span class="sxs-lookup"><span data-stu-id="d4f9c-221">smartScreenEnableInShell</span></span>|<span data-ttu-id="d4f9c-222">Booleano</span><span class="sxs-lookup"><span data-stu-id="d4f9c-222">Boolean</span></span>|<span data-ttu-id="d4f9c-223">Permite que los administradores de TI configuren SmartScreen para Windows.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-223">Allows IT Admins to configure SmartScreen for Windows.</span></span>|
|<span data-ttu-id="d4f9c-224">smartScreenBlockOverrideForFiles</span><span class="sxs-lookup"><span data-stu-id="d4f9c-224">smartScreenBlockOverrideForFiles</span></span>|<span data-ttu-id="d4f9c-225">Boolean</span><span class="sxs-lookup"><span data-stu-id="d4f9c-225">Boolean</span></span>|<span data-ttu-id="d4f9c-226">Permite que los administradores de TI controlen si los usuarios pueden omitir advertencias de SmartScreen y ejecutar archivos malintencionados.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-226">Allows IT Admins to control whether users can can ignore SmartScreen warnings and run malicious files.</span></span>|
|<span data-ttu-id="d4f9c-227">applicationGuardEnabled</span><span class="sxs-lookup"><span data-stu-id="d4f9c-227">applicationGuardEnabled</span></span>|<span data-ttu-id="d4f9c-228">Boolean</span><span class="sxs-lookup"><span data-stu-id="d4f9c-228">Boolean</span></span>|<span data-ttu-id="d4f9c-229">Habilita la Protección de aplicaciones de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-229">Enable Windows Defender Application Guard</span></span>|
|<span data-ttu-id="d4f9c-230">applicationGuardBlockFileTransfer</span><span class="sxs-lookup"><span data-stu-id="d4f9c-230">applicationGuardBlockFileTransfer</span></span>|[<span data-ttu-id="d4f9c-231">applicationGuardBlockFileTransferType</span><span class="sxs-lookup"><span data-stu-id="d4f9c-231">applicationGuardBlockFileTransferType</span></span>](../resources/intune-deviceconfig-applicationguardblockfiletransfertype.md)|<span data-ttu-id="d4f9c-232">Portapapeles de bloqueo para el archivo de transferencia de imagen, archivo de texto o ninguno de ellos.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-232">Block clipboard to transfer image file, text file or neither of them.</span></span> <span data-ttu-id="d4f9c-233">Los valores posibles son: `notConfigured`, `blockImageAndTextFile`, `blockImageFile`, `blockNone` y `blockTextFile`.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-233">Possible values are: `notConfigured`, `blockImageAndTextFile`, `blockImageFile`, `blockNone`, `blockTextFile`.</span></span>|
|<span data-ttu-id="d4f9c-234">applicationGuardBlockNonEnterpriseContent</span><span class="sxs-lookup"><span data-stu-id="d4f9c-234">applicationGuardBlockNonEnterpriseContent</span></span>|<span data-ttu-id="d4f9c-235">Boolean</span><span class="sxs-lookup"><span data-stu-id="d4f9c-235">Boolean</span></span>|<span data-ttu-id="d4f9c-236">Impide que los sitios de la empresa carguen contenido no empresarial, como complementos de terceros.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-236">Block enterprise sites to load non-enterprise content, such as third party plug-ins</span></span>|
|<span data-ttu-id="d4f9c-237">applicationGuardAllowPersistence</span><span class="sxs-lookup"><span data-stu-id="d4f9c-237">applicationGuardAllowPersistence</span></span>|<span data-ttu-id="d4f9c-238">Booleano</span><span class="sxs-lookup"><span data-stu-id="d4f9c-238">Boolean</span></span>|<span data-ttu-id="d4f9c-239">Permite el almacenamiento de los datos generados por el usuario en el contenedor de la protección de aplicaciones (favoritos, cookies, contraseñas web, etc.).</span><span class="sxs-lookup"><span data-stu-id="d4f9c-239">Allow persisting user generated data inside the App Guard Containter (favorites, cookies, web passwords, etc.)</span></span>|
|<span data-ttu-id="d4f9c-240">applicationGuardForceAuditing</span><span class="sxs-lookup"><span data-stu-id="d4f9c-240">applicationGuardForceAuditing</span></span>|<span data-ttu-id="d4f9c-241">Boolean</span><span class="sxs-lookup"><span data-stu-id="d4f9c-241">Boolean</span></span>|<span data-ttu-id="d4f9c-242">La auditoría forzada conservará los registros y eventos de Windows para cumplir con los criterios de seguridad y cumplimiento (algunos eventos de ejemplo son el inicio y cierre de sesión del usuario, el uso de derechos de privilegio, la instalación de software, los cambios del sistema, etc.).</span><span class="sxs-lookup"><span data-stu-id="d4f9c-242">Force auditing will persist Windows logs and events to meet security/compliance criteria (sample events are user login-logoff, use of privilege rights, software installation, system changes, etc.)</span></span>|
|<span data-ttu-id="d4f9c-243">applicationGuardBlockClipboardSharing</span><span class="sxs-lookup"><span data-stu-id="d4f9c-243">applicationGuardBlockClipboardSharing</span></span>|[<span data-ttu-id="d4f9c-244">applicationGuardBlockClipboardSharingType</span><span class="sxs-lookup"><span data-stu-id="d4f9c-244">applicationGuardBlockClipboardSharingType</span></span>](../resources/intune-deviceconfig-applicationguardblockclipboardsharingtype.md)|<span data-ttu-id="d4f9c-245">Impide que el Portapapeles comparta los datos del host al contenedor, del contenedor al host, en ambas direcciones o en ninguna.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-245">Block clipboard to share data from Host to Container, or from Container to Host, or both ways, or neither ways.</span></span> <span data-ttu-id="d4f9c-246">Los valores posibles son: `notConfigured`, `blockBoth`, `blockHostToContainer`, `blockContainerToHost` y `blockNone`.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-246">Possible values are: `notConfigured`, `blockBoth`, `blockHostToContainer`, `blockContainerToHost`, `blockNone`.</span></span>|
|<span data-ttu-id="d4f9c-247">applicationGuardAllowPrintToPDF</span><span class="sxs-lookup"><span data-stu-id="d4f9c-247">applicationGuardAllowPrintToPDF</span></span>|<span data-ttu-id="d4f9c-248">Boolean</span><span class="sxs-lookup"><span data-stu-id="d4f9c-248">Boolean</span></span>|<span data-ttu-id="d4f9c-249">Permite la impresión en PDF desde el contenedor.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-249">Allow printing to PDF from Container</span></span>|
|<span data-ttu-id="d4f9c-250">applicationGuardAllowPrintToXPS</span><span class="sxs-lookup"><span data-stu-id="d4f9c-250">applicationGuardAllowPrintToXPS</span></span>|<span data-ttu-id="d4f9c-251">Boolean</span><span class="sxs-lookup"><span data-stu-id="d4f9c-251">Boolean</span></span>|<span data-ttu-id="d4f9c-252">Permite la impresión en XPS desde el contenedor.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-252">Allow printing to XPS from Container</span></span>|
|<span data-ttu-id="d4f9c-253">applicationGuardAllowPrintToLocalPrinters</span><span class="sxs-lookup"><span data-stu-id="d4f9c-253">applicationGuardAllowPrintToLocalPrinters</span></span>|<span data-ttu-id="d4f9c-254">Booleano</span><span class="sxs-lookup"><span data-stu-id="d4f9c-254">Boolean</span></span>|<span data-ttu-id="d4f9c-255">Permite la impresión en impresoras locales desde el contenedor.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-255">Allow printing to Local Printers from Container</span></span>|
|<span data-ttu-id="d4f9c-256">applicationGuardAllowPrintToNetworkPrinters</span><span class="sxs-lookup"><span data-stu-id="d4f9c-256">applicationGuardAllowPrintToNetworkPrinters</span></span>|<span data-ttu-id="d4f9c-257">Boolean</span><span class="sxs-lookup"><span data-stu-id="d4f9c-257">Boolean</span></span>|<span data-ttu-id="d4f9c-258">Permite la impresión en impresoras en red desde el contenedor.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-258">Allow printing to Network Printers from Container</span></span>|
|<span data-ttu-id="d4f9c-259">bitLockerDisableWarningForOtherDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="d4f9c-259">bitLockerDisableWarningForOtherDiskEncryption</span></span>|<span data-ttu-id="d4f9c-260">Booleano</span><span class="sxs-lookup"><span data-stu-id="d4f9c-260">Boolean</span></span>|<span data-ttu-id="d4f9c-261">Permite que el administrador deshabilite el mensaje de advertencia para otro cifrado de disco en los equipos de usuario.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-261">Allows the Admin to disable the warning prompt for other disk encryption on the user machines.</span></span>|
|<span data-ttu-id="d4f9c-262">bitLockerEnableStorageCardEncryptionOnMobile</span><span class="sxs-lookup"><span data-stu-id="d4f9c-262">bitLockerEnableStorageCardEncryptionOnMobile</span></span>|<span data-ttu-id="d4f9c-263">Boolean</span><span class="sxs-lookup"><span data-stu-id="d4f9c-263">Boolean</span></span>|<span data-ttu-id="d4f9c-264">Permite que el administrador exija que se active el cifrado con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-264">Allows the admin to require encryption to be turned on using BitLocker.</span></span> <span data-ttu-id="d4f9c-265">Esta directiva solo es válida para una SKU móvil.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-265">This policy is valid only for a mobile SKU.</span></span>|
|<span data-ttu-id="d4f9c-266">bitLockerEncryptDevice</span><span class="sxs-lookup"><span data-stu-id="d4f9c-266">bitLockerEncryptDevice</span></span>|<span data-ttu-id="d4f9c-267">Booleano</span><span class="sxs-lookup"><span data-stu-id="d4f9c-267">Boolean</span></span>|<span data-ttu-id="d4f9c-268">Permite que el administrador exija que se active el cifrado con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-268">Allows the admin to require encryption to be turned on using BitLocker.</span></span>|
|<span data-ttu-id="d4f9c-269">bitLockerRemovableDrivePolicy</span><span class="sxs-lookup"><span data-stu-id="d4f9c-269">bitLockerRemovableDrivePolicy</span></span>|[<span data-ttu-id="d4f9c-270">bitLockerRemovableDrivePolicy</span><span class="sxs-lookup"><span data-stu-id="d4f9c-270">bitLockerRemovableDrivePolicy</span></span>](../resources/intune-deviceconfig-bitlockerremovabledrivepolicy.md)|<span data-ttu-id="d4f9c-271">Directiva de unidad extraíble de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-271">BitLocker Removable Drive Policy.</span></span>|



## <a name="response"></a><span data-ttu-id="d4f9c-272">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d4f9c-272">Response</span></span>
<span data-ttu-id="d4f9c-273">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-273">If successful, this method returns a `200 OK` response code and an updated [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d4f9c-274">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d4f9c-274">Example</span></span>
### <a name="request"></a><span data-ttu-id="d4f9c-275">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d4f9c-275">Request</span></span>
<span data-ttu-id="d4f9c-276">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-276">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="d4f9c-277">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d4f9c-277">Response</span></span>
<span data-ttu-id="d4f9c-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d4f9c-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



