---
title: Actualizar iosEnterpriseWiFiConfiguration
description: Actualizar las propiedades de un objeto iosEnterpriseWiFiConfiguration.
ms.openlocfilehash: b49c80bffe7de912c6f79b7b238fd84cbc6c6292
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087251"
---
# <a name="update-iosenterprisewificonfiguration"></a><span data-ttu-id="f062e-103">Actualizar iosEnterpriseWiFiConfiguration</span><span class="sxs-lookup"><span data-stu-id="f062e-103">Update iosEnterpriseWiFiConfiguration</span></span>

> <span data-ttu-id="f062e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f062e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f062e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f062e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f062e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f062e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f062e-107">Actualizar las propiedades de un objeto [iosEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-iosenterprisewificonfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="f062e-107">Update the properties of a [iosEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-iosenterprisewificonfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f062e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f062e-108">Prerequisites</span></span>
<span data-ttu-id="f062e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f062e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f062e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f062e-111">Permission type</span></span>|<span data-ttu-id="f062e-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f062e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f062e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f062e-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f062e-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f062e-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="f062e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f062e-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f062e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f062e-116">Not supported.</span></span>|
|<span data-ttu-id="f062e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f062e-117">Application</span></span>|<span data-ttu-id="f062e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f062e-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f062e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f062e-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="f062e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f062e-120">Request headers</span></span>
|<span data-ttu-id="f062e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f062e-121">Header</span></span>|<span data-ttu-id="f062e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f062e-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f062e-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="f062e-123">Authorization</span></span>|<span data-ttu-id="f062e-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f062e-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f062e-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f062e-125">Accept</span></span>|<span data-ttu-id="f062e-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f062e-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f062e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f062e-127">Request body</span></span>
<span data-ttu-id="f062e-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [iosEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-iosenterprisewificonfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="f062e-128">In the request body, supply a JSON representation for the [iosEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-iosenterprisewificonfiguration.md) object.</span></span>

<span data-ttu-id="f062e-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [iosEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-iosenterprisewificonfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="f062e-129">The following table shows the properties that are required when you create the [iosEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-iosenterprisewificonfiguration.md).</span></span>

|<span data-ttu-id="f062e-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f062e-130">Property</span></span>|<span data-ttu-id="f062e-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="f062e-131">Type</span></span>|<span data-ttu-id="f062e-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="f062e-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f062e-133">id</span><span class="sxs-lookup"><span data-stu-id="f062e-133">id</span></span>|<span data-ttu-id="f062e-134">String</span><span class="sxs-lookup"><span data-stu-id="f062e-134">String</span></span>|<span data-ttu-id="f062e-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f062e-135">Key of the entity.</span></span> <span data-ttu-id="f062e-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f062e-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f062e-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="f062e-137">lastModifiedDateTime</span></span>|<span data-ttu-id="f062e-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f062e-138">DateTimeOffset</span></span>|<span data-ttu-id="f062e-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="f062e-139">DateTime the object was last modified.</span></span> <span data-ttu-id="f062e-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f062e-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f062e-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="f062e-141">roleScopeTagIds</span></span>|<span data-ttu-id="f062e-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="f062e-142">String collection</span></span>|<span data-ttu-id="f062e-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="f062e-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="f062e-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f062e-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f062e-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="f062e-145">supportsScopeTags</span></span>|<span data-ttu-id="f062e-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="f062e-146">Boolean</span></span>|<span data-ttu-id="f062e-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="f062e-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="f062e-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="f062e-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="f062e-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="f062e-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="f062e-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f062e-150">This property is read-only.</span></span> <span data-ttu-id="f062e-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f062e-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f062e-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="f062e-152">createdDateTime</span></span>|<span data-ttu-id="f062e-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f062e-153">DateTimeOffset</span></span>|<span data-ttu-id="f062e-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="f062e-154">DateTime the object was created.</span></span> <span data-ttu-id="f062e-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f062e-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f062e-156">descripción</span><span class="sxs-lookup"><span data-stu-id="f062e-156">description</span></span>|<span data-ttu-id="f062e-157">String</span><span class="sxs-lookup"><span data-stu-id="f062e-157">String</span></span>|<span data-ttu-id="f062e-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f062e-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="f062e-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f062e-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f062e-160">displayName</span><span class="sxs-lookup"><span data-stu-id="f062e-160">displayName</span></span>|<span data-ttu-id="f062e-161">String</span><span class="sxs-lookup"><span data-stu-id="f062e-161">String</span></span>|<span data-ttu-id="f062e-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f062e-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="f062e-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f062e-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f062e-164">version</span><span class="sxs-lookup"><span data-stu-id="f062e-164">version</span></span>|<span data-ttu-id="f062e-165">Int32</span><span class="sxs-lookup"><span data-stu-id="f062e-165">Int32</span></span>|<span data-ttu-id="f062e-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f062e-166">Version of the device configuration.</span></span> <span data-ttu-id="f062e-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f062e-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f062e-168">networkName</span><span class="sxs-lookup"><span data-stu-id="f062e-168">networkName</span></span>|<span data-ttu-id="f062e-169">String</span><span class="sxs-lookup"><span data-stu-id="f062e-169">String</span></span>|<span data-ttu-id="f062e-170">Nombre de red se hereda de [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f062e-170">Network Name Inherited from [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span></span>|
|<span data-ttu-id="f062e-171">SSID</span><span class="sxs-lookup"><span data-stu-id="f062e-171">ssid</span></span>|<span data-ttu-id="f062e-172">String</span><span class="sxs-lookup"><span data-stu-id="f062e-172">String</span></span>|<span data-ttu-id="f062e-173">Esto es el nombre de la red Wi-Fi que se difunde a todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="f062e-173">This is the name of the Wi-Fi network that is broadcast to all devices.</span></span> <span data-ttu-id="f062e-174">Se hereda de [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f062e-174">Inherited from [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span></span>|
|<span data-ttu-id="f062e-175">connectAutomatically</span><span class="sxs-lookup"><span data-stu-id="f062e-175">connectAutomatically</span></span>|<span data-ttu-id="f062e-176">Booleano</span><span class="sxs-lookup"><span data-stu-id="f062e-176">Boolean</span></span>|<span data-ttu-id="f062e-177">Conectar automáticamente cuando esta red esté en el intervalo.</span><span class="sxs-lookup"><span data-stu-id="f062e-177">Connect automatically when this network is in range.</span></span> <span data-ttu-id="f062e-178">Si se establece en true omitirá el símbolo del sistema del usuario y el dispositivo se conecte automáticamente a la red Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="f062e-178">Setting this to true will skip the user prompt and automatically connect the device to Wi-Fi network.</span></span> <span data-ttu-id="f062e-179">Se hereda de [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f062e-179">Inherited from [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span></span>|
|<span data-ttu-id="f062e-180">connectWhenNetworkNameIsHidden</span><span class="sxs-lookup"><span data-stu-id="f062e-180">connectWhenNetworkNameIsHidden</span></span>|<span data-ttu-id="f062e-181">Booleano</span><span class="sxs-lookup"><span data-stu-id="f062e-181">Boolean</span></span>|<span data-ttu-id="f062e-182">Conectar cuando la red no sea de difusión su nombre (SSID).</span><span class="sxs-lookup"><span data-stu-id="f062e-182">Connect when the network is not broadcasting its name (SSID).</span></span> <span data-ttu-id="f062e-183">Cuando se establece en true, este perfil fuerza el dispositivo para conectarse a una red que no difundir su SSID para todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="f062e-183">When set to true, this profile forces the device to connect to a network that doesn't broadcast its SSID to all devices.</span></span> <span data-ttu-id="f062e-184">Se hereda de [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f062e-184">Inherited from [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span></span>|
|<span data-ttu-id="f062e-185">wiFiSecurityType</span><span class="sxs-lookup"><span data-stu-id="f062e-185">wiFiSecurityType</span></span>|[<span data-ttu-id="f062e-186">wiFiSecurityType</span><span class="sxs-lookup"><span data-stu-id="f062e-186">wiFiSecurityType</span></span>](../resources/intune-deviceconfig-wifisecuritytype.md)|<span data-ttu-id="f062e-187">Indica si el extremo de Wi-Fi utiliza un tipo de EAP en función de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f062e-187">Indicates whether Wi-Fi endpoint uses an EAP based security type.</span></span> <span data-ttu-id="f062e-188">Se hereda de [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="f062e-188">Inherited from [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md).</span></span> <span data-ttu-id="f062e-189">Los valores posibles son: `open`, `wpaPersonal`, `wpaEnterprise`, `wep`, `wpa2Personal`, `wpa2Enterprise`.</span><span class="sxs-lookup"><span data-stu-id="f062e-189">Possible values are: `open`, `wpaPersonal`, `wpaEnterprise`, `wep`, `wpa2Personal`, `wpa2Enterprise`.</span></span>|
|<span data-ttu-id="f062e-190">proxySettings</span><span class="sxs-lookup"><span data-stu-id="f062e-190">proxySettings</span></span>|[<span data-ttu-id="f062e-191">wiFiProxySetting</span><span class="sxs-lookup"><span data-stu-id="f062e-191">wiFiProxySetting</span></span>](../resources/intune-deviceconfig-wifiproxysetting.md)|<span data-ttu-id="f062e-192">Tipo de proxy para esta conexión Wi-Fi Inherited desde [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="f062e-192">Proxy Type for this Wi-Fi connection Inherited from [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md).</span></span> <span data-ttu-id="f062e-193">Los valores posibles son: `none`, `manual` y `automatic`.</span><span class="sxs-lookup"><span data-stu-id="f062e-193">Possible values are: `none`, `manual`, `automatic`.</span></span>|
|<span data-ttu-id="f062e-194">proxyManualAddress</span><span class="sxs-lookup"><span data-stu-id="f062e-194">proxyManualAddress</span></span>|<span data-ttu-id="f062e-195">String</span><span class="sxs-lookup"><span data-stu-id="f062e-195">String</span></span>|<span data-ttu-id="f062e-196">Nombre de host DNS o dirección IP del servidor proxy cuando se selecciona la configuración manual.</span><span class="sxs-lookup"><span data-stu-id="f062e-196">IP Address or DNS hostname of the proxy server when manual configuration is selected.</span></span> <span data-ttu-id="f062e-197">Se hereda de [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f062e-197">Inherited from [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span></span>|
|<span data-ttu-id="f062e-198">proxyManualPort</span><span class="sxs-lookup"><span data-stu-id="f062e-198">proxyManualPort</span></span>|<span data-ttu-id="f062e-199">Int32</span><span class="sxs-lookup"><span data-stu-id="f062e-199">Int32</span></span>|<span data-ttu-id="f062e-200">Puerto del servidor proxy cuando se selecciona la configuración manual.</span><span class="sxs-lookup"><span data-stu-id="f062e-200">Port of the proxy server when manual configuration is selected.</span></span> <span data-ttu-id="f062e-201">Se hereda de [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f062e-201">Inherited from [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span></span>|
|<span data-ttu-id="f062e-202">proxyAutomaticConfigurationUrl</span><span class="sxs-lookup"><span data-stu-id="f062e-202">proxyAutomaticConfigurationUrl</span></span>|<span data-ttu-id="f062e-203">String</span><span class="sxs-lookup"><span data-stu-id="f062e-203">String</span></span>|<span data-ttu-id="f062e-204">URL de la secuencia de la configuración automática de servidor proxy cuando se selecciona la configuración automática.</span><span class="sxs-lookup"><span data-stu-id="f062e-204">URL of the proxy server automatic configuration script when automatic configuration is selected.</span></span> <span data-ttu-id="f062e-205">Normalmente, esta dirección URL es la ubicación del archivo PAC (configuración automática de Proxy).</span><span class="sxs-lookup"><span data-stu-id="f062e-205">This URL is typically the location of PAC (Proxy Auto Configuration) file.</span></span> <span data-ttu-id="f062e-206">Se hereda de [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f062e-206">Inherited from [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span></span>|
|<span data-ttu-id="f062e-207">preSharedKey</span><span class="sxs-lookup"><span data-stu-id="f062e-207">preSharedKey</span></span>|<span data-ttu-id="f062e-208">String</span><span class="sxs-lookup"><span data-stu-id="f062e-208">String</span></span>|<span data-ttu-id="f062e-209">Ésta es la clave previamente compartida para la red Wi-Fi Personal WPA.</span><span class="sxs-lookup"><span data-stu-id="f062e-209">This is the pre-shared key for WPA Personal Wi-Fi network.</span></span> <span data-ttu-id="f062e-210">Se hereda de [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f062e-210">Inherited from [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md)</span></span>|
|<span data-ttu-id="f062e-211">eapType</span><span class="sxs-lookup"><span data-stu-id="f062e-211">eapType</span></span>|[<span data-ttu-id="f062e-212">eapType</span><span class="sxs-lookup"><span data-stu-id="f062e-212">eapType</span></span>](../resources/intune-deviceconfig-eaptype.md)|<span data-ttu-id="f062e-213">Protocolo de autenticación extensible (EAP).</span><span class="sxs-lookup"><span data-stu-id="f062e-213">Extensible Authentication Protocol (EAP).</span></span> <span data-ttu-id="f062e-214">Indica el tipo de protocolo EAP establecido en el extremo de Wi-Fi (enrutador).</span><span class="sxs-lookup"><span data-stu-id="f062e-214">Indicates the type of EAP protocol set on the the Wi-Fi endpoint (router).</span></span> <span data-ttu-id="f062e-215">Los valores posibles son: `eapTls`, `leap`, `eapSim`, `eapTtls`, `peap`, `eapFast`.</span><span class="sxs-lookup"><span data-stu-id="f062e-215">Possible values are: `eapTls`, `leap`, `eapSim`, `eapTtls`, `peap`, `eapFast`.</span></span>|
|<span data-ttu-id="f062e-216">eapFastConfiguration</span><span class="sxs-lookup"><span data-stu-id="f062e-216">eapFastConfiguration</span></span>|[<span data-ttu-id="f062e-217">eapFastConfiguration</span><span class="sxs-lookup"><span data-stu-id="f062e-217">eapFastConfiguration</span></span>](../resources/intune-deviceconfig-eapfastconfiguration.md)|<span data-ttu-id="f062e-218">Opción de configuración de EAP-FAST cuando EAP-FAST es el tipo de EAP seleccionado.</span><span class="sxs-lookup"><span data-stu-id="f062e-218">EAP-FAST Configuration Option when EAP-FAST is the selected EAP Type.</span></span> <span data-ttu-id="f062e-219">Los valores posibles son: `noProtectedAccessCredential`, `useProtectedAccessCredential`, `useProtectedAccessCredentialAndProvision` y `useProtectedAccessCredentialAndProvisionAnonymously`.</span><span class="sxs-lookup"><span data-stu-id="f062e-219">Possible values are: `noProtectedAccessCredential`, `useProtectedAccessCredential`, `useProtectedAccessCredentialAndProvision`, `useProtectedAccessCredentialAndProvisionAnonymously`.</span></span>|
|<span data-ttu-id="f062e-220">trustedServerCertificateNames</span><span class="sxs-lookup"><span data-stu-id="f062e-220">trustedServerCertificateNames</span></span>|<span data-ttu-id="f062e-221">Colección String</span><span class="sxs-lookup"><span data-stu-id="f062e-221">String collection</span></span>|<span data-ttu-id="f062e-222">Los nombres de certificado de servidor de confianza cuando se configura el tipo de EAP a FAST/EAP-TLS o TTLS o PEAP.</span><span class="sxs-lookup"><span data-stu-id="f062e-222">Trusted server certificate names when EAP Type is configured to EAP-TLS/TTLS/FAST or PEAP.</span></span> <span data-ttu-id="f062e-223">Esto es el nombre común que se usa en los certificados emitidos por su entidad emisora de certificados de confianza (CA).</span><span class="sxs-lookup"><span data-stu-id="f062e-223">This is the common name used in the certificates issued by your trusted certificate authority (CA).</span></span> <span data-ttu-id="f062e-224">Si proporciona esta información, puede omitir el cuadro de diálogo de confianza dinámica que se muestra en los dispositivos de los usuarios finales cuando se conectan a esta red Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="f062e-224">If you provide this information, you can bypass the dynamic trust dialog that is displayed on end users' devices when they connect to this Wi-Fi network.</span></span>|
|<span data-ttu-id="f062e-225">authenticationMethod</span><span class="sxs-lookup"><span data-stu-id="f062e-225">authenticationMethod</span></span>|[<span data-ttu-id="f062e-226">wiFiAuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="f062e-226">wiFiAuthenticationMethod</span></span>](../resources/intune-deviceconfig-wifiauthenticationmethod.md)|<span data-ttu-id="f062e-227">Método de autenticación cuando se configura el tipo de EAP PEAP o EAP-TTLS.</span><span class="sxs-lookup"><span data-stu-id="f062e-227">Authentication Method when EAP Type is configured to PEAP or EAP-TTLS.</span></span> <span data-ttu-id="f062e-228">Los valores posibles son: `certificate` y `usernameAndPassword`.</span><span class="sxs-lookup"><span data-stu-id="f062e-228">Possible values are: `certificate`, `usernameAndPassword`.</span></span>|
|<span data-ttu-id="f062e-229">innerAuthenticationProtocolForEapTtls</span><span class="sxs-lookup"><span data-stu-id="f062e-229">innerAuthenticationProtocolForEapTtls</span></span>|[<span data-ttu-id="f062e-230">nonEapAuthenticationMethodForEapTtlsType</span><span class="sxs-lookup"><span data-stu-id="f062e-230">nonEapAuthenticationMethodForEapTtlsType</span></span>](../resources/intune-deviceconfig-noneapauthenticationmethodforeapttlstype.md)|<span data-ttu-id="f062e-231">Método no EAP para la autenticación cuando el tipo de EAP es EAP-TTLS y Authenticationmethod es el nombre de usuario y contraseña.</span><span class="sxs-lookup"><span data-stu-id="f062e-231">Non-EAP Method for Authentication when EAP Type is EAP-TTLS and Authenticationmethod is Username and Password.</span></span> <span data-ttu-id="f062e-232">Los valores posibles son: `unencryptedPassword`, `challengeHandshakeAuthenticationProtocol`, `microsoftChap` y `microsoftChapVersionTwo`.</span><span class="sxs-lookup"><span data-stu-id="f062e-232">Possible values are: `unencryptedPassword`, `challengeHandshakeAuthenticationProtocol`, `microsoftChap`, `microsoftChapVersionTwo`.</span></span>|
|<span data-ttu-id="f062e-233">outerIdentityPrivacyTemporaryValue</span><span class="sxs-lookup"><span data-stu-id="f062e-233">outerIdentityPrivacyTemporaryValue</span></span>|<span data-ttu-id="f062e-234">String</span><span class="sxs-lookup"><span data-stu-id="f062e-234">String</span></span>|<span data-ttu-id="f062e-235">Habilitar privacidad de identidad (identidad externa) cuando se configura el tipo de EAP a EAP - TTLS, EAP - FAST o PEAP.</span><span class="sxs-lookup"><span data-stu-id="f062e-235">Enable identity privacy (Outer Identity) when EAP Type is configured to EAP - TTLS, EAP - FAST or PEAP.</span></span> <span data-ttu-id="f062e-236">Esta propiedad enmascara los nombres de usuario con el texto que escriba.</span><span class="sxs-lookup"><span data-stu-id="f062e-236">This property masks usernames with the text you enter.</span></span> <span data-ttu-id="f062e-237">Por ejemplo, si usa 'anonymous', cada usuario que se autentica con esta conexión Wi-Fi con su nombre de usuario real se muestra como 'anonymous'.</span><span class="sxs-lookup"><span data-stu-id="f062e-237">For example, if you use 'anonymous', each user that authenticates with this Wi-Fi connection using their real username is displayed as 'anonymous'.</span></span>|



## <a name="response"></a><span data-ttu-id="f062e-238">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f062e-238">Response</span></span>
<span data-ttu-id="f062e-239">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [iosEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-iosenterprisewificonfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f062e-239">If successful, this method returns a `200 OK` response code and an updated [iosEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-iosenterprisewificonfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f062e-240">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f062e-240">Example</span></span>
### <a name="request"></a><span data-ttu-id="f062e-241">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f062e-241">Request</span></span>
<span data-ttu-id="f062e-242">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f062e-242">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 1078

{
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

### <a name="response"></a><span data-ttu-id="f062e-243">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f062e-243">Response</span></span>
<span data-ttu-id="f062e-p126">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f062e-p126">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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




