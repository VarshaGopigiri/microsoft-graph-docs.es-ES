---
title: Crear iosWiFiConfiguration
description: Crear un nuevo objeto iosWiFiConfiguration.
author: tfitzmac
ms.openlocfilehash: 0e16c9ed6877977ff0e0b6c3c5c4e21597934130
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27362254"
---
# <a name="create-ioswificonfiguration"></a><span data-ttu-id="77955-103">Crear iosWiFiConfiguration</span><span class="sxs-lookup"><span data-stu-id="77955-103">Create iosWiFiConfiguration</span></span>

> <span data-ttu-id="77955-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="77955-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="77955-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="77955-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="77955-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="77955-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="77955-107">Crear un nuevo objeto [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="77955-107">Create a new [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="77955-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="77955-108">Prerequisites</span></span>
<span data-ttu-id="77955-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="77955-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="77955-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="77955-111">Permission type</span></span>|<span data-ttu-id="77955-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="77955-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="77955-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="77955-113">Delegated (work or school account)</span></span>|<span data-ttu-id="77955-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="77955-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="77955-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="77955-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="77955-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="77955-116">Not supported.</span></span>|
|<span data-ttu-id="77955-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="77955-117">Application</span></span>|<span data-ttu-id="77955-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="77955-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="77955-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="77955-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="77955-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="77955-120">Request headers</span></span>
|<span data-ttu-id="77955-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="77955-121">Header</span></span>|<span data-ttu-id="77955-122">Valor</span><span class="sxs-lookup"><span data-stu-id="77955-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="77955-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="77955-123">Authorization</span></span>|<span data-ttu-id="77955-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="77955-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="77955-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="77955-125">Accept</span></span>|<span data-ttu-id="77955-126">application/json</span><span class="sxs-lookup"><span data-stu-id="77955-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="77955-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="77955-127">Request body</span></span>
<span data-ttu-id="77955-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto iosWiFiConfiguration.</span><span class="sxs-lookup"><span data-stu-id="77955-128">In the request body, supply a JSON representation for the iosWiFiConfiguration object.</span></span>

<span data-ttu-id="77955-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el iosWiFiConfiguration.</span><span class="sxs-lookup"><span data-stu-id="77955-129">The following table shows the properties that are required when you create the iosWiFiConfiguration.</span></span>

|<span data-ttu-id="77955-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="77955-130">Property</span></span>|<span data-ttu-id="77955-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="77955-131">Type</span></span>|<span data-ttu-id="77955-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="77955-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="77955-133">id</span><span class="sxs-lookup"><span data-stu-id="77955-133">id</span></span>|<span data-ttu-id="77955-134">String</span><span class="sxs-lookup"><span data-stu-id="77955-134">String</span></span>|<span data-ttu-id="77955-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="77955-135">Key of the entity.</span></span> <span data-ttu-id="77955-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="77955-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="77955-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="77955-137">lastModifiedDateTime</span></span>|<span data-ttu-id="77955-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="77955-138">DateTimeOffset</span></span>|<span data-ttu-id="77955-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="77955-139">DateTime the object was last modified.</span></span> <span data-ttu-id="77955-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="77955-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="77955-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="77955-141">roleScopeTagIds</span></span>|<span data-ttu-id="77955-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="77955-142">String collection</span></span>|<span data-ttu-id="77955-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="77955-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="77955-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="77955-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="77955-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="77955-145">supportsScopeTags</span></span>|<span data-ttu-id="77955-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="77955-146">Boolean</span></span>|<span data-ttu-id="77955-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="77955-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="77955-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="77955-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="77955-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="77955-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="77955-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="77955-150">This property is read-only.</span></span> <span data-ttu-id="77955-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="77955-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="77955-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="77955-152">createdDateTime</span></span>|<span data-ttu-id="77955-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="77955-153">DateTimeOffset</span></span>|<span data-ttu-id="77955-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="77955-154">DateTime the object was created.</span></span> <span data-ttu-id="77955-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="77955-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="77955-156">descripción</span><span class="sxs-lookup"><span data-stu-id="77955-156">description</span></span>|<span data-ttu-id="77955-157">String</span><span class="sxs-lookup"><span data-stu-id="77955-157">String</span></span>|<span data-ttu-id="77955-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="77955-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="77955-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="77955-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="77955-160">displayName</span><span class="sxs-lookup"><span data-stu-id="77955-160">displayName</span></span>|<span data-ttu-id="77955-161">String</span><span class="sxs-lookup"><span data-stu-id="77955-161">String</span></span>|<span data-ttu-id="77955-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="77955-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="77955-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="77955-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="77955-164">version</span><span class="sxs-lookup"><span data-stu-id="77955-164">version</span></span>|<span data-ttu-id="77955-165">Int32</span><span class="sxs-lookup"><span data-stu-id="77955-165">Int32</span></span>|<span data-ttu-id="77955-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="77955-166">Version of the device configuration.</span></span> <span data-ttu-id="77955-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="77955-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="77955-168">networkName</span><span class="sxs-lookup"><span data-stu-id="77955-168">networkName</span></span>|<span data-ttu-id="77955-169">String</span><span class="sxs-lookup"><span data-stu-id="77955-169">String</span></span>|<span data-ttu-id="77955-170">Nombre de red</span><span class="sxs-lookup"><span data-stu-id="77955-170">Network Name</span></span>|
|<span data-ttu-id="77955-171">SSID</span><span class="sxs-lookup"><span data-stu-id="77955-171">ssid</span></span>|<span data-ttu-id="77955-172">String</span><span class="sxs-lookup"><span data-stu-id="77955-172">String</span></span>|<span data-ttu-id="77955-173">Esto es el nombre de la red Wi-Fi que se difunde a todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="77955-173">This is the name of the Wi-Fi network that is broadcast to all devices.</span></span>|
|<span data-ttu-id="77955-174">connectAutomatically</span><span class="sxs-lookup"><span data-stu-id="77955-174">connectAutomatically</span></span>|<span data-ttu-id="77955-175">Boolean</span><span class="sxs-lookup"><span data-stu-id="77955-175">Boolean</span></span>|<span data-ttu-id="77955-176">Conectar automáticamente cuando esta red esté en el intervalo.</span><span class="sxs-lookup"><span data-stu-id="77955-176">Connect automatically when this network is in range.</span></span> <span data-ttu-id="77955-177">Si se establece en true omitirá el símbolo del sistema del usuario y el dispositivo se conecte automáticamente a la red Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="77955-177">Setting this to true will skip the user prompt and automatically connect the device to Wi-Fi network.</span></span>|
|<span data-ttu-id="77955-178">connectWhenNetworkNameIsHidden</span><span class="sxs-lookup"><span data-stu-id="77955-178">connectWhenNetworkNameIsHidden</span></span>|<span data-ttu-id="77955-179">Boolean</span><span class="sxs-lookup"><span data-stu-id="77955-179">Boolean</span></span>|<span data-ttu-id="77955-180">Conectar cuando la red no sea de difusión su nombre (SSID).</span><span class="sxs-lookup"><span data-stu-id="77955-180">Connect when the network is not broadcasting its name (SSID).</span></span> <span data-ttu-id="77955-181">Cuando se establece en true, este perfil fuerza el dispositivo para conectarse a una red que no difundir su SSID para todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="77955-181">When set to true, this profile forces the device to connect to a network that doesn't broadcast its SSID to all devices.</span></span>|
|<span data-ttu-id="77955-182">wiFiSecurityType</span><span class="sxs-lookup"><span data-stu-id="77955-182">wiFiSecurityType</span></span>|[<span data-ttu-id="77955-183">wiFiSecurityType</span><span class="sxs-lookup"><span data-stu-id="77955-183">wiFiSecurityType</span></span>](../resources/intune-deviceconfig-wifisecuritytype.md)|<span data-ttu-id="77955-184">Indica si el extremo de Wi-Fi utiliza un tipo de EAP en función de seguridad.</span><span class="sxs-lookup"><span data-stu-id="77955-184">Indicates whether Wi-Fi endpoint uses an EAP based security type.</span></span> <span data-ttu-id="77955-185">Los valores posibles son: `open`, `wpaPersonal`, `wpaEnterprise`, `wep`, `wpa2Personal`, `wpa2Enterprise`.</span><span class="sxs-lookup"><span data-stu-id="77955-185">Possible values are: `open`, `wpaPersonal`, `wpaEnterprise`, `wep`, `wpa2Personal`, `wpa2Enterprise`.</span></span>|
|<span data-ttu-id="77955-186">proxySettings</span><span class="sxs-lookup"><span data-stu-id="77955-186">proxySettings</span></span>|[<span data-ttu-id="77955-187">wiFiProxySetting</span><span class="sxs-lookup"><span data-stu-id="77955-187">wiFiProxySetting</span></span>](../resources/intune-deviceconfig-wifiproxysetting.md)|<span data-ttu-id="77955-188">Tipo de proxy para esta conexión Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="77955-188">Proxy Type for this Wi-Fi connection.</span></span> <span data-ttu-id="77955-189">Los valores posibles son: `none`, `manual` y `automatic`.</span><span class="sxs-lookup"><span data-stu-id="77955-189">Possible values are: `none`, `manual`, `automatic`.</span></span>|
|<span data-ttu-id="77955-190">proxyManualAddress</span><span class="sxs-lookup"><span data-stu-id="77955-190">proxyManualAddress</span></span>|<span data-ttu-id="77955-191">String</span><span class="sxs-lookup"><span data-stu-id="77955-191">String</span></span>|<span data-ttu-id="77955-192">Nombre de host DNS o dirección IP del servidor proxy cuando se selecciona la configuración manual.</span><span class="sxs-lookup"><span data-stu-id="77955-192">IP Address or DNS hostname of the proxy server when manual configuration is selected.</span></span>|
|<span data-ttu-id="77955-193">proxyManualPort</span><span class="sxs-lookup"><span data-stu-id="77955-193">proxyManualPort</span></span>|<span data-ttu-id="77955-194">Int32</span><span class="sxs-lookup"><span data-stu-id="77955-194">Int32</span></span>|<span data-ttu-id="77955-195">Puerto del servidor proxy cuando se selecciona la configuración manual.</span><span class="sxs-lookup"><span data-stu-id="77955-195">Port of the proxy server when manual configuration is selected.</span></span>|
|<span data-ttu-id="77955-196">proxyAutomaticConfigurationUrl</span><span class="sxs-lookup"><span data-stu-id="77955-196">proxyAutomaticConfigurationUrl</span></span>|<span data-ttu-id="77955-197">String</span><span class="sxs-lookup"><span data-stu-id="77955-197">String</span></span>|<span data-ttu-id="77955-198">URL de la secuencia de la configuración automática de servidor proxy cuando se selecciona la configuración automática.</span><span class="sxs-lookup"><span data-stu-id="77955-198">URL of the proxy server automatic configuration script when automatic configuration is selected.</span></span> <span data-ttu-id="77955-199">Normalmente, esta dirección URL es la ubicación del archivo PAC (configuración automática de Proxy).</span><span class="sxs-lookup"><span data-stu-id="77955-199">This URL is typically the location of PAC (Proxy Auto Configuration) file.</span></span>|
|<span data-ttu-id="77955-200">preSharedKey</span><span class="sxs-lookup"><span data-stu-id="77955-200">preSharedKey</span></span>|<span data-ttu-id="77955-201">String</span><span class="sxs-lookup"><span data-stu-id="77955-201">String</span></span>|<span data-ttu-id="77955-202">Ésta es la clave previamente compartida para la red Wi-Fi Personal WPA.</span><span class="sxs-lookup"><span data-stu-id="77955-202">This is the pre-shared key for WPA Personal Wi-Fi network.</span></span>|



## <a name="response"></a><span data-ttu-id="77955-203">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77955-203">Response</span></span>
<span data-ttu-id="77955-204">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77955-204">If successful, this method returns a `201 Created` response code and a [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="77955-205">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="77955-205">Example</span></span>
### <a name="request"></a><span data-ttu-id="77955-206">Solicitud</span><span class="sxs-lookup"><span data-stu-id="77955-206">Request</span></span>
<span data-ttu-id="77955-207">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="77955-207">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 739

{
  "@odata.type": "#microsoft.graph.iosWiFiConfiguration",
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
  "preSharedKey": "Pre Shared Key value"
}
```

### <a name="response"></a><span data-ttu-id="77955-208">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77955-208">Response</span></span>
<span data-ttu-id="77955-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="77955-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 847

{
  "@odata.type": "#microsoft.graph.iosWiFiConfiguration",
  "id": "516f9ef9-9ef9-516f-f99e-6f51f99e6f51",
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
  "preSharedKey": "Pre Shared Key value"
}
```





