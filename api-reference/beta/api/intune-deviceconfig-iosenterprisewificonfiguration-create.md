---
title: Crear iosEnterpriseWiFiConfiguration
description: Crear un nuevo objeto iosEnterpriseWiFiConfiguration.
ms.openlocfilehash: 88b9258f7d2939884f11e29cfd139d03016f0b15
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089053"
---
# <a name="create-iosenterprisewificonfiguration"></a><span data-ttu-id="7f6b8-103">Crear iosEnterpriseWiFiConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f6b8-103">Create iosEnterpriseWiFiConfiguration</span></span>

> <span data-ttu-id="7f6b8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7f6b8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7f6b8-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7f6b8-107">Crear un nuevo objeto [iosEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-iosenterprisewificonfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="7f6b8-107">Create a new [iosEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-iosenterprisewificonfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7f6b8-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7f6b8-108">Prerequisites</span></span>
<span data-ttu-id="7f6b8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7f6b8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7f6b8-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7f6b8-111">Permission type</span></span>|<span data-ttu-id="7f6b8-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7f6b8-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7f6b8-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7f6b8-113">Delegated (work or school account)</span></span>|<span data-ttu-id="7f6b8-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7f6b8-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="7f6b8-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7f6b8-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7f6b8-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-116">Not supported.</span></span>|
|<span data-ttu-id="7f6b8-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7f6b8-117">Application</span></span>|<span data-ttu-id="7f6b8-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7f6b8-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7f6b8-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="7f6b8-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7f6b8-120">Request headers</span></span>
|<span data-ttu-id="7f6b8-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7f6b8-121">Header</span></span>|<span data-ttu-id="7f6b8-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7f6b8-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7f6b8-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="7f6b8-123">Authorization</span></span>|<span data-ttu-id="7f6b8-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7f6b8-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="7f6b8-125">Accept</span></span>|<span data-ttu-id="7f6b8-126">application/json</span><span class="sxs-lookup"><span data-stu-id="7f6b8-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7f6b8-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7f6b8-127">Request body</span></span>
<span data-ttu-id="7f6b8-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto iosEnterpriseWiFiConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-128">In the request body, supply a JSON representation for the iosEnterpriseWiFiConfiguration object.</span></span>

<span data-ttu-id="7f6b8-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el iosEnterpriseWiFiConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-129">The following table shows the properties that are required when you create the iosEnterpriseWiFiConfiguration.</span></span>

|<span data-ttu-id="7f6b8-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7f6b8-130">Property</span></span>|<span data-ttu-id="7f6b8-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="7f6b8-131">Type</span></span>|<span data-ttu-id="7f6b8-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="7f6b8-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7f6b8-133">id</span><span class="sxs-lookup"><span data-stu-id="7f6b8-133">id</span></span>|<span data-ttu-id="7f6b8-134">String</span><span class="sxs-lookup"><span data-stu-id="7f6b8-134">String</span></span>|<span data-ttu-id="7f6b8-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-135">Key of the entity.</span></span> <span data-ttu-id="7f6b8-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7f6b8-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7f6b8-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="7f6b8-137">lastModifiedDateTime</span></span>|<span data-ttu-id="7f6b8-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7f6b8-138">DateTimeOffset</span></span>|<span data-ttu-id="7f6b8-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-139">DateTime the object was last modified.</span></span> <span data-ttu-id="7f6b8-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7f6b8-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7f6b8-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="7f6b8-141">roleScopeTagIds</span></span>|<span data-ttu-id="7f6b8-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="7f6b8-142">String collection</span></span>|<span data-ttu-id="7f6b8-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="7f6b8-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7f6b8-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7f6b8-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="7f6b8-145">supportsScopeTags</span></span>|<span data-ttu-id="7f6b8-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="7f6b8-146">Boolean</span></span>|<span data-ttu-id="7f6b8-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="7f6b8-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="7f6b8-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="7f6b8-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-150">This property is read-only.</span></span> <span data-ttu-id="7f6b8-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7f6b8-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7f6b8-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="7f6b8-152">createdDateTime</span></span>|<span data-ttu-id="7f6b8-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7f6b8-153">DateTimeOffset</span></span>|<span data-ttu-id="7f6b8-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-154">DateTime the object was created.</span></span> <span data-ttu-id="7f6b8-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7f6b8-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7f6b8-156">descripción</span><span class="sxs-lookup"><span data-stu-id="7f6b8-156">description</span></span>|<span data-ttu-id="7f6b8-157">String</span><span class="sxs-lookup"><span data-stu-id="7f6b8-157">String</span></span>|<span data-ttu-id="7f6b8-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="7f6b8-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7f6b8-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7f6b8-160">displayName</span><span class="sxs-lookup"><span data-stu-id="7f6b8-160">displayName</span></span>|<span data-ttu-id="7f6b8-161">String</span><span class="sxs-lookup"><span data-stu-id="7f6b8-161">String</span></span>|<span data-ttu-id="7f6b8-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="7f6b8-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7f6b8-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7f6b8-164">version</span><span class="sxs-lookup"><span data-stu-id="7f6b8-164">version</span></span>|<span data-ttu-id="7f6b8-165">Int32</span><span class="sxs-lookup"><span data-stu-id="7f6b8-165">Int32</span></span>|<span data-ttu-id="7f6b8-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-166">Version of the device configuration.</span></span> <span data-ttu-id="7f6b8-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7f6b8-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7f6b8-168">networkName</span><span class="sxs-lookup"><span data-stu-id="7f6b8-168">networkName</span></span>|<span data-ttu-id="7f6b8-169">String</span><span class="sxs-lookup"><span data-stu-id="7f6b8-169">String</span></span>|<span data-ttu-id="7f6b8-170">Nombre de red se hereda de [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7f6b8-170">Network Name Inherited from [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span></span>|
|<span data-ttu-id="7f6b8-171">SSID</span><span class="sxs-lookup"><span data-stu-id="7f6b8-171">ssid</span></span>|<span data-ttu-id="7f6b8-172">String</span><span class="sxs-lookup"><span data-stu-id="7f6b8-172">String</span></span>|<span data-ttu-id="7f6b8-173">Esto es el nombre de la red Wi-Fi que se difunde a todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-173">This is the name of the Wi-Fi network that is broadcast to all devices.</span></span> <span data-ttu-id="7f6b8-174">Se hereda de [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7f6b8-174">Inherited from [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span></span>|
|<span data-ttu-id="7f6b8-175">connectAutomatically</span><span class="sxs-lookup"><span data-stu-id="7f6b8-175">connectAutomatically</span></span>|<span data-ttu-id="7f6b8-176">Booleano</span><span class="sxs-lookup"><span data-stu-id="7f6b8-176">Boolean</span></span>|<span data-ttu-id="7f6b8-177">Conectar automáticamente cuando esta red esté en el intervalo.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-177">Connect automatically when this network is in range.</span></span> <span data-ttu-id="7f6b8-178">Si se establece en true omitirá el símbolo del sistema del usuario y el dispositivo se conecte automáticamente a la red Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-178">Setting this to true will skip the user prompt and automatically connect the device to Wi-Fi network.</span></span> <span data-ttu-id="7f6b8-179">Se hereda de [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7f6b8-179">Inherited from [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span></span>|
|<span data-ttu-id="7f6b8-180">connectWhenNetworkNameIsHidden</span><span class="sxs-lookup"><span data-stu-id="7f6b8-180">connectWhenNetworkNameIsHidden</span></span>|<span data-ttu-id="7f6b8-181">Booleano</span><span class="sxs-lookup"><span data-stu-id="7f6b8-181">Boolean</span></span>|<span data-ttu-id="7f6b8-182">Conectar cuando la red no sea de difusión su nombre (SSID).</span><span class="sxs-lookup"><span data-stu-id="7f6b8-182">Connect when the network is not broadcasting its name (SSID).</span></span> <span data-ttu-id="7f6b8-183">Cuando se establece en true, este perfil fuerza el dispositivo para conectarse a una red que no difundir su SSID para todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-183">When set to true, this profile forces the device to connect to a network that doesn't broadcast its SSID to all devices.</span></span> <span data-ttu-id="7f6b8-184">Se hereda de [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7f6b8-184">Inherited from [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span></span>|
|<span data-ttu-id="7f6b8-185">wiFiSecurityType</span><span class="sxs-lookup"><span data-stu-id="7f6b8-185">wiFiSecurityType</span></span>|[<span data-ttu-id="7f6b8-186">wiFiSecurityType</span><span class="sxs-lookup"><span data-stu-id="7f6b8-186">wiFiSecurityType</span></span>](../resources/intune-deviceconfig-wifisecuritytype.md)|<span data-ttu-id="7f6b8-187">Indica si el extremo de Wi-Fi utiliza un tipo de EAP en función de seguridad.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-187">Indicates whether Wi-Fi endpoint uses an EAP based security type.</span></span> <span data-ttu-id="7f6b8-188">Se hereda de [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="7f6b8-188">Inherited from [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md).</span></span> <span data-ttu-id="7f6b8-189">Los valores posibles son: `open`, `wpaPersonal`, `wpaEnterprise`, `wep`, `wpa2Personal`, `wpa2Enterprise`.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-189">Possible values are: `open`, `wpaPersonal`, `wpaEnterprise`, `wep`, `wpa2Personal`, `wpa2Enterprise`.</span></span>|
|<span data-ttu-id="7f6b8-190">proxySettings</span><span class="sxs-lookup"><span data-stu-id="7f6b8-190">proxySettings</span></span>|[<span data-ttu-id="7f6b8-191">wiFiProxySetting</span><span class="sxs-lookup"><span data-stu-id="7f6b8-191">wiFiProxySetting</span></span>](../resources/intune-deviceconfig-wifiproxysetting.md)|<span data-ttu-id="7f6b8-192">Tipo de proxy para esta conexión Wi-Fi Inherited desde [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="7f6b8-192">Proxy Type for this Wi-Fi connection Inherited from [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md).</span></span> <span data-ttu-id="7f6b8-193">Los valores posibles son: `none`, `manual` y `automatic`.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-193">Possible values are: `none`, `manual`, `automatic`.</span></span>|
|<span data-ttu-id="7f6b8-194">proxyManualAddress</span><span class="sxs-lookup"><span data-stu-id="7f6b8-194">proxyManualAddress</span></span>|<span data-ttu-id="7f6b8-195">String</span><span class="sxs-lookup"><span data-stu-id="7f6b8-195">String</span></span>|<span data-ttu-id="7f6b8-196">Nombre de host DNS o dirección IP del servidor proxy cuando se selecciona la configuración manual.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-196">IP Address or DNS hostname of the proxy server when manual configuration is selected.</span></span> <span data-ttu-id="7f6b8-197">Se hereda de [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7f6b8-197">Inherited from [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span></span>|
|<span data-ttu-id="7f6b8-198">proxyManualPort</span><span class="sxs-lookup"><span data-stu-id="7f6b8-198">proxyManualPort</span></span>|<span data-ttu-id="7f6b8-199">Int32</span><span class="sxs-lookup"><span data-stu-id="7f6b8-199">Int32</span></span>|<span data-ttu-id="7f6b8-200">Puerto del servidor proxy cuando se selecciona la configuración manual.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-200">Port of the proxy server when manual configuration is selected.</span></span> <span data-ttu-id="7f6b8-201">Se hereda de [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7f6b8-201">Inherited from [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span></span>|
|<span data-ttu-id="7f6b8-202">proxyAutomaticConfigurationUrl</span><span class="sxs-lookup"><span data-stu-id="7f6b8-202">proxyAutomaticConfigurationUrl</span></span>|<span data-ttu-id="7f6b8-203">String</span><span class="sxs-lookup"><span data-stu-id="7f6b8-203">String</span></span>|<span data-ttu-id="7f6b8-204">URL de la secuencia de la configuración automática de servidor proxy cuando se selecciona la configuración automática.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-204">URL of the proxy server automatic configuration script when automatic configuration is selected.</span></span> <span data-ttu-id="7f6b8-205">Normalmente, esta dirección URL es la ubicación del archivo PAC (configuración automática de Proxy).</span><span class="sxs-lookup"><span data-stu-id="7f6b8-205">This URL is typically the location of PAC (Proxy Auto Configuration) file.</span></span> <span data-ttu-id="7f6b8-206">Se hereda de [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7f6b8-206">Inherited from [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span></span>|
|<span data-ttu-id="7f6b8-207">preSharedKey</span><span class="sxs-lookup"><span data-stu-id="7f6b8-207">preSharedKey</span></span>|<span data-ttu-id="7f6b8-208">String</span><span class="sxs-lookup"><span data-stu-id="7f6b8-208">String</span></span>|<span data-ttu-id="7f6b8-209">Ésta es la clave previamente compartida para la red Wi-Fi Personal WPA.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-209">This is the pre-shared key for WPA Personal Wi-Fi network.</span></span> <span data-ttu-id="7f6b8-210">Se hereda de [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7f6b8-210">Inherited from [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span></span>|
|<span data-ttu-id="7f6b8-211">eapType</span><span class="sxs-lookup"><span data-stu-id="7f6b8-211">eapType</span></span>|[<span data-ttu-id="7f6b8-212">eapType</span><span class="sxs-lookup"><span data-stu-id="7f6b8-212">eapType</span></span>](../resources/intune-deviceconfig-eaptype.md)|<span data-ttu-id="7f6b8-213">Protocolo de autenticación extensible (EAP).</span><span class="sxs-lookup"><span data-stu-id="7f6b8-213">Extensible Authentication Protocol (EAP).</span></span> <span data-ttu-id="7f6b8-214">Indica el tipo de protocolo EAP establecido en el extremo de Wi-Fi (enrutador).</span><span class="sxs-lookup"><span data-stu-id="7f6b8-214">Indicates the type of EAP protocol set on the the Wi-Fi endpoint (router).</span></span> <span data-ttu-id="7f6b8-215">Los valores posibles son: `eapTls`, `leap`, `eapSim`, `eapTtls`, `peap`, `eapFast`.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-215">Possible values are: `eapTls`, `leap`, `eapSim`, `eapTtls`, `peap`, `eapFast`.</span></span>|
|<span data-ttu-id="7f6b8-216">eapFastConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f6b8-216">eapFastConfiguration</span></span>|[<span data-ttu-id="7f6b8-217">eapFastConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f6b8-217">eapFastConfiguration</span></span>](../resources/intune-deviceconfig-eapfastconfiguration.md)|<span data-ttu-id="7f6b8-218">Opción de configuración de EAP-FAST cuando EAP-FAST es el tipo de EAP seleccionado.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-218">EAP-FAST Configuration Option when EAP-FAST is the selected EAP Type.</span></span> <span data-ttu-id="7f6b8-219">Los valores posibles son: `noProtectedAccessCredential`, `useProtectedAccessCredential`, `useProtectedAccessCredentialAndProvision` y `useProtectedAccessCredentialAndProvisionAnonymously`.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-219">Possible values are: `noProtectedAccessCredential`, `useProtectedAccessCredential`, `useProtectedAccessCredentialAndProvision`, `useProtectedAccessCredentialAndProvisionAnonymously`.</span></span>|
|<span data-ttu-id="7f6b8-220">trustedServerCertificateNames</span><span class="sxs-lookup"><span data-stu-id="7f6b8-220">trustedServerCertificateNames</span></span>|<span data-ttu-id="7f6b8-221">Colección String</span><span class="sxs-lookup"><span data-stu-id="7f6b8-221">String collection</span></span>|<span data-ttu-id="7f6b8-222">Los nombres de certificado de servidor de confianza cuando se configura el tipo de EAP a FAST/EAP-TLS o TTLS o PEAP.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-222">Trusted server certificate names when EAP Type is configured to EAP-TLS/TTLS/FAST or PEAP.</span></span> <span data-ttu-id="7f6b8-223">Esto es el nombre común que se usa en los certificados emitidos por su entidad emisora de certificados de confianza (CA).</span><span class="sxs-lookup"><span data-stu-id="7f6b8-223">This is the common name used in the certificates issued by your trusted certificate authority (CA).</span></span> <span data-ttu-id="7f6b8-224">Si proporciona esta información, puede omitir el cuadro de diálogo de confianza dinámica que se muestra en los dispositivos de los usuarios finales cuando se conectan a esta red Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-224">If you provide this information, you can bypass the dynamic trust dialog that is displayed on end users' devices when they connect to this Wi-Fi network.</span></span>|
|<span data-ttu-id="7f6b8-225">authenticationMethod</span><span class="sxs-lookup"><span data-stu-id="7f6b8-225">authenticationMethod</span></span>|[<span data-ttu-id="7f6b8-226">wiFiAuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="7f6b8-226">wiFiAuthenticationMethod</span></span>](../resources/intune-deviceconfig-wifiauthenticationmethod.md)|<span data-ttu-id="7f6b8-227">Método de autenticación cuando se configura el tipo de EAP PEAP o EAP-TTLS.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-227">Authentication Method when EAP Type is configured to PEAP or EAP-TTLS.</span></span> <span data-ttu-id="7f6b8-228">Los valores posibles son: `certificate` y `usernameAndPassword`.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-228">Possible values are: `certificate`, `usernameAndPassword`.</span></span>|
|<span data-ttu-id="7f6b8-229">innerAuthenticationProtocolForEapTtls</span><span class="sxs-lookup"><span data-stu-id="7f6b8-229">innerAuthenticationProtocolForEapTtls</span></span>|[<span data-ttu-id="7f6b8-230">nonEapAuthenticationMethodForEapTtlsType</span><span class="sxs-lookup"><span data-stu-id="7f6b8-230">nonEapAuthenticationMethodForEapTtlsType</span></span>](../resources/intune-deviceconfig-noneapauthenticationmethodforeapttlstype.md)|<span data-ttu-id="7f6b8-231">Método no EAP para la autenticación cuando el tipo de EAP es EAP-TTLS y Authenticationmethod es el nombre de usuario y contraseña.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-231">Non-EAP Method for Authentication when EAP Type is EAP-TTLS and Authenticationmethod is Username and Password.</span></span> <span data-ttu-id="7f6b8-232">Los valores posibles son: `unencryptedPassword`, `challengeHandshakeAuthenticationProtocol`, `microsoftChap` y `microsoftChapVersionTwo`.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-232">Possible values are: `unencryptedPassword`, `challengeHandshakeAuthenticationProtocol`, `microsoftChap`, `microsoftChapVersionTwo`.</span></span>|
|<span data-ttu-id="7f6b8-233">outerIdentityPrivacyTemporaryValue</span><span class="sxs-lookup"><span data-stu-id="7f6b8-233">outerIdentityPrivacyTemporaryValue</span></span>|<span data-ttu-id="7f6b8-234">String</span><span class="sxs-lookup"><span data-stu-id="7f6b8-234">String</span></span>|<span data-ttu-id="7f6b8-235">Habilitar privacidad de identidad (identidad externa) cuando se configura el tipo de EAP a EAP - TTLS, EAP - FAST o PEAP.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-235">Enable identity privacy (Outer Identity) when EAP Type is configured to EAP - TTLS, EAP - FAST or PEAP.</span></span> <span data-ttu-id="7f6b8-236">Esta propiedad enmascara los nombres de usuario con el texto que escriba.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-236">This property masks usernames with the text you enter.</span></span> <span data-ttu-id="7f6b8-237">Por ejemplo, si usa 'anonymous', cada usuario que se autentica con esta conexión Wi-Fi con su nombre de usuario real se muestra como 'anonymous'.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-237">For example, if you use 'anonymous', each user that authenticates with this Wi-Fi connection using their real username is displayed as 'anonymous'.</span></span>|



## <a name="response"></a><span data-ttu-id="7f6b8-238">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7f6b8-238">Response</span></span>
<span data-ttu-id="7f6b8-239">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [iosEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-iosenterprisewificonfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-239">If successful, this method returns a `201 Created` response code and a [iosEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-iosenterprisewificonfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7f6b8-240">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7f6b8-240">Example</span></span>
### <a name="request"></a><span data-ttu-id="7f6b8-241">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7f6b8-241">Request</span></span>
<span data-ttu-id="7f6b8-242">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-242">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 1147

{
  "@odata.type": "#microsoft.graph.iosEnterpriseWiFiConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "networkName": "Network Name value",
  "ssid": "Ssid value",
  "connectAutomatically": true,
  "connectWhenNetworkNameIsHidden": true,
  "wiFiSecurityType": "wpaPersonal",
  "proxySettings": "manual",
  "proxyManualAddress": "Proxy Manual Address value",
  "proxyManualPort": 15,
  "proxyAutomaticConfigurationUrl": "https://example.com/proxyAutomaticConfigurationUrl/",
  "preSharedKey": "Pre Shared Key value",
  "eapType": "leap",
  "eapFastConfiguration": "useProtectedAccessCredential",
  "trustedServerCertificateNames": [
    "Trusted Server Certificate Names value"
  ],
  "authenticationMethod": "usernameAndPassword",
  "innerAuthenticationProtocolForEapTtls": "challengeHandshakeAuthenticationProtocol",
  "outerIdentityPrivacyTemporaryValue": "Outer Identity Privacy Temporary Value value"
}
```

### <a name="response"></a><span data-ttu-id="7f6b8-243">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7f6b8-243">Response</span></span>
<span data-ttu-id="7f6b8-p126">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-p126">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1255

{
  "@odata.type": "#microsoft.graph.iosEnterpriseWiFiConfiguration",
  "id": "7593f7ba-f7ba-7593-baf7-9375baf79375",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "networkName": "Network Name value",
  "ssid": "Ssid value",
  "connectAutomatically": true,
  "connectWhenNetworkNameIsHidden": true,
  "wiFiSecurityType": "wpaPersonal",
  "proxySettings": "manual",
  "proxyManualAddress": "Proxy Manual Address value",
  "proxyManualPort": 15,
  "proxyAutomaticConfigurationUrl": "https://example.com/proxyAutomaticConfigurationUrl/",
  "preSharedKey": "Pre Shared Key value",
  "eapType": "leap",
  "eapFastConfiguration": "useProtectedAccessCredential",
  "trustedServerCertificateNames": [
    "Trusted Server Certificate Names value"
  ],
  "authenticationMethod": "usernameAndPassword",
  "innerAuthenticationProtocolForEapTtls": "challengeHandshakeAuthenticationProtocol",
  "outerIdentityPrivacyTemporaryValue": "Outer Identity Privacy Temporary Value value"
}
```




