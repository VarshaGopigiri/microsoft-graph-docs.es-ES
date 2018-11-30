---
title: Crear macOSWiFiConfiguration
description: Crear un nuevo objeto macOSWiFiConfiguration.
ms.openlocfilehash: c0974fa16e89b514332303c1779663c5b7795619
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090816"
---
# <a name="create-macoswificonfiguration"></a><span data-ttu-id="63ddb-103">Crear macOSWiFiConfiguration</span><span class="sxs-lookup"><span data-stu-id="63ddb-103">Create macOSWiFiConfiguration</span></span>

> <span data-ttu-id="63ddb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="63ddb-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="63ddb-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="63ddb-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="63ddb-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="63ddb-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="63ddb-107">Crear un nuevo objeto [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="63ddb-107">Create a new [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="63ddb-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="63ddb-108">Prerequisites</span></span>
<span data-ttu-id="63ddb-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="63ddb-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="63ddb-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="63ddb-111">Permission type</span></span>|<span data-ttu-id="63ddb-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="63ddb-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="63ddb-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="63ddb-113">Delegated (work or school account)</span></span>|<span data-ttu-id="63ddb-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="63ddb-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="63ddb-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="63ddb-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="63ddb-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="63ddb-116">Not supported.</span></span>|
|<span data-ttu-id="63ddb-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="63ddb-117">Application</span></span>|<span data-ttu-id="63ddb-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="63ddb-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="63ddb-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="63ddb-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="63ddb-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="63ddb-120">Request headers</span></span>
|<span data-ttu-id="63ddb-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63ddb-121">Header</span></span>|<span data-ttu-id="63ddb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="63ddb-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="63ddb-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="63ddb-123">Authorization</span></span>|<span data-ttu-id="63ddb-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="63ddb-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="63ddb-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="63ddb-125">Accept</span></span>|<span data-ttu-id="63ddb-126">application/json</span><span class="sxs-lookup"><span data-stu-id="63ddb-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="63ddb-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="63ddb-127">Request body</span></span>
<span data-ttu-id="63ddb-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto macOSWiFiConfiguration.</span><span class="sxs-lookup"><span data-stu-id="63ddb-128">In the request body, supply a JSON representation for the macOSWiFiConfiguration object.</span></span>

<span data-ttu-id="63ddb-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el macOSWiFiConfiguration.</span><span class="sxs-lookup"><span data-stu-id="63ddb-129">The following table shows the properties that are required when you create the macOSWiFiConfiguration.</span></span>

|<span data-ttu-id="63ddb-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="63ddb-130">Property</span></span>|<span data-ttu-id="63ddb-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="63ddb-131">Type</span></span>|<span data-ttu-id="63ddb-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="63ddb-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="63ddb-133">id</span><span class="sxs-lookup"><span data-stu-id="63ddb-133">id</span></span>|<span data-ttu-id="63ddb-134">String</span><span class="sxs-lookup"><span data-stu-id="63ddb-134">String</span></span>|<span data-ttu-id="63ddb-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="63ddb-135">Key of the entity.</span></span> <span data-ttu-id="63ddb-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="63ddb-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="63ddb-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="63ddb-137">lastModifiedDateTime</span></span>|<span data-ttu-id="63ddb-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="63ddb-138">DateTimeOffset</span></span>|<span data-ttu-id="63ddb-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="63ddb-139">DateTime the object was last modified.</span></span> <span data-ttu-id="63ddb-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="63ddb-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="63ddb-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="63ddb-141">roleScopeTagIds</span></span>|<span data-ttu-id="63ddb-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="63ddb-142">String collection</span></span>|<span data-ttu-id="63ddb-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="63ddb-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="63ddb-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="63ddb-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="63ddb-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="63ddb-145">supportsScopeTags</span></span>|<span data-ttu-id="63ddb-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="63ddb-146">Boolean</span></span>|<span data-ttu-id="63ddb-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="63ddb-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="63ddb-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="63ddb-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="63ddb-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="63ddb-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="63ddb-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="63ddb-150">This property is read-only.</span></span> <span data-ttu-id="63ddb-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="63ddb-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="63ddb-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="63ddb-152">createdDateTime</span></span>|<span data-ttu-id="63ddb-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="63ddb-153">DateTimeOffset</span></span>|<span data-ttu-id="63ddb-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="63ddb-154">DateTime the object was created.</span></span> <span data-ttu-id="63ddb-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="63ddb-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="63ddb-156">descripción</span><span class="sxs-lookup"><span data-stu-id="63ddb-156">description</span></span>|<span data-ttu-id="63ddb-157">String</span><span class="sxs-lookup"><span data-stu-id="63ddb-157">String</span></span>|<span data-ttu-id="63ddb-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63ddb-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="63ddb-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="63ddb-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="63ddb-160">displayName</span><span class="sxs-lookup"><span data-stu-id="63ddb-160">displayName</span></span>|<span data-ttu-id="63ddb-161">String</span><span class="sxs-lookup"><span data-stu-id="63ddb-161">String</span></span>|<span data-ttu-id="63ddb-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63ddb-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="63ddb-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="63ddb-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="63ddb-164">version</span><span class="sxs-lookup"><span data-stu-id="63ddb-164">version</span></span>|<span data-ttu-id="63ddb-165">Int32</span><span class="sxs-lookup"><span data-stu-id="63ddb-165">Int32</span></span>|<span data-ttu-id="63ddb-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63ddb-166">Version of the device configuration.</span></span> <span data-ttu-id="63ddb-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="63ddb-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="63ddb-168">networkName</span><span class="sxs-lookup"><span data-stu-id="63ddb-168">networkName</span></span>|<span data-ttu-id="63ddb-169">String</span><span class="sxs-lookup"><span data-stu-id="63ddb-169">String</span></span>|<span data-ttu-id="63ddb-170">Nombre de red</span><span class="sxs-lookup"><span data-stu-id="63ddb-170">Network Name</span></span>|
|<span data-ttu-id="63ddb-171">SSID</span><span class="sxs-lookup"><span data-stu-id="63ddb-171">ssid</span></span>|<span data-ttu-id="63ddb-172">String</span><span class="sxs-lookup"><span data-stu-id="63ddb-172">String</span></span>|<span data-ttu-id="63ddb-173">Esto es el nombre de la red Wi-Fi que se difunde a todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="63ddb-173">This is the name of the Wi-Fi network that is broadcast to all devices.</span></span>|
|<span data-ttu-id="63ddb-174">connectAutomatically</span><span class="sxs-lookup"><span data-stu-id="63ddb-174">connectAutomatically</span></span>|<span data-ttu-id="63ddb-175">Booleano</span><span class="sxs-lookup"><span data-stu-id="63ddb-175">Boolean</span></span>|<span data-ttu-id="63ddb-176">Conectar automáticamente cuando esta red esté en el intervalo.</span><span class="sxs-lookup"><span data-stu-id="63ddb-176">Connect automatically when this network is in range.</span></span> <span data-ttu-id="63ddb-177">Si se establece en true omitirá el símbolo del sistema del usuario y el dispositivo se conecte automáticamente a la red Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="63ddb-177">Setting this to true will skip the user prompt and automatically connect the device to Wi-Fi network.</span></span>|
|<span data-ttu-id="63ddb-178">connectWhenNetworkNameIsHidden</span><span class="sxs-lookup"><span data-stu-id="63ddb-178">connectWhenNetworkNameIsHidden</span></span>|<span data-ttu-id="63ddb-179">Booleano</span><span class="sxs-lookup"><span data-stu-id="63ddb-179">Boolean</span></span>|<span data-ttu-id="63ddb-180">Conectar cuando la red no sea de difusión su nombre (SSID).</span><span class="sxs-lookup"><span data-stu-id="63ddb-180">Connect when the network is not broadcasting its name (SSID).</span></span> <span data-ttu-id="63ddb-181">Cuando se establece en true, este perfil fuerza el dispositivo para conectarse a una red que no difundir su SSID para todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="63ddb-181">When set to true, this profile forces the device to connect to a network that doesn't broadcast its SSID to all devices.</span></span>|
|<span data-ttu-id="63ddb-182">wiFiSecurityType</span><span class="sxs-lookup"><span data-stu-id="63ddb-182">wiFiSecurityType</span></span>|[<span data-ttu-id="63ddb-183">wiFiSecurityType</span><span class="sxs-lookup"><span data-stu-id="63ddb-183">wiFiSecurityType</span></span>](../resources/intune-deviceconfig-wifisecuritytype.md)|<span data-ttu-id="63ddb-184">Indica si el extremo de Wi-Fi utiliza un tipo de EAP en función de seguridad.</span><span class="sxs-lookup"><span data-stu-id="63ddb-184">Indicates whether Wi-Fi endpoint uses an EAP based security type.</span></span> <span data-ttu-id="63ddb-185">Los valores posibles son: `open`, `wpaPersonal`, `wpaEnterprise`, `wep`, `wpa2Personal`, `wpa2Enterprise`.</span><span class="sxs-lookup"><span data-stu-id="63ddb-185">Possible values are: `open`, `wpaPersonal`, `wpaEnterprise`, `wep`, `wpa2Personal`, `wpa2Enterprise`.</span></span>|
|<span data-ttu-id="63ddb-186">proxySettings</span><span class="sxs-lookup"><span data-stu-id="63ddb-186">proxySettings</span></span>|[<span data-ttu-id="63ddb-187">wiFiProxySetting</span><span class="sxs-lookup"><span data-stu-id="63ddb-187">wiFiProxySetting</span></span>](../resources/intune-deviceconfig-wifiproxysetting.md)|<span data-ttu-id="63ddb-188">Tipo de proxy para esta conexión Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="63ddb-188">Proxy Type for this Wi-Fi connection.</span></span> <span data-ttu-id="63ddb-189">Los valores posibles son: `none`, `manual` y `automatic`.</span><span class="sxs-lookup"><span data-stu-id="63ddb-189">Possible values are: `none`, `manual`, `automatic`.</span></span>|
|<span data-ttu-id="63ddb-190">proxyManualAddress</span><span class="sxs-lookup"><span data-stu-id="63ddb-190">proxyManualAddress</span></span>|<span data-ttu-id="63ddb-191">String</span><span class="sxs-lookup"><span data-stu-id="63ddb-191">String</span></span>|<span data-ttu-id="63ddb-192">Nombre de host DNS o dirección IP del servidor proxy cuando se selecciona la configuración manual.</span><span class="sxs-lookup"><span data-stu-id="63ddb-192">IP Address or DNS hostname of the proxy server when manual configuration is selected.</span></span>|
|<span data-ttu-id="63ddb-193">proxyManualPort</span><span class="sxs-lookup"><span data-stu-id="63ddb-193">proxyManualPort</span></span>|<span data-ttu-id="63ddb-194">Int32</span><span class="sxs-lookup"><span data-stu-id="63ddb-194">Int32</span></span>|<span data-ttu-id="63ddb-195">Puerto del servidor proxy cuando se selecciona la configuración manual.</span><span class="sxs-lookup"><span data-stu-id="63ddb-195">Port of the proxy server when manual configuration is selected.</span></span>|
|<span data-ttu-id="63ddb-196">proxyAutomaticConfigurationUrl</span><span class="sxs-lookup"><span data-stu-id="63ddb-196">proxyAutomaticConfigurationUrl</span></span>|<span data-ttu-id="63ddb-197">String</span><span class="sxs-lookup"><span data-stu-id="63ddb-197">String</span></span>|<span data-ttu-id="63ddb-198">URL de la secuencia de la configuración automática de servidor proxy cuando se selecciona la configuración automática.</span><span class="sxs-lookup"><span data-stu-id="63ddb-198">URL of the proxy server automatic configuration script when automatic configuration is selected.</span></span> <span data-ttu-id="63ddb-199">Normalmente, esta dirección URL es la ubicación del archivo PAC (configuración automática de Proxy).</span><span class="sxs-lookup"><span data-stu-id="63ddb-199">This URL is typically the location of PAC (Proxy Auto Configuration) file.</span></span>|
|<span data-ttu-id="63ddb-200">preSharedKey</span><span class="sxs-lookup"><span data-stu-id="63ddb-200">preSharedKey</span></span>|<span data-ttu-id="63ddb-201">String</span><span class="sxs-lookup"><span data-stu-id="63ddb-201">String</span></span>|<span data-ttu-id="63ddb-202">Ésta es la clave previamente compartida para la red Wi-Fi Personal WPA.</span><span class="sxs-lookup"><span data-stu-id="63ddb-202">This is the pre-shared key for WPA Personal Wi-Fi network.</span></span>|



## <a name="response"></a><span data-ttu-id="63ddb-203">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63ddb-203">Response</span></span>
<span data-ttu-id="63ddb-204">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63ddb-204">If successful, this method returns a `201 Created` response code and a [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="63ddb-205">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="63ddb-205">Example</span></span>
### <a name="request"></a><span data-ttu-id="63ddb-206">Solicitud</span><span class="sxs-lookup"><span data-stu-id="63ddb-206">Request</span></span>
<span data-ttu-id="63ddb-207">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63ddb-207">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 741

{
  "@odata.type": "#microsoft.graph.macOSWiFiConfiguration",
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

### <a name="response"></a><span data-ttu-id="63ddb-208">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63ddb-208">Response</span></span>
<span data-ttu-id="63ddb-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="63ddb-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 849

{
  "@odata.type": "#microsoft.graph.macOSWiFiConfiguration",
  "id": "471203fb-03fb-4712-fb03-1247fb031247",
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





