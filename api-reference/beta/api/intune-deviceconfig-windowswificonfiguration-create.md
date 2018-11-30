---
title: Crear windowsWifiConfiguration
description: Crear un nuevo objeto windowsWifiConfiguration.
ms.openlocfilehash: b065d86bca4d804f6edeceb193ea5b283859fde7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086784"
---
# <a name="create-windowswificonfiguration"></a><span data-ttu-id="87c8f-103">Crear windowsWifiConfiguration</span><span class="sxs-lookup"><span data-stu-id="87c8f-103">Create windowsWifiConfiguration</span></span>

> <span data-ttu-id="87c8f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="87c8f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="87c8f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="87c8f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="87c8f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="87c8f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="87c8f-107">Crear un nuevo objeto [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="87c8f-107">Create a new [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="87c8f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="87c8f-108">Prerequisites</span></span>
<span data-ttu-id="87c8f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="87c8f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="87c8f-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="87c8f-111">Permission type</span></span>|<span data-ttu-id="87c8f-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="87c8f-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="87c8f-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="87c8f-113">Delegated (work or school account)</span></span>|<span data-ttu-id="87c8f-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="87c8f-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="87c8f-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="87c8f-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="87c8f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="87c8f-116">Not supported.</span></span>|
|<span data-ttu-id="87c8f-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="87c8f-117">Application</span></span>|<span data-ttu-id="87c8f-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="87c8f-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="87c8f-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="87c8f-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="87c8f-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="87c8f-120">Request headers</span></span>
|<span data-ttu-id="87c8f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87c8f-121">Header</span></span>|<span data-ttu-id="87c8f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="87c8f-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="87c8f-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="87c8f-123">Authorization</span></span>|<span data-ttu-id="87c8f-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="87c8f-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="87c8f-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="87c8f-125">Accept</span></span>|<span data-ttu-id="87c8f-126">application/json</span><span class="sxs-lookup"><span data-stu-id="87c8f-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="87c8f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="87c8f-127">Request body</span></span>
<span data-ttu-id="87c8f-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto windowsWifiConfiguration.</span><span class="sxs-lookup"><span data-stu-id="87c8f-128">In the request body, supply a JSON representation for the windowsWifiConfiguration object.</span></span>

<span data-ttu-id="87c8f-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el windowsWifiConfiguration.</span><span class="sxs-lookup"><span data-stu-id="87c8f-129">The following table shows the properties that are required when you create the windowsWifiConfiguration.</span></span>

|<span data-ttu-id="87c8f-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="87c8f-130">Property</span></span>|<span data-ttu-id="87c8f-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="87c8f-131">Type</span></span>|<span data-ttu-id="87c8f-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="87c8f-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="87c8f-133">id</span><span class="sxs-lookup"><span data-stu-id="87c8f-133">id</span></span>|<span data-ttu-id="87c8f-134">String</span><span class="sxs-lookup"><span data-stu-id="87c8f-134">String</span></span>|<span data-ttu-id="87c8f-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="87c8f-135">Key of the entity.</span></span> <span data-ttu-id="87c8f-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="87c8f-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="87c8f-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="87c8f-137">lastModifiedDateTime</span></span>|<span data-ttu-id="87c8f-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="87c8f-138">DateTimeOffset</span></span>|<span data-ttu-id="87c8f-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="87c8f-139">DateTime the object was last modified.</span></span> <span data-ttu-id="87c8f-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="87c8f-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="87c8f-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="87c8f-141">roleScopeTagIds</span></span>|<span data-ttu-id="87c8f-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="87c8f-142">String collection</span></span>|<span data-ttu-id="87c8f-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="87c8f-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="87c8f-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="87c8f-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="87c8f-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="87c8f-145">supportsScopeTags</span></span>|<span data-ttu-id="87c8f-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="87c8f-146">Boolean</span></span>|<span data-ttu-id="87c8f-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="87c8f-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="87c8f-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="87c8f-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="87c8f-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="87c8f-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="87c8f-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="87c8f-150">This property is read-only.</span></span> <span data-ttu-id="87c8f-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="87c8f-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="87c8f-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="87c8f-152">createdDateTime</span></span>|<span data-ttu-id="87c8f-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="87c8f-153">DateTimeOffset</span></span>|<span data-ttu-id="87c8f-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="87c8f-154">DateTime the object was created.</span></span> <span data-ttu-id="87c8f-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="87c8f-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="87c8f-156">descripción</span><span class="sxs-lookup"><span data-stu-id="87c8f-156">description</span></span>|<span data-ttu-id="87c8f-157">String</span><span class="sxs-lookup"><span data-stu-id="87c8f-157">String</span></span>|<span data-ttu-id="87c8f-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="87c8f-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="87c8f-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="87c8f-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="87c8f-160">displayName</span><span class="sxs-lookup"><span data-stu-id="87c8f-160">displayName</span></span>|<span data-ttu-id="87c8f-161">String</span><span class="sxs-lookup"><span data-stu-id="87c8f-161">String</span></span>|<span data-ttu-id="87c8f-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="87c8f-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="87c8f-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="87c8f-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="87c8f-164">version</span><span class="sxs-lookup"><span data-stu-id="87c8f-164">version</span></span>|<span data-ttu-id="87c8f-165">Int32</span><span class="sxs-lookup"><span data-stu-id="87c8f-165">Int32</span></span>|<span data-ttu-id="87c8f-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="87c8f-166">Version of the device configuration.</span></span> <span data-ttu-id="87c8f-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="87c8f-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="87c8f-168">preSharedKey</span><span class="sxs-lookup"><span data-stu-id="87c8f-168">preSharedKey</span></span>|<span data-ttu-id="87c8f-169">String</span><span class="sxs-lookup"><span data-stu-id="87c8f-169">String</span></span>|<span data-ttu-id="87c8f-170">Ésta es la clave previamente compartida para la red Wi-Fi Personal WPA.</span><span class="sxs-lookup"><span data-stu-id="87c8f-170">This is the pre-shared key for WPA Personal Wi-Fi network.</span></span>|
|<span data-ttu-id="87c8f-171">wifiSecurityType</span><span class="sxs-lookup"><span data-stu-id="87c8f-171">wifiSecurityType</span></span>|[<span data-ttu-id="87c8f-172">wiFiSecurityType</span><span class="sxs-lookup"><span data-stu-id="87c8f-172">wiFiSecurityType</span></span>](../resources/intune-deviceconfig-wifisecuritytype.md)|<span data-ttu-id="87c8f-173">Especificar el tipo de seguridad Wifi.</span><span class="sxs-lookup"><span data-stu-id="87c8f-173">Specify the Wifi Security Type.</span></span> <span data-ttu-id="87c8f-174">Los valores posibles son: `open`, `wpaPersonal`, `wpaEnterprise`, `wep`, `wpa2Personal`, `wpa2Enterprise`.</span><span class="sxs-lookup"><span data-stu-id="87c8f-174">Possible values are: `open`, `wpaPersonal`, `wpaEnterprise`, `wep`, `wpa2Personal`, `wpa2Enterprise`.</span></span>|
|<span data-ttu-id="87c8f-175">meteredConnectionLimit</span><span class="sxs-lookup"><span data-stu-id="87c8f-175">meteredConnectionLimit</span></span>|[<span data-ttu-id="87c8f-176">meteredConnectionLimitType</span><span class="sxs-lookup"><span data-stu-id="87c8f-176">meteredConnectionLimitType</span></span>](../resources/intune-deviceconfig-meteredconnectionlimittype.md)|<span data-ttu-id="87c8f-177">Especificar el tipo de límite de conexión intencionadas para la conexión wifi.</span><span class="sxs-lookup"><span data-stu-id="87c8f-177">Specify the metered connection limit type for the wifi connection.</span></span> <span data-ttu-id="87c8f-178">Los valores posibles son: `unrestricted`, `fixed` y `variable`.</span><span class="sxs-lookup"><span data-stu-id="87c8f-178">Possible values are: `unrestricted`, `fixed`, `variable`.</span></span>|
|<span data-ttu-id="87c8f-179">SSID</span><span class="sxs-lookup"><span data-stu-id="87c8f-179">ssid</span></span>|<span data-ttu-id="87c8f-180">String</span><span class="sxs-lookup"><span data-stu-id="87c8f-180">String</span></span>|<span data-ttu-id="87c8f-181">Especifique el SSID de la conexión wifi.</span><span class="sxs-lookup"><span data-stu-id="87c8f-181">Specify the SSID of the wifi connection.</span></span>|
|<span data-ttu-id="87c8f-182">networkName</span><span class="sxs-lookup"><span data-stu-id="87c8f-182">networkName</span></span>|<span data-ttu-id="87c8f-183">String</span><span class="sxs-lookup"><span data-stu-id="87c8f-183">String</span></span>|<span data-ttu-id="87c8f-184">Especifique el nombre de la configuración de red.</span><span class="sxs-lookup"><span data-stu-id="87c8f-184">Specify the network configuration name.</span></span>|
|<span data-ttu-id="87c8f-185">connectAutomatically</span><span class="sxs-lookup"><span data-stu-id="87c8f-185">connectAutomatically</span></span>|<span data-ttu-id="87c8f-186">Booleano</span><span class="sxs-lookup"><span data-stu-id="87c8f-186">Boolean</span></span>|<span data-ttu-id="87c8f-187">Especifique si la conexión wifi debe conectarse automáticamente cuando en el rango.</span><span class="sxs-lookup"><span data-stu-id="87c8f-187">Specify whether the wifi connection should connect automatically when in range.</span></span>|
|<span data-ttu-id="87c8f-188">connectToPreferredNetwork</span><span class="sxs-lookup"><span data-stu-id="87c8f-188">connectToPreferredNetwork</span></span>|<span data-ttu-id="87c8f-189">Booleano</span><span class="sxs-lookup"><span data-stu-id="87c8f-189">Boolean</span></span>|<span data-ttu-id="87c8f-190">Especifique si la conexión wifi debe conectarse a redes más preferidas cuando ya está conectado a éste.</span><span class="sxs-lookup"><span data-stu-id="87c8f-190">Specify whether the wifi connection should connect to more preferred networks when already connected to this one.</span></span>  <span data-ttu-id="87c8f-191">Requiere ConnectAutomatically sea true.</span><span class="sxs-lookup"><span data-stu-id="87c8f-191">Requires ConnectAutomatically to be true.</span></span>|
|<span data-ttu-id="87c8f-192">connectWhenNetworkNameIsHidden</span><span class="sxs-lookup"><span data-stu-id="87c8f-192">connectWhenNetworkNameIsHidden</span></span>|<span data-ttu-id="87c8f-193">Booleano</span><span class="sxs-lookup"><span data-stu-id="87c8f-193">Boolean</span></span>|<span data-ttu-id="87c8f-194">Especifique si la conexión wifi debe conectarse automáticamente incluso cuando el SSID no sea de difusión.</span><span class="sxs-lookup"><span data-stu-id="87c8f-194">Specify whether the wifi connection should connect automatically even when the SSID is not broadcasting.</span></span>|
|<span data-ttu-id="87c8f-195">proxySetting</span><span class="sxs-lookup"><span data-stu-id="87c8f-195">proxySetting</span></span>|[<span data-ttu-id="87c8f-196">wiFiProxySetting</span><span class="sxs-lookup"><span data-stu-id="87c8f-196">wiFiProxySetting</span></span>](../resources/intune-deviceconfig-wifiproxysetting.md)|<span data-ttu-id="87c8f-197">Especificar la configuración para la configuración de Wi-Fi del proxy.</span><span class="sxs-lookup"><span data-stu-id="87c8f-197">Specify the proxy setting for Wi-Fi configuration.</span></span> <span data-ttu-id="87c8f-198">Los valores posibles son: `none`, `manual` y `automatic`.</span><span class="sxs-lookup"><span data-stu-id="87c8f-198">Possible values are: `none`, `manual`, `automatic`.</span></span>|
|<span data-ttu-id="87c8f-199">proxyManualAddress</span><span class="sxs-lookup"><span data-stu-id="87c8f-199">proxyManualAddress</span></span>|<span data-ttu-id="87c8f-200">String</span><span class="sxs-lookup"><span data-stu-id="87c8f-200">String</span></span>|<span data-ttu-id="87c8f-201">Especifique la dirección IP del servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="87c8f-201">Specify the IP address for the proxy server.</span></span>|
|<span data-ttu-id="87c8f-202">proxyManualPort</span><span class="sxs-lookup"><span data-stu-id="87c8f-202">proxyManualPort</span></span>|<span data-ttu-id="87c8f-203">Int32</span><span class="sxs-lookup"><span data-stu-id="87c8f-203">Int32</span></span>|<span data-ttu-id="87c8f-204">Especifique el puerto del servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="87c8f-204">Specify the port for the proxy server.</span></span>|
|<span data-ttu-id="87c8f-205">proxyAutomaticConfigurationUrl</span><span class="sxs-lookup"><span data-stu-id="87c8f-205">proxyAutomaticConfigurationUrl</span></span>|<span data-ttu-id="87c8f-206">String</span><span class="sxs-lookup"><span data-stu-id="87c8f-206">String</span></span>|<span data-ttu-id="87c8f-207">Especifique la dirección URL de la secuencia de comandos de configuración de servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="87c8f-207">Specify the URL for the proxy server configuration script.</span></span>|
|<span data-ttu-id="87c8f-208">forceFIPSCompliance</span><span class="sxs-lookup"><span data-stu-id="87c8f-208">forceFIPSCompliance</span></span>|<span data-ttu-id="87c8f-209">Booleano</span><span class="sxs-lookup"><span data-stu-id="87c8f-209">Boolean</span></span>|<span data-ttu-id="87c8f-210">Especifique si debe forzarse la compatibilidad con FIPS.</span><span class="sxs-lookup"><span data-stu-id="87c8f-210">Specify whether to force FIPS compliance.</span></span>|



## <a name="response"></a><span data-ttu-id="87c8f-211">Respuesta</span><span class="sxs-lookup"><span data-stu-id="87c8f-211">Response</span></span>
<span data-ttu-id="87c8f-212">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="87c8f-212">If successful, this method returns a `201 Created` response code and a [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="87c8f-213">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="87c8f-213">Example</span></span>
### <a name="request"></a><span data-ttu-id="87c8f-214">Solicitud</span><span class="sxs-lookup"><span data-stu-id="87c8f-214">Request</span></span>
<span data-ttu-id="87c8f-215">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="87c8f-215">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 850

{
  "@odata.type": "#microsoft.graph.windowsWifiConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "preSharedKey": "Pre Shared Key value",
  "wifiSecurityType": "wpaPersonal",
  "meteredConnectionLimit": "fixed",
  "ssid": "Ssid value",
  "networkName": "Network Name value",
  "connectAutomatically": true,
  "connectToPreferredNetwork": true,
  "connectWhenNetworkNameIsHidden": true,
  "proxySetting": "manual",
  "proxyManualAddress": "Proxy Manual Address value",
  "proxyManualPort": 15,
  "proxyAutomaticConfigurationUrl": "https://example.com/proxyAutomaticConfigurationUrl/",
  "forceFIPSCompliance": true
}
```

### <a name="response"></a><span data-ttu-id="87c8f-216">Respuesta</span><span class="sxs-lookup"><span data-stu-id="87c8f-216">Response</span></span>
<span data-ttu-id="87c8f-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="87c8f-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 958

{
  "@odata.type": "#microsoft.graph.windowsWifiConfiguration",
  "id": "8a9e790f-790f-8a9e-0f79-9e8a0f799e8a",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "preSharedKey": "Pre Shared Key value",
  "wifiSecurityType": "wpaPersonal",
  "meteredConnectionLimit": "fixed",
  "ssid": "Ssid value",
  "networkName": "Network Name value",
  "connectAutomatically": true,
  "connectToPreferredNetwork": true,
  "connectWhenNetworkNameIsHidden": true,
  "proxySetting": "manual",
  "proxyManualAddress": "Proxy Manual Address value",
  "proxyManualPort": 15,
  "proxyAutomaticConfigurationUrl": "https://example.com/proxyAutomaticConfigurationUrl/",
  "forceFIPSCompliance": true
}
```





